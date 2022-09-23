---
title: Integrācijas žurnāls risinājumā Project Operations
description: Šajā rakstā ir sniegta informācija par darbu ar integrācijas žurnālu programmā Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541087"
---
# <a name="integration-journal-in-project-operations"></a>Integrācijas žurnāls risinājumā Project Operations

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Laiks, izdevumi, maksa un materiālie ieraksti rada **Faktiskās transakcijas**, kas atspoguļo darbības skatu uz darbu, kas pabeigts pret projektu. Dynamics 365 Project Operations nodrošina grāmatvežus ar rīku, lai pārskatītu transakcijas un vajadzības gadījumā pielāgotu uzskaites atribūtus. Kad pārskatīšana un pielāgojumi ir pabeigti, darbības tiek grāmatotas Projekta apakšgrāmatā un Virsgrāmatā. Grāmatvedis var veikt šīs darbības, izmantojot žurnālu **Project Operations Integration** (**Dynamics 365 Finance** > **Project management and accounting** > **Journals Project Operations Integration** > **žurnālu**.

![Integrācijas žurnāla plūsma.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Ierakstu izveide Project Operations integrācijas žurnālā

Ieraksti Project Operations integrācijas žurnālā tiek izveidoti, izmantojot periodisku procesu **Importēšana no Izstādīšanas tabulas**. Šo procesu var palaist, dodoties uz **Dynamics 365 Finance** > **Project pārvaldība un grāmatvedība** > **Periodiska** > **projekta operāciju integrācija** > **Importēšana no inscenēšanas tabulas**. Procesu var izpildīt interaktīvi vai pēc nepieciešamības konfigurēt procesu, lai tas tiktu izpildīts fonā.

Veicot periodisku procesu, tiek atrasti visi faktiskie dati, kas vēl nav pievienoti Project Operations integrācijas žurnālam. Tiek izveidota žurnāla rinda katrai faktiskajai darbībai.
Sistēma grupē žurnāla rindas atsevišķos žurnālos, pamatojoties uz vērtību, kas atlasīta žurnāla lauka **Project Operations Integration (** Finance **Project management and accounting Setup Project management and accounting** > **Setup** > **Project management and accounting parameters** > **,** Project Operations on Dynamics 365 Customer Engagement **tab) atlasīto** vērtību. Šī lauka iespējamās vērtības ir šādas:

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
    - Ja **kategorija Transakcija nav iestatīta projekta faktiskajā, sistēma izmanto vērtību** laukā Projekta kategorijas noklusējumi cilnē **Projekta** operācijas Dynamics 365 Customer Engagement **lapas Projekta vadības un uzskaites** parametri cilnē Projekta vadība un uzskaites parametri **.**
  - Lauks **Resursi** norāda ar šo transakciju saistīto projekta resursu. Resurss tiek izmantots kā atsauce projekta rēķina priekšlikumos klientiem.
  - Lauks **Valūtas kurss** pēc noklusējuma tiek izmantots valūtas **maiņas kursā**, kas iestatīts Dynamics 365 Finance. Ja nav maiņas kursa iestatījuma, periodiskais process **Importēšana no izstādīšanas** nepievienos šo ieraksta žurnālā, un darba izpildes žurnālā tiks pievienots kļūdas ziņojums.
  - Lauks **Rindas rekvizīts** apzīmē norēķinu tipu projekta faktiskajos datos. Rindas rekvizītu un norēķinu tipu kartēšana ir definēta **lapas Projektu vadības un uzskaites parametri** cilnē **Projekta operācijas Dynamics 365 Customer Engagement**.

Project Operations integrācijas žurnāla rindās var atjaunināt tikai šādus uzskaites atribūtus:

- **Rēķinu PVN grupa** un **Rēķina vienuma PVN grupa**
- **Finanšu dimensijas** (izmantojot darbību **Sadalīt summas**)

Integrācijas žurnāla rindas var izdzēst. Tomēr visas nepublicētās rindas tiks atkal ievietotas žurnālā pēc tam, kad būsit atkārtoti palaidis **importēšanas periodisko** procesu.

### <a name="post-the-project-operations-integration-journal"></a>Projekta operāciju integrācijas žurnāla publicēšana

Kad tiek grāmatots integrācijas žurnāls, tiek izveidotas projekta apakšgrāmatas un virsgrāmatas darbības. Tās izmanto pakārtotā klienta rēķina izrakstīšanai, ieņēmumu atzīšanai un finanšu atskaišu izveidei.

Atlasīto Project Operations integrācijas žurnālu var publicēt, izmantojot **opciju Post** Project Operations integrācijas žurnāla lapā. Visus žurnālus var automātiski grāmatot, palaižot procesu periodisko projektu operāciju integrācijas žurnālā **Post Project Operations** > **.** > **·**

Publicēšanu var veikt interaktīvi vai partijā. Ņemiet vērā, ka visi žurnāli, kuros ir vairāk nekā 100 rindiņu, tiks automātiski publicēti partijā. Lai nodrošinātu labāku veiktspēju, ja žurnāli, kuros ir daudz rindu, tiek grāmatoti paketē, iespējojiet **integrācijas žurnālu Post Project Operations, izmantojot vairākus pakešizdevumus** darbvietā **Līdzekļu pārvaldība**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Pārsūtiet visas rindas, kurās ir publicēšanas kļūdas, uz jaunu žurnālu

> [!NOTE]
> Lai izmantotu šo iespēju, iespējojiet opciju **Pārsūtīt visas rindas ar grāmatošanas kļūdām uz jaunu Project Operations integrācijas žurnāla** līdzekli līdzekļu pārvaldības darbvietā **Līdzekļu pārvaldība**.

Šis līdzeklis palīdz uzlabot pieredzi ar Project Operations integrācijas žurnālu. Kad tas ir iespējots, dubultās rakstīšanas laika problēmas un iestatīšanas problēmas vairs neliedz publicēt derīgus žurnālus. Publicējot project operations integrācijas žurnālā, sistēma validē katru rindu žurnālā. Tas publicē visas rindas, kurās nav kļūdu, un izveido jaunu žurnālu visām rindām, kurās ir publicēšanas kļūdas.

Lai pārskatītu žurnālus, kuros ir grāmatošanas kļūdu rindas, dodieties uz **projektu vadības un uzskaites** \> **žurnālu projektu operāciju integrācijas** \> **žurnālu** un filtrējiet žurnālu sarakstu, izmantojot **lauku Sākotnējais žurnāls.** Nākamajā attēlā ir parādīts piemērs, kur žurnāli projekta operāciju integrācijas **žurnāla** lapā ir filtrēti šādā veidā.

![Oriģinālais žurnāls, kas tiek rādīts Project Operations integrācijas žurnāla lapā.](./media/transferLines-originalJournal.png)

Ja periodisks pakešdarbs ir konfigurēts integrācijas žurnāla publicēšanai, grāmatošana tiks pievienota atkārtoti, un žurnāli tiks publicēti, ja laika problēma ir novērsta. Visi atlikušie žurnāli ir jāizpēta manuāli, pārskatot žurnālus un veicot visas nepieciešamās darbības.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
