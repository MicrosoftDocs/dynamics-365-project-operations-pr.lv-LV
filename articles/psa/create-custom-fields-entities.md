---
title: Pielāgotu lauku un entītiju izveide
description: Šajā tēmā ir paskaidrots, kā izveidot opciju kopas un entītijas jūsu risinājumā Power Apps platformā.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080513"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="a6091-103">Pielāgotu lauku un entītiju izveide</span><span class="sxs-lookup"><span data-stu-id="a6091-103">Create custom fields and entities</span></span> 

<span data-ttu-id="a6091-104">Veiciet tālāk norādītās darbības jebkurā laikā, kad vēlaties izveidot pielāgotu opciju kopu vai entītiju platformā Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a6091-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="a6091-105">Šajā tēmā aprakstītās procedūras ir jāizpilda, izmantojot Project Service Automation (PSA) tīmekļa saskarni.</span><span class="sxs-lookup"><span data-stu-id="a6091-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6091-106">Iesakām veikt visas pielāgotās cenu noteikšanas dimensijas izmaiņas katrā atsevišķā risinājumā.</span><span class="sxs-lookup"><span data-stu-id="a6091-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="a6091-107">Šī svarīgā paraugprakse nodrošina elastību nākotnē, lai atjauninātu vai noņemtu nepieciešamās izmaiņas; tā palīdzēs ar jūsu darba atkārtotu izmantošanu un vienkāršos šo izmaiņu saglabāšanu citā gadījumā.</span><span class="sxs-lookup"><span data-stu-id="a6091-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="a6091-108">Pēc visu nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldīts risinājums** un importējiet to citās instancēs, lai izmantotu cenas noteikšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="a6091-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="a6091-109">Pielāgotu lauku un opciju kopu izveide izmaksu dimensijas risinājumā</span><span class="sxs-lookup"><span data-stu-id="a6091-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="a6091-110">Cenas noteikšanas dimensija var būt opciju kopa vai entītija.</span><span class="sxs-lookup"><span data-stu-id="a6091-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="a6091-111">Abi ir jāizveido cenas noteikšanas risinājumā.</span><span class="sxs-lookup"><span data-stu-id="a6091-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="a6091-112">Šīs procedūras darbībās ir paskaidrots, kā izveidot entītiju pamatotas dimensijas un opciju kopas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="a6091-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="a6091-113">Entītiju pamatotas dimensijas</span><span class="sxs-lookup"><span data-stu-id="a6091-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="a6091-114">Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="a6091-114">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="a6091-115">Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet vienumu **Entītijas**.</span><span class="sxs-lookup"><span data-stu-id="a6091-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="a6091-116">Noklikšķiniet uz **Jauns** , lai izveidotu jaunu entītiju ar nosaukumu **Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="a6091-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="a6091-117">Ievadiet pārējo pieprasīto informāciju un pēc tam pieskarieties vienumam **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a6091-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standarta nosaukuma entītijas definīcija](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="a6091-119">Opciju kopas dimensijas</span><span class="sxs-lookup"><span data-stu-id="a6091-119">Option set-based dimensions</span></span> 
<span data-ttu-id="a6091-120">Var izveidot divas opciju kopas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="a6091-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="a6091-121">Izmantojiet sadaļu **Resursa darba vieta** , lai izsekotu cenai opcijās **Mājas** un **Darbā** , kā arī lietotu **Resursa darba stundas** ar vērtībām **Regulārs** un **Virsstundas** , lai pievienotu atzīmi, kad darbs ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="a6091-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="a6091-122">Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="a6091-122">In PSA, click **Settings** > **Solutions** , and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="a6091-123">Sadaļas Risinājumu pārlūks kreisajā navigācijas rūtī atlasiet vienumu **Opciju kopas**.</span><span class="sxs-lookup"><span data-stu-id="a6091-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="a6091-124">Noklikšķiniet uz **Jauns** , lai izveidotu jaunu opciju kopu, ievadiet atlikušo nepieciešamo informāciju un pēc tam t uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a6091-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="a6091-125">Opciju kopa atkarībā no cenas, ko sauc par Resursu darba vietu</span><span class="sxs-lookup"><span data-stu-id="a6091-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="a6091-126">Opciju kopa atkarībā no cenas, ko sauc par Resursu darba stundām</span><span class="sxs-lookup"><span data-stu-id="a6091-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="a6091-127">Datu izveide entītijai atbilstošām dimensijām</span><span class="sxs-lookup"><span data-stu-id="a6091-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="a6091-128">Entītijas dimensijām datus var izveidot manuāli vai izmantojot Microsoft Excel importēšanas vai pakalpojuma izsaukumus.</span><span class="sxs-lookup"><span data-stu-id="a6091-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="a6091-129">Izmantojiet šajā procedūrā norādītās darbības, lai izveidotu divu standarta nosaukumus: **Standarta inženieris** un **Vecākais sistēmu inženieris** , izmantojot entītijas dimensiju, kas pamatota sadaļā **Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="a6091-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="a6091-130">Ja dati, ko vēlaties izveidot, ir neliela izmēra, kā redzams šajā piemērā, varat izmantot standarta veidlapu.</span><span class="sxs-lookup"><span data-stu-id="a6091-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="a6091-131">Noklikšķiniet uz **Detalizētā atrašana**.</span><span class="sxs-lookup"><span data-stu-id="a6091-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="a6091-132">Atlasiet entītiju **Standarta nosaukums** un pēc tam noklikšķiniet uz **Rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="a6091-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="a6091-133">Tiks rādītas visas **Standarta nosaukums** entītijas rindas.</span><span class="sxs-lookup"><span data-stu-id="a6091-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="a6091-134">Noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a6091-134">Click **New**.</span></span> <span data-ttu-id="a6091-135">Laukā **Nosaukums** ievadiet “Sistēmas inženieris ” un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a6091-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="a6091-136">Aizveriet veidlapu.</span><span class="sxs-lookup"><span data-stu-id="a6091-136">Close the form.</span></span> 
4. <span data-ttu-id="a6091-137">Atkārtojiet 1.–3. darbību, lai izveidotu vēl vienu standarta nosaukumu “Vecākais sistēmas inženieris”.</span><span class="sxs-lookup"><span data-stu-id="a6091-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="a6091-138">Standarta nosaukuma entītijas datu paraugs</span><span class="sxs-lookup"><span data-stu-id="a6091-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


