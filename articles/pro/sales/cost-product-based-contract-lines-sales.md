---
title: Produktu izmaksu aprēķina līgumu rindas — Lite
description: Šajā tēmā ir sniegta informācija par izveidi
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177250"
---
# <a name="cost-product-based-contract-lines---lite"></a>Produktu izmaksu aprēķina līgumu rindas — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_


Produkta līguma rindas risinājumā Dynamics 365 Project Operations iekļauj lauku **Izmaksas**, kas saglabā produkta izmaksas lejupstraumes ienesīguma aprēķiniem.

Ja kataloga precei ir izveidota produkta līguma rinda, produkta līguma rindas izmaksas pēc noklusējuma tiek ņemtas no preču kataloga lauka **Standarta izmaksas**. Preču kataloga lauks **Standarta izmaksas** tiek iestatīts Organizācijas pamatvalūtā. Ja tiek atjaunotas vienības izmaksas līguma rindā, tās tiek konvertētas līguma pārdošanas valūtā.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Vienības izmaksas produkta līguma rindā

Vienības izmaksas produkta līguma rindā pieļauj atsevišķas produktu izmaksas katras vienības pārdošanas gadījumam. Lai gan ne vienmēr nepieciešams, ir dažas situācijas, kurās piegādātājs var piešķirt klientam atlaidi par produkta izmaksām. Tālāk ir aprakstīts ieteicamais scenārijs.

Uzņēmums Fabrikam Robotics uzstāda robotu rokas korporācijas Adatum konveijeros. Uzņēmums Fabrikam nodrošina uzstādīšanas pakalpojumus, taču robotu rokas tiek iegādātas no uzņēmuma Trey Research. Ja robotu roku uzstādīšana korporācijā Adatum paver jaunu nozares vertikāli uzņēmumam Trey Research, uzņēmums varētu šim darījumam piedāvāt īpašu atlaidi uzņēmumam Fabrikam. Šajā gadījumā Fabrikam izveido produkta līguma rindu robotu rokām un ievada vienības pašizmaksu šim līgumam, kas atšķiras no Trey Research robota roku standarta izmaksām.
