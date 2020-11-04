---
title: Kā tīmekļa lietotnē piešķirt rezervējamu resursu uzdevumam
description: Pārskats par to, kā var piešķirt rezervējamus resursus.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 7b95eff52351904f97c62b3806f17b02db47860b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080632"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="21277-103">Kā tīmekļa programmā (Project Service v2.x) piešķirt rezervējamu resursu uzdevumam?</span><span class="sxs-lookup"><span data-stu-id="21277-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="21277-104">Ir divi veidi, kā programmā Project Service resursu piešķirt uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="21277-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="21277-105">Varat rezervēt resursu kā darba grupas dalībnieku un pēc tam to piešķirt uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="21277-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="21277-106">Vai arī varat izveidot vispārējo grupas dalībnieku, izmantojot lomu piešķiršanu uzdevumos, izveidot darba grupu un pēc tam izpildīt dublējuma prasības ar nosauktu resursu.</span><span class="sxs-lookup"><span data-stu-id="21277-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="21277-107">Ņemiet vērā: ja vēlaties piešķirt uzdevumam rezervējamu resursu, rezervējamam resursu darba grupas dalībniekam ir jābūt pietiekami daudz pieejamām rezervācijām.</span><span class="sxs-lookup"><span data-stu-id="21277-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="21277-108">Rezervācijas statusa saistību tipam ir jābūt Stingrs, bet statusam — Iesniegts.</span><span class="sxs-lookup"><span data-stu-id="21277-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="21277-109">Ja resursam nav pietiekami daudz rezervāciju, Project Service noņem piešķiri un parādīta šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="21277-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="21277-110">*Nevar piešķirt resursu uzdevumam — tālāk norādītajiem resursiem projektā nav pietiekami daudz rezervētu stundu*</span><span class="sxs-lookup"><span data-stu-id="21277-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="21277-111">Rezervējiet resursu kā darba grupas dalībnieku un pēc tam to piešķirt uzdevumam</span><span class="sxs-lookup"><span data-stu-id="21277-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="21277-112">Izmantojot šo metodi, jūs pievienojat resursu projekta darba grupai un pēc tam piešķirat uzdevumus resursam projekta grafikā.</span><span class="sxs-lookup"><span data-stu-id="21277-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="21277-113">Lūk, kā to paveikt:</span><span class="sxs-lookup"><span data-stu-id="21277-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="21277-114">Darba grupas dalībnieku režģī pievienojiet jaunu darba grupas dalībnieku, atlasot **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="21277-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="21277-115">Darba grupas dalībnieku ātrās izveides ekrānā atlasiet rezervējamā resursa vārdu un iestatiet lomu.</span><span class="sxs-lookup"><span data-stu-id="21277-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="21277-116">Atlasiet **sākuma** un **beigu** datumus.</span><span class="sxs-lookup"><span data-stu-id="21277-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="21277-117">![Ekrānuzņēmums: darba grupas dalībnieka pievienošana](media/FAQ-Resources-to-Tasks2-1.png "Ekrānuzņēmums: darba grupas dalībnieka pievienošana")</span><span class="sxs-lookup"><span data-stu-id="21277-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="21277-118">Atlasiet kādu no šīm sadales metodēm resursa rezervēšanai:</span><span class="sxs-lookup"><span data-stu-id="21277-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="21277-119">**Pilna noslodze** : izmantojot šo metodi, tiek rezervēta resursa pilna noslodze norādītajā laika posmā (no sākuma līdz beigu datumam).</span><span class="sxs-lookup"><span data-stu-id="21277-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="21277-120">**Noslodzes procentuāla vērtība** : izmantojot šo metodi, tiek rezervēta resursa noslodzes procentuālā vertība norādītajā laika posmā (no sākuma līdz beigu datumam).</span><span class="sxs-lookup"><span data-stu-id="21277-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="21277-121">**Sadalīt vienmērīgi pa stundām** : rezervē resursu noteiktu skaitu stundu, vienmērīgi katru sadalot dienā rezervēto laiku norādītajā laika periodā.</span><span class="sxs-lookup"><span data-stu-id="21277-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="21277-122">**Pa stundām — sākotnējā slodze** : rezervē resursu noteiktu skaitu stundu, sadalot sākotnējās slodzes stundas dienā norādītajā laika periodā.</span><span class="sxs-lookup"><span data-stu-id="21277-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="21277-123">Neatlasiet **Nav** , jo tā pievieno resursu darba grupai, bet netiek izveidotas rezervācijas, kas izmanto resursa noslodzi.</span><span class="sxs-lookup"><span data-stu-id="21277-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="21277-124">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="21277-124">Select **Save**.</span></span>

    <span data-ttu-id="21277-125">Ņemiet vērā, ka rezervācijas stundām ir jāpietiek, lai segtu ieguldīto laiku un datumu diapazonu uzdevumiem, kuriem piešķirat šo resursu.</span><span class="sxs-lookup"><span data-stu-id="21277-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="21277-126">Ja tās nav, nevarat piešķirt resursu uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="21277-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="21277-127">Uzdevuma darba sadalījuma struktūrā (WBS) noklikšķiniet uz resursu nolaižamajā šūnu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="21277-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="21277-128">Tad:</span><span class="sxs-lookup"><span data-stu-id="21277-128">Then:</span></span> 

    1. <span data-ttu-id="21277-129">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="21277-129">Select **Add**.</span></span>
    2. <span data-ttu-id="21277-130">Sadaļā **Resursi** atlasiet nolaižamo sarakstu un atlasiet iepriekš pievienoto darba grupas dalībnieku.</span><span class="sxs-lookup"><span data-stu-id="21277-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="21277-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="21277-131">Select **OK**.</span></span> <span data-ttu-id="21277-132">Grupas dalībnieks tagad ir piešķirts uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="21277-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="21277-133">![Ekrānuzņēmums: resursu pievienošana ar WBS](media/FAQ-Resources-to-Tasks2-2.png "Ekrānuzņēmums: resursu pievienošana ar WBS")</span><span class="sxs-lookup"><span data-stu-id="21277-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="21277-134">Darba grupas dalībnieku režģa sadaļā Piešķirtās stundas jūs redzēsit resursam piešķirto stundu apkopojumu.</span><span class="sxs-lookup"><span data-stu-id="21277-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="21277-135">Tas būs mazāks par vai vienāds ar resursam rezervēto stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="21277-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="21277-136">![Ekrānuzņēmums: resursam piešķirtās stundas](media/FAQ-Resources-to-Tasks2-3.png "Ekrānuzņēmums: resursam piešķirtās stundas")</span><span class="sxs-lookup"><span data-stu-id="21277-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="21277-137">Ja uzdevums, ko mēģināt piešķirt resursam, sākas pēc resursa rezervāciju beigu datuma, resurss vairs netiek rādīts nolaižamajā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="21277-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="21277-138">Ņemiet vērā, ka varat resursam piešķirt vairāk stundu nekā tā rezervētās stundas, ja resursam ir atlikusi nepiešķirta noslodze.</span><span class="sxs-lookup"><span data-stu-id="21277-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="21277-139">Šajā gadījumā resurss tiek tikai daļēji piešķirts rezervācijām.</span><span class="sxs-lookup"><span data-stu-id="21277-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="21277-140">Atlikušās nepiešķirtās uzdevuma stundas varat skatīt, darba sadalījuma struktūrai pievienojot kolonnu Stundas bez personāla.</span><span class="sxs-lookup"><span data-stu-id="21277-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="21277-141">Ja resursi tiek piešķirti to rezervētajām stundām (rezervētās stundas ir vienādas ar piešķirtajām stundām) un jūs mēģināsiet piešķirt tiem papildu uzdevumus, redzēsiet šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="21277-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="21277-142">*Nevar piešķirt resursu uzdevumam — tālāk norādītajiem resursiem projektā nav pietiekami daudz rezervētu stundu.*</span><span class="sxs-lookup"><span data-stu-id="21277-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="21277-143">Turklāt noklusējuma projektu vadītāju darba grupas dalībnieks, kas tiek pievienots darba grupai, kad izveidojat projektu, tiek pievienots bez rezervācijām un to nevar piešķirt nevienam uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="21277-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="21277-144">Tas netiks rādīts uzdevumu resursu nolaižamajā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="21277-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="21277-145">Ja vēlaties piešķirt šo resursu, jums ir nepieciešams noņemt to no darba grupas un pēc tam atkārtoti pievieno to ar sadalījuma metodi, izņemot Nav.</span><span class="sxs-lookup"><span data-stu-id="21277-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="21277-146">Resurss tiek pievienots darba grupai, kad projekts ir izveidots, tāpēc ka projektam pēc noklusējuma ir nepieciešams vismaz viens projekta apstiprinātājs.</span><span class="sxs-lookup"><span data-stu-id="21277-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="21277-147">Vispārējā darba grupas dalībnieka izveide, izmantojot lomu piešķiri uzdevumos</span><span class="sxs-lookup"><span data-stu-id="21277-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="21277-148">Šī metode nodrošina, ka resursiem uzdevumos ir pietiekami daudz rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="21277-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="21277-149">Vispirms izveidojiet vietturi vai vispārējo resursu, kas apraksta tā nosauktā resursa īpašības, kuram būtu vēlams strādāt pie uzdevumiem, izveidojot darba grupu pēc lomu piešķiršanas uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="21277-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="21277-150">Lūk, kā to paveikt:</span><span class="sxs-lookup"><span data-stu-id="21277-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="21277-151">Darba sadalījuma struktūrā atlasiet uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="21277-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="21277-152">Resursa šūnā atlasiet nolaižamā saraksta ikonu **Piešķirta loma**.</span><span class="sxs-lookup"><span data-stu-id="21277-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="21277-153">Atlasiet nolaižamo sarakstu **Loma** un atlasiet lomu vispārējam resursam.</span><span class="sxs-lookup"><span data-stu-id="21277-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="21277-154">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="21277-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="21277-155">![Ekrānuzņēmums: WBS izmantošana resursa piešķiršanai](media/FAQ-Resources-to-Tasks2-4.png "Ekrānuzņēmums: WBS izmantošana resursa piešķiršanai")</span><span class="sxs-lookup"><span data-stu-id="21277-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="21277-156">Kad WBS esat pabeidzis piešķirt lomas uzdevumiem, atlasiet **Izveidot darba grupu**.</span><span class="sxs-lookup"><span data-stu-id="21277-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="21277-157">Project Service izveido vispārējās darba grupas dalībnieku minimālo skaitu atbilstoši lomām, resursu organizācijas vienībām un projekta kalendāram, apkopojot uzdevumu piešķiri.</span><span class="sxs-lookup"><span data-stu-id="21277-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="21277-158">![Ekrānuzņēmums: projekta komandas ģenerēšana](media/FAQ-Resources-to-Tasks2-5.png "Ekrānuzņēmums: projekta komandas ģenerēšana")</span><span class="sxs-lookup"><span data-stu-id="21277-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="21277-159">Darba grupas dalībnieku režģī jūs redzēsiet resursus ar vispārējā resursa tipu un to lomas un pozīciju nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="21277-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="21277-160">Ja darba veikšanai vienai lomai ir nepieciešami divi resursi, līdzeklis Izveidot darba grupu izveido divus darba grupas dalībniekus un izmanto pozīcijas nosaukumu, lai tos atšķirtu.</span><span class="sxs-lookup"><span data-stu-id="21277-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="21277-161">![Ekrānuzņēmums: divu vispārējo resursu pievienošana](media/FAQ-Resources-to-Tasks2-6.png "Ekrānuzņēmums: divu vispārējo resursu pievienošana")</span><span class="sxs-lookup"><span data-stu-id="21277-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="21277-162">Varat atvērt vispārēja darba grupas dalībnieka resursa dublējuma prasību, atlasot saiti sadaļā Resursa prasības.</span><span class="sxs-lookup"><span data-stu-id="21277-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="21277-163">![Ekrānuzņēmums: dublēta resursa pieprasījuma atvēršana](media/FAQ-Resources-to-Tasks2-7.png "Ekrānuzņēmums: dublēta resursa pieprasījuma atvēršana")</span><span class="sxs-lookup"><span data-stu-id="21277-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="21277-164">Vispārejam resursam atlasiet **Rezervēt** un pēc tam varat izmantot plānošanas paneli, lai atrastu un rezervētu reālu resursu.</span><span class="sxs-lookup"><span data-stu-id="21277-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="21277-165">Jūs varat arī iesniegt, ka prasība ir jāizpilda resursu pārvaldniekam, atlasot **Iesniegt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="21277-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="21277-166">Kad vispārējais resurss ir aizpildīts ar nosauktu resursu, vispārējais resurss tiek noņemts no darba grupas un vispārējam resursam piešķirtie uzdevumi tiek piešķirti nosauktajam resursu, kas izpildīja vispārējā resursa prasības.</span><span class="sxs-lookup"><span data-stu-id="21277-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

