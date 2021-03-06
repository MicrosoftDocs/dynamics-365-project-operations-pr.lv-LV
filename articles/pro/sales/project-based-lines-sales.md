---
title: Uz projektiem balstītas iespēju rindas (Pro)
description: Šajā tēmā ir sniegta informācija par iespēju rindām, kuras ir balstītas uz projektu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896380"
---
# <a name="project-based-opportunity-lines-pro"></a>Uz projektiem balstītas iespēju rindas (Pro)

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta iespēju rindas ir pieejamas tikai projekta iespējās. Projekta iespēju ierakstiem lauka vērtība **Tips** ir iestatīta kā **Balstīts uz darbu**.

Projektu iespēju rindas ir rindas vienumi, kas tiks nodrošināti klientam, izmantojot projektu. Tomēr projektu nevar saistīt ar projekta iespēju rindu. Projektus var saistīt ar rindas vienumiem no posma **Piedāvājums** un tālāk, jo parasti iespēja ir darījuma dzīves cikla agrīnā posmā. To, cik daudz projektu tiks izmantots, lai izpildītu darbu klientam, ir lēmums, kas vēlāk tiks pieņemts pārdošanas fāzē. Iespējas fāzi var izmantot, lai identificētu diskrētos izpildes komponentus klientam. Lēmumus saistībā ar šo komponentu izpildei izmantoto projektu faktisko skaitu var virzīt cauri, līdz ir zināms vairāk informācijas par pašu darbu.

Tālāk ir uzskaitīti lauki projekta iespējas rindā.

| **Lauks** | **Atrašanās vieta** | **Atbilstība, mērķis un norādes** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Preces tips | Cilne Vispārīgi (slēpta) | Varat atlasīt vienu no šīm opcijām:</br>- Projekta pakalpojums (pieejams tikai tad, ja ir instalēts Dynamics 365 Project Operations)</br>- Produkts (pieejams tikai tad, ja ir instalēts Project Operations un Dynamics 365 Sales) | Šī lauka vērtība tiek iestatīta uz **Projekta pakalpojums**, kad iespējai tiek izveidota projekta iespēju rinda no projekta rindu režģa. <br> Ja šī vērtība tiek mainīta vai ignorēta, projekta funkcionalitāte projekta rindas vienumiem netiks iespējota. |
| Iespēja | Cilne Vispārīgi | Šis lauks ir tikai lasāms, un tajā ir atsauce uz primāro iespējas ierakstu, kam pieder šis rindas vienums. | Šim laukam nav lejupstraumes ietekmes. |
| Nosaukums/vārds, uzvārds | Cilne Vispārīgi | Šis rediģējamais teksta lauks ir izmantojams, lai rindas vienumam piešķirtu īsu identitāti. | Šī vērtība tiek pārnesta uz piedāvājuma rindu, veidojot piedāvājumu no šīs iespējas. |
| Klienta budžets | Cilne Vispārīgi | Šo rediģējamo valūtas lauku var izmantot, lai izsekotu summu, ko klients ir gatavs tērēt šim rindas vienumam. | Šī vērtība tiek pārnesta uz atbilstošo lauku piedāvājuma rindā, veidojot piedāvājumu no šīs iespējas. |
| Rēķinu izrakstīšanas metode | Cilne Vispārīgi | Šim rediģējamajam laukam ir šādas vērtības:</br>- laiks un materiāli;</br>- fiksēta cena. | Šī vērtība tiek pārnesta uz atbilstošo lauku piedāvājuma rindā, veidojot piedāvājumu no šīs iespējas. Pēc tam, kad ir izveidota piedāvājuma rinda, lauks tiek bloķēts, un to nevar mainīt. Piešķiriet šī lauka vērtību, cik precīzi vien iespējams. Ja šī lauka vērtība ir jāmaina piedāvājuma rindā, dzēsiet piedāvājuma rindu un izveidojiet to atkārtoti. |
