---
title: Projekta aprēķinu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta stundu aprēķinu un projekta izmaksu aprēķinu sinhronizēšanai tieši no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080572"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a5016-103">Projekta aprēķinu sinhronizēšana tieši no Project Service Automation uz Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5016-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a5016-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta stundu aprēķinu un projekta izmaksu aprēķinu sinhronizēšanai tieši no Dynamics 365 Project Service Automation uz Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a5016-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="a5016-105">8.0 versijā varat izmantot projekta uzdevumu integrāciju, izdevumu darbības kategorijas, stundu aprēķinus, izdevumu aprēķinus un funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="a5016-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="a5016-106">Faktisko datu integrācija ir pieejama 8.0.1 vai jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="a5016-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="a5016-107">Datu plūsma Project Service Automation uz Finance</span><span class="sxs-lookup"><span data-stu-id="a5016-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="a5016-108">Project Service Automation uz Finance integrācijas risinājumam tiek izmantots datu integrācijas līdzeklis, lai sinhronizētu datus starp Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="a5016-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="a5016-109">Integrācijas veidnes, kas ir pieejamas kopā ar datu integrācijas līdzekli, iespējo datu plūsmu par projekta stundu aprēķiniem un projekta izmaksu aprēķiniem no Project Service Automation līdz Finance.</span><span class="sxs-lookup"><span data-stu-id="a5016-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a5016-110">Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti starp Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="a5016-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="a5016-111">[![Datu plūsma Project Service Automation integrācijai ar Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a5016-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="a5016-112">Projekta stundu aprēķini</span><span class="sxs-lookup"><span data-stu-id="a5016-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="a5016-113">Veidne un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="a5016-113">Template and tasks</span></span>

<span data-ttu-id="a5016-114">Lai piekļūtu pieejamajām veidnēm, Microsoft Power Apps administrēšanas centrā atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts** , lai atlasītu publiskas veidnes.</span><span class="sxs-lookup"><span data-stu-id="a5016-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a5016-115">Lai sinhronizētu projekta stundu aprēķinus no Project Service Automation uz Finance, tiek izmantota šāda veidne un pamata uzdevumi:</span><span class="sxs-lookup"><span data-stu-id="a5016-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a5016-116">**Veidnes nosaukums datu integrācijā:** Projekta stundu aprēķini (PSA uz Fin un Ops)</span><span class="sxs-lookup"><span data-stu-id="a5016-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a5016-117">**Projekta uzdevumu nosaukums:**</span><span class="sxs-lookup"><span data-stu-id="a5016-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="a5016-118">Transakciju saistības</span><span class="sxs-lookup"><span data-stu-id="a5016-118">Transaction relationships</span></span>
    - <span data-ttu-id="a5016-119">Izdevumu tāmes</span><span class="sxs-lookup"><span data-stu-id="a5016-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="a5016-120">Entītiju kopa</span><span class="sxs-lookup"><span data-stu-id="a5016-120">Entity set</span></span>

| <span data-ttu-id="a5016-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a5016-121">Project Service Automation</span></span> | <span data-ttu-id="a5016-122">Finance</span><span class="sxs-lookup"><span data-stu-id="a5016-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="a5016-123">Projekta uzdevumi</span><span class="sxs-lookup"><span data-stu-id="a5016-123">Project tasks</span></span>              | <span data-ttu-id="a5016-124">Integrācijas entitīja projekta stundu aprēķiniem</span><span class="sxs-lookup"><span data-stu-id="a5016-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="a5016-125">Entītijas plūsma</span><span class="sxs-lookup"><span data-stu-id="a5016-125">Entity flow</span></span>

<span data-ttu-id="a5016-126">Projekta stundu aprēķini tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta stundu prognozes.</span><span class="sxs-lookup"><span data-stu-id="a5016-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a5016-127">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="a5016-127">Prerequisites</span></span>

<span data-ttu-id="a5016-128">Pirms var notikt projekta stundu aprēķinu sinhronizēšana, ir jāsinhronizē projekti, projekta uzdevumi un projekta izdevumu transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="a5016-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a5016-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="a5016-129">Power Query</span></span>

<span data-ttu-id="a5016-130">Projekta stundu aprēķinu veidnē ir jāizmanto Microsoft Power Query for Excel, lai izpildītu šos uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="a5016-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="a5016-131">Iestatiet noklusējuma prognozes modeļa ID, kas tiks izmantots, kad integrācija veidos jaunas stundu prognozes.</span><span class="sxs-lookup"><span data-stu-id="a5016-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="a5016-132">Izfiltrējiet visus resursiem specifiskos ierakstus uzdevumā, kas nevarēs integrēties stundu prognozēs.</span><span class="sxs-lookup"><span data-stu-id="a5016-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="a5016-133">Izfiltrējiet visas tukšās transakcijas kategoriju rindas.</span><span class="sxs-lookup"><span data-stu-id="a5016-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="a5016-134">Ja šo uzdevumu nevar izpildīt, var rasties nepareizas stundu prognozes.</span><span class="sxs-lookup"><span data-stu-id="a5016-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="a5016-135">Iestatiet noklusējuma prognozes modeļa ID</span><span class="sxs-lookup"><span data-stu-id="a5016-135">Set the default forecast model ID</span></span>

<span data-ttu-id="a5016-136">Lai veidnē atjauninātu noklusējuma prognozes modeļa ID, noklikšķiniet uz bultiņas **Karte** , lai atvērtu kartējumu.</span><span class="sxs-lookup"><span data-stu-id="a5016-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a5016-137">Pēc tam atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti.</span><span class="sxs-lookup"><span data-stu-id="a5016-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="a5016-138">Ja izmantojat noklusējuma Projekta stundu aprēķinu (PSA uz Fin un Ops) veidni, **Piemērojamo darbību** sarakstā atlasiet **Ievietoto nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="a5016-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="a5016-139">**Funkciju** ierakstā aizstājiet **O\_prognozi** ar tā prognozes modeļa ID, kuru vajadzētu izmantot ar integrāciju.</span><span class="sxs-lookup"><span data-stu-id="a5016-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="a5016-140">Noklusējuma veidnei ir prognozes modeļa ID no demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="a5016-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="a5016-141">Ja izveidojat jaunu veidni, šī kolonna ir jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="a5016-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="a5016-142">Power Query atlasiet **Pievienot nosacījuma kolonnu** un ievadiet jaunās kolonnas nosaukumu, piemēram, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="a5016-142">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="a5016-143">Ievadiet kolonnas nosacījumu, kur, ja projekta uzdevums nav Null, tad \<enter the forecast model ID\>; pretējā gadījumā tas ir Null.</span><span class="sxs-lookup"><span data-stu-id="a5016-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="a5016-144">Resursiem specifisku ierakstu izfiltrēšana</span><span class="sxs-lookup"><span data-stu-id="a5016-144">Filter out resource-specific records</span></span>

<span data-ttu-id="a5016-145">Projekta stundas aprēķinu (PSA uz Fin un Ops) veidnei ir noklusējuma filtrs, kas noņem jebkādus resursiem specifiskos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a5016-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="a5016-146">Ja izveidojat savu veidni, šis filtrs ir jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="a5016-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="a5016-147">Atlasiet **Detalizētā vaicājuma un filtrēšanas** saiti, lai filtrētu **msdyn\_islinetask** kolonnā, lai tiek iekļauti vienīgi ieraksti **False**.</span><span class="sxs-lookup"><span data-stu-id="a5016-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="a5016-148">Izfiltrējiet tukšās transakcijas kategoriju rindas</span><span class="sxs-lookup"><span data-stu-id="a5016-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="a5016-149">Lai noņemtu rindas, kurās ir tukšas transakciju kategorijas, ir jāpievieno filtrs.</span><span class="sxs-lookup"><span data-stu-id="a5016-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="a5016-150">Šis uzdevums ir obligāts neatkarīgi no tā, vai izmantojat noklusējuma veidni, vai izveidojat paši savu.</span><span class="sxs-lookup"><span data-stu-id="a5016-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="a5016-151">Ar šo filtru tiek noņemtas visas kopsavilkuma rindas no Project Service Automation, kuras varētu radīt nepareizas stundu prognozes risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="a5016-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="a5016-152">Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti, lai izfiltrētu tukšos ierakstus kolonnā **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="a5016-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a5016-153">Veidņu kartēšana datu integrācijā</span><span class="sxs-lookup"><span data-stu-id="a5016-153">Template mapping in Data integration</span></span>

<span data-ttu-id="a5016-154">Nākamajā ilustrācijā ir redzams piemērs no veidnes uzdevumu kartējuma datu integrācijā.</span><span class="sxs-lookup"><span data-stu-id="a5016-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="a5016-155">Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="a5016-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a5016-156">[![Veidnes uzdevuma kartēšana datu integrācijā](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a5016-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="a5016-157">Projekta izmaksu aplēses</span><span class="sxs-lookup"><span data-stu-id="a5016-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="a5016-158">Veidne un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="a5016-158">Template and tasks</span></span>

<span data-ttu-id="a5016-159">Lai sinhronizētu projekta izmaksu aprēķinus no Project Service Automation uz Finance, tiek izmantota šāda veidne un pamata uzdevumi:</span><span class="sxs-lookup"><span data-stu-id="a5016-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a5016-160">**Veidnes nosaukums datu integrācijā:** Projekta izmaksu aprēķini (PSA uz Fin un Ops)</span><span class="sxs-lookup"><span data-stu-id="a5016-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a5016-161">**Projekta uzdevumu nosaukums:**</span><span class="sxs-lookup"><span data-stu-id="a5016-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="a5016-162">Transakciju saistības</span><span class="sxs-lookup"><span data-stu-id="a5016-162">Transaction relationships</span></span> 
    - <span data-ttu-id="a5016-163">Izdevumu tāmes</span><span class="sxs-lookup"><span data-stu-id="a5016-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="a5016-164">Entītiju kopa</span><span class="sxs-lookup"><span data-stu-id="a5016-164">Entity set</span></span>

| <span data-ttu-id="a5016-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a5016-165">Project Service Automation</span></span> | <span data-ttu-id="a5016-166">Finance</span><span class="sxs-lookup"><span data-stu-id="a5016-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="a5016-167">Transakcijas savienojumi</span><span class="sxs-lookup"><span data-stu-id="a5016-167">Transaction Connections</span></span>    | <span data-ttu-id="a5016-168">Integrāciju entitīja projekta transakciju relācijām</span><span class="sxs-lookup"><span data-stu-id="a5016-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="a5016-169">Novērtējuma rindas</span><span class="sxs-lookup"><span data-stu-id="a5016-169">Estimate Lines</span></span>             | <span data-ttu-id="a5016-170">Integrācijas entitīja projekta izmaksu aprēķiniem</span><span class="sxs-lookup"><span data-stu-id="a5016-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="a5016-171">Entītijas plūsma</span><span class="sxs-lookup"><span data-stu-id="a5016-171">Entity flow</span></span>

<span data-ttu-id="a5016-172">Projekta izmaksu aprēķini tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta izmaksu prognozes.</span><span class="sxs-lookup"><span data-stu-id="a5016-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a5016-173">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="a5016-173">Prerequisites</span></span>

<span data-ttu-id="a5016-174">Pirms var notikt projekta stundu izmaksu sinhronizēšana, ir jāsinhronizē projekti, projekta uzdevumi un projekta izdevumu transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="a5016-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a5016-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="a5016-175">Power Query</span></span>

<span data-ttu-id="a5016-176">Projekta izmaksu aprēķinu veidnē ir jāizmanto Power Query, lai izpildītu šos uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="a5016-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="a5016-177">Filtrēt, lai iekļautu tikai izmaksas aprēķinu rindas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a5016-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="a5016-178">Iestatiet noklusējuma prognozes modeļa ID, kas tiks izmantots, kad integrācija veidos jaunas stundu prognozes.</span><span class="sxs-lookup"><span data-stu-id="a5016-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="a5016-179">Pārvērstu norēķinu veidus.</span><span class="sxs-lookup"><span data-stu-id="a5016-179">Transform the billing types.</span></span>
- <span data-ttu-id="a5016-180">Pārvērstu transakciju veidus.</span><span class="sxs-lookup"><span data-stu-id="a5016-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="a5016-181">Filtrēt, lai iekļautu vienīgi izmaksu aprēķinu rindas</span><span class="sxs-lookup"><span data-stu-id="a5016-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="a5016-182">Projekta izmaksu aprēķinu (PSA uz Fin un Ops) veidnei ir noklusējuma filtrs, kas integrācijā iekļauj vienīgi izmaksu rindas.</span><span class="sxs-lookup"><span data-stu-id="a5016-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="a5016-183">Ja izveidojat savu veidni, šis filtrs ir jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="a5016-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="a5016-184">Atlasiet uzdevumu **Transakciju relācijas** un pēc tam noklikšķiniet uz bulttaustiņa **Karte** , lai atvērtu kartējumu.</span><span class="sxs-lookup"><span data-stu-id="a5016-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a5016-185">Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti.</span><span class="sxs-lookup"><span data-stu-id="a5016-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="a5016-186">Filtrējiet kolonnu **msdyn\_transactiontype1** tā, lai tā ietver vienīgi **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="a5016-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="a5016-187">Iestatiet noklusējuma prognozes modeļa ID</span><span class="sxs-lookup"><span data-stu-id="a5016-187">Set the default forecast model ID</span></span>

<span data-ttu-id="a5016-188">Lai veidnē atjauninātu noklusējuma prognozes modeļa ID, atlasiet uzdevumu **Izmaksu aprēķini** un pēc tam noklikšķiniet uz bulttaustiņa **Karte** , lai atvērtu kartējumu.</span><span class="sxs-lookup"><span data-stu-id="a5016-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a5016-189">Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti.</span><span class="sxs-lookup"><span data-stu-id="a5016-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="a5016-190">Ja izmantojat noklusējuma Projekta izmaksu aprēķinus (PSA uz Fin un Ops) veidni, Power Query sadaļā **Piemērojamās darbības** atlasiet pirmo **Ievietoto nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="a5016-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="a5016-191">**Funkciju** ierakstā aizstājiet **O\_prognozi** ar tā prognozes modeļa ID, kuru vajadzētu izmantot ar integrāciju.</span><span class="sxs-lookup"><span data-stu-id="a5016-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="a5016-192">Noklusējuma veidnei ir prognozes modeļa ID no demonstrācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="a5016-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="a5016-193">Ja izveidojat jaunu veidni, šī kolonna ir jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="a5016-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="a5016-194">Power Query atlasiet **Pievienot nosacījuma kolonnu** un ievadiet jaunās kolonnas nosaukumu, piemēram, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="a5016-194">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="a5016-195">Ievadiet kolonnas nosacījumu, kur, ja novērtējuma rindas ID nav Null, tad \<enter the forecast model ID\>; pretējā gadījumā tas ir Null.</span><span class="sxs-lookup"><span data-stu-id="a5016-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="a5016-196">Pārvērtiet norēķinu veidus</span><span class="sxs-lookup"><span data-stu-id="a5016-196">Transform the billing types</span></span>

<span data-ttu-id="a5016-197">Projekta izmaksu aprēķinu (PSA uz Fin un Opc) veidne ietver nosacījuma kolonnu, kas tiek izmantota, lai pārvērstu norēķinu veidus, kuri integrēšanas laikā tiek saņemti no Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a5016-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="a5016-198">Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna.</span><span class="sxs-lookup"><span data-stu-id="a5016-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="a5016-199">Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti un pēc tam atlasiet **Pievienot nosacījuma kolonnu**.</span><span class="sxs-lookup"><span data-stu-id="a5016-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="a5016-200">Ievadiet jaunās kolonnas nosaukumu, piemēram, **NorēķinuTips**.</span><span class="sxs-lookup"><span data-stu-id="a5016-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="a5016-201">Pēc tam ievadiet šādu nosacījumu:</span><span class="sxs-lookup"><span data-stu-id="a5016-201">Then enter the following condition:</span></span>

<span data-ttu-id="a5016-202">Ja **msdyn\_billingtype** = 192350000, tad **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="a5016-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="a5016-203">pretējā gadījumā, ja **msdyn\_billingtype** = 192350001, tad **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="a5016-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="a5016-204">pretējā gadījumā, ja **msdyn\_billingtype** = 192350002, tad **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="a5016-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="a5016-205">pretējā gadījumā **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="a5016-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="a5016-206">Pārvērtiet transakciju veidus</span><span class="sxs-lookup"><span data-stu-id="a5016-206">Transform the transaction types</span></span>

<span data-ttu-id="a5016-207">Projekta izmaksu aprēķinu (PSA uz Fin un Opc) veidne ietver nosacījuma kolonnu, kas tiek izmantota, lai pārvērstu transakciju veidus, kuri integrēšanas laikā tiek saņemti no Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a5016-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="a5016-208">Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna.</span><span class="sxs-lookup"><span data-stu-id="a5016-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="a5016-209">Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti un pēc tam atlasiet **Pievienot nosacījuma kolonnu**.</span><span class="sxs-lookup"><span data-stu-id="a5016-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="a5016-210">Ievadiet jaunās kolonnas nosaukumu, piemēram, **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="a5016-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="a5016-211">Pēc tam ievadiet šādu nosacījumu:</span><span class="sxs-lookup"><span data-stu-id="a5016-211">Then enter the following condition:</span></span>

<span data-ttu-id="a5016-212">Ja **msdyn\_transactiontypecode** = 192350000, tad **Cost**</span><span class="sxs-lookup"><span data-stu-id="a5016-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="a5016-213">pretējā gadījumā, ja **msdyn\_transactiontypecode** = 192350005, tad **Sales**</span><span class="sxs-lookup"><span data-stu-id="a5016-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="a5016-214">pretējā gadījumā **tukšs**</span><span class="sxs-lookup"><span data-stu-id="a5016-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a5016-215">Veidņu kartēšana datu integrācijā</span><span class="sxs-lookup"><span data-stu-id="a5016-215">Template mapping in Data integration</span></span>

<span data-ttu-id="a5016-216">Nākamajās ilustrācijās ir redzami piemēri no veidnes uzdevumu kartējumiem datu integrācijā.</span><span class="sxs-lookup"><span data-stu-id="a5016-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="a5016-217">Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="a5016-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a5016-218">[![Izmaksu novērtējuma transakciju veidnes kartēšana](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a5016-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="a5016-219">[![Izmaksu novērtējuma veidnes kartēšana](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a5016-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
