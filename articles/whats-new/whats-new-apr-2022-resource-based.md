---
title: Jaunumi 2022. gada aprīlī — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada aprīļa laidienā resursu/neuzkrātu scenāriju gadījumā.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110893"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. gada aprīlī — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.41.0.45
- Projektu vadība un uzskaite Dynamics 365 Finance vidē versija 10.0.26

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Sagādes kategorijas var izmantot projektu pirkšanas pasūtījumos un gaidošajos kreditoru rēķinos. Papildinformāciju skatiet rakstā [Sagādes kategoriju izmantošana ar projektu pirkšanas pasūtījumiem un gaidošajiem kreditoru rēķiniem](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Nākamajā tabulā ir parādītas divu rakstu kartes, kas ir modificētas vai pievienotas Project Operations 2022. gada marta laidienā.

| Entītiju karte | Atjauninātā versija | Komentāri |
| -------------- | ------------------- | ------------|
| Project Operations integrācijas projekta kreditora rēķina rindas eksportēšanas entītija msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Šī karte atbalsta sagādes kategoriju izmantošanu ar pirkšanas pasūtījumiem un gaidošiem kreditoru rēķiniem. |

Vienmēr palaidiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes, atjauninot project operations Dataverse risinājumu un finance risinājuma versiju. Daži līdzekļi un iespējas var nedarboties pareizi, ja kartes jaunākā versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis lietošanai gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas sniegti [divrakstīšanas problēmu novēršanas ceļveža sadaļā Trūkstošās tabulas kolonnas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) kartēs.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| ------------ | ---------------- | -------------- |
| Laiks un izdevumi | 2573900 | Līdzeklis **Modern Approval** ir jāiespējo pēc noklusējuma. |
| Cenu noteikšana un norēķini | 2603313 | Novērsta dubulta ieraksta kļūda, kas neļāva pievienot citātu un līguma rindas, kurām ir prece. |
| Izvietošana un konfigurācija | 2611368 | Klientiem ir jābūt iespējai pievienot risinājumam līdz pat piecām pielāgotām entītijām, izmantojot moderno programmu noformētāju. |
| Laiks un izdevumi | 2628285 | Novērsta problēma, kas ietekmēja iespēju iestatīt pareizo resursu kategoriju laika ieraksta importēšanas laikā. |
|   Iespēju pārvaldība| 2628815 | Atjauniniet citāta rindiņas detalizētās informācijas apraksta rakstzīmju ierobežojumu, lai tas atbilstu uzdevuma tēmas rakstzīmju ierobežojumam, lai importēšana izdotos uzdevumiem, kuru tēma ir garāka par 100 rakstzīmēm. |
| Laiks un izdevumi| 2629547 | Projekta **apstiprinājumu laukam Iesniegts ir** jānorāda uz lietotāju, kurš iesniedzis ierakstu. |
| Laiks un izdevumi| 2629865 | Lauks **Kopēt kategoriju** uzdevumiem, kad projekti tiek kopēti. |
| Laiks un izdevumi| 2636463 | Fiksēja filtrus apstiprinājumiem modernās apstiprinājuma veidlapās. |
| Projektu plānošana un izsekošana | 2648300 | Novērsta problēma, kas neļauj mainīt projekta īpašnieku. |
| Cenu noteikšana un norēķini | 2563000 | Nedrīkst pieļaut žurnāla rindas par nebilātisku pārdošanu, ja valūta atšķiras no līguma valūtas. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektu vadība un grāmatvedība Dynamics 365 Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas ir iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services (LCS) un skatiet [zināšanu bāzes rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
