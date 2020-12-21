---
title: Vienumu saņemšana pirkšanas pasūtījumā no vienuma prasībām
description: Šajā tēmā izskaidrots, kā no vienuma prasībām saņemt pirkšanas pasūtījuma elementus.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080611"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="dfc30-103">Vienumu saņemšana pirkšanas pasūtījumā no vienuma prasībām</span><span class="sxs-lookup"><span data-stu-id="dfc30-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dfc30-104">Šajā tēmā izskaidrots, kā no vienuma prasībām saņemt pirkšanas pasūtījuma elementus.</span><span class="sxs-lookup"><span data-stu-id="dfc30-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="dfc30-105">Izmantojot vienuma prasības, nevis vienumu transakciju, var plānot piegādi tieši pirms elementa faktiskās izmantošanas, izveidot pirkšanas pasūtījumu, iekļaut to pārdošanas līgumu shēmā, un iekļaut vienuma prasības ražošanas plānošanā.</span><span class="sxs-lookup"><span data-stu-id="dfc30-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="dfc30-106">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="dfc30-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="dfc30-107">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Projekti > Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="dfc30-108">Sarakstā atlasiet saiti vēlamajā rindā.</span><span class="sxs-lookup"><span data-stu-id="dfc30-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="dfc30-109">Darbību rūtī atlasiet **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="dfc30-110">Atlasiet **Vienumu prasības**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="dfc30-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-111">Select **New**.</span></span>
6. <span data-ttu-id="dfc30-112">Jaunajā rindā ievadiet vai atlasiet vērtību laukā **Vienuma numurs**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="dfc30-113">Laukā **Daudzums** ievadiet numuru.</span><span class="sxs-lookup"><span data-stu-id="dfc30-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="dfc30-114">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-114">Select **Save**.</span></span>
9. <span data-ttu-id="dfc30-115">Darbību rūtī atlasiet **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="dfc30-116">Atlasiet vienumu **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-116">Select **Functions**.</span></span>
11. <span data-ttu-id="dfc30-117">Atlasiet **Pirkšanas pasūtījuma izveide**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="dfc30-118">Atzīmējiet izvēles rūtiņu **Ietvert visus**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="dfc30-119">Laukā **Piegādātāja uzņēmums** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="dfc30-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="dfc30-120">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-120">Select **OK**.</span></span>
15. <span data-ttu-id="dfc30-121">Navigācijas rūtī ejiet uz **Moduļi > Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="dfc30-122">Sarakstā atlasiet saiti vēlamajā rindā.</span><span class="sxs-lookup"><span data-stu-id="dfc30-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="dfc30-123">Darbību rūtī atlasiet **Pirkt**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="dfc30-124">Atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="dfc30-125">Darbību rūtī atlasiet **Saņemt**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="dfc30-126">Atlasiet **Produkta kvīts**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="dfc30-127">Laukā **Produkta kvīts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="dfc30-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="dfc30-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="dfc30-128">Select **OK**.</span></span>
