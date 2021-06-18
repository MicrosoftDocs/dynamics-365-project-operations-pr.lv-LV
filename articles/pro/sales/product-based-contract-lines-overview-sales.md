---
title: Uz produktiem balstītu līgumu rindu pārskats — Lite
description: Šajā tēmā ir sniegta informācija par līguma rindām, kuras ir balstītas uz produktu.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f248865287cdd3b1fdb3bbc40ad1c48b5302c2c0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994550"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="74ae7-103">Uz produktiem balstītu līgumu rindu pārskats — Lite</span><span class="sxs-lookup"><span data-stu-id="74ae7-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="74ae7-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="74ae7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="74ae7-105">Programmā Dynamics 365 Project Operations varat izveidot uz produktu balstītas līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="74ae7-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="74ae7-106">Uz produktu balstītas līguma rindas var būt manuāli izveidotas rindas, vai tās var būt vienumi no produktu kataloga.</span><span class="sxs-lookup"><span data-stu-id="74ae7-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="74ae7-107">Preču katalogs</span><span class="sxs-lookup"><span data-stu-id="74ae7-107">Product catalog</span></span>

<span data-ttu-id="74ae7-108">Produktiem preču katalogā ir noklusējuma vienība un vienību grupa.</span><span class="sxs-lookup"><span data-stu-id="74ae7-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="74ae7-109">Ja vairākiem produktiem ir vienāda atribūtu kopa, varat izveidot produktu saimi, kurai arī ir šie atribūti.</span><span class="sxs-lookup"><span data-stu-id="74ae7-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="74ae7-110">Visi produkti vienā produktu saimē pārmanto vienādu atribūtu kopu.</span><span class="sxs-lookup"><span data-stu-id="74ae7-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="74ae7-111">Piemēram, uzņēmums pārdod abonementa licences dažādu veidu programmatūrai.</span><span class="sxs-lookup"><span data-stu-id="74ae7-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="74ae7-112">Katrai abonējamajai programmatūrai ir divi tālāk norādītie atribūti.</span><span class="sxs-lookup"><span data-stu-id="74ae7-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="74ae7-113">Lietotāju skaits</span><span class="sxs-lookup"><span data-stu-id="74ae7-113">Number of users</span></span>
- <span data-ttu-id="74ae7-114">Abonementa ilgums (mēnešos)</span><span class="sxs-lookup"><span data-stu-id="74ae7-114">Subscription duration (in months)</span></span>

<span data-ttu-id="74ae7-115">Lai uzturētu šāda tipa katalogu, izveidojiet produktu saimi, kuras nosaukums ir **Abonēšanas programmatūra**.</span><span class="sxs-lookup"><span data-stu-id="74ae7-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="74ae7-116">Pievienojiet atribūtus **Lietotāju skaits** un **Abonementa ilgums** produktu saimei.</span><span class="sxs-lookup"><span data-stu-id="74ae7-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="74ae7-117">Pēc tam pievienojiet **Abonementa programmatūra** produktu saimei atsevišķus produktus.</span><span class="sxs-lookup"><span data-stu-id="74ae7-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="74ae7-118">Produktu kataloga vienumu pievienošana projekta līgumam</span><span class="sxs-lookup"><span data-stu-id="74ae7-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="74ae7-119">Projekta līgumam ir sadaļas divu tipu rindām: uz projektu balstītām rindām un uz produktu balstītām rindām.</span><span class="sxs-lookup"><span data-stu-id="74ae7-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="74ae7-120">Produktu bāzētās rindās ir iekļauti visi līguma produktu cenrāža produkti un vienības.</span><span class="sxs-lookup"><span data-stu-id="74ae7-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="74ae7-121">Var pievienot produktus, kas nav iekļauti līguma produktu cenrādī.</span><span class="sxs-lookup"><span data-stu-id="74ae7-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="74ae7-122">Varat atlasīt produktus no citiem cenrāžiem vai tieši no preču kataloga.</span><span class="sxs-lookup"><span data-stu-id="74ae7-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="74ae7-123">Ja produktus atlasāt tieši no kāda preču kataloga, lai iegūtu produkta pārdošanas cenu, tiek izmantots šī produkta noklusējuma cenrādis.</span><span class="sxs-lookup"><span data-stu-id="74ae7-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="74ae7-124">Ja noklusējuma cenrādis nav iestatīts, cena tiek iestatīta uz 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="74ae7-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="74ae7-125">Ja līguma rinda ir balstīta uz preču katalogu, pārdošanas cenu varat pārlabot tieši rindā.</span><span class="sxs-lookup"><span data-stu-id="74ae7-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="74ae7-126">Līguma rindai ir lauks **Cenu noteikšana** ar divām vērtībām:</span><span class="sxs-lookup"><span data-stu-id="74ae7-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="74ae7-127">**Pārlabot izcenojumu**</span><span class="sxs-lookup"><span data-stu-id="74ae7-127">**Override pricing**</span></span>
- <span data-ttu-id="74ae7-128">**Izmantot noklusējumu**</span><span class="sxs-lookup"><span data-stu-id="74ae7-128">**Use default**</span></span>

<span data-ttu-id="74ae7-129">Ja iestatāt lauku **Cenu noteikšana** uz **Pārlabot cenu noteikšanu**, noklusējuma cena nav iestatīta.</span><span class="sxs-lookup"><span data-stu-id="74ae7-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="74ae7-130">Ievadiet produkta cenu līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="74ae7-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="74ae7-131">Ja iestatījāt lauku uz **Izmantotu noklusējumu**, tiek izmantota noklusējuma pārdošanas cena un lauku nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="74ae7-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="74ae7-132">Pēc Project Operations instalēšanas noklusētās pārdošanas cenas tiek ievadītas līguma produktu rindās.</span><span class="sxs-lookup"><span data-stu-id="74ae7-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="74ae7-133">Lauks **Cenu noteikšana** tiek iestatīts uz **Pārlabot cenu noteikšanu**, lai jūs varētu rediģēt noteiktā cenu līguma rindās.</span><span class="sxs-lookup"><span data-stu-id="74ae7-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="74ae7-134">Šī ir Project Operations specifiska pārlabošana uz produktu bāzētu līniju uzvedībai risinājumā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="74ae7-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]