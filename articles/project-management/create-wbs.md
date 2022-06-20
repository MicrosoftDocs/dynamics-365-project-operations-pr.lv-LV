---
title: Darba sadalījuma struktūras izveide
description: Šajā rakstā paskaidrots, kā izveidot darba sadalījuma struktūru (WBS), iekļaujot pamata vadīklas jaunajā plānošanas saskarnē.
author: ruhercul
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: a947c0a44464bfad6c3bd74b0cb4fb8128924859
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932075"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Darba sadalījuma struktūras (WBS) izveide

Projekta grafikā ir pateikts, kāds darbs ir jāpaveic, kuri resursi šo dabu paveiks un kādā laika posmā šis darbs ir jāpabeidz. Grafiks atspoguļo pilnībā visu darbu, kas saistīts ar savlaicīgu projekta nodošanu. Programmā Dynamics 365 Project Operations jūs izveidojat projekta grafiku:

  - Sadalot darbu pārvaldāmos uzdevumos.
  - Aprēķinot laiku, kas ir nepieciešams katra uzdevuma izpildei.
  - Iestatos uzdevuma atkarības.
  - Iestatot uzdevuma ilgumus.
  - Aprēķinot vispārīgos resursus, kuri izpildīs uzdevumus. 

Projekta grafiks tiek izveidots **Projekta** lapas cilnē **Grafiks**.

## <a name="tasks"></a>Uzdevumi

Projekta grafika izveidošanas pirmais posms ir visa darba sadalīšana pārvaldāmās daļās. Programmaā Project Operations grafiks atbalsta tālāk norādītos līdzekļus.

- Kopsavilkuma vai konteinera uzdevumi
- Lapas mezgla uzdevumi

### <a name="summary-tasks"></a>Kopsavilkuma uzdevumi

Kopsavilkuma uzdevumus var glabāt citi kopsavilkuma uzdevumi vai lapas mezglu uzdevumi. Tiem nav pašiem savas darba piepūles vai izmaksu. Tā vietā šo uzdevumu darba piepūli un izmaksas veido apkopojums no darba piepūles un izmaksām to konteineru uzdevumos. Kopsavilkuma uzdevuma sākuma datums ir konteinera uzdevumu sākuma datums, un tā beigu datums ir konteinera uzdevumu beigu datums. Kopsavilkuma uzdevuma nosaukumu var rediģēt, bet plānošanas rekvizītus, tostarp piepūli, datumus un ilgumu, nevar rediģēt. Ja izdzēšat kādu kopsavilkuma uzdevumu, tiek izdzēsti arī visi tā konteinera uzdevumi.

### <a name="leaf-node-tasks"></a>Lapas mezgla uzdevumi

Lapas mezgla uzdevumi pārstāv projekta darba vissīkāko iedalījumu. Tiem ir aplēstā piepūle, resursi, plānotais sākuma un beigu datums un ilgums.

## <a name="create-a-task-hierarchy"></a>Uzdevumu hierarhijas izveidošana

### <a name="add-a-task"></a>Uzdevuma pievienošana

Lai pievienotu vienu vai vairākus uzdevumus, izpildiet tālāk norādītās darbības.

1. Dodieties uz **Projekti** un atlasiet un atveriet projekta ierakstu, kuram vēlaties izveidot grafiku. 
2. Atlasiet cilni **Uzdevumi**. 
3. Atlasiet **Pievienot jaunu uzdevumu**, ievadiet uzdevuma nosaukumu un pēc tam nospiediet Enter.
2. Ievadiet citu uzdevuma nosaukumu un vēlreiz nospiediet taustiņu Enter, līdz ir iegūts pilns uzdevumu saraksts.

### <a name="manage-hierarchy-of-a-task"></a>Uzdevuma hierarhijas pārvaldība

Kad uzdevumam tiek pielikta atkāpe, tas kļūst par bērnelementu uzdevumam, kurš atrodas tieši virs tā. Pēc tam šī uzdevuma grafika ID tiek pārrēķināts, lai tas būtu balstīts uz tā jaunā vecākelementa grafika ID un atbilstu strukturējuma numerācijas shēmai. Primārais uzdevums tagad ir kopsavilkuma uzdevums. Līdz ar to tas kļūst par savu pakārtoto uzdevumu apkopojumu. Kad uzdevums tiek paaugstināts, tas vairs nav bērnelements tam uzdevumam, kurš bija tā pamatuzdevums. Pēc tam grafika ID tiek pārrēķināts tā, lai tas atspoguļotu uzdevuma atjaunināto dziļumu un pozīciju hierarhijā. Iepriekšējā pamatuzdevuma piepūle, izmaksas un datumi tiek pārrēķināti, lai tie neiekļautu šo uzdevumu.

Lai veidotu atkāpi vai paaugstinātu uzdevumu, izpildiet tālāk norādītās darbības.

1. Lapas **Projekts** cilnes **Uzdevumi** sadaļā **Kopsavilkuma uzdevumi** atlasiet trīs vertikālos punktus blakus uzdevuma nosaukumam un pēc tam atlasiet **Izveidot apakšuzdevumu**. 
2. Atlasiet uzdevumu, kuram veidot atkāpi vai kuru paaugstināt. Lai atlasītu vairāk nekā vienu uzdevumu, atlasiet uzdevumu, nospiediet un turiet nospiestu taustiņu CTRL un pēc tam atlasiet papildu uzdevumus.
2. Atlasiet **Veidot atkāpi** vai **Paaugstināt apakšuzdevumu**, lai uzdevumi vairs neatrastos zem kopsavilkuma uzdevumiem.

### <a name="move-tasks-up-and-down"></a>Uzdevumu pārvietošana uz augšu un leju

Uzdevumus var pārvietot uz jebkuru darba sadalījuma struktūras līmeni vienā no diviem veidiem:

- Atlasiet vienu vai vairākus uzdevumus un velciet tos uz vēlamo atrašanās vietu.
- Atlasiet vienu vai vairākus uzdevumus, noklikšķiniet ar labo peles pogu un atlasiet **Izgriezt**, atlasiet grafikā mērķa šūnu, noklikšķiniet ar labo peles taustiņu un atlasiet **Ielīmēt**.

## <a name="task-attributes"></a>Uzdevuma atribūti

Uzdevuma nosaukums apraksta darbu, kas ir jāizpilda. Programmā Project Operations ar uzdevumu saistītie atribūti apraksta šī uzdevuma grafiku un tā personāla komplektēšanas prasības.

## <a name="schedule-attributes"></a>Grafika atribūti

Atribūti **Piepūle**, **Sākuma datums**, **Beigu datums** un **Ilgums** nosaka grafiku attiecīgajam uzdevumam.

Šajā tabulā redzami papildu grafika atribūti.

| **Galīgais parādāmais nosaukums** | **Galīgais apraksts** |
| --- | --- |
| Veiktais darbs (stundas) | Pabeigtais uzdevuma darbs, izteikts stundās |
| Ilgums | Rāda uzdevuma ilgumu dienās. |
| Kopējais ieguldījums | Kopējais uzdevuma darbs, izteikts stundās. |
| Pabeigt | Beigu datums un laiks. |
| % pabeigti | Uzdevuma izpildītā daļa, izteikta procentos. |
| Projekta bloks | Uzdevumu paneli var grupēt pēc bloka, tāpēc katram blokam ir sava kolonna. |
| Atlikušais darbs (stundas) | Uzdevuma atlikušais darbs, izteikts stundās. |
| Sākt | Sākuma datums un laiks. |
| Nosaukums/vārds, uzvārds | Uzdevuma nosaukums. |
| ID | Darba sadalījuma struktūras uzdevuma ID. |

Kā administrators uzdevuma entītijai var definēt pielāgotus laukus. Tomēr laukus nevar parādīt plānošanas režģī. Lai skatītu pielāgotos laukus, pievienojiet tos vienuma **Projekta uzdevums** informācijas lapai.

## <a name="staffing-attributes"></a>Darbspēka atribūti

Personāla komplektēšanas atribūtiem piekļūst, grafikā izmantojot lauku **Resursi**. Varat vai nu meklēt jau esošu resursu, vai rūtī **Ātrā izveide** atlasīt **Izveidot** un pievienot projekta darba grupas dalībnieku kā jaunu resursu.  Meklējot resursu, izmantojot resursu atlasītāju uzdevumu režģī, dēļa skatā vai gantā, meklēšana atgriež esošos projekta grupas dalībniekus vai aktīvos rezervējamos resursus.

Uzdevuma personāla komplektēšanas prasību aprakstīšanai tiek izmantoti lauki **Loma**, **Resursu vienība** un **Amata nosaukums**. Šie personāla komplektēšanas atribūti kopā ar uzdevuma grafiku tiek izmantoti, lai atrastu pieejamos resursus šī uzdevuma veikšanai.

   - **Loma**: norādiet uzdevuma veikšanai nepieciešamā resursa tipu.,
   - **Resursu vienība**: Norādiet struktūrvienību, no kuras ir jāpiešķir resursi šim uzdevumam. Ja resursa izmaksu un norēķinu likmes ir iestatītas, pamatojoties uz resursu vienībām, šis atribūts uzdevumam ietekmē izmaksu un pārdošanas tāmi.
   - **Amata nosaukums**: Ievadiet draudzīgu nosaukumu vispārējam resursam, kas tiek izmantots kā vietturis resursam, kurš galu galā darīs šo darbu.

Laukā **Resursi** ir vispārējā resursa amata nosaukums vai nosaukts resurss, ja tāds tiek atrasts.

Laukā **Kategorija** ir vērtības, kas norāda plašāku darba tipu, kurā šo uzdevumu var ieļaut. Šis lauks neietekmē plānošanu un personāla komplektēšanu. Tā vietā lauks tiek izmantots vienīgi atskaišu veidošanai.

## <a name="task-dependencies"></a>Uzdevuma atkarības

Grafiku programmā Project Operations varat izmantot, lai starp uzdevumiem izveidotu pirmstecīgas aktivitātes attiecības. Lauks **Pirmstecīga aktivitāte** izmanto vienu vai vairākas vērtības, lai norādītu uzdevumus, no kuriem kāds uzdevums ir atkarīgs. Ja kādam uzdevumam ir piešķirtas pirmstecīgas aktivitātes vērtības, šis uzdevums var sākties tikai pēc tam, kad ir pabeigti visi tā pirmstecīgie uzdevumi. Atkarības dēļ uzdevuma plānotais sākuma datums tiek atiestatīts uz datumu, kad ir pabeigti pirmstecīgie uzdevumi.

Uzdevuma režīms neietekmē atjauninājumus, kas tiek veikti pirmstecīgo/atkarīgo uzdevumu sākuma un beigu datumiem.

## <a name="accessibility-and-keyboard-shortcuts"></a>Pieejamība un īsinājumtaustiņi

Režģis **Grafiks** ir pilnībā pieejams, un to var izmantot ar tādiem ekrāna lasītājiem kā Diktors, JAWS un NVDA. Pa režģa laukumu varat pārvietoties, izmantojot bulttaustiņus (tāpat kā programmā Microsoft Excel), varat izmantot tabulēšanas taustiņu, lai pārvietotos pa interaktīvajiem lietotāja interfeisa elementiem, kā arī varat izmantot lejupvērsto bultiņu, taustiņu Enter vai atstarpes taustiņu, lai atlasītu un atvērtu nolaižamās izvēlnes.

## <a name="project-limitations"></a>Projekta ierobežojumi 
Ja izmantojat Project Operations darba sadalījuma struktūru, ņemiet vērā tālāk sniegtos ierobežojumus. Šie ierobežojumi attiecas uz projektiem un uzdevumiem. Papildinformāciju skatiet sadaļā [Projekta tīmekļa ierobežojumi un robežas](/project-for-the-web/project-for-the-web-limits-and-boundaries).

| **Lauks**                                          |  **Ierobežojums**           |
|----------------------------------------------------|----------------------|
| Projekta maksimālais uzdevumu skaits                  | 500                  |
| Projekta maksimālais ilgums               | 3650 dienas (10 gadi) |
| Projekta maksimālais resursu skaits              | 300                  |
| Projekta maksimālais saišu skaits (tikai pēctecis) | 600                  |
| Projekta maksimālais pielāgoto lauku skaits          | 10                   |
| Maksimālais kontrolsaraksta vienumu skaits katram uzdevumam                   | 20                   |

**Uzdevumu ierobežojumi**

| **Lauks**                               |   **Ierobežojums**           |
|-----------------------------------------|-----------------------|
| Maksimālais hierarhijas līmenis                 | 10 līmeņi             |
| Maksimālais saišu skaits (pēctecis + priekštecis) | 20                    |
| Maksimālais atbildes uzdevuma ilgums           | 1250 dienas             |
| Maksimālais kopsavilkuma uzdevuma ilgums      | 3650 dienas (10 gadi)  |
| Maksimālais uzdevumam piešķirto resursu skaits    | 20 resursi          |
| Atbalstītais uzdevuma datumu diapazons         | 1/1/2000 - 12/31/2149 |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
