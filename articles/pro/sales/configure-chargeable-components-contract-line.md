---
title: Uz projektiem balstītu līguma rindu maksas komponentu konfigurēšana — Lite
description: Šajā tēmā ir sniegta informācija par to, kā projektu operācijās līguma rindām pievienot apmaksājamus komponentus.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513888"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a><span data-ttu-id="674fc-103">Uz projektiem balstītu līguma rindu maksas komponentu konfigurēšana — Lite</span><span class="sxs-lookup"><span data-stu-id="674fc-103">Configure chargeable components of a project-based contract line - lite</span></span>

<span data-ttu-id="674fc-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="674fc-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="674fc-105">Projekta līguma rindā ir *iekļauti* komponenti un *apmaksājami* komponenti.</span><span class="sxs-lookup"><span data-stu-id="674fc-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="674fc-106">Iekļautie komponenti ir komponenti, uz kuriem attiecas tālāk minētais.</span><span class="sxs-lookup"><span data-stu-id="674fc-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="674fc-107">Norēķinu metode un klientu sadalījums</span><span class="sxs-lookup"><span data-stu-id="674fc-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="674fc-108">Nepārsniedzamie ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="674fc-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="674fc-109">Rēķina izrakstīšanas biežuma iestatījumi, kas definēti projekta līguma rindā</span><span class="sxs-lookup"><span data-stu-id="674fc-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="674fc-110">Iekļauto komponentu apakškopu var atzīmēt kā apmaksājamu, izmantojot lauku **Norēķinu tips**.</span><span class="sxs-lookup"><span data-stu-id="674fc-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="674fc-111">Lauks **Rēķina tips** ir opciju kopa, kas līguma rindas kontekstā ļauj izmantot šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="674fc-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="674fc-112">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-112">Chargeable</span></span>
  - <span data-ttu-id="674fc-113">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="674fc-113">Non-chargeable</span></span>

<span data-ttu-id="674fc-114">Apmaksājamus komponentus var definēt uzdevumos, lomās un darījumu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="674fc-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="674fc-115">Iekļaujamība rēķinā tiek definēta par projekta līguma rindas uzdevumiem un tā attiecas uz visām rindā iekļautajām darījumu klasēm.</span><span class="sxs-lookup"><span data-stu-id="674fc-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="674fc-116">Ja lauks **Iekļaut uzdevumus** līguma rindā ir tukšs vai iestatīts uz **Viss projekts**, cilne **Rēķinā iekļaujamie uzdevumi** nebūs pieejama.</span><span class="sxs-lookup"><span data-stu-id="674fc-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="674fc-117">Apmaksas apjoms, kas definēts pēc lomām projekta līguma rinai, attiecas tikai uz darījumu klasi **Laiks**.</span><span class="sxs-lookup"><span data-stu-id="674fc-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="674fc-118">Ja lauks **Iekļaut laiku** līguma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās lomas** nebūs pieejama.</span><span class="sxs-lookup"><span data-stu-id="674fc-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="674fc-119">Apmaksas apjoms, kas definēts pēc darījumu kategorijām projekta līguma rindai, attiecas tikai uz darījumu klasi **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="674fc-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="674fc-120">Ja lauks **Iekļaut izdevumus** līguma rindā ir iestatīts uz **Nē**, cilne **Apmaksājamās kategorijas** nebūs pieejama.</span><span class="sxs-lookup"><span data-stu-id="674fc-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="674fc-121">Projekta uzdevuma atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="674fc-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="674fc-122">Projekta uzdevums var būt apmaksājams vai neapmaksājam noteiktā līguma rindā, kas nodrošina šādas iestatīšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="674fc-122">A project task can be chargeable or non-chargeable on a specific contract line which makes the following setup possible:</span></span>

<span data-ttu-id="674fc-123">Ja projekta līguma rindā ir iekļauts lauks **Laiks** un noteikts uzdevums, **T1** ir saistīts ar to kā apmaksājams.</span><span class="sxs-lookup"><span data-stu-id="674fc-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="674fc-124">Ja ir otra līguma rinda, kurā ir iekļautas lauks **Izmaksas**, varat saistīt T1 uzdevumu līguma rindā kā neapmaksājamu.</span><span class="sxs-lookup"><span data-stu-id="674fc-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="674fc-125">Rezultāts ir tāds, ka viss šajā uzdevumā reģistrētais laiks ir apmaksājams, un visi izdevumi ir neapmaksājami.</span><span class="sxs-lookup"><span data-stu-id="674fc-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="674fc-126">Uzdevuma norēķinu tipu var konfigurēt līguma rindas cilnē **Rēķinā iekļaujamie uzdevumi**, atjauninot lauku **Norēķinu tips** līguma rindu uzdevumu apakšrežģī.</span><span class="sxs-lookup"><span data-stu-id="674fc-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="674fc-127">Vai arī varat atjaunināt lauku **Norēķinu tips** projekta norēķinu iestatījumu apakšrežģī, kas rāda ar uzdevumu saistītās līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="674fc-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="674fc-128">Lomas atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="674fc-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="674fc-129">Loma var būt apmaksājama vai neapmaksājama noteiktā līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="674fc-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="674fc-130">Lomu norēķina veidu var konfigurēt līguma rindas cilnē **Apmaksājamās lomas**.</span><span class="sxs-lookup"><span data-stu-id="674fc-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="674fc-131">Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās lomas**.</span><span class="sxs-lookup"><span data-stu-id="674fc-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="674fc-132">Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="674fc-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="674fc-133">Darījumu kategorija var būt apmaksājama vai neapmaksājama noteiktā līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="674fc-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="674fc-134">Darījuma norēķina veidu var konfigurēt projekta līguma rindas cilnē **Apmaksājamās kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="674fc-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="674fc-135">Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="674fc-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="674fc-136">Apmaksājamības atrisināšana</span><span class="sxs-lookup"><span data-stu-id="674fc-136">Resolve chargeability</span></span>

<span data-ttu-id="674fc-137">Aprēķins vai faktiski dati, kas izveidoti par laiku, tiks uzskatīti par apmaksājamiem tikai tad, ja līguma rindā būs iekļauts lauks **Laiks** un lauki **Uzdevums** un **Loma** līguma rindā būs konfigurēta kā apmaksājama.</span><span class="sxs-lookup"><span data-stu-id="674fc-137">An estimate or actual created for time will only be considered chargeable if **Time** is included on the contract line, and if **Task** and **Role** are configured as chargeable on the contract line.</span></span>

<span data-ttu-id="674fc-138">Aprēķins vai faktiski dati, kas izveidoti par izdevumiem, tiks uzskatīti par apmaksājamiem tikai tad, ja līguma rindā būs iekļautas kategorijas **Izdevumi** un lauki **Uzdevums** un **Darījums** līguma rindā būs konfigurēta kā apmaksājama.</span><span class="sxs-lookup"><span data-stu-id="674fc-138">An estimate or actual created for expense is only considered chargeable if **Expense** is included on the contract line and if the **Task** and **Transaction** categories are configured as chargeable on the contract line.</span></span>


| <span data-ttu-id="674fc-139">Iekļauts laiks</span><span class="sxs-lookup"><span data-stu-id="674fc-139">Includes Time</span></span> | <span data-ttu-id="674fc-140">Iekļauti izdevumi</span><span class="sxs-lookup"><span data-stu-id="674fc-140">Includes Expense</span></span> | <span data-ttu-id="674fc-141">Iekļauti uzdevumi</span><span class="sxs-lookup"><span data-stu-id="674fc-141">Includes Tasks</span></span> | <span data-ttu-id="674fc-142">Loma</span><span class="sxs-lookup"><span data-stu-id="674fc-142">Role</span></span>           | <span data-ttu-id="674fc-143">Kategorija</span><span class="sxs-lookup"><span data-stu-id="674fc-143">Category</span></span>       | <span data-ttu-id="674fc-144">Uzdevums</span><span class="sxs-lookup"><span data-stu-id="674fc-144">Task</span></span>                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="674fc-145">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-145">Yes</span></span>           | <span data-ttu-id="674fc-146">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-146">Yes</span></span>              | <span data-ttu-id="674fc-147">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="674fc-147">Entire project</span></span> | <span data-ttu-id="674fc-148">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-148">Chargeable</span></span>     | <span data-ttu-id="674fc-149">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-149">Chargeable</span></span>     | <span data-ttu-id="674fc-150">Norēķini par laika faktiskajiem datiem: **Apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-150">Billing on a Time actual: **Chargeable**</span></span> </br> <span data-ttu-id="674fc-151">Norēķinu veids par izdevumu faktiskajiem datiem: **Apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-151">Billing type on Expense actual: **Chargeable**</span></span>           |
| <span data-ttu-id="674fc-152">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-152">Yes</span></span>           | <span data-ttu-id="674fc-153">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-153">Yes</span></span>              | <span data-ttu-id="674fc-154">Atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="674fc-154">Selected tasks</span></span> | <span data-ttu-id="674fc-155">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-155">Chargeable</span></span>     | <span data-ttu-id="674fc-156">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-156">Chargeable</span></span>     | <span data-ttu-id="674fc-157">Norēķini par laika faktiskajiem datiem: **Apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-157">Billing on a Time actual: **Chargeable**</span></span> </br> <span data-ttu-id="674fc-158">Norēķinu veids par izdevumu faktiskajiem datiem: **Apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-158">Billing type on Expense actual: **Chargeable**</span></span>           |
| <span data-ttu-id="674fc-159">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-159">Yes</span></span>           | <span data-ttu-id="674fc-160">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-160">Yes</span></span>              | <span data-ttu-id="674fc-161">Atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="674fc-161">Selected tasks</span></span> | <span data-ttu-id="674fc-162">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="674fc-162">Non-chargeable</span></span> | <span data-ttu-id="674fc-163">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-163">Chargeable</span></span>     | <span data-ttu-id="674fc-164">Norēķini par laika faktiskajiem datiem: **Nav apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-164">Billing on a Time actual: **Non-chargeable**</span></span> </br> <span data-ttu-id="674fc-165">Norēķinu veids par izdevumu faktiskajiem datiem: **Apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-165">Billing type on Expense actual: **Chargeable**</span></span>       |
| <span data-ttu-id="674fc-166">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-166">Yes</span></span>           | <span data-ttu-id="674fc-167">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-167">Yes</span></span>              | <span data-ttu-id="674fc-168">Atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="674fc-168">Selected tasks</span></span> | <span data-ttu-id="674fc-169">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-169">Chargeable</span></span>     | <span data-ttu-id="674fc-170">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-170">Chargeable</span></span>     | <span data-ttu-id="674fc-171">Norēķini par laika faktiskajiem datiem: **Nav apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-171">Billing on a Time actual: **Non-chargeable**</span></span> </br> <span data-ttu-id="674fc-172">Norēķinu veids par izdevumu faktiskajiem datiem: **Nav apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-172">Billing type on Expense actual:   **Non-chargeable**</span></span> |
| <span data-ttu-id="674fc-173">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-173">Yes</span></span>           | <span data-ttu-id="674fc-174">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-174">Yes</span></span>              | <span data-ttu-id="674fc-175">Atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="674fc-175">Selected tasks</span></span> | <span data-ttu-id="674fc-176">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="674fc-176">Non-chargeable</span></span> | <span data-ttu-id="674fc-177">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-177">Chargeable</span></span>     | <span data-ttu-id="674fc-178">Norēķini par laika faktiskajiem datiem: **Nav apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-178">Billing on a Time actual: **Non-chargeable**</span></span> </br> <span data-ttu-id="674fc-179">Norēķinu veids par izdevumu faktiskajiem datiem: **Nav apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-179">Billing type on Expense actual:   **Non-chargeable**</span></span> |
| <span data-ttu-id="674fc-180">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-180">Yes</span></span>           | <span data-ttu-id="674fc-181">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-181">Yes</span></span>              | <span data-ttu-id="674fc-182">Atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="674fc-182">Selected tasks</span></span> | <span data-ttu-id="674fc-183">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="674fc-183">Non-chargeable</span></span> | <span data-ttu-id="674fc-184">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="674fc-184">Non-chargeable</span></span> | <span data-ttu-id="674fc-185">Norēķini par laika faktiskajiem datiem: **Nav apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-185">Billing on a Time actual: **Non-chargeable**</span></span> </br> <span data-ttu-id="674fc-186">Norēķinu veids par izdevumu faktiskajiem datiem: **Nav apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-186">Billing type on Expense actual:   **Non-chargeable**</span></span> |
| <span data-ttu-id="674fc-187">No</span><span class="sxs-lookup"><span data-stu-id="674fc-187">No</span></span>            | <span data-ttu-id="674fc-188">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-188">Yes</span></span>              | <span data-ttu-id="674fc-189">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="674fc-189">Entire project</span></span> | <span data-ttu-id="674fc-190">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="674fc-190">Can't be set</span></span>   | <span data-ttu-id="674fc-191">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-191">Chargeable</span></span>     | <span data-ttu-id="674fc-192">Norēķini par laika faktiskajiem datiem: **Nav pieejams**</span><span class="sxs-lookup"><span data-stu-id="674fc-192">Billing on a Time actual: **Not available**</span></span></br><span data-ttu-id="674fc-193">Norēķinu veids par izdevumu faktiskajiem datiem: **Apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-193">Billing type on Expense actual: **Chargeable**</span></span>          |
| <span data-ttu-id="674fc-194">No</span><span class="sxs-lookup"><span data-stu-id="674fc-194">No</span></span>            | <span data-ttu-id="674fc-195">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-195">Yes</span></span>              | <span data-ttu-id="674fc-196">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="674fc-196">Entire project</span></span> | <span data-ttu-id="674fc-197">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="674fc-197">Can't be set</span></span>   | <span data-ttu-id="674fc-198">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="674fc-198">Non-chargeable</span></span> | <span data-ttu-id="674fc-199">Norēķini par laika faktiskajiem datiem: **Nav pieejams**</span><span class="sxs-lookup"><span data-stu-id="674fc-199">Billing on a Time actual: **Not available**</span></span></br> <span data-ttu-id="674fc-200">Norēķinu veids par izdevumu faktiskajiem datiem: **Nav apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-200">Billing type on Expense actual: **Non-chargeable**</span></span>     |
| <span data-ttu-id="674fc-201">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-201">Yes</span></span>           | <span data-ttu-id="674fc-202">No</span><span class="sxs-lookup"><span data-stu-id="674fc-202">No</span></span>               | <span data-ttu-id="674fc-203">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="674fc-203">Entire project</span></span> | <span data-ttu-id="674fc-204">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="674fc-204">Chargeable</span></span>     | <span data-ttu-id="674fc-205">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="674fc-205">Can't be set</span></span>   | <span data-ttu-id="674fc-206">Norēķini par laika faktiskajiem datiem: **Apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-206">Billing on a Time actual: **Chargeable**</span></span> </br> <span data-ttu-id="674fc-207">Norēķinu veids par izdevumu faktiskajiem datiem: **Nav pieejams**</span><span class="sxs-lookup"><span data-stu-id="674fc-207">Billing type on Expense actual: **Not available**</span></span>        |
| <span data-ttu-id="674fc-208">Jā</span><span class="sxs-lookup"><span data-stu-id="674fc-208">Yes</span></span>           | <span data-ttu-id="674fc-209">No</span><span class="sxs-lookup"><span data-stu-id="674fc-209">No</span></span>               | <span data-ttu-id="674fc-210">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="674fc-210">Entire project</span></span> | <span data-ttu-id="674fc-211">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="674fc-211">Non-chargeable</span></span> | <span data-ttu-id="674fc-212">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="674fc-212">Can't be set</span></span>   | <span data-ttu-id="674fc-213">Norēķini par laika faktiskajiem datiem: **Nav apmaksājams**</span><span class="sxs-lookup"><span data-stu-id="674fc-213">Billing on a Time actual: **Non-chargeable**</span></span> </br><span data-ttu-id="674fc-214">Norēķinu veids par izdevumu faktiskajiem datiem: **Nav pieejams**</span><span class="sxs-lookup"><span data-stu-id="674fc-214">Billing type on Expense actual: **Not   available**</span></span>   |