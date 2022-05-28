---
title: Jaunumi 2022. gada aprīlī — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada aprīļa laidienā resursiem/neuzkrātiem scenārijiem.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613357"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. gada aprīlī — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šī tēma attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projekta operācijas Dataverse vides versijā 4.41.0.45
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.26

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Sagādes kategorijas var izmantot projekta pirkšanas pasūtījumos un gaidošajos kreditoru rēķinos. Plašāku informāciju skatiet Use [procurement categories with project purchase orders and pending vendor invoices](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā tabulā parādītas divu rakstīšanas kartes, kas ir modificētas vai pievienotas projekta darbību 2022. gada marta laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| -------------- | ------------------- | ------------|
| Projekta operāciju integrācija projekta kreditora rēķina rindas eksporta entītija msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Šī karte atbalsta sagādes kategoriju izmantošanu ar pirkšanas pasūtījumiem un gaidošiem kreditoru rēķiniem. |

Atjauninot projektu operāciju Dataverse risinājumu un Finance risinājuma versiju, vienmēr palaidiet vidē jaunāko kartes versiju un iespējojiet visas saistītās tabulu kartes. Daži līdzekļi un iespējas var nedarboties pareizi, ja jaunākā kartes versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas [sniegti dual-write problēmu novēršanas rokasgrāmatas sadaļā Trūkstošo tabulu kolonnu problēma karšu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sadaļā.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| ------------ | ---------------- | -------------- |
| Laiks un izdevumi | 2573900 | Modernā **apstiprinājuma** līdzeklis ir jāiespējo pēc noklusējuma. |
| Cenu noteikšana un norēķini | 2603313 | Novērsa ieraksta dublikāta kļūdu, kas neļāva pievienot piedāvājuma un līguma rindas, kurām ir prece. |
| Izvietošana un konfigurēšana | 2611368 | Izmantojot moderno lietotņu noformētāju, klientiem risinājumam ir jāpievieno ne vairāk kā piecas pielāgotas entītijas. |
| Laiks un izdevumi | 2628285 | Novērsta problēma, kas ietekmēja iespēju iestatīt pareizo resursu kategoriju importēšanas laikā. |
|   Iespēju pārvaldība| 2628815 | Atjauniniet piedāvājuma rindas detalizētās informācijas apraksta rakstzīmju ierobežojumu, lai tas atbilstu uzdevuma tēmas rakstzīmju ierobežojumam, lai importēšana izdotos uzdevumiem, kuros tēma ir garāka par 100 rakstzīmēm. |
| Laiks un izdevumi| 2629547 | Projekta **apstiprinājumu laukam Iesniegts** jānorāda uz lietotāju, kurš iesniedzis ierakstu. |
| Laiks un izdevumi| 2629865 | Lauku **Kopēt kategoriju** uzdevumiem, kad projekti tiek kopēti. |
| Laiks un izdevumi| 2636463 | Laboja filtrus apstiprinājumiem modernās apstiprinājumu veidlapās. |
| Projektu plānošana un izsekošana | 2648300 | Novērsta problēma, kas neļauj mainīt projekta īpašnieku. |
| Cenu noteikšana un norēķini | 2563000 | Nedrīkst atļaut žurnāla rindas neierobežotai pārdošanai, ja valūta atšķiras no līguma valūtas. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektu vadība un grāmatvedība Dynamics 365 Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas ir iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics lifecycle services (LCS) un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
