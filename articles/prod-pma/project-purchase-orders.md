---
title: Projekta pirkšanas pasūtījumi
description: Šajā rakstā ir aprakstītas dažādas metodes, ko varat izmantot, lai izveidotu projekta pirkšanas pasūtījumus. Jūsu izmantotā metode ir atkarīga no pirkšanas pasūtījuma nolūka, iegādāto preču patēriņa laika un pievienošanas projekta izmaksām.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080432"
---
# <a name="purchase-orders-for-a-project"></a>Projekta pirkšanas pasūtījumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas dažādas metodes, ko varat izmantot, lai izveidotu projekta pirkšanas pasūtījumus. Jūsu izmantotā metode ir atkarīga no pirkšanas pasūtījuma nolūka, iegādāto preču patēriņa laika un pievienošanas projekta izmaksām.

### <a name="methods-for-creating-a-purchase-order"></a>Pirkuma pasūtījuma izveides metodes

Lai Projekta pārvaldībā un uzskaitē izveidotu pirkuma pasūtījumu, varat izmantot vienu no šīm metodēm. Pirkuma pasūtījuma mērķis nosaka, kad pirkuma pasūtījums tiek patērēts un līdz ar to kad preces tiek pievienotas projekta izmaksām.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Nolūks</th>
<th>Preču patēriņš</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Izveidojiet pirkuma pasūtījumu tieši no projekta.</td>
<td>Izmantojiet šo metodi, lai iegādātos preces no ārēja tirgotāja patērēšanai projektā. Pirkšanas pasūtījumu var izveidot divos veidos:
<ul>
<li>No paša projekta. Šajā gadījumā projekts ir jau definēts pirkšanas pasūtījumam.</li>
<li>Naviģējot uz projekta pirkuma pasūtījumu. Ir jāatlasa gan pārdevējs, gan projekts, kuram jāizveido pirkuma pasūtījums.</li>
</ul></td>
<td>Preces tiek patērētas, kad ir atjaunots pārdevēja rēķins.</td>
</tr>
<tr class="even">
<td>Izveidojiet pirkuma pasūtījumu no pārdošanas pasūtījuma.</td>
<td>Izmantojiet šo metodi, lai iegādātos vienumus, kad no projekta izveidojat pārdošanas pasūtījumu.</td>
<td>Preces tiek patērētas, kad klientam tiek izrakstīts pārdošanas pasūtījuma rēķins.</td>
</tr>
<tr class="odd">
<td>Izveidojiet pirkšanas pasūtījumu no preces prasības.</td>
<td>Izmantojiet šo metodi, lai iegādātos vienumus, kad no projekta izveidojat preces prasību.</td>
<td>Preces tiek patērētas, kad ir atjaunināta preces prasības pavadzīme.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Atjauninot kreditora rēķinu vai pavadzīmi, tiek parādīta uzvedne ar aicinājumu atjaunināt preces prasības pavadzīmi.

Papildinformāciju skatiet tēmā [Preču saņemšana pirkuma pasūtījumā no preču prasības](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]