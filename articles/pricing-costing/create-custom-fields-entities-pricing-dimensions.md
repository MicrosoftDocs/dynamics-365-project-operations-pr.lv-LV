---
title: Pielāgotu lauku un entītiju kā cenu noteikšanas kategoriju izveide
description: Šajā tēmā sniegta informācija par to, kā izveidot pielāgotas opciju kopas vai entitījas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080482"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="38679-103">Pielāgotu lauku un entītiju kā cenu noteikšanas kategoriju izveide</span><span class="sxs-lookup"><span data-stu-id="38679-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="38679-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="38679-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="38679-105">Veiciet tālāk norādītās darbības jebkurā laikā, kad vēlaties izveidot pielāgotu opciju kopu vai entītiju.</span><span class="sxs-lookup"><span data-stu-id="38679-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="38679-106">Iesakām veikt visas pielāgotās cenu noteikšanas dimensijas izmaiņas katrā atsevišķā risinājumā.</span><span class="sxs-lookup"><span data-stu-id="38679-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="38679-107">Šī svarīgā paraugprakse nodrošina elastību nākotnē, lai atjauninātu vai noņemtu nepieciešamās izmaiņas; tā palīdzēs ar jūsu darba atkārtotu izmantošanu un vienkāršos šo izmaiņu saglabāšanu citā gadījumā.</span><span class="sxs-lookup"><span data-stu-id="38679-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="38679-108">Pēc visu nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldīts risinājums** un importējiet to citās instancēs, lai izmantotu cenas noteikšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="38679-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="38679-109">Pielāgota risinājuma izveide cenu noteikšanas dimensijām</span><span class="sxs-lookup"><span data-stu-id="38679-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="38679-110">Dodieties uz **Iestatījumi** > **Risinājumi** un pēc tam atlasiet **Jauns** , lai izveidotu jaunu risinājumu.</span><span class="sxs-lookup"><span data-stu-id="38679-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="38679-111">Nosauciet risinājumu **\<your organization name>cenu noteikšanas dimensijas** , ievadiet atlikušo nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="38679-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="38679-112">Pielāgotu lauku un opciju kopu izveide izmaksu dimensijas risinājumā</span><span class="sxs-lookup"><span data-stu-id="38679-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="38679-113">Cenas noteikšanas dimensija var būt opciju kopa vai entītija.</span><span class="sxs-lookup"><span data-stu-id="38679-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="38679-114">Abi ir jāizveido cenas noteikšanas risinājumā.</span><span class="sxs-lookup"><span data-stu-id="38679-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="38679-115">Šīs procedūras darbībās ir paskaidrots, kā izveidot entītiju pamatotas dimensijas un opciju kopas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="38679-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="38679-116">Entītiju pamatotas dimensijas</span><span class="sxs-lookup"><span data-stu-id="38679-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="38679-117">Dodieties uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="38679-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="38679-118">Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet vienumu **Entītijas**.</span><span class="sxs-lookup"><span data-stu-id="38679-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="38679-119">Atlasiet **Jauns** , lai izveidotu jaunu entītiju ar nosaukumu **Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="38679-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="38679-120">Ievadiet pārējo pieprasīto informāciju un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="38679-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="38679-121">Opciju kopas dimensijas</span><span class="sxs-lookup"><span data-stu-id="38679-121">Option set-based dimensions</span></span> 
<span data-ttu-id="38679-122">Var izveidot divas opciju kopas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="38679-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="38679-123">Izmantojiet sadaļu **Resursa darba vieta** , lai izsekotu cenai opcijās **Mājas** un **Darbā** , kā arī lietotu **Resursa darba stundas** ar vērtībām **Regulārs** un **Virsstundas** , lai pievienotu atzīmi, kad darbs ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="38679-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="38679-124">Dodieties uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="38679-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="38679-125">Sadaļas Risinājumu pārlūks kreisajā navigācijas rūtī atlasiet vienumu **Opciju kopas**.</span><span class="sxs-lookup"><span data-stu-id="38679-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="38679-126">Atlasiet **Jauns** , lai izveidotu jaunu opciju kopu, ievadiet atlikušo nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="38679-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="38679-127">Datu izveide entītijai atbilstošām dimensijām</span><span class="sxs-lookup"><span data-stu-id="38679-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="38679-128">Entītijas dimensijām datus var izveidot manuāli vai izmantojot Microsoft Excel importēšanas vai pakalpojuma izsaukumus.</span><span class="sxs-lookup"><span data-stu-id="38679-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="38679-129">Izmantojiet šajā procedūrā norādītās darbības, lai izveidotu divu standarta nosaukumus: **Standarta inženieris** un **Vecākais sistēmu inženieris** , izmantojot entītijas dimensiju, kas pamatota sadaļā **Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="38679-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="38679-130">Ja dati, ko vēlaties izveidot, ir neliela izmēra, kā redzams šajā piemērā, varat izmantot standarta veidlapu.</span><span class="sxs-lookup"><span data-stu-id="38679-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="38679-131">Atlasiet **Detalizēta atrašana** , atlasiet entitīju **Standarta nosaukums** un pēc tam atlasiet **Rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="38679-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="38679-132">Tiks rādītas visas **Standarta nosaukums** entītijas rindas.</span><span class="sxs-lookup"><span data-stu-id="38679-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="38679-133">Atlasiet **Jauns** un laukā **Nosaukums** ievadiet "Sistēmu inženieris", un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="38679-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="38679-134">Aizvērt veidlapu.</span><span class="sxs-lookup"><span data-stu-id="38679-134">Close the form.</span></span> 
4. <span data-ttu-id="38679-135">Atkārtojiet 1.–3. darbību, lai izveidotu vēl vienu standarta nosaukumu “Vecākais sistēmas inženieris”.</span><span class="sxs-lookup"><span data-stu-id="38679-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="38679-136">Pievienojiet visas prasītās entītijas un ar tām saistītos komponentus cenas noteikšanas risinājumam.</span><span class="sxs-lookup"><span data-stu-id="38679-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="38679-137">Cenas risinājumam ir jāpievieno tālāk norādītās entītijas.</span><span class="sxs-lookup"><span data-stu-id="38679-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="38679-138">Izmantojiet šajā procedūrā norādītās darbības, lai veiktu dažas svarīgas shēmas izmaiņas cenas noteikšanas risinājumā un lai entītijas apzinātos jaunās cenu noteikšanas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="38679-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="38679-139">Atlasiet **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="38679-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="38679-140">Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Pievienot esošo** > **Entītijas**.</span><span class="sxs-lookup"><span data-stu-id="38679-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="38679-141">Dialoglodziņā **Risinājumu sastāvdaļas** atlasiet vienu no šīm entītijām:</span><span class="sxs-lookup"><span data-stu-id="38679-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="38679-142">Faktiski</span><span class="sxs-lookup"><span data-stu-id="38679-142">Actual</span></span>
  - <span data-ttu-id="38679-143">Rezervējams resurss</span><span class="sxs-lookup"><span data-stu-id="38679-143">Bookable Resource</span></span>
  - <span data-ttu-id="38679-144">Novērtējuma rinda</span><span class="sxs-lookup"><span data-stu-id="38679-144">Estimate Line</span></span>
  - <span data-ttu-id="38679-145">Rēķina rindas informācija</span><span class="sxs-lookup"><span data-stu-id="38679-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="38679-146">Žurnāla rinda</span><span class="sxs-lookup"><span data-stu-id="38679-146">Journal Line</span></span>
  - <span data-ttu-id="38679-147">Projekta līguma rindas informācija</span><span class="sxs-lookup"><span data-stu-id="38679-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="38679-148">Projekta grupas dalībnieks</span><span class="sxs-lookup"><span data-stu-id="38679-148">Project Team Member</span></span>
  - <span data-ttu-id="38679-149">Piedāvājuma rindas informācija</span><span class="sxs-lookup"><span data-stu-id="38679-149">Quote Line Detail</span></span>
  - <span data-ttu-id="38679-150">Lomas cenas uzcenojums</span><span class="sxs-lookup"><span data-stu-id="38679-150">Role Price Markup</span></span>
  - <span data-ttu-id="38679-151">Lomas cena</span><span class="sxs-lookup"><span data-stu-id="38679-151">Role Price</span></span> 
  - <span data-ttu-id="38679-152">Laika ieraksts</span><span class="sxs-lookup"><span data-stu-id="38679-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="38679-153">Pārliecinieties, vai visām atlasītajām entītijām ir atlasītas visas formas un skati.</span><span class="sxs-lookup"><span data-stu-id="38679-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="38679-154">Kad tiek piedāvāts iekļaut iepriekš atlasīto entītiju atkarīgās entītijas, atlasiet **Nē**.</span><span class="sxs-lookup"><span data-stu-id="38679-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

