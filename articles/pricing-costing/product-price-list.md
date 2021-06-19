---
title: Produktu cenrāži
description: Šajā tēmā sniegta informācija par cenu sarakstiem katalogu cenrāžos, ko izmanto projektu piedāvājumos un līgumos.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 02d274725983e50adc35a4cae1ac60c35be346a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004945"
---
# <a name="product-price-lists"></a><span data-ttu-id="5f5ae-103">Produktu cenrāži</span><span class="sxs-lookup"><span data-stu-id="5f5ae-103">Product price lists</span></span>

<span data-ttu-id="5f5ae-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="5f5ae-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="5f5ae-105">Programmā Project Operations **produktu cenrāži** un ar tiem saistītās cenrāža elementu entītijas atbalsta funkcionalitāti produktu cenu noteikšanai pēc produkta piedāvājuma un līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="5f5ae-106">Projektos lietotajiem produktiem tiek izmantoti projekta cenrāži ar cenrāža elementu ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="5f5ae-107">Produkti ir jāiestata tā, lai produktu katalogā tiem būtu noklusējuma izmaksu un cenu saraksti.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="5f5ae-108">Šī saraksta cena, standarta izmaksas un pašreizējās izmaksas ir jāizmanto, lai konfigurētu noklusējuma izmaksas un saraksta cenas.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="5f5ae-109">Noklusējuma saraksta cenas piedāvājuma rindā vai projekta līguma rindā tiek izmantotas tikai tad, ja sistēma nevar atrast attiecīgā produkta cenrāža rindu piedāvājuma vai projekta līguma produktu cenrādī.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="5f5ae-110">Produktu kataloga rindu izmaksu cenu starp piedāvājumiem var mainīt.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="5f5ae-111">Šī iespēja ir svarīga, jo, ja netiek veikta precīza izmaksu izsekošana, nevar noteikt operatīvo peļņu no projekta saistībām.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="5f5ae-112">Pēc noklusējuma kā izmaksu cena tiek izmantota produkta standarta cena.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="5f5ae-113">Taču piedāvājuma rindā noklusējuma izmaksu cenu var atjaunināt, ja šim piedāvājumam ir citāda izmaksu cena.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="5f5ae-114">Cenrāža elementi</span><span class="sxs-lookup"><span data-stu-id="5f5ae-114">Price list items</span></span>

<span data-ttu-id="5f5ae-115">Produktus no produktu kataloga varat pievienot dažādiem cenrāžiem.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="5f5ae-116">Cenrāža rindas produktiem vienmēr atsaucas uz noteiktu vienību.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="5f5ae-117">Cenrāža elementos minēta produkta cenas noteikšanu var konfigurēt kā valūtas summu.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="5f5ae-118">Vai arī to var konfigurēt kā saraksta cenas, pašreizējo izmaksu vai standarta izmaksu funkciju.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="5f5ae-119">Cenu noteikšanas funkcionalitāte atbalsta dažādas noapaļošanas opcijas, kad produktu cenas tiek konfigurētas kā saraksta cenas, standarta izmaksu vai pašreizējo izmaksu funkcija.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="5f5ae-120">Papildus vairāku cenu noteikšanas metožu un noapaļošanas opciju izmantošanai ir iespējams arī sasaistīt atlaižu sarakstus un cenrāža elementus.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="5f5ae-121">Noklusējuma produktu cenrādis</span><span class="sxs-lookup"><span data-stu-id="5f5ae-121">Default product price list</span></span>
<span data-ttu-id="5f5ae-122">Katram klienta ierakstam ir lauks **Noklusējuma cenrādis**, kur varat norādīt cenrādi, kurš atbilst šī klienta valūtai.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="5f5ae-123">Šajā laukā noklusējuma vērtība netiek ievadīta automātiski.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="5f5ae-124">Ja ar noteiktu klientu pastāv pielāgota vienošanās par cenu noteikšanu, šo lauku varat izmantot, lai saistītu kādu cenrādi ar šo klientu.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="5f5ae-125">Lai ievadītu noklusējuma produktu cenrāžus, iespējas, piedāvājuma un projekta līguma entītijas izmanto tālāk norādīto secību.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="5f5ae-126">Tāda pati secība tiek izmantota projektu cenrāžiem.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="5f5ae-127">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="5f5ae-127">Quote</span></span>
2.  <span data-ttu-id="5f5ae-128">Iespēja</span><span class="sxs-lookup"><span data-stu-id="5f5ae-128">Opportunity</span></span>
3.  <span data-ttu-id="5f5ae-129">Klients</span><span class="sxs-lookup"><span data-stu-id="5f5ae-129">Customer</span></span>
4.  <span data-ttu-id="5f5ae-130">Globālie iestatījumi</span><span class="sxs-lookup"><span data-stu-id="5f5ae-130">Global settings</span></span> 

<span data-ttu-id="5f5ae-131">Pēc noklusējuma piedāvājuma rindas laukā **Produkts** ir uzskaitīti visi aktīvie produkti, kas atrodas attiecīgā piedāvājuma produktu cenrādī.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="5f5ae-132">Ja kāds produkts ir deaktivizēts vai ja tas ir melnraksta produkts, tas nav iekļauts sarakstā pat tad, ja šis produkts ir cenrādī.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="5f5ae-133">Produktu kataloga rindas tiek pievienotas kā rēķina rindas pirmajā rēķinā, kurš tiek izveidots projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="5f5ae-134">Melnraksta rēķinā šīs rēķina rindas var izdzēst.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="5f5ae-135">Tādā gadījumā rindas būs redzamas nākamajā rēķinā, līdz par tām ir izrakstīts rēķins vai līdz rēķins tiek nosūtīts klientam.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="5f5ae-136">Produkta rēķina rindā nevar izrakstīt rēķinu par daļēju daudzumu.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="5f5ae-137">Kad tiek izrakstīts rēķins par produktu rindām no projekta līguma, tiek izveidotas faktiskās vērtības.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="5f5ae-138">Taču šīs faktiskās vērtības nav sasaistītas ar attiecīgo projekta entītiju.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="5f5ae-139">Citiem vārdiem sakot, uz produktu balstītās projekta līguma rindas ir neatkarīgas no jebkāda uz projektu balstītā lietojuma.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
