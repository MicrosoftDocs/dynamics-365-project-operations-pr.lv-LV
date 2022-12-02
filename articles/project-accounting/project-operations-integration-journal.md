---
title: Integrācijas žurnāls risinājumā Project Operations
description: Šajā rakstā ir sniegta informācija par darbu ar integrācijas žurnālu risinājumā Project Operations.
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

Laika, izdevumu, maksu un materiālu ieraksti veido **Faktiskās** transakcijas, kas atspoguļo projekta pabeigto darbu operatīvo skatu. Dynamics 365 Project Operations nodrošina grāmatvežus ar rīku, lai pārskatītu transakcijas un vajadzības gadījumā pielāgotu uzskaites atribūtus. Kad pārskatīšana un pielāgojumi ir pabeigti, darbības tiek grāmatotas Projekta apakšgrāmatā un Virsgrāmatā. Grāmatvedis var veikt šīs darbības, izmantojot žurnālu **Project Operations integrācija** (**Dynamics 365 Finance** > **Projekta pārvaldība un grāmatvedība** > **Žurnāli** > **Project Operations integrācijas žurnāls**).

![Integrācijas žurnāla plūsma.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Ierakstu izveide Project Operations integrācijas žurnālā

Ieraksti Project Operations integrācijas žurnālā tiek izveidoti, izmantojot periodisku procesu **Importēšana no Izstādīšanas tabulas**. Šo procesu var izpildīt, dodoties uz **Dynamics 365 Finance** > **Projektu pārvaldība un grāmatvedība** > **Periodiski** > **Project Operations integrācija** > **Importēšana no izstādīšanas tabulas**. Procesu var izpildīt interaktīvi vai pēc nepieciešamības konfigurēt procesu, lai tas tiktu izpildīts fonā.

Veicot periodisku procesu, tiek atrasti visi faktiskie dati, kas vēl nav pievienoti Project Operations integrācijas žurnālam. Tiek izveidota žurnāla rinda katrai faktiskajai darbībai.
Sistēma grupē žurnāla rindas atsevišķos žurnālos, pamatojoties uz vērtību, kas ir atlasīta laukā **Perioda vienība Project Operations integrācijas žurnālā** (**Finance** > **Projekta pārvaldība un uzskaite** > **Iestatīšana** > **Projekta pārvaldība un uzskaites parametri**, **Project Operations Dynamics 365 Customer Engagement** cilne). Šī lauka iespējamās vērtības ir šādas:

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
    - Ja **Darbības kategorija** nav iestatīta projekta faktiskajos datos, sistēma izmanto vērtību no lauka **Projekta kategoriju noklusējumi** cilnē **Project Operations pakalpojumā Dynamics 365 Customer Engagement**, kas atrodas lapā **Projekta pārvaldības un uzskaites parametri**.
  - Lauks **Resursi** norāda ar šo transakciju saistīto projekta resursu. Resurss tiek izmantots kā atsauce projekta rēķina priekšlikumos klientiem.
  - Lauks **Valūtas kurss** pēc noklusējuma tiek ņemts no **Valūtas maiņas kursa**, kas iestatīts programmā Dynamics 365 Finance. Ja nav maiņas kursa iestatījuma, periodiskais process **Importēšana no izstādīšanas** nepievienos šo ieraksta žurnālā, un darba izpildes žurnālā tiks pievienots kļūdas ziņojums.
  - Lauks **Rindas rekvizīts** apzīmē norēķinu tipu projekta faktiskajos datos. Rindas statuss un norēķinu tipu kartēšana tiek definēta cilnē **Project Operations pakalpojumā Dynamics 365 Customer Engagement**, kas atrodas lapā **Projekta pārvaldības un grāmatvedības parametri**.

Project Operations integrācijas žurnāla rindās var atjaunināt tikai šādus uzskaites atribūtus:

- **Rēķinu PVN grupa** un **Rēķina vienuma PVN grupa**
- **Finanšu dimensijas** (izmantojot darbību **Sadalīt summas**)

Integrācijas žurnāla rindas nav iespējams dzēst. Taču visas neiegrāmatotās rindas tiks ievietotas žurnālā vēlreiz pēc tam, kad atkārtoti palaidīsit periodisko procesu **Importēšana no izstādīšanas**.

### <a name="post-the-project-operations-integration-journal"></a>Project Operations integrācijas žurnāla grāmatošana

Kad tiek grāmatots integrācijas žurnāls, tiek izveidotas projekta apakšgrāmatas un virsgrāmatas darbības. Tās izmanto pakārtotā klienta rēķina izrakstīšanai, ieņēmumu atzīšanai un finanšu atskaišu izveidei.

Atlasīto Project Operations integrācijas žurnālu var iegrāmatot, izmantojot funkciju **Grāmatot** Public Operations integrācijas žurnāla lapā. Visas darba grupas var automātiski grāmato, palaižot procesu sadaļā **Periodiski** > **Project Operations integrācija** > **Grāmatot Project Operations integrācijas žurnālu**.

Grāmatošanu var veikt interaktīvi vai partijā. Ņemiet vērā, ka visi žurnāli ar vairāk nekā 100 rindām tiek automātiski grāmatoti partijā. Lai nodrošinātu labāku veiktspēju, kad partijā tiek grāmatoti žurnāli ar daudz rindām, iespējojiet līdzekli **Grāmatot Project Operations integrācijas žurnālu, izmantojot vairāku partiju uzdevumus** darbvietā **Līdzekļu pārvaldība**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Pārsūtīt visas rindas, kurās ir ziņu kļūdas, uz jaunu žurnālu

> [!NOTE]
> Lai izmantotu šo iespēju, darbvietā **Līdzekļu pārvaldība** iespējojiet līdzekli **Pārsūtīt visas rindas ar grāmatošanas kļūdām uz Project Operations integrāciju žurnālu**.

Šis līdzeklis palīdz uzlabot Project Operations integrāciju žurnāla lietošanu. Ja šī opcija ir iespējota, nekādas problēmas ar rakstīto laika grafiku un iestatīšanas problēmas vairs nekavēs derīgu žurnālu grāmatošanu. Veicot grāmatošanu Project Operations integrāciju žurnālā, sistēma pārbaude katru žurnāla rindu. Tiek izliktas visas rindas, kurās nav kļūdu, un tiek izveidots jauns kļūdu saraksts visām rindām, kurās ir grāmatošanas kļūdas.

Lai pārskatītu žurnālus ar grāmatošanas kļūmju rindām, dodieties uz **Projektu pārvaldība un uzskaite**\>**Žurnāli**\>**Project Operations integrāciju žurnāls** un filtrējiet žurnālu sarakstu, izmantojot lauku **Sākotnējais žurnāls**. Attēlā tālāk parādīts piemērs, kurā šādā veidā ir filtrēti žurnāli lapā **Project Operations integrāciju žurnāls**.

![Sākotnējais žurnāls, parādīts Project Operations integrāciju žurnāla lapā.](./media/transferLines-originalJournal.png)

Ja periodisks pakešu uzdevums tiek konfigurēts, lai grāmatotu integrācijas žurnālu, grāmatošanas mēģinājums tiks atkārtots un žurnāli tiks grāmatoti, ja būs labota laika kļūda. Jebkurš atlikušais žurnāls ir manuāli jāpārbauda, izskatot žurnālus un veicot vajadzīgās darbības.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
