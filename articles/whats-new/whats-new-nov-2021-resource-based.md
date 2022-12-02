---
title: Jaunumi 2021. novembrī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2021. gada novembra laidienā Project Operations resursu/bez krājumu scenārijiem.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932903"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2021. novembrī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem

*Attiecas uz: Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem*

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.22.

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Šajā laidienā ir ietverti tālāk minētie līdzekļi.

- Projektu plānošanas programmas programmēšanas saskarnes (API) tagad atbalsta iespēju izveidot un dzēst projektu intervālus.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](/dynamics365/project-operations/environment/resource-dual-write-maps).

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-in-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2240080 | Laukam **Maksājumu nosacījumi** nedrīkst dublēt pro forma rēķinā. |
| Cenu noteikšana un norēķini | 2358236 | Rēķina korekcijai ir jāatļauj veikt korekcijas, kurām ir nulles cenas rindas. |
| Resursu pārvaldība | 2410072 | Atļauja iestatīt resursu, kas ir piešķirts uzdevumam kā projekta vadītājs. |
| Cenu noteikšana un norēķini | 2430234 | Labota izmaksu veiktspējas aprēķina problēma. |
| Laiks un izdevumi | 2436978 | Atļauts ievadīt laiku formātā hh:mm. |
| Cenu noteikšana un norēķini | 2448623 | Atļauts atjaunināt cenrāžus pēc tam, kad tie ir saistīti ar organizācijas vienību. |
| Laiks un izdevumi | 2460396 | Atļauts dzēst laika ierakstu, notīrot šūnu. |
| Cenu noteikšana un norēķini | 2467386 | Atļauts dzēst projektu, kam ir uzdevums, pat tad, ja uzdevums ir saistīts ar iegūtu piedāvājumu. |
| Laiks un izdevumi | 2461744 | Skatā **Mani nesekmīgie apstiprinājumi** skats ietver tikai projekta apstiprinājumus ar posmu **Iesniegts**. |
| Laiks un izdevumi | 2464082 | Noņemta saite no projekta apstiprinājumiem uz apstiprinājuma kopu, kad mērķa statuss ir saskaņots. |
| Laiks un izdevumi | 2468108 | Plānošanas uzdevumam nav jāiestata statuss **Apstrāde** apstiprinājuma kopai. |
| Laiks un izdevumi | 2471503 | Tiek dzēstas apstiprinājuma kopas, kas ir septiņu dienu vecas. |
| Cenu noteikšana un norēķini | 2480687 | Veidojot piedāvājuma rindas atskaites punktu, piedāvājuma rindas atsauci nedrīkst noņemt. |

### <a name="project-management-and-accounting-in-finance"></a>Pārskats par projektu pārvaldību un uzskaiti pakalpojumā Finance

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Projektu pārvaldība un uzskaite | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Saglabātās piegādātāju summas projekta izdevumu transakcijās netiek parādītas transakciju sarakstā. |
| Projektu pārvaldība un uzskaite | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Kad ir ieslēgta piegādātāju rēķinu integrācija, tiek pārtraukts starpuzņēmumu piegādātāju rēķins. |
| Projektu pārvaldība un uzskaite | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projekta rēķinu apmaksas nosacījumi nedarbojas, kā paredzēts. |
| Projektu pārvaldība un uzskaite | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Izlaižot piegādātāja saglabāšanu, dokumentu grāmatojumam ir papildu rindas, kas nav pareizas. |
| Projektu pārvaldība un uzskaite | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Kad tiek grāmatots Project Operations integrācijas žurnāls, tas neizdodas, jo trūkst dimensiju attiecībā uz kontu, kas netiek grāmatots. |
| Projektu pārvaldība un uzskaite | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Cilne **Projekts** nav rediģējama gaidošā piegādātāja rēķinā, kad sagādes kategorija ir piešķirta vienumam. |
| Projektu pārvaldība un uzskaite | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Nav navigācijas rūts, ja neesat pieteicies programmā Project Operations Dataverse. |
| Projektu pārvaldība un uzskaite | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Grāmatojot ieņēmumus no projekta rēķina atbilstošā honorāra gadījumā, rodas problēma, jo transakcijas dokumentā nav līdzsvarotas. |
| Projektu pārvaldība un uzskaite | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Novērtējuma izveide pēc rēķina priekšlikuma publicēšanas bloķē labojumu rindu importēšanu. |
| Projektu pārvaldība un uzskaite | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Nevar modificēt atskaites punktu ierakstus ar pilnībā izrakstītu rēķinu. |
| Komandējumi un izdevumi | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visus izdevumu pārskatus var redzēt, meklējot kategoriju izdevumu mobilajā programmā. |
| Komandējumi un izdevumi | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepareizas summas piegādātāju transakcijās un pārdošanas nodokļu transakcijās tiek grāmatotas no izdevumiem, kas tiek izveidots no kredītkaršu transakcijām. |
| Komandējumi un izdevumi | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Atsvaidzinot lapu **Izdevumu pārskats**, rodas nesaistīts brīdinājums. |
| Komandējumi un izdevumi | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Tiek izmantots nepareizais pagaidu apstiprinātājs, kad dzēšat pagaidu apstiprinātāju un pēc tam atkārtoti iesniedzat izdevumu pārskatu, izmantojot darbplūsmu. |
| Komandējumi un izdevumi | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Rodas ar nobraukuma iestatīšanu saistīta grāmatošanas kļūda. |
