---
title: Honorāra grafika iestatīšana — Lite
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt honorāra grafiku risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181281"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Honorāra grafika iestatīšana — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Honorāra grafiki tiek iestatīti lapā **Projekta līgums** pakalpojumā Dynamics 365 Project Operations.

1. Lapas **Projekta līgums** cilnē **Avansi un honorāri** atlasiet **Iestatīt honorāra grafiku**.
2. Atvērtajā dialoga lapā tiek parādīti tālāk redzamajā tabulā uzskaitītie lauki. Tabulā ir sniegts priekšstats par to, kā ievadītās vērtības ietekmē vai iespaidos honorāra grafiku, kas tiks izveidots.

| Lauks | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- |
| Projekta līguma klients | Līgumā paredzētais klients, kuram tiks izrakstīts rēķins par šo honorāru vai avansu. | Ja līgumā ir vairāki klienti un katram no tiem nepieciešams izrakstīt rēķinu par noteiktu honorāru vai avansa summu, manuāli izveidojiet vienu rēķinu katram klientam. |
| Honorāru grafika sākums | Ievadiet honorāra grafika sākuma datumu. | Šis datums var arī nebūt diena, kurā ir izveidots pirmais honorārs vai avanss. Rēķina biežums ietekmē arī datumu, kurā ir izveidots pirmais honorārs vai avanss. |
| Honorāru grafika beigas | Ievadiet honorāra grafika beigu datumu. | Šis datums var arī nebūt diena, kurā ir izveidots pēdējais honorārs vai avanss. Rēķina biežums ietekmē arī datumu, kurā ir izveidots pēdējais honorārs vai avanss. |
| Veidojamo honorāru skaits | Kad tiek ievadīts izveidojamo honorāru skaits, sistēma izmanto sākuma datumu un biežumu, lai šajā laukā izveidotu numuru. | Ja šis lauks tiek atjaunināts manuāli, sistēma ignorē vērtību laukā **Honorāra grafika beigas** un tā vietā izveido noteiktu honorāru vai avansu skaitu. |
| Rēķina izrakstīšanas biežums | Cik bieži lietojumprogramma izveidos honorārus un avansus. | Šī vērtība tieši ietekmē honorāru un avansu skaitu un izveidotos datumus. |
| Kopsumma | Kopsumma ir summa, kas sadalīta atsevišķos honorāra vai avansa maksājumos, kas tiks izveidoti. | Šim laukam nav lejupstraumes ietekmes. |
