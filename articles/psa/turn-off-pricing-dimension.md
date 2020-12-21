---
title: Cenas noteikšanas dimensijas izslēgšana
description: Šajā tēmā ir parādīts, kā Project Service risinājumā iestatīt cenu noteikšanas dimensijas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080529"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="a9b40-103">Cenas noteikšanas dimensijas izslēgšana</span><span class="sxs-lookup"><span data-stu-id="a9b40-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="a9b40-104">Iespējams, ik pēc dažiem gadiem jums ir jāpārskata un jāatjaunina sava cenu noteikšanas stratēģija.</span><span class="sxs-lookup"><span data-stu-id="a9b40-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="a9b40-105">Jūsu veiktajiem atjauninājumiem var būt nepieciešams izslēgt esošu cenas noteikšanas dimensiju un izveidot jaunu.</span><span class="sxs-lookup"><span data-stu-id="a9b40-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="a9b40-106">Piemēram, iepriekš jūs noteicāt cenas, izmantojot **Lomu** , bet tagad esat izlēmis noteikt cenas, izmantojot **Darba pieredzi**.</span><span class="sxs-lookup"><span data-stu-id="a9b40-106">For example, you may have previously priced by **Role** , but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="a9b40-107">Tam var būt nepieciešams izslēgt **Lomu** kā cenas noteikšanas dimensiju un izveidot **Darba pieredzi** kā jaunu cenas noteikšanas dimensiju.</span><span class="sxs-lookup"><span data-stu-id="a9b40-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="a9b40-108">Cenas noteikšanas dimensijas izslēgšanu, neatkarīgi no tā, vai tā ir iekļauta vai pielāgota, var izdarīt, iestatot Cenas noteikšanas dimensijas laukus **Piemērojams izmaksām** un **Piemērojams pārdošanai** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="a9b40-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="a9b40-109">Tomēr, to darot, var parādīties šāds kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="a9b40-109">However, when you do this, you might receive the following error message.</span></span>

![Biznesa procesa kļūda ir iespējama, izslēdzot cenas noteikšanas dimensiju](media/Business-Process-Error.png)


<span data-ttu-id="a9b40-111">Šis kļūdas ziņojums norāda, ka pastāv cenu ieraksti, kas iepriekš tika iestatīti izslēgtai dimensijai.</span><span class="sxs-lookup"><span data-stu-id="a9b40-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="a9b40-112">Visi **Lomas cenas** un **Lomas cenas uzcenojuma** ieraksti, kas norāda uz dimensiju, ir jādzēš, pirms dimensiju piemērojamību var iestatīt uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="a9b40-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="a9b40-113">Šīs noteikums attiecas gan uz iekļautām cenu noteikšanas dimensijām, gan uz jebkurām pielāgotām cenu noteikšanas dimensijām, kuras, iespējams, esat izveidojis.</span><span class="sxs-lookup"><span data-stu-id="a9b40-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="a9b40-114">Šīs pārbaudes iemesls – programmai Project Service ir ierobežojums, ka katram **Lomas cenas** ierakstam ir jābūt unikālai dimensiju kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="a9b40-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="a9b40-115">Piemēram, cenrādī ar nosaukumu **ASV izmaksu likmes 2018. gadā** ir šādas **Lomu cenu** rindas.</span><span class="sxs-lookup"><span data-stu-id="a9b40-115">For example, on a price list called **US Cost Rates 2018** , you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="a9b40-116">Standarta nosaukums</span><span class="sxs-lookup"><span data-stu-id="a9b40-116">Standard Title</span></span>         | <span data-ttu-id="a9b40-117">Org. struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="a9b40-117">Org Unit</span></span>    |<span data-ttu-id="a9b40-118">Vienība</span><span class="sxs-lookup"><span data-stu-id="a9b40-118">Unit</span></span>   |<span data-ttu-id="a9b40-119">Cena</span><span class="sxs-lookup"><span data-stu-id="a9b40-119">Price</span></span>  |<span data-ttu-id="a9b40-120">Valūta</span><span class="sxs-lookup"><span data-stu-id="a9b40-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="a9b40-121">Sistēmas inženieris</span><span class="sxs-lookup"><span data-stu-id="a9b40-121">Systems Engineer</span></span>|<span data-ttu-id="a9b40-122">Contoso ASV</span><span class="sxs-lookup"><span data-stu-id="a9b40-122">Contoso US</span></span>|<span data-ttu-id="a9b40-123">Hour</span><span class="sxs-lookup"><span data-stu-id="a9b40-123">Hour</span></span>| <span data-ttu-id="a9b40-124">100</span><span class="sxs-lookup"><span data-stu-id="a9b40-124">100</span></span>|<span data-ttu-id="a9b40-125">USD</span><span class="sxs-lookup"><span data-stu-id="a9b40-125">USD</span></span>|
| <span data-ttu-id="a9b40-126">Vecākais sistēmu inženieris</span><span class="sxs-lookup"><span data-stu-id="a9b40-126">Senior Systems Engineer</span></span>|<span data-ttu-id="a9b40-127">Contoso ASV</span><span class="sxs-lookup"><span data-stu-id="a9b40-127">Contoso US</span></span>|<span data-ttu-id="a9b40-128">Hour</span><span class="sxs-lookup"><span data-stu-id="a9b40-128">Hour</span></span>| <span data-ttu-id="a9b40-129">150</span><span class="sxs-lookup"><span data-stu-id="a9b40-129">150</span></span>| <span data-ttu-id="a9b40-130">USD</span><span class="sxs-lookup"><span data-stu-id="a9b40-130">USD</span></span>|


<span data-ttu-id="a9b40-131">Izslēdzot **Standarta nosaukumu** kā cenas noteikšanas dimensiju un kad Project Service cenas noteikšanas programma meklē noteiktu cenu, tā izmantos tikai **Org. struktūrvienības** vērtību no ievades konteksta.</span><span class="sxs-lookup"><span data-stu-id="a9b40-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="a9b40-132">Ja ievades konteksta **Organizācijas struktūrvienība** ir Contoso ASV, rezultāts nebūs noteikts, jo abas rindas sakritīs.</span><span class="sxs-lookup"><span data-stu-id="a9b40-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="a9b40-133">Lai izvairītos no šāda scenārija, veidojot **Lomu cenu** ierakstus, programma Project Service pārbauda, lai dimensiju kombinācija ir unikāla.</span><span class="sxs-lookup"><span data-stu-id="a9b40-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="a9b40-134">Ja dimensija ir izslēgta pēc **Lomu cenu** izveides, šo ierobežojumu var pārkāpt.</span><span class="sxs-lookup"><span data-stu-id="a9b40-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="a9b40-135">Tāpēc pirms dimensijas izslēgšanas ir jādzēš visas **Lomu cenu** un **Lomu cenu uzcenojumu** rindas, kurām ir šī dimensijas vērtība.</span><span class="sxs-lookup"><span data-stu-id="a9b40-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
