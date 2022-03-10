---
title: Produktu izmaksu aprēķina līgumu rindas — Lite
description: Šajā tēmā ir sniegta informācija par izveidi
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55f74b016b55945433083e11902003cea99f1aa463264cdd95b0aad389592e20
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997345"
---
# <a name="cost-product-based-contract-lines---lite"></a>Produktu izmaksu aprēķina līgumu rindas — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_


Produktu līgumu rindas programmā Dynamics 365 Project Operations ietver **Izmaksu** lauku, kurā tiek glabātas produkta izmaksas lejupstraumes ienesīguma aprēķiniem.

Kad kataloga produktam tiek izveidota produkta līguma rinda, rindas izmaksu noklusējuma vērtība tiek iegūta no produktu kataloga lauka **Standarta izmaksas**. Preču kataloga lauks **Standarta izmaksas** tiek iestatīts Organizācijas pamatvalūtā. Ja tiek atjaunotas vienības izmaksas līguma rindā, tās tiek konvertētas līguma pārdošanas valūtā.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Vienības izmaksas produkta līguma rindā

Vienības izmaksas produkta līguma rindā pieļauj atsevišķas produktu izmaksas katras vienības pārdošanas gadījumam. Lai gan ne vienmēr nepieciešams, ir dažas situācijas, kurās piegādātājs var piešķirt klientam atlaidi par produkta izmaksām. Tālāk ir aprakstīts ieteicamais scenārijs.

Uzņēmums Fabrikam Robotics uzstāda robotu rokas korporācijas Adatum konveijeros. Fabrikam nodrošina instalēšanas pakalpojumus, bet robotu rokas ir no Trey Research. Ja robotu roku uzstādīšana korporācijā Adatum paver jaunu nozares vertikāli uzņēmumam Trey Research, uzņēmums varētu šim darījumam piedāvāt īpašu atlaidi uzņēmumam Fabrikam. Šajā gadījumā Fabrikam izveidot produkta līguma rindu robotu rokām. Šim līgumam tiek ievadīta vienības cena. Šī cena atšķiras no Trey Research robotu roku cenas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]