---
title: Plānošanas API izmantošana operāciju veikšanai ar plānošanas entītijām
description: Šajā tēmā ir sniegta informācija un piemēri plānošanas API izmantošanai.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116806"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="7d1fa-103">Plānošanas API izmantošana operāciju veikšanai ar plānošanas entītijām</span><span class="sxs-lookup"><span data-stu-id="7d1fa-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="7d1fa-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="7d1fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="7d1fa-105">Daļa vai visa šajā tēmā norādītā funkcionalitāte ir pieejama lietotājiem kā daļa no priekšskatījuma laidiena.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="7d1fa-106">Saturs un funkcionalitāte var mainīties.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="7d1fa-107">Plānošanas entītijas</span><span class="sxs-lookup"><span data-stu-id="7d1fa-107">Scheduling entities</span></span>

<span data-ttu-id="7d1fa-108">Plānošanas API nodrošina iespēju veikt izveides, atjaunināšanas un dzēšanas operācijas ar **plānošanas entītijām**.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="7d1fa-109">Šīs entītijas tiek pārvaldītas, izmantojot projekta tīmekļa plānošanas programmu.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="7d1fa-110">Iepriekšējos Dynamics 365 Project Operations laidienos tika ierobežotas izveides, atjaunināšanas un dzēšanas operācijas ar **plānošanas entītijām**.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="7d1fa-111">Tālāk sniegtajā tabulā ir sniegts pilnīgs **plānošanas entītiju** saraksts.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="7d1fa-112">Entītijas nosaukums</span><span class="sxs-lookup"><span data-stu-id="7d1fa-112">Entity name</span></span>  | <span data-ttu-id="7d1fa-113">Entītijas loģiskais nosaukums</span><span class="sxs-lookup"><span data-stu-id="7d1fa-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="7d1fa-114">Project</span><span class="sxs-lookup"><span data-stu-id="7d1fa-114">Project</span></span> | <span data-ttu-id="7d1fa-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="7d1fa-115">msdyn_project</span></span> |
| <span data-ttu-id="7d1fa-116">Projekta uzdevums</span><span class="sxs-lookup"><span data-stu-id="7d1fa-116">Project Task</span></span>  | <span data-ttu-id="7d1fa-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="7d1fa-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="7d1fa-118">Projekta uzdevuma atkarība</span><span class="sxs-lookup"><span data-stu-id="7d1fa-118">Project Task Dependency</span></span>  | <span data-ttu-id="7d1fa-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="7d1fa-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="7d1fa-120">Resursu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="7d1fa-120">Resource Assignment</span></span> | <span data-ttu-id="7d1fa-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="7d1fa-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="7d1fa-122">Projekta bloks</span><span class="sxs-lookup"><span data-stu-id="7d1fa-122">Project Bucket</span></span>  | <span data-ttu-id="7d1fa-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="7d1fa-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="7d1fa-124">Projekta grupas dalībnieks</span><span class="sxs-lookup"><span data-stu-id="7d1fa-124">Project Team Member</span></span> | <span data-ttu-id="7d1fa-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="7d1fa-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="7d1fa-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="7d1fa-126">OperationSet</span></span>

<span data-ttu-id="7d1fa-127">OperationSet ir darba vienības shēma, ko var izmantot, kad transakcijā ir jāapstrādā vairāki plānošanas ietekmēšanas pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="7d1fa-128">Plānošanas API</span><span class="sxs-lookup"><span data-stu-id="7d1fa-128">Schedule APIs</span></span>

<span data-ttu-id="7d1fa-129">Tālāk ir saraksts ar pašreizējiem plānošanas API.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="7d1fa-130">**msdyn_CreateProjectV1**: šo API var izmantot, lai izveidotu projektu.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="7d1fa-131">Nekavējoties tiek izveidots projekts un noklusējuma projekta bloks.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="7d1fa-132">**msdyn_CreateTeamMemberV1**: šo API var izmantot, lai izveidotu projekta darba grupas dalībnieku.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="7d1fa-133">Darba grupas dalībnieka ieraksts tiek izveidots nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="7d1fa-134">**msdyn_CreateOperationSetV1**: šo API var izmantot, lai ieplānotu vairākus pieprasījumus, kas jāveic transakcijā.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="7d1fa-135">**msdyn_PSSCreateV1**: šo API var izmantot, lai izveidotu entītiju.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="7d1fa-136">Entītija var būt jebkura no plānošanas entītijām, kas atbalsta izveides operāciju.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="7d1fa-137">**msdyn_PSSUpdateV1**: šo API var izmantot, lai atjauninātu entītiju.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="7d1fa-138">Entītija var būt jebkura no plānošanas entītijām, kas atbalsta atjaunināšanas operāciju.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="7d1fa-139">**msdyn_PSSDeleteV1**: šo API var izmantot, lai dzēstu entītiju.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="7d1fa-140">Entītija var būt jebkura no plānošanas entītijām, kas atbalsta dzēšanas operāciju.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="7d1fa-141">**msdyn_ExecuteOperationSetV1**: šis API tiek izmantots, lai izpildītu visas operācijas attiecīgajā operāciju kopā.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="7d1fa-142">Plānošanas API izmantošana ar OperationSet</span><span class="sxs-lookup"><span data-stu-id="7d1fa-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="7d1fa-143">Tā kā ieraksti, kuriem ir gan **CreateProjectV1**, gan **CreateTeamMemberV1**, tiek izveidoti nekavējoties, šos API nevar izmantot tieši kopā **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="7d1fa-144">Tomēr API var lietot, lai izveidotu nepieciešamos ierakstus, izveidotu **OperationSet** un pēc tam izmantotu šos iepriekš izveidotos ierakstus kopā **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="7d1fa-145">Atbalstītās operācijas</span><span class="sxs-lookup"><span data-stu-id="7d1fa-145">Supported operations</span></span>

| <span data-ttu-id="7d1fa-146">Plānošanas entītija</span><span class="sxs-lookup"><span data-stu-id="7d1fa-146">Scheduling entity</span></span> | <span data-ttu-id="7d1fa-147">Izveide</span><span class="sxs-lookup"><span data-stu-id="7d1fa-147">Create</span></span> | <span data-ttu-id="7d1fa-148">Atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="7d1fa-148">Update</span></span> | <span data-ttu-id="7d1fa-149">Delete</span><span class="sxs-lookup"><span data-stu-id="7d1fa-149">Delete</span></span> | <span data-ttu-id="7d1fa-150">Svarīgi ieteikumi</span><span class="sxs-lookup"><span data-stu-id="7d1fa-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="7d1fa-151">Projekta uzdevums</span><span class="sxs-lookup"><span data-stu-id="7d1fa-151">Project task</span></span> | <span data-ttu-id="7d1fa-152">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-152">Yes</span></span> | <span data-ttu-id="7d1fa-153">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-153">Yes</span></span> | <span data-ttu-id="7d1fa-154">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-154">Yes</span></span> | <span data-ttu-id="7d1fa-155">Nevienu</span><span class="sxs-lookup"><span data-stu-id="7d1fa-155">None</span></span> |
| <span data-ttu-id="7d1fa-156">Projekta uzdevuma atkarība</span><span class="sxs-lookup"><span data-stu-id="7d1fa-156">Project task dependency</span></span> | <span data-ttu-id="7d1fa-157">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-157">Yes</span></span> | <span data-ttu-id="7d1fa-158">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-158">Yes</span></span> | | <span data-ttu-id="7d1fa-159">Projekta uzdevumu atkarības ieraksti netiek atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="7d1fa-160">Tā vietā var izdzēst veco ierakstu un izveidot jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="7d1fa-161">Resursu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="7d1fa-161">Resource assignment</span></span> | <span data-ttu-id="7d1fa-162">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-162">Yes</span></span> | <span data-ttu-id="7d1fa-163">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-163">Yes</span></span> | | <span data-ttu-id="7d1fa-164">Netiek atbalstītas operācijas ar šādiem laukiem: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** un **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="7d1fa-165">Resursu piešķiršanas ieraksti netiek atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="7d1fa-166">Tā vietā var izdzēst veco ierakstu un izveidot jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="7d1fa-167">Projekta bloks</span><span class="sxs-lookup"><span data-stu-id="7d1fa-167">Project bucket</span></span> | <span data-ttu-id="7d1fa-168">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="7d1fa-168">N/A</span></span> | <span data-ttu-id="7d1fa-169">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="7d1fa-169">N/A</span></span> | <span data-ttu-id="7d1fa-170">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="7d1fa-170">N/A</span></span> | <span data-ttu-id="7d1fa-171">Noklusējuma bloks tiek izveidots, izmantojot **CreateProjectV1** API.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="7d1fa-172">Projekta darba grupas dalībnieks</span><span class="sxs-lookup"><span data-stu-id="7d1fa-172">Project team member</span></span> | <span data-ttu-id="7d1fa-173">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-173">Yes</span></span> | <span data-ttu-id="7d1fa-174">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-174">Yes</span></span> | <span data-ttu-id="7d1fa-175">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-175">Yes</span></span> | <span data-ttu-id="7d1fa-176">Izveides operācijai izmantojiet **CreateTeamMemberV1** API.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="7d1fa-177">Project</span><span class="sxs-lookup"><span data-stu-id="7d1fa-177">Project</span></span> | <span data-ttu-id="7d1fa-178">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-178">Yes</span></span> | <span data-ttu-id="7d1fa-179">Jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-179">Yes</span></span> | <span data-ttu-id="7d1fa-180">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="7d1fa-180">N/A</span></span> | <span data-ttu-id="7d1fa-181">Netiek atbalstītas operācijas ar šādiem laukiem: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** un **Duration**.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="7d1fa-182">Šos API var izsaukt ar entītijas objektiem, kuros ir pielāgoti lauki.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="7d1fa-183">Rekvizīts ID nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-183">The ID property is optional.</span></span> <span data-ttu-id="7d1fa-184">Ja tas ir nodrošināts, sistēma mēģina to izmantot un rodas izņēmums, ja to nevar izmantot.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="7d1fa-185">Ja tas nav nodrošināts, sistēma to ģenerēs.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="7d1fa-186">Ierobežotie lauki</span><span class="sxs-lookup"><span data-stu-id="7d1fa-186">Restricted fields</span></span>

<span data-ttu-id="7d1fa-187">Tālāk redzamajās tabulās ir definēti lauki, kuriem ir **Izveidot** un **Rediģēt** ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="7d1fa-188">Projekta uzdevums</span><span class="sxs-lookup"><span data-stu-id="7d1fa-188">Project task</span></span>

| <span data-ttu-id="7d1fa-189">**Loģiskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-189">**Logical name**</span></span>                       | <span data-ttu-id="7d1fa-190">**Var izveidot**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-190">**Can create**</span></span> | <span data-ttu-id="7d1fa-191">**Var rediģēt**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="7d1fa-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="7d1fa-193">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-193">no</span></span>             | <span data-ttu-id="7d1fa-194">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-194">no</span></span>               |
| <span data-ttu-id="7d1fa-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="7d1fa-196">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-196">no</span></span>             | <span data-ttu-id="7d1fa-197">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-197">no</span></span>               |
| <span data-ttu-id="7d1fa-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="7d1fa-198">msdyn_actualend</span></span>                        | <span data-ttu-id="7d1fa-199">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-199">no</span></span>             | <span data-ttu-id="7d1fa-200">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-200">no</span></span>               |
| <span data-ttu-id="7d1fa-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="7d1fa-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="7d1fa-202">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-202">no</span></span>             | <span data-ttu-id="7d1fa-203">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-203">no</span></span>               |
| <span data-ttu-id="7d1fa-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="7d1fa-205">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-205">no</span></span>             | <span data-ttu-id="7d1fa-206">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-206">no</span></span>               |
| <span data-ttu-id="7d1fa-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="7d1fa-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="7d1fa-208">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-208">no</span></span>             | <span data-ttu-id="7d1fa-209">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-209">no</span></span>               |
| <span data-ttu-id="7d1fa-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="7d1fa-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="7d1fa-211">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-211">no</span></span>             | <span data-ttu-id="7d1fa-212">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-212">no</span></span>               |
| <span data-ttu-id="7d1fa-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="7d1fa-214">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-214">no</span></span>             | <span data-ttu-id="7d1fa-215">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-215">no</span></span>               |
| <span data-ttu-id="7d1fa-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="7d1fa-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="7d1fa-217">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-217">no</span></span>             | <span data-ttu-id="7d1fa-218">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-218">no</span></span>               |
| <span data-ttu-id="7d1fa-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7d1fa-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="7d1fa-220">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-220">no</span></span>             | <span data-ttu-id="7d1fa-221">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-221">no</span></span>               |
| <span data-ttu-id="7d1fa-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7d1fa-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="7d1fa-223">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-223">no</span></span>             | <span data-ttu-id="7d1fa-224">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-224">no</span></span>               |
| <span data-ttu-id="7d1fa-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="7d1fa-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="7d1fa-226">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-226">no</span></span>             | <span data-ttu-id="7d1fa-227">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-227">no</span></span>               |
| <span data-ttu-id="7d1fa-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="7d1fa-229">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-229">no</span></span>             | <span data-ttu-id="7d1fa-230">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-230">no</span></span>               |
| <span data-ttu-id="7d1fa-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="7d1fa-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="7d1fa-232">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-232">no</span></span>             | <span data-ttu-id="7d1fa-233">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-233">no</span></span>               |
| <span data-ttu-id="7d1fa-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="7d1fa-235">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-235">no</span></span>             | <span data-ttu-id="7d1fa-236">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-236">no</span></span>               |
| <span data-ttu-id="7d1fa-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="7d1fa-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="7d1fa-238">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-238">no</span></span>             | <span data-ttu-id="7d1fa-239">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-239">no</span></span>               |
| <span data-ttu-id="7d1fa-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="7d1fa-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="7d1fa-241">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-241">no</span></span>             | <span data-ttu-id="7d1fa-242">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-242">no</span></span>               |
| <span data-ttu-id="7d1fa-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="7d1fa-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="7d1fa-244">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-244">no</span></span>             | <span data-ttu-id="7d1fa-245">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-245">no</span></span>               |
| <span data-ttu-id="7d1fa-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="7d1fa-247">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-247">no</span></span>             | <span data-ttu-id="7d1fa-248">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-248">no</span></span>               |
| <span data-ttu-id="7d1fa-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="7d1fa-250">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-250">no</span></span>             | <span data-ttu-id="7d1fa-251">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-251">no</span></span>               |
| <span data-ttu-id="7d1fa-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="7d1fa-253">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-253">no</span></span>             | <span data-ttu-id="7d1fa-254">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-254">no</span></span>               |
| <span data-ttu-id="7d1fa-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="7d1fa-256">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-256">no</span></span>             | <span data-ttu-id="7d1fa-257">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-257">no</span></span>               |
| <span data-ttu-id="7d1fa-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7d1fa-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="7d1fa-259">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-259">no</span></span>             | <span data-ttu-id="7d1fa-260">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-260">no</span></span>               |
| <span data-ttu-id="7d1fa-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="7d1fa-262">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-262">no</span></span>             | <span data-ttu-id="7d1fa-263">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-263">no</span></span>               |
| <span data-ttu-id="7d1fa-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="7d1fa-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="7d1fa-265">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-265">no</span></span>             | <span data-ttu-id="7d1fa-266">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-266">no</span></span>               |
| <span data-ttu-id="7d1fa-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="7d1fa-267">msdyn_progress</span></span>                         | <span data-ttu-id="7d1fa-268">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-268">no</span></span>             | <span data-ttu-id="7d1fa-269">nē (jā P4W)</span><span class="sxs-lookup"><span data-stu-id="7d1fa-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="7d1fa-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="7d1fa-271">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-271">no</span></span>             | <span data-ttu-id="7d1fa-272">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-272">no</span></span>               |
| <span data-ttu-id="7d1fa-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="7d1fa-274">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-274">no</span></span>             | <span data-ttu-id="7d1fa-275">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-275">no</span></span>               |
| <span data-ttu-id="7d1fa-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="7d1fa-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="7d1fa-277">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-277">no</span></span>             | <span data-ttu-id="7d1fa-278">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-278">no</span></span>               |
| <span data-ttu-id="7d1fa-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="7d1fa-280">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-280">no</span></span>             | <span data-ttu-id="7d1fa-281">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-281">no</span></span>               |
| <span data-ttu-id="7d1fa-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="7d1fa-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="7d1fa-283">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-283">no</span></span>             | <span data-ttu-id="7d1fa-284">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-284">no</span></span>               |
| <span data-ttu-id="7d1fa-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="7d1fa-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="7d1fa-286">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-286">no</span></span>             | <span data-ttu-id="7d1fa-287">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-287">no</span></span>               |
| <span data-ttu-id="7d1fa-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="7d1fa-289">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-289">no</span></span>             | <span data-ttu-id="7d1fa-290">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-290">no</span></span>               |
| <span data-ttu-id="7d1fa-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="7d1fa-292">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-292">no</span></span>             | <span data-ttu-id="7d1fa-293">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-293">no</span></span>               |
| <span data-ttu-id="7d1fa-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="7d1fa-295">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-295">no</span></span>             | <span data-ttu-id="7d1fa-296">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-296">no</span></span>               |
| <span data-ttu-id="7d1fa-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="7d1fa-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="7d1fa-298">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-298">no</span></span>             | <span data-ttu-id="7d1fa-299">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-299">no</span></span>               |
| <span data-ttu-id="7d1fa-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7d1fa-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="7d1fa-301">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-301">no</span></span>             | <span data-ttu-id="7d1fa-302">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-302">no</span></span>               |
| <span data-ttu-id="7d1fa-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="7d1fa-304">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-304">no</span></span>             | <span data-ttu-id="7d1fa-305">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-305">no</span></span>               |
| <span data-ttu-id="7d1fa-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="7d1fa-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="7d1fa-307">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-307">no</span></span>             | <span data-ttu-id="7d1fa-308">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-308">no</span></span>               |
| <span data-ttu-id="7d1fa-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="7d1fa-310">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-310">no</span></span>             | <span data-ttu-id="7d1fa-311">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-311">no</span></span>               |
| <span data-ttu-id="7d1fa-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="7d1fa-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="7d1fa-313">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-313">no</span></span>             | <span data-ttu-id="7d1fa-314">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-314">no</span></span>               |
| <span data-ttu-id="7d1fa-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="7d1fa-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="7d1fa-316">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-316">no</span></span>             | <span data-ttu-id="7d1fa-317">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-317">no</span></span>               |
| <span data-ttu-id="7d1fa-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="7d1fa-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="7d1fa-319">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-319">no</span></span>             | <span data-ttu-id="7d1fa-320">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-320">no</span></span>               |
| <span data-ttu-id="7d1fa-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="7d1fa-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="7d1fa-322">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-322">no</span></span>             | <span data-ttu-id="7d1fa-323">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-323">no</span></span>               |
| <span data-ttu-id="7d1fa-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="7d1fa-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="7d1fa-325">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-325">no</span></span>             | <span data-ttu-id="7d1fa-326">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-326">no</span></span>               |
| <span data-ttu-id="7d1fa-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="7d1fa-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="7d1fa-328">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-328">no</span></span>             | <span data-ttu-id="7d1fa-329">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-329">no</span></span>               |
| <span data-ttu-id="7d1fa-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="7d1fa-330">msdyn_summary</span></span>                          | <span data-ttu-id="7d1fa-331">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-331">no</span></span>             | <span data-ttu-id="7d1fa-332">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-332">no</span></span>               |
| <span data-ttu-id="7d1fa-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="7d1fa-334">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-334">no</span></span>             | <span data-ttu-id="7d1fa-335">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-335">no</span></span>               |
| <span data-ttu-id="7d1fa-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="7d1fa-337">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-337">no</span></span>             | <span data-ttu-id="7d1fa-338">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="7d1fa-339">Projekta uzdevuma atkarība</span><span class="sxs-lookup"><span data-stu-id="7d1fa-339">Project task dependency</span></span>

| <span data-ttu-id="7d1fa-340">**Loģiskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-340">**Logical name**</span></span>              | <span data-ttu-id="7d1fa-341">**Var izveidot**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-341">**Can create**</span></span> | <span data-ttu-id="7d1fa-342">**Var rediģēt**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="7d1fa-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="7d1fa-343">msdyn_linktype</span></span>                | <span data-ttu-id="7d1fa-344">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-344">no</span></span>             | <span data-ttu-id="7d1fa-345">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-345">no</span></span>           |
| <span data-ttu-id="7d1fa-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="7d1fa-346">msdyn_linktypename</span></span>            | <span data-ttu-id="7d1fa-347">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-347">no</span></span>             | <span data-ttu-id="7d1fa-348">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-348">no</span></span>           |
| <span data-ttu-id="7d1fa-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="7d1fa-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="7d1fa-350">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-350">yes</span></span>            | <span data-ttu-id="7d1fa-351">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-351">no</span></span>           |
| <span data-ttu-id="7d1fa-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="7d1fa-353">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-353">yes</span></span>            | <span data-ttu-id="7d1fa-354">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-354">no</span></span>           |
| <span data-ttu-id="7d1fa-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="7d1fa-355">msdyn_project</span></span>                 | <span data-ttu-id="7d1fa-356">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-356">yes</span></span>            | <span data-ttu-id="7d1fa-357">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-357">no</span></span>           |
| <span data-ttu-id="7d1fa-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-358">msdyn_projectname</span></span>             | <span data-ttu-id="7d1fa-359">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-359">yes</span></span>            | <span data-ttu-id="7d1fa-360">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-360">no</span></span>           |
| <span data-ttu-id="7d1fa-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="7d1fa-362">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-362">yes</span></span>            | <span data-ttu-id="7d1fa-363">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-363">no</span></span>           |
| <span data-ttu-id="7d1fa-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="7d1fa-364">msdyn_successortask</span></span>           | <span data-ttu-id="7d1fa-365">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-365">yes</span></span>            | <span data-ttu-id="7d1fa-366">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-366">no</span></span>           |
| <span data-ttu-id="7d1fa-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="7d1fa-368">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-368">yes</span></span>            | <span data-ttu-id="7d1fa-369">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="7d1fa-370">Resursu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="7d1fa-370">Resource assignment</span></span>

| <span data-ttu-id="7d1fa-371">**Loģiskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-371">**Logical name**</span></span>             | <span data-ttu-id="7d1fa-372">**Var izveidot**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-372">**Can create**</span></span> | <span data-ttu-id="7d1fa-373">**Var rediģēt**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="7d1fa-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="7d1fa-375">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-375">yes</span></span>            | <span data-ttu-id="7d1fa-376">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-376">no</span></span>           |
| <span data-ttu-id="7d1fa-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="7d1fa-378">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-378">yes</span></span>            | <span data-ttu-id="7d1fa-379">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-379">no</span></span>           |
| <span data-ttu-id="7d1fa-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="7d1fa-381">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-381">no</span></span>             | <span data-ttu-id="7d1fa-382">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-382">no</span></span>           |
| <span data-ttu-id="7d1fa-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="7d1fa-384">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-384">no</span></span>             | <span data-ttu-id="7d1fa-385">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-385">no</span></span>           |
| <span data-ttu-id="7d1fa-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="7d1fa-386">msdyn_committype</span></span>             | <span data-ttu-id="7d1fa-387">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-387">no</span></span>             | <span data-ttu-id="7d1fa-388">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-388">no</span></span>           |
| <span data-ttu-id="7d1fa-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="7d1fa-389">msdyn_committypename</span></span>         | <span data-ttu-id="7d1fa-390">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-390">no</span></span>             | <span data-ttu-id="7d1fa-391">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-391">no</span></span>           |
| <span data-ttu-id="7d1fa-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7d1fa-392">msdyn_effort</span></span>                 | <span data-ttu-id="7d1fa-393">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-393">no</span></span>             | <span data-ttu-id="7d1fa-394">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-394">no</span></span>           |
| <span data-ttu-id="7d1fa-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7d1fa-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="7d1fa-396">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-396">no</span></span>             | <span data-ttu-id="7d1fa-397">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-397">no</span></span>           |
| <span data-ttu-id="7d1fa-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7d1fa-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="7d1fa-399">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-399">no</span></span>             | <span data-ttu-id="7d1fa-400">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-400">no</span></span>           |
| <span data-ttu-id="7d1fa-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7d1fa-401">msdyn_finish</span></span>                 | <span data-ttu-id="7d1fa-402">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-402">no</span></span>             | <span data-ttu-id="7d1fa-403">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-403">no</span></span>           |
| <span data-ttu-id="7d1fa-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="7d1fa-405">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-405">no</span></span>             | <span data-ttu-id="7d1fa-406">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-406">no</span></span>           |
| <span data-ttu-id="7d1fa-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="7d1fa-408">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-408">no</span></span>             | <span data-ttu-id="7d1fa-409">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-409">no</span></span>           |
| <span data-ttu-id="7d1fa-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="7d1fa-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="7d1fa-411">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-411">no</span></span>             | <span data-ttu-id="7d1fa-412">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-412">no</span></span>           |
| <span data-ttu-id="7d1fa-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7d1fa-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="7d1fa-414">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-414">no</span></span>             | <span data-ttu-id="7d1fa-415">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-415">no</span></span>           |
| <span data-ttu-id="7d1fa-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="7d1fa-417">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-417">no</span></span>             | <span data-ttu-id="7d1fa-418">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-418">no</span></span>           |
| <span data-ttu-id="7d1fa-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="7d1fa-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="7d1fa-420">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-420">no</span></span>             | <span data-ttu-id="7d1fa-421">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-421">no</span></span>           |
| <span data-ttu-id="7d1fa-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="7d1fa-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="7d1fa-423">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-423">no</span></span>             | <span data-ttu-id="7d1fa-424">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-424">no</span></span>           |
| <span data-ttu-id="7d1fa-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-425">msdyn_projectid</span></span>              | <span data-ttu-id="7d1fa-426">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-426">yes</span></span>            | <span data-ttu-id="7d1fa-427">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-427">no</span></span>           |
| <span data-ttu-id="7d1fa-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-428">msdyn_projectidname</span></span>          | <span data-ttu-id="7d1fa-429">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-429">no</span></span>             | <span data-ttu-id="7d1fa-430">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-430">no</span></span>           |
| <span data-ttu-id="7d1fa-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="7d1fa-432">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-432">no</span></span>             | <span data-ttu-id="7d1fa-433">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-433">no</span></span>           |
| <span data-ttu-id="7d1fa-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="7d1fa-435">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-435">no</span></span>             | <span data-ttu-id="7d1fa-436">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-436">no</span></span>           |
| <span data-ttu-id="7d1fa-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="7d1fa-437">msdyn_start</span></span>                  | <span data-ttu-id="7d1fa-438">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-438">no</span></span>             | <span data-ttu-id="7d1fa-439">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-439">no</span></span>           |
| <span data-ttu-id="7d1fa-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-440">msdyn_taskid</span></span>                 | <span data-ttu-id="7d1fa-441">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-441">no</span></span>             | <span data-ttu-id="7d1fa-442">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-442">no</span></span>           |
| <span data-ttu-id="7d1fa-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-443">msdyn_taskidname</span></span>             | <span data-ttu-id="7d1fa-444">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-444">no</span></span>             | <span data-ttu-id="7d1fa-445">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-445">no</span></span>           |
| <span data-ttu-id="7d1fa-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="7d1fa-447">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-447">no</span></span>             | <span data-ttu-id="7d1fa-448">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="7d1fa-449">Projekta darba grupas dalībnieks</span><span class="sxs-lookup"><span data-stu-id="7d1fa-449">Project team member</span></span>

| <span data-ttu-id="7d1fa-450">**Loģiskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-450">**Logical name**</span></span>                                 | <span data-ttu-id="7d1fa-451">**Var izveidot**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-451">**Can create**</span></span> | <span data-ttu-id="7d1fa-452">**Var rediģēt**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="7d1fa-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="7d1fa-454">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-454">no</span></span>             | <span data-ttu-id="7d1fa-455">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-455">no</span></span>           |
| <span data-ttu-id="7d1fa-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="7d1fa-457">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-457">no</span></span>             | <span data-ttu-id="7d1fa-458">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-458">no</span></span>           |
| <span data-ttu-id="7d1fa-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="7d1fa-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="7d1fa-460">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-460">no</span></span>             | <span data-ttu-id="7d1fa-461">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-461">no</span></span>           |
| <span data-ttu-id="7d1fa-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="7d1fa-463">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-463">no</span></span>             | <span data-ttu-id="7d1fa-464">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-464">no</span></span>           |
| <span data-ttu-id="7d1fa-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7d1fa-465">msdyn_effort</span></span>                                     | <span data-ttu-id="7d1fa-466">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-466">no</span></span>             | <span data-ttu-id="7d1fa-467">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-467">no</span></span>           |
| <span data-ttu-id="7d1fa-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7d1fa-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="7d1fa-469">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-469">no</span></span>             | <span data-ttu-id="7d1fa-470">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-470">no</span></span>           |
| <span data-ttu-id="7d1fa-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7d1fa-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="7d1fa-472">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-472">no</span></span>             | <span data-ttu-id="7d1fa-473">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-473">no</span></span>           |
| <span data-ttu-id="7d1fa-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7d1fa-474">msdyn_finish</span></span>                                     | <span data-ttu-id="7d1fa-475">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-475">no</span></span>             | <span data-ttu-id="7d1fa-476">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-476">no</span></span>           |
| <span data-ttu-id="7d1fa-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="7d1fa-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="7d1fa-478">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-478">no</span></span>             | <span data-ttu-id="7d1fa-479">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-479">no</span></span>           |
| <span data-ttu-id="7d1fa-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="7d1fa-480">msdyn_hours</span></span>                                      | <span data-ttu-id="7d1fa-481">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-481">no</span></span>             | <span data-ttu-id="7d1fa-482">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-482">no</span></span>           |
| <span data-ttu-id="7d1fa-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="7d1fa-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="7d1fa-484">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-484">no</span></span>             | <span data-ttu-id="7d1fa-485">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-485">no</span></span>           |
| <span data-ttu-id="7d1fa-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="7d1fa-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="7d1fa-487">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-487">no</span></span>             | <span data-ttu-id="7d1fa-488">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-488">no</span></span>           |
| <span data-ttu-id="7d1fa-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="7d1fa-490">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-490">no</span></span>             | <span data-ttu-id="7d1fa-491">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-491">no</span></span>           |
| <span data-ttu-id="7d1fa-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="7d1fa-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="7d1fa-493">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-493">no</span></span>             | <span data-ttu-id="7d1fa-494">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-494">no</span></span>           |
| <span data-ttu-id="7d1fa-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="7d1fa-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="7d1fa-496">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-496">no</span></span>             | <span data-ttu-id="7d1fa-497">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-497">no</span></span>           |
| <span data-ttu-id="7d1fa-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="7d1fa-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="7d1fa-499">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-499">no</span></span>             | <span data-ttu-id="7d1fa-500">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-500">no</span></span>           |
| <span data-ttu-id="7d1fa-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="7d1fa-501">msdyn_start</span></span>                                      | <span data-ttu-id="7d1fa-502">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-502">no</span></span>             | <span data-ttu-id="7d1fa-503">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="7d1fa-504">Project</span><span class="sxs-lookup"><span data-stu-id="7d1fa-504">Project</span></span>

| <span data-ttu-id="7d1fa-505">**Loģiskais nosaukums**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-505">**Logical name**</span></span>                       | <span data-ttu-id="7d1fa-506">**Var izveidot**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-506">**Can create**</span></span> | <span data-ttu-id="7d1fa-507">**Var rediģēt**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="7d1fa-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="7d1fa-509">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-509">no</span></span>             | <span data-ttu-id="7d1fa-510">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-510">no</span></span>           |
| <span data-ttu-id="7d1fa-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="7d1fa-512">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-512">no</span></span>             | <span data-ttu-id="7d1fa-513">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-513">no</span></span>           |
| <span data-ttu-id="7d1fa-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="7d1fa-515">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-515">no</span></span>             | <span data-ttu-id="7d1fa-516">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-516">no</span></span>           |
| <span data-ttu-id="7d1fa-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="7d1fa-518">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-518">no</span></span>             | <span data-ttu-id="7d1fa-519">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-519">no</span></span>           |
| <span data-ttu-id="7d1fa-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="7d1fa-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="7d1fa-521">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-521">no</span></span>             | <span data-ttu-id="7d1fa-522">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-522">no</span></span>           |
| <span data-ttu-id="7d1fa-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="7d1fa-524">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-524">no</span></span>             | <span data-ttu-id="7d1fa-525">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-525">no</span></span>           |
| <span data-ttu-id="7d1fa-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="7d1fa-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="7d1fa-527">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-527">yes</span></span>            | <span data-ttu-id="7d1fa-528">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-528">no</span></span>           |
| <span data-ttu-id="7d1fa-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="7d1fa-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="7d1fa-530">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-530">yes</span></span>            | <span data-ttu-id="7d1fa-531">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-531">no</span></span>           |
| <span data-ttu-id="7d1fa-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="7d1fa-533">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-533">yes</span></span>            | <span data-ttu-id="7d1fa-534">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-534">no</span></span>           |
| <span data-ttu-id="7d1fa-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="7d1fa-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="7d1fa-536">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-536">no</span></span>             | <span data-ttu-id="7d1fa-537">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-537">no</span></span>           |
| <span data-ttu-id="7d1fa-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="7d1fa-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="7d1fa-539">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-539">no</span></span>             | <span data-ttu-id="7d1fa-540">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-540">no</span></span>           |
| <span data-ttu-id="7d1fa-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="7d1fa-542">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-542">no</span></span>             | <span data-ttu-id="7d1fa-543">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-543">no</span></span>           |
| <span data-ttu-id="7d1fa-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="7d1fa-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="7d1fa-545">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-545">no</span></span>             | <span data-ttu-id="7d1fa-546">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-546">no</span></span>           |
| <span data-ttu-id="7d1fa-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="7d1fa-548">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-548">no</span></span>             | <span data-ttu-id="7d1fa-549">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-549">no</span></span>           |
| <span data-ttu-id="7d1fa-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="7d1fa-550">msdyn_duration</span></span>                         | <span data-ttu-id="7d1fa-551">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-551">no</span></span>             | <span data-ttu-id="7d1fa-552">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-552">no</span></span>           |
| <span data-ttu-id="7d1fa-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="7d1fa-553">msdyn_effort</span></span>                           | <span data-ttu-id="7d1fa-554">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-554">no</span></span>             | <span data-ttu-id="7d1fa-555">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-555">no</span></span>           |
| <span data-ttu-id="7d1fa-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="7d1fa-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="7d1fa-557">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-557">no</span></span>             | <span data-ttu-id="7d1fa-558">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-558">no</span></span>           |
| <span data-ttu-id="7d1fa-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="7d1fa-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="7d1fa-560">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-560">no</span></span>             | <span data-ttu-id="7d1fa-561">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-561">no</span></span>           |
| <span data-ttu-id="7d1fa-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="7d1fa-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="7d1fa-563">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-563">no</span></span>             | <span data-ttu-id="7d1fa-564">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-564">no</span></span>           |
| <span data-ttu-id="7d1fa-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="7d1fa-565">msdyn_finish</span></span>                           | <span data-ttu-id="7d1fa-566">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-566">yes</span></span>            | <span data-ttu-id="7d1fa-567">jā</span><span class="sxs-lookup"><span data-stu-id="7d1fa-567">yes</span></span>          |
| <span data-ttu-id="7d1fa-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="7d1fa-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="7d1fa-569">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-569">no</span></span>             | <span data-ttu-id="7d1fa-570">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-570">no</span></span>           |
| <span data-ttu-id="7d1fa-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="7d1fa-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="7d1fa-572">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-572">no</span></span>             | <span data-ttu-id="7d1fa-573">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-573">no</span></span>           |
| <span data-ttu-id="7d1fa-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="7d1fa-575">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-575">no</span></span>             | <span data-ttu-id="7d1fa-576">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-576">no</span></span>           |
| <span data-ttu-id="7d1fa-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="7d1fa-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="7d1fa-578">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-578">no</span></span>             | <span data-ttu-id="7d1fa-579">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-579">no</span></span>           |
| <span data-ttu-id="7d1fa-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="7d1fa-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="7d1fa-581">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-581">no</span></span>             | <span data-ttu-id="7d1fa-582">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-582">no</span></span>           |
| <span data-ttu-id="7d1fa-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="7d1fa-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="7d1fa-584">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-584">no</span></span>             | <span data-ttu-id="7d1fa-585">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-585">no</span></span>           |
| <span data-ttu-id="7d1fa-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="7d1fa-587">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-587">no</span></span>             | <span data-ttu-id="7d1fa-588">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-588">no</span></span>           |
| <span data-ttu-id="7d1fa-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="7d1fa-590">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-590">no</span></span>             | <span data-ttu-id="7d1fa-591">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-591">no</span></span>           |
| <span data-ttu-id="7d1fa-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="7d1fa-593">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-593">no</span></span>             | <span data-ttu-id="7d1fa-594">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-594">no</span></span>           |
| <span data-ttu-id="7d1fa-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="7d1fa-596">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-596">no</span></span>             | <span data-ttu-id="7d1fa-597">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-597">no</span></span>           |
| <span data-ttu-id="7d1fa-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7d1fa-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="7d1fa-599">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-599">no</span></span>             | <span data-ttu-id="7d1fa-600">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-600">no</span></span>           |
| <span data-ttu-id="7d1fa-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="7d1fa-602">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-602">no</span></span>             | <span data-ttu-id="7d1fa-603">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-603">no</span></span>           |
| <span data-ttu-id="7d1fa-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="7d1fa-604">msdyn_progress</span></span>                         | <span data-ttu-id="7d1fa-605">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-605">no</span></span>             | <span data-ttu-id="7d1fa-606">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-606">no</span></span>           |
| <span data-ttu-id="7d1fa-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="7d1fa-608">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-608">no</span></span>             | <span data-ttu-id="7d1fa-609">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-609">no</span></span>           |
| <span data-ttu-id="7d1fa-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="7d1fa-611">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-611">no</span></span>             | <span data-ttu-id="7d1fa-612">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-612">no</span></span>           |
| <span data-ttu-id="7d1fa-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="7d1fa-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="7d1fa-614">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-614">no</span></span>             | <span data-ttu-id="7d1fa-615">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-615">no</span></span>           |
| <span data-ttu-id="7d1fa-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="7d1fa-617">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-617">no</span></span>             | <span data-ttu-id="7d1fa-618">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-618">no</span></span>           |
| <span data-ttu-id="7d1fa-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="7d1fa-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="7d1fa-620">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-620">no</span></span>             | <span data-ttu-id="7d1fa-621">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-621">no</span></span>           |
| <span data-ttu-id="7d1fa-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="7d1fa-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="7d1fa-623">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-623">no</span></span>             | <span data-ttu-id="7d1fa-624">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-624">no</span></span>           |
| <span data-ttu-id="7d1fa-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="7d1fa-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="7d1fa-626">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-626">no</span></span>             | <span data-ttu-id="7d1fa-627">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-627">no</span></span>           |
| <span data-ttu-id="7d1fa-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="7d1fa-629">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-629">no</span></span>             | <span data-ttu-id="7d1fa-630">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-630">no</span></span>           |
| <span data-ttu-id="7d1fa-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="7d1fa-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="7d1fa-632">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-632">no</span></span>             | <span data-ttu-id="7d1fa-633">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-633">no</span></span>           |
| <span data-ttu-id="7d1fa-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="7d1fa-635">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-635">no</span></span>             | <span data-ttu-id="7d1fa-636">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-636">no</span></span>           |
| <span data-ttu-id="7d1fa-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="7d1fa-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="7d1fa-638">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-638">no</span></span>             | <span data-ttu-id="7d1fa-639">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-639">no</span></span>           |
| <span data-ttu-id="7d1fa-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="7d1fa-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="7d1fa-641">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-641">no</span></span>             | <span data-ttu-id="7d1fa-642">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-642">no</span></span>           |
| <span data-ttu-id="7d1fa-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="7d1fa-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="7d1fa-644">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-644">no</span></span>             | <span data-ttu-id="7d1fa-645">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-645">no</span></span>           |
| <span data-ttu-id="7d1fa-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="7d1fa-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="7d1fa-647">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-647">no</span></span>             | <span data-ttu-id="7d1fa-648">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-648">no</span></span>           |
| <span data-ttu-id="7d1fa-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="7d1fa-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="7d1fa-650">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-650">no</span></span>             | <span data-ttu-id="7d1fa-651">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-651">no</span></span>           |
| <span data-ttu-id="7d1fa-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="7d1fa-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="7d1fa-653">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-653">no</span></span>             | <span data-ttu-id="7d1fa-654">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-654">no</span></span>           |
| <span data-ttu-id="7d1fa-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="7d1fa-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="7d1fa-656">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-656">no</span></span>             | <span data-ttu-id="7d1fa-657">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-657">no</span></span>           |
| <span data-ttu-id="7d1fa-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="7d1fa-659">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-659">no</span></span>             | <span data-ttu-id="7d1fa-660">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-660">no</span></span>           |
| <span data-ttu-id="7d1fa-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="7d1fa-662">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-662">no</span></span>             | <span data-ttu-id="7d1fa-663">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-663">no</span></span>           |
| <span data-ttu-id="7d1fa-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="7d1fa-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="7d1fa-665">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-665">no</span></span>             | <span data-ttu-id="7d1fa-666">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-666">no</span></span>           |
| <span data-ttu-id="7d1fa-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="7d1fa-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="7d1fa-668">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-668">no</span></span>             | <span data-ttu-id="7d1fa-669">nē</span><span class="sxs-lookup"><span data-stu-id="7d1fa-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="7d1fa-670">Zināmās problēmas un ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="7d1fa-670">Limitations and known issues</span></span>
<span data-ttu-id="7d1fa-671">Tālāk ir saraksts ar ierobežojumiem un zināmajām problēmām.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="7d1fa-672">Plānošanas API var izmantot tikai **lietotāji ar Microsoft Project License.**</span><span class="sxs-lookup"><span data-stu-id="7d1fa-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="7d1fa-673">Tos nevar izmantot tālāk minētie lietotāji.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-673">They can't be used by:</span></span>
    - <span data-ttu-id="7d1fa-674">Programmas lietotāji</span><span class="sxs-lookup"><span data-stu-id="7d1fa-674">Application users</span></span>
    - <span data-ttu-id="7d1fa-675">Sistēmas lietotāji</span><span class="sxs-lookup"><span data-stu-id="7d1fa-675">System users</span></span>
    - <span data-ttu-id="7d1fa-676">Integrācijas lietotāji</span><span class="sxs-lookup"><span data-stu-id="7d1fa-676">Integration users</span></span>
    - <span data-ttu-id="7d1fa-677">Citi lietotāji, kuriem nav nepieciešamās licences</span><span class="sxs-lookup"><span data-stu-id="7d1fa-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="7d1fa-678">Katrai **OperationSet** var būt ne vairāk par 100 operācijām.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="7d1fa-679">Katram lietotājam var būt ne vairāk par 10 atvērtām **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="7d1fa-680">Project Operations pašlaik atbalsta ne vairāk kā 500 uzdevumu vienā projektā.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="7d1fa-681">**OperationSet** kļūmes statusa un kļūmju žurnāli pašlaik nav pieejami.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="7d1fa-682">Projektu un uzdevumu ierobežojumi un robežas</span><span class="sxs-lookup"><span data-stu-id="7d1fa-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="7d1fa-683">Kļūdu apstrāde</span><span class="sxs-lookup"><span data-stu-id="7d1fa-683">Error handling</span></span>

   - <span data-ttu-id="7d1fa-684">Lai pārskatītu operāciju kopās ģenerētās kļūdas, atveriet sadaļu **Iestatījumi** \> **Plānot integrāciju** \> **Operāciju kopas**.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="7d1fa-685">Lai pārskatītu Project Scheduling Service ģenerētās kļūdas, atveriet sadaļu **Iestatījumi** \> **Plānot integrāciju** \> **PSS kļūdu žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="7d1fa-686">Scenārija paraugs</span><span class="sxs-lookup"><span data-stu-id="7d1fa-686">Sample scenario</span></span>

<span data-ttu-id="7d1fa-687">Šādā scenārijā jums būs jāizveido projekts, darba grupas dalībnieks, četri uzdevumi un divi resursu piešķīrumi.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="7d1fa-688">Pēc tam jūs atjaunināsiet vienu uzdevumu, atjaunināsiet projektu, izdzēsiet vienu uzdevumu, izdzēsiet vienu resursa piešķīrumu un izveidosiet uzdevuma atkarību.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="7d1fa-689">Papildu paraugi</span><span class="sxs-lookup"><span data-stu-id="7d1fa-689">Additional samples</span></span>

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
