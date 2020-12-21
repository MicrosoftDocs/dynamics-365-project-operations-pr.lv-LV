---
title: Produkta piedāvājuma rindas pārskats — Lite
description: Šajā tēmā ir sniegta informācija par darbu ar produkta piedāvājuma rindām.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178197"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="82d14-103">Produkta piedāvājuma rindas pārskats — Lite</span><span class="sxs-lookup"><span data-stu-id="82d14-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="82d14-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="82d14-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="82d14-105">Programmā Dynamics 365 Project Operations varat izveidot uz produktu balstītas piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="82d14-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="82d14-106">Uz produktu balstītas piedāvājuma rindas var būt manuāli pievienotas, vai tās var būt vienumi no produkti kataloga.</span><span class="sxs-lookup"><span data-stu-id="82d14-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="82d14-107">Preču katalogs</span><span class="sxs-lookup"><span data-stu-id="82d14-107">Product catalog</span></span>

<span data-ttu-id="82d14-108">Katram produktam produktu katalogā ir noklusējuma vienība un vienību grupa.</span><span class="sxs-lookup"><span data-stu-id="82d14-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="82d14-109">Ja vairākiem produktiem ir vienāda atribūtu kopa, varat izveidot produktu saimi, kurai kopīgi šie atribūti.</span><span class="sxs-lookup"><span data-stu-id="82d14-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="82d14-110">Piemēram, uzņēmums pārdod abonementa licences dažādu veidu programmatūrai.</span><span class="sxs-lookup"><span data-stu-id="82d14-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="82d14-111">Katrai abonējamajai programmatūrai ir divi tālāk norādītie atribūti.</span><span class="sxs-lookup"><span data-stu-id="82d14-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="82d14-112">Lietotāju skaits</span><span class="sxs-lookup"><span data-stu-id="82d14-112">Number of users</span></span>
- <span data-ttu-id="82d14-113">Abonementa ilgums mēnešos</span><span class="sxs-lookup"><span data-stu-id="82d14-113">A subscription duration measured in months</span></span>

<span data-ttu-id="82d14-114">Lai uzturētu šāda tipa katalogu, izveidojiet produktu saimi, kuras nosaukums ir **Abonējama programmatūra**, un kā atribūtus pievienojiet lietotāju skaitu un abonementa ilgumu.</span><span class="sxs-lookup"><span data-stu-id="82d14-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="82d14-115">Pēc tam varat pievienot atsevišķus produktus produktu saimei **Abonējama programmatūra**.</span><span class="sxs-lookup"><span data-stu-id="82d14-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="82d14-116">Produktu kataloga vienumu pievienošana projekta piedāvājumam</span><span class="sxs-lookup"><span data-stu-id="82d14-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="82d14-117">Lapās **Projekta piedāvājums** un **Projekta līgums** ir sadaļas, kas paredzētas uz projektu balstītām rindām un uz produktu balstītām rindām.</span><span class="sxs-lookup"><span data-stu-id="82d14-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="82d14-118">Attiecībā uz produkta rindām — piedāvājuma rindas vai projekta līguma rindas nolaižamajā sarakstā ir iekļauti visi produkti un vienības attiecīgajā produktu cenrādī.</span><span class="sxs-lookup"><span data-stu-id="82d14-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="82d14-119">Varat arī pievienot produktus, kas neveido daļu no produktu cenrāža.</span><span class="sxs-lookup"><span data-stu-id="82d14-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="82d14-120">Turklāt varat atlasīt produktus no citiem cenrāžiem vai tieši no produktu kataloga.</span><span class="sxs-lookup"><span data-stu-id="82d14-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="82d14-121">Ja produktus atlasāt tieši no kāda produktu kataloga, lai iegūtu produkta pārdošanas cenu, tiek izmantots šī produkta noklusējuma cenrādis.</span><span class="sxs-lookup"><span data-stu-id="82d14-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="82d14-122">Ja noklusējuma cenrādis nav iestatīts, cena tiek iestatīta uz nulli (0).</span><span class="sxs-lookup"><span data-stu-id="82d14-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="82d14-123">Kad piedāvājuma rinda ir balstīta uz produktu katalogu, pārdošanas cenu varat pārlabot tieši piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="82d14-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="82d14-124">Piedāvājuma rinda laukā **Cenu noteikšana** ar divām pieejamām vērtībām:</span><span class="sxs-lookup"><span data-stu-id="82d14-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="82d14-125">**Pārlabot izcenojumu**</span><span class="sxs-lookup"><span data-stu-id="82d14-125">**Override Pricing**</span></span>
- <span data-ttu-id="82d14-126">**Izmantot noklusējumu**</span><span class="sxs-lookup"><span data-stu-id="82d14-126">**Use Default**</span></span>

<span data-ttu-id="82d14-127">Ja atlasāt **Pārlabot izcenojumu**, noklusējuma cena netiek iestatīta.</span><span class="sxs-lookup"><span data-stu-id="82d14-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="82d14-128">Tā vietā jums ir jāievada cena šim produktam piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="82d14-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="82d14-129">Ja atlasāt opciju **Lietot noklusējumu**, tiek izmantota noklusējuma pārdošanas cena, kā arī lauks ir slēgts rediģēšanai.</span><span class="sxs-lookup"><span data-stu-id="82d14-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="82d14-130">Piedāvājuma produktu rindās tiek ievadītas noklusējuma pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="82d14-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="82d14-131">Pēc tam lauks **Cenu noteikšana** tiek iestatīts uz **Pārlabot izcenojumu**, lai jūs varētu rediģēt noteiktā cenu piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="82d14-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="82d14-132">Šī ir risinājumam Project Operations specifiska pārlabošana uz produkta rindu uzvedību programmā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="82d14-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>