---
title: Projekta plānošana, izmantojot darba sadalījuma struktūru
description: Projekta plānošana, izmantojot darba sadalījuma struktūru programmā Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127887"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="65ed5-103">Projekta plānošana, izmantojot darba sadalījuma struktūru (Project Service)</span><span class="sxs-lookup"><span data-stu-id="65ed5-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="65ed5-104">Projekta grafikā var uzzināt, kāds darbs ir jāveic un kuri resursi šo dabu veiks, kā arī laikposmu, kurā darbs ir jāveic.</span><span class="sxs-lookup"><span data-stu-id="65ed5-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="65ed5-105">Projekta grafiks atspoguļo pilnībā visu darbu, kas saistīts ar savlaicīgu projekta nodošanu.</span><span class="sxs-lookup"><span data-stu-id="65ed5-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="65ed5-106">Viena no pirmajām darbībām projekta sākuma fāzē projekta grafika izstrāde.</span><span class="sxs-lookup"><span data-stu-id="65ed5-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="65ed5-107">Lai izveidotu projekta grafiku, ir jāizveido darba sadalījuma struktūra.</span><span class="sxs-lookup"><span data-stu-id="65ed5-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="65ed5-108">Izveidojot projekta struktūru ar darba sadalījuma struktūru, varat veikt šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="65ed5-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="65ed5-109">sadalīt darbu pārvaldāmos uzdevumos;</span><span class="sxs-lookup"><span data-stu-id="65ed5-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="65ed5-110">aprēķināt uzdevuma izpildei nepieciešamo laiku;</span><span class="sxs-lookup"><span data-stu-id="65ed5-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="65ed5-111">iestatīt uzdevuma atkarības un ilgumu;</span><span class="sxs-lookup"><span data-stu-id="65ed5-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="65ed5-112">noteikt lomas, kas nepieciešamas, lai izpildītu katru uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="65ed5-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="65ed5-113">Projekta grafikam darba sadalījuma struktūrā ir vienkāršs izskats un izkārtojums, kā arī tajā ir pieejama interaktīva Ganta diagramma.</span><span class="sxs-lookup"><span data-stu-id="65ed5-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="65ed5-114">Projekta darba sadalījuma struktūras izveide</span><span class="sxs-lookup"><span data-stu-id="65ed5-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="65ed5-115">Izveidojiet darba sadalījuma struktūru, lai norādītu projekta uzdevumu izpildes secību.</span><span class="sxs-lookup"><span data-stu-id="65ed5-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="65ed5-116">Darba sadalījuma struktūra ietver uzdevumus un prasības attiecībā uz to izpildi, kā arī ieņēmumu un izdevumu informāciju.</span><span class="sxs-lookup"><span data-stu-id="65ed5-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="65ed5-117">Darba sadalījuma struktūrai var pievienot:</span><span class="sxs-lookup"><span data-stu-id="65ed5-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="65ed5-118">projekta uzdevumu izpildes secību hierarhijā;</span><span class="sxs-lookup"><span data-stu-id="65ed5-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="65ed5-119">citus uzdevumus, ja tādi ir, kas jāizpilda, lai varētu sākt uzdevuma izpildi;</span><span class="sxs-lookup"><span data-stu-id="65ed5-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="65ed5-120">uzdevuma sākuma datumu, beigu datumu un ilgumu;</span><span class="sxs-lookup"><span data-stu-id="65ed5-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="65ed5-121">uzdevuma izpildei nepieciešamo stundu skaitu;</span><span class="sxs-lookup"><span data-stu-id="65ed5-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="65ed5-122">visas nepieciešamās darba prasmes un izglītību;</span><span class="sxs-lookup"><span data-stu-id="65ed5-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="65ed5-123">darbiniekus, kam uzdevums tika piešķirts;</span><span class="sxs-lookup"><span data-stu-id="65ed5-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="65ed5-124">prognozējamos ieņēmumus un izdevumus.</span><span class="sxs-lookup"><span data-stu-id="65ed5-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="65ed5-125">Uzdevumu tipi</span><span class="sxs-lookup"><span data-stu-id="65ed5-125">Task types</span></span>  
<span data-ttu-id="65ed5-126">Veidojot darba sadalījuma struktūru, izmantosit tālāk aprakstīto veidu uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="65ed5-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="65ed5-127">**Projekta saknes mezgls**</span><span class="sxs-lookup"><span data-stu-id="65ed5-127">**Project root node**</span></span> | <span data-ttu-id="65ed5-128">Projekta augšējā līmeņa kopsavilkuma uzdevums.</span><span class="sxs-lookup"><span data-stu-id="65ed5-128">The top-level summary task for the project.</span></span> <span data-ttu-id="65ed5-129">Visi citi projekta uzdevumi tiek izveidoti saskaņā ar to.</span><span class="sxs-lookup"><span data-stu-id="65ed5-129">All other project tasks are created under it.</span></span> <span data-ttu-id="65ed5-130">Saknes uzdevuma nosaukums ir projekta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="65ed5-130">The name of the root task is the project name.</span></span> <span data-ttu-id="65ed5-131">Saknes mezgla ieguldījums, datumi un ilgums ir balstīti uz tās hierarhijas vērtībām, kas atrodas zem tā.</span><span class="sxs-lookup"><span data-stu-id="65ed5-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="65ed5-132">Saknes mezgla rekvizītus nevar rediģēt un saknes mezglu nevar dzēst.</span><span class="sxs-lookup"><span data-stu-id="65ed5-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="65ed5-133">**Kopsavilkuma vai konteinera uzdevumi**</span><span class="sxs-lookup"><span data-stu-id="65ed5-133">**Summary or container tasks**</span></span> | <span data-ttu-id="65ed5-134">Kopsavilkuma uzdevums ir uzdevums, kam ir pakārtoti apakšuzdevumi.</span><span class="sxs-lookup"><span data-stu-id="65ed5-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="65ed5-135">Kopsavilkuma uzdevumam nav jebkāda darba ieguldījuma vai izmaksu.</span><span class="sxs-lookup"><span data-stu-id="65ed5-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="65ed5-136">Tā darba ieguldījums un izmaksas ir tā apakšuzdevumu apkopojums.</span><span class="sxs-lookup"><span data-stu-id="65ed5-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="65ed5-137">Kopsavilkuma uzdevuma nosaukumu var mainīt, tomēr nevar mainīt ieguldījumu, datumus vai ilgumu, jo šīs vērtības tiek aprēķinātas automātiski.</span><span class="sxs-lookup"><span data-stu-id="65ed5-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="65ed5-138">Dzēšot kopsavilkuma uzdevumu, tiek dzēsts uzdevums un visi tā apakšuzdevumi.</span><span class="sxs-lookup"><span data-stu-id="65ed5-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="65ed5-139">**Lapas mezgla uzdevumi**</span><span class="sxs-lookup"><span data-stu-id="65ed5-139">**Leaf node tasks**</span></span> | <span data-ttu-id="65ed5-140">Lapas mezgla uzdevums ir projekta darbs ar visdetalizētāko informāciju.</span><span class="sxs-lookup"><span data-stu-id="65ed5-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="65ed5-141">Tajā ir ietverta aptuvenais ieguldījums, plānotais resursu skaits, plānotais sākuma un beigu datums un ilgums.</span><span class="sxs-lookup"><span data-stu-id="65ed5-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="65ed5-142">Uzdevumu hierarhija</span><span class="sxs-lookup"><span data-stu-id="65ed5-142">Task hierarchy</span></span>  
 <span data-ttu-id="65ed5-143">Veidojot uzdevumu hierarhiju, ir pieejamas tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="65ed5-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="65ed5-144">**Uzdevuma pievienošana**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-144">**Add task**.</span></span>   <span data-ttu-id="65ed5-145">Varat pievienot uzdevumu izvēlētajā pozīcijā uzdevumu hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="65ed5-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="65ed5-146">Ja pozīciju neatlasāt, jaunais uzdevums tiek pievienots beigās.</span><span class="sxs-lookup"><span data-stu-id="65ed5-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="65ed5-147">**Uzdevuma atkāpes izveide**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-147">**Indent task**.</span></span>   <span data-ttu-id="65ed5-148">Veidojiet uzdevumam atkāpi, lai tas būtu tā uzdevuma apakšuzdevums, kas atrodas tieši virs šī uzdevuma.</span><span class="sxs-lookup"><span data-stu-id="65ed5-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="65ed5-149">**Uzdevuma pārkaru atkāpes izveide**</span><span class="sxs-lookup"><span data-stu-id="65ed5-149">**Outdent task**.</span></span>   <span data-ttu-id="65ed5-150">Veidojiet uzdevumam pārkaru atkāpi, lai tas vairs nebūtu sākotnējā galvenā uzdevuma apakšuzdevums.</span><span class="sxs-lookup"><span data-stu-id="65ed5-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="65ed5-151">**Pārvietot augšup un pārvietot lejup**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-151">**Move up and Move down**.</span></span>   <span data-ttu-id="65ed5-152">Pārvietojiet uzdevumus augšup un lejup galveno uzdevumu hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="65ed5-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="65ed5-153">Pārvietojot uzdevumu augšup vai lejup, netiek ietekmēts tā ieguldījums, izmaksas, datumi vai ilgums.</span><span class="sxs-lookup"><span data-stu-id="65ed5-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="65ed5-154">Uzdevuma atribūti</span><span class="sxs-lookup"><span data-stu-id="65ed5-154">Task attributes</span></span>  
 <span data-ttu-id="65ed5-155">Uzdevuma nosaukums raksturo darbu, kas jāizpilda.</span><span class="sxs-lookup"><span data-stu-id="65ed5-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="65ed5-156">Uzdevuma grafika un darbspēka vajadzību aprakstīšanai izmanto dažādus uzdevuma atribūtus.</span><span class="sxs-lookup"><span data-stu-id="65ed5-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="65ed5-157">Grafika atribūti</span><span class="sxs-lookup"><span data-stu-id="65ed5-157">Schedule attributes</span></span>

 - <span data-ttu-id="65ed5-158">Piešķiriet vērtības atribūtam **Ieguldījuma stundas**, **Resursu skaits**, **Sākuma datums**, **Beigu datums** un **Ilgums**, lai noteiktu uzdevuma grafiku.</span><span class="sxs-lookup"><span data-stu-id="65ed5-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="65ed5-159">Atribūts **Ieguldījums** ir aptuvenais laiks stundās, kas nepieciešams uzdevuma izpildei.</span><span class="sxs-lookup"><span data-stu-id="65ed5-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="65ed5-160">Atribūts **Resursu skaits** ir aprēķins, ko projekta vadītājs iestata uzdevumam, lai izstrādātu vislabāko iespējamo grafiku.</span><span class="sxs-lookup"><span data-stu-id="65ed5-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="65ed5-161">Atribūts **Ilgums** (dienās) norāda darba dienu skaitu, kas nepieciešams uzdevuma izpildei.</span><span class="sxs-lookup"><span data-stu-id="65ed5-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="65ed5-162">Darbspēka atribūti</span><span class="sxs-lookup"><span data-stu-id="65ed5-162">Staffing attributes</span></span>

 - <span data-ttu-id="65ed5-163">Atribūts **Loma**, **Resursu organizācijas struktūrvienība**, **Resursu skaits** un **Resursi** apraksta darbspēka vajadzības šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="65ed5-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="65ed5-164">Atribūts **Loma** apraksta, kāda tipa resurss ir vajadzīgs uzdevuma izpildei.</span><span class="sxs-lookup"><span data-stu-id="65ed5-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="65ed5-165">Atribūts **Resursu organizācijas struktūrvienība** norāda organizācijas struktūrvienību, no kuras jānodrošina resursi šī uzdevuma izpildei; tas ietekmē arī uzdevuma izmaksu un pārdošanas budžeta aprēķinus, jo tiek ņemts vērā, nosakot struktūrvienības pārdošanas cenu šim resursam.</span><span class="sxs-lookup"><span data-stu-id="65ed5-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="65ed5-166">Atribūts **Resursi** satur vispārējus resurss vai nosauktos resursus, ja tādi tiek atrasti.</span><span class="sxs-lookup"><span data-stu-id="65ed5-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="65ed5-167">Uzdevuma atkarības</span><span class="sxs-lookup"><span data-stu-id="65ed5-167">Task dependencies</span></span>  
 <span data-ttu-id="65ed5-168">Vienam vai vairākiem darba sadalījuma struktūras uzdevumiem varat izveidot pirmstecīgas relācijas.</span><span class="sxs-lookup"><span data-stu-id="65ed5-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="65ed5-169">Pirmstecīga uzdevuma laukam var iestatīt vienu vai vairākas vērtības, lai norādītu uzdevumus, no kuriem tas būs atkarīgs.</span><span class="sxs-lookup"><span data-stu-id="65ed5-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="65ed5-170">Piešķirot uzdevumam pirmstecīgu vērtību, uzdevumu var sākt tikai tad, kad ir pabeigti visi pirmstecīgie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="65ed5-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="65ed5-171">Iestatot uzdevumam šādu atkarību, tiks pārrēķināts plānotaisuzdevuma sākuma datums, ņemot vērā visu pirmstecīgo uzdevumu pēdējo beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="65ed5-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="65ed5-172">Pirmstecīgie uzdevumi ietekmē ne tikai grafika uzdevuma režīmu, kas definēts uzdevumā.</span><span class="sxs-lookup"><span data-stu-id="65ed5-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="65ed5-173">Uzdevuma režīms</span><span class="sxs-lookup"><span data-stu-id="65ed5-173">Task mode</span></span>  
 <span data-ttu-id="65ed5-174">Uzdevuma režīms ir viens no svarīgajiem faktoriem, kas nosaka lapu mezgla uzdevumu plānošanu.</span><span class="sxs-lookup"><span data-stu-id="65ed5-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="65ed5-175">Katram uzdevumam ir divi uzdevuma režīmi: automātisks plānošanas režīms un manuāls plānošanas režīms.</span><span class="sxs-lookup"><span data-stu-id="65ed5-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="65ed5-176">**Automātiskā plānošana**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-176">**Auto scheduling**.</span></span>   <span data-ttu-id="65ed5-177">Automātisks plānošanas režīms. Iestatot uzdevuma režīmu Automātiski plānots, uzdevuma plānošanas programma izmanto plānošanas kartulas šādos uzdevumu atribūtos, lai noteiktu uzdevumu grafiku:</span><span class="sxs-lookup"><span data-stu-id="65ed5-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="65ed5-178">Pirmstecīgie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="65ed5-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="65ed5-179">Ieguldījums</span><span class="sxs-lookup"><span data-stu-id="65ed5-179">Effort</span></span>  
  
    -   <span data-ttu-id="65ed5-180">Resursu skaits</span><span class="sxs-lookup"><span data-stu-id="65ed5-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="65ed5-181">Sākuma un beigu datumi</span><span class="sxs-lookup"><span data-stu-id="65ed5-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="65ed5-182">**Plānošanas kārtulas**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-182">**Scheduling rules**.</span></span>   <span data-ttu-id="65ed5-183">Tā lapas mezgla uzdevuma sākuma datums, kam projekta plānošanas sākuma datumā nav noklusējuma pirmstecīgu uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="65ed5-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="65ed5-184">Lapas mezgla uzdevuma ilgums vienmēr tiek aprēķināts kā darba dienu skaits no tā sākuma līdz beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="65ed5-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="65ed5-185">Ja uzdevums tiek plānots automātiski, plānošanas programma ievēro tālāk aprakstītās kārtulas.</span><span class="sxs-lookup"><span data-stu-id="65ed5-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="65ed5-186">Uzdevuma sākuma un beigu datumam vienmēr jābūt darbdienās atbilstoši projekta plānošanas kalendāram.</span><span class="sxs-lookup"><span data-stu-id="65ed5-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="65ed5-187">Uzdevuma, kam ir pirmstecīgi uzdevumi, sākuma datums pēc noklusējuma tiek iestatīts kā to pirmstecīgo uzdevumu vēlākais datums.</span><span class="sxs-lookup"><span data-stu-id="65ed5-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="65ed5-188">Ieguldījums = personu skaits * Ilgums * Stundas standarta projekta kalendāra darba dienā</span><span class="sxs-lookup"><span data-stu-id="65ed5-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="65ed5-189">**Manuāla plānošana**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-189">**Manual scheduling**.</span></span>   <span data-ttu-id="65ed5-190">Dažos gadījumos ieteicams atkāpties no šīm kārtulām.</span><span class="sxs-lookup"><span data-stu-id="65ed5-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="65ed5-191">Šajos gadījumos uzdevuma režīmam var iestatīt manuālu plānošanu.</span><span class="sxs-lookup"><span data-stu-id="65ed5-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="65ed5-192">Tas aptur plānošanas programmu no citu plānošanas atribūtu vērtību aprēķināšanas.</span><span class="sxs-lookup"><span data-stu-id="65ed5-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="65ed5-193">Iestatot pirmstecīgus uzdevumus, vienmēr tiek ietekmēti atkarīgo uzdevumu sākuma datums.</span><span class="sxs-lookup"><span data-stu-id="65ed5-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="65ed5-194">Darba sadalījuma struktūras izveide</span><span class="sxs-lookup"><span data-stu-id="65ed5-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="65ed5-195">Dodieties uz **Project Service > Projekti**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="65ed5-196">Noklikšķiniet uz projekta, pie kura gribat strādāt.</span><span class="sxs-lookup"><span data-stu-id="65ed5-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="65ed5-197">Ekrāna augšdaļā esošajā joslā atlasiet lejupvērsto bultiņu pie projekta nosaukuma un pēc tam noklikšķiniet uz Darba sadalījuma struktūra.</span><span class="sxs-lookup"><span data-stu-id="65ed5-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="65ed5-198">Lai pievienotu uzdevumu, noklikšķiniet uz **Pievienot uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="65ed5-199">Aizpildiet uzdevuma laukus un pēc tam noklikšķiniet uz vienuma **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="65ed5-200">Turpiniet pievienot uzdevumus, līdz darba sadalījuma struktūra ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="65ed5-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="65ed5-201">Veidojot darba sadalījuma struktūru, varat veikt tālāk minētās darbības, lai sakārtotu uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="65ed5-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="65ed5-202">Atlasiet uzdevumu un noklikšķiniet uz **Izveidot atkāpi**, lai to pārvietotu zem cita uzdevuma, vai noklikšķiniet uz Izveidot pārkaru atkāpi, lai to izņemto no esošā līmeņa.</span><span class="sxs-lookup"><span data-stu-id="65ed5-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="65ed5-203">Atlasiet uzdevumu un noklikšķiniet uz **Pārvietot uz augšu** vai **Pārvietot uz leju**, lai to pārvietotu augšup vai lejup sarakstā.</span><span class="sxs-lookup"><span data-stu-id="65ed5-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="65ed5-204">Noklikšķiniet uz **Paslēpt Ganta diagrammu**, lai paslēptu Ganta diagrammu, un noklikšķiniet uz **Parādīt Ganta diagrammu**, lai to atkal parādītu.</span><span class="sxs-lookup"><span data-stu-id="65ed5-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="65ed5-205">Atlasiet dažādus laika posmus Ganta diagrammas sadaļā **Laika skala**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="65ed5-206">Lai pievienotu lomas, ko projekta darba grupa dalībniekiem norādījāt darba sadalījuma struktūrā, noklikšķiniet uz **Ģenerēt projekta darba grupu**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="65ed5-207">Kad esat pabeidzis izmaiņu veikšanu, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="65ed5-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="65ed5-208">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="65ed5-208">See Also</span></span>  
 [<span data-ttu-id="65ed5-209">Projektu vadītāja rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="65ed5-209">Project manager guide</span></span>](../psa/project-manager-guide.md)