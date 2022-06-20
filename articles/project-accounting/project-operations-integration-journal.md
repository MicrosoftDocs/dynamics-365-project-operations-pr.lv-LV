---
title: Integrācijas žurnāls risinājumā Project Operations
description: Šajā rakstā ir sniegta informācija par darbu ar integrācijas žurnālu projektu operācijās.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: befb1756ad77708805f3cbb06168b93e44296df0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923887"
---
# <a name="integration-journal-in-project-operations"></a>Integrācijas žurnāls risinājumā Project Operations

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Laika un izdevumu ieraksti veido **Faktiskās** transakcijas, kas atspoguļo projekta pabeigto darbu operatīvo skatu. Dynamics 365 Project Operations nodrošina grāmatvežus ar rīku, lai pārskatītu transakcijas un vajadzības gadījumā pielāgotu uzskaites atribūtus. Kad pārskatīšana un pielāgojumi ir pabeigti, darbības tiek grāmatotas Projekta apakšgrāmatā un Virsgrāmatā. Grāmatvedis var veikt šīs darbības, **izmantojot projektu operāciju integrācijas** žurnālu(**Dynamics 365 Finance** > **Projektu vadības un grāmatvedības** > **žurnālu** > **projektu operāciju integrācijas** žurnālu.

![Integrācijas žurnāla plūsma.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Ierakstu izveide Project Operations integrācijas žurnālā

Ieraksti Project Operations integrācijas žurnālā tiek izveidoti, izmantojot periodisku procesu **Importēšana no Izstādīšanas tabulas**. Šo procesu var palaist, dodoties uz **Dynamics 365 Finance** > **Projektu vadība un grāmatvedība** > **Periodisko** > **projektu operāciju integrācijas** > **importēšana no sagatavošanas tabulas**. Procesu var izpildīt interaktīvi vai pēc nepieciešamības konfigurēt procesu, lai tas tiktu izpildīts fonā.

Veicot periodisku procesu, tiek atrasti visi faktiskie dati, kas vēl nav pievienoti Project Operations integrācijas žurnālam. Tiek izveidota žurnāla rinda katrai faktiskajai darbībai.
Sistēma grupē žurnāla rindas atsevišķos žurnālos, pamatojoties uz vērtību, kas atlasīta **žurnāla** laukā Projektu operāciju integrācija atlasītā perioda vienība (**Finance** > **Project management and accounting** > **Setup** > **Project management and accounting parameters**, **Project Operations on Dynamics 365 Customer Engagement** tab). Šī lauka iespējamās vērtības ir šādas:

  - **Dienas**: faktiskie dati ir grupēti pēc darbības datuma. Katrai dienai tiek izveidots atsevišķs žurnāls.
  - **Mēneši**: faktiskie dati ir grupēti pēc kalendāra mēneša. Katram mēnesim tiek izveidots atsevišķs žurnāls.
  - **Gadi**: faktiskie dati ir grupēti pēc kalendāra gada. Katram gadam tiek izveidots atsevišķs žurnāls.
  - **Visi**: vienā integrācijas žurnālā tiek iekļauti visi faktiskie darījumi. Ja pēc periodiskā procesa izpildes žurnāls nav pieejams, piemēram, ja žurnāls ir darījumu grāmatošanas procesā, tiek izveidots jauns žurnāls.

Žurnāla rindas tiek veidotas, pamatojoties uz projekta faktiskajiem ierakstiem. Tālāk sniegtajā sarakstā ir iekļautas dažas svarīgākās noklusējuma un transformācijas kārtulas:

  - Katram projekta faktiskajam darījumam ir rinda Project Operations integrācijas žurnālā. Izmaksas un rēķinos neiekļautie pārdošanas darījumi attiecībā uz laika un materiālu norēķinu tipu tiek rādīti atsevišķās rindās.
  - Lauks **Datums** norāda darījuma datumu. Lauks **Uzskaites datums** norāda datumu, kurā darbība tika ierakstīta Virsgrāmatā. Ja uzskaites datums ir [slēgtā finanšu periodā](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) un parametrs **Automātiski iestatīt grāmatvedības datumu uz atvērtās virsgrāmatas periodu** tiek iestatīts lapas **Projekta pārvaldības un uzskaites parametri** cilnē **Finanses**, sistēma darījuma uzskaites datumu pielāgos pirmajam datumam nākamajā atvērtā Virsgrāmatas periodā.
  - Lauks **Dokuments** rāda dokumenta numuru visām faktiskajām transakcijām. Dokumentu numuru sērija ir definēta cilnē **Numuru sērijas**, kas atrodas lapā **Projektu pārvaldības un uzskaites parametri**. Katrai rindai tiek piešķirts jauns numurs. Pēc tam kad dokuments ir iegrāmatots, varat skatīt, kā izmaksas un rēķinos neiekļautie pārdošanas darījumi ir saistīti, atlasot **Saistītos dokumentus** lapā **Dokumentu darbības**.
  - Lauks **Kategorija** atspoguļo projekta transakciju un noklusējuma vērtības, pamatojoties uz saistīto projekta faktisko datu kategoriju.
    - Ja **Darbību kategorija** ir iestatīta projekta faktiskajos datos un dotajā juridiskajā entītijā pastāv saistītā **Projekta kategorija**, kategorijas noklusējums ir šī projekta kategorija.
    - Ja **darbību kategorija** nav iestatīta projektā faktiskais, sistēma izmanto vērtību **laukā** Projekta kategorijas noklusējumi **lapas Projekta vadība un uzskaites parametri** cilnē **Projekta operācijas Dynamics 365 Customer Engagement**.
  - Lauks **Resursi** norāda ar šo transakciju saistīto projekta resursu. Resurss tiek izmantots kā atsauce projekta rēķina priekšlikumos klientiem.
  - Lauks **Valūtas kurss** noklusē **no valūtas kursa**, kas iestatīts Dynamics 365 Finance. Ja nav maiņas kursa iestatījuma, periodiskais process **Importēšana no izstādīšanas** nepievienos šo ieraksta žurnālā, un darba izpildes žurnālā tiks pievienots kļūdas ziņojums.
  - Lauks **Rindas rekvizīts** apzīmē norēķinu tipu projekta faktiskajos datos. Rindas rekvizīts un norēķinu tipa kartējums ir definēti **lapas Projekta vadības un uzskaites parametri** cilnē **Projekta operācijas Dynamics 365 Customer Engagement**.

Project Operations integrācijas žurnāla rindās var atjaunināt tikai šādus uzskaites atribūtus:

- **Rēķinu PVN grupa** un **Rēķina vienuma PVN grupa**
- **Finanšu dimensijas** (izmantojot darbību **Sadalīt summas**)

Integrācijas žurnāla rindas var dzēst, tomēr visas neiegrāmatotās rindas tiks ievietotas žurnālā vēlreiz pēc tam, kad atkārtoti palaidīsit periodisko procesu **Importēšana no izstādīšanas**.

Kad tiek grāmatots integrācijas žurnāls, tiek izveidotas projekta apakšgrāmatas un virsgrāmatas darbības. Tās izmanto pakārtotā klienta rēķina izrakstīšanai, ieņēmumu atzīšanai un finanšu atskaišu izveidei.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
