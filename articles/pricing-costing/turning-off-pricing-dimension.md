---
title: Cenu noteikšanas dimensiju izslēgšana
description: Šajā tēmā ir sniegta informācija par cenu noteikšanas dimensiju izslēgšanu.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650058"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="98361-103">Cenu noteikšanas dimensiju izslēgšana</span><span class="sxs-lookup"><span data-stu-id="98361-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="98361-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="98361-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="98361-105">Iespējams, ik pēc dažiem gadiem jums ir jāpārskata un jāatjaunina sava cenu noteikšanas stratēģija.</span><span class="sxs-lookup"><span data-stu-id="98361-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="98361-106">Jūsu veiktajiem atjauninājumiem var būt nepieciešams izslēgt esošu cenas noteikšanas dimensiju un izveidot jaunu.</span><span class="sxs-lookup"><span data-stu-id="98361-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="98361-107">Piemēram, iepriekš jūs noteicāt cenas, izmantojot **Lomu**, bet tagad esat izlēmis noteikt cenas, izmantojot **Darba pieredzi**.</span><span class="sxs-lookup"><span data-stu-id="98361-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="98361-108">Tam var būt nepieciešams izslēgt **Lomu** kā cenas noteikšanas dimensiju un izveidot **Darba pieredzi** kā jaunu cenas noteikšanas dimensiju.</span><span class="sxs-lookup"><span data-stu-id="98361-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="98361-109">Cenas noteikšanas dimensijas izslēgšanu, neatkarīgi no tā, vai tā ir iekļauta vai pielāgota, var izdarīt, iestatot Cenas noteikšanas dimensijas laukus **Piemērojams izmaksām** un **Piemērojams pārdošanai** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="98361-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="98361-110">Tomēr, ja tas ir izdarīts, iespējams, saņemsit kļūdas ziņojumu, ka **Cenu noteikšanas dimensiju nevar atjaunināt vai dzēst, ja ir saistīti cenu ieraksti.**</span><span class="sxs-lookup"><span data-stu-id="98361-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Biznesa procesa kļūda ir iespējama, izslēdzot cenas noteikšanas dimensiju](media/Business-Process-Error.png)

<span data-ttu-id="98361-112">Šis kļūdas ziņojums norāda, ka pastāv cenu ieraksti, kas iepriekš tika iestatīti izslēgtai dimensijai.</span><span class="sxs-lookup"><span data-stu-id="98361-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="98361-113">Visi **Lomas cenas** un **Lomas cenas uzcenojuma** ieraksti, kas norāda uz dimensiju, ir jādzēš, pirms dimensiju piemērojamību var iestatīt uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="98361-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="98361-114">Šīs noteikums attiecas gan uz iekļautām cenu noteikšanas dimensijām, gan uz jebkurām pielāgotām cenu noteikšanas dimensijām, kuras, iespējams, esat izveidojis.</span><span class="sxs-lookup"><span data-stu-id="98361-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="98361-115">Šīs pārbaudes iemesls – katram **Lomas cenas** ierakstam ir jābūt unikālai dimensiju kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="98361-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="98361-116">Piemēram, cenrādī ar nosaukumu **ASV izmaksu likmes 2018. gadā** ir šādas **Lomu cenu** rindas.</span><span class="sxs-lookup"><span data-stu-id="98361-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="98361-117">Standarta nosaukums</span><span class="sxs-lookup"><span data-stu-id="98361-117">Standard Title</span></span>         | <span data-ttu-id="98361-118">Org. struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="98361-118">Org Unit</span></span>    |<span data-ttu-id="98361-119">Vienība</span><span class="sxs-lookup"><span data-stu-id="98361-119">Unit</span></span>   |<span data-ttu-id="98361-120">Cena</span><span class="sxs-lookup"><span data-stu-id="98361-120">Price</span></span>  |<span data-ttu-id="98361-121">Valūta</span><span class="sxs-lookup"><span data-stu-id="98361-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="98361-122">Sistēmas inženieris</span><span class="sxs-lookup"><span data-stu-id="98361-122">Systems Engineer</span></span>|<span data-ttu-id="98361-123">Contoso ASV</span><span class="sxs-lookup"><span data-stu-id="98361-123">Contoso US</span></span>|<span data-ttu-id="98361-124">Hour</span><span class="sxs-lookup"><span data-stu-id="98361-124">Hour</span></span>| <span data-ttu-id="98361-125">100</span><span class="sxs-lookup"><span data-stu-id="98361-125">100</span></span>|<span data-ttu-id="98361-126">USD</span><span class="sxs-lookup"><span data-stu-id="98361-126">USD</span></span>|
| <span data-ttu-id="98361-127">Vecākais sistēmu inženieris</span><span class="sxs-lookup"><span data-stu-id="98361-127">Senior Systems Engineer</span></span>|<span data-ttu-id="98361-128">Contoso ASV</span><span class="sxs-lookup"><span data-stu-id="98361-128">Contoso US</span></span>|<span data-ttu-id="98361-129">Hour</span><span class="sxs-lookup"><span data-stu-id="98361-129">Hour</span></span>| <span data-ttu-id="98361-130">150</span><span class="sxs-lookup"><span data-stu-id="98361-130">150</span></span>| <span data-ttu-id="98361-131">USD</span><span class="sxs-lookup"><span data-stu-id="98361-131">USD</span></span>|


<span data-ttu-id="98361-132">Izslēdzot **Standarta nosaukumu** kā cenas noteikšanas dimensiju un kad cenas noteikšanas programma meklē noteiktu cenu, tā izmantos tikai **Org. struktūrvienības** vērtību no ievades konteksta.</span><span class="sxs-lookup"><span data-stu-id="98361-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="98361-133">Ja ievades konteksta **Organizācijas struktūrvienība** ir Contoso ASV, rezultāts nebūs noteikts, jo abas rindas sakritīs.</span><span class="sxs-lookup"><span data-stu-id="98361-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="98361-134">Lai izvairītos no šāda scenārija, veidojot **Lomu cenu** ierakstus, sistēma pārbauda, lai dimensiju kombinācija ir unikāla.</span><span class="sxs-lookup"><span data-stu-id="98361-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="98361-135">Ja dimensija ir izslēgta pēc **Lomu cenu** izveides, šo ierobežojumu var pārkāpt.</span><span class="sxs-lookup"><span data-stu-id="98361-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="98361-136">Tāpēc pirms dimensijas izslēgšanas ir jādzēš visas **Lomu cenu** un **Lomu cenu uzcenojumu** rindas, kurām ir šī dimensijas vērtība.</span><span class="sxs-lookup"><span data-stu-id="98361-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
