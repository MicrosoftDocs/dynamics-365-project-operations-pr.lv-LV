---
title: Rēķinā iekļaujamo uzdevumu konfigurēšana projekta piedāvājuma rindā
description: Šajā tēmā ir sniegta informācija par iekļautajiem, rēķinā iekļaujamajiem un rēķinā neiekļaujamajiem komponentiem projekta piedāvājuma rindās.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642552"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a><span data-ttu-id="5f2fe-103">Rēķinā iekļaujamo uzdevumu konfigurēšana projekta piedāvājuma rindā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-103">Configure the chargeable components of a project-based quote line</span></span>

<span data-ttu-id="5f2fe-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="5f2fe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5f2fe-105">Projekta piedāvājuma rindā var būt iekļautie komponenti un rēķinā iekļaujamie komponenti.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-105">A project-based quote line can have included components and chargeable components.</span></span>

<span data-ttu-id="5f2fe-106">Uz iekļautajiem komponentiem attiecas norēķinu metodes, klientu sadalījumu, nepārsniedzamo ierobežojumu un rēķinu izrakstīšanas biežuma iestatījumi, kas definēti projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-106">Included components are subject to the billing method, customer splits, not-to-exceed limits, and invoice frequency settings defined on the project-based quote line.</span></span>
<span data-ttu-id="5f2fe-107">Iekļauto komponentu apakškopu var atzīmēt kā rēķinā iekļaujamu, izmantojot vienumu **Norēķinu tips**.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-107">A subset of the included components can be marked as chargeable by using **Billing Type**.</span></span> <span data-ttu-id="5f2fe-108">Piedāvājuma rindas kontekstā var atlasīt vienu no tālāk norādītajām lauka **Norēķinu tips** opcijām.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-108">You can select one of the following options in the **Billing Type** field in the context of a quote line:</span></span>

   - <span data-ttu-id="5f2fe-109">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="5f2fe-109">Chargeable</span></span>
   - <span data-ttu-id="5f2fe-110">Nav iekļaujams rēķinā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-110">Non-chargeable</span></span>

<span data-ttu-id="5f2fe-111">Rēķinā iekļaujamos komponentus var definēt lomās un darbību kategorijās.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-111">Chargeable components can be defined on roles and transaction categories.</span></span>

<span data-ttu-id="5f2fe-112">Iekļaujamība, kas ir definēta projekta piedāvājuma rindas lomās, attiecas tikai uz darbību klasi **Laiks**.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-112">Chargeability that is defined on roles for a project quote line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="5f2fe-113">Ja projekta piedāvājuma rindā ir iestatījums **Iekļaut laiku** = **Nē**, cilne **Rēķinā iekļaujamās lomas** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-113">If a project quote line has **Include Time** = **No**, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="5f2fe-114">Iekļaujamība, kas ir definēta projekta piedāvājuma rindas darbību kategorijās, attiecas tikai uz darbību klasi **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-114">Chargeability that is defined on transaction categories for a project quote line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="5f2fe-115">Ja projekta piedāvājuma rindā ir iestatījums **Iekļaut izdevumus** = **Nē**, cilne **Rēķinā iekļaujamās kategorijas** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-115">If a project quote line has **Include Expenses** = **No**, the **Chargeable Categories** tab isn't available.</span></span>

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="5f2fe-116">Lomas atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="5f2fe-116">Update a role to be chargeable or non-chargeable</span></span>
<span data-ttu-id="5f2fe-117">Loma projekta piedāvājuma rindā var būt rēķinā iekļaujama vai rēķinā neiekļaujama.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-117">A role can be chargeable or non-chargeable on a project-based quote line.</span></span> <span data-ttu-id="5f2fe-118">Lomas norēķinu tipu var konfigurēt projekta piedāvājuma rindas cilnē **Rēķinā iekļaujamās lomas**.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-118">The billing type on a role can be configured on the **Chargeable Roles** tab of a project-based quote line.</span></span> <span data-ttu-id="5f2fe-119">Lai to paveiktu, atjauniniet lauku **Norēķinu tips** apakšrežģī **Rēķinā iekļaujamās lomas**.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-119">To do this, update **Billing Type** on the **Chargeable Roles** subgrid.</span></span> 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="5f2fe-120">Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu</span><span class="sxs-lookup"><span data-stu-id="5f2fe-120">Update a transaction category to be chargeable or non-chargeable</span></span>
<span data-ttu-id="5f2fe-121">Darbību kategorija projekta piedāvājuma rindā var būt rēķinā iekļaujama vai rēķinā neiekļaujama.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-121">A transaction category can be chargeable or non-chargeable on a project-based quote line.</span></span> <span data-ttu-id="5f2fe-122">Darbības norēķinu tipu var konfigurēt projekta piedāvājuma rindas cilnē **Rēķinā iekļaujamās kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-122">The billing type on a transaction can be configured on the **Chargeable Categories** tab of a project-based quote line.</span></span> <span data-ttu-id="5f2fe-123">Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-123">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span> 

## <a name="resolve-chargeability"></a><span data-ttu-id="5f2fe-124">Apmaksājamības atrisināšana</span><span class="sxs-lookup"><span data-stu-id="5f2fe-124">Resolve chargeability</span></span>

<span data-ttu-id="5f2fe-125">Izveidotais laika aprēķins vai faktiskais laiks tiks uzskatīts kā rēķinā iekļaujams tikai tad, ja laiks būs iekļauts piedāvājuma rindā un loma būs konfigurēta kā rēķinā iekļaujama.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-125">An estimate or actual created for time will only be considered chargeable if the time is included on the quote line and if the role is configured as chargeable.</span></span>
<span data-ttu-id="5f2fe-126">Izveidotais izdevumu aprēķins vai faktiskie izdevumi tiks uzskatīti kā rēķinā iekļaujami tikai tad, ja izdevumi būs iekļauti piedāvājuma rindā un darbību kategorija piedāvājuma rindā būs konfigurēta kā rēķinā iekļaujama.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-126">An estimate or actual created for an expense will only be considered chargeable if the expense is included on the quote line and if the transaction category is configured as chargeable on the quote line.</span></span> <span data-ttu-id="5f2fe-127">Tālāk esošajā tabulā ir parādīti iekļaujamības nokklusējumi katram faktiskajam ierakstam.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-127">The following table shows how chargeability defaults on each actual.</span></span> <span data-ttu-id="5f2fe-128">Noklusējumu pamatā ir iekļautie komponenti un piedāvājuma rindā iestatītais norēķinu tips.</span><span class="sxs-lookup"><span data-stu-id="5f2fe-128">The defaults are based on the included components and the billing type that is set up on the quote line.</span></span>

| <span data-ttu-id="5f2fe-129">Iekļauts laiks</span><span class="sxs-lookup"><span data-stu-id="5f2fe-129">Includes time</span></span> | <span data-ttu-id="5f2fe-130">Iekļauti izdevumi</span><span class="sxs-lookup"><span data-stu-id="5f2fe-130">Includes expense</span></span> | <span data-ttu-id="5f2fe-131">Loma</span><span class="sxs-lookup"><span data-stu-id="5f2fe-131">Role</span></span> | <span data-ttu-id="5f2fe-132">Kategorija</span><span class="sxs-lookup"><span data-stu-id="5f2fe-132">Category</span></span> | <span data-ttu-id="5f2fe-133">Uzdevums</span><span class="sxs-lookup"><span data-stu-id="5f2fe-133">Task</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="5f2fe-134">Jā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-134">Yes</span></span> | <span data-ttu-id="5f2fe-135">Jā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-135">Yes</span></span> | <span data-ttu-id="5f2fe-136">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="5f2fe-136">Chargeable</span></span> | <span data-ttu-id="5f2fe-137">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="5f2fe-137">Chargeable</span></span> | <span data-ttu-id="5f2fe-138">Norēķini par laika faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-138">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="5f2fe-139">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-139">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="5f2fe-140">Jā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-140">Yes</span></span> | <span data-ttu-id="5f2fe-141">Jā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-141">Yes</span></span> | <span data-ttu-id="5f2fe-142">Nav apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-142">Non - Chargeable</span></span> | <span data-ttu-id="5f2fe-143">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="5f2fe-143">Chargeable</span></span> | <span data-ttu-id="5f2fe-144">Norēķini par laika faktiskajiem datiem: Nav apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-144">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="5f2fe-145">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-145">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="5f2fe-146">Jā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-146">Yes</span></span> | <span data-ttu-id="5f2fe-147">Jā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-147">Yes</span></span> | <span data-ttu-id="5f2fe-148">Nav apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-148">Non-Chargeable</span></span> | <span data-ttu-id="5f2fe-149">Nav apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-149">Non-Chargeable</span></span> | <span data-ttu-id="5f2fe-150">Norēķini par laika faktiskajiem datiem: Nav apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-150">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="5f2fe-151">Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-151">Billing type on an expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="5f2fe-152">No</span><span class="sxs-lookup"><span data-stu-id="5f2fe-152">No</span></span> | <span data-ttu-id="5f2fe-153">Jā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-153">Yes</span></span> | <span data-ttu-id="5f2fe-154">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="5f2fe-154">Can't be set</span></span> | <span data-ttu-id="5f2fe-155">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="5f2fe-155">Chargeable</span></span> | <span data-ttu-id="5f2fe-156">Norēķini par laika faktiskajiem datiem: Nav pieejams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-156">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="5f2fe-157">Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-157">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="5f2fe-158">No</span><span class="sxs-lookup"><span data-stu-id="5f2fe-158">No</span></span> | <span data-ttu-id="5f2fe-159">Jā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-159">Yes</span></span> | <span data-ttu-id="5f2fe-160">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="5f2fe-160">Can't be set</span></span> | <span data-ttu-id="5f2fe-161">Nav apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-161">Non-Chargeable</span></span> | <span data-ttu-id="5f2fe-162">Norēķini par laika faktiskajiem datiem: Nav pieejams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-162">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="5f2fe-163">Norēķinu veids par izdevumu faktiskajiem datiem: Nav apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-163">Billing type on an expense actual: Non-chargeable</span></span> |
| <span data-ttu-id="5f2fe-164">Jā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-164">Yes</span></span> | <span data-ttu-id="5f2fe-165">No</span><span class="sxs-lookup"><span data-stu-id="5f2fe-165">No</span></span> | <span data-ttu-id="5f2fe-166">Izrakstāms rēķins</span><span class="sxs-lookup"><span data-stu-id="5f2fe-166">Chargeable</span></span> | <span data-ttu-id="5f2fe-167">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="5f2fe-167">Can't be set</span></span> | <span data-ttu-id="5f2fe-168">Norēķini par laika faktiskajiem datiem: Apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-168">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="5f2fe-169">Norēķinu veids par izdevumu faktiskajiem datiem: Nav pieejams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-169">Billing type on an expense actual: Not available</span></span> |
| <span data-ttu-id="5f2fe-170">Jā</span><span class="sxs-lookup"><span data-stu-id="5f2fe-170">Yes</span></span> | <span data-ttu-id="5f2fe-171">No</span><span class="sxs-lookup"><span data-stu-id="5f2fe-171">No</span></span> | <span data-ttu-id="5f2fe-172">Nav apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-172">Non-Chargeable</span></span> | <span data-ttu-id="5f2fe-173">Nevar iestatīt</span><span class="sxs-lookup"><span data-stu-id="5f2fe-173">Can't be set</span></span> | <span data-ttu-id="5f2fe-174">Norēķini par laika faktiskajiem datiem: Nav apmaksājams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-174">Billing on a time actual: Non-chargeable</span></span> </br> <span data-ttu-id="5f2fe-175">Norēķinu veids par izdevumu faktiskajiem datiem: Nav pieejams</span><span class="sxs-lookup"><span data-stu-id="5f2fe-175">Billing type on an expense actual: Not available</span></span> |