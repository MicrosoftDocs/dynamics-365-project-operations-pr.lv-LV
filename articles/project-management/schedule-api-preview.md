---
title: Plānošanas API izmantošana operāciju veikšanai ar plānošanas entītijām
description: Šajā tēmā ir sniegta informācija un piemēri plānošanas API izmantošanai.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950813"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="64df6-103">Plānošanas API izmantošana operāciju veikšanai ar plānošanas entītijām</span><span class="sxs-lookup"><span data-stu-id="64df6-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="64df6-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="64df6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="64df6-105">Daļa vai visa šajā tēmā norādītā funkcionalitāte ir pieejama lietotājiem kā daļa no priekšskatījuma laidiena.</span><span class="sxs-lookup"><span data-stu-id="64df6-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="64df6-106">Saturs un funkcionalitāte var mainīties.</span><span class="sxs-lookup"><span data-stu-id="64df6-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="64df6-107">Plānošanas entītijas</span><span class="sxs-lookup"><span data-stu-id="64df6-107">Scheduling entities</span></span>

<span data-ttu-id="64df6-108">Plānošanas API nodrošina iespēju veikt izveides, atjaunināšanas un dzēšanas operācijas ar **plānošanas entītijām**.</span><span class="sxs-lookup"><span data-stu-id="64df6-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="64df6-109">Šīs entītijas tiek pārvaldītas, izmantojot projekta tīmekļa plānošanas programmu.</span><span class="sxs-lookup"><span data-stu-id="64df6-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="64df6-110">Iepriekšējos Dynamics 365 Project Operations laidienos tika ierobežotas izveides, atjaunināšanas un dzēšanas operācijas ar **plānošanas entītijām**.</span><span class="sxs-lookup"><span data-stu-id="64df6-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="64df6-111">Tālāk sniegtajā tabulā ir sniegts pilnīgs **plānošanas entītiju** saraksts.</span><span class="sxs-lookup"><span data-stu-id="64df6-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="64df6-112">Entītijas nosaukums</span><span class="sxs-lookup"><span data-stu-id="64df6-112">Entity name</span></span>  | <span data-ttu-id="64df6-113">Entītijas loģiskais nosaukums</span><span class="sxs-lookup"><span data-stu-id="64df6-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="64df6-114">Project</span><span class="sxs-lookup"><span data-stu-id="64df6-114">Project</span></span> | <span data-ttu-id="64df6-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="64df6-115">msdyn_project</span></span> |
| <span data-ttu-id="64df6-116">Projekta uzdevums</span><span class="sxs-lookup"><span data-stu-id="64df6-116">Project Task</span></span>  | <span data-ttu-id="64df6-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="64df6-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="64df6-118">Projekta uzdevuma atkarība</span><span class="sxs-lookup"><span data-stu-id="64df6-118">Project Task Dependency</span></span>  | <span data-ttu-id="64df6-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="64df6-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="64df6-120">Resursu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="64df6-120">Resource Assignment</span></span> | <span data-ttu-id="64df6-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="64df6-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="64df6-122">Projekta bloks</span><span class="sxs-lookup"><span data-stu-id="64df6-122">Project Bucket</span></span>  | <span data-ttu-id="64df6-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="64df6-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="64df6-124">Projekta grupas dalībnieks</span><span class="sxs-lookup"><span data-stu-id="64df6-124">Project Team Member</span></span> | <span data-ttu-id="64df6-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="64df6-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="64df6-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="64df6-126">OperationSet</span></span>

<span data-ttu-id="64df6-127">OperationSet ir darba vienības shēma, ko var izmantot, kad transakcijā ir jāapstrādā vairāki plānošanas ietekmēšanas pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="64df6-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="64df6-128">Plānošanas API</span><span class="sxs-lookup"><span data-stu-id="64df6-128">Schedule APIs</span></span>

<span data-ttu-id="64df6-129">Tālāk ir saraksts ar pašreizējiem plānošanas API.</span><span class="sxs-lookup"><span data-stu-id="64df6-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="64df6-130">**msdyn_CreateProjectV1**: šo API var izmantot, lai izveidotu projektu.</span><span class="sxs-lookup"><span data-stu-id="64df6-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="64df6-131">Nekavējoties tiek izveidots projekts un noklusējuma projekta bloks.</span><span class="sxs-lookup"><span data-stu-id="64df6-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="64df6-132">**msdyn_CreateTeamMemberV1**: šo API var izmantot, lai izveidotu projekta darba grupas dalībnieku.</span><span class="sxs-lookup"><span data-stu-id="64df6-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="64df6-133">Darba grupas dalībnieka ieraksts tiek izveidots nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="64df6-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="64df6-134">**msdyn_CreateOperationSetV1**: šo API var izmantot, lai ieplānotu vairākus pieprasījumus, kas jāveic transakcijā.</span><span class="sxs-lookup"><span data-stu-id="64df6-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="64df6-135">**msdyn_PSSCreateV1**: šo API var izmantot, lai izveidotu entītiju.</span><span class="sxs-lookup"><span data-stu-id="64df6-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="64df6-136">Entītija var būt jebkura no plānošanas entītijām, kas atbalsta izveides operāciju.</span><span class="sxs-lookup"><span data-stu-id="64df6-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="64df6-137">**msdyn_PSSUpdateV1**: šo API var izmantot, lai atjauninātu entītiju.</span><span class="sxs-lookup"><span data-stu-id="64df6-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="64df6-138">Entītija var būt jebkura no plānošanas entītijām, kas atbalsta atjaunināšanas operāciju.</span><span class="sxs-lookup"><span data-stu-id="64df6-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="64df6-139">**msdyn_PSSDeleteV1**: šo API var izmantot, lai dzēstu entītiju.</span><span class="sxs-lookup"><span data-stu-id="64df6-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="64df6-140">Entītija var būt jebkura no plānošanas entītijām, kas atbalsta dzēšanas operāciju.</span><span class="sxs-lookup"><span data-stu-id="64df6-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="64df6-141">**msdyn_ExecuteOperationSetV1**: šis API tiek izmantots, lai izpildītu visas operācijas attiecīgajā operāciju kopā.</span><span class="sxs-lookup"><span data-stu-id="64df6-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="64df6-142">Plānošanas API izmantošana ar OperationSet</span><span class="sxs-lookup"><span data-stu-id="64df6-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="64df6-143">Tā kā ieraksti, kuriem ir gan **CreateProjectV1**, gan **CreateTeamMemberV1**, tiek izveidoti nekavējoties, šos API nevar izmantot tieši kopā **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="64df6-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="64df6-144">Tomēr API var lietot, lai izveidotu nepieciešamos ierakstus, izveidotu **OperationSet** un pēc tam izmantotu šos iepriekš izveidotos ierakstus kopā **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="64df6-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="64df6-145">Atbalstītās operācijas</span><span class="sxs-lookup"><span data-stu-id="64df6-145">Supported operations</span></span>

| <span data-ttu-id="64df6-146">Plānošanas entītija</span><span class="sxs-lookup"><span data-stu-id="64df6-146">Scheduling entity</span></span> | <span data-ttu-id="64df6-147">Izveide</span><span class="sxs-lookup"><span data-stu-id="64df6-147">Create</span></span> | <span data-ttu-id="64df6-148">Atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="64df6-148">Update</span></span> | <span data-ttu-id="64df6-149">Delete</span><span class="sxs-lookup"><span data-stu-id="64df6-149">Delete</span></span> | <span data-ttu-id="64df6-150">Svarīgi ieteikumi</span><span class="sxs-lookup"><span data-stu-id="64df6-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="64df6-151">Projekta uzdevums</span><span class="sxs-lookup"><span data-stu-id="64df6-151">Project task</span></span> | <span data-ttu-id="64df6-152">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-152">Yes</span></span> | <span data-ttu-id="64df6-153">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-153">Yes</span></span> | <span data-ttu-id="64df6-154">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-154">Yes</span></span> | <span data-ttu-id="64df6-155">Nevienu</span><span class="sxs-lookup"><span data-stu-id="64df6-155">None</span></span> |
| <span data-ttu-id="64df6-156">Projekta uzdevuma atkarība</span><span class="sxs-lookup"><span data-stu-id="64df6-156">Project task dependency</span></span> | <span data-ttu-id="64df6-157">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-157">Yes</span></span> | <span data-ttu-id="64df6-158">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-158">Yes</span></span> | | <span data-ttu-id="64df6-159">Projekta uzdevumu atkarības ieraksti netiek atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="64df6-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="64df6-160">Tā vietā var izdzēst veco ierakstu un izveidot jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="64df6-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="64df6-161">Resursu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="64df6-161">Resource assignment</span></span> | <span data-ttu-id="64df6-162">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-162">Yes</span></span> | <span data-ttu-id="64df6-163">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-163">Yes</span></span> | | <span data-ttu-id="64df6-164">Netiek atbalstītas operācijas ar šādiem laukiem: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** un **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="64df6-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="64df6-165">Resursu piešķiršanas ieraksti netiek atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="64df6-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="64df6-166">Tā vietā var izdzēst veco ierakstu un izveidot jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="64df6-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="64df6-167">Projekta bloks</span><span class="sxs-lookup"><span data-stu-id="64df6-167">Project bucket</span></span> | <span data-ttu-id="64df6-168">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="64df6-168">N/A</span></span> | <span data-ttu-id="64df6-169">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="64df6-169">N/A</span></span> | <span data-ttu-id="64df6-170">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="64df6-170">N/A</span></span> | <span data-ttu-id="64df6-171">Noklusējuma bloks tiek izveidots, izmantojot **CreateProjectV1** API.</span><span class="sxs-lookup"><span data-stu-id="64df6-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="64df6-172">Projekta darba grupas dalībnieks</span><span class="sxs-lookup"><span data-stu-id="64df6-172">Project team member</span></span> | <span data-ttu-id="64df6-173">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-173">Yes</span></span> | <span data-ttu-id="64df6-174">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-174">Yes</span></span> | <span data-ttu-id="64df6-175">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-175">Yes</span></span> | <span data-ttu-id="64df6-176">Izveides operācijai izmantojiet **CreateTeamMemberV1** API.</span><span class="sxs-lookup"><span data-stu-id="64df6-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="64df6-177">Project</span><span class="sxs-lookup"><span data-stu-id="64df6-177">Project</span></span> | <span data-ttu-id="64df6-178">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-178">Yes</span></span> | <span data-ttu-id="64df6-179">Jā</span><span class="sxs-lookup"><span data-stu-id="64df6-179">Yes</span></span> | <span data-ttu-id="64df6-180">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="64df6-180">N/A</span></span> | <span data-ttu-id="64df6-181">Netiek atbalstītas operācijas ar šādiem laukiem: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** un **Duration**.</span><span class="sxs-lookup"><span data-stu-id="64df6-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="64df6-182">Šos API var izsaukt ar entītijas objektiem, kuros ir pielāgoti lauki.</span><span class="sxs-lookup"><span data-stu-id="64df6-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="64df6-183">Rekvizīts ID nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="64df6-183">The ID property is optional.</span></span> <span data-ttu-id="64df6-184">Ja tas ir nodrošināts, sistēma mēģina to izmantot un rodas izņēmums, ja to nevar izmantot.</span><span class="sxs-lookup"><span data-stu-id="64df6-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="64df6-185">Ja tas nav nodrošināts, sistēma to ģenerēs.</span><span class="sxs-lookup"><span data-stu-id="64df6-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="64df6-186">Ierobežotie lauki</span><span class="sxs-lookup"><span data-stu-id="64df6-186">Restricted fields</span></span>

<span data-ttu-id="64df6-187">Tālāk redzamajās tabulās ir definēti lauki, kuriem ir **Izveidot** un **Rediģēt** ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="64df6-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="64df6-188">Projekta uzdevums</span><span class="sxs-lookup"><span data-stu-id="64df6-188">Project task</span></span>

| <span data-ttu-id="64df6-189">**Loģiskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="64df6-189">**Logical name**</span></span>                       | <span data-ttu-id="64df6-190">**Var izveidot**</span><span class="sxs-lookup"><span data-stu-id="64df6-190">**Can create**</span></span> | <span data-ttu-id="64df6-191">**Var rediģēt**</span><span class="sxs-lookup"><span data-stu-id="64df6-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="64df6-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="64df6-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="64df6-193">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-193">no</span></span>             | <span data-ttu-id="64df6-194">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-194">no</span></span>               |
| <span data-ttu-id="64df6-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="64df6-196">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-196">no</span></span>             | <span data-ttu-id="64df6-197">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-197">no</span></span>               |
| <span data-ttu-id="64df6-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="64df6-198">msdyn_actualend</span></span>                        | <span data-ttu-id="64df6-199">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-199">no</span></span>             | <span data-ttu-id="64df6-200">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-200">no</span></span>               |
| <span data-ttu-id="64df6-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="64df6-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="64df6-202">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-202">no</span></span>             | <span data-ttu-id="64df6-203">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-203">no</span></span>               |
| <span data-ttu-id="64df6-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="64df6-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="64df6-205">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-205">no</span></span>             | <span data-ttu-id="64df6-206">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-206">no</span></span>               |
| <span data-ttu-id="64df6-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="64df6-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="64df6-208">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-208">no</span></span>             | <span data-ttu-id="64df6-209">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-209">no</span></span>               |
| <span data-ttu-id="64df6-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="64df6-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="64df6-211">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-211">no</span></span>             | <span data-ttu-id="64df6-212">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-212">no</span></span>               |
| <span data-ttu-id="64df6-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="64df6-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="64df6-214">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-214">no</span></span>             | <span data-ttu-id="64df6-215">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-215">no</span></span>               |
| <span data-ttu-id="64df6-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="64df6-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="64df6-217">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-217">no</span></span>             | <span data-ttu-id="64df6-218">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-218">no</span></span>               |
| <span data-ttu-id="64df6-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="64df6-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="64df6-220">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-220">no</span></span>             | <span data-ttu-id="64df6-221">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-221">no</span></span>               |
| <span data-ttu-id="64df6-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="64df6-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="64df6-223">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-223">no</span></span>             | <span data-ttu-id="64df6-224">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-224">no</span></span>               |
| <span data-ttu-id="64df6-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="64df6-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="64df6-226">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-226">no</span></span>             | <span data-ttu-id="64df6-227">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-227">no</span></span>               |
| <span data-ttu-id="64df6-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="64df6-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="64df6-229">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-229">no</span></span>             | <span data-ttu-id="64df6-230">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-230">no</span></span>               |
| <span data-ttu-id="64df6-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="64df6-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="64df6-232">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-232">no</span></span>             | <span data-ttu-id="64df6-233">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-233">no</span></span>               |
| <span data-ttu-id="64df6-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="64df6-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="64df6-235">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-235">no</span></span>             | <span data-ttu-id="64df6-236">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-236">no</span></span>               |
| <span data-ttu-id="64df6-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="64df6-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="64df6-238">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-238">no</span></span>             | <span data-ttu-id="64df6-239">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-239">no</span></span>               |
| <span data-ttu-id="64df6-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="64df6-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="64df6-241">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-241">no</span></span>             | <span data-ttu-id="64df6-242">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-242">no</span></span>               |
| <span data-ttu-id="64df6-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="64df6-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="64df6-244">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-244">no</span></span>             | <span data-ttu-id="64df6-245">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-245">no</span></span>               |
| <span data-ttu-id="64df6-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="64df6-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="64df6-247">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-247">no</span></span>             | <span data-ttu-id="64df6-248">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-248">no</span></span>               |
| <span data-ttu-id="64df6-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="64df6-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="64df6-250">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-250">no</span></span>             | <span data-ttu-id="64df6-251">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-251">no</span></span>               |
| <span data-ttu-id="64df6-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="64df6-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="64df6-253">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-253">no</span></span>             | <span data-ttu-id="64df6-254">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-254">no</span></span>               |
| <span data-ttu-id="64df6-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="64df6-256">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-256">no</span></span>             | <span data-ttu-id="64df6-257">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-257">no</span></span>               |
| <span data-ttu-id="64df6-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="64df6-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="64df6-259">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-259">no</span></span>             | <span data-ttu-id="64df6-260">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-260">no</span></span>               |
| <span data-ttu-id="64df6-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="64df6-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="64df6-262">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-262">no</span></span>             | <span data-ttu-id="64df6-263">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-263">no</span></span>               |
| <span data-ttu-id="64df6-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="64df6-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="64df6-265">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-265">no</span></span>             | <span data-ttu-id="64df6-266">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-266">no</span></span>               |
| <span data-ttu-id="64df6-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="64df6-267">msdyn_progress</span></span>                         | <span data-ttu-id="64df6-268">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-268">no</span></span>             | <span data-ttu-id="64df6-269">nē (jā P4W)</span><span class="sxs-lookup"><span data-stu-id="64df6-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="64df6-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="64df6-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="64df6-271">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-271">no</span></span>             | <span data-ttu-id="64df6-272">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-272">no</span></span>               |
| <span data-ttu-id="64df6-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="64df6-274">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-274">no</span></span>             | <span data-ttu-id="64df6-275">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-275">no</span></span>               |
| <span data-ttu-id="64df6-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="64df6-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="64df6-277">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-277">no</span></span>             | <span data-ttu-id="64df6-278">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-278">no</span></span>               |
| <span data-ttu-id="64df6-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="64df6-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="64df6-280">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-280">no</span></span>             | <span data-ttu-id="64df6-281">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-281">no</span></span>               |
| <span data-ttu-id="64df6-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="64df6-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="64df6-283">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-283">no</span></span>             | <span data-ttu-id="64df6-284">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-284">no</span></span>               |
| <span data-ttu-id="64df6-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="64df6-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="64df6-286">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-286">no</span></span>             | <span data-ttu-id="64df6-287">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-287">no</span></span>               |
| <span data-ttu-id="64df6-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="64df6-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="64df6-289">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-289">no</span></span>             | <span data-ttu-id="64df6-290">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-290">no</span></span>               |
| <span data-ttu-id="64df6-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="64df6-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="64df6-292">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-292">no</span></span>             | <span data-ttu-id="64df6-293">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-293">no</span></span>               |
| <span data-ttu-id="64df6-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="64df6-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="64df6-295">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-295">no</span></span>             | <span data-ttu-id="64df6-296">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-296">no</span></span>               |
| <span data-ttu-id="64df6-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="64df6-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="64df6-298">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-298">no</span></span>             | <span data-ttu-id="64df6-299">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-299">no</span></span>               |
| <span data-ttu-id="64df6-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="64df6-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="64df6-301">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-301">no</span></span>             | <span data-ttu-id="64df6-302">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-302">no</span></span>               |
| <span data-ttu-id="64df6-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="64df6-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="64df6-304">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-304">no</span></span>             | <span data-ttu-id="64df6-305">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-305">no</span></span>               |
| <span data-ttu-id="64df6-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="64df6-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="64df6-307">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-307">no</span></span>             | <span data-ttu-id="64df6-308">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-308">no</span></span>               |
| <span data-ttu-id="64df6-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="64df6-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="64df6-310">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-310">no</span></span>             | <span data-ttu-id="64df6-311">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-311">no</span></span>               |
| <span data-ttu-id="64df6-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="64df6-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="64df6-313">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-313">no</span></span>             | <span data-ttu-id="64df6-314">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-314">no</span></span>               |
| <span data-ttu-id="64df6-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="64df6-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="64df6-316">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-316">no</span></span>             | <span data-ttu-id="64df6-317">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-317">no</span></span>               |
| <span data-ttu-id="64df6-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="64df6-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="64df6-319">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-319">no</span></span>             | <span data-ttu-id="64df6-320">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-320">no</span></span>               |
| <span data-ttu-id="64df6-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="64df6-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="64df6-322">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-322">no</span></span>             | <span data-ttu-id="64df6-323">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-323">no</span></span>               |
| <span data-ttu-id="64df6-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="64df6-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="64df6-325">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-325">no</span></span>             | <span data-ttu-id="64df6-326">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-326">no</span></span>               |
| <span data-ttu-id="64df6-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="64df6-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="64df6-328">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-328">no</span></span>             | <span data-ttu-id="64df6-329">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-329">no</span></span>               |
| <span data-ttu-id="64df6-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="64df6-330">msdyn_summary</span></span>                          | <span data-ttu-id="64df6-331">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-331">no</span></span>             | <span data-ttu-id="64df6-332">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-332">no</span></span>               |
| <span data-ttu-id="64df6-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="64df6-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="64df6-334">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-334">no</span></span>             | <span data-ttu-id="64df6-335">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-335">no</span></span>               |
| <span data-ttu-id="64df6-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="64df6-337">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-337">no</span></span>             | <span data-ttu-id="64df6-338">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="64df6-339">Projekta uzdevuma atkarība</span><span class="sxs-lookup"><span data-stu-id="64df6-339">Project task dependency</span></span>

| <span data-ttu-id="64df6-340">**Loģiskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="64df6-340">**Logical name**</span></span>              | <span data-ttu-id="64df6-341">**Var izveidot**</span><span class="sxs-lookup"><span data-stu-id="64df6-341">**Can create**</span></span> | <span data-ttu-id="64df6-342">**Var rediģēt**</span><span class="sxs-lookup"><span data-stu-id="64df6-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="64df6-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="64df6-343">msdyn_linktype</span></span>                | <span data-ttu-id="64df6-344">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-344">no</span></span>             | <span data-ttu-id="64df6-345">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-345">no</span></span>           |
| <span data-ttu-id="64df6-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="64df6-346">msdyn_linktypename</span></span>            | <span data-ttu-id="64df6-347">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-347">no</span></span>             | <span data-ttu-id="64df6-348">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-348">no</span></span>           |
| <span data-ttu-id="64df6-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="64df6-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="64df6-350">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-350">yes</span></span>            | <span data-ttu-id="64df6-351">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-351">no</span></span>           |
| <span data-ttu-id="64df6-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="64df6-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="64df6-353">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-353">yes</span></span>            | <span data-ttu-id="64df6-354">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-354">no</span></span>           |
| <span data-ttu-id="64df6-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="64df6-355">msdyn_project</span></span>                 | <span data-ttu-id="64df6-356">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-356">yes</span></span>            | <span data-ttu-id="64df6-357">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-357">no</span></span>           |
| <span data-ttu-id="64df6-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="64df6-358">msdyn_projectname</span></span>             | <span data-ttu-id="64df6-359">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-359">yes</span></span>            | <span data-ttu-id="64df6-360">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-360">no</span></span>           |
| <span data-ttu-id="64df6-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="64df6-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="64df6-362">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-362">yes</span></span>            | <span data-ttu-id="64df6-363">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-363">no</span></span>           |
| <span data-ttu-id="64df6-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="64df6-364">msdyn_successortask</span></span>           | <span data-ttu-id="64df6-365">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-365">yes</span></span>            | <span data-ttu-id="64df6-366">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-366">no</span></span>           |
| <span data-ttu-id="64df6-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="64df6-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="64df6-368">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-368">yes</span></span>            | <span data-ttu-id="64df6-369">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="64df6-370">Resursu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="64df6-370">Resource assignment</span></span>

| <span data-ttu-id="64df6-371">**Loģiskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="64df6-371">**Logical name**</span></span>             | <span data-ttu-id="64df6-372">**Var izveidot**</span><span class="sxs-lookup"><span data-stu-id="64df6-372">**Can create**</span></span> | <span data-ttu-id="64df6-373">**Var rediģēt**</span><span class="sxs-lookup"><span data-stu-id="64df6-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="64df6-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="64df6-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="64df6-375">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-375">yes</span></span>            | <span data-ttu-id="64df6-376">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-376">no</span></span>           |
| <span data-ttu-id="64df6-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="64df6-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="64df6-378">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-378">yes</span></span>            | <span data-ttu-id="64df6-379">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-379">no</span></span>           |
| <span data-ttu-id="64df6-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="64df6-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="64df6-381">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-381">no</span></span>             | <span data-ttu-id="64df6-382">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-382">no</span></span>           |
| <span data-ttu-id="64df6-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="64df6-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="64df6-384">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-384">no</span></span>             | <span data-ttu-id="64df6-385">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-385">no</span></span>           |
| <span data-ttu-id="64df6-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="64df6-386">msdyn_committype</span></span>             | <span data-ttu-id="64df6-387">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-387">no</span></span>             | <span data-ttu-id="64df6-388">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-388">no</span></span>           |
| <span data-ttu-id="64df6-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="64df6-389">msdyn_committypename</span></span>         | <span data-ttu-id="64df6-390">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-390">no</span></span>             | <span data-ttu-id="64df6-391">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-391">no</span></span>           |
| <span data-ttu-id="64df6-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="64df6-392">msdyn_effort</span></span>                 | <span data-ttu-id="64df6-393">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-393">no</span></span>             | <span data-ttu-id="64df6-394">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-394">no</span></span>           |
| <span data-ttu-id="64df6-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="64df6-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="64df6-396">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-396">no</span></span>             | <span data-ttu-id="64df6-397">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-397">no</span></span>           |
| <span data-ttu-id="64df6-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="64df6-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="64df6-399">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-399">no</span></span>             | <span data-ttu-id="64df6-400">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-400">no</span></span>           |
| <span data-ttu-id="64df6-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="64df6-401">msdyn_finish</span></span>                 | <span data-ttu-id="64df6-402">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-402">no</span></span>             | <span data-ttu-id="64df6-403">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-403">no</span></span>           |
| <span data-ttu-id="64df6-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="64df6-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="64df6-405">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-405">no</span></span>             | <span data-ttu-id="64df6-406">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-406">no</span></span>           |
| <span data-ttu-id="64df6-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="64df6-408">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-408">no</span></span>             | <span data-ttu-id="64df6-409">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-409">no</span></span>           |
| <span data-ttu-id="64df6-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="64df6-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="64df6-411">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-411">no</span></span>             | <span data-ttu-id="64df6-412">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-412">no</span></span>           |
| <span data-ttu-id="64df6-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="64df6-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="64df6-414">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-414">no</span></span>             | <span data-ttu-id="64df6-415">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-415">no</span></span>           |
| <span data-ttu-id="64df6-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="64df6-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="64df6-417">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-417">no</span></span>             | <span data-ttu-id="64df6-418">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-418">no</span></span>           |
| <span data-ttu-id="64df6-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="64df6-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="64df6-420">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-420">no</span></span>             | <span data-ttu-id="64df6-421">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-421">no</span></span>           |
| <span data-ttu-id="64df6-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="64df6-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="64df6-423">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-423">no</span></span>             | <span data-ttu-id="64df6-424">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-424">no</span></span>           |
| <span data-ttu-id="64df6-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="64df6-425">msdyn_projectid</span></span>              | <span data-ttu-id="64df6-426">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-426">yes</span></span>            | <span data-ttu-id="64df6-427">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-427">no</span></span>           |
| <span data-ttu-id="64df6-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="64df6-428">msdyn_projectidname</span></span>          | <span data-ttu-id="64df6-429">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-429">no</span></span>             | <span data-ttu-id="64df6-430">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-430">no</span></span>           |
| <span data-ttu-id="64df6-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="64df6-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="64df6-432">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-432">no</span></span>             | <span data-ttu-id="64df6-433">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-433">no</span></span>           |
| <span data-ttu-id="64df6-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="64df6-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="64df6-435">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-435">no</span></span>             | <span data-ttu-id="64df6-436">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-436">no</span></span>           |
| <span data-ttu-id="64df6-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="64df6-437">msdyn_start</span></span>                  | <span data-ttu-id="64df6-438">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-438">no</span></span>             | <span data-ttu-id="64df6-439">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-439">no</span></span>           |
| <span data-ttu-id="64df6-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="64df6-440">msdyn_taskid</span></span>                 | <span data-ttu-id="64df6-441">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-441">no</span></span>             | <span data-ttu-id="64df6-442">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-442">no</span></span>           |
| <span data-ttu-id="64df6-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="64df6-443">msdyn_taskidname</span></span>             | <span data-ttu-id="64df6-444">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-444">no</span></span>             | <span data-ttu-id="64df6-445">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-445">no</span></span>           |
| <span data-ttu-id="64df6-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="64df6-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="64df6-447">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-447">no</span></span>             | <span data-ttu-id="64df6-448">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="64df6-449">Projekta darba grupas dalībnieks</span><span class="sxs-lookup"><span data-stu-id="64df6-449">Project team member</span></span>

| <span data-ttu-id="64df6-450">**Loģiskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="64df6-450">**Logical name**</span></span>                                 | <span data-ttu-id="64df6-451">**Var izveidot**</span><span class="sxs-lookup"><span data-stu-id="64df6-451">**Can create**</span></span> | <span data-ttu-id="64df6-452">**Var rediģēt**</span><span class="sxs-lookup"><span data-stu-id="64df6-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="64df6-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="64df6-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="64df6-454">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-454">no</span></span>             | <span data-ttu-id="64df6-455">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-455">no</span></span>           |
| <span data-ttu-id="64df6-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="64df6-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="64df6-457">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-457">no</span></span>             | <span data-ttu-id="64df6-458">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-458">no</span></span>           |
| <span data-ttu-id="64df6-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="64df6-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="64df6-460">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-460">no</span></span>             | <span data-ttu-id="64df6-461">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-461">no</span></span>           |
| <span data-ttu-id="64df6-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="64df6-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="64df6-463">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-463">no</span></span>             | <span data-ttu-id="64df6-464">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-464">no</span></span>           |
| <span data-ttu-id="64df6-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="64df6-465">msdyn_effort</span></span>                                     | <span data-ttu-id="64df6-466">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-466">no</span></span>             | <span data-ttu-id="64df6-467">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-467">no</span></span>           |
| <span data-ttu-id="64df6-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="64df6-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="64df6-469">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-469">no</span></span>             | <span data-ttu-id="64df6-470">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-470">no</span></span>           |
| <span data-ttu-id="64df6-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="64df6-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="64df6-472">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-472">no</span></span>             | <span data-ttu-id="64df6-473">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-473">no</span></span>           |
| <span data-ttu-id="64df6-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="64df6-474">msdyn_finish</span></span>                                     | <span data-ttu-id="64df6-475">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-475">no</span></span>             | <span data-ttu-id="64df6-476">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-476">no</span></span>           |
| <span data-ttu-id="64df6-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="64df6-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="64df6-478">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-478">no</span></span>             | <span data-ttu-id="64df6-479">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-479">no</span></span>           |
| <span data-ttu-id="64df6-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="64df6-480">msdyn_hours</span></span>                                      | <span data-ttu-id="64df6-481">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-481">no</span></span>             | <span data-ttu-id="64df6-482">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-482">no</span></span>           |
| <span data-ttu-id="64df6-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="64df6-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="64df6-484">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-484">no</span></span>             | <span data-ttu-id="64df6-485">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-485">no</span></span>           |
| <span data-ttu-id="64df6-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="64df6-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="64df6-487">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-487">no</span></span>             | <span data-ttu-id="64df6-488">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-488">no</span></span>           |
| <span data-ttu-id="64df6-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="64df6-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="64df6-490">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-490">no</span></span>             | <span data-ttu-id="64df6-491">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-491">no</span></span>           |
| <span data-ttu-id="64df6-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="64df6-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="64df6-493">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-493">no</span></span>             | <span data-ttu-id="64df6-494">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-494">no</span></span>           |
| <span data-ttu-id="64df6-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="64df6-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="64df6-496">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-496">no</span></span>             | <span data-ttu-id="64df6-497">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-497">no</span></span>           |
| <span data-ttu-id="64df6-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="64df6-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="64df6-499">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-499">no</span></span>             | <span data-ttu-id="64df6-500">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-500">no</span></span>           |
| <span data-ttu-id="64df6-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="64df6-501">msdyn_start</span></span>                                      | <span data-ttu-id="64df6-502">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-502">no</span></span>             | <span data-ttu-id="64df6-503">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="64df6-504">Project</span><span class="sxs-lookup"><span data-stu-id="64df6-504">Project</span></span>

| <span data-ttu-id="64df6-505">**Loģiskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="64df6-505">**Logical name**</span></span>                       | <span data-ttu-id="64df6-506">**Var izveidot**</span><span class="sxs-lookup"><span data-stu-id="64df6-506">**Can create**</span></span> | <span data-ttu-id="64df6-507">**Var rediģēt**</span><span class="sxs-lookup"><span data-stu-id="64df6-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="64df6-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="64df6-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="64df6-509">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-509">no</span></span>             | <span data-ttu-id="64df6-510">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-510">no</span></span>           |
| <span data-ttu-id="64df6-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="64df6-512">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-512">no</span></span>             | <span data-ttu-id="64df6-513">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-513">no</span></span>           |
| <span data-ttu-id="64df6-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="64df6-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="64df6-515">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-515">no</span></span>             | <span data-ttu-id="64df6-516">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-516">no</span></span>           |
| <span data-ttu-id="64df6-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="64df6-518">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-518">no</span></span>             | <span data-ttu-id="64df6-519">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-519">no</span></span>           |
| <span data-ttu-id="64df6-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="64df6-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="64df6-521">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-521">no</span></span>             | <span data-ttu-id="64df6-522">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-522">no</span></span>           |
| <span data-ttu-id="64df6-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="64df6-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="64df6-524">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-524">no</span></span>             | <span data-ttu-id="64df6-525">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-525">no</span></span>           |
| <span data-ttu-id="64df6-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="64df6-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="64df6-527">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-527">yes</span></span>            | <span data-ttu-id="64df6-528">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-528">no</span></span>           |
| <span data-ttu-id="64df6-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="64df6-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="64df6-530">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-530">yes</span></span>            | <span data-ttu-id="64df6-531">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-531">no</span></span>           |
| <span data-ttu-id="64df6-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="64df6-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="64df6-533">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-533">yes</span></span>            | <span data-ttu-id="64df6-534">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-534">no</span></span>           |
| <span data-ttu-id="64df6-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="64df6-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="64df6-536">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-536">no</span></span>             | <span data-ttu-id="64df6-537">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-537">no</span></span>           |
| <span data-ttu-id="64df6-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="64df6-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="64df6-539">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-539">no</span></span>             | <span data-ttu-id="64df6-540">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-540">no</span></span>           |
| <span data-ttu-id="64df6-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="64df6-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="64df6-542">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-542">no</span></span>             | <span data-ttu-id="64df6-543">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-543">no</span></span>           |
| <span data-ttu-id="64df6-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="64df6-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="64df6-545">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-545">no</span></span>             | <span data-ttu-id="64df6-546">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-546">no</span></span>           |
| <span data-ttu-id="64df6-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="64df6-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="64df6-548">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-548">no</span></span>             | <span data-ttu-id="64df6-549">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-549">no</span></span>           |
| <span data-ttu-id="64df6-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="64df6-550">msdyn_duration</span></span>                         | <span data-ttu-id="64df6-551">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-551">no</span></span>             | <span data-ttu-id="64df6-552">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-552">no</span></span>           |
| <span data-ttu-id="64df6-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="64df6-553">msdyn_effort</span></span>                           | <span data-ttu-id="64df6-554">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-554">no</span></span>             | <span data-ttu-id="64df6-555">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-555">no</span></span>           |
| <span data-ttu-id="64df6-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="64df6-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="64df6-557">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-557">no</span></span>             | <span data-ttu-id="64df6-558">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-558">no</span></span>           |
| <span data-ttu-id="64df6-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="64df6-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="64df6-560">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-560">no</span></span>             | <span data-ttu-id="64df6-561">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-561">no</span></span>           |
| <span data-ttu-id="64df6-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="64df6-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="64df6-563">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-563">no</span></span>             | <span data-ttu-id="64df6-564">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-564">no</span></span>           |
| <span data-ttu-id="64df6-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="64df6-565">msdyn_finish</span></span>                           | <span data-ttu-id="64df6-566">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-566">yes</span></span>            | <span data-ttu-id="64df6-567">jā</span><span class="sxs-lookup"><span data-stu-id="64df6-567">yes</span></span>          |
| <span data-ttu-id="64df6-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="64df6-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="64df6-569">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-569">no</span></span>             | <span data-ttu-id="64df6-570">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-570">no</span></span>           |
| <span data-ttu-id="64df6-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="64df6-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="64df6-572">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-572">no</span></span>             | <span data-ttu-id="64df6-573">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-573">no</span></span>           |
| <span data-ttu-id="64df6-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="64df6-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="64df6-575">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-575">no</span></span>             | <span data-ttu-id="64df6-576">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-576">no</span></span>           |
| <span data-ttu-id="64df6-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="64df6-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="64df6-578">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-578">no</span></span>             | <span data-ttu-id="64df6-579">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-579">no</span></span>           |
| <span data-ttu-id="64df6-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="64df6-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="64df6-581">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-581">no</span></span>             | <span data-ttu-id="64df6-582">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-582">no</span></span>           |
| <span data-ttu-id="64df6-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="64df6-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="64df6-584">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-584">no</span></span>             | <span data-ttu-id="64df6-585">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-585">no</span></span>           |
| <span data-ttu-id="64df6-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="64df6-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="64df6-587">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-587">no</span></span>             | <span data-ttu-id="64df6-588">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-588">no</span></span>           |
| <span data-ttu-id="64df6-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="64df6-590">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-590">no</span></span>             | <span data-ttu-id="64df6-591">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-591">no</span></span>           |
| <span data-ttu-id="64df6-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="64df6-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="64df6-593">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-593">no</span></span>             | <span data-ttu-id="64df6-594">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-594">no</span></span>           |
| <span data-ttu-id="64df6-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="64df6-596">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-596">no</span></span>             | <span data-ttu-id="64df6-597">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-597">no</span></span>           |
| <span data-ttu-id="64df6-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="64df6-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="64df6-599">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-599">no</span></span>             | <span data-ttu-id="64df6-600">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-600">no</span></span>           |
| <span data-ttu-id="64df6-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="64df6-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="64df6-602">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-602">no</span></span>             | <span data-ttu-id="64df6-603">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-603">no</span></span>           |
| <span data-ttu-id="64df6-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="64df6-604">msdyn_progress</span></span>                         | <span data-ttu-id="64df6-605">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-605">no</span></span>             | <span data-ttu-id="64df6-606">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-606">no</span></span>           |
| <span data-ttu-id="64df6-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="64df6-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="64df6-608">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-608">no</span></span>             | <span data-ttu-id="64df6-609">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-609">no</span></span>           |
| <span data-ttu-id="64df6-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="64df6-611">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-611">no</span></span>             | <span data-ttu-id="64df6-612">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-612">no</span></span>           |
| <span data-ttu-id="64df6-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="64df6-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="64df6-614">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-614">no</span></span>             | <span data-ttu-id="64df6-615">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-615">no</span></span>           |
| <span data-ttu-id="64df6-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="64df6-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="64df6-617">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-617">no</span></span>             | <span data-ttu-id="64df6-618">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-618">no</span></span>           |
| <span data-ttu-id="64df6-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="64df6-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="64df6-620">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-620">no</span></span>             | <span data-ttu-id="64df6-621">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-621">no</span></span>           |
| <span data-ttu-id="64df6-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="64df6-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="64df6-623">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-623">no</span></span>             | <span data-ttu-id="64df6-624">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-624">no</span></span>           |
| <span data-ttu-id="64df6-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="64df6-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="64df6-626">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-626">no</span></span>             | <span data-ttu-id="64df6-627">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-627">no</span></span>           |
| <span data-ttu-id="64df6-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="64df6-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="64df6-629">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-629">no</span></span>             | <span data-ttu-id="64df6-630">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-630">no</span></span>           |
| <span data-ttu-id="64df6-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="64df6-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="64df6-632">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-632">no</span></span>             | <span data-ttu-id="64df6-633">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-633">no</span></span>           |
| <span data-ttu-id="64df6-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="64df6-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="64df6-635">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-635">no</span></span>             | <span data-ttu-id="64df6-636">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-636">no</span></span>           |
| <span data-ttu-id="64df6-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="64df6-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="64df6-638">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-638">no</span></span>             | <span data-ttu-id="64df6-639">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-639">no</span></span>           |
| <span data-ttu-id="64df6-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="64df6-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="64df6-641">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-641">no</span></span>             | <span data-ttu-id="64df6-642">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-642">no</span></span>           |
| <span data-ttu-id="64df6-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="64df6-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="64df6-644">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-644">no</span></span>             | <span data-ttu-id="64df6-645">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-645">no</span></span>           |
| <span data-ttu-id="64df6-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="64df6-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="64df6-647">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-647">no</span></span>             | <span data-ttu-id="64df6-648">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-648">no</span></span>           |
| <span data-ttu-id="64df6-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="64df6-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="64df6-650">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-650">no</span></span>             | <span data-ttu-id="64df6-651">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-651">no</span></span>           |
| <span data-ttu-id="64df6-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="64df6-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="64df6-653">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-653">no</span></span>             | <span data-ttu-id="64df6-654">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-654">no</span></span>           |
| <span data-ttu-id="64df6-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="64df6-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="64df6-656">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-656">no</span></span>             | <span data-ttu-id="64df6-657">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-657">no</span></span>           |
| <span data-ttu-id="64df6-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="64df6-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="64df6-659">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-659">no</span></span>             | <span data-ttu-id="64df6-660">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-660">no</span></span>           |
| <span data-ttu-id="64df6-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="64df6-662">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-662">no</span></span>             | <span data-ttu-id="64df6-663">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-663">no</span></span>           |
| <span data-ttu-id="64df6-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="64df6-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="64df6-665">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-665">no</span></span>             | <span data-ttu-id="64df6-666">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-666">no</span></span>           |
| <span data-ttu-id="64df6-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="64df6-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="64df6-668">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-668">no</span></span>             | <span data-ttu-id="64df6-669">nē</span><span class="sxs-lookup"><span data-stu-id="64df6-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="64df6-670">Zināmās problēmas un ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="64df6-670">Limitations and known issues</span></span>
<span data-ttu-id="64df6-671">Tālāk ir saraksts ar ierobežojumiem un zināmajām problēmām.</span><span class="sxs-lookup"><span data-stu-id="64df6-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="64df6-672">Plānošanas API var izmantot tikai **lietotāji ar Microsoft Project License.**</span><span class="sxs-lookup"><span data-stu-id="64df6-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="64df6-673">Tos nevar izmantot tālāk minētie lietotāji.</span><span class="sxs-lookup"><span data-stu-id="64df6-673">They can't be used by:</span></span>
    - <span data-ttu-id="64df6-674">Programmas lietotāji</span><span class="sxs-lookup"><span data-stu-id="64df6-674">Application users</span></span>
    - <span data-ttu-id="64df6-675">Sistēmas lietotāji</span><span class="sxs-lookup"><span data-stu-id="64df6-675">System users</span></span>
    - <span data-ttu-id="64df6-676">Integrācijas lietotāji</span><span class="sxs-lookup"><span data-stu-id="64df6-676">Integration users</span></span>
    - <span data-ttu-id="64df6-677">Citi lietotāji, kuriem nav nepieciešamās licences</span><span class="sxs-lookup"><span data-stu-id="64df6-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="64df6-678">Katrai **OperationSet** var būt ne vairāk par 100 operācijām.</span><span class="sxs-lookup"><span data-stu-id="64df6-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="64df6-679">Katram lietotājam var būt ne vairāk par 10 atvērtām **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="64df6-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="64df6-680">Project Operations pašlaik atbalsta ne vairāk kā 500 uzdevumu vienā projektā.</span><span class="sxs-lookup"><span data-stu-id="64df6-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="64df6-681">**OperationSet** kļūmes statusa un kļūmju žurnāli pašlaik nav pieejami.</span><span class="sxs-lookup"><span data-stu-id="64df6-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="64df6-682">Plānošanas API ir publiskā priekšskatījumā.</span><span class="sxs-lookup"><span data-stu-id="64df6-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="64df6-683">Korporācija Microsoft neatbalsta šo API izmantošana ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="64df6-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="64df6-684">Projektu un uzdevumu ierobežojumi un robežas</span><span class="sxs-lookup"><span data-stu-id="64df6-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="64df6-685">Kļūdu apstrāde</span><span class="sxs-lookup"><span data-stu-id="64df6-685">Error handling</span></span>

   - <span data-ttu-id="64df6-686">Lai pārskatītu operāciju kopās ģenerētās kļūdas, atveriet sadaļu **Iestatījumi** \> **Plānot integrāciju** \> **Operāciju kopas**.</span><span class="sxs-lookup"><span data-stu-id="64df6-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="64df6-687">Lai pārskatītu Project Scheduling Service ģenerētās kļūdas, atveriet sadaļu **Iestatījumi** \> **Plānot integrāciju** \> **PSS kļūdu žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="64df6-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="64df6-688">Scenārija paraugs</span><span class="sxs-lookup"><span data-stu-id="64df6-688">Sample scenario</span></span>

<span data-ttu-id="64df6-689">Šādā scenārijā jums būs jāizveido projekts, darba grupas dalībnieks, četri uzdevumi un divi resursu piešķīrumi.</span><span class="sxs-lookup"><span data-stu-id="64df6-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="64df6-690">Pēc tam jūs atjaunināsiet vienu uzdevumu, atjaunināsiet projektu, izdzēsiet vienu uzdevumu, izdzēsiet vienu resursa piešķīrumu un izveidosiet uzdevuma atkarību.</span><span class="sxs-lookup"><span data-stu-id="64df6-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="64df6-691">Papildu paraugi</span><span class="sxs-lookup"><span data-stu-id="64df6-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
