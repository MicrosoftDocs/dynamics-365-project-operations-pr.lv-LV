---
title: Jaunumi 2021. novembrī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2021. gada novembra projekta operāciju laidienā scenārijiem, kuru pamatā ir resursi/uzkrājumi.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827335"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2021. novembrī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem

*Attiecas uz: Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem*

Šī tēma attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projekta operācijas Dataverse vides versijā 4.26.0.145, 4.26.0.148, vai 4.26.0.150
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.22

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Šajā laidienā ir ietverti tālāk minētie līdzekļi.

- Projektu plānošanas programmu programmēšanas interfeisi (API) tagad atbalsta iespēju izveidot un dzēst projektu kopas.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](/dynamics365/project-operations/environment/resource-dual-write-maps).

Vienmēr palaidiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulu kartes, atjauninot projekta operāciju Dataverse risinājumu un Finanšu risinājuma versiju. Daži līdzekļi un iespējas var nedarboties pareizi, ja nav aktivizēta jaunākā kartes versija. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis gatavu tabulas karti, atkārtoti pieteikties uz izmaiņām. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet divējādas [rakstīšanas problēmu novēršanas rokasgrāmatas sadaļā Trūkstošo tabulu kolonnu problēmas sadaļā Trūkstošās tabulas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) kolonnas.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-in-dataverse"></a>Projekta operācijas Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2240080 | Pro **forma rēķinā nedrīkst dublēt lauku Apmaksas** nosacījumi. |
| Cenu noteikšana un norēķini | 2358236 | Rēķina labojumam ir jāatļauj labojumi, kuriem ir nulles cenas rindas. |
| Resursu pārvaldība | 2410072 | Atļaut iestatīt resursa iestatījumus, kas uzdevumam piešķirts kā projekta vadītājs. |
| Cenu noteikšana un norēķini | 2430234 | Novērsiet izmaksu veiktspējas aprēķina problēmu. |
| Laiks un izdevumi | 2436978 | Atļaut laiku ievadīt hh:mm formātā. |
| Cenu noteikšana un norēķini | 2448623 | Atļaut cenrāžus atjaunināt pēc to saisti ar organizācijas vienību. |
| Laiks un izdevumi | 2460396 | Atļaut dzēst laika ievadni, notīrot šūnu. |
| Cenu noteikšana un norēķini | 2467386 | Atļaut dzēst projektu, kuram ir uzdevums, pat ja uzdevums ir saistīts ar uzvarētu piedāvājumu. |
| Laiks un izdevumi | 2461744 | **Skatā Mans neveiksmīgais apstiprinājums satur tikai projektu** apstiprinājumus iesniegšanas **posmā**. |
| Laiks un izdevumi | 2464082 | Noņemiet saiti no projekta apstiprinājumiem uz apstiprinājuma kopu, ja tiek saskaņots mērķa statuss. |
| Laiks un izdevumi | 2468108 | Plānošanas darbam nevajadzētu iestatīt **apstiprinājuma kopas apstrādes** statusu. |
| Laiks un izdevumi | 2471503 | Dzēst septiņu dienu vecus apstiprinājuma kopas. |
| Cenu noteikšana un norēķini | 2480687 | Veidojot piedāvājuma rindas atskaites punktu, piedāvājuma rindas atsauci nedrīkst noņemt. |

### <a name="project-management-and-accounting-in-finance"></a>Projektu vadība un grāmatvedība finansēs

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Projektu pārvaldība un uzskaite | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Projekta izdevumu darbībās saglabātās kreditoru summas netiek rādītas darbību sarakstā. |
| Projektu pārvaldība un uzskaite | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Starpuzņēmumu kreditora rēķins tiek pārtraukts, ja ir ieslēgta kreditora rēķinu integrācija. |
| Projektu pārvaldība un uzskaite | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projekta rēķinu apmaksas nosacījumi nedarbojas, kā paredzēts. |
| Projektu pārvaldība un uzskaite | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kad kreditora ieturējums ir nodots izpildei, dokumentu grāmatošanai ir papildu rindas, kas nav pareizas. |
| Projektu pārvaldība un uzskaite | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Grāmatojot projekta operāciju integrācijas žurnālu, tas neizdodas, jo kontam, kas netiek grāmatots, trūkst dimensiju. |
| Projektu pārvaldība un uzskaite | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Cilne Projekts nav** rediģējama gaidošā kreditora rēķinā, kad precei ir piešķirta sagādes kategorija. |
| Projektu pārvaldība un uzskaite | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Ja neesat pieteicies projekta operācijās Dataverse, trūkst navigācijas rūts. |
| Projektu pārvaldība un uzskaite | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Grāmatojot ieņēmumus no projekta rēķina attiecinātā aizturētāja gadījumā, rodas problēma, jo dokumenta darbības nav līdzsvarā. |
| Projektu pārvaldība un uzskaite | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Budžeta izveide pēc rēķina priekšlikuma grāmatošanas bloķē korekcijas rindas no importēšanas. |
| Projektu pārvaldība un uzskaite | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Pilnībā izrakstīta starpposma ieraksta modificēšanai nevajadzētu būt iespējamai. |
| Komandējumi un izdevumi | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visi izdevumu pārskati ir redzami, meklējot kategoriju mobilajā programmā Izdevumi. |
| Komandējumi un izdevumi | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepareizas summas kreditoru darbībām un PVN darbībām tiek grāmatotas no izdevumiem, kas izveidoti no kredītkartes darbības. |
| Komandējumi un izdevumi | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Atsvaidzinot lapu Izdevumu pārskats, tiek parādīts neatbilstošs **brīdinājums**. |
| Komandējumi un izdevumi | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Nepareizs pagaidu apstiprinātājs tiek izmantots, dzēšot pagaidu apstiprinātāju un pēc tam atkārtoti iesniedzot izdevumu pārskatu, izmantojot darbplūsmu. |
| Komandējumi un izdevumi | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Rodas grāmatošanas kļūda, kas saistīta ar nobraukuma iestatīšanu. |
