---
title: Jaunumi 2022. gada jūnijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada jūnija laidienā, laidienā uz resursiem/neuzkrātiem scenārijiem.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959682"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. gada jūnijā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projekta operācijas Dataverse vides versijā 4.43.0.77
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā tabulā ir parādītas divu rakstīšanas kartes, kas ir modificētas vai pievienotas projekta operāciju 2022. gada jūnija laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| --- | --- | --- |
| Project Operations integrācijas projekta piegādātāju rēķinu eksportēšanas entītija (msdyn_projectvendorinvoices) | 1.0.0.1 | Novecojis mantotais lauks un kartēts uz jauno lauku kreditora rēķina stāvokļa izsekošanai. |

Atjauninot projektu operāciju Dataverse risinājumu un Finance risinājuma versiju, vienmēr palaidiet vidē jaunāko kartes versiju un iespējojiet visas saistītās tabulu kartes. Daži līdzekļi un iespējas var nedarboties pareizi, ja jaunākā kartes versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas [sniegti dual-write problēmu novēršanas rokasgrāmatas sadaļā Trūkstošo tabulu kolonnu problēma karšu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sadaļā.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Apakšuzņēmuma līgumi | 2708885 | Novērsts kļūdas ziņojums, kas tiek parādīts, kad lietotājs izveido rezervējamu resursu rezervēšanas virsraksta ierakstu, kurā nav aizpildīts rezervējams resurss. |
| Projektu plānošana un izsekošana | 2629441 | Laboja darbplūsmas aktivizēšanas loģiku, lai palīdzētu novērst bezgalīgu cilpu, atjauninot projekta uzdevumus. |
| Laiks un izdevumi | 2641209 | Laika ieraksta importēšanai no cesijām/rezervācijām jāsaglabā rezervējamā resursa atsauce. |
| Projektu plānošana un izsekošana | 2651148 | Projekta dokumenta virsraksts ir jāsargā.|
| Projektu plānošana un izsekošana | 2653145 | Pievienotas pārbaudes, lai nodrošinātu, ka nevar izveidot projekta ierakstu, kura nosaukumā ir nederīgas rakstzīmes. |
| Laiks un izdevumi | 2654710 | Laboja filtrēšanu **lapā Apstiprinājumi**. |
| Cenu noteikšana un norēķini | 2667805 | Pievienotas pārbaudes, kas palīdz novērst rēķinā iekļautās pārdošanas faktisko datu izveidi, ja nepastāv nemainīgas pārdošanas faktiskās summas. |
| Cenu noteikšana un norēķini | 2668378 | Pievienotas pārbaudes, kas palīdz novērst pielāgotas cenu kategorijas pievienošanu, ja vien nav aizpildīts loģiskais nosaukums un lauka nosaukums. |
| Apakšuzņēmuma līgumi | 2677485 | Atjaunināja kreditora rēķina rindu divrakstīšanas kartes mērķa versiju. |
| Laiks un izdevumi | 2700428 | Uzlabota apstiprinājumu loģika, lai nodrošinātu, ka citas projekta apstiprināšanas kopas var apstrādāt pat tad, ja kāda no apstiprināšanas kopām ir iestrēgusi sistēmas darbos. |

### <a name="project-management-and-accounting-in-finance"></a>Projektu vadība un grāmatvedība finansēs

Lai iegūtu informāciju par kļūdu labojumiem, kas ir iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics lifecycle services (LCS) un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
