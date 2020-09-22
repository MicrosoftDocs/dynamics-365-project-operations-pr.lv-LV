---
title: Pielāgotu lauku un entītiju izveide
description: Šajā tēmā ir paskaidrots, kā izveidot opciju kopas un entītijas jūsu risinājumā Power Apps platformā.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753551"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="c19a1-103">Pielāgotu lauku un entītiju izveide</span><span class="sxs-lookup"><span data-stu-id="c19a1-103">Create custom fields and entities</span></span> 

<span data-ttu-id="c19a1-104">Veiciet tālāk norādītās darbības jebkurā laikā, kad vēlaties izveidot pielāgotu opciju kopu vai entītiju platformā Power Apps.</span><span class="sxs-lookup"><span data-stu-id="c19a1-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="c19a1-105">Šajā tēmā aprakstītās procedūras ir jāizpilda, izmantojot Project Service Automation (PSA) tīmekļa saskarni.</span><span class="sxs-lookup"><span data-stu-id="c19a1-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c19a1-106">Iesakām veikt visas pielāgotās cenu noteikšanas dimensijas izmaiņas katrā atsevišķā risinājumā.</span><span class="sxs-lookup"><span data-stu-id="c19a1-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="c19a1-107">Šī svarīgā paraugprakse nodrošina elastību nākotnē, lai atjauninātu vai noņemtu nepieciešamās izmaiņas; tā palīdzēs ar jūsu darba atkārtotu izmantošanu un vienkāršos šo izmaiņu saglabāšanu citā gadījumā.</span><span class="sxs-lookup"><span data-stu-id="c19a1-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c19a1-108">Pēc visu nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldīts risinājums** un importējiet to citās instancēs, lai izmantotu cenas noteikšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="c19a1-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="c19a1-109">Pielāgota risinājuma izveide cenu noteikšanas dimensijām</span><span class="sxs-lookup"><span data-stu-id="c19a1-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="c19a1-110">PSA platformā noklikšķiniet uz **Iestatījumi** > **Risinājumi**un pēc tam uz **Jauns**, lai izveidotu jaunu risinājumu.</span><span class="sxs-lookup"><span data-stu-id="c19a1-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="c19a1-111">Nosauciet risinājumu **\<Organizācijas nosaukumu > Cenas noteikšanas dimensijas**, ievadiet visu nepieciešamo informāciju un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Pielāgota risinājuma izveide cenu noteikšanas dimensijām](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="c19a1-113">Pielāgotu lauku un opciju kopu izveide izmaksu dimensijas risinājumā</span><span class="sxs-lookup"><span data-stu-id="c19a1-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="c19a1-114">Cenas noteikšanas dimensija var būt opciju kopa vai entītija.</span><span class="sxs-lookup"><span data-stu-id="c19a1-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="c19a1-115">Abi ir jāizveido cenas noteikšanas risinājumā.</span><span class="sxs-lookup"><span data-stu-id="c19a1-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="c19a1-116">Šīs procedūras darbībās ir paskaidrots, kā izveidot entītiju pamatotas dimensijas un opciju kopas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="c19a1-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="c19a1-117">Entītiju pamatotas dimensijas</span><span class="sxs-lookup"><span data-stu-id="c19a1-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="c19a1-118">Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<Organizācijas nosaukums > Cenas noteikšanas dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="c19a1-119">Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet vienumu **Entītijas**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="c19a1-120">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu entītiju ar nosaukumu **Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="c19a1-121">Ievadiet pārējo pieprasīto informāciju un pēc tam pieskarieties vienumam **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standarta nosaukuma entītijas definīcija](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="c19a1-123">Opciju kopas dimensijas</span><span class="sxs-lookup"><span data-stu-id="c19a1-123">Option set-based dimensions</span></span> 
<span data-ttu-id="c19a1-124">Var izveidot divas opciju kopas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="c19a1-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="c19a1-125">Izmantojiet sadaļu **Resursa darba vieta**, lai izsekotu cenai opcijās **Mājas** un **Darbā**, kā arī lietotu **Resursa darba stundas** ar vērtībām **Regulārs** un **Virsstundas**, lai pievienotu atzīmi, kad darbs ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="c19a1-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="c19a1-126">Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi**un pēc tam veiciet dubultklikšķi uz **\<Organizācijas nosaukums > Cenas noteikšanas dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c19a1-127">Sadaļas Risinājumu pārlūks kreisajā navigācijas rūtī atlasiet vienumu **Opciju kopas**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="c19a1-128">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu opciju kopu, ievadiet atlikušo nepieciešamo informāciju un pēc tam t uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="c19a1-129">Opciju kopa atkarībā no cenas, ko sauc par Resursu darba vietu</span><span class="sxs-lookup"><span data-stu-id="c19a1-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="c19a1-130">Opciju kopa atkarībā no cenas, ko sauc par Resursu darba stundām</span><span class="sxs-lookup"><span data-stu-id="c19a1-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="c19a1-131">Datu izveide entītijai atbilstošām dimensijām</span><span class="sxs-lookup"><span data-stu-id="c19a1-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="c19a1-132">Entītijas dimensijām datus var izveidot manuāli vai izmantojot Microsoft Excel importēšanas vai pakalpojuma izsaukumus.</span><span class="sxs-lookup"><span data-stu-id="c19a1-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="c19a1-133">Izmantojiet šajā procedūrā norādītās darbības, lai izveidotu divu standarta nosaukumus: **Standarta inženieris** un **Vecākais sistēmu inženieris**, izmantojot entītijas dimensiju, kas pamatota sadaļā **Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="c19a1-134">Ja dati, ko vēlaties izveidot, ir neliela izmēra, kā redzams šajā piemērā, varat izmantot standarta veidlapu.</span><span class="sxs-lookup"><span data-stu-id="c19a1-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="c19a1-135">Noklikšķiniet uz **Detalizētā atrašana**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="c19a1-136">Atlasiet entītiju **Standarta nosaukums** un pēc tam noklikšķiniet uz **Rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="c19a1-137">Tiks rādītas visas **Standarta nosaukums** entītijas rindas.</span><span class="sxs-lookup"><span data-stu-id="c19a1-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="c19a1-138">Noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-138">Click **New**.</span></span> <span data-ttu-id="c19a1-139">Laukā **Nosaukums** ievadiet “Sistēmas inženieris ” un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="c19a1-140">Aizveriet veidlapu.</span><span class="sxs-lookup"><span data-stu-id="c19a1-140">Close the form.</span></span> 
4. <span data-ttu-id="c19a1-141">Atkārtojiet 1.–3. darbību, lai izveidotu vēl vienu standarta nosaukumu “Vecākais sistēmas inženieris”.</span><span class="sxs-lookup"><span data-stu-id="c19a1-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="c19a1-142">Standarta nosaukuma entītijas datu paraugs</span><span class="sxs-lookup"><span data-stu-id="c19a1-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="c19a1-143">Pievienojiet visas prasītās PSA entītijas un ar tām saistītos komponentus cenas noteikšanas risinājumam.</span><span class="sxs-lookup"><span data-stu-id="c19a1-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="c19a1-144">Cenas risinājumam ir jāpievieno tālāk norādītās Project Service entītijas.</span><span class="sxs-lookup"><span data-stu-id="c19a1-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="c19a1-145">Izmantojiet šajā procedūrā norādītās darbības, lai veiktu dažas svarīgas shēmas izmaiņas cenas noteikšanas risinājumā un lai entītijas apzinātos jaunās cenu noteikšanas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="c19a1-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="c19a1-146">Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<Organizācijas nosaukums > Cenas noteikšanas dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c19a1-147">Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Pievienot esošo** > **Entītijas**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="c19a1-148">Dialoglodziņā **Risinājumu sastāvdaļas** atlasiet vienu no šīm entītijām:</span><span class="sxs-lookup"><span data-stu-id="c19a1-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="c19a1-149">Faktiski</span><span class="sxs-lookup"><span data-stu-id="c19a1-149">Actual</span></span>
- <span data-ttu-id="c19a1-150">Rezervējams resurss</span><span class="sxs-lookup"><span data-stu-id="c19a1-150">Bookable Resource</span></span>
- <span data-ttu-id="c19a1-151">Novērtējuma rinda</span><span class="sxs-lookup"><span data-stu-id="c19a1-151">Estimate Line</span></span>
- <span data-ttu-id="c19a1-152">Rēķina rindas informācija</span><span class="sxs-lookup"><span data-stu-id="c19a1-152">Invoice Line Detail</span></span>
- <span data-ttu-id="c19a1-153">Žurnāla rinda</span><span class="sxs-lookup"><span data-stu-id="c19a1-153">Journal Line</span></span>
- <span data-ttu-id="c19a1-154">Projekta līguma rindas informācija</span><span class="sxs-lookup"><span data-stu-id="c19a1-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="c19a1-155">Projekta grupas dalībnieks</span><span class="sxs-lookup"><span data-stu-id="c19a1-155">Project Team Member</span></span>
- <span data-ttu-id="c19a1-156">Piedāvājuma rindas informācija</span><span class="sxs-lookup"><span data-stu-id="c19a1-156">Quote Line Detail</span></span>
- <span data-ttu-id="c19a1-157">Lomas cenas uzcenojums</span><span class="sxs-lookup"><span data-stu-id="c19a1-157">Role Price Markup</span></span>
- <span data-ttu-id="c19a1-158">Lomas cena</span><span class="sxs-lookup"><span data-stu-id="c19a1-158">Role Price</span></span> 
- <span data-ttu-id="c19a1-159">Laika ieraksts</span><span class="sxs-lookup"><span data-stu-id="c19a1-159">Time Entry</span></span> 

> ![Esošu entītiju pievienošana cenu dimensiju risinājumam](media/Existing-entities-to-PD-solution.png)

> ![Atlasiet risinājuma komponentus](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="c19a1-162">Pārliecinieties, vai visām atlasītajām entītijām ir atlasītas visas formas un skati.</span><span class="sxs-lookup"><span data-stu-id="c19a1-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="c19a1-163">Kad tiek piedāvāts iekļaut iepriekš atlasīto entītiju atkarīgās entītijas, noklikšķiniet uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="c19a1-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Neiekļaut nepieciešamos komponentus.](media/Do-not-include-required.png)


