---
title: Pārskats faktiski
description: Šajā tēmā ir sniegta informācija par projekta faktiskajiem datiem.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146132"
---
# <a name="actuals-overview"></a><span data-ttu-id="89de6-103">Pārskats faktiski</span><span class="sxs-lookup"><span data-stu-id="89de6-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="89de6-104">Faktiskie dati ir darba apjoms, kas ir pabeigts projektā.</span><span class="sxs-lookup"><span data-stu-id="89de6-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="89de6-105">Projekta faktiskos datus var izsekot līdz to avota dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="89de6-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="89de6-106">Šie avota dokumenti ietver laika, izdevumu un žurnālu ierakstus, kā arī rēķinus.</span><span class="sxs-lookup"><span data-stu-id="89de6-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kā projekta faktiskie dati tiek izsekoti līdz avota dokumentiem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="89de6-108">Laika ieraksta iesniegšana</span><span class="sxs-lookup"><span data-stu-id="89de6-108">Submitting a time entry</span></span>

<span data-ttu-id="89de6-109">Kad programmā PSA tiek iesniegts laika ieraksts projektam, kas ir kartēts uz laika un materiālu līguma rindu, tiek izveidotas divas žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="89de6-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="89de6-110">Viena rinda ir izmaksām, bet otra rinda ir paredzēta rēķinā neiekļautajai pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="89de6-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="89de6-111">Kad tiek iesniegts laika ieraksts projektam, kas ir kartēts uz fiksētas cenas līguma rindu, tiek izveidota žurnāla rinda tikai izmaksām.</span><span class="sxs-lookup"><span data-stu-id="89de6-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="89de6-112">Noklusējuma cenu ievadīšanas loģika atrodas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="89de6-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="89de6-113">Visas lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="89de6-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="89de6-114">Šajos laukos ir iekļauts transakcijas datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.</span><span class="sxs-lookup"><span data-stu-id="89de6-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="89de6-115">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Org. vienība**, izraisa atbilstošu cenu, kas pēc noklusējuma ir jāievada žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="89de6-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="89de6-116">Ja laika ierakstā pievienojat pielāgotu lauku un vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku entītijā Faktiskie dati un izmantojiet lauku kartējumus, lai kopētu lauku no laika ieraksta uz faktisko.</span><span class="sxs-lookup"><span data-stu-id="89de6-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="89de6-117">Izdevumu ieraksta iesniegšana</span><span class="sxs-lookup"><span data-stu-id="89de6-117">Submitting an expense entry</span></span>

<span data-ttu-id="89de6-118">Kad programmā PSA tiek iesniegts izdevumu ieraksts projektam, kas ir kartēts uz laika un materiālu līguma rindu, tiek izveidotas divas žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="89de6-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="89de6-119">Viena rinda ir izmaksām, bet otra rinda ir paredzēta rēķinā neiekļautajai pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="89de6-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="89de6-120">Kad tiek iesniegts izdevumu ieraksts projektam, kas ir kartēts uz fiksētas cenas līguma rindu, tiek izveidota žurnāla rinda tikai izmaksām.</span><span class="sxs-lookup"><span data-stu-id="89de6-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="89de6-121">Loģika, kas paredzēta izdevumu noklusējuma cenu ievadīšanai, ir atkarīga no izdevumu kategorijas, kas atlasīta lapā **Izdevumu ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="89de6-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="89de6-122">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="89de6-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="89de6-123">Tomēr pašai cenai summa, ko lietotājs ir ievadījis, tiek pēc noklusējuma iestatīta tieši saistītajās izdevumu žurnāla rindās izmaksām un pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="89de6-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="89de6-124">Pašreizējā PSA versijā nav pieejams no kategorijas atkarīgs noklusējuma cenu par vienību ieraksts izdevumu ierakstos.</span><span class="sxs-lookup"><span data-stu-id="89de6-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="89de6-125">Ierakstu žurnālu izmantošana izmaksu reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="89de6-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="89de6-126">Programmā PSA ierakstu žurnāli ļauj ierakstīt izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs.</span><span class="sxs-lookup"><span data-stu-id="89de6-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="89de6-127">Žurnālā ir virsraksts, rindas un darbība **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="89de6-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="89de6-128">Piedāvājam dažus scenārijus, kuros jūs varētu izmantot žurnālu.</span><span class="sxs-lookup"><span data-stu-id="89de6-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="89de6-129">Jums projektā Ir jāieraksta materiālu faktiskās izmaksas un pārdošana.</span><span class="sxs-lookup"><span data-stu-id="89de6-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="89de6-130">Jums ir jāpārvieto transakciju faktiskie dati no citas sistēmas uz PSA.</span><span class="sxs-lookup"><span data-stu-id="89de6-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="89de6-131">Jums ir jāieraksta izmaksas, kas radās citā sistēmā, piemēram, sagādes vai apakšlīgumu slēgšanas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="89de6-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89de6-132">Ierakstu žurnālu izmantošana, lai izveidotu faktiskos rezultātus, ir jāveic tikai lietotājam, kas pilnībā pārzina grāmatvedības ietekmi, kāda ir attiecībā uz faktiskajiem projektiem.</span><span class="sxs-lookup"><span data-stu-id="89de6-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="89de6-133">Tas ir tāpēc, ka lietojumprogramma neapstiprina žurnāla rindas tipu vai saistīto izcenojumu, kas ievadīts žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="89de6-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="89de6-134">Ņemot vērā šī žurnāla tipa ietekmi, esiet piesardzīgs, kam tiek nodrošināta piekļuve, lai izveidotu ierakstu žurnālus.</span><span class="sxs-lookup"><span data-stu-id="89de6-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="89de6-135">Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem</span><span class="sxs-lookup"><span data-stu-id="89de6-135">Recording actuals based on project events</span></span>

<span data-ttu-id="89de6-136">PSA ieraksta finanšu transakcijas, kas notiek projekta laikā.</span><span class="sxs-lookup"><span data-stu-id="89de6-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="89de6-137">Šīs transakcijas tiek ierakstītas kā **faktiskie dati**.</span><span class="sxs-lookup"><span data-stu-id="89de6-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="89de6-138">Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.</span><span class="sxs-lookup"><span data-stu-id="89de6-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="89de6-139">**Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība**</span><span class="sxs-lookup"><span data-stu-id="89de6-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="89de6-140">Notikums</span><span class="sxs-lookup"><span data-stu-id="89de6-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="89de6-141">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="89de6-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="89de6-142">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="89de6-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="89de6-143">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="89de6-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="89de6-144">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="89de6-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="89de6-145">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="89de6-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="89de6-146">Faktiski</span><span class="sxs-lookup"><span data-stu-id="89de6-146">Actuals</span></span></th>
<th><span data-ttu-id="89de6-147">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-147">Transaction currency</span></span></th>
<th><span data-ttu-id="89de6-148">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="89de6-148">Fixed price</span></span></th>
<th><span data-ttu-id="89de6-149">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="89de6-150">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="89de6-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="89de6-151">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="89de6-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-152">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="89de6-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="89de6-153">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="89de6-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="89de6-154">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="89de6-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="89de6-155">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-155">Cost actual</span></span></td>
<td><span data-ttu-id="89de6-156">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-157">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-158">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="89de6-159">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-160">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-161">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="89de6-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="89de6-162">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="89de6-163">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="89de6-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="89de6-164">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-164">Cost actual</span></span></td>
<td><span data-ttu-id="89de6-165">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-166">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-167">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-168">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-169">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-170">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="89de6-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="89de6-171">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-172">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="89de6-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="89de6-173">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="89de6-174">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="89de6-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="89de6-175">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="89de6-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="89de6-176">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-177">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="89de6-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-178">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-179">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-180">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-181">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="89de6-181">Billed sales</span></span></td>
<td><span data-ttu-id="89de6-182">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="89de6-183">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="89de6-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="89de6-184">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="89de6-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="89de6-185">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-186">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-187">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-188">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-189">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-190">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="89de6-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="89de6-191">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-192">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="89de6-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="89de6-193">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="89de6-194">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="89de6-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="89de6-195">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="89de6-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="89de6-196">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="89de6-197">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="89de6-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="89de6-198">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="89de6-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="89de6-199">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="89de6-200">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="89de6-201">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-202">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="89de6-202">Billed sales</span></span></td>
<td><span data-ttu-id="89de6-203">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="89de6-204">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="89de6-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="89de6-205">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="89de6-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="89de6-206">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-207">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="89de6-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="89de6-208">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-209">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="89de6-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="89de6-210">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="89de6-211">**Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības**</span><span class="sxs-lookup"><span data-stu-id="89de6-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="89de6-212">Notikums</span><span class="sxs-lookup"><span data-stu-id="89de6-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="89de6-213">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="89de6-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="89de6-214">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="89de6-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="89de6-215">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="89de6-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="89de6-216">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="89de6-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="89de6-217">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="89de6-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="89de6-218">Faktiski</span><span class="sxs-lookup"><span data-stu-id="89de6-218">Actuals</span></span></th>
<th><span data-ttu-id="89de6-219">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-219">Transaction currency</span></span></th>
<th><span data-ttu-id="89de6-220">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="89de6-220">Fixed price</span></span></th>
<th><span data-ttu-id="89de6-221">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="89de6-222">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="89de6-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="89de6-223">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="89de6-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-224">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="89de6-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="89de6-225">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="89de6-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="89de6-226">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="89de6-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="89de6-227">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-227">Cost actual</span></span></td>
<td><span data-ttu-id="89de6-228">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="89de6-229">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="89de6-230">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="89de6-231">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="89de6-232">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-233">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="89de6-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="89de6-234">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-235">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="89de6-236">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-237">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="89de6-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="89de6-238">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="89de6-239">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="89de6-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="89de6-240">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-240">Cost actual</span></span></td>
<td><span data-ttu-id="89de6-241">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="89de6-242">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="89de6-243">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="89de6-244">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="89de6-245">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-246">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="89de6-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="89de6-247">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-248">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="89de6-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="89de6-249">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-250">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="89de6-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="89de6-251">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-252">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="89de6-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="89de6-253">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="89de6-254">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="89de6-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="89de6-255">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="89de6-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="89de6-256">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-257">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="89de6-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-258">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-259">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="89de6-260">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-261">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="89de6-261">Billed sales</span></span></td>
<td><span data-ttu-id="89de6-262">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="89de6-263">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="89de6-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="89de6-264">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="89de6-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="89de6-265">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-266">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-267">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-268">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="89de6-269">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-270">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="89de6-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="89de6-271">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-272">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="89de6-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="89de6-273">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="89de6-274">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="89de6-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="89de6-275">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="89de6-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="89de6-276">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="89de6-277">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="89de6-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="89de6-278">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="89de6-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="89de6-279">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="89de6-280">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="89de6-281">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="89de6-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-282">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="89de6-282">Billed sales</span></span></td>
<td><span data-ttu-id="89de6-283">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="89de6-284">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="89de6-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="89de6-285">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="89de6-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="89de6-286">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-287">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="89de6-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="89de6-288">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="89de6-289">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="89de6-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="89de6-290">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="89de6-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
