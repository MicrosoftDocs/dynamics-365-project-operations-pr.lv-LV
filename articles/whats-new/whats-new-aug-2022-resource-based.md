---
title: Jaunumi 2022. gada augustā — Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada augusta laidienā uz resursiem/nepiegādātiem scenārijiem.
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
- Projektu vadīšana un uzskaite Dynamics 365 Finance vidē versija 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Vienmēr palaidiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes, atjauninot project operations Dataverse risinājumu un finance risinājuma versiju. Daži līdzekļi un iespējas var nedarboties pareizi, ja kartes jaunākā versija nav aktivizēta. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja esat pielāgojis lietošanai gatavu tabulas karti, atkārtoti lietojiet izmaiņas. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja, startējot karti, rodas problēma, izpildiet norādījumus, kas sniegti [divrakstīšanas problēmu novēršanas ceļveža sadaļā Trūkstošās tabulas kolonnas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) kartēs.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
|   Iespēju pārvaldība | 2762089 | Kļūdu apstrāde, aizverot līgumu kā zaudētu, ja organizācijā ir atspējota automātiskā saglabāšana.|
|Projektu plānošana un izsekošana | 2767841 | Telemetrijas atjauninājumi Projekta entītija Izveidojiet vai atjauniniet scenārijus.|
|Cenu noteikšana un norēķini | 2771072 | Nulles atsauces izņēmuma apstrāde, uzvarot citātu.|
|Cenu noteikšana un norēķini | 2844181 |Nespēja iegūt korelācijas ID un bloķēt rēķina izveidi.|
|Cenu noteikšana un norēķini | 2852836 | Starpuzņēmumu faktiskie dati trūkst starpuzņēmumu izdevumiem, kas izveidoti un apstiprināti CE.|


### <a name="project-management-and-accounting-in-finance"></a>Projektu vadība un grāmatvedība finanšu jomā

Lai iegūtu informāciju par kļūdu labojumiem, kas ir iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services (LCS) un skatiet [zināšanu bāzes rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
