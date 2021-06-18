---
title: Uz projektu balstītas iespēju rindas — Lite
description: Šajā tēmā ir sniegta informācija par iespēju rindām, kuras ir balstītas uz projektu. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 90b1b078d51c2842f6406c4455188a4433820a77
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994415"
---
# <a name="project-based-opportunity-lines---lite"></a>Uz projektu balstītas iespēju rindas — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta iespēju rindas ir pieejamas tikai projekta iespējās. Projekta iespēju ierakstiem lauka vērtība **Tips** ir iestatīta kā **Balstīts uz darbu**.

Projektu iespēju rindas ir rindas vienumi, kas tiks nodrošināti klientam, izmantojot projektu. Tomēr projektu nevar saistīt ar projekta iespēju rindu. Projektus var saistīt ar rindas vienumiem no posma **Piedāvājums** un tālāk, jo parasti iespēja ir darījuma dzīves cikla agrīnā posmā. To, cik daudz projektu tiks izmantots, lai izpildītu darbu klientam, ir lēmums, kas vēlāk tiks pieņemts pārdošanas fāzē. Iespējas fāzi var izmantot, lai identificētu diskrētos izpildes komponentus klientam. Lēmumus saistībā ar šo komponentu izpildei izmantoto projektu faktisko skaitu var virzīt cauri, līdz ir zināms vairāk informācijas par pašu darbu.

Tālāk ir uzskaitīti lauki projekta iespējas rindā.

| **Lauks** | **Atrašanās vieta** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Preces tips | Cilne Vispārīgi (slēpta) | Varat atlasīt vienu no šīm opcijām:</br>- Projekta pakalpojumi (pieejami tikai tad, ja Dynamics 365 Project Operations ir instalēts)</br>- Produkts (pieejams tikai tad, ja ir instalēts Project Operations un Dynamics 365 Sales) | Šī lauka vērtība tiek iestatīta uz **Projekta pakalpojums**, kad iespējai tiek izveidota projekta iespēju rinda no projekta rindu režģa. <br> Ja šī vērtība tiek mainīta vai ignorēta, projekta funkcionalitāte projekta rindas vienumiem netiks iespējota. |
| Iespēja | Cilne Vispārīgi | Šis lauks ir tikai lasāms, un tajā ir atsauce uz primāro iespējas ierakstu, kam pieder šis rindas vienums. | Šim laukam nav lejupstraumes ietekmes. |
| Nosaukums/vārds, uzvārds | Cilne Vispārīgi | Šis rediģējamais teksta lauks ir izmantojams, lai rindas vienumam piešķirtu īsu identitāti. | Šī vērtība tiek pārnesta uz piedāvājuma rindu, veidojot piedāvājumu no šīs iespējas. |
| Klienta budžets | Cilne Vispārīgi | Šo rediģējamo valūtas lauku var izmantot, lai izsekotu summu, ko klients ir gatavs tērēt šim rindas vienumam. | Šī vērtība tiek pārnesta uz atbilstošo lauku piedāvājuma rindā, veidojot piedāvājumu no šīs iespējas. |
| Rēķinu izrakstīšanas metode | Cilne Vispārīgi | Šim rediģējamajam laukam ir šādas vērtības:</br>- laiks un materiāli;</br>- fiksēta cena. | Šī vērtība tiek pārnesta uz atbilstošo lauku piedāvājuma rindā, veidojot piedāvājumu no šīs iespējas. Pēc tam, kad ir izveidota piedāvājuma rinda, lauks tiek bloķēts, un to nevar mainīt. Piešķiriet šī lauka vērtību, cik precīzi vien iespējams. Ja šī lauka vērtība ir jāmaina piedāvājuma rindā, dzēsiet piedāvājuma rindu un izveidojiet to atkārtoti. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]