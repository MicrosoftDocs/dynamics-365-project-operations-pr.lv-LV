---
title: Pašreizējās
description: Šajā tēmā ir sniegta informācija par to, kā strādāt ar faktiskajiem datiem Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080434"
---
# <a name="actuals"></a><span data-ttu-id="83389-103">Pašreizējās</span><span class="sxs-lookup"><span data-stu-id="83389-103">Actuals</span></span> 

<span data-ttu-id="83389-104">_**Attiecas uz:** Project Operations scenārijiem, kas kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="83389-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="83389-105">Faktiskie dati ir darba apjoms, kas ir pabeigts projektā.</span><span class="sxs-lookup"><span data-stu-id="83389-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="83389-106">Tos izveido laika un izdevumu ierakstu, kā arī žurnāla ierakstu un rēķinu rezultātā.</span><span class="sxs-lookup"><span data-stu-id="83389-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="83389-107">Žurnāla rindu un laika iesniegšana</span><span class="sxs-lookup"><span data-stu-id="83389-107">Journal lines and time submission</span></span>

<span data-ttu-id="83389-108">Papildinformāciju par laika ievadīšanu skatiet šeit: [Laika ieraksta pārskats](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83389-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="83389-109">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="83389-109">Time and materials</span></span>

<span data-ttu-id="83389-110">Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="83389-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="83389-111">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="83389-111">Fixed price</span></span>

<span data-ttu-id="83389-112">Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz fiksētas cenas līguma rindu, sistēma izveido vienu žurnāla rindu – par izmaksām.</span><span class="sxs-lookup"><span data-stu-id="83389-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="83389-113">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="83389-113">Default pricing</span></span>

<span data-ttu-id="83389-114">Noklusējuma cenu izveides loģika atrodas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="83389-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="83389-115">Lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="83389-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="83389-116">Šajās vērtībās ir iekļauts darījuma datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.</span><span class="sxs-lookup"><span data-stu-id="83389-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="83389-117">Laukus, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Org. vienība** , izmanto atbilstošas cenas noteikšanai žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="83389-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="83389-118">Varat pievienot pielāgotu lauku laika ierakstam.</span><span class="sxs-lookup"><span data-stu-id="83389-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="83389-119">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku entītijā Faktiskie dati un izmantojiet lauku kartējumus, lai kopētu lauku no laika ieraksta uz faktisko.</span><span class="sxs-lookup"><span data-stu-id="83389-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="83389-120">Žurnāla rindu un pamata izdevumu iesniegšana</span><span class="sxs-lookup"><span data-stu-id="83389-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="83389-121">Papildinformāciju par izdevumu ievadīšanu skatiet šeit: [Izdevumu pārskats](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83389-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="83389-122">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="83389-122">Time and materials</span></span>

<span data-ttu-id="83389-123">Kad iesniegts pamata izdevumu ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="83389-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="83389-124">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="83389-124">Fixed price</span></span>

<span data-ttu-id="83389-125">Kad iesniegts pamata izdevumu ieraksts ir saistīts ar projektu, kas ir kartēts uz fiksētas cenas līguma rindu, sistēma izveido vienu žurnāla rindu – par izmaksām.</span><span class="sxs-lookup"><span data-stu-id="83389-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="83389-126">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="83389-126">Default pricing</span></span>

<span data-ttu-id="83389-127">Izdevumu noklusējuma cenu ievadīšanas loģikas pamatā ir izdevumu kategorija.</span><span class="sxs-lookup"><span data-stu-id="83389-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="83389-128">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="83389-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="83389-129">Tomēr pēc noklusējuma summa, kas ievadīta pašai cenai, tiek iestatīta tieši saistītajās izdevumu žurnāla rindās izmaksām un pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="83389-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="83389-130">Izdevumu ierakstiem kategorijā valstīta cenas par vienību ievade nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="83389-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="83389-131">Ierakstu žurnālu izmantošana izmaksu reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="83389-131">Use entry journals to record costs</span></span>

<span data-ttu-id="83389-132">Varat izmantot ierakstu žurnālus, lai ierakstītu izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs.</span><span class="sxs-lookup"><span data-stu-id="83389-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="83389-133">Žurnālus var izmantot šādiem mērķiem:</span><span class="sxs-lookup"><span data-stu-id="83389-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="83389-134">Reģistrēt materiālu un pārdošanas faktiskās izmaksas projektā.</span><span class="sxs-lookup"><span data-stu-id="83389-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="83389-135">Pārvietot darījuma faktiskos datus no citas sistēmas uz Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="83389-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="83389-136">Reģistrēt izmaksas, kas notikušas citā sistēmā.</span><span class="sxs-lookup"><span data-stu-id="83389-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="83389-137">Šīs izmaksas var ietvert iegādes vai apakšuzņēmēju izmaksas.</span><span class="sxs-lookup"><span data-stu-id="83389-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83389-138">Programma nevalidē žurnāla rindas tipu vai saistīto cenu, kas ievadīta žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="83389-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="83389-139">Tādējādi ierakstu žurnālus izmantot faktisko datu izveidei drīkst tikai lietotājs, kas pilnībā apzinās faktisko datu ietekmi uz projekta uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="83389-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="83389-140">Šī žurnāla veida ietekmes dēļ jums rūpīgi jāizvēlas personas, kurām ir piekļuve ierakstu žurnālu izveidei.</span><span class="sxs-lookup"><span data-stu-id="83389-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="83389-141">Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem</span><span class="sxs-lookup"><span data-stu-id="83389-141">Record actuals based on project events</span></span>

<span data-ttu-id="83389-142">Project Operations ieraksta finanšu transakcijas, kas notiek projekta laikā.</span><span class="sxs-lookup"><span data-stu-id="83389-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="83389-143">Šīs transakcijas tiek ierakstītas kā faktiskie dati.</span><span class="sxs-lookup"><span data-stu-id="83389-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="83389-144">Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.</span><span class="sxs-lookup"><span data-stu-id="83389-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="83389-145">Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="83389-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="83389-146">Notikums</span><span class="sxs-lookup"><span data-stu-id="83389-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="83389-147">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="83389-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="83389-148">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="83389-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="83389-149">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="83389-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="83389-150">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="83389-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="83389-151">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="83389-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="83389-152">Faktiski</span><span class="sxs-lookup"><span data-stu-id="83389-152">Actuals</span></span></th>
<th><span data-ttu-id="83389-153">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="83389-153">Transaction currency</span></span></th>
<th><span data-ttu-id="83389-154">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="83389-154">Fixed price</span></span></th>
<th><span data-ttu-id="83389-155">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="83389-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="83389-156">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="83389-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="83389-157">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="83389-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-158">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="83389-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="83389-159">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="83389-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="83389-160">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="83389-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="83389-161">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-161">Cost actual</span></span></td>
<td><span data-ttu-id="83389-162">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-163">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-164">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="83389-165">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-166">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-167">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="83389-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="83389-168">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="83389-169">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="83389-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="83389-170">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-170">Cost actual</span></span></td>
<td><span data-ttu-id="83389-171">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-172">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-173">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-174">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-175">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-176">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="83389-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="83389-177">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-178">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="83389-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="83389-179">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="83389-180">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="83389-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="83389-181">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="83389-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="83389-182">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-183">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="83389-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-184">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-185">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-186">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-187">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="83389-187">Billed sales</span></span></td>
<td><span data-ttu-id="83389-188">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="83389-189">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="83389-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="83389-190">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="83389-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="83389-191">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-192">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-193">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-194">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-195">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-196">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="83389-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="83389-197">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-198">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="83389-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="83389-199">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="83389-200">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="83389-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="83389-201">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="83389-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="83389-202">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="83389-203">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="83389-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="83389-204">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="83389-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="83389-205">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="83389-206">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="83389-207">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-208">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="83389-208">Billed sales</span></span></td>
<td><span data-ttu-id="83389-209">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="83389-210">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="83389-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="83389-211">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="83389-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="83389-212">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-213">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="83389-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="83389-214">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-215">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="83389-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="83389-216">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="83389-217">Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības</span><span class="sxs-lookup"><span data-stu-id="83389-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="83389-218">Notikums</span><span class="sxs-lookup"><span data-stu-id="83389-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="83389-219">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="83389-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="83389-220">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="83389-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="83389-221">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="83389-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="83389-222">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="83389-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="83389-223">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="83389-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="83389-224">Faktiski</span><span class="sxs-lookup"><span data-stu-id="83389-224">Actuals</span></span></th>
<th><span data-ttu-id="83389-225">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="83389-225">Transaction currency</span></span></th>
<th><span data-ttu-id="83389-226">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="83389-226">Fixed price</span></span></th>
<th><span data-ttu-id="83389-227">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="83389-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="83389-228">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="83389-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="83389-229">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="83389-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-230">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="83389-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="83389-231">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="83389-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="83389-232">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="83389-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="83389-233">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-233">Cost actual</span></span></td>
<td><span data-ttu-id="83389-234">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="83389-235">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="83389-236">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="83389-237">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="83389-238">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-239">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="83389-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="83389-240">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-241">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="83389-242">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-243">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="83389-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="83389-244">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="83389-245">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="83389-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="83389-246">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-246">Cost actual</span></span></td>
<td><span data-ttu-id="83389-247">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="83389-248">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="83389-249">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="83389-250">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="83389-251">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-252">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="83389-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="83389-253">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-254">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="83389-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="83389-255">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="83389-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-256">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="83389-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="83389-257">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-258">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="83389-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="83389-259">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="83389-260">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="83389-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="83389-261">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="83389-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="83389-262">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-263">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="83389-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-264">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-265">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="83389-266">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-267">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="83389-267">Billed sales</span></span></td>
<td><span data-ttu-id="83389-268">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="83389-269">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="83389-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="83389-270">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="83389-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="83389-271">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-272">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-273">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-274">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="83389-275">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-276">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="83389-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="83389-277">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-278">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="83389-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="83389-279">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="83389-280">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="83389-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="83389-281">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="83389-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="83389-282">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="83389-283">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="83389-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="83389-284">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="83389-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="83389-285">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="83389-286">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="83389-287">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="83389-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-288">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="83389-288">Billed sales</span></span></td>
<td><span data-ttu-id="83389-289">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="83389-290">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="83389-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="83389-291">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="83389-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="83389-292">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-293">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="83389-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="83389-294">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83389-295">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="83389-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="83389-296">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="83389-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
