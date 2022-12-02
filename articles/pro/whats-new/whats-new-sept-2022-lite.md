---
title: Jaunumi 2022. gada septembra Project Operations Lite izvietošanā
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations lite izvietošanas 2022. gada septembra laidienā.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634862"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Jaunumi 2022. gada septembra Project Operations Lite izvietošanā

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.46.0.60

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

| Līdzekļu apgabals | Līdzekļa nosaukums | Papildinformācija |
| --- | --- | --- |
| Iespēju pārvaldība | **Piedāvājumu pārskatīšana un aktivizēšana**<br>Project Operations pilnībā atbalsta pārdošanas procesu. Projektu piedāvājumus var aktivizēt, lai atspoguļotu statusu, kurā piedāvājums ir tikai lasāms un tiek pārskatīts. Aktivizētos piedāvājumus var pārskatīt, lai izveidotu jaunus piedāvājumus ar palielinātu pārskatīšanas numuru. Aktivizētos projektu piedāvājumus vai piedāvājumu pārskatījumus var aizvērt kā iegūtus vai zaudētus. | [Projekta piedāvājuma aktivizēšana un pārskatīšana](/dynamics365/project-operations/sales/activation-and-revision) |
| Cenu noteikšana un norēķini | **No laika joslas neatkarīga cenas noklusējuma izmantošana**<br>Project Operations ir ieviesusi no laika joslas neatkarīgu datumu koncepciju visos projekta faktiskajos datos. Žurnāla rindās un faktiskajos datos tagad ir pieejams jauns lauks **Transakcijas datums**, kas tiks izmantots transakcijas datuma saglabāšanai, nepārvēršot šo datumu universālajā koordinētajā laikā. Šis datums tiks lietots lejupstraumes procesiem, piemēram, cenu noklusējumam un rēķinu izveidei. | <p>[Izmaksu likmju noteikšana projekta aprēķinos un faktiskajos datos](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Pārdošanas cenu noteikšana projekta aprēķinos un datos](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Cenu noteikšana un norēķini | **Datuma un spēkā esošās cenas pārlabošana programmā Project Operations**<br>Datuma un spēkā esošās cenas pārlabošana nodrošina veidu, kā pārlabot vai mainīt konkrētas cenas cenrādī. | [Datuma un spēkā esošās cenas pārlabošana](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Laiks un izdevumi | **Globālais apstiprinātājs**<br>Šis līdzeklis iespējo neatkarīga programmatūras izstrādātāja (ISV) un centralizētu apstiprināšanu neatkarīgi no projekta vai darba grupas dalībnieka statusa projektā. | [Drošība un apstiprinājumi](/dynamics365/project-operations/approvals/approvals-security) |
|Projektu plānošana un izsekošana|**Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām** </br> </br>Resursu piešķiršanas kontūras rediģēšanas API ļauj izstrādātājiem programmiski norādīt uzdevuma saņēmēja ieguldījumu jebkurā atbalstītajā datumu diapazonā, lai ļautu detalizētāk plānot ieguldījuma laika sadalījumu.|[Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2754422 | Kad projekti tiek kopēti Dataverse, materiālu un izmaksu aprēķini neplūst uz Dynamics 365 Finance. |
| Laiks un izdevumi | 2787409 | Nederīgs apstiprinātājs var apstiprināt projektam nepiederīgu laika ierakstu. |
| Iespēju pārvaldība | 2788907 | Atjaunināts kļūdas ziņojums par unikalitātes apstiprināšanu pasūtījuma rindām, kas ietver karodziņus. |
| Laiks un izdevumi | 2842253 | Nulles izņēmumu apstrāde laika apstiprināšanai. |
| Cenu noteikšana un norēķini | 2844181 | Neizdevās iegūt korelācijas ID, tāpēc tiek bloķēta rēķina izveide. |
| Cenu noteikšana un norēķini | 2876628 | QLD, CLD — aprēķinātajam cenrāža risinājumam ir jāizmanto cenrāža mantotie datumu diapazona lauki. |
| Apakšlīgumu slēgšana | 2893222 | Ja apakšlīguma rindai nav norādīta loma, šo rindu vajadzētu varēt atlasīt darba grupas dalībniekam jebkurai lomai. |
