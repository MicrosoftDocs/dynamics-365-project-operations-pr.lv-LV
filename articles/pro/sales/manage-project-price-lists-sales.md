---
title: Projekta cenrāžu pārvaldība projekta piedāvājumos
description: Šajā tēmā ir sniegta informācija par darbu ar projekta cenrāžiem piedāvājumos. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080367"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Projekta cenrāžu pārvaldība projekta piedāvājumos (Pārdošana)

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta piedāvājumi ir paredzēti, lai atbalstītu vairākus spēkā esošus pārdošanas cenrāžus. Izmantojot Dynamics 365 Project Operations, tiek pievienota jauna saistītā entītija, kas saucas **Projekta cenrāži**. Šai entītijai ar projekta piedāvājumu ir attiecība viens pret daudziem.

Projekta cenrāžus izmanto, lai noteiktu projekta laika un izdevumu darījumu cenas. Ja piedāvājumam ir viens vai vairāki projekta cenrāži, šos cenrāžus izmanto, lai noteiktu laika un izdevumu aprēķinātās un faktiskās cenas projektos, kas saistīti ar piedāvājumu caur piedāvājuma rindu.

Ja projekta piedāvājumam nav projekta cenrāžu, tiek parādīts brīdinājuma ziņojums. Ziņojumā ir norādīts: nav projekta cenrāžu, tādēļ jūsu aprēķinātajiem un faktiskajiem darbiem un izdevumiem šajā projektā netiks noteiktas cenas. Tā vietā to pārdošanas vērtībām būs nulle (0) cenas.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Projekta cenrāža saistīšana ar projekta piedāvājumu vai atsaiste no tā

Lai izveidotu vai atlasītu konkrētu cenrādi, ko izmantot projekta darbu un izdevumu aprēķinam, izpildiet tālāk norādītās darbības.

1. Piedāvājumā atlasiet cilni **Projekta cena** un apakšrežģī atlasiet vienumu **+ Pievienot jaunu projekta cenrādi**.
2. Ātrās izveides lapā atlasiet cenrādi. Nolaižamajā sarakstā ir parādīti visi cenrāži, kuru konteksts ir iestatīts kā **Pārdošana** , un valūta atbilst piedāvājuma valūtai.
4. Ievadiet projekta cenrāža saistības aprakstu un atlasiet vienumu **Saglabāt un aizvērt**.

Tiek izveidota projekta cenrāža sasaiste.

Šo procesu varat atkārtot, ja projekta piedāvājumam ir jāpiesaista vairāk nekā viens projekta cenrādis. Vairākus projekta cenrāžus veidojiet tikai tad, ja katram no saistītajiem projekta cenrāžiem ir atšķirīgi spēkā esamības datumi.

> [!NOTE]
> Project Operations neatbalsta spēkā esamības datumu pārklāšanos projektu cenrāžos. Ja darījumam ar norādīto datumu ir vairāki projekta cenrāži, šī darījuma cena pēc noklusējuma tiek iestatīta kā nulle (0).
Lai noņemtu projekta cenrāža piesaisti, atlasiet projekta cenrādi un pēc tam atlasiet vienumu **Dzēst piedāvājuma projekta cenrādi**. Cenrādis tiek noņemts no piedāvājuma projekta cenrāžiem, taču pats cenrādis netiek dzēsts. Tiek izdzēsta tikai tā sasaiste ar piedāvājumu.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Noklusējuma projekta cenrāžu iestatīšana piedāvājumam

Projekta cenrāžus var iestatīt projekta piedāvājumam pēc noklusējuma. Šis iestatījums nodrošina to, ka visi jūsu organizācijas piedāvājumi vienmēr sākas ar attiecīgā cenu perioda standarta cenrādi.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Organizācijas noklusējuma vērtību iestatīšana projektu cenrāžiem

1. Dodieties uz sadaļu **Iestatījumi** > **Vispārīgi** > **Parametri**.
2. Saraksta lapā **Aktīvie parametri** atrodiet ierakstu un veiciet dubultklikšķi, lai to atvērtu. 
3. Lapā **Parametri** atlasiet cilni **Cenrādis**. Tiek rādīts noklusējuma cenrāžu saraksts. Šis ir standarta izmaksu un pārdošanas cenrāžu saraksts. Pārdošanas cenrāža saistīšana ar katru valūtu, kurā veicat pārdošanu, nodrošina to, ka šis pārdošanas cenrādis pēc noklusējuma tiek izmantots jebkurā piedāvājumā, ko izveidojat klientiem, kas veic darījumus šajā valūtā.

### <a name="set-up-customer-specific-project-price-lists"></a>Klienta specifisku projekta cenrāžu iestatīšana

Klienta specifiskos projekta cenrāžus var iestatīt arī tad, ja ar klientiem ir noslēgta vispārēja vienošanās par izcenojumu.

Lai iestatītu klienta specifisko projekta cenrādi, izpildiet tālāk norādītās darbības.

1. Zonā **Pārdošana** atlasiet vienumu **Klienti**.
2. Aktīvo uzņēmumu sarakstā atlasiet un atveriet klienta ierakstu, kuram ir īpašs cenrādis.
3. Cilnē **Projekta cenrāži** varat izveidot jaunu saistību ar cenrādi, lai izmantotu šī klienta specifisko cenrādi.

## <a name="create-custom-pricing-on-a-project-quote"></a>Pielāgota izcenojuma izveide projekta piedāvājumam

Kad ir izveidoti noklusējuma specifiski projekta cenrāži organizācijai un klientam, projekta piedāvājumi tiek automātiski veidoti ar šīm projekta cenrāžu saistībām. Tomēr noteiktos gadījumos var rasties vajadzība izveidot pielāgotu izcenojumu konkrētam projekta piedāvājumam. 

1. Sadaļas **Projekta piedāvājums** cilnes **Projekta cenrādis** apakšrežģī pārliecinieties, ka nav atlasīts neviens konkrēts cenrāža ieraksts.
2. Atlasiet vienumu **Izveidot pielāgotu izcenojumu**. Ar šo darbību tiks kopēti visi standarta cenrāži, kas pašlaik ir saistīti ar piedāvājumu, un šīs kopijas tiks saistītas ar piedāvājumu. Esošās saistības ar standarta cenrāžiem tiks noņemtas. Pēc tam pārdevējs var sākt veikt cenu rediģējumus šajās kopijās. Šīs mainītās cenas būs attiecināmas tikai uz šo projekta piedāvājumu.
