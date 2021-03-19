---
title: Resursu pārvaldības izmaiņas (Project Service Automation 3.x)
description: Šajā tēmā ir sniegta informācija par izmaiņām resursu pārvaldības apgabalā.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284772"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="310bf-103">Resursu pārvaldības izmaiņas (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="310bf-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="310bf-104">Šīs tēmas sadaļās ir sniegta informācija par izmaiņām, kas veiktas attiecībā uz resursu pārvaldības apgabalu programmas Dynamics 365 Project Service Automation versijā 3.x.</span><span class="sxs-lookup"><span data-stu-id="310bf-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="310bf-105">Projekta tāmes</span><span class="sxs-lookup"><span data-stu-id="310bf-105">Project estimates</span></span>

<span data-ttu-id="310bf-106">Projektu tāmes ir balstītas nevis uz entītiju **msdyn\_projecttask** (**Projekta uzdevums**), bet uz entītiju **msdynuz\_resourceassignment** (**Resursu piešķiršana**).</span><span class="sxs-lookup"><span data-stu-id="310bf-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="310bf-107">Resursu piešķires ir kļuvušas par “patiesās informācijas avotu” uzdevumu plānošanai un cenu noteikšanai.</span><span class="sxs-lookup"><span data-stu-id="310bf-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="310bf-108">Rindu uzdevumi</span><span class="sxs-lookup"><span data-stu-id="310bf-108">Line tasks</span></span>

<span data-ttu-id="310bf-109">Programmā PSA 3.x rindas uzdevumi ir novecojuši.</span><span class="sxs-lookup"><span data-stu-id="310bf-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="310bf-110">Uzdevumi tagad norāda uz visu uzdevumu, nevis uz rindu uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="310bf-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="310bf-111">Tālāk minētajā piemērā norādīts, kā uzdevums ar nosaukumu “Testa uzdevums”, ir piešķirts darba grupas dalībniekiem A un B iepriekšējās PSA versijās un PSA versijā 3.x.</span><span class="sxs-lookup"><span data-stu-id="310bf-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="310bf-112">**Pirms PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="310bf-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="310bf-113">Testa uzdevums</span><span class="sxs-lookup"><span data-stu-id="310bf-113">Test task</span></span>

        - <span data-ttu-id="310bf-114">Testa uzdevuma — 1. rindas uzdevums</span><span class="sxs-lookup"><span data-stu-id="310bf-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="310bf-115">Piešķiršana dalībniekam A</span><span class="sxs-lookup"><span data-stu-id="310bf-115">Assignment to A</span></span>

        - <span data-ttu-id="310bf-116">Testa uzdevuma — 2. rindas uzdevums</span><span class="sxs-lookup"><span data-stu-id="310bf-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="310bf-117">Piešķiršana dalībniekam B</span><span class="sxs-lookup"><span data-stu-id="310bf-117">Assignment to B</span></span>

- <span data-ttu-id="310bf-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="310bf-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="310bf-119">Testa uzdevums</span><span class="sxs-lookup"><span data-stu-id="310bf-119">Test task</span></span>

        - <span data-ttu-id="310bf-120">Piešķiršana dalībniekam A</span><span class="sxs-lookup"><span data-stu-id="310bf-120">Assignment to A</span></span>
        - <span data-ttu-id="310bf-121">Piešķiršana dalībniekam B</span><span class="sxs-lookup"><span data-stu-id="310bf-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="310bf-122">Nepiešķirta piešķire</span><span class="sxs-lookup"><span data-stu-id="310bf-122">Unassigned assignment</span></span>

<span data-ttu-id="310bf-123">Programmā PSA 3.x, nepiešķirta piešķire ir tāda piešķire, kas piešķirta darba grupas dalībniekam **NULL** un resursam **NULL**.</span><span class="sxs-lookup"><span data-stu-id="310bf-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="310bf-124">Nepiešķirtas piešķires var rasties vairākos scenārijos:</span><span class="sxs-lookup"><span data-stu-id="310bf-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="310bf-125">Ja uzdevums ir izveidots, bet tas vēl nav piešķirts nevienam darba grupas dalībniekam, vienmēr tiek izveidota nepiešķirta piešķire.</span><span class="sxs-lookup"><span data-stu-id="310bf-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="310bf-126">Ja tiek noņemti visi uzdevuma saņēmēji, attiecīgajam uzdevumam tiek atkārtoti izveidota nepiešķirta piešķire.</span><span class="sxs-lookup"><span data-stu-id="310bf-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="310bf-127">Entītijas Projekta uzdevums plānošanas lauki</span><span class="sxs-lookup"><span data-stu-id="310bf-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="310bf-128">Entītijas **msdyn\_projecttask** lauki ir novecojuši vai pārvietoti uz entītiju **msdyn\_resourceassignment**, vai arī uz tiem tagad ir atsauce no entītijas **msdyn\_projectteam** (**Projekta darba grupas dalībnieks**).</span><span class="sxs-lookup"><span data-stu-id="310bf-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="310bf-129">Novecojis lauks entītijā msdyn\_projecttask (Projekta uzdevums)</span><span class="sxs-lookup"><span data-stu-id="310bf-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="310bf-130">Jauns lauks entītijā msdyn\_resourceassignment (Resursa piešķiršana)</span><span class="sxs-lookup"><span data-stu-id="310bf-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="310bf-131">Komentārs</span><span class="sxs-lookup"><span data-stu-id="310bf-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="310bf-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="310bf-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="310bf-133">Nav</span><span class="sxs-lookup"><span data-stu-id="310bf-133">None</span></span> | |
| <span data-ttu-id="310bf-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="310bf-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="310bf-135">Nav</span><span class="sxs-lookup"><span data-stu-id="310bf-135">None</span></span> | |
| <span data-ttu-id="310bf-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="310bf-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="310bf-137">Nav</span><span class="sxs-lookup"><span data-stu-id="310bf-137">None</span></span> | |
| <span data-ttu-id="310bf-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="310bf-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="310bf-139">Nav</span><span class="sxs-lookup"><span data-stu-id="310bf-139">None</span></span> | |
| <span data-ttu-id="310bf-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="310bf-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="310bf-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="310bf-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="310bf-142">Ir mainīts JavaScript Object Notation (JSON) datu struktūras formāts, kas tiek glabāts laukā.</span><span class="sxs-lookup"><span data-stu-id="310bf-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="310bf-143">Plānošanas kontūra</span><span class="sxs-lookup"><span data-stu-id="310bf-143">Schedule contour</span></span>

<span data-ttu-id="310bf-144">Plānošanas kontūra tiek glabāta laukā **Plānotais darbs** (**msdyn\_plannedwork**) katrai entītijai **Resursa piešķiršana** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="310bf-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="310bf-145">Struktūra</span><span class="sxs-lookup"><span data-stu-id="310bf-145">Structure</span></span>

<span data-ttu-id="310bf-146">Plānošanas kontūras jaunā struktūra sastāv no elastīgiem laika sektoriem, kas ir definēti katrai grafika dienai.</span><span class="sxs-lookup"><span data-stu-id="310bf-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="310bf-147">Katram laika sektoram ir šādi rekvizīti:</span><span class="sxs-lookup"><span data-stu-id="310bf-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="310bf-148">**Sākums** — dienas darba stundu sākums atbilstoši projekta kalendāram.</span><span class="sxs-lookup"><span data-stu-id="310bf-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="310bf-149">**Beigas** — dienas darba stundu beigas atbilstoši projekta kalendāram.</span><span class="sxs-lookup"><span data-stu-id="310bf-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="310bf-150">**Stundas** — dienā piešķirto stundu skaits.</span><span class="sxs-lookup"><span data-stu-id="310bf-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="310bf-151">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="310bf-151">**Example**</span></span>

<span data-ttu-id="310bf-152">Šajā piemērā tiek izmantots projekta kalendārs, kurā darba diena ir no 9:00 līdz 17:00 UTC-8 laika joslā.</span><span class="sxs-lookup"><span data-stu-id="310bf-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="310bf-153">Automātiska plānošana un manuāla plānošana</span><span class="sxs-lookup"><span data-stu-id="310bf-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="310bf-154">Ja uzdevums tiek plānots automātiski, stundas tiek koncentrētas perioda sākumā un uzdevuma ilgums var tikt samazināts.</span><span class="sxs-lookup"><span data-stu-id="310bf-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="310bf-155">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="310bf-155">**Example**</span></span>

<span data-ttu-id="310bf-156">Šis uzdevums ir plānots automātiski, paredzot 18 stundas trīs dienu periodā (no 2018. gada 3. decembra līdz 2018. gada 5. decembrim).</span><span class="sxs-lookup"><span data-stu-id="310bf-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="310bf-157">Ja uzdevums tiek plānots manuāli, stundas tiek vienmērīgi sadalītas visos datumos.</span><span class="sxs-lookup"><span data-stu-id="310bf-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="310bf-158">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="310bf-158">**Example**</span></span>

<span data-ttu-id="310bf-159">Šis uzdevums ir plānots manuāli, paredzot 18 stundas trīs dienu periodā (no 2018. gada 3. decembra līdz 2018. gada 5. decembrim).</span><span class="sxs-lookup"><span data-stu-id="310bf-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="310bf-160">Piešķires vienība</span><span class="sxs-lookup"><span data-stu-id="310bf-160">Assignment unit</span></span>

<span data-ttu-id="310bf-161">Piešķires vienība ir novecojusi programmā PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="310bf-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="310bf-162">Tagad uzdevuma ieguldījuma stundas ir vienlīdzīgi sadalītas pa dienām visiem piešķirtajiem resursiem.</span><span class="sxs-lookup"><span data-stu-id="310bf-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="310bf-163">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="310bf-163">**Example**</span></span>

<span data-ttu-id="310bf-164">Šajā piemērā uzdevums tiek piešķirts diviem resursiem un tas tiek plānots automātiski, paredzot 36 stundas trīs dienu periodā (no 2018. gada 3. decembra līdz 2018. gada 5. decembrim).</span><span class="sxs-lookup"><span data-stu-id="310bf-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="310bf-165">1. piešķire:</span><span class="sxs-lookup"><span data-stu-id="310bf-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="310bf-166">2. piešķire:</span><span class="sxs-lookup"><span data-stu-id="310bf-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="310bf-167">Cenu noteikšanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="310bf-167">Pricing dimensions</span></span>

<span data-ttu-id="310bf-168">Programmā PSA 3.x dimensijas lauki, kas saistīti ar cenas noteikšanu resursam (piemēram, **Loma** un **Organizācijas vienība**), ir noņemti no entītijas **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="310bf-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="310bf-169">Šos laukus tagad var izgūt no resursu piešķiršanas (**msdyn\_resourceassignment**) atbilstošā projekta darba grupas dalībnieka (**msdyn\_projectteam**), kad tiek ģenerētas projektu tāmes.</span><span class="sxs-lookup"><span data-stu-id="310bf-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="310bf-170">Entītijai **msdyn\_projectteam** ir pievienots jauns lauks **msdyn\_organizationalunit**.</span><span class="sxs-lookup"><span data-stu-id="310bf-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="310bf-171">Novecojis lauks entītijā msdyn\_projecttask (Projekta uzdevums)</span><span class="sxs-lookup"><span data-stu-id="310bf-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="310bf-172">Lauks no msdyn\_projectteam (Projekta darba grupas dalībnieks), kas tiek izmantots tā vietā</span><span class="sxs-lookup"><span data-stu-id="310bf-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="310bf-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="310bf-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="310bf-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="310bf-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="310bf-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="310bf-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="310bf-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="310bf-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="310bf-177">Kontūras</span><span class="sxs-lookup"><span data-stu-id="310bf-177">Contours</span></span>

<span data-ttu-id="310bf-178">Entītijā **msdyn\_projecttask** ir novecojuši cenu noteikšanas un novērtējuma kontūru lauki.</span><span class="sxs-lookup"><span data-stu-id="310bf-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="310bf-179">Tie ir pārvietoti uz entītiju **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="310bf-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="310bf-180">Novecojis lauks entītijā msdyn\_projecttask (Projekta uzdevums)</span><span class="sxs-lookup"><span data-stu-id="310bf-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="310bf-181">Jauns lauks entītijā msdyn\_resourceassignment (Resursa piešķiršana)</span><span class="sxs-lookup"><span data-stu-id="310bf-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="310bf-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="310bf-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="310bf-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="310bf-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="310bf-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="310bf-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="310bf-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="310bf-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="310bf-186">Šie lauki ir pievienoti entītijai **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="310bf-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="310bf-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="310bf-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="310bf-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="310bf-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="310bf-189">Entītijai **msdyn\_projecttask** nav mainīti šādi lauki attiecībā uz plānotajām, faktiskajām un atlikušajām izmaksām un pārdošanas darījumiem:</span><span class="sxs-lookup"><span data-stu-id="310bf-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="310bf-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="310bf-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="310bf-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="310bf-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="310bf-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="310bf-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="310bf-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="310bf-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="310bf-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="310bf-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="310bf-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="310bf-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]