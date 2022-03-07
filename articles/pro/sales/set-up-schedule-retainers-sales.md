---
title: Honorāru grafika iestatīšana
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt honorāra grafiku risinājumā Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a1cfd83837a91a8d1b3db6df688da6e216a90ada4735e5909a7e8cb26b87247d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994375"
---
# <a name="set-up-a-retainer-schedule"></a>Honorāru grafika iestatīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Honorāra grafiki tiek iestatīti lapā **Projekta līgums** pakalpojumā Dynamics 365 Project Operations.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]