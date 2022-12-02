---
title: Jaunumi 2022. gada augustā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2022. gada augusta laidienā programmā Microsoft Dynamics 365 Project Operations resursos/noliktavā neesošos krājumos balstītiem scenārijiem.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403866"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. gada augustā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.45.0.53
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.28.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
|   Iespēju pārvaldība | 2762089 | Kļūdu apstrāde, aizverot līgumu kā zaudētu, ja organizācijā ir atspējota automātiskā saglabāšana.|
|Projektu plānošana un izsekošana | 2767841 | Telemetrija atjaunina projekta entītijas izveides vai atjaunināšanas scenārijus.|
|Cenu noteikšana un norēķini | 2771072 | Nulles atsauces izņēmuma apstrāde, iegūstot piedāvājumu.|
|Cenu noteikšana un norēķini | 2844181 |Kļūme, iegūstot korelācijas ID un bloķējot rēķina izveidi.|
|Cenu noteikšana un norēķini | 2852836 | Trūkst starpuzņēmumu faktisko datu starpuzņēmumu izdevumos, kas izveidoti un apstiprināti CE.|


### <a name="project-management-and-accounting-in-finance"></a>Pārskats par projektu pārvaldību un uzskaiti pakalpojumā Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services (LCS) un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
