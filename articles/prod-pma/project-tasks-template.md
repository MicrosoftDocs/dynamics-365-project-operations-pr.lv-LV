---
title: Projekta uzdevumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir aprakstīta veidne un pamata uzdevums, kas tiek izmantots projekta uzdevumu sinhronizēšanai tieši no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Finance.
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
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080426"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="4a4f1-103">Projekta uzdevumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4a4f1-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4a4f1-104">Šajā tēmā ir aprakstīta veidne un pamata uzdevums, kas tiek izmantots projekta uzdevumu sinhronizēšanai tieši no Dynamics 365 Project Service Automation uz Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="4a4f1-105">8.0 versijā varat izmantot projekta uzdevumu integrāciju, izdevumu darbības kategorijas, stundu aprēķinus, izdevumu aprēķinus un funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="4a4f1-106">Ja izmantojat Enterprise edition 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu aprēķinus, izdevumu aprēķinus un faktiskos datus un konfigurēt funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="4a4f1-107">Ja ir jāatiestata uzskaites sadales, ieteicams instalēt arī KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="4a4f1-108">Faktisko datu integrācija ir pieejama 8.0.1 vai jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="4a4f1-109">Datu plūsma Project Service Automation uz Finance</span><span class="sxs-lookup"><span data-stu-id="4a4f1-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="4a4f1-110">Project Service Automation uz Finance integrācijas risinājumam tiek izmantots datu integrācijas līdzeklis, lai sinhronizētu datus starp Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="4a4f1-111">Integrācijas veidne, kas ir pieejama kopā ar datu integrācijas līdzekli, iespējo datu plūsmu par projekta uzdevumiem no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="4a4f1-112">Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti starp Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="4a4f1-113">[![Datu plūsma Project Service Automation integrācijai ar Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="4a4f1-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="4a4f1-114">Veidne un uzdevums</span><span class="sxs-lookup"><span data-stu-id="4a4f1-114">Template and task</span></span>

<span data-ttu-id="4a4f1-115">Lai piekļūtu veidnei, Microsoft Power Apps administrēšanas centrā atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts** , lai atlasītu publiskas veidnes.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-115">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4a4f1-116">Šajā tēmā ir aprakstīta veidne un pamata uzdevums, kas tiek izmantots projekta uzdevumu sinhronizēšanai tieši no Project Service Automation uz Finance:</span><span class="sxs-lookup"><span data-stu-id="4a4f1-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="4a4f1-117">**Veidnes nosaukums datu integrācijā:** Projekta uzdevumi (PSA uz Fin un Ops)</span><span class="sxs-lookup"><span data-stu-id="4a4f1-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="4a4f1-118">**Projekta uzdevuma nosaukums:** Projekta uzdevumi</span><span class="sxs-lookup"><span data-stu-id="4a4f1-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="4a4f1-119">Pirms projekta uzdevumu sinhronizēšanas, ir jāsinhronizē projekta līgumi un projekti.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="4a4f1-120">Entītiju kopa</span><span class="sxs-lookup"><span data-stu-id="4a4f1-120">Entity set</span></span>

| <span data-ttu-id="4a4f1-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4a4f1-121">Project Service Automation</span></span> | <span data-ttu-id="4a4f1-122">Finanses</span><span class="sxs-lookup"><span data-stu-id="4a4f1-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="4a4f1-123">Projekta uzdevumi</span><span class="sxs-lookup"><span data-stu-id="4a4f1-123">Project Tasks</span></span>              | <span data-ttu-id="4a4f1-124">Projekta uzdevuma integrācijas entītija</span><span class="sxs-lookup"><span data-stu-id="4a4f1-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="4a4f1-125">Entītijas plūsma</span><span class="sxs-lookup"><span data-stu-id="4a4f1-125">Entity flow</span></span>

<span data-ttu-id="4a4f1-126">Projekta uzdevumi tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta darbības.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="4a4f1-127">Priekšnosacījumi un kartēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4a4f1-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="4a4f1-128">Pirms projekta uzdevumu sinhronizēšanas, ir jāsinhronizē projekta līgumi un projekti.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="4a4f1-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="4a4f1-129">Power Query</span></span>

<span data-ttu-id="4a4f1-130">Ja ir izpildīts šis nosacījums, ir jāizmanto Microsoft Power Query programmai Excel, lai filtrētu datus:</span><span class="sxs-lookup"><span data-stu-id="4a4f1-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="4a4f1-131">Projekta uzdevumā ir resursam specifiski ieraksti.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="4a4f1-132">Ja ir jāizmanto Power Query, ievērojiet šo vadlīniju:</span><span class="sxs-lookup"><span data-stu-id="4a4f1-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="4a4f1-133">Projekta uzdevumu (PSA uz Fin un Ops) veidnei ir noklusējuma filtrs, kas projekta uzdevumam neietver resursu specifiskos ierakstus, iestatot filtru sadaļā **IsLineTask** uz **Aplams**.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="4a4f1-134">Ja izveidojat savu veidni, šis filtrs ir jāpievieno.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4a4f1-135">Veidņu kartēšana datu integrācijā</span><span class="sxs-lookup"><span data-stu-id="4a4f1-135">Template mapping in Data integration</span></span>

<span data-ttu-id="4a4f1-136">Nākamajā ilustrācijā ir redzams piemērs no veidnes uzdevumu kartējumiem datu integrācijā.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="4a4f1-137">Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="4a4f1-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="4a4f1-138">[![Veidņu kartēšana](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="4a4f1-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
