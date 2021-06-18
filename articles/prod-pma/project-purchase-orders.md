---
title: Projekta pirkšanas pasūtījumi
description: Šajā rakstā ir aprakstītas dažādas metodes, ko varat izmantot, lai izveidotu projekta pirkšanas pasūtījumus. Jūsu izmantotā metode ir atkarīga no pirkšanas pasūtījuma nolūka, iegādāto preču patēriņa laika un pievienošanas projekta izmaksām.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999365"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="4295a-104">Projekta pirkšanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="4295a-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4295a-105">Šajā rakstā ir aprakstītas dažādas metodes, ko varat izmantot, lai izveidotu projekta pirkšanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="4295a-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="4295a-106">Jūsu izmantotā metode ir atkarīga no pirkšanas pasūtījuma nolūka, iegādāto preču patēriņa laika un pievienošanas projekta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="4295a-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="4295a-107">Pirkuma pasūtījuma izveides metodes</span><span class="sxs-lookup"><span data-stu-id="4295a-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="4295a-108">Lai Projekta pārvaldībā un uzskaitē izveidotu pirkuma pasūtījumu, varat izmantot vienu no šīm metodēm.</span><span class="sxs-lookup"><span data-stu-id="4295a-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="4295a-109">Pirkuma pasūtījuma mērķis nosaka, kad pirkuma pasūtījums tiek patērēts un līdz ar to kad preces tiek pievienotas projekta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="4295a-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4295a-110">Metode</span><span class="sxs-lookup"><span data-stu-id="4295a-110">Method</span></span></th>
<th><span data-ttu-id="4295a-111">Nolūks</span><span class="sxs-lookup"><span data-stu-id="4295a-111">Purpose</span></span></th>
<th><span data-ttu-id="4295a-112">Preču patēriņš</span><span class="sxs-lookup"><span data-stu-id="4295a-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4295a-113">Izveidojiet pirkuma pasūtījumu tieši no projekta.</span><span class="sxs-lookup"><span data-stu-id="4295a-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="4295a-114">Izmantojiet šo metodi, lai iegādātos preces no ārēja tirgotāja patērēšanai projektā.</span><span class="sxs-lookup"><span data-stu-id="4295a-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="4295a-115">Pirkšanas pasūtījumu var izveidot divos veidos:</span><span class="sxs-lookup"><span data-stu-id="4295a-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="4295a-116">No paša projekta.</span><span class="sxs-lookup"><span data-stu-id="4295a-116">From the project itself.</span></span> <span data-ttu-id="4295a-117">Šajā gadījumā projekts ir jau definēts pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="4295a-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="4295a-118">Naviģējot uz projekta pirkuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="4295a-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="4295a-119">Ir jāatlasa gan pārdevējs, gan projekts, kuram jāizveido pirkuma pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="4295a-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="4295a-120">Preces tiek patērētas, kad ir atjaunots pārdevēja rēķins.</span><span class="sxs-lookup"><span data-stu-id="4295a-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4295a-121">Izveidojiet pirkuma pasūtījumu no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="4295a-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="4295a-122">Izmantojiet šo metodi, lai iegādātos vienumus, kad no projekta izveidojat pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="4295a-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="4295a-123">Preces tiek patērētas, kad klientam tiek izrakstīts pārdošanas pasūtījuma rēķins.</span><span class="sxs-lookup"><span data-stu-id="4295a-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4295a-124">Izveidojiet pirkšanas pasūtījumu no preces prasības.</span><span class="sxs-lookup"><span data-stu-id="4295a-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="4295a-125">Izmantojiet šo metodi, lai iegādātos vienumus, kad no projekta izveidojat preces prasību.</span><span class="sxs-lookup"><span data-stu-id="4295a-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="4295a-126">Preces tiek patērētas, kad ir atjaunināta preces prasības pavadzīme.</span><span class="sxs-lookup"><span data-stu-id="4295a-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="4295a-127">Atjauninot kreditora rēķinu vai pavadzīmi, tiek parādīta uzvedne ar aicinājumu atjaunināt preces prasības pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="4295a-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="4295a-128">Papildinformāciju skatiet tēmā [Preču saņemšana pirkuma pasūtījumā no preču prasības](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="4295a-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]