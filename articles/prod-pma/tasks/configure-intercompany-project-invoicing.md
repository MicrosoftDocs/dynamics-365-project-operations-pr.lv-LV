---
title: Starpuzņēmumu projektu rēķinu izrakstīšanas konfigurēšana
description: Šajā tēmā parādīts, kā iestatīt projektu rēķinu izrakstīšanu starp diviem uzņēmumiem jūsu organizācijā.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080503"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="ddd25-103">Starpuzņēmumu projektu rēķinu izrakstīšanas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="ddd25-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ddd25-104">Šajā tēmā parādīts, kā iestatīt projektu rēķinu izrakstīšanu starp diviem uzņēmumiem jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="ddd25-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="ddd25-105">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="ddd25-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="ddd25-106">Navigācijas rūtī ejiet uz **Moduļi > Kreditori > Piegādātāji > Visi piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="ddd25-107">Sarakstā **Visi piegādātāji** atrodiet un atlasiet nepieciešamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ddd25-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="ddd25-108">Darbību rūtī atlasiet **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="ddd25-109">Atlasiet **Starpuzņēmumu**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="ddd25-110">Iestatiet **Aktīvs** uz **Jā** , lai iespējotu starpuzņēmumu tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="ddd25-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="ddd25-111">Laukā **Klienta uzņēmums** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ddd25-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="ddd25-112">Laukā **Mans uzņēmums** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ddd25-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="ddd25-113">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-113">Select **Save**.</span></span>
9. <span data-ttu-id="ddd25-114">Aizveriet lapas, lai atgrieztos sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="ddd25-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="ddd25-115">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Iestatīšana > Projekta pārvaldības un grāmatvedības parametri**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="ddd25-116">Atlasiet cilni **Starpuzņēmumu**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="ddd25-117">Pārvietojiet slīdni uz **Jā** , lai iespējotu starpuzņēmumu resursu plānošanu un laika uzskaites tabulas.</span><span class="sxs-lookup"><span data-stu-id="ddd25-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="ddd25-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ddd25-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="ddd25-119">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-119">Select **New**.</span></span>
15. <span data-ttu-id="ddd25-120">Laukā **Aizņemošā juridiskā persona** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ddd25-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="ddd25-121">Atzīmējiet izvēles rūtiņu **Uzkrāt peļņu**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="ddd25-122">Laukā **Noklusējuma laika uzskaites tabulu kategorija** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ddd25-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="ddd25-123">Laukā **Noklusējuma izdevumu kategorija** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ddd25-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="ddd25-124">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-124">Select **Save**.</span></span>
20. <span data-ttu-id="ddd25-125">Aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="ddd25-125">Close the page.</span></span>
21. <span data-ttu-id="ddd25-126">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Iestatīšana > Publicēšana > Virsgrāmatas publicēšanas iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="ddd25-127">Laukā **Virsgrāmatas uzņēmumu tipi** atlasiet kādu no opcijām.</span><span class="sxs-lookup"><span data-stu-id="ddd25-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="ddd25-128">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-128">Select **New**.</span></span>
24. <span data-ttu-id="ddd25-129">Jaunās rindas laukā **Galvenais konts** norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="ddd25-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="ddd25-130">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-130">Select **Save**.</span></span>
26. <span data-ttu-id="ddd25-131">Aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="ddd25-131">Close the page.</span></span>
27. <span data-ttu-id="ddd25-132">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Iestatīšana > Cenas > Pārsūtīšanas cena**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="ddd25-133">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-133">Select **New**.</span></span>
29. <span data-ttu-id="ddd25-134">Laukā **Sākot ar** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="ddd25-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="ddd25-135">Laukā **Aizņemošā juridiskā persona** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ddd25-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="ddd25-136">Laukā **Pārsūtīšanas cenas modelis** atlasiet kādu no opcijām.</span><span class="sxs-lookup"><span data-stu-id="ddd25-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="ddd25-137">Laukā **Cenas noteikšana** ievadiet numuru.</span><span class="sxs-lookup"><span data-stu-id="ddd25-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="ddd25-138">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ddd25-138">Select **Save**.</span></span>
