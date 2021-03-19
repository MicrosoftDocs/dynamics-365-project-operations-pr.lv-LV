---
title: Pašreizējās
description: Šajā tēmā ir sniegta informācija par to, kā veikt darbības ar faktiskajiem darbiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291808"
---
# <a name="actuals"></a><span data-ttu-id="d18fe-103">Faktiskie dati</span><span class="sxs-lookup"><span data-stu-id="d18fe-103">Actuals</span></span> 

<span data-ttu-id="d18fe-104">_**Attiecas uz:** Project Operations scenārijiem, kas kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="d18fe-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d18fe-105">Faktiskie dati ir darba apjoms, kas ir pabeigts projektā.</span><span class="sxs-lookup"><span data-stu-id="d18fe-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="d18fe-106">Tos izveido laika un izdevumu ierakstu, kā arī žurnāla ierakstu un rēķinu rezultātā.</span><span class="sxs-lookup"><span data-stu-id="d18fe-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="d18fe-107">Žurnāla rindu un laika iesniegšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-107">Journal lines and time submission</span></span>

<span data-ttu-id="d18fe-108">Papildinformāciju par laika ievadīšanu skatiet šeit: [Laika ieraksta pārskats](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d18fe-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="d18fe-109">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="d18fe-109">Time and materials</span></span>

<span data-ttu-id="d18fe-110">Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="d18fe-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="d18fe-111">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="d18fe-111">Fixed price</span></span>

<span data-ttu-id="d18fe-112">Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz fiksētas cenas līguma rindu, sistēma izveido vienu žurnāla rindu – par izmaksām.</span><span class="sxs-lookup"><span data-stu-id="d18fe-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="d18fe-113">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-113">Default pricing</span></span>

<span data-ttu-id="d18fe-114">Noklusējuma cenu izveides loģika atrodas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="d18fe-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="d18fe-115">Lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="d18fe-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="d18fe-116">Šajās vērtībās ir iekļauts darījuma datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.</span><span class="sxs-lookup"><span data-stu-id="d18fe-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="d18fe-117">Laukus, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Org. vienība**, izmanto atbilstošas cenas noteikšanai žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="d18fe-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="d18fe-118">Varat pievienot pielāgotu lauku laika ierakstam.</span><span class="sxs-lookup"><span data-stu-id="d18fe-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="d18fe-119">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku entītijā Faktiskie dati un izmantojiet lauku kartējumus, lai kopētu lauku no laika ieraksta uz faktisko.</span><span class="sxs-lookup"><span data-stu-id="d18fe-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="d18fe-120">Žurnāla rindu un pamata izdevumu iesniegšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="d18fe-121">Papildinformāciju par izdevumu ievadīšanu skatiet šeit: [Izdevumu pārskats](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d18fe-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="d18fe-122">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="d18fe-122">Time and materials</span></span>

<span data-ttu-id="d18fe-123">Kad iesniegts pamata izdevumu ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="d18fe-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="d18fe-124">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="d18fe-124">Fixed price</span></span>

<span data-ttu-id="d18fe-125">Kad iesniegts pamata izdevumu ieraksts ir saistīts ar projektu, kas ir kartēts uz fiksētas cenas līguma rindu, sistēma izveido vienu žurnāla rindu – par izmaksām.</span><span class="sxs-lookup"><span data-stu-id="d18fe-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="d18fe-126">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-126">Default pricing</span></span>

<span data-ttu-id="d18fe-127">Izdevumu noklusējuma cenu ievadīšanas loģikas pamatā ir izdevumu kategorija.</span><span class="sxs-lookup"><span data-stu-id="d18fe-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="d18fe-128">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="d18fe-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="d18fe-129">Tomēr pēc noklusējuma summa, kas ievadīta pašai cenai, tiek iestatīta tieši saistītajās izdevumu žurnāla rindās izmaksām un pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="d18fe-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="d18fe-130">Izdevumu ierakstiem kategorijā valstīta cenas par vienību ievade nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="d18fe-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="d18fe-131">Ierakstu žurnālu izmantošana izmaksu reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="d18fe-131">Use entry journals to record costs</span></span>

<span data-ttu-id="d18fe-132">Varat izmantot ierakstu žurnālus, lai ierakstītu izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs.</span><span class="sxs-lookup"><span data-stu-id="d18fe-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="d18fe-133">Žurnālus var izmantot šādiem mērķiem:</span><span class="sxs-lookup"><span data-stu-id="d18fe-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="d18fe-134">Reģistrēt materiālu un pārdošanas faktiskās izmaksas projektā.</span><span class="sxs-lookup"><span data-stu-id="d18fe-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="d18fe-135">Pārvietojiet transakciju faktiskos datus no citas sistēmas uz Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d18fe-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="d18fe-136">Reģistrēt izmaksas, kas notikušas citā sistēmā.</span><span class="sxs-lookup"><span data-stu-id="d18fe-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="d18fe-137">Šīs izmaksas var ietvert iegādes vai apakšuzņēmēju izmaksas.</span><span class="sxs-lookup"><span data-stu-id="d18fe-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d18fe-138">Programma nevalidē žurnāla rindas tipu vai saistīto cenu, kas ievadīta žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="d18fe-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="d18fe-139">Tādējādi ierakstu žurnālus izmantot faktisko datu izveidei drīkst tikai lietotājs, kas pilnībā apzinās faktisko datu ietekmi uz projekta uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="d18fe-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="d18fe-140">Šī žurnāla veida ietekmes dēļ jums rūpīgi jāizvēlas personas, kurām ir piekļuve ierakstu žurnālu izveidei.</span><span class="sxs-lookup"><span data-stu-id="d18fe-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="d18fe-141">Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem</span><span class="sxs-lookup"><span data-stu-id="d18fe-141">Record actuals based on project events</span></span>

<span data-ttu-id="d18fe-142">Project Operations ieraksta finanšu transakcijas, kas notiek projekta laikā.</span><span class="sxs-lookup"><span data-stu-id="d18fe-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="d18fe-143">Šīs transakcijas tiek ierakstītas kā faktiskie dati.</span><span class="sxs-lookup"><span data-stu-id="d18fe-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="d18fe-144">Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.</span><span class="sxs-lookup"><span data-stu-id="d18fe-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="d18fe-145">Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="d18fe-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d18fe-146">Notikums</span><span class="sxs-lookup"><span data-stu-id="d18fe-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d18fe-147">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="d18fe-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d18fe-148">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="d18fe-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d18fe-149">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="d18fe-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d18fe-150">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="d18fe-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d18fe-151">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="d18fe-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d18fe-152">Faktiski</span><span class="sxs-lookup"><span data-stu-id="d18fe-152">Actuals</span></span></th>
<th><span data-ttu-id="d18fe-153">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-153">Transaction currency</span></span></th>
<th><span data-ttu-id="d18fe-154">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="d18fe-154">Fixed price</span></span></th>
<th><span data-ttu-id="d18fe-155">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d18fe-156">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="d18fe-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d18fe-157">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="d18fe-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-158">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="d18fe-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d18fe-159">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="d18fe-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d18fe-160">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="d18fe-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d18fe-161">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-161">Cost actual</span></span></td>
<td><span data-ttu-id="d18fe-162">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-163">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-164">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="d18fe-165">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-166">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-167">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="d18fe-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d18fe-168">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d18fe-169">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="d18fe-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d18fe-170">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-170">Cost actual</span></span></td>
<td><span data-ttu-id="d18fe-171">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-172">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-173">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-174">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-175">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-176">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="d18fe-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d18fe-177">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-178">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="d18fe-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d18fe-179">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d18fe-180">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="d18fe-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d18fe-181">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d18fe-182">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-183">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="d18fe-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-184">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-185">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-186">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-187">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="d18fe-187">Billed sales</span></span></td>
<td><span data-ttu-id="d18fe-188">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d18fe-189">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="d18fe-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d18fe-190">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d18fe-191">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-192">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-193">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-194">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-195">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-196">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="d18fe-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d18fe-197">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-198">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="d18fe-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d18fe-199">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d18fe-200">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d18fe-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d18fe-201">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d18fe-202">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d18fe-203">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="d18fe-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d18fe-204">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="d18fe-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d18fe-205">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d18fe-206">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d18fe-207">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-208">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="d18fe-208">Billed sales</span></span></td>
<td><span data-ttu-id="d18fe-209">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d18fe-210">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d18fe-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d18fe-211">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d18fe-212">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-213">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="d18fe-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d18fe-214">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-215">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="d18fe-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d18fe-216">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="d18fe-217">Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības</span><span class="sxs-lookup"><span data-stu-id="d18fe-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d18fe-218">Notikums</span><span class="sxs-lookup"><span data-stu-id="d18fe-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d18fe-219">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="d18fe-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d18fe-220">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="d18fe-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d18fe-221">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="d18fe-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d18fe-222">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="d18fe-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d18fe-223">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="d18fe-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d18fe-224">Faktiski</span><span class="sxs-lookup"><span data-stu-id="d18fe-224">Actuals</span></span></th>
<th><span data-ttu-id="d18fe-225">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-225">Transaction currency</span></span></th>
<th><span data-ttu-id="d18fe-226">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="d18fe-226">Fixed price</span></span></th>
<th><span data-ttu-id="d18fe-227">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d18fe-228">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="d18fe-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d18fe-229">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="d18fe-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-230">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="d18fe-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d18fe-231">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="d18fe-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d18fe-232">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="d18fe-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d18fe-233">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-233">Cost actual</span></span></td>
<td><span data-ttu-id="d18fe-234">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d18fe-235">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d18fe-236">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d18fe-237">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d18fe-238">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-239">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="d18fe-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d18fe-240">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-241">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d18fe-242">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-243">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="d18fe-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d18fe-244">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d18fe-245">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="d18fe-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d18fe-246">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-246">Cost actual</span></span></td>
<td><span data-ttu-id="d18fe-247">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d18fe-248">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d18fe-249">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d18fe-250">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d18fe-251">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-252">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="d18fe-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d18fe-253">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-254">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="d18fe-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d18fe-255">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-256">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="d18fe-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d18fe-257">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-258">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="d18fe-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d18fe-259">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d18fe-260">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="d18fe-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d18fe-261">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d18fe-262">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-263">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="d18fe-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-264">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-265">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d18fe-266">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-267">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="d18fe-267">Billed sales</span></span></td>
<td><span data-ttu-id="d18fe-268">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d18fe-269">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="d18fe-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d18fe-270">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d18fe-271">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-272">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-273">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-274">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d18fe-275">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-276">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="d18fe-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d18fe-277">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-278">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="d18fe-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d18fe-279">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d18fe-280">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d18fe-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d18fe-281">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d18fe-282">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d18fe-283">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="d18fe-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d18fe-284">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="d18fe-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d18fe-285">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d18fe-286">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d18fe-287">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="d18fe-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-288">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="d18fe-288">Billed sales</span></span></td>
<td><span data-ttu-id="d18fe-289">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d18fe-290">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d18fe-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d18fe-291">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="d18fe-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d18fe-292">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-293">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="d18fe-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d18fe-294">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d18fe-295">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="d18fe-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d18fe-296">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="d18fe-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]