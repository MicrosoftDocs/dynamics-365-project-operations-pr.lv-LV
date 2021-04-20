---
title: Maksas komponentu konfigurēšana projekta balstīta līguma rindā
description: Šajā tēmā ir sniegta informācija par to, kā projektu operācijās līguma rindām pievienot apmaksājamus komponentus.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858482"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="a5b0a-103">Maksas komponentu konfigurēšana projekta balstīta līguma rindā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="a5b0a-104">_**Attiecas uz:** Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu, Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem_</span><span class="sxs-lookup"><span data-stu-id="a5b0a-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a5b0a-105">Projekta līguma rindā ir *iekļauti* komponenti un *apmaksājami* komponenti.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="a5b0a-106">Iekļautie komponenti ir komponenti, uz kuriem attiecas tālāk minētais.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="a5b0a-107">Norēķinu metode un klientu sadalījums</span><span class="sxs-lookup"><span data-stu-id="a5b0a-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="a5b0a-108">Nepārsniedzamie ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="a5b0a-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="a5b0a-109">Rēķina izrakstīšanas biežuma iestatījumi, kas definēti projekta līguma rindā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="a5b0a-110">Iekļauto komponentu apakškopu var atzīmēt kā apmaksājamu, izmantojot lauku **Norēķinu tips**.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="a5b0a-111">Lauks **Rēķina tips** ir opciju kopa, kas līguma rindas kontekstā ļauj izmantot šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="a5b0a-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="a5b0a-112">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-112">Chargeable</span></span>
  - <span data-ttu-id="a5b0a-113">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-113">Non-chargeable</span></span>

<span data-ttu-id="a5b0a-114">Apmaksājamus komponentus var definēt uzdevumos, lomās un darījumu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="a5b0a-115">Iekļaujamība rēķinā tiek definēta par projekta līguma rindas uzdevumiem un tā attiecas uz visām rindā iekļautajām darījumu klasēm.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="a5b0a-116">Ja lauks **Iekļaut uzdevumus** līguma rindā ir tukšs vai iestatīts uz **Viss projekts**, cilne **Rēķinā iekļaujamie uzdevumi** nebūs pieejama.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="a5b0a-117">Apmaksas apjoms, kas definēts pēc lomām projekta līguma rinai, attiecas tikai uz darījumu klasi **Laiks**.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="a5b0a-118">Ja lauks **Iekļaut laiku** līguma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās lomas** nebūs pieejama.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="a5b0a-119">Apmaksas apjoms, kas definēts pēc darījumu kategorijām projekta līguma rindai, attiecas tikai uz darījumu klasi **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="a5b0a-120">Ja lauks **Iekļaut izdevumus** līguma rindā ir iestatīts uz **Nē**, cilne **Apmaksājamās kategorijas** nebūs pieejama.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="a5b0a-121">Projekta uzdevuma atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="a5b0a-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="a5b0a-122">Projekta uzdevums var būt apmaksājams vai neapmaksājamss noteiktā līguma rindā, kas nodrošina šādas iestatīšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="a5b0a-123">Ja projekta līguma rindā ir iekļauts lauks **Laiks** un noteikts uzdevums, **T1** ir saistīts ar to kā apmaksājams.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="a5b0a-124">Ja ir otra līguma rinda, kurā ir iekļautas lauks **Izmaksas**, varat saistīt T1 uzdevumu līguma rindā kā neapmaksājamu.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="a5b0a-125">Rezultāts ir tāds, ka viss šajā uzdevumā reģistrētais laiks ir apmaksājams, un visi izdevumi ir neapmaksājami.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="a5b0a-126">Uzdevuma norēķinu tipu var konfigurēt līguma rindas cilnē **Rēķinā iekļaujamie uzdevumi**, atjauninot lauku **Norēķinu tips** līguma rindu uzdevumu apakšrežģī.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="a5b0a-127">Vai arī varat atjaunināt lauku **Norēķinu tips** projekta norēķinu iestatījumu apakšrežģī, kas rāda ar uzdevumu saistītās līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="a5b0a-128">Lomas atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="a5b0a-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="a5b0a-129">Loma var būt apmaksājama vai neapmaksājama noteiktā līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="a5b0a-130">Lomu norēķina veidu var konfigurēt līguma rindas cilnē **Apmaksājamās lomas**.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="a5b0a-131">Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās lomas**.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="a5b0a-132">Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="a5b0a-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="a5b0a-133">Darījumu kategorija var būt apmaksājama vai neapmaksājama noteiktā līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="a5b0a-134">Darījuma norēķina veidu var konfigurēt projekta līguma rindas cilnē **Apmaksājamās kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="a5b0a-135">Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="a5b0a-136">Apmaksājamības atrisināšana</span><span class="sxs-lookup"><span data-stu-id="a5b0a-136">Resolve chargeability</span></span>

<span data-ttu-id="a5b0a-137">Laika novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="a5b0a-138">**Laiks** ir iekļauts līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="a5b0a-139">**Loma** līguma rindā ir konfigurēta kā apmaksājama.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="a5b0a-140">**Iekļautie uzdevumi** līguma rindā ir iestatīti uz **Atlasītie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="a5b0a-141">Ja šie trīs nosacījumi ir izpildīti, uzdevums arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="a5b0a-142">Izdevumu novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="a5b0a-143">**Izdevumi** ir iekļauts līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="a5b0a-144">**Transakcijas kategorija** līguma rindā ir konfigurēta kā apmaksājama.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="a5b0a-145">**Iekļautie uzdevumi** līguma rindā ir iestatīti uz **Atlasītais uzdevums**.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="a5b0a-146">Ja šie trīs nosacījumi ir izpildīti,  **Uzdevums** arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="a5b0a-147">Materiālu novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="a5b0a-148">**Materiāli** ir iekļauts līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="a5b0a-149">**Iekļautie uzdevumi** līguma rindā ir iestatīti uz **Atlasītie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="a5b0a-150">Ja šie divi nosacījumi ir izpildīti, **Uzdevums** arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu.</span><span class="sxs-lookup"><span data-stu-id="a5b0a-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="a5b0a-151">
                    <strong>Iekļauts laiks</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="a5b0a-152">
                    <strong>Iekļauti izdevumi</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="a5b0a-153">
                    <strong>Iekļauti materiāli</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="a5b0a-154">
                    <strong>Iekļautie uzdevumi</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a5b0a-155">
                    <strong>Loma</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="a5b0a-156">
                    <strong>Kategorija</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a5b0a-157">
                    <strong>Uzdevums</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="a5b0a-158">
                    <strong>Iekasēšanas ietekme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-159">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a5b0a-160">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a5b0a-161">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-162">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="a5b0a-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-163">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-164">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-165">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-166">Rēķins par laika faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-167">Rēķins par izdevumu faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-168">Rēķins par materiālu faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-169">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a5b0a-170">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a5b0a-171">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-172">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="a5b0a-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-173">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-174">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-175">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-176">Rēķins par laika faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-177">Rēķins par izdevumu faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-178">Rēķins par materiālu faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-179">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a5b0a-180">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a5b0a-181">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-182">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="a5b0a-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a5b0a-183">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-184">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-185">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-186">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-187">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a5b0a-188">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-189">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a5b0a-190">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a5b0a-191">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-192">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="a5b0a-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-193">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-194">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a5b0a-195">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-196">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-197">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-198">Rēķina tips materiālu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-199">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a5b0a-200">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a5b0a-201">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-202">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="a5b0a-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a5b0a-203">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-204">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a5b0a-205">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-206">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-207">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-208">Rēķina tips materiālu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-209">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a5b0a-210">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a5b0a-211">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-212">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="a5b0a-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a5b0a-213">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="a5b0a-214">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-215">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-216">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-217">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-218">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="a5b0a-219">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a5b0a-220">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a5b0a-221">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-222">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="a5b0a-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-223">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="a5b0a-224">
                    <strong>Izrakstāms rēķins</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-225">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-226">Rēķins ar laika faktiskajām vērtībām: <strong>Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-227">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a5b0a-228">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="a5b0a-229">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a5b0a-230">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a5b0a-231">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-232">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="a5b0a-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-233">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="a5b0a-234">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-235">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-236">Rēķins ar laika faktiskajām vērtībām: <strong>Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-237">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-238">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-239">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="a5b0a-240">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a5b0a-241">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-242">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="a5b0a-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-243">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-244">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-245">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-246">Norēķini par laika faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a5b0a-247">Rēķina tips izdevumu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-248">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-249">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="a5b0a-250">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="a5b0a-251">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-252">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="a5b0a-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a5b0a-253">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-254">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-255">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-256">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-257">Rēķina tips izdevumu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-258">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-259">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a5b0a-260">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="a5b0a-261">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-262">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="a5b0a-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-263">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-264">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="a5b0a-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-265">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-266">Norēķini par laika faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a5b0a-267">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="a5b0a-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="a5b0a-268">Rēķina tips materiālu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="a5b0a-269">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="a5b0a-270">Jā</span><span class="sxs-lookup"><span data-stu-id="a5b0a-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="a5b0a-271">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="a5b0a-272">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="a5b0a-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="a5b0a-273">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="a5b0a-274">
                    <strong>Nav iekļaujams rēķinā</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="a5b0a-275">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="a5b0a-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="a5b0a-276">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-277">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="a5b0a-278">Rēķina tips materiālu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a5b0a-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
