---
title: Jaunumi 2022. gada maijā — Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2022. gada maija laidienā programmā Microsoft Dynamics 365 Project Operations resursos/noliktavā neesošos krājumos balstītiem scenārijiem.
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

- Project Operations Dataverse vides versijā 4.42.0.70
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.26.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi
### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Resursu pārvaldība | 2634019 | Uzlaboti kļūdu ziņojumi uzņēmējdarbības pārbaudēm, pievienojot vispārējus darba grupas dalībniekus kā resursus. |
| Projektu plānošana un izsekošana | 2648515 | Ierobežoti **ownerid**, **state** un **status** atjauninājumi entītiju plānošanā. |
| Cenu noteikšana un norēķini | 2653167 | Režģa **Aprēķini** decimālatdalītājam ir jāatbilst formāta iestatījumiem sadaļā **Personiskās opcijas**. |
| Cenu noteikšana un norēķini| 2662251 | Vērtībām laukos **Labotā vienība** un **Vienību grupa** tiek atjaunoti noklusējuma iestatījumi, veidojot ierakstus materiālu aprēķinos. |
| Cenu noteikšana un norēķini| 2571408 | Rēķinos neiekļautas faktiskās pārdošanas tiek apzīmogotas ar pro formas rēķina ID, veidojot rēķina melnrakstu. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektu pārvaldība un uzskaite programmā Dynamics 365 Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services (LCS) un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
