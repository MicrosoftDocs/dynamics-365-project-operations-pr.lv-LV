---
title: Resursa piešķiršana uzdevumam
description: Šajā tēmā ir sniegta informācija par to, kā piešķirt resursus uzdevumiem.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080633"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="25c9b-103">Resursa piešķiršana uzdevumam</span><span class="sxs-lookup"><span data-stu-id="25c9b-103">Assign a resource to a task</span></span>

<span data-ttu-id="25c9b-104">Ir divi veidi, kā programmā Project Service resursu piešķirt uzdevumam risinājumā Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="25c9b-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="25c9b-105">Rezervējiet resursu kā darba grupas dalībnieku un pēc tam to piešķiriet uzdevumam</span><span class="sxs-lookup"><span data-stu-id="25c9b-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="25c9b-106">Varat pievienot resursu projekta darba grupai un pēc tam piešķirt uzdevumus resursam projekta grafikā.</span><span class="sxs-lookup"><span data-stu-id="25c9b-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="25c9b-107">Cilnē **Darba grupas dalībnieks** pievienojiet jaunu darba grupas dalībnieku, atlasot vienumu **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="25c9b-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="25c9b-108">Tiek atvērts panelis **Darba grupas dalībnieku ātrā izveide** , kur varat atlasīt rezervējamā resursa vārdu un iestatīt lomu.</span><span class="sxs-lookup"><span data-stu-id="25c9b-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="25c9b-109">Atlasiet kādu no šīm piešķiršanas metodēm resursa rezervēšanai:</span><span class="sxs-lookup"><span data-stu-id="25c9b-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="25c9b-110">**Pilna noslodze** : izmantojot šo metodi, tiek rezervēta resursa pilna noslodze norādītajā laika posmā (no sākuma līdz beigu datumam).</span><span class="sxs-lookup"><span data-stu-id="25c9b-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="25c9b-111">**Noslodzes procentuāla vērtība** : izmantojot šo metodi, tiek rezervēta resursa noslodzes procentuālā vertība norādītajā laika posmā (no sākuma līdz beigu datumam).</span><span class="sxs-lookup"><span data-stu-id="25c9b-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="25c9b-112">Vienums **Sadalīt vienmērīgi pa stundām** : rezervē resursu noteiktu skaitu stundu, vienmērīgi katru sadalot dienā rezervēto laiku norādītajā laika periodā.</span><span class="sxs-lookup"><span data-stu-id="25c9b-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="25c9b-113">**Pa stundām — sākotnējā slodze** : rezervē resursu noteiktu skaitu stundu, sadalot sākotnējās slodzes stundas dienā norādītajā laika periodā.</span><span class="sxs-lookup"><span data-stu-id="25c9b-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="25c9b-114">**Nav** pievieno resursu darba grupai, bet netiek izveidotas rezervācijas, kas izmanto resursa noslodzi.</span><span class="sxs-lookup"><span data-stu-id="25c9b-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="25c9b-115">Uzdevuma režģa **Plānot** atlasiet ikonu **Resurss** resursa šūnā un pēc tam sadaļā **Darba grupas dalībnieki** atlasiet darba grupas dalībnieku, ko tikko pievienojāt.</span><span class="sxs-lookup"><span data-stu-id="25c9b-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="25c9b-116">Ņemiet vērā, ka resursam gan cilnē **Darba grupas dalībnieks** , gan cilnē **Saskaņošana** tiek rādītas rezervētās stundas un piešķirtās stundas.</span><span class="sxs-lookup"><span data-stu-id="25c9b-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="25c9b-117">Stundu skaitam ir jābūt vienādam, tomēr tā var nebūt, jo rezervācijas un piešķīrumi nav cieši saistīti.</span><span class="sxs-lookup"><span data-stu-id="25c9b-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="25c9b-118">Cilnē **Saskaņošana** tiek sniegta informācija, ja šie rādītāji atšķiras, piemēram, ja piešķirat resursam vairāk stundu, nekā esat tam rezervējis.</span><span class="sxs-lookup"><span data-stu-id="25c9b-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="25c9b-119">Pēc tam varat veikt korekcijas šajā informācija, paplašinot resursa rezervācijas vai mainot piešķīrumu.</span><span class="sxs-lookup"><span data-stu-id="25c9b-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="25c9b-120">Vispārēja darba grupas dalībnieka izveide, izmantojot uzdevumu piešķiri</span><span class="sxs-lookup"><span data-stu-id="25c9b-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="25c9b-121">Veidojot vispārēju darba grupas dalībnieku, piešķirot uzdevumu, izveidojat vietturi vai vispārēju resursu, kas raksturo nosauktā resursa īpašības, kuras jums nepieciešamas darbam ar uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="25c9b-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="25c9b-122">Pēc tam jūs ģenerējat prasību (vai iesniedzat pieprasījumu, izmantojot prasību), kas tiek izmantota nosauktā resursa meklēšanai un rezervēšanai.</span><span class="sxs-lookup"><span data-stu-id="25c9b-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="25c9b-123">Uzdevuma režģī **Plānot** resursa šūnā atlasiet ikonu **Resurss**.</span><span class="sxs-lookup"><span data-stu-id="25c9b-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="25c9b-124">Ierakstiet nosaukumu, ko lietot kā viettura resursa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="25c9b-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="25c9b-125">Piemēram, programmas vadītājs</span><span class="sxs-lookup"><span data-stu-id="25c9b-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="25c9b-126">Atlasiet vienumu **Izveidot** un pēc tam laukā **Projekta darba grupas dalībnieka ātrā izveide** iestatiet lomu vispārējam resursam.</span><span class="sxs-lookup"><span data-stu-id="25c9b-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="25c9b-127">Varat turpināt piešķirt uzdevumus šim viettura resursam, atlasot vienumu **Resursa atlase** uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="25c9b-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="25c9b-128">Tie ir uzskaitīti sadaļā **Darba grupas dalībnieki**.</span><span class="sxs-lookup"><span data-stu-id="25c9b-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="25c9b-129">Kad esat pabeidzis vispārējā resursa piešķiršanu, atlasiet vispārējo resursu cilnē **Darba grupa** un atlasiet **Izveidot prasību** , lai izveidotu resursa prasību vispārējam resursam.</span><span class="sxs-lookup"><span data-stu-id="25c9b-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="25c9b-130">Vispārejam resursam atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="25c9b-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="25c9b-131">Pēc tam varat izmantot plānošanas paneli, lai atrastu un rezervētu reālu resursu.</span><span class="sxs-lookup"><span data-stu-id="25c9b-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="25c9b-132">Jūs varat arī iesniegt, ka prasība ir jāizpilda resursu pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="25c9b-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="25c9b-133">Kad vispārējais resurss ir aizpildīts ar nosauktu resursu, vispārējais resurss tiek noņemts no darba grupas un vispārējam resursam piešķirtie uzdevumi tiek piešķirti nosauktajam resursu, kas izpildīja vispārējā resursa prasības.</span><span class="sxs-lookup"><span data-stu-id="25c9b-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="25c9b-134">Nosaukta resursa piešķiršana no visu rezervējamo resursu saraksta</span><span class="sxs-lookup"><span data-stu-id="25c9b-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="25c9b-135">Varat izmantot meklēšanas lodziņu **Resursu atlasītājs** , lai meklētu visus rezervējamos resursus un piešķirtu tos uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="25c9b-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="25c9b-136">Šādā veidā piešķirtie resursi tiek pievienoti darba grupai bez jebkādām rezervācijām.</span><span class="sxs-lookup"><span data-stu-id="25c9b-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="25c9b-137">Tas ir līdzīgi kā pievienot darba grupas dalībnieku un atlasot Nav kā piešķiršanas metodi.</span><span class="sxs-lookup"><span data-stu-id="25c9b-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="25c9b-138">Šis resurss cilnē **Darba grupa** un cilnē **Saskaņošana** tiek rādīti kā resursi, kuriem ir tikai piešķīrumi un rezervāciju trūkums.</span><span class="sxs-lookup"><span data-stu-id="25c9b-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="25c9b-139">Ja vēlaties izmantot to pieejamību, rezervējiet tos.</span><span class="sxs-lookup"><span data-stu-id="25c9b-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="25c9b-140">Uzdevuma režģī **Plānot** resursa šūnā atlasiet ikonu **Resurss**.</span><span class="sxs-lookup"><span data-stu-id="25c9b-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="25c9b-141">Sāciet rakstīt nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="25c9b-141">Start typing a name.</span></span> <span data-ttu-id="25c9b-142">Sadaļā **Resursu atlasītājs** pie **Citi resursi** tiek rādīti nosaukuma meklēšanas rezultāti.</span><span class="sxs-lookup"><span data-stu-id="25c9b-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="25c9b-143">Sarakstā atlasiet resursu, kuru vēlaties piešķirt uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="25c9b-143">Select the resource that you want to assign to the task.</span></span>

