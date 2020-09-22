---
title: Jaunināšanas apsvērumi darba sadalījuma struktūrai
description: Šajā tēmā ir sniegta informācija par darba sadalījuma struktūras jaunināšanu no programmas Project Service Automation 2.x uz 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753522"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="8873a-103">Jaunināšanas apsvērumi darba sadalījuma struktūrai</span><span class="sxs-lookup"><span data-stu-id="8873a-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="8873a-104">Šajā tēmā ir sniegta informācija par darba sadalījuma struktūras jaunināšanu no programmas Project Service Automation 2.x uz 3.x.</span><span class="sxs-lookup"><span data-stu-id="8873a-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="8873a-105">Šajā tēmā ir definēts labs projekta stāvoklis programmā Project Service Automation (PSA), kas ir nepieciešams sekmīgai jaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="8873a-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="8873a-106">Ir pieejama arī informācija par vispārējiem bloķēšanas nosacījumiem, kas var izraisīt jaunināšanas kļūmi.</span><span class="sxs-lookup"><span data-stu-id="8873a-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="8873a-107">Papildinformāciju par projekta uzdevumu un to funkciju definēšanu projekta grafikā skatiet sadaļā [Projektu grafiki](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="8873a-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="8873a-108">Galvenās entītijas</span><span class="sxs-lookup"><span data-stu-id="8873a-108">Key entities</span></span>
<span data-ttu-id="8873a-109">Lai iegūtu precīzu darba sadalījuma struktūru, kas jau ir ielādēta ar resursiem, ir nepieciešamas šādas entītijas:</span><span class="sxs-lookup"><span data-stu-id="8873a-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="8873a-110">Projekts</span><span class="sxs-lookup"><span data-stu-id="8873a-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="8873a-111">Projekta darba grupa</span><span class="sxs-lookup"><span data-stu-id="8873a-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="8873a-112">Projekta uzdevums</span><span class="sxs-lookup"><span data-stu-id="8873a-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="8873a-113">Resursu piešķires</span><span class="sxs-lookup"><span data-stu-id="8873a-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="8873a-114">Projekta uzdevuma atkarība</span><span class="sxs-lookup"><span data-stu-id="8873a-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="8873a-115">Rezervējamie resursi</span><span class="sxs-lookup"><span data-stu-id="8873a-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="8873a-116">Lai definētu resursu ielādētu darba sadalījuma struktūru, ir jāveic šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="8873a-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="8873a-117">Izveidojiet jaunu projektu.</span><span class="sxs-lookup"><span data-stu-id="8873a-117">Create a new project.</span></span> <span data-ttu-id="8873a-118">Papildinformāciju par to, kā izveidot jaunu projektu, skatiet [msdyn_project](../developer/entities/msdyn_project.md).</span><span class="sxs-lookup"><span data-stu-id="8873a-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="8873a-119">Izveidojiet vienu vai vairākus uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="8873a-119">Create one or more tasks.</span></span> <span data-ttu-id="8873a-120">Papildinformāciju par to, kā izveidot uzdevumu, skatiet [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span><span class="sxs-lookup"><span data-stu-id="8873a-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="8873a-121">Definējiet uzdevumu atkarības.</span><span class="sxs-lookup"><span data-stu-id="8873a-121">Define the task dependencies.</span></span> <span data-ttu-id="8873a-122">Papildinformāciju skatiet tēmā [Projekta uzdevuma atkarība](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="8873a-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="8873a-123">Projektam nozīmējiet projekta grupas dalībniekus.</span><span class="sxs-lookup"><span data-stu-id="8873a-123">Assign project team members to the project.</span></span> <span data-ttu-id="8873a-124">Papildinformāciju skatiet [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span><span class="sxs-lookup"><span data-stu-id="8873a-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="8873a-125">Uzdevumiem nozīmējiet projekta darba grupas dalībniekus.</span><span class="sxs-lookup"><span data-stu-id="8873a-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="8873a-126">Papildinformāciju skatiet [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span><span class="sxs-lookup"><span data-stu-id="8873a-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="8873a-127">Projekta darba grupas attiecības</span><span class="sxs-lookup"><span data-stu-id="8873a-127">Project team relationships</span></span>

<span data-ttu-id="8873a-128">Lai nodrošinātu veiksmīgu jaunināšanu, pareizi jāsaglabā šādas attiecības:</span><span class="sxs-lookup"><span data-stu-id="8873a-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="8873a-129">Visiem projekta grupas dalībniekiem ir jābūt saistītiem ar rezervējamo resursu.</span><span class="sxs-lookup"><span data-stu-id="8873a-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="8873a-130">Visiem projekta grupas dalībniekiem ir jābūt saistītiem ar vienu un to pašu projektu.</span><span class="sxs-lookup"><span data-stu-id="8873a-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="8873a-131">Projekta uzdevumu attiecības</span><span class="sxs-lookup"><span data-stu-id="8873a-131">Project task relationships</span></span>
<span data-ttu-id="8873a-132">Lai nodrošinātu veiksmīgu jaunināšanu, pareizi jāsaglabā šādas attiecības:</span><span class="sxs-lookup"><span data-stu-id="8873a-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="8873a-133">Visi saistītie uzdevumi ir jāsaista ar vienu un to pašu projektu.</span><span class="sxs-lookup"><span data-stu-id="8873a-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="8873a-134">Katram rindas uzdevumam ir jābūt pamatuzdevumam.</span><span class="sxs-lookup"><span data-stu-id="8873a-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="8873a-135">Katram uzdevumam ir jābūt pamatprojektam.</span><span class="sxs-lookup"><span data-stu-id="8873a-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="8873a-136">Derīgi nosacījumi</span><span class="sxs-lookup"><span data-stu-id="8873a-136">Valid conditions</span></span>

- <span data-ttu-id="8873a-137">Visiem uzdevumu ilgumiem jābūt lielākiem par vai vienādiem ar (> =) vienu stundu un mazākiem par 1 800 000 minūtēm (1 250 dienām).\*</span><span class="sxs-lookup"><span data-stu-id="8873a-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="8873a-138">Visiem uzdevumiem ir jābūt sākuma datumam, kas nav agrāks par 01.01.2000.\*</span><span class="sxs-lookup"><span data-stu-id="8873a-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="8873a-139">Visiem uzdevumiem ir jābūt sākuma datumam, kas nav vēlāks kā 17 gadi pēc šīs dienas.\*</span><span class="sxs-lookup"><span data-stu-id="8873a-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="8873a-140">Visiem uzdevumiem sākuma datumam ir jābūt agrākam vai vienādam ar to pabeigšanas datumu.</span><span class="sxs-lookup"><span data-stu-id="8873a-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="8873a-141">Visiem transakciju tipiem pēc klasifikācijām (izdevumi, materiāls, nodoklis un laiks) ir jābūt norādītām vērtībām attiecībā uz **Noklusējuma vienību** un **Vienības grupu**.</span><span class="sxs-lookup"><span data-stu-id="8873a-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="8873a-142">Ir jāizvairās no datu formātu rakstīšanas ar burtiem.</span><span class="sxs-lookup"><span data-stu-id="8873a-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="8873a-143">Potenciālās samazināšanas darbības</span><span class="sxs-lookup"><span data-stu-id="8873a-143">Potential mitigation steps</span></span>
- <span data-ttu-id="8873a-144">Izmantojiet detalizēto atrašanu, lai identificētu projekta uzdevumus, kas nesatur projekta ID.</span><span class="sxs-lookup"><span data-stu-id="8873a-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="8873a-145">Izmantojiet detalizēto atrašanu, lai identificētu projekta uzdevumus, kuru plānotais ilgums pārsniedz > 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="8873a-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="8873a-146">Pirms datu izmaiņu veikšanas jāizpēta visi pielāgojumi, kas saistīti ar entītiju, kas, iespējams, ir izraisījuši datu nokļūšanu sliktā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="8873a-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="8873a-147">Šie pielāgojumi ir jāskata, lai turpinātu jebkurus ar datiem saistītos atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="8873a-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="8873a-148">Noteiktajiem uzdevumiem, kas ir nošķirti no vecākprojekta, apsveriet iespēju dzēst šos uzdevumus, ja tie nav nepieciešami vai tie ir jāsaista ar pareizo primāro projektu.</span><span class="sxs-lookup"><span data-stu-id="8873a-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="8873a-149">Visiem uzdevumiem, kuru ilgums pārsniedz 1250 dienas, apsveriet iespēju pievienot vairākus uzdevumus, lai atspoguļotu kopējo ilgumu, ja tas ir iespējams.</span><span class="sxs-lookup"><span data-stu-id="8873a-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="8873a-150">Ar zvaigznīti (\*) atzīmētajiem elementiem ir ierobežojumi, kas ir saistīti ar faktu, ka klientu attiecību pārvaldība (CRM) atbalsta tikai 7320 atkārtošanās paplašinājumus.</span><span class="sxs-lookup"><span data-stu-id="8873a-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="8873a-151">Nepārsniedziet šo ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="8873a-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="8873a-152">Resursa piešķiršanas attiecības</span><span class="sxs-lookup"><span data-stu-id="8873a-152">Resource Assignment relationships</span></span>
<span data-ttu-id="8873a-153">Lai nodrošinātu veiksmīgu jaunināšanu, pareizi jāsaglabā šādas attiecības:</span><span class="sxs-lookup"><span data-stu-id="8873a-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="8873a-154">Visām resursu piešķirēm darba sadalījuma struktūrā ir jābūt saistītiem ar vienu un to pašu projektu.</span><span class="sxs-lookup"><span data-stu-id="8873a-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="8873a-155">Visām resursu piešķirēm darba sadalījuma struktūrā ir jābūt saistītiem ar projekta grupas dalībniekiem vienā un tajā pašā projektā.</span><span class="sxs-lookup"><span data-stu-id="8873a-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="8873a-156">Potenciālās samazināšanas darbības</span><span class="sxs-lookup"><span data-stu-id="8873a-156">Potential mitigation steps</span></span>
- <span data-ttu-id="8873a-157">Norādiet visus uzdevumus, kas neatbilst iepriekš aprakstītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="8873a-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="8873a-158">Visas resursu piešķires, kas vairs nav derīgas, ir jāizdzēš.</span><span class="sxs-lookup"><span data-stu-id="8873a-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="8873a-159">Projekta uzdevuma atkarības attiecības</span><span class="sxs-lookup"><span data-stu-id="8873a-159">Project task dependency relationships</span></span>
<span data-ttu-id="8873a-160">Lai nodrošinātu veiksmīgu jaunināšanu, pareizi jāsaglabā šādas attiecības:</span><span class="sxs-lookup"><span data-stu-id="8873a-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="8873a-161">Visām projekta uzdevuma atkarībām ir jābūt saistītām ar vienu un to pašu projektu.</span><span class="sxs-lookup"><span data-stu-id="8873a-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="8873a-162">Uzdevumam nevar būt vienas un tās pašas atkarības atsauces vairāk nekā vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="8873a-162">A task can't have the same dependency referenced more than once.</span></span>
