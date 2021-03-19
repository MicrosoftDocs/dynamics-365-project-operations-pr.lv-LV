---
title: Automātiskas rēķina izveides konfigurēšana
description: Šajā tēmā sniegta informācija par to, kā konfigurēt sistēmu, lai automātiski izveidotu rēķinus.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0dddd963e79f8ecd91a96a6e684ab79e1b95bd6d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287922"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="9e3fd-103">Automātiskas rēķina izveides konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9e3fd-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="9e3fd-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="9e3fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="9e3fd-105">Izpildiet šīs darbības, lai konfigurētu automatizētu rēķinu izpildi risinājumā Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="9e3fd-106">Dodieties uz **Iestatījumi** > **Lielapjoma darbi**.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="9e3fd-107">Izveidojiet lielapjoma darbu un nosauciet to **Projekta darbību rēķinu izveide**.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="9e3fd-108">Lielapjoma darba nosaukumā jābūt iekļautiem vārdiem “rēķinu izveide”.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="9e3fd-109">Laukā **Darba tips** atlasiet vienumu **Nav**.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="9e3fd-110">**Pēc noklusējuma** Biežuma aizkave **Aktīvs** opcijas ir iestatītas uz **Jā.**</span><span class="sxs-lookup"><span data-stu-id="9e3fd-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="9e3fd-111">Atlasiet **Palaist darbplūsmu**.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-111">Select **Run Workflow**.</span></span> <span data-ttu-id="9e3fd-112">Dialoglodziņā **Meklēt ierakstu** redzēsiet trīs darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="9e3fd-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="9e3fd-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="9e3fd-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="9e3fd-114">ProcessRunner</span></span>
    - <span data-ttu-id="9e3fd-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="9e3fd-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="9e3fd-116">Atlasiet vienumu **ProcessRunCaller** un pēc tam **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="9e3fd-117">Nākamajā dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="9e3fd-118">Darbplūsma **Miegs** seko darbplūsmai **Apstrādāt**.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="9e3fd-119">5. darbībā varat arī atlasīt **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="9e3fd-120">Pēc tam, kad atlasā **Labi** **Apstrādāt** darbplūsmai seko **Miegs** darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="9e3fd-121">**ProcessRunCaller** un **ProcessRunner** darbplūsmas veido rēķinus.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="9e3fd-122">**ProcessRunCaller** izsauc **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="9e3fd-123">**ProcessRunner** ir darbplūsma, kas faktiski izveido rēķinus.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="9e3fd-124">Tā darbojas caur visām līguma rindām, kurām ir jāizveido rēķini, un izveido rēķinu šīm rindām.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="9e3fd-125">Lai noteiktu līguma rindas, kurām jāizveido rēķini, darbs tiek apskatīts līguma rindu rēķina izpildes datumos.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="9e3fd-126">Ja līguma rindām, kas attiecas uz vienu līgumu, ir vienāds rēķina izpildes datums, darījumi tiek apvienoti vienā rēķinā, kurā ir divas rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="9e3fd-127">Ja nav nevienas transakcijas rēķinu izveidei, darbs izlaiž rēķina veidošanu.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="9e3fd-128">Kad **ProcessRunner** ir beidzis darboties, tas izsauc **ProcessRunCaller**, nodrošina beigu laiku un ir slēgts.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="9e3fd-129">**ProcessRunCaller** pēc tam sāk skaitīt laiku, kas darbojas 24 stundas no norādītā beigu laika.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="9e3fd-130">Taimera laika skaitīšanas beigās **ProcessRunCaller** tiek slēgts.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="9e3fd-131">Lielapjoma izpildes darbs rēķinu izveidošanai ir kārtējais darbs.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="9e3fd-132">Ja šis pakešapstrādes process ir palaists vairākas reizes, tiek izveidoti vairāki darba gadījumi un var tikt izraisītas kļūdas.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="9e3fd-133">Tāpēc pakešapstrāde jāsāk tikai vienu reizi, un tā ir jārestartē tikai tad, ja tā pārstāj darboties.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="9e3fd-134">Lielapjomu rēķinu izveide darbojas vienīgi projekta līguma rindām, kuras ir konfigurējuši rēķinu grafiki.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="9e3fd-135">Līguma rindai ar fiksētu cenas aprēķina metodi jābūt konfigurētiem atskaites punktiem.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="9e3fd-136">Projekta līguma rindai ar laika un materiālu aprēķinu metodi ir jābūt iestatītam datuma bāzes rēķina grafikam.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="9e3fd-137">Tas pats attiecas uz līguma rindu, kuras pamatā ir projekts.</span><span class="sxs-lookup"><span data-stu-id="9e3fd-137">The same applies to a project-based contract line.</span></span>     


[!INCLUDE[footer-include](../includes/footer-banner.md)]