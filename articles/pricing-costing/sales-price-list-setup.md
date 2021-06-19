---
title: Pārdošanas cenrāžu iestatīšana
description: Šajā tēmā ir sniegta informācija par pārdošanas cenrāžiem projekta cenu noteikšanai.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004900"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="69120-103">Pārdošanas cenrāžu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="69120-103">Set up a sales price list</span></span>

<span data-ttu-id="69120-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="69120-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="69120-105">Attiecībā uz projektu piedāvājumiem un līgumiem projekta cenrādim ir no preču cenrāža atšķirīgs cenas pārlabošanas modelis.</span><span class="sxs-lookup"><span data-stu-id="69120-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="69120-106">Preču kataloga piedāvājuma rindā varat pārlabot cenu uz lomām un kategorijām tieši piedāvājuma rindā, jo katra piedāvājuma rinda norāda uz vienu kataloga vienumu.</span><span class="sxs-lookup"><span data-stu-id="69120-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="69120-107">Taču projekta piedāvājuma rindā nevarat pārlabot cenu uz lomām un kategorijām tieši piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="69120-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="69120-108">Varat izmantot projekta cenrādi, lai strādātu ar divām atšķirīgām, pārlabotām sistēmām.</span><span class="sxs-lookup"><span data-stu-id="69120-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="69120-109">Ieteicams projekta resursiem un kataloga vienumiem izmantot atsevišķus cenrāžus, jo starp abiem pastāv uzvedības atšķirības, kad pārlabojat cenas.</span><span class="sxs-lookup"><span data-stu-id="69120-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="69120-110">Katrai no tālāk minētajām entītijām var būt viens vai vairāki piesaistītie pārdošanas cenrāži projekta izcenojumam.</span><span class="sxs-lookup"><span data-stu-id="69120-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="69120-111">Klients (uzņēmums)</span><span class="sxs-lookup"><span data-stu-id="69120-111">Customer (account)</span></span> 
- <span data-ttu-id="69120-112">Iespēja</span><span class="sxs-lookup"><span data-stu-id="69120-112">Opportunity</span></span> 
- <span data-ttu-id="69120-113">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="69120-113">Quote</span></span> 
- <span data-ttu-id="69120-114">Projekta līgums</span><span class="sxs-lookup"><span data-stu-id="69120-114">Project Contract</span></span>

<span data-ttu-id="69120-115">Šo entītiju saistību ar cenrādi norāda projekta cenrāži.</span><span class="sxs-lookup"><span data-stu-id="69120-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="69120-116">Varat saistīt vienu vai vairākus cenrāžus ar entītijām Klients, Iespēja, Piedāvājums un Projekta līguma pārdošana.</span><span class="sxs-lookup"><span data-stu-id="69120-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="69120-117">Noklusējuma projekta cenrādis netiek automātiski ievadīts klienta ierakstā.</span><span class="sxs-lookup"><span data-stu-id="69120-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="69120-118">Tomēr varat manuāli pievienot projekta cenrādi klienta ierakstam.</span><span class="sxs-lookup"><span data-stu-id="69120-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="69120-119">Taču projekta cenrādi drīkst manuāli pievienot tikai tad, ja jums ir pielāgots izcenojuma līgums ar klientu.</span><span class="sxs-lookup"><span data-stu-id="69120-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="69120-120">Kad pārdošanas entītijai tiek pievienots projekta cenrādis, tiek pārbaudīta šāda informācija:</span><span class="sxs-lookup"><span data-stu-id="69120-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="69120-121">Cenrādim ir entītijas **Pārdošana** konteksts.</span><span class="sxs-lookup"><span data-stu-id="69120-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="69120-122">Cenrāža valūta atbilst klienta valūtai.</span><span class="sxs-lookup"><span data-stu-id="69120-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="69120-123">Projekta līgumā izmanto tālāk norādīto prioritāšu secību, lai automātiski iestatītu saistītos projekta cenrāžus.</span><span class="sxs-lookup"><span data-stu-id="69120-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="69120-124">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="69120-124">Quote</span></span>
2. <span data-ttu-id="69120-125">Iespēja</span><span class="sxs-lookup"><span data-stu-id="69120-125">Opportunity</span></span>
3. <span data-ttu-id="69120-126">Klients</span><span class="sxs-lookup"><span data-stu-id="69120-126">Customer</span></span> 
4. <span data-ttu-id="69120-127">Globālie iestatījumi</span><span class="sxs-lookup"><span data-stu-id="69120-127">Global settings</span></span> 

<span data-ttu-id="69120-128">Kad projekta cenrādis tiek ievadīts pēc noklusējuma, sistēma pārbauda, vai šī valūta atbilst klienta valūtai un vai ievadītajiem noklusējuma cenrāžiem ir entītijas **Pārdošana** konteksts.</span><span class="sxs-lookup"><span data-stu-id="69120-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="69120-129">Varat saistīt vairākus cenrāžus ar entītijām Klients, Iespēja, Piedāvājums un Projekta līgums.</span><span class="sxs-lookup"><span data-stu-id="69120-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="69120-130">Šī iespēja atbalsta datumam specifiskas noklusējuma cenas ilgstošam projekta līgumam, kam var būt nepieciešams vairāk nekā viens cenrādis, lai uzskaitītu cenas atjauninājumus, kas rodas inflācijas dēļ.</span><span class="sxs-lookup"><span data-stu-id="69120-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="69120-131">Tomēr, ja cenrāžos, ko saistāt ar entītiju Klients, Iespēja, Piedāvājums vai Projekta līgums, pārklājas spēkā stāšanās datumi, noklusējuma cenas var būt nepareizas.</span><span class="sxs-lookup"><span data-stu-id="69120-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="69120-132">Tāpēc ir jāpārliecinās, vai projekta cenrāži, kam pārklājas spēkā esošie datumi, netiek saistīti ar šīm entītijām.</span><span class="sxs-lookup"><span data-stu-id="69120-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]