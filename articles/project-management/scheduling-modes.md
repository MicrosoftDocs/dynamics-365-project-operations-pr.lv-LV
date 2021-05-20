---
title: Plānošanas režīmi
description: Šajā tēmā ir sniegta informācija par plānošanas režīmiem.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981444"
---
# <a name="scheduling-modes"></a><span data-ttu-id="05f25-103">Plānošanas režīmi</span><span class="sxs-lookup"><span data-stu-id="05f25-103">Scheduling modes</span></span>

<span data-ttu-id="05f25-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="05f25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="05f25-105">Dynamics 365 Project Operations sniedz organizācijām iespēju definēt, kā pārvaldīt galveno mainīgo izmaiņas darba sadalījuma struktūras uzdevumos.</span><span class="sxs-lookup"><span data-stu-id="05f25-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="05f25-106">Pamatojoties uz organizācijas specifiskajām vajadzībām, projekta vadītāji var veikt plānošanas režīma izmaiņas projekta izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="05f25-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="05f25-107">Programmā Project Operations ir pieejami trīs plānošanas režīmi.</span><span class="sxs-lookup"><span data-stu-id="05f25-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="05f25-108">Fiksēts ilgums (šis ir noklusējuma režīms)</span><span class="sxs-lookup"><span data-stu-id="05f25-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="05f25-109">Fiksēts darbs</span><span class="sxs-lookup"><span data-stu-id="05f25-109">Fixed work</span></span>
  - <span data-ttu-id="05f25-110">Fiksētas vienības</span><span class="sxs-lookup"><span data-stu-id="05f25-110">Fixed units</span></span>

<span data-ttu-id="05f25-111">Vērtības, ko ietekmē noteikta plānošanas režīma definēšana, nosaka šāda formula:</span><span class="sxs-lookup"><span data-stu-id="05f25-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="05f25-112">Ieguldījums (*Darbs*) = Ilgums x vienības</span><span class="sxs-lookup"><span data-stu-id="05f25-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="05f25-113">Definējot projekta plānošanas režīmu, tiek iestatīta viena no šīm vērtībām, ko pēc tam nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="05f25-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="05f25-114">Paturot šo vērtību kā nemainīgu, tā tiek iestatīta kā prioritāte, kas nozīmē, ka sistēma to nemaina, kad tiek mainītas abas pārējās vērtības.</span><span class="sxs-lookup"><span data-stu-id="05f25-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="05f25-115">Tālāk redzamajā tabulā ir sniegta informācija par katra konkrētā režīma atlases ietekmi.</span><span class="sxs-lookup"><span data-stu-id="05f25-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="05f25-116">**Šajā uzdevumā**</span><span class="sxs-lookup"><span data-stu-id="05f25-116">**In this task**</span></span>             | <span data-ttu-id="05f25-117">**Ja tiek pārskatītas vienības**</span><span class="sxs-lookup"><span data-stu-id="05f25-117">**If you revise units**</span></span>   | <span data-ttu-id="05f25-118">**Ja tiek pārskatīts ilgums**</span><span class="sxs-lookup"><span data-stu-id="05f25-118">**If you revise duration**</span></span> | <span data-ttu-id="05f25-119">**Ja tiek pārskatīts ieguldījums**</span><span class="sxs-lookup"><span data-stu-id="05f25-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="05f25-120">Fiksētu vienību uzdevums</span><span class="sxs-lookup"><span data-stu-id="05f25-120">Fixed units task</span></span>     | <span data-ttu-id="05f25-121">Ilgums tiek pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="05f25-121">Duration is recalculated.</span></span> | <span data-ttu-id="05f25-122">Ieguldījums tiek pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="05f25-122">Effort is recalculated.</span></span>    | <span data-ttu-id="05f25-123">Ilgums tiek pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="05f25-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="05f25-124">Fiksēta ieguldījuma uzdevums</span><span class="sxs-lookup"><span data-stu-id="05f25-124">Fixed effort task</span></span>    | <span data-ttu-id="05f25-125">Ilgums tiek pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="05f25-125">Duration is recalculated.</span></span> | <span data-ttu-id="05f25-126">Vienības tiek pārrēķinātas.</span><span class="sxs-lookup"><span data-stu-id="05f25-126">Units are recalculated.</span></span>    | <span data-ttu-id="05f25-127">Ilgums tiek pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="05f25-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="05f25-128">Fiksēta ilguma uzdevums</span><span class="sxs-lookup"><span data-stu-id="05f25-128">Fixed duration task</span></span>  | <span data-ttu-id="05f25-129">Ieguldījums tiek pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="05f25-129">Effort is recalculated.</span></span>   | <span data-ttu-id="05f25-130">Ieguldījums tiek pārrēķināts.</span><span class="sxs-lookup"><span data-stu-id="05f25-130">Effort is recalculated.</span></span>    | <span data-ttu-id="05f25-131">Vienības tiek pārrēķinātas.</span><span class="sxs-lookup"><span data-stu-id="05f25-131">Units are recalculated.</span></span>   |

<span data-ttu-id="05f25-132">Papildinformāciju par konkrētā režīma nosacījumiem skatiet sadaļā [Uzdevuma tipa mainīšana precīzākai plānošanai](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="05f25-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="05f25-133">Tēmā tiek lietots vārds **Darbs**, nevis **Ieguldījums**.</span><span class="sxs-lookup"><span data-stu-id="05f25-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="05f25-134">Organizācijas plānošanas režīma maiņa</span><span class="sxs-lookup"><span data-stu-id="05f25-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="05f25-135">Lai definētu organizācijas plānošanas režīmu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="05f25-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="05f25-136">Dodieties uz **Iestatījumi** \> **Vispārīgi** \> **Parametri** un pēc tam atlasiet projekta parametru.</span><span class="sxs-lookup"><span data-stu-id="05f25-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="05f25-137">Lapā **Projekta parametri** atlasiet organizācijas noklusējuma plānošanas režīmu un pēc tam definējiet projekta vadītāja iespēju pārlabot iestatījumu, izveidojot jaunu projektu.</span><span class="sxs-lookup"><span data-stu-id="05f25-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="05f25-138">Plānošanas režīma iestatījuma maiņa projektam</span><span class="sxs-lookup"><span data-stu-id="05f25-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="05f25-139">Ja organizācija ļauj projekta vadītājam pārlabot noklusējuma plānošanas režīmu, projekta vadītājs var veikt šīs izmaiņas, izveidojot jaunu projektu.</span><span class="sxs-lookup"><span data-stu-id="05f25-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="05f25-140">Tomēr pēc projekta saglabāšanas plānošanas režīmu nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="05f25-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="05f25-141">Kopēti projekti</span><span class="sxs-lookup"><span data-stu-id="05f25-141">Copied projects</span></span>

<span data-ttu-id="05f25-142">Tā kā projekts tiek izveidots, veicot projekta kopēšanas darbību, projekta vadītājs nevar iestatīt plānošanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="05f25-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="05f25-143">Mērķa projekta režīms vienmēr tiek iestatīts pēc noklusējuma, kas definēts organizācijas līmenī.</span><span class="sxs-lookup"><span data-stu-id="05f25-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="05f25-144">Kopētie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="05f25-144">Copied tasks</span></span>

<span data-ttu-id="05f25-145">Kad uzdevums tiek kopēts no viena projekta uz citu, uzdevums pārmanto mērķa projekta plānošanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="05f25-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
