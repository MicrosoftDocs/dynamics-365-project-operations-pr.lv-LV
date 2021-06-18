---
title: Pielāgotu lauku un entītiju kā cenu noteikšanas kategoriju izveide
description: Šajā tēmā sniegta informācija par to, kā izveidot pielāgotas opciju kopas vai entitījas.
author: rumant
ms.date: 11/18/2020
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
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000535"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="d008d-103">Pielāgotu lauku un entītiju kā cenu noteikšanas kategoriju izveide</span><span class="sxs-lookup"><span data-stu-id="d008d-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="d008d-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="d008d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d008d-105">Veiciet tālāk norādītās darbības, kad vēlaties izveidot pielāgotu opciju kopu vai entītiju, lai to izmantotu kā cenu noteikšanas dimensiju.</span><span class="sxs-lookup"><span data-stu-id="d008d-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="d008d-106">Papildinformāciju skatiet sadaļā [Cenu noteikšanas dimensiju pārskats](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d008d-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="d008d-107">Iesakām veikt visas pielāgotās cenu noteikšanas dimensijas izmaiņas katrā atsevišķā risinājumā.</span><span class="sxs-lookup"><span data-stu-id="d008d-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="d008d-108">Šī svarīgā paraugprakse nodrošina elastību nākotnē, lai atjauninātu vai noņemtu nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="d008d-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="d008d-109">Tā arī palīdzēs atkārtoti izmantot darbu un vienkāršos šo izmaiņu saglabāšanu citā instancē. Pēc visu nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldītu risinājumu** un importējiet to citās instancēs, lai atkārtoti izmantotu cenu noteikšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="d008d-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="d008d-110">Pielāgotu lauku un opciju kopu izveide izmaksu dimensijas risinājumā</span><span class="sxs-lookup"><span data-stu-id="d008d-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="d008d-111">Cenas noteikšanas dimensija var būt opciju kopa vai entītija.</span><span class="sxs-lookup"><span data-stu-id="d008d-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="d008d-112">Abi ir jāizveido cenas noteikšanas risinājumā.</span><span class="sxs-lookup"><span data-stu-id="d008d-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="d008d-113">Šīs procedūras darbībās ir paskaidrots, kā izveidot entītiju pamatotas dimensijas un opciju kopas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="d008d-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="d008d-114">Entītiju pamatotas dimensijas</span><span class="sxs-lookup"><span data-stu-id="d008d-114">Entity-based dimensions</span></span>
<span data-ttu-id="d008d-115">Lai izveidotu entītiju dimensijas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d008d-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="d008d-116">Dodieties uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="d008d-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="d008d-117">Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Entītijas**.</span><span class="sxs-lookup"><span data-stu-id="d008d-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="d008d-118">Atlasiet **Jauns**, lai izveidotu jaunu entītiju ar nosaukumu **Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="d008d-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="d008d-119">Ievadiet pārējo pieprasīto informāciju un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d008d-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Standarta nosaukuma entītijas definīcija](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="d008d-121">Opciju kopas dimensijas</span><span class="sxs-lookup"><span data-stu-id="d008d-121">Option set-based dimensions</span></span> 
<span data-ttu-id="d008d-122">Var izveidot divas opciju kopas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="d008d-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="d008d-123">Izmantojiet opciju **Resursa darba atrašanās vieta**, lai izsekotu atrašanās vietu **Mājas** un **Uz vietas** darba cenu.</span><span class="sxs-lookup"><span data-stu-id="d008d-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="d008d-124">Izmantojiet **Resursa darba stundas** ar vērtībām **Regulāras** un **Virsstundas**, lai pēc darba pabeigšanas lietotu uzcenojumu.</span><span class="sxs-lookup"><span data-stu-id="d008d-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="d008d-125">Tālāk esošajā grafikā ir sniegts dimensijas **Resursa darba atrašanās vieta** skats.</span><span class="sxs-lookup"><span data-stu-id="d008d-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Opciju kopa atkarībā no cenas, ko sauc par Resursu darba vietu](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="d008d-127">Tālāk esošajā grafikā ir sniegts dimensijas **Resursa darba stundas** skats.</span><span class="sxs-lookup"><span data-stu-id="d008d-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Opciju kopa atkarībā no cenas, ko sauc par Resursu darba stundām](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="d008d-129">Dodieties uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="d008d-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d008d-130">Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Opciju kopas**.</span><span class="sxs-lookup"><span data-stu-id="d008d-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="d008d-131">Atlasiet **Jauns**, lai izveidotu jaunu opciju kopu, ievadiet atlikušo nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d008d-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="d008d-132">Datu izveide entītijai atbilstošām dimensijām</span><span class="sxs-lookup"><span data-stu-id="d008d-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="d008d-133">Entītijas dimensijām datus var izveidot manuāli vai izmantojot Microsoft Excel importēšanas vai pakalpojuma izsaukumus.</span><span class="sxs-lookup"><span data-stu-id="d008d-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="d008d-134">Izmantojiet šajā procedūrā norādītās darbības, lai izveidotu divu standarta nosaukumus: **Standarta inženieris** un **Vecākais sistēmu inženieris**, izmantojot entītijas dimensiju, kas pamatota sadaļā **Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="d008d-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="d008d-135">Ja dati, ko vēlaties izveidot, ir neliela izmēra, kā redzams šajā piemērā, varat izmantot standarta veidlapu.</span><span class="sxs-lookup"><span data-stu-id="d008d-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="d008d-136">Atlasiet **Detalizētā atrašana**.</span><span class="sxs-lookup"><span data-stu-id="d008d-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="d008d-137">Atlasiet entītiju **Standarta nosaukums** un pēc tam atlasiet **Rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="d008d-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="d008d-138">Tiks rādītas visas **Standarta nosaukums** entītijas rindas.</span><span class="sxs-lookup"><span data-stu-id="d008d-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="d008d-139">Atlasiet **Jauns** un laukā **Nosaukums** ievadiet "Sistēmu inženieris", un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d008d-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="d008d-140">Aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="d008d-140">Close the page.</span></span> 
5. <span data-ttu-id="d008d-141">Atkārtojiet 1.–3. darbību, lai izveidotu vēl vienu standarta nosaukumu “Vecākais sistēmas inženieris”.</span><span class="sxs-lookup"><span data-stu-id="d008d-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Standarta nosaukuma entītijas datu paraugs](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]