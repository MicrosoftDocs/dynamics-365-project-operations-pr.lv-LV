---
title: Darba un izdevumu standarta izmaksu konfigurēšana
description: Šajā tēmā ir paskaidrots, kā iestatīt darba un izdevumu standarta izmaksas projektam.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080501"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="55e4e-103">Darba un izdevumu standarta izmaksu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="55e4e-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55e4e-104">Šajā tēmā ir paskaidrots, kā iestatīt darba un izdevumu standarta izmaksas projektam.</span><span class="sxs-lookup"><span data-stu-id="55e4e-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="55e4e-105">Šajā uzdevumā tiek izmantota USSI datu kopa.</span><span class="sxs-lookup"><span data-stu-id="55e4e-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="55e4e-106">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Iestatīšana > Cenas > Izmaksas (stunda)**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="55e4e-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-107">Select **New**.</span></span>
3. <span data-ttu-id="55e4e-108">Laukā **Sākot ar** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="55e4e-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="55e4e-109">Laukā **Izmaksas** ievadiet ciparu.</span><span class="sxs-lookup"><span data-stu-id="55e4e-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="55e4e-110">Varat iestatīt standarta izmaksas projekta kategorijai vai arī iestatīt izmaksas pēc darbinieka numura, projekta numura, kategorijas, datuma vai jebkuras to kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="55e4e-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="55e4e-111">Lietotās izmaksas ir izmaksas ar visaugstāko detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="55e4e-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="55e4e-112">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-112">Select **Save**.</span></span>
6. <span data-ttu-id="55e4e-113">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Iestatīšana > Cenas > Pārdošanas cena (stunda)**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="55e4e-114">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-114">Select **New**.</span></span>
8. <span data-ttu-id="55e4e-115">Laukā **Sākot ar** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="55e4e-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="55e4e-116">Laukā **Derīgums** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="55e4e-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="55e4e-117">Laukā **Cenas noteikšana** ievadiet numuru.</span><span class="sxs-lookup"><span data-stu-id="55e4e-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="55e4e-118">Varat iestatīt standarta pārdošanas cenu stundas transakcijām vai projekta kategorijai.</span><span class="sxs-lookup"><span data-stu-id="55e4e-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="55e4e-119">Varat arī iestatīt pārdošanas cenas pēc darbinieka numura, projekta numura, kategorijas, transakcijas datuma vai jebkuras šo elementu kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="55e4e-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="55e4e-120">Faktiskā pārdošanas cena, kas tiek lietota, kad darbinieks ievada transakciju stundu žurnālā, ir pārdošanas cena ar visaugstāko detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="55e4e-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="55e4e-121">Piemēram, ja ir iestatīta gan vispārējā pārdošanas cena, gan darbinieka norādītā pārdošanas cena, tiek izmantota darbinieka norādītā pārdošanas cena.</span><span class="sxs-lookup"><span data-stu-id="55e4e-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="55e4e-122">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-122">Select **Save**.</span></span>
12. <span data-ttu-id="55e4e-123">Aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="55e4e-123">Close the page.</span></span>
13. <span data-ttu-id="55e4e-124">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Iestatīšana > Cenas > Izmaksas (izdevumi)**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="55e4e-125">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-125">Select **New**.</span></span>
15. <span data-ttu-id="55e4e-126">Laukā **Sākot ar** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="55e4e-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="55e4e-127">Laukā **Izmaksas** ievadiet ciparu.</span><span class="sxs-lookup"><span data-stu-id="55e4e-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="55e4e-128">Var aizpildīt vairākus laukus, bet šis ir minimums, kas nepieciešams ieraksta saglabāšanai.</span><span class="sxs-lookup"><span data-stu-id="55e4e-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="55e4e-129">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-129">Select **Save**.</span></span>
18. <span data-ttu-id="55e4e-130">Navigācijas rūtī ejiet uz **Moduļi > Projekta pārvaldība un grāmatvedība > Iestatīšana > Cenas > Pārdošanas cena (izdevumi)**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="55e4e-131">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-131">Select **New**.</span></span>
20. <span data-ttu-id="55e4e-132">Laukā **Sākot ar** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="55e4e-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="55e4e-133">Laukā **Derīgums** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="55e4e-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="55e4e-134">Laukā **Cenas noteikšana** ievadiet numuru.</span><span class="sxs-lookup"><span data-stu-id="55e4e-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="55e4e-135">Faktiskā pārdošanas cena, kas tiek lietota, kad darbinieks ievada transakcijas izdevumu žurnālā, ir pārdošanas cena ar visaugstāko detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="55e4e-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="55e4e-136">Piemēram, ja ir iestatīta gan vispārējā, gan darbinieka norādītā pārdošanas cena, tiek izmantota darbinieka norādītā pārdošanas cena.</span><span class="sxs-lookup"><span data-stu-id="55e4e-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="55e4e-137">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="55e4e-137">Select **Save**.</span></span>

