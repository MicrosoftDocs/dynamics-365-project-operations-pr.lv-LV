---
title: Maksas komponentu konfigurēšana projekta balstīta līguma rindā
description: Šajā tēmā ir sniegta informācija par to, kā projektu operācijās līguma rindām pievienot apmaksājamus komponentus.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003730"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="d4879-103">Maksas komponentu konfigurēšana projekta balstīta līguma rindā</span><span class="sxs-lookup"><span data-stu-id="d4879-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="d4879-104">_**Attiecas uz:** Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu, Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem_</span><span class="sxs-lookup"><span data-stu-id="d4879-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d4879-105">Projekta līguma rindā ir *iekļauti* komponenti un *apmaksājami* komponenti.</span><span class="sxs-lookup"><span data-stu-id="d4879-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="d4879-106">Iekļautie komponenti ir komponenti, uz kuriem attiecas tālāk minētais.</span><span class="sxs-lookup"><span data-stu-id="d4879-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="d4879-107">Norēķinu metode un klientu sadalījums</span><span class="sxs-lookup"><span data-stu-id="d4879-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="d4879-108">Nepārsniedzamie ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="d4879-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="d4879-109">Rēķina izrakstīšanas biežuma iestatījumi, kas definēti projekta līguma rindā</span><span class="sxs-lookup"><span data-stu-id="d4879-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="d4879-110">Iekļauto komponentu apakškopu var atzīmēt kā apmaksājamu, izmantojot lauku **Norēķinu tips**.</span><span class="sxs-lookup"><span data-stu-id="d4879-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="d4879-111">Lauks **Rēķina tips** ir opciju kopa, kas līguma rindas kontekstā ļauj izmantot šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="d4879-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="d4879-112">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-112">Chargeable</span></span>
  - <span data-ttu-id="d4879-113">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="d4879-113">Non-chargeable</span></span>

<span data-ttu-id="d4879-114">Apmaksājamus komponentus var definēt uzdevumos, lomās un darījumu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="d4879-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="d4879-115">Iekļaujamība rēķinā tiek definēta par projekta līguma rindas uzdevumiem un tā attiecas uz visām rindā iekļautajām darījumu klasēm.</span><span class="sxs-lookup"><span data-stu-id="d4879-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="d4879-116">Ja lauks **Iekļaut uzdevumus** līguma rindā ir tukšs vai iestatīts uz **Viss projekts**, cilne **Rēķinā iekļaujamie uzdevumi** nebūs pieejama.</span><span class="sxs-lookup"><span data-stu-id="d4879-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="d4879-117">Apmaksas apjoms, kas definēts pēc lomām projekta līguma rinai, attiecas tikai uz darījumu klasi **Laiks**.</span><span class="sxs-lookup"><span data-stu-id="d4879-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="d4879-118">Ja lauks **Iekļaut laiku** līguma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās lomas** nebūs pieejama.</span><span class="sxs-lookup"><span data-stu-id="d4879-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="d4879-119">Apmaksas apjoms, kas definēts pēc darījumu kategorijām projekta līguma rindai, attiecas tikai uz darījumu klasi **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="d4879-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="d4879-120">Ja lauks **Iekļaut izdevumus** līguma rindā ir iestatīts uz **Nē**, cilne **Apmaksājamās kategorijas** nebūs pieejama.</span><span class="sxs-lookup"><span data-stu-id="d4879-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="d4879-121">Projekta uzdevuma atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="d4879-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="d4879-122">Projekta uzdevums var būt apmaksājams vai neapmaksājamss noteiktā līguma rindā, kas nodrošina šādas iestatīšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="d4879-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="d4879-123">Ja projekta līguma rindā ir iekļauts lauks **Laiks** un noteikts uzdevums, **T1** ir saistīts ar to kā apmaksājams.</span><span class="sxs-lookup"><span data-stu-id="d4879-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="d4879-124">Ja ir otra līguma rinda, kurā ir iekļautas lauks **Izmaksas**, varat saistīt T1 uzdevumu līguma rindā kā neapmaksājamu.</span><span class="sxs-lookup"><span data-stu-id="d4879-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="d4879-125">Rezultāts ir tāds, ka viss šajā uzdevumā reģistrētais laiks ir apmaksājams, un visi izdevumi ir neapmaksājami.</span><span class="sxs-lookup"><span data-stu-id="d4879-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="d4879-126">Uzdevuma norēķinu tipu var konfigurēt līguma rindas cilnē **Rēķinā iekļaujamie uzdevumi**, atjauninot lauku **Norēķinu tips** līguma rindu uzdevumu apakšrežģī.</span><span class="sxs-lookup"><span data-stu-id="d4879-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="d4879-127">Vai arī varat atjaunināt lauku **Norēķinu tips** projekta norēķinu iestatījumu apakšrežģī, kas rāda ar uzdevumu saistītās līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="d4879-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="d4879-128">Lomas atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="d4879-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="d4879-129">Loma var būt apmaksājama vai neapmaksājama noteiktā līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="d4879-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="d4879-130">Lomu norēķina veidu var konfigurēt līguma rindas cilnē **Apmaksājamās lomas**.</span><span class="sxs-lookup"><span data-stu-id="d4879-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="d4879-131">Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās lomas**.</span><span class="sxs-lookup"><span data-stu-id="d4879-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="d4879-132">Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="d4879-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="d4879-133">Darījumu kategorija var būt apmaksājama vai neapmaksājama noteiktā līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="d4879-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="d4879-134">Darījuma norēķina veidu var konfigurēt projekta līguma rindas cilnē **Apmaksājamās kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="d4879-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="d4879-135">Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="d4879-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="d4879-136">Apmaksājamības atrisināšana</span><span class="sxs-lookup"><span data-stu-id="d4879-136">Resolve chargeability</span></span>

<span data-ttu-id="d4879-137">Laika novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="d4879-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="d4879-138">**Laiks** ir iekļauts līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="d4879-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="d4879-139">**Loma** līguma rindā ir konfigurēta kā apmaksājama.</span><span class="sxs-lookup"><span data-stu-id="d4879-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="d4879-140">**Iekļautie uzdevumi** līguma rindā ir iestatīti uz **Atlasītie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="d4879-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="d4879-141">Ja šie trīs nosacījumi ir izpildīti, uzdevums arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu.</span><span class="sxs-lookup"><span data-stu-id="d4879-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="d4879-142">Izdevumu novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="d4879-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="d4879-143">**Izdevumi** ir iekļauts līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="d4879-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="d4879-144">**Transakcijas kategorija** līguma rindā ir konfigurēta kā apmaksājama.</span><span class="sxs-lookup"><span data-stu-id="d4879-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="d4879-145">**Iekļautie uzdevumi** līguma rindā ir iestatīti uz **Atlasītais uzdevums**.</span><span class="sxs-lookup"><span data-stu-id="d4879-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="d4879-146">Ja šie trīs nosacījumi ir izpildīti,  **Uzdevums** arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu.</span><span class="sxs-lookup"><span data-stu-id="d4879-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="d4879-147">Materiālu novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="d4879-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="d4879-148">**Materiāli** ir iekļauts līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="d4879-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="d4879-149">**Iekļautie uzdevumi** līguma rindā ir iestatīti uz **Atlasītie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="d4879-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="d4879-150">Ja šie divi nosacījumi ir izpildīti, **Uzdevums** arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu.</span><span class="sxs-lookup"><span data-stu-id="d4879-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d4879-151">
                    <strong>Iekļauts laiks</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d4879-152">
                    <strong>Iekļauti izdevumi</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d4879-153">
                    <strong>Iekļauti materiāli</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="d4879-154">
                    <strong>Iekļautie uzdevumi</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4879-155">
                    <strong>Loma</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d4879-156">
                    <strong>Kategorija</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4879-157">
                    <strong>Uzdevums</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="d4879-158">
                    <strong>Iekasēšanas ietekme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-159">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d4879-160">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d4879-161">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-162">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="d4879-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-163">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-164">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-165">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-166">Rēķins par laika faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-167">Rēķins par izdevumu faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-168">Rēķins par materiālu faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-169">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d4879-170">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d4879-171">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-172">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="d4879-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-173">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-174">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-175">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-176">Rēķins par laika faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-177">Rēķins par izdevumu faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-178">Rēķins par materiālu faktisko vērtību: <strong>Iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-179">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d4879-180">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d4879-181">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-182">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="d4879-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4879-183">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-184">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-185">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-186">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-187">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="d4879-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d4879-188">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="d4879-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-189">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d4879-190">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d4879-191">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-192">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="d4879-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-193">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-194">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4879-195">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-196">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-197">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-198">Rēķina tips materiālu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-199">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d4879-200">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d4879-201">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-202">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="d4879-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4879-203">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-204">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4879-205">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-206">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-207">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-208">Rēķina tips materiālu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-209">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d4879-210">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d4879-211">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-212">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="d4879-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4879-213">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d4879-214">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-215">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-216">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-217">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-218">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="d4879-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d4879-219">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d4879-220">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d4879-221">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-222">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="d4879-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-223">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d4879-224">
                    <strong>Izrakstāms rēķins</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-225">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-226">Rēķins ar laika faktiskajām vērtībām: <strong>Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-227">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="d4879-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d4879-228">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="d4879-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d4879-229">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d4879-230">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d4879-231">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-232">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="d4879-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-233">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d4879-234">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-235">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-236">Rēķins ar laika faktiskajām vērtībām: <strong>Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-237">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-238">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="d4879-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-239">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d4879-240">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d4879-241">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-242">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="d4879-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-243">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-244">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-245">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-246">Norēķini par laika faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="d4879-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d4879-247">Rēķina tips izdevumu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-248">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="d4879-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-249">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d4879-250">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d4879-251">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-252">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="d4879-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4879-253">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-254">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-255">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-256">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-257">Rēķina tips izdevumu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-258">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="d4879-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-259">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d4879-260">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d4879-261">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-262">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="d4879-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-263">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-264">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="d4879-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-265">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-266">Norēķini par laika faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="d4879-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d4879-267">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="d4879-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d4879-268">Rēķina tips materiālu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d4879-269">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d4879-270">Jā</span><span class="sxs-lookup"><span data-stu-id="d4879-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d4879-271">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d4879-272">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="d4879-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d4879-273">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d4879-274">
                    <strong>Nav iekļaujams rēķinā</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d4879-275">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="d4879-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d4879-276">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-277">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d4879-278">Rēķina tips materiālu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d4879-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
