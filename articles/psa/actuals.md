---
title: Pārskats faktiski
description: Šajā tēmā ir sniegta informācija par projekta faktiskajiem datiem.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014665"
---
# <a name="actuals-overview"></a><span data-ttu-id="21999-103">Pārskats faktiski</span><span class="sxs-lookup"><span data-stu-id="21999-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="21999-104">Faktiskie dati ir darba apjoms, kas ir pabeigts projektā.</span><span class="sxs-lookup"><span data-stu-id="21999-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="21999-105">Projekta faktiskos datus var izsekot līdz to avota dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="21999-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="21999-106">Šie avota dokumenti ietver laika, izdevumu un žurnālu ierakstus, kā arī rēķinus.</span><span class="sxs-lookup"><span data-stu-id="21999-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kā projekta faktiskie dati tiek izsekoti līdz avota dokumentiem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="21999-108">Laika ieraksta iesniegšana</span><span class="sxs-lookup"><span data-stu-id="21999-108">Submitting a time entry</span></span>

<span data-ttu-id="21999-109">Kad programmā PSA tiek iesniegts laika ieraksts projektam, kas ir kartēts uz laika un materiālu līguma rindu, tiek izveidotas divas žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="21999-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="21999-110">Viena rinda ir izmaksām, bet otra rinda ir paredzēta rēķinā neiekļautajai pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="21999-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="21999-111">Kad tiek iesniegts laika ieraksts projektam, kas ir kartēts uz fiksētas cenas līguma rindu, tiek izveidota žurnāla rinda tikai izmaksām.</span><span class="sxs-lookup"><span data-stu-id="21999-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="21999-112">Noklusējuma cenu ievadīšanas loģika atrodas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="21999-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="21999-113">Visas lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="21999-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="21999-114">Šajos laukos ir iekļauts transakcijas datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.</span><span class="sxs-lookup"><span data-stu-id="21999-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="21999-115">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Org. vienība**, izraisa atbilstošu cenu, kas pēc noklusējuma ir jāievada žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="21999-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="21999-116">Ja laika ierakstā pievienojat pielāgotu lauku un vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku entītijā Faktiskie dati un izmantojiet lauku kartējumus, lai kopētu lauku no laika ieraksta uz faktisko.</span><span class="sxs-lookup"><span data-stu-id="21999-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="21999-117">Izdevumu ieraksta iesniegšana</span><span class="sxs-lookup"><span data-stu-id="21999-117">Submitting an expense entry</span></span>

<span data-ttu-id="21999-118">Kad programmā PSA tiek iesniegts izdevumu ieraksts projektam, kas ir kartēts uz laika un materiālu līguma rindu, tiek izveidotas divas žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="21999-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="21999-119">Viena rinda ir izmaksām, bet otra rinda ir paredzēta rēķinā neiekļautajai pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="21999-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="21999-120">Kad tiek iesniegts izdevumu ieraksts projektam, kas ir kartēts uz fiksētas cenas līguma rindu, tiek izveidota žurnāla rinda tikai izmaksām.</span><span class="sxs-lookup"><span data-stu-id="21999-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="21999-121">Loģika, kas paredzēta izdevumu noklusējuma cenu ievadīšanai, ir atkarīga no izdevumu kategorijas, kas atlasīta lapā **Izdevumu ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="21999-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="21999-122">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="21999-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="21999-123">Tomēr pašai cenai summa, ko lietotājs ir ievadījis, tiek pēc noklusējuma iestatīta tieši saistītajās izdevumu žurnāla rindās izmaksām un pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="21999-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="21999-124">Pašreizējā PSA versijā nav pieejams no kategorijas atkarīgs noklusējuma cenu par vienību ieraksts izdevumu ierakstos.</span><span class="sxs-lookup"><span data-stu-id="21999-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="21999-125">Ierakstu žurnālu izmantošana izmaksu reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="21999-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="21999-126">Programmā PSA ierakstu žurnāli ļauj ierakstīt izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs.</span><span class="sxs-lookup"><span data-stu-id="21999-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="21999-127">Žurnālā ir virsraksts, rindas un darbība **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="21999-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="21999-128">Piedāvājam dažus scenārijus, kuros jūs varētu izmantot žurnālu.</span><span class="sxs-lookup"><span data-stu-id="21999-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="21999-129">Jums projektā Ir jāieraksta materiālu faktiskās izmaksas un pārdošana.</span><span class="sxs-lookup"><span data-stu-id="21999-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="21999-130">Jums ir jāpārvieto transakciju faktiskie dati no citas sistēmas uz PSA.</span><span class="sxs-lookup"><span data-stu-id="21999-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="21999-131">Jums ir jāieraksta izmaksas, kas radās citā sistēmā, piemēram, sagādes vai apakšlīgumu slēgšanas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="21999-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21999-132">Ierakstu žurnālu izmantošana, lai izveidotu faktiskos rezultātus, ir jāveic tikai lietotājam, kas pilnībā pārzina grāmatvedības ietekmi, kāda ir attiecībā uz faktiskajiem projektiem.</span><span class="sxs-lookup"><span data-stu-id="21999-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="21999-133">Tas ir tāpēc, ka lietojumprogramma neapstiprina žurnāla rindas tipu vai saistīto izcenojumu, kas ievadīts žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="21999-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="21999-134">Ņemot vērā šī žurnāla tipa ietekmi, esiet piesardzīgs, kam tiek nodrošināta piekļuve, lai izveidotu ierakstu žurnālus.</span><span class="sxs-lookup"><span data-stu-id="21999-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="21999-135">Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem</span><span class="sxs-lookup"><span data-stu-id="21999-135">Recording actuals based on project events</span></span>

<span data-ttu-id="21999-136">PSA ieraksta finanšu transakcijas, kas notiek projekta laikā.</span><span class="sxs-lookup"><span data-stu-id="21999-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="21999-137">Šīs transakcijas tiek ierakstītas kā **faktiskie dati**.</span><span class="sxs-lookup"><span data-stu-id="21999-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="21999-138">Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.</span><span class="sxs-lookup"><span data-stu-id="21999-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="21999-139">**Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība**</span><span class="sxs-lookup"><span data-stu-id="21999-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="21999-140">Notikums</span><span class="sxs-lookup"><span data-stu-id="21999-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="21999-141">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="21999-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="21999-142">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="21999-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="21999-143">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="21999-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="21999-144">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="21999-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="21999-145">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="21999-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="21999-146">Faktiski</span><span class="sxs-lookup"><span data-stu-id="21999-146">Actuals</span></span></th>
<th><span data-ttu-id="21999-147">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="21999-147">Transaction currency</span></span></th>
<th><span data-ttu-id="21999-148">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="21999-148">Fixed price</span></span></th>
<th><span data-ttu-id="21999-149">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="21999-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="21999-150">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="21999-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="21999-151">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="21999-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-152">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="21999-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="21999-153">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="21999-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="21999-154">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="21999-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="21999-155">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-155">Cost actual</span></span></td>
<td><span data-ttu-id="21999-156">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-157">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-158">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="21999-159">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-160">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-161">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="21999-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="21999-162">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="21999-163">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="21999-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="21999-164">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-164">Cost actual</span></span></td>
<td><span data-ttu-id="21999-165">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-166">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-167">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-168">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-169">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-170">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="21999-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="21999-171">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-172">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="21999-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="21999-173">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="21999-174">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="21999-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="21999-175">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="21999-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="21999-176">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-177">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="21999-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-178">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-179">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-180">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-181">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="21999-181">Billed sales</span></span></td>
<td><span data-ttu-id="21999-182">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="21999-183">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="21999-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="21999-184">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="21999-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="21999-185">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-186">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-187">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-188">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-189">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-190">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="21999-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="21999-191">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-192">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="21999-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="21999-193">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="21999-194">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="21999-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="21999-195">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="21999-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="21999-196">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="21999-197">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="21999-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="21999-198">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="21999-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="21999-199">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="21999-200">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="21999-201">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-202">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="21999-202">Billed sales</span></span></td>
<td><span data-ttu-id="21999-203">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="21999-204">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="21999-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="21999-205">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="21999-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="21999-206">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-207">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="21999-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="21999-208">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-209">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="21999-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="21999-210">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="21999-211">**Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības**</span><span class="sxs-lookup"><span data-stu-id="21999-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="21999-212">Notikums</span><span class="sxs-lookup"><span data-stu-id="21999-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="21999-213">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="21999-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="21999-214">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="21999-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="21999-215">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="21999-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="21999-216">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="21999-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="21999-217">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="21999-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="21999-218">Faktiski</span><span class="sxs-lookup"><span data-stu-id="21999-218">Actuals</span></span></th>
<th><span data-ttu-id="21999-219">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="21999-219">Transaction currency</span></span></th>
<th><span data-ttu-id="21999-220">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="21999-220">Fixed price</span></span></th>
<th><span data-ttu-id="21999-221">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="21999-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="21999-222">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="21999-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="21999-223">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="21999-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-224">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="21999-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="21999-225">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="21999-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="21999-226">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="21999-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="21999-227">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-227">Cost actual</span></span></td>
<td><span data-ttu-id="21999-228">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="21999-229">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="21999-230">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="21999-231">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="21999-232">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-233">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="21999-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="21999-234">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-235">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="21999-236">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-237">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="21999-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="21999-238">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="21999-239">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="21999-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="21999-240">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-240">Cost actual</span></span></td>
<td><span data-ttu-id="21999-241">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="21999-242">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="21999-243">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="21999-244">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="21999-245">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-246">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="21999-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="21999-247">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-248">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="21999-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="21999-249">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="21999-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-250">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="21999-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="21999-251">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-252">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="21999-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="21999-253">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="21999-254">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="21999-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="21999-255">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="21999-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="21999-256">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-257">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="21999-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-258">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-259">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="21999-260">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-261">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="21999-261">Billed sales</span></span></td>
<td><span data-ttu-id="21999-262">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="21999-263">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="21999-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="21999-264">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="21999-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="21999-265">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-266">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-267">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-268">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21999-269">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-270">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="21999-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="21999-271">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-272">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="21999-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="21999-273">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="21999-274">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="21999-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="21999-275">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="21999-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="21999-276">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="21999-277">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="21999-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="21999-278">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="21999-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="21999-279">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="21999-280">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="21999-281">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="21999-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-282">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="21999-282">Billed sales</span></span></td>
<td><span data-ttu-id="21999-283">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="21999-284">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="21999-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="21999-285">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="21999-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="21999-286">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-287">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="21999-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="21999-288">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21999-289">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="21999-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="21999-290">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="21999-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]