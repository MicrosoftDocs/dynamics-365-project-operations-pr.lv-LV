---
title: Pārskats faktiski
description: Šajā tēmā ir sniegta informācija par projekta faktiskajiem datiem.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080642"
---
# <a name="actuals-overview"></a><span data-ttu-id="cec76-103">Pārskats faktiski</span><span class="sxs-lookup"><span data-stu-id="cec76-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cec76-104">Faktiskie dati ir darba apjoms, kas ir pabeigts projektā.</span><span class="sxs-lookup"><span data-stu-id="cec76-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="cec76-105">Projekta faktiskos datus var izsekot līdz to avota dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="cec76-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="cec76-106">Šie avota dokumenti ietver laika, izdevumu un žurnālu ierakstus, kā arī rēķinus.</span><span class="sxs-lookup"><span data-stu-id="cec76-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kā projekta faktiskie dati tiek izsekoti līdz avota dokumentiem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="cec76-108">Laika ieraksta iesniegšana</span><span class="sxs-lookup"><span data-stu-id="cec76-108">Submitting a time entry</span></span>

<span data-ttu-id="cec76-109">Kad programmā PSA tiek iesniegts laika ieraksts projektam, kas ir kartēts uz laika un materiālu līguma rindu, tiek izveidotas divas žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="cec76-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="cec76-110">Viena rinda ir izmaksām, bet otra rinda ir paredzēta rēķinā neiekļautajai pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="cec76-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="cec76-111">Kad tiek iesniegts laika ieraksts projektam, kas ir kartēts uz fiksētas cenas līguma rindu, tiek izveidota žurnāla rinda tikai izmaksām.</span><span class="sxs-lookup"><span data-stu-id="cec76-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="cec76-112">Noklusējuma cenu ievadīšanas loģika atrodas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="cec76-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="cec76-113">Visas lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="cec76-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="cec76-114">Šajos laukos ir iekļauts transakcijas datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.</span><span class="sxs-lookup"><span data-stu-id="cec76-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="cec76-115">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Org. vienība** , izraisa atbilstošu cenu, kas pēc noklusējuma ir jāievada žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="cec76-115">The fields that affect default prices, such as **Role** and **Org Unit** , cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="cec76-116">Ja laika ierakstā pievienojat pielāgotu lauku un vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku entītijā Faktiskie dati un izmantojiet lauku kartējumus, lai kopētu lauku no laika ieraksta uz faktisko.</span><span class="sxs-lookup"><span data-stu-id="cec76-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="cec76-117">Izdevumu ieraksta iesniegšana</span><span class="sxs-lookup"><span data-stu-id="cec76-117">Submitting an expense entry</span></span>

<span data-ttu-id="cec76-118">Kad programmā PSA tiek iesniegts izdevumu ieraksts projektam, kas ir kartēts uz laika un materiālu līguma rindu, tiek izveidotas divas žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="cec76-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="cec76-119">Viena rinda ir izmaksām, bet otra rinda ir paredzēta rēķinā neiekļautajai pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="cec76-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="cec76-120">Kad tiek iesniegts izdevumu ieraksts projektam, kas ir kartēts uz fiksētas cenas līguma rindu, tiek izveidota žurnāla rinda tikai izmaksām.</span><span class="sxs-lookup"><span data-stu-id="cec76-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="cec76-121">Loģika, kas paredzēta izdevumu noklusējuma cenu ievadīšanai, ir atkarīga no izdevumu kategorijas, kas atlasīta lapā **Izdevumu ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="cec76-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="cec76-122">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="cec76-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="cec76-123">Tomēr pašai cenai summa, ko lietotājs ir ievadījis, tiek pēc noklusējuma iestatīta tieši saistītajās izdevumu žurnāla rindās izmaksām un pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="cec76-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="cec76-124">Pašreizējā PSA versijā nav pieejams no kategorijas atkarīgs noklusējuma cenu par vienību ieraksts izdevumu ierakstos.</span><span class="sxs-lookup"><span data-stu-id="cec76-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="cec76-125">Ierakstu žurnālu izmantošana izmaksu reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="cec76-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="cec76-126">Programmā PSA ierakstu žurnāli ļauj ierakstīt izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs.</span><span class="sxs-lookup"><span data-stu-id="cec76-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="cec76-127">Žurnālā ir virsraksts, rindas un darbība **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="cec76-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="cec76-128">Piedāvājam dažus scenārijus, kuros jūs varētu izmantot žurnālu.</span><span class="sxs-lookup"><span data-stu-id="cec76-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="cec76-129">Jums projektā Ir jāieraksta materiālu faktiskās izmaksas un pārdošana.</span><span class="sxs-lookup"><span data-stu-id="cec76-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="cec76-130">Jums ir jāpārvieto transakciju faktiskie dati no citas sistēmas uz PSA.</span><span class="sxs-lookup"><span data-stu-id="cec76-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="cec76-131">Jums ir jāieraksta izmaksas, kas radās citā sistēmā, piemēram, sagādes vai apakšlīgumu slēgšanas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="cec76-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cec76-132">Ierakstu žurnālu izmantošana, lai izveidotu faktiskos rezultātus, ir jāveic tikai lietotājam, kas pilnībā pārzina grāmatvedības ietekmi, kāda ir attiecībā uz faktiskajiem projektiem.</span><span class="sxs-lookup"><span data-stu-id="cec76-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="cec76-133">Tas ir tāpēc, ka lietojumprogramma neapstiprina žurnāla rindas tipu vai saistīto izcenojumu, kas ievadīts žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="cec76-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="cec76-134">Ņemot vērā šī žurnāla tipa ietekmi, esiet piesardzīgs, kam tiek nodrošināta piekļuve, lai izveidotu ierakstu žurnālus.</span><span class="sxs-lookup"><span data-stu-id="cec76-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="cec76-135">Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem</span><span class="sxs-lookup"><span data-stu-id="cec76-135">Recording actuals based on project events</span></span>

<span data-ttu-id="cec76-136">PSA ieraksta finanšu transakcijas, kas notiek projekta laikā.</span><span class="sxs-lookup"><span data-stu-id="cec76-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="cec76-137">Šīs transakcijas tiek ierakstītas kā **faktiskie dati**.</span><span class="sxs-lookup"><span data-stu-id="cec76-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="cec76-138">Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.</span><span class="sxs-lookup"><span data-stu-id="cec76-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="cec76-139">**Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība**</span><span class="sxs-lookup"><span data-stu-id="cec76-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cec76-140">Notikums</span><span class="sxs-lookup"><span data-stu-id="cec76-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cec76-141">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="cec76-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cec76-142">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="cec76-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cec76-143">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="cec76-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cec76-144">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="cec76-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cec76-145">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="cec76-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cec76-146">Faktiski</span><span class="sxs-lookup"><span data-stu-id="cec76-146">Actuals</span></span></th>
<th><span data-ttu-id="cec76-147">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-147">Transaction currency</span></span></th>
<th><span data-ttu-id="cec76-148">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="cec76-148">Fixed price</span></span></th>
<th><span data-ttu-id="cec76-149">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cec76-150">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="cec76-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cec76-151">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="cec76-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-152">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="cec76-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cec76-153">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="cec76-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cec76-154">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="cec76-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cec76-155">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-155">Cost actual</span></span></td>
<td><span data-ttu-id="cec76-156">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-157">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-158">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="cec76-159">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-160">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-161">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="cec76-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cec76-162">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cec76-163">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="cec76-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cec76-164">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-164">Cost actual</span></span></td>
<td><span data-ttu-id="cec76-165">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-166">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-167">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-168">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-169">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-170">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="cec76-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cec76-171">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-172">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="cec76-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cec76-173">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cec76-174">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="cec76-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cec76-175">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="cec76-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cec76-176">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-177">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="cec76-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-178">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-179">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-180">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-181">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="cec76-181">Billed sales</span></span></td>
<td><span data-ttu-id="cec76-182">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cec76-183">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="cec76-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cec76-184">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="cec76-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cec76-185">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-186">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-187">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-188">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-189">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-190">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="cec76-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cec76-191">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-192">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="cec76-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cec76-193">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cec76-194">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="cec76-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cec76-195">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="cec76-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cec76-196">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cec76-197">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="cec76-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cec76-198">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="cec76-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cec76-199">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cec76-200">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cec76-201">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-202">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="cec76-202">Billed sales</span></span></td>
<td><span data-ttu-id="cec76-203">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cec76-204">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="cec76-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cec76-205">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="cec76-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cec76-206">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-207">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="cec76-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cec76-208">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-209">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="cec76-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cec76-210">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cec76-211">**Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības**</span><span class="sxs-lookup"><span data-stu-id="cec76-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cec76-212">Notikums</span><span class="sxs-lookup"><span data-stu-id="cec76-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cec76-213">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="cec76-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cec76-214">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="cec76-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cec76-215">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="cec76-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cec76-216">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="cec76-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cec76-217">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="cec76-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cec76-218">Faktiski</span><span class="sxs-lookup"><span data-stu-id="cec76-218">Actuals</span></span></th>
<th><span data-ttu-id="cec76-219">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-219">Transaction currency</span></span></th>
<th><span data-ttu-id="cec76-220">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="cec76-220">Fixed price</span></span></th>
<th><span data-ttu-id="cec76-221">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cec76-222">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="cec76-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cec76-223">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="cec76-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-224">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="cec76-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cec76-225">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="cec76-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="cec76-226">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="cec76-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cec76-227">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-227">Cost actual</span></span></td>
<td><span data-ttu-id="cec76-228">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cec76-229">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cec76-230">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cec76-231">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cec76-232">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-233">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="cec76-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cec76-234">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-235">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cec76-236">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-237">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="cec76-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cec76-238">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cec76-239">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="cec76-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cec76-240">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-240">Cost actual</span></span></td>
<td><span data-ttu-id="cec76-241">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cec76-242">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cec76-243">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cec76-244">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cec76-245">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-246">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="cec76-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cec76-247">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-248">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="cec76-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cec76-249">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-250">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="cec76-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cec76-251">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-252">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="cec76-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cec76-253">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cec76-254">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="cec76-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cec76-255">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="cec76-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cec76-256">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-257">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="cec76-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-258">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-259">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cec76-260">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-261">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="cec76-261">Billed sales</span></span></td>
<td><span data-ttu-id="cec76-262">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cec76-263">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="cec76-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cec76-264">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="cec76-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cec76-265">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-266">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-267">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-268">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cec76-269">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-270">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="cec76-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cec76-271">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-272">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="cec76-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cec76-273">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cec76-274">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="cec76-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cec76-275">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="cec76-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cec76-276">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cec76-277">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="cec76-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cec76-278">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="cec76-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cec76-279">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cec76-280">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cec76-281">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="cec76-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-282">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="cec76-282">Billed sales</span></span></td>
<td><span data-ttu-id="cec76-283">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cec76-284">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="cec76-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cec76-285">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="cec76-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cec76-286">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-287">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="cec76-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cec76-288">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cec76-289">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="cec76-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cec76-290">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="cec76-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
