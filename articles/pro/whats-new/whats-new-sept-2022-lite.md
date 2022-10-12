---
title: Jaunumi 2022. gada septembra Project Operations Lite izvietošanā
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami Microsoft Dynamics 365 Project Operations lite izvietošanas 2022. gada septembra laidienā.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621355"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Jaunumi 2022. gada septembra Project Operations Lite izvietošanā

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.46.0.60

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

| Līdzekļu apgabals | Līdzekļa nosaukums | Papildinformācija |
| --- | --- | --- |
| Iespēju pārvaldība | **Citātu pārskatīšana un aktivizēšana**<br>Project Operations nodrošina pilnu pārdošanas procesa atbalstu. Projekta citātus var aktivizēt, lai attēlotu stāvokli, kurā piedāvājums ir tikai lasāms un tiek pārskatīts. Aktivizētos citātus var pārskatīt, lai izveidotu jaunus citātus, kuriem ir palielināts pārskatījuma numurs. Aktivizētos projekta citātus vai citātu pārskatījumus var aizvērt kā uzvarētus vai zaudētus. | [Projekta piedāvājuma aktivizēšana un pārskatīšana](/dynamics365/project-operations/sales/activation-and-revision) |
| Cenu noteikšana un norēķini | **Laika joslas agnostiskās cenas saistību neizpilde**<br>Project Operations ir ieviesis laika joslas agnostiskā datuma jēdzienu visos projekta faktiskajos datos. Jauns lauks **— Transakcijas datums** — tagad ir pieejams žurnāla rindās un faktiskajos datos, un tas tiks izmantots, lai saglabātu transakcijas veikšanas datumu, bet nekonvertējot šo datumu par universālo koordinēto laiku. Šis datums tiks izmantots pakārtotiem procesiem, piemēram, cenu saistību neizpildei un rēķinu izveidei. | <p>[Uz projektiem balstītu aplēšu un faktisko izmaksu likmju noteikšana](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Pārdošanas cenu noteikšana uz projektiem balstītām aplēsēm un faktiskajiem datiem](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Cenu noteikšana un norēķini | **Datuma spēkā esošās cenas ignorēšana programmā Project Operations**<br>Datuma spēkā stāšanās cenu ignorēšana nodrošina veidu, kā ignorēt vai mainīt konkrētas cenas cenrādī. | [Datuma spēkā esošā cena ignorē](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Laiks un izdevumi | **Globālais apstiprinātājs**<br>Šis līdzeklis iespējo neatkarīgu programmatūras piegādātāju (ISV) un centralizētu apstiprināšanu neatkarīgi no projekta vai darba grupas dalībnieka statusa projektā. | [Drošība un apstiprinājumi](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Cenu noteikšana un norēķini | 2754422 | Materiālu un izdevumu aprēķini neplūst uz Dynamics 365 Finance, kad projekti tiek kopēti Dataverse. |
| Laiks un izdevumi | 2787409 | Nederīgs apstiprinātājs var apstiprināt ierakstu par laiku, kas nav saistīts ar projektu. |
| Iespēju pārvaldība | 2788907 | Atjaunināts kļūdas ziņojums par unikalitātes validāciju pasūtījuma rindām, kurās ir karodziņi. |
| Laiks un izdevumi | 2842253 | Nulles izņēmuma apstrāde laika apstiprināšanai. |
| Cenu noteikšana un norēķini | 2844181 | Nespēja iegūt korelācijas ID bloķē rēķina izveidi. |
| Cenu noteikšana un norēķini | 2876628 | QLD, CLD - aplēses cenrāža izšķirtspējai jāizmanto cenrāža mantotie datumu diapazona lauki. |
| Apakšuzņēmuma līgumi | 2893222 | Ja apakšlīguma līnijai nav norādīta neviena loma, vajadzētu būt iespējai izvēlēties šo rindu no komandas dalībnieka jebkurai lomai. |
