---
title: Projekta līgumu un projektu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir aprakstīta veidne un pamata uzdevumi, kas tiek izmantots projekta līgumu un projektu sinhronizēšanai tieši no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 09/09/2019
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0b3bc159fff25c4f6e5b1ed1b2eabbba675fb0f5
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642642"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="e4fdf-103">Projekta līgumu un projektu sinhronizēšana tieši no Project Service Automation uz Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e4fdf-103">Synchronize project contracts and projects directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e4fdf-104">Šajā tēmā ir aprakstīta veidne un pamata uzdevumi, kas tiek izmantots projekta līgumu un projektu sinhronizēšanai tieši no Dynamics 365 Project Service Automation uz Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-104">This topic describes the template and underlying tasks that are used to synchronize project contracts and projects directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE] 
> <span data-ttu-id="e4fdf-105">Ja izmantojat Enterprise edition 7.3.0, ir jāinstalē KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-105">If you're using Enterprise edition 7.3.0, you must install KB 4074835.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="e4fdf-106">Datu plūsma Project Service Automation uz Finance</span><span class="sxs-lookup"><span data-stu-id="e4fdf-106">Data flow for Project Service Automation to Finance</span></span>

> [!NOTE]
> <span data-ttu-id="e4fdf-107">Lai varētu izmantot Project Service Automation uz Finance integrācijas risinājumu, ir jāpārzina Dynamics 365 datu integrācijas līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-107">Before you can use the Project Service Automation to Finance integration solution, you should be familiar with the Dynamics 365 Data integration feature.</span></span>

<span data-ttu-id="e4fdf-108">Project Service Automation uz Finance integrācijas risinājumam tiek izmantots datu integrācijas līdzeklis, lai sinhronizētu datus starp Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="e4fdf-109">Integrēšanas veidne, kas ir pieejama ar datu integrācijas līdzekli, iespējo datu plūsmu par projektu līgumiem, projektiem, projekta līguma rindām un projekta līgumu rindu atskaites punktiem no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-109">The integration template that is available with the Data integration feature enables the flow of data about project contracts, projects, project contract lines, and project contract line milestones from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e4fdf-110">Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti starp Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="e4fdf-111">[![Datu plūsma Project Service Automation integrācijai ar Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)</span><span class="sxs-lookup"><span data-stu-id="e4fdf-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e4fdf-112">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="e4fdf-112">Templates and tasks</span></span>

<span data-ttu-id="e4fdf-113">Lai piekļūtu pieejamajām veidnēm, Microsoft Power Apps administrēšanas centrā atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskas veidnes.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-113">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e4fdf-114">Lai sinhronizētu projekta līgumus un projektus no Project Service Automation uz Finance, tiek izmantotas šādas veidnes un pamata uzdevumi:</span><span class="sxs-lookup"><span data-stu-id="e4fdf-114">The following templates and underlying tasks are used to synchronize project contracts and projects from Project Service Automation to Finance:</span></span>

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a><span data-ttu-id="e4fdf-115">Integrēšana ar Dynamics 365 Project Service Automation v2.x</span><span class="sxs-lookup"><span data-stu-id="e4fdf-115">Integrating with Dynamics 365 Project Service Automation v2.x</span></span>
- <span data-ttu-id="e4fdf-116">**Veidnes nosaukums datu integrācijā:** Projekti un līgumi (PSA uz Fin un Ops)</span><span class="sxs-lookup"><span data-stu-id="e4fdf-116">**Name of the template in Data integration:** Projects and contracts (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="e4fdf-117">**Projekta uzdevumu nosaukums:**</span><span class="sxs-lookup"><span data-stu-id="e4fdf-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="e4fdf-118">Projekta līgumi PSA uz Fin un Ops</span><span class="sxs-lookup"><span data-stu-id="e4fdf-118">Project contracts PSA to Fin and Ops</span></span>
    - <span data-ttu-id="e4fdf-119">Projekti PSA uz Fin un Ops</span><span class="sxs-lookup"><span data-stu-id="e4fdf-119">Projects PSA to Fin and Ops</span></span>
    - <span data-ttu-id="e4fdf-120">Projekta līgumu rindas PSA uz Fin un Ops</span><span class="sxs-lookup"><span data-stu-id="e4fdf-120">Project contract lines PSA to Fin and Ops</span></span>
    - <span data-ttu-id="e4fdf-121">Projekta līgumu rindu atskaites punkti PSA uz Fin un Ops</span><span class="sxs-lookup"><span data-stu-id="e4fdf-121">Project contract line milestones PSA to Fin and Ops</span></span>
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a><span data-ttu-id="e4fdf-122">Integrēšana ar Dynamics 365 Project Service Automation v3.x</span><span class="sxs-lookup"><span data-stu-id="e4fdf-122">Integrating with Dynamics 365 Project Service Automation v3.x</span></span>
<span data-ttu-id="e4fdf-123">Project Service Automation ir shēmas izmaiņas, kas ietekmē projekta līguma rindu atskaites punktu veidni, un Project Service Automation v3.x integrēšanai ar Dynamics 365 nepieciešams izmantot veidnes v2 versiju.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-123">There is a schema change in Project Service Automation that impacts the Project contract line milestone template and use of the v2 version of the template is required to integrate Project Service Automation v3.x with Dynamics 365.</span></span>

- <span data-ttu-id="e4fdf-124">**Veidnes nosaukums datu integrācijā:** Projekti un līgumi (PSA 3.x uz Fin un Ops) — v2</span><span class="sxs-lookup"><span data-stu-id="e4fdf-124">**Name of the template in Data integration:** Projects and Contracts (PSA 3.x to Fin and Ops) - v2</span></span>
- <span data-ttu-id="e4fdf-125">**Projekta uzdevumu nosaukums:**</span><span class="sxs-lookup"><span data-stu-id="e4fdf-125">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="e4fdf-126">Projekta līgumi PSA uz Fin un Ops</span><span class="sxs-lookup"><span data-stu-id="e4fdf-126">Project contracts PSA to Fin and Ops</span></span>
    - <span data-ttu-id="e4fdf-127">Projekti PSA uz Fin un Ops</span><span class="sxs-lookup"><span data-stu-id="e4fdf-127">Projects PSA to Fin and Ops</span></span>
    - <span data-ttu-id="e4fdf-128">Projekta līgumu rindas PSA uz Fin un Ops</span><span class="sxs-lookup"><span data-stu-id="e4fdf-128">Project contract lines PSA to Fin and Ops</span></span>
    - <span data-ttu-id="e4fdf-129">Projekta līgumu rindu atskaites punkti PSA uz Fin un Ops</span><span class="sxs-lookup"><span data-stu-id="e4fdf-129">Project contract line milestones PSA to Fin and Ops</span></span>

<span data-ttu-id="e4fdf-130">Pirms projekta līgumu un projektu sinhronizēšanas ir jāsinhronizē uzņēmumi.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-130">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>

## <a name="entity-set"></a><span data-ttu-id="e4fdf-131">Entītiju kopa</span><span class="sxs-lookup"><span data-stu-id="e4fdf-131">Entity set</span></span>

| <span data-ttu-id="e4fdf-132">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e4fdf-132">Project Service Automation</span></span>       | <span data-ttu-id="e4fdf-133">Finanses</span><span class="sxs-lookup"><span data-stu-id="e4fdf-133">Finance</span></span>                                                |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="e4fdf-134">Pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="e4fdf-134">Orders</span></span>                           | <span data-ttu-id="e4fdf-135">Projekta līguma integrācijas entītija</span><span class="sxs-lookup"><span data-stu-id="e4fdf-135">Integration entity for project contract</span></span>                |
| <span data-ttu-id="e4fdf-136">Projekti</span><span class="sxs-lookup"><span data-stu-id="e4fdf-136">Projects</span></span>                         | <span data-ttu-id="e4fdf-137">Projekta integrācijas entītija</span><span class="sxs-lookup"><span data-stu-id="e4fdf-137">Integration entity for project</span></span>                         |
| <span data-ttu-id="e4fdf-138">Pasūtījuma rindas</span><span class="sxs-lookup"><span data-stu-id="e4fdf-138">Order lines</span></span>                      | <span data-ttu-id="e4fdf-139">Projekta līguma rindas integrācijas entītija</span><span class="sxs-lookup"><span data-stu-id="e4fdf-139">Integration entity for project contract line</span></span>           |
| <span data-ttu-id="e4fdf-140">Projekta līguma rindas atskaites punkti</span><span class="sxs-lookup"><span data-stu-id="e4fdf-140">Project contract line milestones</span></span> | <span data-ttu-id="e4fdf-141">Projekta līguma rindas atskaites punkta integrācijas entītija</span><span class="sxs-lookup"><span data-stu-id="e4fdf-141">Integration entity for project contract line milestone</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="e4fdf-142">Entītijas plūsma</span><span class="sxs-lookup"><span data-stu-id="e4fdf-142">Entity flow</span></span>

<span data-ttu-id="e4fdf-143">Projekta līgumi tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta līgumi.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-143">Project contracts are managed in Project Service Automation, and they are synchronized to Finance as project contracts.</span></span> <span data-ttu-id="e4fdf-144">Kā integrācijas veidnes daļu risinājumā Finance var iestatīt integrācijas avotu projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-144">As part of the integration template, you can set the integration source in Finance for the project contract.</span></span>

<span data-ttu-id="e4fdf-145">Laika un materiālu projekti un fiksētas cenas projekti tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekti.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-145">Time and material project and Fixed price projects are managed in Project Service Automation, and they are synchronized to Finance as projects.</span></span> <span data-ttu-id="e4fdf-146">Kā veidnes integrācijas daļu risinājumā Finance var iestatīt integrācijas avotu projektam.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-146">As part of the template integration, you can set the integration source in Finance for the project.</span></span>

<span data-ttu-id="e4fdf-147">Projekta līgumu rindas tiek pārvaldītas pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta līgumu norēķinu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-147">Project contract lines are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rules.</span></span> <span data-ttu-id="e4fdf-148">Ja norēķinu metode atšķiras no noklusējuma projekta tipa, sinhronizācija atjaunina projekta tipu līguma rindas projektam un projekta grupai.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-148">If the billing method differs from the default project type, the synchronization updates the project type for the contract line project and project group.</span></span>

<span data-ttu-id="e4fdf-149">Projekta līgumu rindas atskaites punkti tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta līgumu norēķinu kārtulu atskaites punkti.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-149">Project contract line milestones are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rule milestones.</span></span>

## <a name="project-service-automation-to-finance-integration-solution"></a><span data-ttu-id="e4fdf-150">Project Service Automation uz Finance integrācijas risinājums</span><span class="sxs-lookup"><span data-stu-id="e4fdf-150">Project Service Automation to Finance integration solution</span></span>

<span data-ttu-id="e4fdf-151">Lauks **Projekta līguma ID** ir pieejams lapā **Projekta līgumi**.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-151">The **Project contract ID** field is available on the **Project contracts** page.</span></span> <span data-ttu-id="e4fdf-152">Šis lauks ir padarīts par dabisku un unikālu integrācijas atbalsta atslēgu.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-152">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="e4fdf-153">Kad tiek izveidots jauns projekta līgums, ja vērtība **Projekta līguma ID** vēl nepastāv, tā tiek automātiski ģenerēta, izmantojot numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-153">When a new project contract is created, if a **Project contract ID** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="e4fdf-154">Vērtība sastāv no **ORD** un pēc tam no pieaugušas skaitļu secības, un pēc tam no sešu rakstzīmju sufiksa.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-154">The value consists of **ORD** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="e4fdf-155">Lūk, piemērs: **ORD-01022-Z4M9Q0**.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-155">Here is an example: **ORD-01022-Z4M9Q0**.</span></span>

<span data-ttu-id="e4fdf-156">Lauks **Projekta numurs** ir pieejams lapā **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-156">The **Project Number** field is available on the **Projects** page.</span></span> <span data-ttu-id="e4fdf-157">Šis lauks ir padarīts par dabisku un unikālu integrācijas atbalsta atslēgu.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-157">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="e4fdf-158">Kad tiek izveidots jauns projekts, ja vērtība **Projekta numurs** vēl nepastāv, tā tiek automātiski ģenerēta, izmantojot numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-158">When a new project is created, if a **Project Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="e4fdf-159">Vērtība sastāv no **PRJ** un pēc tam no pieaugušas skaitļu secības, un pēc tam no sešu rakstzīmju sufiksa.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-159">The value consists of **PRJ** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="e4fdf-160">Lūk, piemērs: **PRJ-01049-CCNID0**.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-160">Here is an example: **PRJ-01049-CCNID0**.</span></span>

<span data-ttu-id="e4fdf-161">Kad tiek lietots Project Service Automation uz Finance integrācijas risinājums, jaunināšanas skripts iestata lauku **Projekta līguma ID** esošiem projekta līgumiem un lauku **Projekta numurs** esošiem projektiem Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-161">When the Project Service Automation to Finance integration solution is applied, an upgrade script sets the **Project contract ID** field for existing project contracts and the **Project Number** field for existing projects in Project Service Automation.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e4fdf-162">Priekšnosacījumi un kartēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e4fdf-162">Prerequisites and mapping setup</span></span>

- <span data-ttu-id="e4fdf-163">Pirms projekta līgumu un projektu sinhronizēšanas ir jāsinhronizē uzņēmumi.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-163">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>
- <span data-ttu-id="e4fdf-164">Savienojuma kopā pievienojiet integrācijas atslēgas lauka kartējumu **msdyn\_organizationalunits** uz **msdyn\_name \[Name\]**.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-164">In your connection set, add an integration key field mapping for **msdyn\_organizationalunits** to **msdyn\_name \[Name\]**.</span></span> <span data-ttu-id="e4fdf-165">Iespējams, ka savienojuma kopai vispirms ir jāpievieno projekts.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-165">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="e4fdf-166">Papildinformāciju skatiet rakstā [Datu integrācija pakalpojumā Common Data Service programmām](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="e4fdf-166">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="e4fdf-167">Savienojuma kopā pievienojiet integrācijas atslēgas lauka kartējumu **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-167">In your connection set, add an integration key field mapping for **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span></span> <span data-ttu-id="e4fdf-168">Iespējams, ka savienojuma kopai vispirms ir jāpievieno projekts.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-168">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="e4fdf-169">Papildinformāciju skatiet rakstā [Datu integrācija pakalpojumā Common Data Service programmām](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="e4fdf-169">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="e4fdf-170">**SourceDataID** projektu līgumiem un projektiem var atjaunināt uz citu vērtību vai noņemt no kartējuma.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-170">**SourceDataID** for project contracts and projects can be updated to a different value or removed from the mapping.</span></span> <span data-ttu-id="e4fdf-171">Noklusējuma veidnes vērtība ir **Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-171">The default template value is **Project Service Automation**.</span></span>
- <span data-ttu-id="e4fdf-172">**PaymentTerms** kartējums ir jāatjaunina, lai tas atspoguļotu derīgus maksājuma nosacījumus risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-172">The **PaymentTerms** mapping must be updated so that it reflects valid terms of payment in Finance.</span></span> <span data-ttu-id="e4fdf-173">Varat arī noņemt kartējumu no projekta uzdevuma.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-173">You can also remove the mapping from the project task.</span></span> <span data-ttu-id="e4fdf-174">Noklusējuma vērtību kartē ir demonstrācijas datu noklusējuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-174">The default value map has default values for demo data.</span></span> <span data-ttu-id="e4fdf-175">Nākamajā tabulā ir parādītas Project Service Automation vērtības.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-175">The following table shows the values in Project Service Automation.</span></span>

    | <span data-ttu-id="e4fdf-176">Vērtība</span><span class="sxs-lookup"><span data-stu-id="e4fdf-176">Value</span></span> | <span data-ttu-id="e4fdf-177">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e4fdf-177">Description</span></span>   |
    |-------|---------------|
    | <span data-ttu-id="e4fdf-178">1</span><span class="sxs-lookup"><span data-stu-id="e4fdf-178">1</span></span>     | <span data-ttu-id="e4fdf-179">Apmaksa pēc 30 dienām</span><span class="sxs-lookup"><span data-stu-id="e4fdf-179">Net 30</span></span>        |
    | <span data-ttu-id="e4fdf-180">2</span><span class="sxs-lookup"><span data-stu-id="e4fdf-180">2</span></span>     | <span data-ttu-id="e4fdf-181">Apmaksa pēc 30 dienām ar 2% atlaidi, ja apmaksa veic 10 dienu laikā</span><span class="sxs-lookup"><span data-stu-id="e4fdf-181">2% 10, Net 30</span></span> |
    | <span data-ttu-id="e4fdf-182">3</span><span class="sxs-lookup"><span data-stu-id="e4fdf-182">3</span></span>     | <span data-ttu-id="e4fdf-183">Apmaksa pēc 45 dienām</span><span class="sxs-lookup"><span data-stu-id="e4fdf-183">Net 45</span></span>        |
    | <span data-ttu-id="e4fdf-184">4</span><span class="sxs-lookup"><span data-stu-id="e4fdf-184">4</span></span>     | <span data-ttu-id="e4fdf-185">Apmaksa pēc 60 dienām</span><span class="sxs-lookup"><span data-stu-id="e4fdf-185">Net 60</span></span>        |

## <a name="power-query"></a><span data-ttu-id="e4fdf-186">Power Query</span><span class="sxs-lookup"><span data-stu-id="e4fdf-186">Power Query</span></span>

<span data-ttu-id="e4fdf-187">Ja ir izpildīti tālāk minētie nosacījumi, ir jāizmanto Microsoft Power Query programmai Excel, lai filtrētu datus:</span><span class="sxs-lookup"><span data-stu-id="e4fdf-187">You must use Microsoft Power Query for Excel to filter data if the following conditions are met:</span></span>

- <span data-ttu-id="e4fdf-188">Jums ir pārdošanas pasūtījumi risinājumā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-188">You have sales orders in Dynamics 365 Sales.</span></span>
- <span data-ttu-id="e4fdf-189">Jums ir vairākas organizācijas struktūrvienības Project Service Automation, un šīs organizācijas struktūrvienības tiks kartētas uz vairākām juridiskām personām risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-189">You have multiple organizational units in Project Service Automation, and these organizational units will be mapped to multiple legal entities in Finance.</span></span>

<span data-ttu-id="e4fdf-190">Ja ir jāizmanto Power Query, ievērojiet šīs vadlīnijas:</span><span class="sxs-lookup"><span data-stu-id="e4fdf-190">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="e4fdf-191">Projektu un līgumu (PSA uz Fin un Ops) veidnei ir noklusējuma filtrs, kas ietver tikai pārdošanas pasūtījumus ar tipu **Darba vienums (msdyn\_ordertype = 192350001)**.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-191">The Projects and contracts (PSA to Fin and Ops) template has a default filter that includes only sales orders of the **Work item (msdyn\_ordertype = 192350001)** type.</span></span> <span data-ttu-id="e4fdf-192">Šis filtrs palīdz nodrošināt, lai projekta līgumi netiktu izveidoti pārdošanas pasūtījumiem risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-192">This filter helps guarantee that project contracts aren't created for sales orders in Finance.</span></span> <span data-ttu-id="e4fdf-193">Ja izveidojat savu veidni, šis filtrs ir jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-193">If you create your own template, you must add this filter.</span></span>
- <span data-ttu-id="e4fdf-194">Ir jāizveido Power Query filtrs, kurā ir iekļautas tikai tās līguma organizācijas, kas jāsinhronizē ar integrācijas savienojuma kopas juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-194">You must create a Power Query filter that includes only the contract organizations that should be synchronized to the legal entity of the integration connection set.</span></span> <span data-ttu-id="e4fdf-195">Piemēram, projekta līgumi, kas jums ir ar līguma organizācijas struktūrvienību Contoso US, ir jāsinhronizē ar USSI juridisko personu, bet projekta līgumi, kas jums ir ar organizācijas struktūrvienību Contoso Global, ir jāsinhronizē ar USMF juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-195">For example, project contracts that you have with the contract organizational unit of Contoso US should be synchronized to the USSI legal entity, but project contracts that you have with the contract organizational unit of Contoso Global should be synchronized to the USMF legal entity.</span></span> <span data-ttu-id="e4fdf-196">Ja nepievienosit šo filtru jūsu uzdevumu kartējumam, visi projekta līgumi tiks sinhronizēti ar juridisko personu, kas ir definēta savienojuma kopai, neatkarīgi no līguma organizācijas struktūrvienības.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-196">If you don't add this filter to your task mapping, all project contracts will be synchronized to the legal entity that is defined for the connection set, regardless of the contract organizational unit.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e4fdf-197">Veidņu kartēšana datu integrācijā</span><span class="sxs-lookup"><span data-stu-id="e4fdf-197">Template mapping in Data integration</span></span>

> [!NOTE] 
> <span data-ttu-id="e4fdf-198">Lauki **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** un **AddressZipCode** nav iekļauti projektu līgumu noklusējuma kartējumā.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-198">The **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, and **AddressZipCode** fields aren't included in the default mapping for project contracts.</span></span> <span data-ttu-id="e4fdf-199">Varat pievienot kartējumus, ja jums nepieciešams, lai šie dati tiktu sinhronizēti projekta līgumiem.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-199">You can add the mappings if you require that this data be synchronized for project contracts.</span></span>
>
> <span data-ttu-id="e4fdf-200">Lauki **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** un **ProjectType** nav iekļauti projektu noklusējuma kartējumā</span><span class="sxs-lookup"><span data-stu-id="e4fdf-200">The **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fields aren't included in the default mapping for projects.</span></span> <span data-ttu-id="e4fdf-201">Varat pievienot kartējumus, ja jums nepieciešams, lai šie dati tiktu sinhronizēti projektiem.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-201">You can add the mappings if you require that this data be synchronized for projects.</span></span>

<span data-ttu-id="e4fdf-202">Nākamajās ilustrācijās ir redzami piemēri no veidnes uzdevumu kartējumiem datu integrācijā.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-202">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="e4fdf-203">Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-203">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e4fdf-204">[![Projekta līguma veidnes kartēšana](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="e4fdf-204">[![Project contract template mapping](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span></span>

<span data-ttu-id="e4fdf-205">[![Projekta veidnes kartēšana](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="e4fdf-205">[![Project template mapping](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span></span>

<span data-ttu-id="e4fdf-206">[![Projekta līguma rindu veidnes kartēšana](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="e4fdf-206">[![Project contract lines template mapping](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span></span>

<span data-ttu-id="e4fdf-207">[![Projekta līguma rindu atskaites punkta veidnes kartēšana](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="e4fdf-207">[![Project contract line milestone template mapping](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span></span>

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a><span data-ttu-id="e4fdf-208">Projekta līguma rindu atskaites punktu kartēšana projektos un līgumos (PSA 3.x uz Dynamics) — v2 veidne:</span><span class="sxs-lookup"><span data-stu-id="e4fdf-208">Project contract line milestone mapping in the Projects and Contracts (PSA 3.x to Dynamics) - v2 template:</span></span>

<span data-ttu-id="e4fdf-209">[![Projekta līguma rindu atskaites punkta kartēšana ar versiju, kurā ir divas veidnes](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span><span class="sxs-lookup"><span data-stu-id="e4fdf-209">[![Project contract line milestone mapping with version two template](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span></span>