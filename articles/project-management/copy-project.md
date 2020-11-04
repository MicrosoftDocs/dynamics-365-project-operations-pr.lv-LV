---
title: Projekta kopēšana
description: Šajā tēmā sniegta informācija par projektu kopēšanu risinājumā Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080385"
---
# <a name="copy-a-project"></a><span data-ttu-id="460c0-103">Projekta kopēšana</span><span class="sxs-lookup"><span data-stu-id="460c0-103">Copy a project</span></span>

<span data-ttu-id="460c0-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="460c0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="460c0-105">Izmantojot Dynamics 365 Project Operations, varat ātri izveidot jaunus projektus, atlasot **Kopēt projektu** veidlapā **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="460c0-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="460c0-106">Lai kopētu projektu, atveriet to projektu, ko vēlaties kopēt, un pēc tam atlasiet **Kopēt projektu**.</span><span class="sxs-lookup"><span data-stu-id="460c0-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="460c0-107">Ar šo darbību tiks kopēta šāda informācija:</span><span class="sxs-lookup"><span data-stu-id="460c0-107">The action will copy:</span></span>

- <span data-ttu-id="460c0-108">Projekta rekvizīti</span><span class="sxs-lookup"><span data-stu-id="460c0-108">Project properties</span></span>
- <span data-ttu-id="460c0-109">Darba sadalījuma struktūra</span><span class="sxs-lookup"><span data-stu-id="460c0-109">The Work breakdown structure</span></span>
- <span data-ttu-id="460c0-110">Projekta darba grupas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="460c0-110">Project team members</span></span>
- <span data-ttu-id="460c0-111">Projekta aprēķins</span><span class="sxs-lookup"><span data-stu-id="460c0-111">Project estimates</span></span>
- <span data-ttu-id="460c0-112">Projekta izmaksu aplēses</span><span class="sxs-lookup"><span data-stu-id="460c0-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="460c0-113">Projekta rekvizīti</span><span class="sxs-lookup"><span data-stu-id="460c0-113">Project properties</span></span>

<span data-ttu-id="460c0-114">Kopējot projektu, tiek kopētas šādu lauku vērtības:</span><span class="sxs-lookup"><span data-stu-id="460c0-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="460c0-115">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="460c0-115">Name</span></span>
- <span data-ttu-id="460c0-116">Apraksts</span><span class="sxs-lookup"><span data-stu-id="460c0-116">Description</span></span>
- <span data-ttu-id="460c0-117">Klients</span><span class="sxs-lookup"><span data-stu-id="460c0-117">Customer</span></span>
- <span data-ttu-id="460c0-118">Kalendāra veidne</span><span class="sxs-lookup"><span data-stu-id="460c0-118">Calendar Template</span></span>
- <span data-ttu-id="460c0-119">Valūta</span><span class="sxs-lookup"><span data-stu-id="460c0-119">Currency</span></span>
- <span data-ttu-id="460c0-120">Līgumslēdzēja vienība</span><span class="sxs-lookup"><span data-stu-id="460c0-120">Contracting Unit</span></span>
- <span data-ttu-id="460c0-121">Projekta vadītājs</span><span class="sxs-lookup"><span data-stu-id="460c0-121">Project Manager</span></span>
- <span data-ttu-id="460c0-122">Statuss</span><span class="sxs-lookup"><span data-stu-id="460c0-122">Status</span></span>
- <span data-ttu-id="460c0-123">Vispārējs projekta statuss</span><span class="sxs-lookup"><span data-stu-id="460c0-123">Overall Project Status</span></span>
- <span data-ttu-id="460c0-124">Komentāri</span><span class="sxs-lookup"><span data-stu-id="460c0-124">Comments</span></span>
- <span data-ttu-id="460c0-125">Novērtējumi</span><span class="sxs-lookup"><span data-stu-id="460c0-125">Estimates</span></span>
- <span data-ttu-id="460c0-126">Prognozējamais sākuma datums</span><span class="sxs-lookup"><span data-stu-id="460c0-126">Estimated Start Date</span></span>
- <span data-ttu-id="460c0-127">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="460c0-127">Finish Date</span></span>
- <span data-ttu-id="460c0-128">Ieguldījums (stundas)</span><span class="sxs-lookup"><span data-stu-id="460c0-128">Effort (Hours)</span></span>
- <span data-ttu-id="460c0-129">Novērtētās darba izmaksas</span><span class="sxs-lookup"><span data-stu-id="460c0-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="460c0-130">Novērtētās izdevumu izmaksas</span><span class="sxs-lookup"><span data-stu-id="460c0-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="460c0-131">Darba sadalījuma struktūra</span><span class="sxs-lookup"><span data-stu-id="460c0-131">Work breakdown structure</span></span>

<span data-ttu-id="460c0-132">Kopējot projektu, tiek kopēts visa ar resursu ielādētā darba sadalījuma struktūra.</span><span class="sxs-lookup"><span data-stu-id="460c0-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="460c0-133">Nosauktie resursi tiek aizstāti ar vispārējiem resursiem.</span><span class="sxs-lookup"><span data-stu-id="460c0-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="460c0-134">Ja nosauktajiem resursiem nav tādas pašas darba stundas kā vispārējam resursam, grafiks tiks pārrēķināts, un var mainīties uzdevumu ilgums.</span><span class="sxs-lookup"><span data-stu-id="460c0-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="460c0-135">Projekta darba grupas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="460c0-135">Project team members</span></span>

<span data-ttu-id="460c0-136">Kad tiek kopēta projekta darba grupa no avota projekta, tiek kopēti vispārējie resursi.</span><span class="sxs-lookup"><span data-stu-id="460c0-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="460c0-137">Arī vispārējo resursu piešķires tiek paturētas tādas, kādas tās bija avota projektā.</span><span class="sxs-lookup"><span data-stu-id="460c0-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="460c0-138">Nosauktie resursi tiks konvertēti par vispārīgiem darba grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="460c0-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="460c0-139">Novērtējumi</span><span class="sxs-lookup"><span data-stu-id="460c0-139">Estimates</span></span>

<span data-ttu-id="460c0-140">Kopējot projektu, gan resursu, gan izmaksu aprēķinu rindas tiek kopētas no avota projekta.</span><span class="sxs-lookup"><span data-stu-id="460c0-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="460c0-141">Informāciju par to, kā programmiski piekļūt projekta kopēšanai, skatiet rakstā [Projekta veidņu izstrāde, izmantojot projekta kopēšanu](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="460c0-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>
