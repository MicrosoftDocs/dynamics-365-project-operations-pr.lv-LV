---
title: Pielāgotu risinājumu izveide cenu noteikšanas dimensijām
description: Šajā tēmā izskaidrots, kā izveidot pielāgotu risinājumu, veidojot pielāgotas cenu noteikšanas dimensijas.
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
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080453"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="e8a83-103">Pielāgotu risinājumu izveide cenu noteikšanas dimensijām</span><span class="sxs-lookup"><span data-stu-id="e8a83-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8a83-104">Visām pielāgoto cenu noteikšanas dimensiju izmaiņām jābūt atsevišķā risinājumā.</span><span class="sxs-lookup"><span data-stu-id="e8a83-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="e8a83-105">Šī svarīgā paraugprakse nodrošina elastību nākotnē, lai atjauninātu vai noņemtu nepieciešamās izmaiņas; tā palīdzēs ar jūsu darba atkārtotu izmantošanu un vienkāršos šo izmaiņu saglabāšanu citā gadījumā.</span><span class="sxs-lookup"><span data-stu-id="e8a83-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="e8a83-106">Pēc nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldīts risinājums** un importējiet to citās instancēs, lai izmantotu cenu noteikšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="e8a83-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="e8a83-107">Izvēlieties **Iestatījumi** > **Risinājumi** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e8a83-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="e8a83-108">Nosauciet risinājumu **\<your organization name>cenu noteikšanas dimensijas** , ievadiet atlikušo nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e8a83-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Pielāgota risinājuma izveide cenu noteikšanas dimensijām](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="e8a83-110">Pievienojiet visas prasītās entītijas un ar tām saistītos komponentus cenu noteikšanas dimensijas risinājumam</span><span class="sxs-lookup"><span data-stu-id="e8a83-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="e8a83-111">Cenas risinājumam ir jāpievieno tālāk norādītās Project Service entītijas.</span><span class="sxs-lookup"><span data-stu-id="e8a83-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="e8a83-112">Izpildiet šajā procedūrā norādītās darbības, lai veiktu dažas svarīgas shēmas izmaiņas cenas noteikšanas risinājumā un lai entītijas apzinātos jaunās cenu noteikšanas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e8a83-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="e8a83-113">Atlasiet **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="e8a83-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="e8a83-114">Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Pievienot esošo** > **Entītijas**.</span><span class="sxs-lookup"><span data-stu-id="e8a83-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="e8a83-115">Dialoglodziņā **Risinājumu sastāvdaļas** atlasiet vienu no šīm entītijām:</span><span class="sxs-lookup"><span data-stu-id="e8a83-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="e8a83-116">Faktiski</span><span class="sxs-lookup"><span data-stu-id="e8a83-116">Actual</span></span>
- <span data-ttu-id="e8a83-117">Rezervējamais resurssss</span><span class="sxs-lookup"><span data-stu-id="e8a83-117">Bookable Resource</span></span>
- <span data-ttu-id="e8a83-118">Novērtēšanas rinda</span><span class="sxs-lookup"><span data-stu-id="e8a83-118">Estimate Line</span></span>
- <span data-ttu-id="e8a83-119">Projekta uzdevums</span><span class="sxs-lookup"><span data-stu-id="e8a83-119">Project Task</span></span>
- <span data-ttu-id="e8a83-120">Rēķina rindas informācija</span><span class="sxs-lookup"><span data-stu-id="e8a83-120">Invoice Line Detail</span></span>
- <span data-ttu-id="e8a83-121">Žurnāla rinda</span><span class="sxs-lookup"><span data-stu-id="e8a83-121">Journal Line</span></span>
- <span data-ttu-id="e8a83-122">Projekta līguma rindas informācija</span><span class="sxs-lookup"><span data-stu-id="e8a83-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="e8a83-123">Projekta grupas dalībnieks</span><span class="sxs-lookup"><span data-stu-id="e8a83-123">Project Team Member</span></span>
- <span data-ttu-id="e8a83-124">Piedāvājuma rindas informācija</span><span class="sxs-lookup"><span data-stu-id="e8a83-124">Quote Line Detail</span></span>
- <span data-ttu-id="e8a83-125">Lomas cenas uzcenojums</span><span class="sxs-lookup"><span data-stu-id="e8a83-125">Role Price Markup</span></span>
- <span data-ttu-id="e8a83-126">Lomas cena</span><span class="sxs-lookup"><span data-stu-id="e8a83-126">Role Price</span></span> 
- <span data-ttu-id="e8a83-127">Laika ieraksts</span><span class="sxs-lookup"><span data-stu-id="e8a83-127">Time Entry</span></span> 

> ![Esošu entītiju pievienošana cenu dimensiju risinājumam](media/Existing-entities-to-PD-solution.png)

> ![Atlasiet risinājuma komponentus](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="e8a83-130">Pārliecinieties, vai visām atlasītajām entītijām ir atlasītas visas formas un skati.</span><span class="sxs-lookup"><span data-stu-id="e8a83-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="e8a83-131">Kad atlasītajām entītijām tiek piedāvāts iekļaut atkarīgās entītijas, atlasiet **Nē**.</span><span class="sxs-lookup"><span data-stu-id="e8a83-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Neiekļaut nepieciešamos komponentus.](media/Do-not-include-required.png)


