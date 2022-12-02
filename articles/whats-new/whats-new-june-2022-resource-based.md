---
title: Jaunumi 2022. gada jūnijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2022. gada jūnija laidienā programmā Microsoft Dynamics 365 Project Operations resursos/noliktavā neesošos krājumos balstītiem scenārijiem.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031340"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. gada jūnijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations programmas Dataverse vides versijā 4.43.0.77 vai 4.43.0.119
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.27.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Tālāk redzamajā tabulā ir parādītas duālās rakstīšanas kartes, kas ir modificētas vai pievienotas Project Operations 2022. gada jūnija laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| --- | --- | --- |
| Project Operations integrācijas projekta piegādātāju rēķinu eksportēšanas entītija (msdyn_projectvendorinvoices) | 1.0.0.1 | Novecojis mantotais lauks, un kartēts uz jauno lauku piegādātāja rēķina statusa izsekošanai. |

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Apakšlīgumu slēgšana | 2708885 | Novērsts kļūdas ziņojums, kas tiek rādīts, kad lietotājs izveido rezervējama resursa rezervācijas galvenes ierakstu, kurā nav ievadīts neviens rezervējams resurss. |
| Projektu plānošana un izsekošana | 2629441 | Labota darbplūsmas aktivizēšanas loģika, lai novērstu bezgalīgu cilpu, atjauninot projekta uzdevumus. |
| Laiks un izdevumi | 2641209 | Laika ierakstu importēšanai no piešķīrumiem/rezervācijām jāsaglabā rezervējama resursa atsauce. |
| Projektu plānošana un izsekošana | 2651148 | Projekta dokumenta galvenei jābūt aizsargātai.|
| Projektu plānošana un izsekošana | 2653145 | Pievienotas validācijas, lai nodrošinātu, ka nevar izveidot tādu projekta ierakstu, kura nosaukumā ir nederīgas rakstzīmes. |
| Laiks un izdevumi | 2654710 | Labota filtrēšana lapā **Apstiprinājumi**. |
| Cenu noteikšana un norēķini | 2667805 | Ir pievienotas validācijas, lai nepieļautu rēķinā iekļautu faktisko pārdošanu izveidošanas, ja nepastāv dublētas rēķinā neiekļautas faktiskās pārdošanas. |
| Cenu noteikšana un norēķini | 2668378 | Pievienotas validācijas, lai novērstu pielāgota izcenojuma dimensijas pievienošanu, ja nav norādīts loģiskais nosaukums un lauka nosaukums. |
| Apakšlīgumu slēgšana | 2677485 | Atjaunināta piegādātāja rēķina rindu duālās rakstīšanas kartes mērķa versija. |
| Laiks un izdevumi | 2700428 | Uzlabota apstiprinājumu loģika, lai nodrošinātu, ka citas projekta apstiprinājumu kopas var apstrādāt pat tad, ja viena no apstiprinājumu kopām ir iestrēgusi sistēmas uzdevumos. |

### <a name="project-management-and-accounting-in-finance"></a>Pārskats par projektu pārvaldību un uzskaiti pakalpojumā Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services (LCS) un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
