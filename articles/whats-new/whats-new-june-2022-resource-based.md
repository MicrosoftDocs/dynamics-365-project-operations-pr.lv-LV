---
title: Jaunumi 2022. gada jūnijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada jūnija laidienā resursiem/nepiegādātiem scenārijiem.
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

- Project Operations Dataverse vides versijā 4.43.0.77 vai 4.43.0.119
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Nākamajā tabulā ir parādītas divu rakstu kartes, kas ir modificētas vai pievienotas projekta operāciju 2022. gada jūnija laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| --- | --- | --- |
| Project Operations integrācijas projekta piegādātāju rēķinu eksportēšanas entītija (msdyn_projectvendorinvoices) | 1.0.0.1 | Novecojis mantotais lauks un kartēts uz jauno lauku kreditoru rēķinu stāvokļa izsekošanai. |

Vienmēr palaidiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes, atjauninot project operations Dataverse risinājumu un finance risinājuma versiju. Daži līdzekļi un iespējas var nedarboties pareizi, ja kartes jaunākā versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis lietošanai gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas sniegti [divrakstīšanas problēmu novēršanas ceļveža sadaļā Trūkstošās tabulas kolonnas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) kartēs.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Apakšuzņēmuma līgumi | 2708885 | Novērsta kļūda, kas tiek parādīta, kad lietotājs izveido rezervējamu resursu rezervācijas galvenes ierakstu, kurā nav aizpildīts rezervējams resurss. |
| Projektu plānošana un izsekošana | 2629441 | Laboja darbplūsmas aktivizēšanas loģiku, lai palīdzētu novērst bezgalīgu cilpu, kad projekta uzdevumi tiek atjaunināti. |
| Laiks un izdevumi | 2641209 | Laika ieraksta importēšanai no uzdevumiem/rezervācijām ir jāsaglabā atsauce uz rezervējamiem resursiem. |
| Projektu plānošana un izsekošana | 2651148 | Projekta dokumenta galvene ir jāsargā.|
| Projektu plānošana un izsekošana | 2653145 | Pievienotas validācijas, lai nodrošinātu, ka nevar izveidot projekta ierakstu, kura nosaukumā ir nederīgas rakstzīmes. |
| Laiks un izdevumi | 2654710 | Labota filtrēšana **lapā Apstiprinājumi**. |
| Cenu noteikšana un norēķini | 2667805 | Pievienotas validācijas, lai novērstu rēķinā norādīto pārdošanas faktisko vērtību izveidi, ja nepastāv nesamaksāto pārdošanas faktisko rezultātu dublēšana. |
| Cenu noteikšana un norēķini | 2668378 | Pievienotas validācijas, lai novērstu pielāgotas cenu dimensijas pievienošanu, ja vien nav aizpildīts loģiskais nosaukums un lauka nosaukums. |
| Apakšuzņēmuma līgumi | 2677485 | Atjaunināta kreditoru rēķinu līniju dubultās rakstīšanas kartes mērķa versija. |
| Laiks un izdevumi | 2700428 | Uzlabota apstiprinājumu loģika, lai nodrošinātu, ka citas projekta apstiprināšanas kopas var apstrādāt pat tad, ja viena no apstiprināšanas kopām ir iestrēgusi sistēmas darbos. |

### <a name="project-management-and-accounting-in-finance"></a>Projektu vadība un grāmatvedība finanšu jomā

Lai iegūtu informāciju par kļūdu labojumiem, kas ir iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services (LCS) un skatiet [zināšanu bāzes rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
