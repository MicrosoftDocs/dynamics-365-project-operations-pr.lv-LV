---
title: Uz produktu balstītas piedāvājuma rindas
description: Šajā tēmā ir sniegta informācija par piedāvājuma rindām, kuras ir balstītas uz produktu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c3b2b35abe894e79d6f55a7ddd6e5c64d0f12f2
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123212"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="1b6b9-103">Uz produktu balstītas piedāvājuma rindas</span><span class="sxs-lookup"><span data-stu-id="1b6b9-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="1b6b9-104">Programmā Dynamics 365 Project Service Automation varat izveidot uz produktu balstītas piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="1b6b9-105">Uz produktu balstītas piedāvājuma rindas var būt “ierakstāmas” rindas, vai tās var būt vienumi no produkti kataloga.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="1b6b9-106">Preču katalogs</span><span class="sxs-lookup"><span data-stu-id="1b6b9-106">Product catalog</span></span>

<span data-ttu-id="1b6b9-107">Produktiem Dynamics 365 produktu katalogā ir noklusējuma vienība un vienību grupa.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="1b6b9-108">Ja vairākiem produktiem ir vienāda atribūtu kopa, varat izveidot produktu saimi, kurai arī ir šie atribūti.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="1b6b9-109">Visi produkti vienā produktu saimē pārmanto vienādu atribūtu kopu.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="1b6b9-110">Piemēram, uzņēmums pārdod abonementa licences dažāda veida programmatūrai.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="1b6b9-111">Katrai abonējamajai programmatūrai ir divi tālāk norādītie atribūti.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="1b6b9-112">Lietotāju skaits</span><span class="sxs-lookup"><span data-stu-id="1b6b9-112">Number of users</span></span> 
- <span data-ttu-id="1b6b9-113">Abonementa ilgums (mēnešos)</span><span class="sxs-lookup"><span data-stu-id="1b6b9-113">Subscription duration (in months)</span></span>

<span data-ttu-id="1b6b9-114">Labs veids, kā uzturēt šāda tipa katalogu, ir izveidot produktu saimi, kuras nosaukums ir **Abonējama programmatūra** un kurai ir atribūti **Lietotāju skaits** un **Abonementa ilgums**.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="1b6b9-115">Pēc tam produktu saimei **Abonējama programmatūra** varat pievienot atsevišķus produktus, piemēram, **Dynamics 365 Sales** vai **Dynamics 365 Field Service**.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="1b6b9-116">Produktu kataloga vienumu pievienošana projekta piedāvājumam</span><span class="sxs-lookup"><span data-stu-id="1b6b9-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="1b6b9-117">Projekta piedāvājuma un projekta līguma lapās ir sadaļas divu tipu rindām: uz projektu balstītām rindām un uz produktu balstītām rindām.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="1b6b9-118">Rindām, kas ir balstītas uz produktu, programmatūra Dynamics 365 tiek izmantota, lai piedāvājumam pievienotu vienumus no produktu kataloga.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="1b6b9-119">Piedāvājuma rindas vai projekta līguma rindas nolaižamajā sarakstā ir iekļauti visi produkti un vienības attiecīgajā produktu cenrādī, kurš ir pievienots šim piedāvājumam vai projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="1b6b9-120">Varat arī pievienot produktus, kas neveido daļu no piedāvājuma produktu cenrāža.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="1b6b9-121">Turklāt varat atlasīt produktus no citiem cenrāžiem, kā arī varat atlasīt produktus tieši no produktu kataloga.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="1b6b9-122">Ja produktus atlasāt tieši no kāda produktu kataloga, lai iegūtu produkta pārdošanas cenu, tiek izmantots šī produkta noklusējuma cenrādis.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="1b6b9-123">Ja noklusējuma cenrādis nav iestatīts, cena tiek iestatīta uz 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="1b6b9-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="1b6b9-124">Ja piedāvājuma rinda ir balstīta uz produktu katalogu, pārdošanas cenu varat pārlabot tieši piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="1b6b9-125">Ņemiet vērā, ka piedāvājuma rindai programmatūrā Dynamics 365 ir lauks **Cenu noteikšana**.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="1b6b9-126">Ir pieejamas divas vērtības:</span><span class="sxs-lookup"><span data-stu-id="1b6b9-126">Two values are available:</span></span>

- <span data-ttu-id="1b6b9-127">Pārlabot izcenojumu</span><span class="sxs-lookup"><span data-stu-id="1b6b9-127">Override pricing</span></span>  
- <span data-ttu-id="1b6b9-128">Izmantot noklusējumu</span><span class="sxs-lookup"><span data-stu-id="1b6b9-128">Use default</span></span>

<span data-ttu-id="1b6b9-129">Ja šo lauku iestatāt uz **Pārlabot izcenojumu**, Dynamics 365 neiestata noklusējuma cenu.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="1b6b9-130">Jums ir jāievada cena šim produktam piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="1b6b9-131">Ja šo lauku iestatāt uz **Izmantot noklusējumu**, Dynamics 365 izmanto noklusējuma pārdošanas cenu un bloķē šo lauku, lai nepieļautu turpmāku rediģēšanu.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="1b6b9-132">Pēc PSA instalēšanas piedāvājuma uz produktu balstītajās rindās tiek ievadītas noklusējuma pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="1b6b9-133">Pēc tam lauks **Cenu noteikšana** tiek iestatīts uz **Pārlabot izcenojumu**, lai jūs varētu rediģēt noteiktā cenu piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Cenu pārlabošanas iestatīšana](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="1b6b9-135">Daudzuma koeficienti produktiem</span><span class="sxs-lookup"><span data-stu-id="1b6b9-135">Quantity factors for products</span></span>

<span data-ttu-id="1b6b9-136">Lai atbalstītu uz abonēšanu balstītu produktu pārdošanu, PSA izmanto daudzuma koeficientus.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="1b6b9-137">Uz abonēšanu balstītiem produktiem daudzums piedāvājumā vai projekta līguma rindā tiek izteikts kā lietotāju mēnešu skaits.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="1b6b9-138">Parasti abonējamas programmatūras cena katalogā tiek glabāta kā cena vienam lietotājam vienā mēnesī.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="1b6b9-139">Taču varat izmantot arī citus laika aprakstus.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="1b6b9-140">Pārdošanas procesa laikā cena piedāvājuma rindā parasti ir vienam lietotājam, viena mēneša cena, par kuru notika pārrunas un kuras atlaidi noteica IT pārdošanas aģents.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="1b6b9-141">Katram darījumam ir atšķirīgs lietotāju skaits un atšķirīgs abonēšanas mēnešu skaits.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="1b6b9-142">Daudzums, kas tiek izmantots piedāvājuma rindas summas aprēķināšanai, ir lietotāju skaita un abonēšanas mēnešu skaita reizinājums.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="1b6b9-143">Lai atbalstītu šāda tipa pārdošanu, PSA ieviesa daudzuma koeficientu jēdzienu.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="1b6b9-144">Daudzuma koeficienti izmanto produkta atribūtus programmā Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="1b6b9-145">Kad kādam produktam konfigurējat konkrētus rekvizītus, PSA ļauj jums atzīmēt šo rekvizītu apakškopu vai visus rekvizītus kā daudzuma faktorus.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="1b6b9-146">PSA pārliecinās, ka kā daudzuma koeficienti ir atzīmēti tikai skaitliskie rekvizīti vai produktu rekvizīti, kuriem ir skaitlisks datu tips.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="1b6b9-147">Ja produkts, kuram ir konfigurēti daudzuma koeficienti, tiek pievienots piedāvājuma rindai, lauks **Daudzums** šajā piedāvājuma rindā kļūst par tikai lasāmu lauku.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="1b6b9-148">Kad produktu rekvizītiem ir ievadītas vērtības, kas ir daudzuma koeficienti, PSA aprēķina piedāvājuma rindas daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="1b6b9-149">Programmatūrā Dynamics 365 varētu būt, piemēram, tālāk norādītie rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="1b6b9-150">**Lietotāju skaits** — lietotāju skaits</span><span class="sxs-lookup"><span data-stu-id="1b6b9-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="1b6b9-151">**Mēnešu skaits** — abonēšanas mēnešu skaits</span><span class="sxs-lookup"><span data-stu-id="1b6b9-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="1b6b9-152">**Produkta SKU**</span><span class="sxs-lookup"><span data-stu-id="1b6b9-152">**Product SKU**</span></span> 

<span data-ttu-id="1b6b9-153">Rekvizītus **Lietotāju skaits** un **Mēnešu skaits** var atzīmēt kā daudzuma koeficientus, rediģējot produkta rindas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="1b6b9-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Lietotāju skaita un mēnešu skaita kā kvalitātes koeficientu atzīmēšana](media/basic-guide-11.png)
 
