---
title: Piedāvājuma rindas apmaksājamo komponentu konfigurēšana
description: Šajā tēmā ir sniegta informācija par apmaksājamu un neapmaksājamu komponentu iestatīšanu projekta piedāvājuma rindā.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003775"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="dc62b-103">Piedāvājuma rindas maksas komponentu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="dc62b-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="dc62b-104">_**Attiecas uz:** Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu, Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem_</span><span class="sxs-lookup"><span data-stu-id="dc62b-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dc62b-105">Projekta piedāvājuma rindā ir *iekļauti* komponenti un *apmaksājami* komponenti.</span><span class="sxs-lookup"><span data-stu-id="dc62b-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="dc62b-106">Uz iekļautajiem komponentiem attiecas tālāk norādītais.</span><span class="sxs-lookup"><span data-stu-id="dc62b-106">Included components are subject to:</span></span>

  - <span data-ttu-id="dc62b-107">Norēķinu metode un klientu sadalījums</span><span class="sxs-lookup"><span data-stu-id="dc62b-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="dc62b-108">Nepārsniedzamie ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="dc62b-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="dc62b-109">Rēķina izrakstīšanas biežuma iestatījumi, kas definēti projekta piedāvājuma rindā</span><span class="sxs-lookup"><span data-stu-id="dc62b-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="dc62b-110">Iekļauto komponentu apakškopu var atzīmēt kā apmaksājamu, izmantojot lauku **Norēķinu tips**.</span><span class="sxs-lookup"><span data-stu-id="dc62b-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="dc62b-111">Lauks **Norēķinu tips** ir opciju kopa, kas piedāvājuma rindas kontekstā ļauj izmantot šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="dc62b-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="dc62b-112">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-112">Chargeable</span></span>
  - <span data-ttu-id="dc62b-113">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="dc62b-113">Non-chargeable</span></span>

<span data-ttu-id="dc62b-114">Apmaksājamus komponentus var definēt uzdevumos, lomās un darījumu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="dc62b-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="dc62b-115">Iekļaujamība rēķinā tiek definēta par piedāvājuma rindu un tā attiecas uz visām rindā iekļautajām darījumu klasēm.</span><span class="sxs-lookup"><span data-stu-id="dc62b-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="dc62b-116">Ja lauks **Iekļaut uzdevumus** ir tukšs vai iestatīts uz **Viss projekts**, cilne **Apmaksājamie uzdevumi** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="dc62b-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="dc62b-117">Iekļaujamību rēķinā definē lomām piedāvājuma rindai, un tā attiecas tikai uz darījumu klasi **Laiks**.</span><span class="sxs-lookup"><span data-stu-id="dc62b-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="dc62b-118">Ja lauks **Iekļaut laiku** projekta piedāvājuma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās lomas** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="dc62b-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="dc62b-119">Apmaksas apjoms tiek definēts pēc darījumu kategorijām piedāvājuma rindai, un tas attiecas tikai uz darījumu klasi **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="dc62b-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="dc62b-120">Ja lauks **Iekļaut izdevumus** projekta piedāvājuma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās kategorijas** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="dc62b-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="dc62b-121">Projekta uzdevuma atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="dc62b-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="dc62b-122">Projekta uzdevums var būt apmaksājams vai neapmaksājam noteiktā projekta piedāvājuma rindā, kas nodrošina šādas iestatīšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="dc62b-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="dc62b-123">Ja projekta piedāvājuma rindā ir iekļauts **Laiks** un uzdevums **T1**, uzdevums tiek saistīts ar piedāvājuma rindu kā apmaksājams.</span><span class="sxs-lookup"><span data-stu-id="dc62b-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="dc62b-124">Ja ir otra piedāvājuma rinda, kurā ir iekļautas lauks **Izmaksas**, varat saistīt **T1** uzdevumu piedāvājuma rindā kā neapmaksājamu.</span><span class="sxs-lookup"><span data-stu-id="dc62b-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="dc62b-125">Rezultāts ir tāds, ka viss šajā uzdevumā reģistrētais laiks ir apmaksājams, un visi izdevumi uzdevumā ir neapmaksājami.</span><span class="sxs-lookup"><span data-stu-id="dc62b-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="dc62b-126">Uzdevuma norēķinu tipu var konfigurēt projekta piedāvājuma rindas cilnē **Rēķinā iekļaujamie uzdevumi**, atjauninot lauku **Norēķinu tips** apakšrežģī **Piedāvājuma rindas uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="dc62b-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="dc62b-127">Vai arī varat atjaunināt projekta uzdevuma norēķinu veida lauku **Norēķinu tips** projekta norēķinu iestatījumu apakšrežģī, kas rāda ar uzdevumu saistītās piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="dc62b-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="dc62b-128">Lomas atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="dc62b-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="dc62b-129">Loma var būt apmaksājama vai neapmaksājama noteiktas projekta piedāvājuma rindas kontekstā.</span><span class="sxs-lookup"><span data-stu-id="dc62b-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="dc62b-130">Lomas norēķinu tipu var konfigurēt piedāvājuma rindas cilnē **Rēķinā iekļaujamās lomas**, atjauninot lauku **Norēķinu tips** apakšrežģī **Rēķinā iekļaujamās lomas**.</span><span class="sxs-lookup"><span data-stu-id="dc62b-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="dc62b-131">Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="dc62b-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="dc62b-132">Darījumu kategorija var būt apmaksājama vai neapmaksājama noteiktā piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="dc62b-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="dc62b-133">Transakcijas norēķinu tipu var konfigurēt piedāvājuma rindas cilnē **Rēķinā iekļaujamās kategorijas**, atjauninot lauku **Norēķinu tips** apakšrežģī **Rēķinā iekļaujamās kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="dc62b-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="dc62b-134">Apmaksājamības atrisināšana</span><span class="sxs-lookup"><span data-stu-id="dc62b-134">Resolve chargeability</span></span>
<span data-ttu-id="dc62b-135">Laika novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="dc62b-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="dc62b-136">**Laiks** ir iekļauts piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="dc62b-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="dc62b-137">**Loma** piedāvājuma rindā ir konfigurēta kā apmaksājama.</span><span class="sxs-lookup"><span data-stu-id="dc62b-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="dc62b-138">**Iekļautie uzdevumi** piedāvājuma rindā ir iestatīti uz **Atlasītie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="dc62b-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="dc62b-139">Ja šie trīs nosacījumi ir izpildīti, **Uzdevums** arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu.</span><span class="sxs-lookup"><span data-stu-id="dc62b-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="dc62b-140">Izdevumu novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="dc62b-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="dc62b-141">**Izdevumi** ir iekļauti piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="dc62b-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="dc62b-142">**Transakcijas kategorija** piedāvājuma rindā ir konfigurēta kā apmaksājama.</span><span class="sxs-lookup"><span data-stu-id="dc62b-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="dc62b-143">**Iekļautie uzdevumi** piedāvājuma rindā ir iestatīti uz **Atlasītie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="dc62b-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="dc62b-144">Ja šie trīs nosacījumi ir izpildīti, **Uzdevums** arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu.</span><span class="sxs-lookup"><span data-stu-id="dc62b-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="dc62b-145">Materiālu novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="dc62b-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="dc62b-146">**Materiāli** ir iekļauti piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="dc62b-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="dc62b-147">**Iekļautie uzdevumi** piedāvājuma rindā ir iestatīti uz **Atlasītie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="dc62b-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="dc62b-148">Ja šie divi nosacījumi ir izpildīti, **Uzdevums** tiek konfigurēts kā tāds, par kuru var iekasēt maksu.</span><span class="sxs-lookup"><span data-stu-id="dc62b-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="dc62b-149">
                    <strong>Iekļauts laiks</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="dc62b-150">
                    <strong>Iekļauti izdevumi</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="dc62b-151">
                    <strong>Iekļauti materiāli</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="dc62b-152">
                    <strong>Iekļautie uzdevumi</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="dc62b-153">
                    <strong>Loma</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="dc62b-154">
                    <strong>Kategorija</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="dc62b-155">
                    <strong>Uzdevums</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="dc62b-156">
                    <strong>Iekasēšanas ietekme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-157">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="dc62b-158">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="dc62b-159">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-160">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="dc62b-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-161">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-162">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-163">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-164">Norēķini par laika faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="dc62b-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="dc62b-165">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="dc62b-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="dc62b-166">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="dc62b-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-167">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="dc62b-168">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="dc62b-169">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-170">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="dc62b-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-171">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-172">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-173">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-174">Norēķini par laika faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="dc62b-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="dc62b-175">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="dc62b-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="dc62b-176">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="dc62b-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-177">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="dc62b-178">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="dc62b-179">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-180">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="dc62b-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="dc62b-181">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-182">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-183">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-184">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-185">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="dc62b-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="dc62b-186">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="dc62b-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-187">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="dc62b-188">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="dc62b-189">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-190">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="dc62b-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-191">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-192">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="dc62b-193">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-194">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-195">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-196">Rēķina tips materiālu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-197">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="dc62b-198">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="dc62b-199">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-200">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="dc62b-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="dc62b-201">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-202">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="dc62b-203">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-204">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-205">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-206">Rēķina tips materiālu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-207">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="dc62b-208">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="dc62b-209">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-210">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="dc62b-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="dc62b-211">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="dc62b-212">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-213">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-214">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-215">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-216">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="dc62b-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="dc62b-217">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="dc62b-218">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="dc62b-219">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-220">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="dc62b-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-221">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="dc62b-222">
                    <strong>Izrakstāms rēķins</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-223">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-224">Rēķins ar laika faktiskajām vērtībām: <strong>Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-225">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="dc62b-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="dc62b-226">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="dc62b-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="dc62b-227">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="dc62b-228">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="dc62b-229">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-230">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="dc62b-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-231">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="dc62b-232">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-233">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-234">Rēķins ar laika faktiskajām vērtībām: <strong>Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-235">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-236">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="dc62b-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-237">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="dc62b-238">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="dc62b-239">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-240">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="dc62b-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-241">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-242">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-243">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-244">Norēķini par laika faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="dc62b-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="dc62b-245">Rēķina tips izdevumu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-246">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="dc62b-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-247">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="dc62b-248">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="dc62b-249">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-250">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="dc62b-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="dc62b-251">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-252">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-253">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-254">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-255">Rēķina tips izdevumu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-256">Rēķina tips faktiskajām materiālu vērtībām: iekasējams</span><span class="sxs-lookup"><span data-stu-id="dc62b-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-257">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="dc62b-258">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="dc62b-259">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-260">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="dc62b-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-261">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-262">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="dc62b-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-263">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-264">Norēķini par laika faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="dc62b-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="dc62b-265">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="dc62b-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="dc62b-266">Rēķina tips materiālu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="dc62b-267">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="dc62b-268">Jā</span><span class="sxs-lookup"><span data-stu-id="dc62b-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="dc62b-269">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="dc62b-270">Viss projekts</span><span class="sxs-lookup"><span data-stu-id="dc62b-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="dc62b-271">
                    <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="dc62b-272">
                    <strong>Nav iekļaujams rēķinā</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="dc62b-273">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="dc62b-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="dc62b-274">Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-275">Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="dc62b-276">Rēķina tips materiālu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dc62b-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
