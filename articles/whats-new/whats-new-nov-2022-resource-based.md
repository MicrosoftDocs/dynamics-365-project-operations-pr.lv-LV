---
title: Jaunumi 2022. novembrī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations 2022. gada novembra laidienā scenārijiem, kuru pamatā ir resursi/krājumi.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831135"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. novembrī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.58.0.119
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.30.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Šajā laidienā Project Operations duālās rakstīšanas kartēm nav atjauninājumu. Pašreizējo Project Operations duālās rakstīšanas karšu sarakstu un versijas skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../environment/resource-dual-write-maps.md).

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2781818 | Atslēga nav atrasta kļūda, noklusējot cenu materiālu izmantošanas žurnālam. |
| Cenu noteikšana un norēķini | 2922373 | Nevar saistīt citāta rindiņu ar projektu, kas ir aizvērts kā pazaudēts citāts. |
| Cenu noteikšana un norēķini | 2943206 | **Laukam Līguma rinda** projekta struktūrā jābūt neobligātam. |
| Cenu noteikšana un norēķini | 2953182 | Uzlabojiet kļūdu ziņojumu labošanas rēķiniem.|
| Cenu noteikšana un norēķini | 2959500 | Nevar saistīt citāta rindiņu ar projekta uzdevumu, kas jau ir saistīts ar pazaudētu piedāvājumu.|
| Cenu noteikšana un norēķini | 2959560 | "Šis klients jau ir iekļauts Projekta līgumā" ziņojums, kas saņemts, noslēdzot piedāvājumu, kā uzvarēts noteiktās vietās. |
| Cenu noteikšana un norēķini | 3031727 | Resursu piešķiršana neizdodas, jo trūkst kļūdas laukā Obligātais lauks "msdyn_Company". |
| Cenu noteikšana un norēķini | 3036905 | Piederošais uzņēmums nekad netiek inicializēts ProjectTeamMember. |
| Iespēju pārvaldība | 2763519 | Nulles atsauces kļūda programmā EnsureProjectContractAllowsUpdates. |
| Iespēju pārvaldība | 2783798 | Importējot projekta tāmes piedāvājuma rindā, trūkst uzdevumu aprakstu izdevumu un materiālu tāmēm.|
| Iespēju pārvaldība | 2988635 | Uzlabojiet kļūdas msg aprakstu, dzēšot klientu piedāvājumā. |
| Iespēju pārvaldība | 3001191 | Nevar izveidot piedāvājumu no iespējas, kur norēķinu metode ir norādīta kā Null. |
| Jaunināšana | 3012324 | Projekta konvertēšana neizdevās projektā, kura nosaukumā bija vadīklas rakstzīmes, piemēram, Tab. || Projektu plānošana un izsekošana | 2790384 | Pending OperationSet taimauts ir pārāk īss. |
| Projektu plānošana un izsekošana | 3044275 | Trūkst lokalizācijas: missingProjectSchedulerErrorMessage. |
| Projektu plānošana un izsekošana | 3044277 | Project Recon režģis netiek ielādēts, kad plānotājs ir atiestatīts.|
| Resursu pārvaldība | 2943153 | Atjauniniet cilni Izsekošana, lai parādītu divas decimāldaļas uz Ilgums.|
| Apakšlīgumu slēgšana | 2932774 | Kreditora rēķina rindiņa Lasīt Tikai nepareizi izmetot kļūdu. |
| Apakšlīgumu slēgšana | 2939556 | Kreditora rēķina galvenes statuss nav jāiestata uz Melnraksts tiešsaistes dzēšana, ja tas nav aktīvs. |
| Laiks un izdevumi | 2939998 | Apgūstiet jauno TESA versiju ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Pārskats par projektu pārvaldību un uzskaiti pakalpojumā Finance

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti šajā atjauninājumā, piesakieties Microsoft Dynamics Lifecycle Services un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
