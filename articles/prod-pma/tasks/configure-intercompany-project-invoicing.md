---
title: Starpuzņēmumu projektu rēķinu izrakstīšanas konfigurēšana
description: Šajā tēmā parādīts, kā iestatīt projektu rēķinu izrakstīšanu starp diviem uzņēmumiem jūsu organizācijā.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
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
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001210"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="597ba-103">Starpuzņēmumu projektu rēķinu izrakstīšanas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="597ba-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="597ba-104">Šajā tēmā parādīts, kā iestatīt projektu rēķinu izrakstīšanu starp diviem uzņēmumiem jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="597ba-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="597ba-105">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="597ba-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="597ba-106">Navigācijas rūtī ejiet uz **Moduļi > Kreditori > Piegādātāji > Visi piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="597ba-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="597ba-107">Sarakstā **Visi piegādātāji** atrodiet un atlasiet nepieciešamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="597ba-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="597ba-108">Darbību rūtī atlasiet **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="597ba-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="597ba-109">Atlasiet **Starpuzņēmumu**.</span><span class="sxs-lookup"><span data-stu-id="597ba-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="597ba-110">Iestatiet **Aktīvs** uz **Jā**, lai iespējotu starpuzņēmumu tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="597ba-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="597ba-111">Laukā **Klienta uzņēmums** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="597ba-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="597ba-112">Laukā **Mans uzņēmums** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="597ba-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="597ba-113">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="597ba-113">Select **Save**.</span></span>
9. <span data-ttu-id="597ba-114">Aizveriet lapas, lai atgrieztos sākumlapā.</span><span class="sxs-lookup"><span data-stu-id="597ba-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="597ba-115">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Iestatīšana > Projekta pārvaldības un grāmatvedības parametri**.</span><span class="sxs-lookup"><span data-stu-id="597ba-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="597ba-116">Atlasiet cilni **Starpuzņēmumu**.</span><span class="sxs-lookup"><span data-stu-id="597ba-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="597ba-117">Pārvietojiet slīdni uz **Jā**, lai iespējotu starpuzņēmumu resursu plānošanu un laika uzskaites tabulas.</span><span class="sxs-lookup"><span data-stu-id="597ba-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="597ba-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="597ba-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="597ba-119">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="597ba-119">Select **New**.</span></span>
15. <span data-ttu-id="597ba-120">Laukā **Aizņemošā juridiskā persona** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="597ba-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="597ba-121">Atzīmējiet izvēles rūtiņu **Uzkrāt peļņu**.</span><span class="sxs-lookup"><span data-stu-id="597ba-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="597ba-122">Laukā **Noklusējuma laika uzskaites tabulu kategorija** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="597ba-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="597ba-123">Laukā **Noklusējuma izdevumu kategorija** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="597ba-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="597ba-124">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="597ba-124">Select **Save**.</span></span>
20. <span data-ttu-id="597ba-125">Aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="597ba-125">Close the page.</span></span>
21. <span data-ttu-id="597ba-126">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Iestatīšana > Publicēšana > Virsgrāmatas publicēšanas iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="597ba-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="597ba-127">Laukā **Virsgrāmatas uzņēmumu tipi** atlasiet kādu no opcijām.</span><span class="sxs-lookup"><span data-stu-id="597ba-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="597ba-128">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="597ba-128">Select **New**.</span></span>
24. <span data-ttu-id="597ba-129">Jaunās rindas laukā **Galvenais konts** norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="597ba-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="597ba-130">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="597ba-130">Select **Save**.</span></span>
26. <span data-ttu-id="597ba-131">Aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="597ba-131">Close the page.</span></span>
27. <span data-ttu-id="597ba-132">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Iestatīšana > Cenas > Pārsūtīšanas cena**.</span><span class="sxs-lookup"><span data-stu-id="597ba-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="597ba-133">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="597ba-133">Select **New**.</span></span>
29. <span data-ttu-id="597ba-134">Laukā **Sākot ar** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="597ba-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="597ba-135">Laukā **Aizņemošā juridiskā persona** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="597ba-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="597ba-136">Laukā **Pārsūtīšanas cenas modelis** atlasiet kādu no opcijām.</span><span class="sxs-lookup"><span data-stu-id="597ba-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="597ba-137">Laukā **Cenas noteikšana** ievadiet numuru.</span><span class="sxs-lookup"><span data-stu-id="597ba-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="597ba-138">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="597ba-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]