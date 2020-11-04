---
title: Produktu izmaksu aprēķina līgumu rindas
description: Šajā tēmā ir sniegta informācija par izveidi
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2020
ms.locfileid: "4080675"
---
# <a name="costing-product-based-contract-lines"></a>Produktu izmaksu aprēķina līgumu rindas

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_


Produkta līguma rindas risinājumā Dynamics 365 Project Operations iekļauj lauku **Izmaksas** , kas saglabā produkta izmaksas lejupstraumes ienesīguma aprēķiniem.

Ja kataloga precei ir izveidota produkta līguma rinda, produkta līguma rindas izmaksas pēc noklusējuma tiek ņemtas no preču kataloga lauka **Standarta izmaksas**. Preču kataloga lauks **Standarta izmaksas** tiek iestatīts Organizācijas pamatvalūtā. Ja tiek atjaunotas vienības izmaksas līguma rindā, tās tiek konvertētas līguma pārdošanas valūtā.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Vienības izmaksas produkta līguma rindā

Vienības izmaksas produkta līguma rindā pieļauj atsevišķas produktu izmaksas katras vienības pārdošanas gadījumam. Lai gan ne vienmēr nepieciešams, ir dažas situācijas, kurās piegādātājs var piešķirt klientam atlaidi par produkta izmaksām. Tālāk ir aprakstīts ieteicamais scenārijs.

Uzņēmums Fabrikam Robotics uzstāda robotu rokas korporācijas Adatum konveijeros. Uzņēmums Fabrikam nodrošina uzstādīšanas pakalpojumus, taču robotu rokas tiek iegādātas no uzņēmuma Trey Research. Ja robotu roku uzstādīšana korporācijā Adatum paver jaunu nozares vertikāli uzņēmumam Trey Research, uzņēmums varētu šim darījumam piedāvāt īpašu atlaidi uzņēmumam Fabrikam. Šajā gadījumā Fabrikam izveido produkta līguma rindu robotu rokām un ievada vienības pašizmaksu šim līgumam, kas atšķiras no Trey Research robota roku standarta izmaksām.
