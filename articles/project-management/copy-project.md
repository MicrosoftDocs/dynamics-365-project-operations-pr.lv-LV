---
title: Projekta kopēšana
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumiem risinājumā Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091263"
---
# <a name="copy-a-project"></a><span data-ttu-id="26a82-103">Projekta kopēšana</span><span class="sxs-lookup"><span data-stu-id="26a82-103">Copy a project</span></span>

<span data-ttu-id="26a82-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="26a82-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="26a82-105">Izmantojot opciju Dynamics 365 Project Operations, varat ātri izveidot jaunus projektus, atlasot **Kopēt projektu** veidlapā **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="26a82-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="26a82-106">Lai kopētu projektu, atveriet to projektu, ko vēlaties kopēt, un pēc tam atlasiet **Kopēt projektu**.</span><span class="sxs-lookup"><span data-stu-id="26a82-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="26a82-107">Ar šo darbību tiek nokopēti tālāk norādītie vienumi.</span><span class="sxs-lookup"><span data-stu-id="26a82-107">The action will copy the following:</span></span>

- <span data-ttu-id="26a82-108">Projekta rekvizīti</span><span class="sxs-lookup"><span data-stu-id="26a82-108">Project properties</span></span> 
- <span data-ttu-id="26a82-109">Darba sadalījuma struktūra</span><span class="sxs-lookup"><span data-stu-id="26a82-109">Work breakdown structure</span></span>
- <span data-ttu-id="26a82-110">Projekta darba grupas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="26a82-110">Project team members</span></span>
- <span data-ttu-id="26a82-111">Projekta aprēķins</span><span class="sxs-lookup"><span data-stu-id="26a82-111">Project estimates</span></span>
- <span data-ttu-id="26a82-112">Projekta izmaksu aplēses</span><span class="sxs-lookup"><span data-stu-id="26a82-112">Project expense estimates</span></span>
- <span data-ttu-id="26a82-113">Projekta materiālu aprēķini</span><span class="sxs-lookup"><span data-stu-id="26a82-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="26a82-114">Projekta rekvizīti</span><span class="sxs-lookup"><span data-stu-id="26a82-114">Project properties</span></span>

<span data-ttu-id="26a82-115">Kopējot projektu, tiek kopētas šādu lauku vērtības:</span><span class="sxs-lookup"><span data-stu-id="26a82-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="26a82-116">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="26a82-116">Name</span></span>
- <span data-ttu-id="26a82-117">Apraksts</span><span class="sxs-lookup"><span data-stu-id="26a82-117">Description</span></span>
- <span data-ttu-id="26a82-118">Klients</span><span class="sxs-lookup"><span data-stu-id="26a82-118">Customer</span></span>
- <span data-ttu-id="26a82-119">Kalendāra veidne</span><span class="sxs-lookup"><span data-stu-id="26a82-119">Calendar Template</span></span>
- <span data-ttu-id="26a82-120">Valūta</span><span class="sxs-lookup"><span data-stu-id="26a82-120">Currency</span></span>
- <span data-ttu-id="26a82-121">Līgumslēdzēja vienība</span><span class="sxs-lookup"><span data-stu-id="26a82-121">Contracting Unit</span></span>
- <span data-ttu-id="26a82-122">Projekta vadītājs</span><span class="sxs-lookup"><span data-stu-id="26a82-122">Project Manager</span></span>
- <span data-ttu-id="26a82-123">Statuss</span><span class="sxs-lookup"><span data-stu-id="26a82-123">Status</span></span>
- <span data-ttu-id="26a82-124">Vispārējs projekta statuss</span><span class="sxs-lookup"><span data-stu-id="26a82-124">Overall Project Status</span></span>
- <span data-ttu-id="26a82-125">Komentāri</span><span class="sxs-lookup"><span data-stu-id="26a82-125">Comments</span></span>
- <span data-ttu-id="26a82-126">Aprēķini</span><span class="sxs-lookup"><span data-stu-id="26a82-126">Estimates</span></span>
- <span data-ttu-id="26a82-127">Paredzamais sākuma datums: šis ir datums, kad projekts tiek izveidots no kopijas.</span><span class="sxs-lookup"><span data-stu-id="26a82-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="26a82-128">Paredzamais beigu datums: šis datums tiek pielāgots atkarībā no jaunā jeb no kopijas izveidotā projekta sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="26a82-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="26a82-129">Ieguldījums (stundas)</span><span class="sxs-lookup"><span data-stu-id="26a82-129">Effort (Hours)</span></span>
- <span data-ttu-id="26a82-130">Novērtētās darba izmaksas</span><span class="sxs-lookup"><span data-stu-id="26a82-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="26a82-131">Novērtētās izdevumu izmaksas</span><span class="sxs-lookup"><span data-stu-id="26a82-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="26a82-132">Prognozēto materiālu izmaksas</span><span class="sxs-lookup"><span data-stu-id="26a82-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="26a82-133">Projekta kopēšana ir ilgstoša darbība.</span><span class="sxs-lookup"><span data-stu-id="26a82-133">Copy project is a long running operation.</span></span> <span data-ttu-id="26a82-134">Tiek kopēti arī projekta ieraksti, saistītie atribūti un daudzas saistītās entītijas.</span><span class="sxs-lookup"><span data-stu-id="26a82-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="26a82-135">Darbības ilguma dēļ pēc kopēšanas sākšanas mērķa projekta lapa tiek bloķēta rediģēšanai, līdz kopēšanas darbība ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="26a82-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="26a82-136">Darba sadalījuma struktūra</span><span class="sxs-lookup"><span data-stu-id="26a82-136">Work breakdown structure</span></span>

<span data-ttu-id="26a82-137">Kopējot projektu, tiek kopēts visa ar resursu ielādētā darba sadalījuma struktūra.</span><span class="sxs-lookup"><span data-stu-id="26a82-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="26a82-138">Nosauktie resursi tiek aizstāti ar vispārējiem resursiem.</span><span class="sxs-lookup"><span data-stu-id="26a82-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="26a82-139">Ja nosauktajiem resursiem nav tādas pašas darba stundas kā vispārējam resursam, grafiks tiks pārrēķināts, un var mainīties uzdevumu ilgums.</span><span class="sxs-lookup"><span data-stu-id="26a82-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="26a82-140">Projekta darba grupas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="26a82-140">Project team members</span></span>

<span data-ttu-id="26a82-141">Kad tiek kopēta projekta darba grupa no avota projekta, tiek kopēti vispārējie resursi.</span><span class="sxs-lookup"><span data-stu-id="26a82-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="26a82-142">Arī vispārējo resursu piešķires tiek paturētas tādas, kādas tās bija avota projektā.</span><span class="sxs-lookup"><span data-stu-id="26a82-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="26a82-143">Nosauktie resursi tiks konvertēti par vispārīgiem darba grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="26a82-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="26a82-144">Aprēķini</span><span class="sxs-lookup"><span data-stu-id="26a82-144">Estimates</span></span>

<span data-ttu-id="26a82-145">Kad tiek kopēts projekts, izdevumu un materiālu aprēķinu rindas tiek kopētas no avota projekta.</span><span class="sxs-lookup"><span data-stu-id="26a82-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="26a82-146">Informāciju par to, kā programmiski piekļūt projekta kopēšanai, skatiet rakstā [Projekta veidņu izstrāde, izmantojot projekta kopēšanu](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="26a82-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
