---
title: Jaunumi 2022. gada jūlijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada jūlija laidienā uz resursiem/nepiegādātiem scenārijiem.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403961"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. gada jūlijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.44.0.22
- Projektu vadīšana un uzskaite Dynamics 365 Finance vidē versija 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Vienmēr palaidiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes, atjauninot project operations Dataverse risinājumu un finance risinājuma versiju. Daži līdzekļi un iespējas var nedarboties pareizi, ja kartes jaunākā versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis lietošanai gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas sniegti [divrakstīšanas problēmu novēršanas ceļveža sadaļā Trūkstošās tabulas kolonnas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) kartēs.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Izvietošana un konfigurācija | 2761472 | Tiek apstrādāta Project Operations instalēšanas kļūda. |
| Cenu noteikšana un norēķini | 2746940 | Apakšuzņēmuma līguma rindiņas nosaukumam jābūt ne vairāk kā 100 rakstzīmju garumam. |
| Cenu noteikšana un norēķini | 2739162 | Klientiem ir jābūt iespējai redzēt lentes pogas faktiskā režģa skatā. |
| Projektu plānošana un izsekošana | 2730318 | Atjaunināta validācija neatbalstītām rakstzīmēm projekta tēmā. |
| Cenu noteikšana un norēķini | 2705361 | Atskaites punkta rēķinā norādītie pārdošanas dati ir jāiekļauj projektu izsekošanas laukos. |
| Cenu noteikšana un norēķini | 2675880 | Neļaujiet projektam būt saistītam ar līguma līniju, kas nav balstīta uz darbu. |
| Cenu noteikšana un norēķini | 2664396 | Ja piedāvājuma cenrādis tiek saglabāts bez piedāvājuma, ir jābūt kļūdai, kas norāda, ka piedāvājums nevar būt tukšs. |
| Cenu noteikšana un norēķini | 2184019 | Cilne Uz **uzdevumu balstīti norēķini** nav jārāda projektiem, kuriem nav atbalsta līguma vai piedāvājuma. |
| Laiks un izdevumi | 2754459 | Ja periodiska plānošanas mākoņa plūsma ir neaktīva, parādiet reklāmkarogu un apejiet asinhrono apstrādi. |
| Cenu noteikšana un norēķini | 2724391 | Nepareizs izņēmums tiek izmests, ja projekta līguma sadalītā norēķinu kārtulā trūkst klienta vērtības. |
| Cenu noteikšana un norēķini | 2708638 | Ieraksts netika atrasts, meklējot, izmantojot režģa meklēšanu materiāla lietojumos un materiālu lietojumu apstiprinājumos.|
| Cenu noteikšana un norēķini | 2686977 | Novērsiet rēķina rindas validāciju rēķina izveides laikā. |
| Cenu noteikšana un norēķini | 2683032 | Iekasējamo lomu un kategoriju kopēšana nepārsniedz 5000 ierakstus.|
| Cenu noteikšana un norēķini | 2673363 | Izmaksu patēriņš % projektā tiek bojāts, ja projektam pastāv gan piepūles, gan izdevumu aprēķini un faktiskie dati. |

### <a name="project-management-and-accounting-in-finance"></a>Projektu vadība un grāmatvedība finanšu jomā

Lai iegūtu informāciju par kļūdu labojumiem, kas ir iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services (LCS) un skatiet [zināšanu bāzes rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Līdzekļi, kas pēc noklusējuma ir ieslēgti gaidāmajā laidienā

Šajā tabulā ir uzskaitīti līdzekļi, kas pēc noklusējuma ir ieslēgti versijā 10.0.29. Lielāko daļu līdzekļu, kas ir automātiski ieslēgti, var izslēgt līdzekļu [pārvaldībā](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Nākotnē daži līdzekļi, kas ir automātiski ieslēgti, var tikt noņemti no funkciju pārvaldības un kļūt obligāti. Šīs izmaiņas nodrošina, ka klienti izmanto pašreizējo funkcionalitāti, lai uzlabojumi varētu balstīties uz pašreizējo funkcionalitāti, kad tie tiek pievienoti. Funkcijas nekad netiks automātiski iespējotas mazāk nekā viena gada laikā, ja vien tās netiks atzītas par būtiskām.

| Līdzekļa nosaukums | Datuma iespējošana | Pievienots līdzeklis | Līdzekļa stāvoklis | Modulis |
| --- | --- | --- |--- |--- |
| Iespējot stundas darījuma koriģēšanu, pamatojoties uz izmaiņām finansējuma kārtulu sadalījumā | 2022. gada 16. septembris | 2020. gada 7. oktobris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Projekta pirkšanas pasūtījuma priekšapmaksas rēķina atsaukšanas līdzeklis | 2022. gada 16. septembris | 2021. gada 6. oktobris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Rēķina priekšlikumu rindiņu dzēšana, ja projekta darbības tiek izmantotas uz resursiem balstītiem/neiekrātiem scenārijiem | 2022. gada 16. septembris | 2021. gada 6. oktobris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Grāmatvedības pielāgošana par grāmatotu projekta transakciju | 2022. gada 16. septembris | 2020. gada 10. maijs | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Noklusējuma grāmatvedības iestatīšanas iespējošana projektam | 2022. gada 16. septembris | 2020. gada 19. februāris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Iespējot vairākas projekta līguma rindas | 2022. gada 16. septembris | 2020. gada 29. jūnijs | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Padariet Project Hour žurnālus tikai lasāmus, ja pašreizējais apstiprinājuma statuss neatļauj rediģēšanu | 2022. gada 16. septembris | 2021. gada 6. oktobris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Pirkšanas rindu sinhronizācijas iespējošana no pirkšanas rindām, kad tiek atjauninātas pirkšanas rindas un ir ieslēgts pirkšanas pasūtījuma izmaiņu pārvaldības parametrs | 2022. gada 16. septembris | 2020. gada 7. oktobris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Projekta darbību iespējošana Dynamics 365 Customer Engagement | 2022. gada 16. septembris | 2020. gada 29. jūnijs | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Projekta transakciju apvēršanas korekcijas līdzeklis | 2022. gada 16. septembris | 2020. gada 13. jūlijs | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Līdzekļi, kas kļūst obligāti gaidāmajā laidienā

Nākamajā tabulā ir uzskaitīti līdzekļi, kas ir obligāti, sākot no versijas 10.0.29.

| Līdzekļa nosaukums | Datuma iespējošana | Pievienots līdzeklis | Līdzekļa stāvoklis | Modulis |
| --- | --- | --- | --- | --- |
| Aprēķiniet piešķirto vērtību finansējuma avotā, nenoapaļojot valūtas kursu | 2022. gada 16. septembris | 2020. gada 14. jūnijs | Obligāts | Projektu pārvaldība un uzskaite |
| Projekta korekcijas grāmatošanas iespējošana ar to pašu Virsgrāmatas kontu kā sākotnējā transakcija | 2022. gada 16. septembris | 2020. gada 14. jūnijs | Obligāts | Projektu pārvaldība un uzskaite |
| Detalizēta informācija par projekta līgumā noteikto summu | 2022. gada 16. septembris | 2019. gada 31. augusts | Obligāts | Projektu pārvaldība un uzskaite |
| Kārtošanas pēc resursa iespējošana projekta rēķina priekšlikuma izveides laikā | 2022. gada 16. septembris | 2019. gada 31. augusts | Obligāts | Projektu pārvaldība un uzskaite |
