---
title: Projekta progress un izmaksu patēriņš
description: Šajā tēmā ir sniegta informācija par to, kā sekot līdzi projekta progresam un izmaksu patēriņam.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753544"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="cf6ed-103">Projekta progress un izmaksu patēriņš</span><span class="sxs-lookup"><span data-stu-id="cf6ed-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cf6ed-104">Nepieciešamība sekot līdzi grafika gaitai dažādās nozarēs atšķiras.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="cf6ed-105">Dažās nozarēs izsekošana notiek ļoti smalkā līmenī, turpretī citās nozarēs izsekošana tiek veikta augstākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="cf6ed-106">Šajā tēmā ir parādīts, kā veikt plānošanu, lai izpildītu jūsu organizācijas prasības.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="cf6ed-107">Piepūles izsekošanas skats</span><span class="sxs-lookup"><span data-stu-id="cf6ed-107">Effort tracking view</span></span>

<span data-ttu-id="cf6ed-108">Skats **Piepūles izsekošana** seko līdzi grafikā iekļauto uzdevumu progresam.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="cf6ed-109">Tajā faktiskais piepūles stundu skaits, kas ir patērēts kādam uzdevumam, tiek salīdzināts ar šim uzdevumam plānoto piepūles stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="cf6ed-110">Lai aprēķinātu izsekošanas metriku, programmatūrā PSA tiek izmantotas tālāk norādītās formulas.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="cf6ed-111">Progresa procentuālais daudzums = Līdz šim faktiski patērētā piepūle ÷ Uzdevumam plānotā piepūle</span><span class="sxs-lookup"><span data-stu-id="cf6ed-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="cf6ed-112">Novērtējums līdz pabeigšanai (ETC) = Plānotā piepūle - Līdz šim faktiski patērētā piepūle</span><span class="sxs-lookup"><span data-stu-id="cf6ed-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="cf6ed-113">Novērtējums pabeigšanas laikā (ETC) = Atlikusī piepūle + Līdz šim faktiski patērētā piepūle</span><span class="sxs-lookup"><span data-stu-id="cf6ed-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="cf6ed-114">Projektētā piepūles novirze = Plānotā piepūle - EAC</span><span class="sxs-lookup"><span data-stu-id="cf6ed-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="cf6ed-115">Programmatūrā PSA uzdevumam tiek rādīta projektētā piepūles novirze.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="cf6ed-116">Ja EAC ir lielāks par plānoto piepūli, tiek projektēts, ka uzdevums aizņems vairāk laika, nekā sākotnēji tika plānots.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="cf6ed-117">Tādēļ tas atpaliek no grafika.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="cf6ed-118">Ja EAC ir mazāks par plānoto piepūli, tiek projektēts, ka uzdevums aizņems mazāk laika, nekā sākotnēji tika plānots.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="cf6ed-119">Tādēļ tas apsteidz grafiku.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="cf6ed-120">Piepūles pārprojektēšana</span><span class="sxs-lookup"><span data-stu-id="cf6ed-120">Re-projecting effort</span></span>

<span data-ttu-id="cf6ed-121">Projektu vadītāji bieži vien pārskata sākotnējās uzdevumu aplēses.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="cf6ed-122">Projekta pārprojektēšana ir projektu vadītāja reaģēšana uz prognozēm, ņemot vērā projekta pašreizējo stāvokli.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="cf6ed-123">Taču mēs neiesakām projektu vadītājiem mainīt bāzlīnijas skaitļus, jo projekta bāzlīnija pārstāv noteikto patiesās informācijas avotu projekta grafikam un izmaksu tāmei, un visas projektā ieinteresētās puses par to ir vienojušās.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="cf6ed-124">Projektu vadītājs uzdevumiem var pārprojektēt piepūli divos tālāk norādītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="cf6ed-125">Pārlabot noklusējuma ETC ar jaunu uzdevumam faktiski atlikušās piepūles novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="cf6ed-126">Pārlabot noklusējuma progresa procentuālo daudzumu ar jaunu uzdevuma patiesā progresa novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="cf6ed-127">Katra no šīm metodēm izraisa uzdevuma ETC, EAC un progresa procentuālā daudzuma pārrēķināšanu, kā arī uzdevumam projektētās piepūles novirzes pārrēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="cf6ed-128">Tiek pārrēķināts arī EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un tiek izveidota jauna piepūles novirzes projektēšana.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="cf6ed-129">Piepūles pārprojektēšana kopsavilkuma uzdevumiem</span><span class="sxs-lookup"><span data-stu-id="cf6ed-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="cf6ed-130">Piepūli kopsavilkuma uzdevumiem vai konteinera uzdevumiem var pārprojektēt.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="cf6ed-131">Neatkarīgi no tā, vai lietotājs pārprojektēšanu veic, kopsavilkuma uzdevumiem izmantojot atlikušo piepūli vai progresa procentuālo daudzumu, sākas tālāk norādīto aprēķinu kopa.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="cf6ed-132">Uzdevumam tiek aprēķināts EAC, ETC un progresa procentuālais daudzums.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="cf6ed-133">Jaunais EAC tiek sadalīts uz pakārtotajiem uzdevumiem tādās pašās daļās, kā sākotnējais EAC tika sadalīts uz uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="cf6ed-134">Tiek aprēķināts jaunais EAC uz katru no atsevišķajiem uzdevumiem līdz pat lapas mezgla uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="cf6ed-135">Ietekmētajiem pakārtotajiem uzdevumiem lejup pa lapas mezgliem tiek pārrēķināts to ETC un progresa procentuālais daudzums, pamatojoties uz EAC vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="cf6ed-136">Šādi uzdevumam tiek iegūta jauna piepūles novirzes projektēšana.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="cf6ed-137">Tiek pārrēķināti kopsavilkuma uzdevumu EAC visiem uzdevumiem līdz saknes mezglam.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="cf6ed-138">Izmaksu izsekošanas skats</span><span class="sxs-lookup"><span data-stu-id="cf6ed-138">Cost tracking view</span></span> 

<span data-ttu-id="cf6ed-139">Skatā **Izmaksu izsekošana** faktiskās izmaksas, kuras tika iztērētas uz uzdevumu, tiek salīdzinātas ar plānotajām uzdevuma izmaksām.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="cf6ed-140">Šajā skatā tiek rādītas tikai darbaspēka izmaksas, un nav iekļautas izmaksas no izdevumu tāmēm.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="cf6ed-141">Lai aprēķinātu izsekošanas metriku, programmatūrā PSA tiek izmantotas tālāk norādītās formulas.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="cf6ed-142">Patērēto izmaksu procentuālais daudzums = Līdz šim faktiski iztērētās izmaksas ÷ Uzdevumam plānotās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cf6ed-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="cf6ed-143">Izmaksas līdz pabeigšanai (CTC) = Plānotās izmaksas - Līdz šim faktiski iztērētās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cf6ed-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="cf6ed-144">EAC = CTC + Līdz šim faktiski iztērētās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cf6ed-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="cf6ed-145">Projektētā izmaksu novirze = Plānotās izmaksas - EAC</span><span class="sxs-lookup"><span data-stu-id="cf6ed-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="cf6ed-146">Uzdevumam tiek rādīta projektētā izmaksu novirze.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="cf6ed-147">Ja EAC ir lielāks par plānotajām izmaksām, tiek projektēts, ka uzdevums izmaksās vairāk, nekā sākotnēji tika plānots.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="cf6ed-148">Tādēļ tam ir tendence pārsniegt budžetu.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="cf6ed-149">Ja EAC ir mazāks par plānotajām izmaksām, tiek projektēts, ka uzdevums izmaksās mazāk, nekā sākotnēji tika plānots.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="cf6ed-150">Tādēļ tam ir tendence iekļauties budžetā.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="cf6ed-151">Projektu vadītāja veiktā izmaksu pārprojektēšana</span><span class="sxs-lookup"><span data-stu-id="cf6ed-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="cf6ed-152">Kad notiek piepūles pārprojektēšana, skatā **Izmaksu izsekošana** tiek pārrēķināts CTC, EAC, patērēto izmaksu procentuālais daudzums un projektētā izmaksu nobīde.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="cf6ed-153">Projekta noteikta kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="cf6ed-153">Project status summary</span></span>

<span data-ttu-id="cf6ed-154">Izsekošanas dati skatā **Piepūles izsekošana** un **Izmaksu izsekošana** rāda progresu un izmaksu patēriņu projekta saknes mezgla, kopsavilkuma uzdevumu un lapas mezgla uzdevumu līmeņos.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="cf6ed-155">Lapas **Projekta entītija** sadaļā **Statuss** tiek rādīts projekta līmeņa statusa kopsavilkums.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="cf6ed-156">Statusa kopsavilkuma lauki</span><span class="sxs-lookup"><span data-stu-id="cf6ed-156">Status summary fields</span></span>

<span data-ttu-id="cf6ed-157">Lauks **Vispārējs projekta statuss** ir rediģējams lauks, kur tiek rādīts projekta vispārējais statuss.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="cf6ed-158">Tajā tiek izmantots krāsu kodējums, piemēram, zaļa, dzeltena un sarkana krāsa, lai norādītu uz pieaugošu risku.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="cf6ed-159">Laukā **Komentāri** projektu vadītājs var ievadīt konkrētus komentārus par statusu.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="cf6ed-160">Lauku **Statusa atjaunināšanas laiks** nevar rediģēt, un tā vērtība ir laikspiedols, kas norāda, kad statuss tika atjaunināts pēdējo reizi.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="cf6ed-161">Lauki **Grafika veiktspēja** un **Izmaksu veiktspēja** tiek iestatīti no izsekošanas datuma.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="cf6ed-162">Ja grafika un izmaksu novirze saknes mezglam skatā **Piepūles izsekošana** ir pozitīva, šos laukus varat iestatīt uz **Apsteidz**.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="cf6ed-163">Ja grafika un izmaksu novirze saknes mezglam ir negatīva, varat tos iestatīt uz **Atpaliek**.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
