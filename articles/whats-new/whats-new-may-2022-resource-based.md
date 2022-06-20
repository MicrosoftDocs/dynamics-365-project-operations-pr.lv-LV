---
title: Jaunumi 2022. gada maijā — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada maija laidienā resursu/neuzkrātu scenāriju gadījumā.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921403"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. gada maijā — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projekta operācijas Dataverse vides versijā 4.42.0.70
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot projektu operāciju Dataverse risinājumu un Finance risinājuma versiju, vienmēr palaidiet vidē jaunāko kartes versiju un iespējojiet visas saistītās tabulu kartes. Daži līdzekļi un iespējas var nedarboties pareizi, ja jaunākā kartes versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas [sniegti dual-write problēmu novēršanas rokasgrāmatas sadaļā Trūkstošo tabulu kolonnu problēma karšu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sadaļā.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi
### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Resursu pārvaldība | 2634019 | Uzlaboti kļūdu ziņojumi biznesa validācijām, pievienojot vispārīgus grupas dalībniekus kā resursus. |
| Projektu plānošana un izsekošana | 2648515 | Ierobežoti **ownerid**, **stāvokļa** un **statusa** atjauninājumi plānošanas entītijās. |
| Cenu noteikšana un norēķini | 2653167 | Tāmes **režģa** decimāldaļu atdalītājam ir jāatbilst personisko opciju **formāta iestatījumiem**. |
| Cenu noteikšana un norēķini| 2662251 | Vērtības laukos Labotā **vienība** un **Vienība pēc** noklusējuma, veidojot ierakstus materiālu novērtējumos. |
| Cenu noteikšana un norēķini| 2571408 | Veidojot rēķina melnrakstu, nemainīgās pārdošanas faktiskās versijas tiek apzīmogotas ar proformas rēķina ID. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektu vadība un grāmatvedība Dynamics 365 Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas ir iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics lifecycle services (LCS) un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
