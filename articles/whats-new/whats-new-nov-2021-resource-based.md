---
title: Jaunumi 2021. novembrī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2021. gada novembra projekta darbību laidienā resursu/neuzkrātiem scenārijiem.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 730f9f051c62f44734f2d7915517baf439b1a0b8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584881"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2021. novembrī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem

*Attiecas uz: Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem*

Šī tēma attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projekta operācijas Dataverse vides versijā 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.22

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Šajā laidienā ir ietverti tālāk minētie līdzekļi.

- Projektu plānošanas lietojumprogrammu interfeisi (API) tagad atbalsta iespēju izveidot un dzēst projektu grupas.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](/dynamics365/project-operations/environment/resource-dual-write-maps).

Atjauninot projektu operāciju Dataverse risinājumu un Finance risinājuma versiju, vienmēr palaidiet vidē jaunāko kartes versiju un iespējojiet visas saistītās tabulu kartes. Daži līdzekļi un iespējas var nedarboties pareizi, ja jaunākā kartes versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas [sniegti dual-write problēmu novēršanas rokasgrāmatas sadaļā Trūkstošo tabulu kolonnu problēma karšu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sadaļā.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-in-dataverse"></a>Projekta operācijas Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2240080 | Pro **forma rēķinā lauku Apmaksas nosacījumi** nedrīkst dublēt. |
| Cenu noteikšana un norēķini | 2358236 | Rēķina labošanai jāļauj veikt labojumus ar nulles cenas rindām. |
| Resursu pārvaldība | 2410072 | Atļaut iestatīt resursu, kas uzdevumam piešķirts kā projekta vadītājs. |
| Cenu noteikšana un norēķini | 2430234 | Novērsiet izmaksu veiktspējas aprēķina problēmu. |
| Laiks un izdevumi | 2436978 | Ļaujiet ievadīt laiku hh:mm formātā. |
| Cenu noteikšana un norēķini | 2448623 | Atļaut atjaunināt cenrāžus pēc to saistīšanas ar organizācijas vienību. |
| Laiks un izdevumi | 2460396 | Notīrot šūnu, atļaut dzēst laika ierakstu. |
| Cenu noteikšana un norēķini | 2467386 | Atļaut dzēst projektu, kuram ir uzdevums, pat ja uzdevums ir saistīts ar uzvarētu piedāvājumu. |
| Laiks un izdevumi | 2461744 | Apstiprinājuma **skatā Mans neizdevās ir tikai projekta apstiprinājumi posmā Iesniegts** **.** |
| Laiks un izdevumi | 2464082 | Noņemiet saiti no projekta apstiprinājumiem uz apstiprinājuma kopu, kad mērķa statuss ir saskaņots. |
| Laiks un izdevumi | 2468108 | Grafika darbam nevajadzētu iestatīt apstiprināšanas kopas **apstrādes** statusu. |
| Laiks un izdevumi | 2471503 | Dzēsiet apstiprinājuma kopas, kas ir septiņas dienas vecas. |
| Cenu noteikšana un norēķini | 2480687 | Piedāvājuma rindas atsauci nedrīkst noņemt, kad tiek izveidots piedāvājuma rindas atskaites punkts. |

### <a name="project-management-and-accounting-in-finance"></a>Projektu vadība un grāmatvedība finansēs

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Projektu pārvaldība un uzskaite | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Saglabātās kreditoru summas projekta izdevumu darbībās darbību sarakstā netiek rādītas. |
| Projektu pārvaldība un uzskaite | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Starpuzņēmumu kreditora rēķins tiek sadalīts, kad ir ieslēgta kreditora rēķinu integrācija. |
| Projektu pārvaldība un uzskaite | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Apmaksas nosacījumi projekta rēķinos nedarbojas, kā paredzēts. |
| Projektu pārvaldība un uzskaite | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kad kreditora ieturējums ir nodots izpildei, dokumentu grāmatošanai ir papildu rindas, kas nav pareizas. |
| Projektu pārvaldība un uzskaite | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Grāmatojot projektu operāciju integrācijas žurnālu, tas neizdodas, jo kontam, kurā netiek grāmatots, trūkst dimensiju. |
| Projektu pārvaldība un uzskaite | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Cilne **Projekts** nav rediģējama gaidošajā kreditora rēķinā, ja precei ir piešķirta sagādes kategorija. |
| Projektu pārvaldība un uzskaite | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigācijas rūts trūkst, ja neesat pieteicies projekta operācijās Dataverse. |
| Projektu pārvaldība un uzskaite | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Grāmatojot ieņēmumus no projekta rēķina attiecinātā aizturētāja gadījumā, problēma rodas tāpēc, ka dokumenta darbības nesabalansē. |
| Projektu pārvaldība un uzskaite | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Novērtējuma izveide pēc rēķina priekšlikuma grāmatošanas bloķē korekcijas rindas no importēšanas. |
| Projektu pārvaldība un uzskaite | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Nevajadzētu būt iespējai grozīt milestone record, par kuru ir pilnībā izrakstīts rēķins. |
| Komandējumi un izdevumi | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visi izdevumu pārskati ir redzami, meklējot kategoriju mobilajā lietotnē Izdevumi. |
| Komandējumi un izdevumi | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepareizas summas kreditoru darbībām un PVN darbībām tiek grāmatotas no izdevumiem, kas izveidoti no kredītkartes darbības. |
| Komandējumi un izdevumi | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Atsvaidzinot izdevumu atskaites **lapu, tiek parādīts neatbilstošs brīdinājums**. |
| Komandējumi un izdevumi | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Nepareizs pagaidu apstiprinātājs tiek izmantots, dzēšot pagaidu apstiprinātāju un pēc tam atkārtoti iesniedzot izdevumu pārskatu, izmantojot darbplūsmu. |
| Komandējumi un izdevumi | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Rodas grāmatošanas kļūda, kas saistīta ar nobraukuma iestatīšanu. |
