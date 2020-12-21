---
title: Vairāku valūtu scenāriji (versija 3.x)
description: Šajā tēmā ir sniegta informācija par vairāku valūtu scenārijiem.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 61ca37db59b7d25478434c2376e3a987afd4972d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123387"
---
# <a name="multiple-currency-scenarios"></a><span data-ttu-id="b4f65-103">Vairāku valūtu scenāriji</span><span class="sxs-lookup"><span data-stu-id="b4f65-103">Multiple-currency scenarios</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b4f65-104">Programmā Microsoft Dynamics 365 ir divas valūtu koncepcijas.</span><span class="sxs-lookup"><span data-stu-id="b4f65-104">Microsoft Dynamics 365 has two concepts of currencies:</span></span>

- <span data-ttu-id="b4f65-105">**Transakcijas valūta** — valūta, kādā tiek veikta transakcija.</span><span class="sxs-lookup"><span data-stu-id="b4f65-105">**Transaction currency** - The currency that a transaction occurs in.</span></span> 
- <span data-ttu-id="b4f65-106">**Pamatvalūta** — Dynamics 365 instances valūta.</span><span class="sxs-lookup"><span data-stu-id="b4f65-106">**Base currency** - The currency of the Dynamics 365 instance.</span></span> <span data-ttu-id="b4f65-107">Šī valūta tiek iestatīta, kad tiek nodrošināta Dynamics 365 instance.</span><span class="sxs-lookup"><span data-stu-id="b4f65-107">This currency is set up when a Dynamics 365 instance is provisioned.</span></span> <span data-ttu-id="b4f65-108">To nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="b4f65-108">It can’t be changed.</span></span>

<span data-ttu-id="b4f65-109">Piemēram, Contoso ASV pārdeva 100 T kreklus klientam Apvienotajā Karalistē par 15 sterliņu mārciņām (GBP) gabalā.</span><span class="sxs-lookup"><span data-stu-id="b4f65-109">For example, Contoso US sold 100 t-shirts to a customer in the UK for 15 ounds sterling (GBP) each.</span></span> <span data-ttu-id="b4f65-110">Tālāk esošajā tabulā ir parādīts, kā šī transakcija tiek ierakstīta entītijā Pasūtījuma prece.</span><span class="sxs-lookup"><span data-stu-id="b4f65-110">The following table shows how this transaction is recorded in the Order Product entity.</span></span>

| <span data-ttu-id="b4f65-111">Produkts</span><span class="sxs-lookup"><span data-stu-id="b4f65-111">Product</span></span> | <span data-ttu-id="b4f65-112">Daudzums</span><span class="sxs-lookup"><span data-stu-id="b4f65-112">Quantity</span></span> | <span data-ttu-id="b4f65-113">Vienības cena</span><span class="sxs-lookup"><span data-stu-id="b4f65-113">Price per unit</span></span> | <span data-ttu-id="b4f65-114">Valūta</span><span class="sxs-lookup"><span data-stu-id="b4f65-114">Currency</span></span> | <span data-ttu-id="b4f65-115">Summa</span><span class="sxs-lookup"><span data-stu-id="b4f65-115">Amount</span></span> | <span data-ttu-id="b4f65-116">Maiņas kurss</span><span class="sxs-lookup"><span data-stu-id="b4f65-116">Exchange rate</span></span> | <span data-ttu-id="b4f65-117">Vienības cena (pamatvalūtā)</span><span class="sxs-lookup"><span data-stu-id="b4f65-117">Price per unit (Base)</span></span>| <span data-ttu-id="b4f65-118">Summa (pamatvalūtā)</span><span class="sxs-lookup"><span data-stu-id="b4f65-118">Amount (Base)</span></span>|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| <span data-ttu-id="b4f65-119">T krekls</span><span class="sxs-lookup"><span data-stu-id="b4f65-119">T-shirt</span></span> | <span data-ttu-id="b4f65-120">100</span><span class="sxs-lookup"><span data-stu-id="b4f65-120">100</span></span>      | <span data-ttu-id="b4f65-121">15</span><span class="sxs-lookup"><span data-stu-id="b4f65-121">15</span></span>             | <span data-ttu-id="b4f65-122">GBP</span><span class="sxs-lookup"><span data-stu-id="b4f65-122">GBP</span></span>      | <span data-ttu-id="b4f65-123">1500</span><span class="sxs-lookup"><span data-stu-id="b4f65-123">1500</span></span>   | <span data-ttu-id="b4f65-124">0.94</span><span class="sxs-lookup"><span data-stu-id="b4f65-124">0.94</span></span>          | <span data-ttu-id="b4f65-125">17,25 $</span><span class="sxs-lookup"><span data-stu-id="b4f65-125">$17.25</span></span>               | <span data-ttu-id="b4f65-126">1725 $</span><span class="sxs-lookup"><span data-stu-id="b4f65-126">$1,725</span></span>       |

<span data-ttu-id="b4f65-127">Kolonnā **Valūta** ir redzama transakcijas valūta, kas ir valūta, kurā notika pārdošana.</span><span class="sxs-lookup"><span data-stu-id="b4f65-127">The **Currency** column shows the transaction currency, which is the currency that the sale occurred in.</span></span> <span data-ttu-id="b4f65-128">Kolonnā **Maiņas kurss** ir redzams transakcijas valūtas un pamatvalūtas maiņas kurss.</span><span class="sxs-lookup"><span data-stu-id="b4f65-128">The **Exchange rate** column is the exchange rate between the transaction currency and the base currency.</span></span> <span data-ttu-id="b4f65-129">Pamatvalūta ir ASV dolāri (USD).</span><span class="sxs-lookup"><span data-stu-id="b4f65-129">The base currency is US dollar (USD).</span></span> <span data-ttu-id="b4f65-130">Šī pamatvalūta tika iestatīta, kad tika nodrošināta Dynamics 365 instance.</span><span class="sxs-lookup"><span data-stu-id="b4f65-130">This base currency was set up when the Dynamics 365 instance was provisioned.</span></span>
<span data-ttu-id="b4f65-131">Kā redzams tabulā, katra transakcija tiek ierakstīta gan transakcijas valūtā, gan pamatvalūtā.</span><span class="sxs-lookup"><span data-stu-id="b4f65-131">As the table shows, every transaction is recorded in both the transaction currency and the base currency.</span></span> <span data-ttu-id="b4f65-132">Dynamics 365 izmanto valūtas maiņas kursu, lai aprēķinātu pamatvalūtas summas.</span><span class="sxs-lookup"><span data-stu-id="b4f65-132">Dynamics 365 uses the currency exchange rate to calculate the base currency amounts.</span></span>

## <a name="project-service-automation-extensions"></a><span data-ttu-id="b4f65-133">Project Service Automation paplašinājumi</span><span class="sxs-lookup"><span data-stu-id="b4f65-133">Project Service Automation extensions</span></span>

<span data-ttu-id="b4f65-134">Dynamics 365 Project Service Automation ietekmē transakcijas valūtu, jo biznesa transakcijām parasti ir divi aspekti: izmaksas un pārdošana.</span><span class="sxs-lookup"><span data-stu-id="b4f65-134">Dynamics 365 Project Service Automation influences the transaction currency, because business transactions usually have two aspects: cost and sales.</span></span>

<span data-ttu-id="b4f65-135">Tālāk norādītās entītijas tiek uzskatītas par biznesa transakcijām.</span><span class="sxs-lookup"><span data-stu-id="b4f65-135">The following entities are considered business transactions:</span></span>

- <span data-ttu-id="b4f65-136">Piedāvājuma rindas informācija</span><span class="sxs-lookup"><span data-stu-id="b4f65-136">Quote line detail</span></span>
- <span data-ttu-id="b4f65-137">Projekta līguma rindas detaļas</span><span class="sxs-lookup"><span data-stu-id="b4f65-137">Project contract line detail</span></span>
- <span data-ttu-id="b4f65-138">Novērtējuma rinda</span><span class="sxs-lookup"><span data-stu-id="b4f65-138">Estimate line</span></span>
- <span data-ttu-id="b4f65-139">Žurnāla rinda</span><span class="sxs-lookup"><span data-stu-id="b4f65-139">Journal line</span></span>
- <span data-ttu-id="b4f65-140">Rēķina rindas detaļas</span><span class="sxs-lookup"><span data-stu-id="b4f65-140">Invoice line detail</span></span>
- <span data-ttu-id="b4f65-141">Faktiski</span><span class="sxs-lookup"><span data-stu-id="b4f65-141">Actual</span></span>

<span data-ttu-id="b4f65-142">Katrā no šīm entītijām ir ieraksts, kas norāda izmaksu summu vai pārdošanas summu.</span><span class="sxs-lookup"><span data-stu-id="b4f65-142">In each of these entities, there is a record that represents the cost amount or the sales amount.</span></span> <span data-ttu-id="b4f65-143">Katrai Dynamics 365 entītijai, kurai ir lauks **Summa** katrs ieraksts ietver summas gan transakcijas valūtā, gan pamatvalūtā.</span><span class="sxs-lookup"><span data-stu-id="b4f65-143">As for any Dynamics 365 entity that has an **Amount** field, each record includes amounts in both the transaction currency and the base currency.</span></span> 

<span data-ttu-id="b4f65-144">PSA paplašina transakcijas valūtas koncepciju izmaksām un pārdošanai tālāk aprakstītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="b4f65-144">PSA expands the concept of transaction currency for the cost and sales in the following ways:</span></span>

- <span data-ttu-id="b4f65-145">Izmaksu transakcijas valūta laika transakcijām vienmēr tiek iegūta no tās organizācijas struktūrvienības valūtas, kurai pieder projekts vai kas to pārvalda.</span><span class="sxs-lookup"><span data-stu-id="b4f65-145">The cost transaction currency for time transactions always comes from the currency of the organization unit that owns or manages the project.</span></span> <span data-ttu-id="b4f65-146">Šo organizācijas struktūrvienību sauc par līgumslēdzēja struktūrvienību.</span><span class="sxs-lookup"><span data-stu-id="b4f65-146">This organization unit is known as the contracting unit.</span></span>
- <span data-ttu-id="b4f65-147">Pārdošanas transakcijas valūta laika un izdevumu transakcijām vienmēr tiek iegūta no projekta līguma valūtas.</span><span class="sxs-lookup"><span data-stu-id="b4f65-147">The sales transaction currency for time and expense transactions always comes from the currency of the project contract.</span></span>
- <span data-ttu-id="b4f65-148">Izmaksu transakcijas valūta izdevumiem tiek iegūta no valūtas, kurā tika izveidots izdevumu ieraksts.</span><span class="sxs-lookup"><span data-stu-id="b4f65-148">The cost transaction currency for expenses comes from the currency that the expense entry was created in.</span></span>

## <a name="multiple-currency-scenario"></a><span data-ttu-id="b4f65-149">Vairāku valūtu scenārijs</span><span class="sxs-lookup"><span data-stu-id="b4f65-149">Multiple-currency scenario</span></span>

<span data-ttu-id="b4f65-150">Šajā sadaļā ir aprakstīts projekta piemērs, kurā Contoso UK veic piegādi klientam ar nosaukumu Fabrikam — Japāna.</span><span class="sxs-lookup"><span data-stu-id="b4f65-150">This section describes an example of a project that Contoso UK delivers for a customer that is named Fabrikam, Japan.</span></span> <span data-ttu-id="b4f65-151">Tālāk norādīti scenārija parametri.</span><span class="sxs-lookup"><span data-stu-id="b4f65-151">Here is how the scenario has been set up:</span></span>

1. <span data-ttu-id="b4f65-152">Sadaļās **Iestatījumi** \> **Uzņēmuma pārvaldība** \> **Valūtas** tiek iestatītas valūtas GBP un Japānas jēna (JPY).</span><span class="sxs-lookup"><span data-stu-id="b4f65-152">GBP and Japanese yen (JPY) are set up under **Settings** \> **Business Management** \> **Currencies**.</span></span> 
2. <span data-ttu-id="b4f65-153">Tiek iestatīts klienta uzņēmums ar nosaukumu **Fabrikam — Japāna**, un kā uzņēmuma valūta tiek atlasīta JPY.</span><span class="sxs-lookup"><span data-stu-id="b4f65-153">A customer account that is named **Fabrikam - Japan** is set up, and JPY is selected as the currency on the account.</span></span>
3. <span data-ttu-id="b4f65-154">Tiek iestatīta organizācijas struktūrvienība ar nosaukumu **Contoso UK**, un kā valūta tiek atlasīta GBP.</span><span class="sxs-lookup"><span data-stu-id="b4f65-154">An organization unit that is named **Contoso UK** is set up, and GBP is selected as the currency.</span></span>
4. <span data-ttu-id="b4f65-155">Tiek izveidots projekta līgums, kurā **Contoso UK** ir norādīta kā līgumslēdzēja struktūrvienība, bet uzņēmums **Fabrikam — Japāna** ir norādīts kā klients.</span><span class="sxs-lookup"><span data-stu-id="b4f65-155">A project contract is created, where **Contoso UK** is specified as the contracting unit and **Fabrikam – Japan** is specified as the customer.</span></span>
5. <span data-ttu-id="b4f65-156">Projekta līguma rindas tiek izveidotas, pamatojoties uz dažādo projekta transakciju klašu rēķinu izkārtojumiem, piemēram, rēķina izrakstīšana par laiku un rēķina izrakstīšana par izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="b4f65-156">Project contract lines are created, based on the billing arrangements for the various transaction classes on the project, such as billing for time versus billing for expenses.</span></span>
6. <span data-ttu-id="b4f65-157">Tiek izveidots projekts, kurā **Contoso UK** ir norādīta kā līgumslēdzēja struktūrvienība.</span><span class="sxs-lookup"><span data-stu-id="b4f65-157">A project is created where **Contoso UK** is specified as the contracting unit.</span></span> <span data-ttu-id="b4f65-158">Šis projekts tiek izveidots un kartēts uz projekta līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="b4f65-158">This project is created and mapped to the project contract lines.</span></span>


<span data-ttu-id="b4f65-159">Novērtējuma laikā, kurā tiek izmantotas piedāvājuma rindas detaļas, projekta līguma rindas detaļas vai grafika novērtējuma rinda, entītijā vienmēr tiek izveidoti divi ieraksti.</span><span class="sxs-lookup"><span data-stu-id="b4f65-159">During estimation that uses the quote line detail, the project contract line detail, or on the estimate line of the schedule, two records are always created in the entity.</span></span> <span data-ttu-id="b4f65-160">Viens ieraksts ir izmaksām, bet otrs ieraksts ir paredzēts pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="b4f65-160">One record is for cost, and the other record is for sales.</span></span>

- <span data-ttu-id="b4f65-161">Pēc noklusējuma izmaksu ierakstā transakcijas valūta tiek iestatīta uz projekta līgumslēdzēja struktūrvienības valūtu.</span><span class="sxs-lookup"><span data-stu-id="b4f65-161">By default, the transaction currency on the cost record is set to the currency of the project’s contracting unit.</span></span> <span data-ttu-id="b4f65-162">Šajā piemērā šī valūta ir GBP.</span><span class="sxs-lookup"><span data-stu-id="b4f65-162">In this example, the currency is GBP.</span></span>
- <span data-ttu-id="b4f65-163">Pēc noklusējuma pārdošanas ierakstā transakcijas valūta tiek iestatīta uz projekta līguma valūtu.</span><span class="sxs-lookup"><span data-stu-id="b4f65-163">By default, the transaction currency on the sales record is set to the currency of the project contract.</span></span> <span data-ttu-id="b4f65-164">Šajā piemērā šī valūta ir JPY.</span><span class="sxs-lookup"><span data-stu-id="b4f65-164">In this example, the currency is JPY.</span></span>

<span data-ttu-id="b4f65-165">Kad tiek izveidoti laika faktiskie dati, izmantojot laika ierakstu vai žurnāla rindu, rodas tālāk norādītā uzvedība.</span><span class="sxs-lookup"><span data-stu-id="b4f65-165">When actuals are created for time using time entry or the journal line, the following behavior occurs:</span></span>

- <span data-ttu-id="b4f65-166">Pēc noklusējuma izmaksu ierakstā transakcijas valūta tiek iestatīta uz projekta līgumslēdzēja struktūrvienības valūtu.</span><span class="sxs-lookup"><span data-stu-id="b4f65-166">By default, the transaction currency on the cost record is set to the currency of the project's contracting unit.</span></span>
- <span data-ttu-id="b4f65-167">Pēc noklusējuma pārdošanas ierakstā transakcijas valūta tiek iestatīta uz projekta līguma valūtu.</span><span class="sxs-lookup"><span data-stu-id="b4f65-167">By default, the transaction currency on the sales record is set to the currency of the project contract.</span></span>

<span data-ttu-id="b4f65-168">Kad tiek izveidoti izdevumu faktiskie dati, izmantojot izmaksu ierakstu vai žurnāla rindu, rodas tālāk norādītā uzvedība.</span><span class="sxs-lookup"><span data-stu-id="b4f65-168">When actuals are created for expenses by the expense entry or journal line, the following behavior occurs:</span></span>

- <span data-ttu-id="b4f65-169">Izdevumu summu var reģistrēt jebkurā valūtā.</span><span class="sxs-lookup"><span data-stu-id="b4f65-169">You can record the expense amount in any currency.</span></span> <span data-ttu-id="b4f65-170">Atlasiet valūtu, izmantojot valūtas atlasītāju lapā **Izdevumu ieraksts** vai lapā **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="b4f65-170">Select the currency by using the currency picker on the **Expense Entry** page or the **Journal Line** page.</span></span> <span data-ttu-id="b4f65-171">Pēc noklusējuma izmaksu ierakstā transakcijas valūta tiek iestatīta uz izdevumu ieraksta valūtu.</span><span class="sxs-lookup"><span data-stu-id="b4f65-171">By default, the transaction currency for the cost record is set to the currency on the expense entry.</span></span> 
- <span data-ttu-id="b4f65-172">Pēc noklusējuma pārdošanas ierakstā transakcijas valūta ir projekta līguma valūta.</span><span class="sxs-lookup"><span data-stu-id="b4f65-172">By default, the transaction currency for sales record is the currency of the project contract.</span></span> <span data-ttu-id="b4f65-173">Lai iestatītu šo valūtu, sistēma vispirms pārvērš transakcijas summu valūtā, kādu lietotājs ir ievadījis pamatvalūtā.</span><span class="sxs-lookup"><span data-stu-id="b4f65-173">To set this currency, the system first converts the transaction amount in the currency that the user entered to the base currency.</span></span> <span data-ttu-id="b4f65-174">Pēc tam tā pārvērš summu projekta līguma valūtā.</span><span class="sxs-lookup"><span data-stu-id="b4f65-174">It then converts the amount to the currency of the project contract.</span></span> 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a><span data-ttu-id="b4f65-175">Apkopojumu aprēķināšana, kad projekta faktiskie ieraksti tiek ierakstīti vairākās transakciju valūtās</span><span class="sxs-lookup"><span data-stu-id="b4f65-175">Computing roll-ups when project actuals are recorded in multiple transaction currencies</span></span>

<span data-ttu-id="b4f65-176">Dynamics 365 automātiski apstrādā dažādās valūtās esošu summu apkopojumus.</span><span class="sxs-lookup"><span data-stu-id="b4f65-176">Dynamics 365 automatically handles roll-ups of amounts in different currencies.</span></span> <span data-ttu-id="b4f65-177">Tālāk sniegts piemērs.</span><span class="sxs-lookup"><span data-stu-id="b4f65-177">Here is an example.</span></span>

| <span data-ttu-id="b4f65-178">Transakciju klase</span><span class="sxs-lookup"><span data-stu-id="b4f65-178">Transaction class</span></span> | <span data-ttu-id="b4f65-179">Transakcijas tips</span><span class="sxs-lookup"><span data-stu-id="b4f65-179">Transaction type</span></span>| <span data-ttu-id="b4f65-180">Date</span><span class="sxs-lookup"><span data-stu-id="b4f65-180">Date</span></span>   | <span data-ttu-id="b4f65-181">Resurss</span><span class="sxs-lookup"><span data-stu-id="b4f65-181">Resource</span></span> | <span data-ttu-id="b4f65-182">Transakciju kategorija</span><span class="sxs-lookup"><span data-stu-id="b4f65-182">Transaction category</span></span> | <span data-ttu-id="b4f65-183">Daudzums</span><span class="sxs-lookup"><span data-stu-id="b4f65-183">Quantity</span></span> | <span data-ttu-id="b4f65-184">Vienības cena</span><span class="sxs-lookup"><span data-stu-id="b4f65-184">Unit price</span></span> | <span data-ttu-id="b4f65-185">Summa</span><span class="sxs-lookup"><span data-stu-id="b4f65-185">Amount</span></span>      | <span data-ttu-id="b4f65-186">Maiņas kurss</span><span class="sxs-lookup"><span data-stu-id="b4f65-186">Exchange rate</span></span> | <span data-ttu-id="b4f65-187">Summa pamatvalūtā</span><span class="sxs-lookup"><span data-stu-id="b4f65-187">Amount in base</span></span> |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| <span data-ttu-id="b4f65-188">Time</span><span class="sxs-lookup"><span data-stu-id="b4f65-188">Time</span></span>              | <span data-ttu-id="b4f65-189">Rēķinā neiekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="b4f65-189">Unbilled sales</span></span>   | <span data-ttu-id="b4f65-190">14. jūn.</span><span class="sxs-lookup"><span data-stu-id="b4f65-190">14-Jun</span></span> | <span data-ttu-id="b4f65-191">Konrāds</span><span class="sxs-lookup"><span data-stu-id="b4f65-191">Prakash</span></span>  |                      | <span data-ttu-id="b4f65-192">8 st.</span><span class="sxs-lookup"><span data-stu-id="b4f65-192">8 hrs</span></span>    | <span data-ttu-id="b4f65-193">20 000 JPY</span><span class="sxs-lookup"><span data-stu-id="b4f65-193">20,000 JPY</span></span>    | <span data-ttu-id="b4f65-194">160 000 JPY</span><span class="sxs-lookup"><span data-stu-id="b4f65-194">160,000 JPY</span></span> | <span data-ttu-id="b4f65-195">123</span><span class="sxs-lookup"><span data-stu-id="b4f65-195">123</span></span>           | <span data-ttu-id="b4f65-196">1300,81 USD</span><span class="sxs-lookup"><span data-stu-id="b4f65-196">1,300.81 USD</span></span>    |
| <span data-ttu-id="b4f65-197">Time</span><span class="sxs-lookup"><span data-stu-id="b4f65-197">Time</span></span>              | <span data-ttu-id="b4f65-198">Rēķinā neiekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="b4f65-198">Unbilled sales</span></span>   | <span data-ttu-id="b4f65-199">15. jūn.</span><span class="sxs-lookup"><span data-stu-id="b4f65-199">15-Jun</span></span> | <span data-ttu-id="b4f65-200">Konrāds</span><span class="sxs-lookup"><span data-stu-id="b4f65-200">Prakash</span></span>  |                      | <span data-ttu-id="b4f65-201">8 st.</span><span class="sxs-lookup"><span data-stu-id="b4f65-201">8 hrs</span></span>    | <span data-ttu-id="b4f65-202">20 000 JPY</span><span class="sxs-lookup"><span data-stu-id="b4f65-202">20,000 JPY</span></span>    | <span data-ttu-id="b4f65-203">160 000 JPY</span><span class="sxs-lookup"><span data-stu-id="b4f65-203">160,000 JPY</span></span> | <span data-ttu-id="b4f65-204">123</span><span class="sxs-lookup"><span data-stu-id="b4f65-204">123</span></span>           | <span data-ttu-id="b4f65-205">1300,81 USD</span><span class="sxs-lookup"><span data-stu-id="b4f65-205">1,300.81 USD</span></span>    |
| <span data-ttu-id="b4f65-206">Izdevumi</span><span class="sxs-lookup"><span data-stu-id="b4f65-206">Expense</span></span>           | <span data-ttu-id="b4f65-207">Rēķinā neiekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="b4f65-207">Unbilled sales</span></span>   | <span data-ttu-id="b4f65-208">16. jūn.</span><span class="sxs-lookup"><span data-stu-id="b4f65-208">16-Jun</span></span> | <span data-ttu-id="b4f65-209">Konrāds</span><span class="sxs-lookup"><span data-stu-id="b4f65-209">Prakash</span></span>  | <span data-ttu-id="b4f65-210">Viesnīca</span><span class="sxs-lookup"><span data-stu-id="b4f65-210">Hotel</span></span>                | <span data-ttu-id="b4f65-211">1 EA</span><span class="sxs-lookup"><span data-stu-id="b4f65-211">1 ea</span></span>     | <span data-ttu-id="b4f65-212">250 EUR</span><span class="sxs-lookup"><span data-stu-id="b4f65-212">250 EUR</span></span>      | <span data-ttu-id="b4f65-213">250 EUR</span><span class="sxs-lookup"><span data-stu-id="b4f65-213">250 EUR</span></span>     | <span data-ttu-id="b4f65-214">0.94</span><span class="sxs-lookup"><span data-stu-id="b4f65-214">0.94</span></span>          | <span data-ttu-id="b4f65-215">265,95 USD</span><span class="sxs-lookup"><span data-stu-id="b4f65-215">265.95 USD</span></span>     |
| <span data-ttu-id="b4f65-216">Izdevumi</span><span class="sxs-lookup"><span data-stu-id="b4f65-216">Expense</span></span>           | <span data-ttu-id="b4f65-217">Rēķinā neiekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="b4f65-217">Unbilled sales</span></span>   | <span data-ttu-id="b4f65-218">17. jūn.</span><span class="sxs-lookup"><span data-stu-id="b4f65-218">17-Jun</span></span> | <span data-ttu-id="b4f65-219">Konrāds</span><span class="sxs-lookup"><span data-stu-id="b4f65-219">Prakash</span></span>  | <span data-ttu-id="b4f65-220">Automašīnu noma</span><span class="sxs-lookup"><span data-stu-id="b4f65-220">Car Rental</span></span>           | <span data-ttu-id="b4f65-221">1 EA</span><span class="sxs-lookup"><span data-stu-id="b4f65-221">1 ea</span></span>     | <span data-ttu-id="b4f65-222">150 EUR</span><span class="sxs-lookup"><span data-stu-id="b4f65-222">150 EUR</span></span>      | <span data-ttu-id="b4f65-223">150 EUR</span><span class="sxs-lookup"><span data-stu-id="b4f65-223">150 EUR</span></span>     | <span data-ttu-id="b4f65-224">0.94</span><span class="sxs-lookup"><span data-stu-id="b4f65-224">0.94</span></span>          | <span data-ttu-id="b4f65-225">159,57 USD</span><span class="sxs-lookup"><span data-stu-id="b4f65-225">159.57 USD</span></span>     |

<span data-ttu-id="b4f65-226">Lai projektā aprēķinātu kopējo rēķinā neiekļauto pārdošanas darījumu vērtību, varat izveidot apkopojuma lauku, kas paredzēts laukam **Summas** visiem saistītajiem rēķinā neiekļautās pārdošanas faktiskajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="b4f65-226">To calculate the total unbilled sales value on the project, you can create a roll-up field for the **Amount** field on all the related unbilled sales actuals.</span></span> <span data-ttu-id="b4f65-227">Apkopojuma lauks ir Dynamics 365 konstrukcija, kas ļauj izpildīt ātrās formulas saistītajiem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="b4f65-227">The roll-up field is a construct of Dynamics 365 that allows for quick formulas on related records.</span></span>