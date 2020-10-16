---
title: Projekta piedāvājuma izveide no iespējām
description: Šajā tēmā ir sniegta informācija par projekta piedāvājuma izveidi no iespējas.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898541"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="0f202-103">Projekta piedāvājuma izveide no iespējām</span><span class="sxs-lookup"><span data-stu-id="0f202-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="0f202-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="0f202-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0f202-105">Piedāvājumus var izveidot no projekta iespējām tālāk aprakstītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="0f202-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="0f202-106">No cilnes **Piedāvājumi** lapā **Projekta iespēja**</span><span class="sxs-lookup"><span data-stu-id="0f202-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="0f202-107">No Iespējas pārdošanas procesa plūsmas</span><span class="sxs-lookup"><span data-stu-id="0f202-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="0f202-108">Atjauninot iespējas atsauci esošam piedāvājumam</span><span class="sxs-lookup"><span data-stu-id="0f202-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="0f202-109">No lapas Projekta iespēja cilnes Piedāvājumi</span><span class="sxs-lookup"><span data-stu-id="0f202-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="0f202-110">Lai no iespējas izveidotu projekta piedāvājumu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0f202-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="0f202-111">Atveriet lapu **Projekta iespēja** un atlasiet cilni **Piedāvājumi**.</span><span class="sxs-lookup"><span data-stu-id="0f202-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="0f202-112">Apakšrežģī **Piedāvājumi** atlasiet opciju **+**, lai izveidotu jaunu projekta piedāvājumu, pamatojoties uz iespēju.</span><span class="sxs-lookup"><span data-stu-id="0f202-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="0f202-113">Visas iespējas rindas un saistītie Projekta cenrāži no iespējas tiek kopēti uz jauno piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="0f202-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="0f202-114">No Iespējas pārdošanas procesa plūsmas</span><span class="sxs-lookup"><span data-stu-id="0f202-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="0f202-115">Lai izveidotu piedāvājumu no Iespējas pārdošanas procesa plūsmas, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0f202-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="0f202-116">Iespējas pārdošanas procesa plūsmā atveriet vienumu Iespēja.</span><span class="sxs-lookup"><span data-stu-id="0f202-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="0f202-117">Atlasiet posmu **Kvalificēt**.</span><span class="sxs-lookup"><span data-stu-id="0f202-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="0f202-118">Atlasiet vienumu **Tālāk** un pēc tam vienumu **+ Izveidot**, lai izveidotu jaunu piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="0f202-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="0f202-119">Vairums informācijas, kas redzama šī jaunā piedāvājuma cilnē **Kopsavilkums**, pēc noklusējuma tiek pārņemta no iespējas.</span><span class="sxs-lookup"><span data-stu-id="0f202-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="0f202-120">Ievadiet trūkstošo nepieciešamo informāciju vai pēc vajadzības atjauniniet noklusējuma vērtības cilnē **Kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="0f202-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="0f202-121">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0f202-121">Select **Save**.</span></span> <span data-ttu-id="0f202-122">Jaunais piedāvājums tiek izveidots un saistīts ar iespēju.</span><span class="sxs-lookup"><span data-stu-id="0f202-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="0f202-123">Tagad piedāvājuma informāciju var apskatīt lapas **Piedāvājumi** cilnē **Piedāvājumi**.</span><span class="sxs-lookup"><span data-stu-id="0f202-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="0f202-124">Iespējas pārdošanas process pāriet uz nākamo posmu — **Piedāvāt**.</span><span class="sxs-lookup"><span data-stu-id="0f202-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="0f202-125">Atjauninot iespējas atsauci esošam piedāvājumam</span><span class="sxs-lookup"><span data-stu-id="0f202-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="0f202-126">Esošu piedāvājumu var saistīt ar Iespēju.</span><span class="sxs-lookup"><span data-stu-id="0f202-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="0f202-127">Izpildiet tālāk aprakstītās darbības, lai atjauninātu Iespējas informāciju par esošu piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="0f202-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="0f202-128">Atveriet lapu **Piedāvājums** un atlasiet cilni **Kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="0f202-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="0f202-129">Laukā **Iespēja** atlasiet iespēju, ko vēlaties saistīt ar piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="0f202-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="0f202-130">Piedāvājums ir redzams Iespējas režģī **Piedāvājumi**.</span><span class="sxs-lookup"><span data-stu-id="0f202-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="0f202-131">Izmantojot Iespējas pārdošanas procesu, iespēju var pārvirzīt uz nākamo posmu — **Piedāvāt**.</span><span class="sxs-lookup"><span data-stu-id="0f202-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="0f202-132">Pārvirzot iespēju uz šo posmu, šo piedāvājumu var atlasīt no piedāvājumu saraksta, kas saistīts ar šo iespēju.</span><span class="sxs-lookup"><span data-stu-id="0f202-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="0f202-133">Ja atlasāt šo piedāvājumu, tas nozīmē, ka jūs to turpināt īstenot.</span><span class="sxs-lookup"><span data-stu-id="0f202-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="0f202-134">Visi pārējie ar šo Iespēju saistītie piedāvājumi joprojām būs pieejami un aktīvi, līdz viens no tiem būs iegūts.</span><span class="sxs-lookup"><span data-stu-id="0f202-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="0f202-135">Pārdošanas procesu varat virzīt atpakaļ uz iepriekšējo posmu — **Kvalificēt**, un izvēlēties citu piedāvājumu, ko turpināt īstenot.</span><span class="sxs-lookup"><span data-stu-id="0f202-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
