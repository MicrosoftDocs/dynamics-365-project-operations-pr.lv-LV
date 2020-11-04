---
title: Project Service Automation pārskats
description: Šajā tēmā ir sniegta informācija par Dynamics 365 Project Service Automation integrācijas uz Dynamics 365 Finance risinājumu.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080585"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="3bf23-103">Project Service Automation pārskats</span><span class="sxs-lookup"><span data-stu-id="3bf23-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3bf23-104">Project Service Automation uz Finance integrācijas risinājumam tiek izmantots datu integrācijas līdzeklis, lai sinhronizētu datus starp Dynamics 365 Finance un Dynamics 365 Project Service Automation, izmantojot Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3bf23-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="3bf23-105">Integrēšanas veidnes, kas ir pieejamas ar datu integrācijas līdzekli, iespējo projektu plūsmu, projekta līgumus, projekta līguma rindas, projekta līgumu rindu atskaites punktus, projekta uzdevumus, izdevumu darbību kategorijas, stundu aprēķinus un izdevumu tāmes no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf23-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="3bf23-106">Ja izmantojat versiju 7.3.0, ir jāinstalē KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="3bf23-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="3bf23-107">Tad varēsit integrēt fiksētas cenas projektus.</span><span class="sxs-lookup"><span data-stu-id="3bf23-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="3bf23-108">Ja izmantojat versiju 7.3.0 un no Project Service Automation ir jāievieš maksas transakcijas, jums ir jāinstalē KB 4345320, lai projekta rēķinā iekļautu šīs maksas.</span><span class="sxs-lookup"><span data-stu-id="3bf23-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="3bf23-109">Ja izmantojat versiju 8.0, varēsit izmantot projekta uzdevumu integrāciju, izdevumu darbības kategorijas, stundu aprēķinus, izdevumu aprēķinus un funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="3bf23-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="3bf23-110">Ja izmantojat versiju 8.0.1 vai jaunāku versiju, jūs varēsit sinhronizēt faktiskos datus.</span><span class="sxs-lookup"><span data-stu-id="3bf23-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="3bf23-111">Lai varētu integrēt Project Service Automation sistēmā Finance, ir jākonfigurē Project Service Automation integrācijas parametri.</span><span class="sxs-lookup"><span data-stu-id="3bf23-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="3bf23-112">Papildinformācija: [Project Service Automation integrācijas parametri](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3bf23-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="3bf23-113">Šis integrācijas risinājums nodrošina tiešu sinhronizāciju šādos gadījumos:</span><span class="sxs-lookup"><span data-stu-id="3bf23-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="3bf23-114">Project Service Automation uzturēt projekta līgumus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf23-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3bf23-115">Project Service Automation izveidot projektus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf23-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3bf23-116">Project Service Automation uzturēt projekta līguma rindas, kā arī sinhronizēt tās tieši no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf23-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3bf23-117">Project Service Automation uzturēt projekta līguma rindu atskaites punktus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf23-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3bf23-118">Project Service Automation uzturēt projekta uzdevumus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf23-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3bf23-119">Uzturēt izdevumu transakciju kategorijas sistēmā Finance, kā arī sinhronizēt tās tieši no Finance uz Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3bf23-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="3bf23-120">Project Service Automation izveidot projekta stundu novērtējumus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf23-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3bf23-121">Project Service Automation izveidot projekta izdevumu novērtējumus, kā arī sinhronizēt tos tieši no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf23-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="3bf23-122">Veidot projekta laika, izdevumu un maksas faktiskos datus Project Service Automation, un Project Service Automation integrācijas žurnālā veidot projekta darbības, lai tās varētu grāmatot sistēmā Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf23-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="3bf23-123">Datu sinhronizācija</span><span class="sxs-lookup"><span data-stu-id="3bf23-123">Data synchronization</span></span>

<span data-ttu-id="3bf23-124">Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti kā daļa no integrēšanas starp Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf23-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="3bf23-125">Pašlaik nav pieejamas visas veidnes.</span><span class="sxs-lookup"><span data-stu-id="3bf23-125">Not all templates are currently available.</span></span> <span data-ttu-id="3bf23-126">Veidnes tiks izlaistas, kad tās būs pabeigtas.</span><span class="sxs-lookup"><span data-stu-id="3bf23-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="3bf23-127">[![Project Service Automation integrācija ar Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="3bf23-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="3bf23-128">Finance sistēmas prasības</span><span class="sxs-lookup"><span data-stu-id="3bf23-128">System requirements for Finance</span></span>

<span data-ttu-id="3bf23-129">Lai izmantotu Project Service Automation uz Finance integrācijas risinājumu, ir jāinstalē Enterprise Edition 7.3 ar platformas atjauninājumu 12 vai jaunāku versiju.</span><span class="sxs-lookup"><span data-stu-id="3bf23-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="3bf23-130">Project Service Automation sistēmas prasības</span><span class="sxs-lookup"><span data-stu-id="3bf23-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="3bf23-131">Lai izmantotu Project Service Automation uz Finance integrācijas risinājumu, ir jāinstalē šādi komponenti:</span><span class="sxs-lookup"><span data-stu-id="3bf23-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="3bf23-132">Dynamics 365 Project Service Automation versija 9.0.0.0 vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="3bf23-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="3bf23-133">Izredzes uz naudas risinājumu pakalpojumam Dynamics 365 Sales, versija 1.14.0.0 (V14) vai jaunāka versija</span><span class="sxs-lookup"><span data-stu-id="3bf23-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="3bf23-134">Project Service Automation uz Finance risinājums Dynamics 365 Project Service Automation 1.0.0.0 vai jaunākai versijai</span><span class="sxs-lookup"><span data-stu-id="3bf23-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="3bf23-135">Instalējiet Project Service Automation uz Finance integrācijas risinājumu savā Project Service Automation instancē</span><span class="sxs-lookup"><span data-stu-id="3bf23-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="3bf23-136">Lejupielādējiet Project Service Automation uz Finance integrācijas risinājumu no [Microsoft lejupielādes centra](https://www.microsoft.com/download/details.aspx?id=57016) un izpildiet risinājumā iekļautos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="3bf23-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
