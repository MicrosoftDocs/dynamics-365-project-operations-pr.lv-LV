---
title: Faktiski
description: Šajā tēmā ir sniegta informācija par projekta faktiskajiem datiem.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753548"
---
# <a name="actuals"></a><span data-ttu-id="61c7b-103">Faktiski</span><span class="sxs-lookup"><span data-stu-id="61c7b-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="61c7b-104">Faktiskie dati ir darba apjoms, kas ir pabeigts projektā.</span><span class="sxs-lookup"><span data-stu-id="61c7b-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="61c7b-105">Projekta faktiskos datus var izsekot līdz to avota dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="61c7b-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="61c7b-106">Šie avota dokumenti ietver laika, izdevumu un žurnālu ierakstus, kā arī rēķinus.</span><span class="sxs-lookup"><span data-stu-id="61c7b-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kā projekta faktiskie dati tiek izsekoti līdz avota dokumentiem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="61c7b-108">Laika ieraksta iesniegšana</span><span class="sxs-lookup"><span data-stu-id="61c7b-108">Submitting a time entry</span></span>

<span data-ttu-id="61c7b-109">Kad programmā PSA tiek iesniegts laika ieraksts projektam, kas ir kartēts uz laika un materiālu līguma rindu, tiek izveidotas divas žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="61c7b-110">Viena rinda ir izmaksām, bet otra rinda ir paredzēta rēķinā neiekļautajai pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="61c7b-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="61c7b-111">Kad tiek iesniegts laika ieraksts projektam, kas ir kartēts uz fiksētas cenas līguma rindu, tiek izveidota žurnāla rinda tikai izmaksām.</span><span class="sxs-lookup"><span data-stu-id="61c7b-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="61c7b-112">Noklusējuma cenu ievadīšanas loģika atrodas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="61c7b-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="61c7b-113">Visas lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="61c7b-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="61c7b-114">Šajos laukos ir iekļauts transakcijas datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.</span><span class="sxs-lookup"><span data-stu-id="61c7b-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="61c7b-115">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Org. vienība**, izraisa atbilstošu cenu, kas pēc noklusējuma ir jāievada žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="61c7b-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="61c7b-116">Ja laika ierakstā pievienojat pielāgotu lauku un vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku entītijā Faktiskie dati un izmantojiet lauku kartējumus, lai kopētu lauku no laika ieraksta uz faktisko.</span><span class="sxs-lookup"><span data-stu-id="61c7b-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="61c7b-117">Izdevumu ieraksta iesniegšana</span><span class="sxs-lookup"><span data-stu-id="61c7b-117">Submitting an expense entry</span></span>

<span data-ttu-id="61c7b-118">Kad programmā PSA tiek iesniegts izdevumu ieraksts projektam, kas ir kartēts uz laika un materiālu līguma rindu, tiek izveidotas divas žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="61c7b-119">Viena rinda ir izmaksām, bet otra rinda ir paredzēta rēķinā neiekļautajai pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="61c7b-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="61c7b-120">Kad tiek iesniegts izdevumu ieraksts projektam, kas ir kartēts uz fiksētas cenas līguma rindu, tiek izveidota žurnāla rinda tikai izmaksām.</span><span class="sxs-lookup"><span data-stu-id="61c7b-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="61c7b-121">Loģika, kas paredzēta izdevumu noklusējuma cenu ievadīšanai, ir atkarīga no izdevumu kategorijas, kas atlasīta lapā **Izdevumu ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="61c7b-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="61c7b-122">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="61c7b-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="61c7b-123">Tomēr pašai cenai summa, ko lietotājs ir ievadījis, tiek pēc noklusējuma iestatīta tieši saistītajās izdevumu žurnāla rindās izmaksām un pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="61c7b-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="61c7b-124">Pašreizējā PSA versijā nav pieejams no kategorijas atkarīgs noklusējuma cenu par vienību ieraksts izdevumu ierakstos.</span><span class="sxs-lookup"><span data-stu-id="61c7b-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="61c7b-125">Žurnālu izmantošana izmaksu reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="61c7b-125">Using journals to record costs</span></span>

<span data-ttu-id="61c7b-126">Programmā PSA žurnāli ļauj ierakstīt izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs.</span><span class="sxs-lookup"><span data-stu-id="61c7b-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="61c7b-127">Žurnālā ir virsraksts, rindas un darbība **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="61c7b-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="61c7b-128">Piedāvājam dažus scenārijus, kuros jūs varētu izmantot žurnālu.</span><span class="sxs-lookup"><span data-stu-id="61c7b-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="61c7b-129">Jums projektā Ir jāieraksta materiālu faktiskās izmaksas un pārdošana.</span><span class="sxs-lookup"><span data-stu-id="61c7b-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="61c7b-130">Jums ir jāpārvieto transakciju faktiskie dati no citas sistēmas uz PSA.</span><span class="sxs-lookup"><span data-stu-id="61c7b-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="61c7b-131">Jums ir jāieraksta izmaksas, kas radās citā sistēmā, piemēram, sagādes vai apakšlīgumu slēgšanas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="61c7b-132">Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem</span><span class="sxs-lookup"><span data-stu-id="61c7b-132">Recording actuals based on project events</span></span>

<span data-ttu-id="61c7b-133">PSA ieraksta finanšu transakcijas, kas notiek projekta laikā.</span><span class="sxs-lookup"><span data-stu-id="61c7b-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="61c7b-134">Šīs transakcijas tiek ierakstītas kā **faktiskie dati**.</span><span class="sxs-lookup"><span data-stu-id="61c7b-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="61c7b-135">Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.</span><span class="sxs-lookup"><span data-stu-id="61c7b-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="61c7b-136">**Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība**</span><span class="sxs-lookup"><span data-stu-id="61c7b-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="61c7b-137">Notikums</span><span class="sxs-lookup"><span data-stu-id="61c7b-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="61c7b-138">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="61c7b-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="61c7b-139">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="61c7b-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="61c7b-140">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="61c7b-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="61c7b-141">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="61c7b-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="61c7b-142">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="61c7b-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="61c7b-143">Faktiski</span><span class="sxs-lookup"><span data-stu-id="61c7b-143">Actuals</span></span></th>
<th><span data-ttu-id="61c7b-144">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-144">Transaction currency</span></span></th>
<th><span data-ttu-id="61c7b-145">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="61c7b-145">Fixed price</span></span></th>
<th><span data-ttu-id="61c7b-146">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61c7b-147">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="61c7b-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="61c7b-148">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="61c7b-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-149">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="61c7b-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="61c7b-150">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="61c7b-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="61c7b-151">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="61c7b-152">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-152">Cost actual</span></span></td>
<td><span data-ttu-id="61c7b-153">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-154">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-155">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="61c7b-156">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-157">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-158">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="61c7b-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="61c7b-159">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="61c7b-160">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="61c7b-161">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-161">Cost actual</span></span></td>
<td><span data-ttu-id="61c7b-162">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-163">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-164">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-165">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-166">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-167">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="61c7b-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="61c7b-168">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-169">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="61c7b-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="61c7b-170">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="61c7b-171">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="61c7b-172">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="61c7b-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="61c7b-173">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-174">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="61c7b-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-175">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-176">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-177">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-178">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="61c7b-178">Billed sales</span></span></td>
<td><span data-ttu-id="61c7b-179">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="61c7b-180">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="61c7b-181">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="61c7b-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="61c7b-182">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-183">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-184">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-185">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-186">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-187">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="61c7b-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="61c7b-188">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-189">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="61c7b-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="61c7b-190">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="61c7b-191">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="61c7b-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="61c7b-192">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="61c7b-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="61c7b-193">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="61c7b-194">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="61c7b-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="61c7b-195">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="61c7b-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="61c7b-196">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="61c7b-197">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="61c7b-198">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-199">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="61c7b-199">Billed sales</span></span></td>
<td><span data-ttu-id="61c7b-200">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="61c7b-201">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="61c7b-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="61c7b-202">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="61c7b-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="61c7b-203">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-204">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="61c7b-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="61c7b-205">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-206">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="61c7b-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="61c7b-207">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61c7b-208">**Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības**</span><span class="sxs-lookup"><span data-stu-id="61c7b-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="61c7b-209">Notikums</span><span class="sxs-lookup"><span data-stu-id="61c7b-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="61c7b-210">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="61c7b-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="61c7b-211">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="61c7b-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="61c7b-212">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="61c7b-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="61c7b-213">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="61c7b-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="61c7b-214">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="61c7b-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="61c7b-215">Faktiski</span><span class="sxs-lookup"><span data-stu-id="61c7b-215">Actuals</span></span></th>
<th><span data-ttu-id="61c7b-216">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-216">Transaction currency</span></span></th>
<th><span data-ttu-id="61c7b-217">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="61c7b-217">Fixed price</span></span></th>
<th><span data-ttu-id="61c7b-218">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="61c7b-219">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="61c7b-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="61c7b-220">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="61c7b-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-221">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="61c7b-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="61c7b-222">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="61c7b-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="61c7b-223">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="61c7b-224">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-224">Cost actual</span></span></td>
<td><span data-ttu-id="61c7b-225">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="61c7b-226">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="61c7b-227">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="61c7b-228">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="61c7b-229">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-230">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="61c7b-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="61c7b-231">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-232">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="61c7b-233">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-234">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="61c7b-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="61c7b-235">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="61c7b-236">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="61c7b-237">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-237">Cost actual</span></span></td>
<td><span data-ttu-id="61c7b-238">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="61c7b-239">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="61c7b-240">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="61c7b-241">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="61c7b-242">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-243">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="61c7b-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="61c7b-244">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-245">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="61c7b-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="61c7b-246">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-247">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="61c7b-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="61c7b-248">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-249">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="61c7b-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="61c7b-250">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="61c7b-251">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="61c7b-252">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="61c7b-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="61c7b-253">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-254">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="61c7b-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-255">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-256">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="61c7b-257">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-258">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="61c7b-258">Billed sales</span></span></td>
<td><span data-ttu-id="61c7b-259">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="61c7b-260">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="61c7b-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="61c7b-261">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="61c7b-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="61c7b-262">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-263">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-264">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-265">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="61c7b-266">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-267">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="61c7b-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="61c7b-268">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-269">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="61c7b-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="61c7b-270">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="61c7b-271">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="61c7b-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="61c7b-272">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="61c7b-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="61c7b-273">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="61c7b-274">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="61c7b-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="61c7b-275">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="61c7b-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="61c7b-276">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="61c7b-277">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="61c7b-278">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="61c7b-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-279">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="61c7b-279">Billed sales</span></span></td>
<td><span data-ttu-id="61c7b-280">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="61c7b-281">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="61c7b-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="61c7b-282">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="61c7b-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="61c7b-283">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-284">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="61c7b-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="61c7b-285">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="61c7b-286">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="61c7b-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="61c7b-287">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="61c7b-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
