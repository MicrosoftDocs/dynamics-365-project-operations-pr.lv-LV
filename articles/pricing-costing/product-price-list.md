---
title: Produktu cenrāži
description: Šajā tēmā sniegta informācija par cenu sarakstiem katalogu cenrāžos, ko izmanto projektu piedāvājumos un līgumos.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877499"
---
# <a name="product-price-lists"></a><span data-ttu-id="ebfad-103">Produktu cenrāži</span><span class="sxs-lookup"><span data-stu-id="ebfad-103">Product price lists</span></span>

<span data-ttu-id="ebfad-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="ebfad-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="ebfad-105">Programmā Project Operations **produktu cenrāži** un ar tiem saistītās cenrāža elementu entītijas atbalsta funkcionalitāti produktu cenu noteikšanai pēc produkta piedāvājuma un līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="ebfad-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="ebfad-106">Projektos lietotajiem produktiem tiek izmantoti projekta cenrāži ar cenrāža elementu ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="ebfad-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="ebfad-107">Produkti ir jāiestata tā, lai produktu katalogā tiem būtu noklusējuma izmaksu un cenu saraksti.</span><span class="sxs-lookup"><span data-stu-id="ebfad-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="ebfad-108">Šī saraksta cena, standarta izmaksas un pašreizējās izmaksas ir jāizmanto, lai konfigurētu noklusējuma izmaksas un saraksta cenas.</span><span class="sxs-lookup"><span data-stu-id="ebfad-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="ebfad-109">Noklusējuma saraksta cenas piedāvājuma rindā vai projekta līguma rindā tiek izmantotas tikai tad, ja sistēma nevar atrast attiecīgā produkta cenrāža rindu piedāvājuma vai projekta līguma produktu cenrādī.</span><span class="sxs-lookup"><span data-stu-id="ebfad-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="ebfad-110">Produktu kataloga rindu izmaksu cenu starp piedāvājumiem var mainīt.</span><span class="sxs-lookup"><span data-stu-id="ebfad-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="ebfad-111">Šī iespēja ir svarīga, jo, ja netiek veikta precīza izmaksu izsekošana, nevar noteikt operatīvo peļņu no projekta saistībām.</span><span class="sxs-lookup"><span data-stu-id="ebfad-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="ebfad-112">Pēc noklusējuma kā izmaksu cena tiek izmantota produkta standarta cena.</span><span class="sxs-lookup"><span data-stu-id="ebfad-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="ebfad-113">Taču piedāvājuma rindā noklusējuma izmaksu cenu var atjaunināt, ja šim piedāvājumam ir citāda izmaksu cena.</span><span class="sxs-lookup"><span data-stu-id="ebfad-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="ebfad-114">Cenrāža elementi</span><span class="sxs-lookup"><span data-stu-id="ebfad-114">Price list items</span></span>

<span data-ttu-id="ebfad-115">Produktus no produktu kataloga varat pievienot dažādiem cenrāžiem.</span><span class="sxs-lookup"><span data-stu-id="ebfad-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="ebfad-116">Cenrāža rindas produktiem vienmēr atsaucas uz noteiktu vienību.</span><span class="sxs-lookup"><span data-stu-id="ebfad-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="ebfad-117">Cenrāža elementos minēta produkta cenas noteikšanu var konfigurēt kā valūtas summu.</span><span class="sxs-lookup"><span data-stu-id="ebfad-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="ebfad-118">Vai arī to var konfigurēt kā saraksta cenas, pašreizējo izmaksu vai standarta izmaksu funkciju.</span><span class="sxs-lookup"><span data-stu-id="ebfad-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="ebfad-119">Cenu noteikšanas funkcionalitāte atbalsta dažādas noapaļošanas opcijas, kad produktu cenas tiek konfigurētas kā saraksta cenas, standarta izmaksu vai pašreizējo izmaksu funkcija.</span><span class="sxs-lookup"><span data-stu-id="ebfad-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="ebfad-120">Papildus vairāku cenu noteikšanas metožu un noapaļošanas opciju izmantošanai ir iespējams arī sasaistīt atlaižu sarakstus un cenrāža elementus.</span><span class="sxs-lookup"><span data-stu-id="ebfad-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="ebfad-121">Noklusējuma produktu cenrādis</span><span class="sxs-lookup"><span data-stu-id="ebfad-121">Default product price list</span></span>
<span data-ttu-id="ebfad-122">Katram klienta ierakstam ir lauks **Noklusējuma cenrādis**, kur varat norādīt cenrādi, kurš atbilst šī klienta valūtai.</span><span class="sxs-lookup"><span data-stu-id="ebfad-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="ebfad-123">Šajā laukā noklusējuma vērtība netiek ievadīta automātiski.</span><span class="sxs-lookup"><span data-stu-id="ebfad-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="ebfad-124">Ja ar noteiktu klientu pastāv pielāgota vienošanās par cenu noteikšanu, šo lauku varat izmantot, lai saistītu kādu cenrādi ar šo klientu.</span><span class="sxs-lookup"><span data-stu-id="ebfad-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="ebfad-125">Lai ievadītu noklusējuma produktu cenrāžus, iespējas, piedāvājuma un projekta līguma entītijas izmanto tālāk norādīto secību.</span><span class="sxs-lookup"><span data-stu-id="ebfad-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="ebfad-126">Tāda pati secība tiek izmantota projektu cenrāžiem.</span><span class="sxs-lookup"><span data-stu-id="ebfad-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="ebfad-127">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="ebfad-127">Quote</span></span>
2.  <span data-ttu-id="ebfad-128">Iespēja</span><span class="sxs-lookup"><span data-stu-id="ebfad-128">Opportunity</span></span>
3.  <span data-ttu-id="ebfad-129">Klients</span><span class="sxs-lookup"><span data-stu-id="ebfad-129">Customer</span></span>
4.  <span data-ttu-id="ebfad-130">Globālie iestatījumi</span><span class="sxs-lookup"><span data-stu-id="ebfad-130">Global settings</span></span> 

<span data-ttu-id="ebfad-131">Pēc noklusējuma piedāvājuma rindas laukā **Produkts** ir uzskaitīti visi aktīvie produkti, kas atrodas attiecīgā piedāvājuma produktu cenrādī.</span><span class="sxs-lookup"><span data-stu-id="ebfad-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="ebfad-132">Ja kāds produkts ir deaktivizēts vai ja tas ir melnraksta produkts, tas nav iekļauts sarakstā pat tad, ja šis produkts ir cenrādī.</span><span class="sxs-lookup"><span data-stu-id="ebfad-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="ebfad-133">Produktu kataloga rindas tiek pievienotas kā rēķina rindas pirmajā rēķinā, kurš tiek izveidots projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="ebfad-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="ebfad-134">Melnraksta rēķinā šīs rēķina rindas var izdzēst.</span><span class="sxs-lookup"><span data-stu-id="ebfad-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="ebfad-135">Tādā gadījumā rindas būs redzamas nākamajā rēķinā, līdz par tām ir izrakstīts rēķins vai līdz rēķins tiek nosūtīts klientam.</span><span class="sxs-lookup"><span data-stu-id="ebfad-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="ebfad-136">Produkta rēķina rindā nevar izrakstīt rēķinu par daļēju daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ebfad-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="ebfad-137">Kad tiek izrakstīts rēķins par produktu rindām no projekta līguma, tiek izveidotas faktiskās vērtības.</span><span class="sxs-lookup"><span data-stu-id="ebfad-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="ebfad-138">Taču šīs faktiskās vērtības nav sasaistītas ar attiecīgo projekta entītiju.</span><span class="sxs-lookup"><span data-stu-id="ebfad-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="ebfad-139">Citiem vārdiem sakot, uz produktu balstītās projekta līguma rindas ir neatkarīgas no jebkāda uz projektu balstītā lietojuma.</span><span class="sxs-lookup"><span data-stu-id="ebfad-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
