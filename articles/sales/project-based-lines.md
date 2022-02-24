---
title: Uz projektiem balstītas iespēju rindas
description: Šajā tēmā ir sniegta informācija par darbu ar iespēju rindām, kuras ir balstītas uz projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ede474e3d8830b420dc5b183f14327206c10288
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181956"
---
# <a name="project-based-opportunity-lines"></a>Uz projektiem balstītas iespēju rindas

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_


Projekta iespēju rindas ir pieejamas tikai projekta iespējās. Projekta iespēju ierakstiem lauka vērtība **Tips** ir iestatīta kā **Balstīts uz darbu**.

Projektu iespēju rindas ir rindas vienumi, kas tiks nodrošināti klientam, izmantojot projektu. Tomēr projektu nevar saistīt ar projekta iespēju rindu. Projektus var saistīt ar rindas vienumiem no posma **Piedāvājums** un tālāk, jo parasti iespēja rodas darījuma dzīves cikla agrīnā posmā. To, cik daudz projektu tiks izmantots, lai izpildītu darbu klientam, ir lēmums, kas vēlāk tiks pieņemts pārdošanas fāzē. Izmantojiet iespējas fāzi, lai identificētu diskrētos izpildes komponentus klientam. Lēmumus saistībā ar šo komponentu izpildei izmantoto projektu faktisko skaitu var virzīt cauri, līdz ir zināms vairāk informācijas par pašu darbu.

Tālāk ir uzskaitīti lauki projekta iespējas rindā.

| **Lauks** | **Atrašanās vieta** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Preces tips | Cilne Vispārīgi (slēpta) | Šis ir opciju kopas lauks. Ja ir instalēts Dynamics 365 Operations, viena no pieejamajām opcijām ir **Projekta pakalpojums**.  | Šī lauka vērtība tiek iestatīta uz **Projekta pakalpojums**, kad iespējai tiek izveidota projekta iespēju rinda no projekta rindu režģa. <br> Ja šī vērtība tiek mainīta vai ignorēta, projekta funkcionalitāte projekta rindas vienumiem netiks iespējota. |
| Iespēja | Cilne Vispārīgi | Šis lauks ir tikai lasāms, un tajā ir atsauce uz primāro iespējas ierakstu, kam pieder šis rindas vienums. | Šim laukam nav lejupstraumes ietekmes. |
| Nosaukums/vārds, uzvārds | Cilne Vispārīgi | Šis ir rediģējams teksta lauks, ko var izmantot, lai šim rindas vienumam piešķirtu īsu identitāti | Šī vērtība tiek pārnesta uz piedāvājuma rindu, veidojot piedāvājumu no šīs iespējas |
| Klienta budžets | Cilne Vispārīgi | Šo rediģējamo valūtas lauku var izmantot, lai izsekotu summu, ko klients ir gatavs tērēt šim rindas vienumam. | Šī vērtība tiek pārnesta uz atbilstošo lauku piedāvājuma rindā, veidojot piedāvājumu no šīs iespējas |
| Rēķinu izrakstīšanas metode | Cilne Vispārīgi | Šim rediģējamajam laukam ir šādas vērtības:</br>- laiks un materiāli;</br>- fiksēta cena. | Šī vērtība tiek pārnesta uz atbilstošo lauku piedāvājuma rindā, veidojot piedāvājumu no šīs iespējas. Pēc tam, kad ir izveidota piedāvājuma rinda, lauks tiek bloķēts, un to nevar mainīt. Piešķiriet šī lauka vērtību, cik precīzi vien iespējams. Ja šī lauka vērtība ir jāmaina piedāvājuma rindā, dzēsiet piedāvājuma rindu un izveidojiet to atkārtoti. |
