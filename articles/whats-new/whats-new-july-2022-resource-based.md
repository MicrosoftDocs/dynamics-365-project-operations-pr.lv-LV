---
title: Jaunumi 2022. gada jūlijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2022. gada jūlija laidienā programmā Microsoft Dynamics 365 Project Operations resursos/noliktavā neesošos krājumos balstītiem scenārijiem.
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
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.28.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Izvietošana un konfigurācija | 2761472 | Novērsta Project Operations instalēšanas kļūda. |
| Cenu noteikšana un norēķini | 2746940 | Apakšlīguma rindas nosaukuma maksimālais garums nedrīkst pārsniegt 100 rakstzīmes. |
| Cenu noteikšana un norēķini | 2739162 | Klientiem jāvar redzēt lentes pogas faktisko datu režģa skatā. |
| Projektu plānošana un izsekošana | 2730318 | Atjaunināta neatbalstīto rakstzīmju pārbaude projekta tēmā. |
| Cenu noteikšana un norēķini | 2705361 | Projekta izsekošanas laukos ir jāiekļauj rēķinā iekļautās atskaites punktu faktiskās pārdošanas. |
| Cenu noteikšana un norēķini | 2675880 | Netiek pieļauta projekta saistīšana ar līguma rindu, kas nav balstīta uz darbu. |
| Cenu noteikšana un norēķini | 2664396 | Ja piedāvājuma cenrādis tiek saglabāts bez piedāvājuma, ir jābūt kļūdai, kurā norādīts, ka piedāvājums nevar būt tukšs. |
| Cenu noteikšana un norēķini | 2184019 | Cilnei **Norēķini, kuru pamatā ir uzdevums** nav jābūt redzamai projektos, kam nav dublēta līguma vai piedāvājuma. |
| Laiks un izdevumi | 2754459 | Ja periodiskas plānošanas mākoņa plūsma ir neaktīva, jārāda reklāmkarogs un jāapiet asinhronā apstrāde. |
| Cenu noteikšana un norēķini | 2724391 | Ja projekta līguma sadalīšanas norēķinu kārtulā trūkst klienta vērtības, rodas nepareizs izņēmums. |
| Cenu noteikšana un norēķini | 2708638 | Meklēšanas laikā, izmantojot režģa meklēšanu materiālu lietojumos un materiālu lietojumu apstiprinājumos, ieraksts netika atrasts.|
| Cenu noteikšana un norēķini | 2686977 | Jānovērš rēķina rindas apstiprināšana rēķina izveides laikā. |
| Cenu noteikšana un norēķini | 2683032 | Rēķinā iekļaujamo lomu un kategoriju kopēšanu nevar mērogot virs 5000 ierakstiem.|
| Cenu noteikšana un norēķini | 2673363 | Izmaksu patēriņš % projektā ir kļūdains, ja projektam pastāv gan ieguldījuma un izdevumu aprēķini, gan faktiskie dati. |

### <a name="project-management-and-accounting-in-finance"></a>Pārskats par projektu pārvaldību un uzskaiti pakalpojumā Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services (LCS) un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Līdzekļi, kas nākamajā laidienā ir ieslēgti pēc noklusējuma

Šajā tabulā ir uzskaitīti līdzekļi, kas pēc noklusējuma ir ieslēgtas versijā 10.0.29. Lielāko daļu līdzekļu, kas ir automātiski ieslēgti, var izslēgt [Līdzekļu pārvaldībā](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Turpmāk daži automātiski ieslēgtie līdzekļi var tikt noņemti no līdzekļu pārvaldības un kļūt obligāti. Šīs izmaiņas nodrošina, ka klienti izmanto pašreizējo funkcionalitāti, lai uzlabojumi varētu balstīties uz pašreizējo funkcionalitāti pievienošanas laikā. Līdzekļi nekad netiks automātiski iespējoti pēc mazāk nekā viena gada, ja vien tie nav noteikti kā būtiski.

| Līdzekļa nosaukums | Iespējošanas datums | Līdzeklis pievienots | Līdzekļa statuss | Modulis |
| --- | --- | --- |--- |--- |
| Iespējot stundu transakciju korekcijas, ņemot vērā finansējuma nosacījumu sadalījuma izmaiņas | 2022. gada 16. septembris | 2020. gada 7. oktobris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Projekta pirkuma pasūtījuma priekšapmaksas rēķina atgriešanas līdzeklis | 2022. gada 16. septembris | 2021. gada 6. oktobris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Dzēst rēķinu priekšlikumu rindas, izmantojot Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem | 2022. gada 16. septembris | 2021. gada 6. oktobris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Pielāgot grāmatotas projekta transakcijas uzskaiti | 2022. gada 16. septembris | 2020. gada 10. maijs | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Iespējot projekta noklusējuma uzskaites iestatījumus | 2022. gada 16. septembris | 2020. gada 19. februāris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Iespējot vairākas projekta līguma rindas | 2022. gada 16. septembris | 2020. gada 29. jūnijs | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Padarīt projekta stundu žurnālus tikai lasāmus, ja pašreizējais apstiprinājuma statuss neļauj rediģēt | 2022. gada 16. septembris | 2021. gada 6. oktobris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Iespējot pārdošanas rindu sinhronizāciju no pirkšanas rindām, kad pirkšanas rindas tiek atjauninātas un ir ieslēgts pirkumu pasūtījuma izmaiņu pārvaldības parametrs | 2022. gada 16. septembris | 2020. gada 7. oktobris | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Iespējot Project Operations pakalpojumā Dynamics 365 Customer Engagement | 2022. gada 16. septembris | 2020. gada 29. jūnijs | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |
| Projekta transakciju atsaukšanas labošanas līdzeklis | 2022. gada 16. septembris | 2020. gada 13. jūlijs | Ieslēgts pēc noklusējuma | Projektu pārvaldība un uzskaite |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Līdzekļi, kas gaidāmajā laidienā kļūs obligāti

Šajā tabulā ir uzskaitīti līdzekļi, kas līdz ar versiju 10.0.29 kļūs obligāti

| Līdzekļa nosaukums | Iespējošanas datums | Līdzeklis pievienots | Līdzekļa statuss | Modulis |
| --- | --- | --- | --- | --- |
| Aprēķināt piešķirto vērtību finansējuma avotā, nenoapaļojot valūtas kursu | 2022. gada 16. septembris | 2020. gada 14. jūnijs | Obligāts | Projektu pārvaldība un uzskaite |
| Iespējot projekta korekciju grāmatošanu ar to pašu virsgrāmatas kontu kā sākotnējai transakcijai | 2022. gada 16. septembris | 2020. gada 14. jūnijs | Obligāts | Projektu pārvaldība un uzskaite |
| Projekta līguma piešķirtās summas detalizēta informācija | 2022. gada 16. septembris | 2019. gada 31. augusts | Obligāts | Projektu pārvaldība un uzskaite |
| Iespējot kārtošanu pēc resursa projekta rēķina priekšlikuma izveides laikā | 2022. gada 16. septembris | 2019. gada 31. augusts | Obligāts | Projektu pārvaldība un uzskaite |
