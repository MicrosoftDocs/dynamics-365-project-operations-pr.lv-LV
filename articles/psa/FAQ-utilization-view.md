---
title: Skatīt rēķinā iekļaujamo resursu lietojumu
description: Šajā tēmā ir sniegta informācija par resursu lietojuma skatu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a1d1db532c65b2a13f3cf4e1281a5987490b96df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122172"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="9a84e-103">Skatīt rēķinā iekļaujamo resursu lietojumu</span><span class="sxs-lookup"><span data-stu-id="9a84e-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="9a84e-104">**Lietojuma skats** lapā **Project Service resursu lietojums** rāda katram rezervējamam resursam piemērojamu lietojumu.</span><span class="sxs-lookup"><span data-stu-id="9a84e-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="9a84e-105">Skata pamatā ir plānošanas panelis, tādēļ tajā ir atrodamas daudzas tās pašas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="9a84e-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Lietojuma skata ekrānuzņēmums](media/FAQ-utilization-1.png)
 

<span data-ttu-id="9a84e-107">Rēķinā iekļaujamā lietojuma aprēķinu veic šādi:</span><span class="sxs-lookup"><span data-stu-id="9a84e-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="9a84e-108">Rēķinā iekļaujamais lietojums = (faktiskais rēķinā iekļaujamo stundu skaits)/resursa noslodze.</span><span class="sxs-lookup"><span data-stu-id="9a84e-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="9a84e-109">Šūnās ir norādīts aprēķinātais rēķinā iekļaujamais lietojums atlasītajam periodam (dienas, nedēļas vai mēneši).</span><span class="sxs-lookup"><span data-stu-id="9a84e-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="9a84e-110">Katras šūnas krāsa norāda resursa rēķinā iekļaujamo lietojumu salīdzinājumā ar to mērķa rēķinā iekļaujamo lietojumu.</span><span class="sxs-lookup"><span data-stu-id="9a84e-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="9a84e-111">Mērķa lietojumu var iestatīt resursa noklusējuma lomai vai atsevišķam resursam.</span><span class="sxs-lookup"><span data-stu-id="9a84e-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="9a84e-112">Aprēķinā vispirms tiek ņemta vērā atsevišķa resursa mērķa vērtība un pēc tam resursa noklusējuma loma.</span><span class="sxs-lookup"><span data-stu-id="9a84e-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="9a84e-113">Mērķa iestatīšana resursā</span><span class="sxs-lookup"><span data-stu-id="9a84e-113">Set target on a resource</span></span>

1. <span data-ttu-id="9a84e-114">Atveriet sadaļu **Resursi** \> **Resursi.**</span><span class="sxs-lookup"><span data-stu-id="9a84e-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="9a84e-115">Atlasiet resursu, lai atvērtu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9a84e-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="9a84e-116">Cilnē **Project Service** var iestatīt resursa mērķa izmantojumu.</span><span class="sxs-lookup"><span data-stu-id="9a84e-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Ekrānuzņēmums, kurā redzama cilnes Project Service izmantošana, lai iestatītu mērķa lietojumu](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="9a84e-118">Mērķa lietojuma iestatīšana lomai</span><span class="sxs-lookup"><span data-stu-id="9a84e-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="9a84e-119">Dodieties uz **Resursi** \> **Resursu lomas**.</span><span class="sxs-lookup"><span data-stu-id="9a84e-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="9a84e-120">Atlasiet lomu un pēc tam atveriet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9a84e-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="9a84e-121">Iestatiet lomai mērķa lietojumu.</span><span class="sxs-lookup"><span data-stu-id="9a84e-121">Set the target utilization for the role.</span></span>

> ![Ekrānuzņēmums, kurā redzama resursu lomu izmantošana, lai iestatītu mērķa lietojumu](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="9a84e-123">Rēķinā iekļaujamo resursu lietojumu aprēķins</span><span class="sxs-lookup"><span data-stu-id="9a84e-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="9a84e-124">Lai aprēķinātu resursa rēķinā iekļaujamo lietojumu, ir nepieciešams veikt dažas priekšdarbības.</span><span class="sxs-lookup"><span data-stu-id="9a84e-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="9a84e-125">Noklusējuma lomas iestatīšana atsevišķam resursam</span><span class="sxs-lookup"><span data-stu-id="9a84e-125">Set default role for individual resource</span></span>

<span data-ttu-id="9a84e-126">Pirmkārt, mērķa lietojums ir jāiestata atsevišķam resursam vai resursu noklusējuma lomām.</span><span class="sxs-lookup"><span data-stu-id="9a84e-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="9a84e-127">Ja mērķa vērtībām tiek izmantotas resursu lomas, katram atsevišķam resursam jābūt noklusējuma lomai.</span><span class="sxs-lookup"><span data-stu-id="9a84e-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="9a84e-128">Lai to iestatītu, atveriet vienumu **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="9a84e-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="9a84e-129">Atlasiet resursu, atveriet ierakstu un pēc tam atlasiet cilni **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="9a84e-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="9a84e-130">Režģī **Resursu lomas** pārliecinieties, vai resursam ir viena loma un vai **Noklusējuma** iestatījums ir **Jā.**</span><span class="sxs-lookup"><span data-stu-id="9a84e-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="9a84e-131">Norēķinu tipa maiņa šai resursa lomai.</span><span class="sxs-lookup"><span data-stu-id="9a84e-131">Change billing type for resource role</span></span>

<span data-ttu-id="9a84e-132">Resursu lomu norēķinu tipam jābūt **Rēķinā iekļaujams**.</span><span class="sxs-lookup"><span data-stu-id="9a84e-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="9a84e-133">Dodieties uz **Resursi** \> **Resursu lomas**.</span><span class="sxs-lookup"><span data-stu-id="9a84e-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="9a84e-134">Noklikšķiniet uz lomas, lai atvērtu ierakstu, un pēc tam iestatiet norēķinu tipa noklusējuma vērtību **Rēķinā iekļaujams**.</span><span class="sxs-lookup"><span data-stu-id="9a84e-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="9a84e-135">Darba stundu iestatīšana resursu lomai</span><span class="sxs-lookup"><span data-stu-id="9a84e-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="9a84e-136">Resursam ir jābūt darba stundām noslodzes aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="9a84e-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="9a84e-137">Atveriet sadaļu **Resursi** \> **Resursi.**</span><span class="sxs-lookup"><span data-stu-id="9a84e-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="9a84e-138">Noklikšķiniet uz resursa, lai atvērtu ierakstu, un pēc tam noklikšķiniet uz **Rādīt darba stundas**.</span><span class="sxs-lookup"><span data-stu-id="9a84e-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="9a84e-139">Varat veikt resursu saraksta lielapjoma atjaunināšanu, lietojot **Darba stundu veidne** skatā **Resursu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="9a84e-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="9a84e-140">Rēķinā iekļaujamo faktisko stundu traucējummeklēšana</span><span class="sxs-lookup"><span data-stu-id="9a84e-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="9a84e-141">Faktiskā rēķinā iekļaujamo stundu skaita avots ir entītija **Faktiskās vērtības**.</span><span class="sxs-lookup"><span data-stu-id="9a84e-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="9a84e-142">Faktiskās vērtības, kurām norēķinu tips ir **Rēķinā iekļaujams**, tiek iekļautas aprēķinā, un tādēļ ir jābūt projektiem, kuros faktiskās vērtības tiek iekļautas rēķinā.</span><span class="sxs-lookup"><span data-stu-id="9a84e-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="9a84e-143">Ja rēķinā iekļaujamais lietojums nav redzams, var pārbaudīt šādus aspektus:</span><span class="sxs-lookup"><span data-stu-id="9a84e-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="9a84e-144">Resursa noslodzei ir noteiktas darba stundas.</span><span class="sxs-lookup"><span data-stu-id="9a84e-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="9a84e-145">Resursam ir atsevišķi noteikts mērķa lietojums, vai tam ir piešķirta noklusējuma loma.</span><span class="sxs-lookup"><span data-stu-id="9a84e-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="9a84e-146">Lomai ir noteikts mērķa lietojums.</span><span class="sxs-lookup"><span data-stu-id="9a84e-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="9a84e-147">Faktiskajām vērtībām norēķinu tips ir **Rēķinā iekļaujams** plānotajā lietojuma aprēķināšanas periodā.</span><span class="sxs-lookup"><span data-stu-id="9a84e-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="9a84e-148">Tālāk skatiet dažus aspektus, kuri jāpārbauda, ja tiek rādītas faktiskās vērtības, kuru norēķinu tips nav Rēķinā iekļaujams:</span><span class="sxs-lookup"><span data-stu-id="9a84e-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="9a84e-149">Lomai, kas izmantota faktiskajai vērtība, noklusējuma norēķinu tips nav Rēķinā iekļaujams.</span><span class="sxs-lookup"><span data-stu-id="9a84e-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="9a84e-150">Projekta pamatojumam izmantotās projekta līguma rindas lomai ir atlasīts iestatījums Nav iekļaujams rēķinā.</span><span class="sxs-lookup"><span data-stu-id="9a84e-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="9a84e-151">Projektam nav saistītās līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="9a84e-151">The project does not have an associated contract line.</span></span>

