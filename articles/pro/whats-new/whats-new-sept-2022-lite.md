---
title: Jaunumi 2022. gada septembra Project Operations Lite izvietošanā
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations lite izvietošanas 2022. gada septembra laidienā.
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

- Projekta operācijas Dataverse vides versijā 4.46.0.60

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

| Līdzekļu apgabals | Līdzekļa nosaukums | Papildinformācija |
| --- | --- | --- |
| Iespēju pārvaldība | **Citātu pārskatīšana un aktivizēšana**<br>Project Operations nodrošina pilnu pārdošanas procesa atbalstu. Projekta citātus var aktivizēt, lai attēlotu stāvokli, kurā citāts ir tikai lasāms un tiek pārskatīts. Aktivizētos citātus var pārskatīt, lai izveidotu jaunus citātus ar palielinātu pārskatīšanas numuru. Aktivizētos projektu citātus vai citātu pārskatījumus var aizvērt kā uzvarētus vai zaudētus. | [Projekta piedāvājuma aktivizēšana un pārskatīšana](/dynamics365/project-operations/sales/activation-and-revision) |
| Cenu noteikšana un norēķini | **Laika joslas agnostiskā cenas noklusēšana**<br>Project Operations ir ieviesis laika joslas agnostiskā datuma koncepciju visos projekta faktiskajos apstākļos. Jauns lauks **Transakcijas datums** tagad ir pieejams žurnāla rindās un faktiskajos datumos, un tas tiks izmantots, lai saglabātu datumu, kad transakcija notika, bet nepārvēršot šo datumu par universālo koordinēto laiku. Šis datums tiks izmantots pakārtotajiem procesiem, piemēram, cenu noklusēšanai un rēķinu izveidei. | <p>[Nosakiet izmaksu likmes uz projektiem balstītām aplēsēm un faktiskajiem datiem](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Nosakiet pārdošanas cenas uz projektiem balstītām aplēsēm un faktiskajiem datiem](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Cenu noteikšana un norēķini | **Datuma efektīvās cenas ignorēšana projekta darbībās**<br>Datuma spēkā stāšanās cenu ignorēšana nodrošina veidu, kā ignorēt vai mainīt konkrētas cenas cenrādī. | [Datuma spēkā stāšanās cenu ignorēšana](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Laiks un izdevumi | **Globālais apstiprinātājs**<br>Šis līdzeklis iespējo neatkarīgu programmatūras piegādātāju (ISV) un centralizētu apstiprināšanu neatkarīgi no projekta vai darba grupas dalībnieka statusa projektā. | [Drošība un apstiprinājumi](/dynamics365/project-operations/approvals/approvals-security) |
|Projektu plānošana un izsekošana|**Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām** </br> </br>Resursu piešķiršanas kontūras rediģēšanas API ļauj izstrādātājiem programmiski norādīt uzdevuma saņēmēja pūles jebkurā atbalstītajā datumu diapazonā, lai iegūtu detalizētāku laika pakāpenisku piepūles plānošanu.|[Projekta plānošanas API izmantošana, lai veiktu operācijas ar plānošanas entītijām](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2754422 | Materiālu un izdevumu aprēķini neplūst uz Dynamics 365 Finance, kad projekti tiek kopēti Dataverse. |
| Laiks un izdevumi | 2787409 | Nederīgs apstiprinātājs var apstiprināt ar projektu nesaistītu laika ierakstu. |
| Iespēju pārvaldība | 2788907 | Atjaunināts kļūdas ziņojums par unikalitātes validāciju pasūtījuma rindām, kurās ir karodziņi. |
| Laiks un izdevumi | 2842253 | Nulles izņēmuma apstrāde laika apstiprināšanai. |
| Cenu noteikšana un norēķini | 2844181 | Ja neizdodas iegūt korelācijas ID, tiek bloķēta rēķina izveide. |
| Cenu noteikšana un norēķini | 2876628 | QLD, CLD — novērtējuma cenrāža izšķirtspējā jāizmanto cenrāža mantotie datumu diapazona lauki. |
| Apakšuzņēmuma līgumi | 2893222 | Ja apakšuzņēmuma līguma rindai nav norādīta neviena loma, vajadzētu būt iespējai atlasīt šo līniju no komandas dalībnieka jebkurai lomai. |
