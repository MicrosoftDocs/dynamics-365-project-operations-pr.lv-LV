---
title: Projekta līguma iestatījumi — Lite
description: Šajā tēmā ir informācija par laukiem, kas ietekmē līguma rindas, un informācija par līgumu, kas tiek apkopota visiem rindas vienumiem.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28dfb256eb75ca9484161f053969c205fcd60965
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180923"
---
# <a name="project-contract-settings---lite"></a><span data-ttu-id="ec354-103">Projekta līguma iestatījumi — Lite</span><span class="sxs-lookup"><span data-stu-id="ec354-103">Project contract settings - lite</span></span>

<span data-ttu-id="ec354-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="ec354-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ec354-105">Šī tēma sniedz informāciju par laukiem, kas attiecas uz visu projekta līgumu, ieskaitot iestatījumus, kas ietekmē visas līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="ec354-105">This topic provides information about fields that apply to the entire project contract including settings that impact all contract lines.</span></span> <span data-ttu-id="ec354-106">Ir iekļauta arī informācija par līgumu, kas ir apkopota visos projekta līguma apakšpunktos, lai vadītu KPI.</span><span class="sxs-lookup"><span data-stu-id="ec354-106">Information about the contract that is summarized across all the line items to drive KPIs of the project contract is also included.</span></span>

<span data-ttu-id="ec354-107">Tālāk sniegtajā tabulā ir uzskaitīti projekta līguma lauki, kas ir unikāli Dynamics 365 projektu darbībām vai kuriem ir dažas svarīgas izmaiņas, veicot pārdošanas pasūtījumus programmā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="ec354-107">The following table lists the fields on a project contract that are unique to Dynamics 365 Project Operations or have some important changes in behavior from sales orders in Dynamics 365 Sales.</span></span>

| <span data-ttu-id="ec354-108">Lauks</span><span class="sxs-lookup"><span data-stu-id="ec354-108">Field</span></span> | <span data-ttu-id="ec354-109">Atrašanās vieta</span><span class="sxs-lookup"><span data-stu-id="ec354-109">Location</span></span> | <span data-ttu-id="ec354-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="ec354-110">Description</span></span> | <span data-ttu-id="ec354-111">Lejupstraumes ietekme</span><span class="sxs-lookup"><span data-stu-id="ec354-111">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="ec354-112">Veidi</span><span class="sxs-lookup"><span data-stu-id="ec354-112">Type</span></span> | <span data-ttu-id="ec354-113">**Kopsavilkuma** cilne (paslēpta)</span><span class="sxs-lookup"><span data-stu-id="ec354-113">**Summary** tab (hidden)</span></span> | <span data-ttu-id="ec354-114">Šis ir opciju kopas lauks ar šādām opcijām:</span><span class="sxs-lookup"><span data-stu-id="ec354-114">This is an option set field with the following options:</span></span></br><span data-ttu-id="ec354-115">- **Balstīts uz darbu** (pieejama tikai tad, ja ir instalēts Project Operations)</span><span class="sxs-lookup"><span data-stu-id="ec354-115">- **Work-based** (Available only when Project Operations is installed)</span></span></br><span data-ttu-id="ec354-116">- **Balstīts uz vienumu** (pieejama tikai tad, ja ir instalēts Project Operations un Sales)</span><span class="sxs-lookup"><span data-stu-id="ec354-116">- **Item-based** (Available only when Project Operations and Sales are installed)</span></span></br><span data-ttu-id="ec354-117">- **Balstīts uz pakalpojuma uzturēšanu** (pieejama, ja ir instalēts Dynamics 365 Field Service)</span><span class="sxs-lookup"><span data-stu-id="ec354-117">- **Service Maintenance-based** (Available when Dynamics 365 Field Service is installed)</span></span> | <span data-ttu-id="ec354-118">Projekta operācijās šī lauka vērtība noklusējumā ir **Balstīts uz darbu**, un līgums tiek klasificēts kā projekta līgums.</span><span class="sxs-lookup"><span data-stu-id="ec354-118">In Project Operations, the value of this field defaults to **Work-based** and classifies the contract as a project-based contract.</span></span> <span data-ttu-id="ec354-119">Līgumam ir jābūt uz projektu balstītam, lai iespējotu visus projektam specifiskos paplašinājumus un funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="ec354-119">A contract should be project-based to enable all project-specific extensions and functionality.</span></span> |
| <span data-ttu-id="ec354-120">Potenciāls klients</span><span class="sxs-lookup"><span data-stu-id="ec354-120">Potential Customer</span></span> | <span data-ttu-id="ec354-121">Cilne **Kopsavilkums**</span><span class="sxs-lookup"><span data-stu-id="ec354-121">**Summary** tab</span></span> | <span data-ttu-id="ec354-122">Atsauce uz klienta uzņēmuma vai konta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ec354-122">The reference to the customers company or account record.</span></span> <span data-ttu-id="ec354-123">Veidojot līgumu no piedāvājuma, šis lauks tiek kopēts no piedāvājuma ieraksta atbilstošā lauka.</span><span class="sxs-lookup"><span data-stu-id="ec354-123">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> | <span data-ttu-id="ec354-124">Projekta līguma noklusējuma valūta, pamatojoties uz klienta valūtu.</span><span class="sxs-lookup"><span data-stu-id="ec354-124">The currency on the project contract defaults based on the currency of the customer.</span></span> <span data-ttu-id="ec354-125">To var mainīt, pirms līgums ir saglabāts.</span><span class="sxs-lookup"><span data-stu-id="ec354-125">This can be changed before the contract is saved.</span></span> |
| <span data-ttu-id="ec354-126">Konta pārvaldnieks</span><span class="sxs-lookup"><span data-stu-id="ec354-126">Account Manager</span></span> | <span data-ttu-id="ec354-127">Cilne **Kopsavilkums**</span><span class="sxs-lookup"><span data-stu-id="ec354-127">**Summary** tab</span></span> | <span data-ttu-id="ec354-128">Šī darījuma konta pārvaldnieka vārds.</span><span class="sxs-lookup"><span data-stu-id="ec354-128">The name of the Account Manager for this deal.</span></span> <span data-ttu-id="ec354-129">Veidojot līgumu no piedāvājuma, šis lauks tiek kopēts no piedāvājuma ieraksta atbilstošā lauka.</span><span class="sxs-lookup"><span data-stu-id="ec354-129">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> | <span data-ttu-id="ec354-130">Konta pārvaldnieks ir atbildīgs par attiecību ar klientu pārvaldīšanu līdz projekta pabeigšanai.</span><span class="sxs-lookup"><span data-stu-id="ec354-130">The Account Manager is responsible for managing the relationship with the customer through the completion of the project.</span></span> <span data-ttu-id="ec354-131">Pamatojoties uz grāmatojamo resursu ierakstu, kas saistīts ar konta pārvaldnieku, līguma vienība neizpilda projekta līguma saistības.</span><span class="sxs-lookup"><span data-stu-id="ec354-131">Based on the bookable resource record tied to the Account Manager, the contracting unit defaults on the project contract.</span></span> |
| <span data-ttu-id="ec354-132">Līgumslēdzēja vienība</span><span class="sxs-lookup"><span data-stu-id="ec354-132">Contracting Unit</span></span> | <span data-ttu-id="ec354-133">Cilne **Kopsavilkums**</span><span class="sxs-lookup"><span data-stu-id="ec354-133">**Summary** tab</span></span> | <span data-ttu-id="ec354-134">Organizācijas vienība, kas atbild par ar šo līgumu saistīto projektu nodrošināšanu.</span><span class="sxs-lookup"><span data-stu-id="ec354-134">The organization unit responsible for the delivery of the projects associated with this contract.</span></span> <span data-ttu-id="ec354-135">Veidojot līgumu no piedāvājuma, šis lauks tiek kopēts no piedāvājuma ieraksta atbilstošā lauka.</span><span class="sxs-lookup"><span data-stu-id="ec354-135">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> | <span data-ttu-id="ec354-136">Līgumslēdzēja struktūrvienība ir tā uzņēmuma nodaļa, kas izpilda projektus.</span><span class="sxs-lookup"><span data-stu-id="ec354-136">The contracting unit is the division of the company that executes the projects.</span></span> <span data-ttu-id="ec354-137">Katrai līgumslēdzējai vienībai ir valūta, un šo valūtu lieto, lai ziņotu projekta laikā radušās prognozētās un faktiskās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="ec354-137">Every contracting unit has a currency, and this currency is used to report estimated and actual costs incurred during the project.</span></span> |
| <span data-ttu-id="ec354-138">Produktu cenrādis</span><span class="sxs-lookup"><span data-stu-id="ec354-138">Product Price List</span></span> | <span data-ttu-id="ec354-139">Cilne **Kopsavilkums**</span><span class="sxs-lookup"><span data-stu-id="ec354-139">**Summary** tab</span></span> | <span data-ttu-id="ec354-140">Šis cenrādis tiek izmantots noklusētajām cenām uz produktu balstītās līgumu rindās.</span><span class="sxs-lookup"><span data-stu-id="ec354-140">This price list is used to default prices on product-based contract lines.</span></span> <span data-ttu-id="ec354-141">Nolaižamo opciju saraksts šim laukam rāda cenrādi sarakstu, kurā cenrāža valūta atbilst līgumā norādītajai valūtai.</span><span class="sxs-lookup"><span data-stu-id="ec354-141">The list of drop-down options for this field shows a list of price lists where the price list currency matches the currency on the contract.</span></span> <span data-ttu-id="ec354-142">Veidojot līgumu no piedāvājuma, šis lauks tiek kopēts no piedāvājuma ieraksta atbilstošā lauka.</span><span class="sxs-lookup"><span data-stu-id="ec354-142">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> <span data-ttu-id="ec354-143">Projekta līgumā šis lauks ir noklusēts no konta ieraksta, bet to var mainīt.</span><span class="sxs-lookup"><span data-stu-id="ec354-143">On the project contract, this field is defaulted from the account record but can be changed.</span></span> | <span data-ttu-id="ec354-144">Šai jomai nav nekādas pakārtotas atbilstības.</span><span class="sxs-lookup"><span data-stu-id="ec354-144">There is no downstream relevance for this field.</span></span> |
| <span data-ttu-id="ec354-145">Valūta</span><span class="sxs-lookup"><span data-stu-id="ec354-145">Currency</span></span> | <span data-ttu-id="ec354-146">Cilne **Kopsavilkums**</span><span class="sxs-lookup"><span data-stu-id="ec354-146">**Summary** tab</span></span> | <span data-ttu-id="ec354-147">Valūta, kas izmantota, lai uzrādītu šī darījuma vērtību, un valūta, kurā klientam tiks izrakstīts rēķins.</span><span class="sxs-lookup"><span data-stu-id="ec354-147">The currency used to report the value of this deal and the currency in which the customer will be invoiced.</span></span> <span data-ttu-id="ec354-148">Veidojot līgumu no piedāvājuma, šis lauks tiek kopēts no piedāvājuma ieraksta atbilstošā lauka.</span><span class="sxs-lookup"><span data-stu-id="ec354-148">When a contract is created from a quote, this field is copied from the corresponding field on the quote record.</span></span> <span data-ttu-id="ec354-149">Projekta līgumā šis lauks ir noklusējums no konta ieraksta, bet to var mainīt.</span><span class="sxs-lookup"><span data-stu-id="ec354-149">On the project contract, this field defaults from the account record but can be changed.</span></span> | <span data-ttu-id="ec354-150">Pēc tam, kad līgums ir saglabāts, šis lauks vairs nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="ec354-150">After a contract is saved, this field is no longer editable.</span></span> <span data-ttu-id="ec354-151">Šo lauku izmanto, lai iestatītu produkta un projekta cenrāžus kā noklusējumu līgumā.</span><span class="sxs-lookup"><span data-stu-id="ec354-151">This field is used to default the product and project price lists on the contract.</span></span> <span data-ttu-id="ec354-152">Tiek izmantota tāda līguma valūta, kas atbilst cenrāža valūtai.</span><span class="sxs-lookup"><span data-stu-id="ec354-152">The currency on the contract is used to match the currency on the price list.</span></span> |
| <span data-ttu-id="ec354-153">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="ec354-153">Not-to-Exceed Limit</span></span> | <span data-ttu-id="ec354-154">Cilne **Kopsavilkums**</span><span class="sxs-lookup"><span data-stu-id="ec354-154">**Summary** tab</span></span> | <span data-ttu-id="ec354-155">Šis lauks norāda norunāto gala vērtības maksimālo robežvērtību, kam klients ir piekritis šī darījuma ietvaros.</span><span class="sxs-lookup"><span data-stu-id="ec354-155">This field indicates the negotiated cap on the final value that the customer has agreed to for this deal.</span></span> | <span data-ttu-id="ec354-156">Maksimālā robežvērtība tiek aplēsta izpildes laikā un ir piemērojama visiem rindu vienumiem un projektiem, kas saistīti ar šo darījumu.</span><span class="sxs-lookup"><span data-stu-id="ec354-156">The cap is evaluated during execution and is applicable across all line items and projects associated with this deal.</span></span> |
| <span data-ttu-id="ec354-157">Pieprasītais piegādes datums</span><span class="sxs-lookup"><span data-stu-id="ec354-157">Requested Delivery Date</span></span> | <span data-ttu-id="ec354-158">Cilne **Kopsavilkums**</span><span class="sxs-lookup"><span data-stu-id="ec354-158">**Summary** tab</span></span> | <span data-ttu-id="ec354-159">Veidojot līgumu no projekta piedāvājuma, šis lauks tiek kopēts no projekta piedāvājuma atbilstošā lauka.</span><span class="sxs-lookup"><span data-stu-id="ec354-159">When a contract is created from a project quote, this field is copied from the corresponding field on the project quote.</span></span> | <span data-ttu-id="ec354-160">Šis datums tiek lietots kā rēķinu ģenerēšanas grafiku beigu datums.</span><span class="sxs-lookup"><span data-stu-id="ec354-160">This date is used as the end date to generate invoice schedules.</span></span> |

<span data-ttu-id="ec354-161">Projekta līguma cilnē **Līguma veiktspēja** ir pieejami šādi KPI:</span><span class="sxs-lookup"><span data-stu-id="ec354-161">The following KPIs are available on the **Contract Performance** tab of a project contract.</span></span>

| <span data-ttu-id="ec354-162">Lauks</span><span class="sxs-lookup"><span data-stu-id="ec354-162">Field</span></span> | <span data-ttu-id="ec354-163">Atrašanās vieta</span><span class="sxs-lookup"><span data-stu-id="ec354-163">Location</span></span> | <span data-ttu-id="ec354-164">Apraksts</span><span class="sxs-lookup"><span data-stu-id="ec354-164">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ec354-165">Līguma vērtība</span><span class="sxs-lookup"><span data-stu-id="ec354-165">Contract Value</span></span> | <span data-ttu-id="ec354-166">Kopējais līgums</span><span class="sxs-lookup"><span data-stu-id="ec354-166">Overall contract</span></span> | <span data-ttu-id="ec354-167">Projekta līguma kopējā vērtība.</span><span class="sxs-lookup"><span data-stu-id="ec354-167">The total value of the Project contract.</span></span> |
| <span data-ttu-id="ec354-168">Rēķinā norādītā summa</span><span class="sxs-lookup"><span data-stu-id="ec354-168">Billed Amount</span></span> | <span data-ttu-id="ec354-169">Kopējais līgums</span><span class="sxs-lookup"><span data-stu-id="ec354-169">Overall contract</span></span> | <span data-ttu-id="ec354-170">Visu to rēķinu vērtību summa, kas ir atbilstoši šim līgumam.</span><span class="sxs-lookup"><span data-stu-id="ec354-170">The sum of the amounts on all invoices against this contract.</span></span> |
| <span data-ttu-id="ec354-171">Radušās izmaksas</span><span class="sxs-lookup"><span data-stu-id="ec354-171">Cost Incurred</span></span> | <span data-ttu-id="ec354-172">Kopējais līgums</span><span class="sxs-lookup"><span data-stu-id="ec354-172">Overall contract</span></span> | <span data-ttu-id="ec354-173">Visu to izmaksu faktisko datu summa, kas pieteiktas visos projektos, kuri ir kartēti uz līgumu.</span><span class="sxs-lookup"><span data-stu-id="ec354-173">The sum of all cost actuals logged on all projects that are mapped to the contract.</span></span> |
| <span data-ttu-id="ec354-174">Bruto peļņa</span><span class="sxs-lookup"><span data-stu-id="ec354-174">Gross Margin</span></span> | <span data-ttu-id="ec354-175">Kopējais līgums</span><span class="sxs-lookup"><span data-stu-id="ec354-175">Overall contract</span></span> | <span data-ttu-id="ec354-176">Samaksātā summa — izmaksas, kas nav saistītas ar datumu/rēķinu summu</span><span class="sxs-lookup"><span data-stu-id="ec354-176">Billed amount - Cost incurred till date / Billed amount</span></span> |
| <span data-ttu-id="ec354-177">Paredzamā peļņa</span><span class="sxs-lookup"><span data-stu-id="ec354-177">Expected Margin</span></span> | <span data-ttu-id="ec354-178">Kopējais līgums</span><span class="sxs-lookup"><span data-stu-id="ec354-178">Overall contract</span></span> | <span data-ttu-id="ec354-179">(Līguma vērtība — prognozētās izmaksas)/līguma valueEstimated izmaksas = visu paredzamo izmaksu summa, kas ir kartētas uz šo līgumu.</span><span class="sxs-lookup"><span data-stu-id="ec354-179">(Contract value - Estimated costs) / Contract valueEstimated costs = The sum of all estimated costs on all projects mapped to the contract.</span></span>|
| <span data-ttu-id="ec354-180">Līguma vērtība</span><span class="sxs-lookup"><span data-stu-id="ec354-180">Contract Value</span></span> | <span data-ttu-id="ec354-181">Projektu līnijas</span><span class="sxs-lookup"><span data-stu-id="ec354-181">Project-based lines</span></span> | <span data-ttu-id="ec354-182">Līguma rindas vērtība.</span><span class="sxs-lookup"><span data-stu-id="ec354-182">The value of the contract line.</span></span> |
| <span data-ttu-id="ec354-183">Rēķinā norādītā summa</span><span class="sxs-lookup"><span data-stu-id="ec354-183">Billed amount</span></span> | <span data-ttu-id="ec354-184">Projektu līnijas</span><span class="sxs-lookup"><span data-stu-id="ec354-184">Project-based lines</span></span> | <span data-ttu-id="ec354-185">Fiksētas cenas līguma rindai: kopsumma visiem rēķinu pārdošanas atskaites punktu faktiskaijiem datiem attiecībā pret šo līguma rindu dažādiem rēķiniem, kas izveidoti šim līgumam.</span><span class="sxs-lookup"><span data-stu-id="ec354-185">For fixed price contract line: The sum of the amounts on all billed sales milestone actuals against this contract line on various invoices created for this contract.</span></span> <span data-ttu-id="ec354-186">Laika un materiālu līguma rindai: summa no visām apmaksājamām pārdošanas izmaksām šajā līguma rindā dažādos rēķinos, kas izveidoti šim līgumam.</span><span class="sxs-lookup"><span data-stu-id="ec354-186">For time and material contract line: The sum of the amounts on all chargeable billed sales actuals against this contract line on various invoices created for this contract.</span></span> |
| <span data-ttu-id="ec354-187">Radušās izmaksas</span><span class="sxs-lookup"><span data-stu-id="ec354-187">Cost Incurred</span></span> | <span data-ttu-id="ec354-188">Projektu līnijas</span><span class="sxs-lookup"><span data-stu-id="ec354-188">Project-based lines</span></span> | <span data-ttu-id="ec354-189">Visu to izmaksu faktisko datu summa, kas pieteiktas visos projektos, kuri ir kartēti uz līgumu.</span><span class="sxs-lookup"><span data-stu-id="ec354-189">The sum of all cost actuals logged on all projects mapped to the contract line.</span></span> |
| <span data-ttu-id="ec354-190">Bruto peļņa</span><span class="sxs-lookup"><span data-stu-id="ec354-190">Gross Margin</span></span> | <span data-ttu-id="ec354-191">Projektu līnijas</span><span class="sxs-lookup"><span data-stu-id="ec354-191">Project-based lines</span></span> | <span data-ttu-id="ec354-192">(Samaksātā summa — izmaksas, kas nav saistītas ar datumu) / rēķinu summu</span><span class="sxs-lookup"><span data-stu-id="ec354-192">(Billed amount - Cost incurred till date) / Billed amount</span></span> |
| <span data-ttu-id="ec354-193">Paredzamā peļņa</span><span class="sxs-lookup"><span data-stu-id="ec354-193">Expected Margin</span></span> | <span data-ttu-id="ec354-194">Projektu līnijas</span><span class="sxs-lookup"><span data-stu-id="ec354-194">Project-based lines</span></span> | <span data-ttu-id="ec354-195">(Līguma rindas summa bāzes valūtā — līguma rindas prognozējamās izmaksas pamatvalūtā) / līguma rindu summa pamatvalūtā</span><span class="sxs-lookup"><span data-stu-id="ec354-195">(Contract line amount in base currency - Estimated costs for the contract line in base currency) / Contract line amount in base currency</span></span> |
| <span data-ttu-id="ec354-196">Radušās izmaksas</span><span class="sxs-lookup"><span data-stu-id="ec354-196">Cost Incurred</span></span> | <span data-ttu-id="ec354-197">Projekta rindas detalizētā informācija</span><span class="sxs-lookup"><span data-stu-id="ec354-197">Detail of a project-based line</span></span> | <span data-ttu-id="ec354-198">Laiks: summa, kas ierakstīta izmaksu faktiskajā attiecībā uz šo lomu projektā, kas kartēts uz līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="ec354-198">Time: The sum of the amount on time cost actuals logged for this role on the project mapped to the contract line.</span></span> <span data-ttu-id="ec354-199">Izmaksas: summa no visiem izmaksu izmaksu faktiskaijiem datiem, kas reģistrēti šai kategorijai projektā, kas kartēts uz līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="ec354-199">Expenses: The sum of the amount on all expense cost actuals logged for this category on the project mapped to the contract line.</span></span> |
| <span data-ttu-id="ec354-200">Reģistrētais daudzums</span><span class="sxs-lookup"><span data-stu-id="ec354-200">Logged Quantity</span></span> | <span data-ttu-id="ec354-201">Projekta rindas detalizētā informācija</span><span class="sxs-lookup"><span data-stu-id="ec354-201">Detail of a project-based line</span></span> | <span data-ttu-id="ec354-202">Laiks: summa, kas ierakstīta izmaksu faktiskajā attiecībā uz šo lomu projektā, kas kartēts uz līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="ec354-202">Time: The quantity on total time cost actuals for a role on the project that is mapped to this contract line.</span></span> <span data-ttu-id="ec354-203">Izmaksas: visi šīs izdevumu kategorijas daudzumi uz projekta izdevumu izmaksu aktuāļiem ir kartēti uz šo līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="ec354-203">Expenses: All quantities for this expense category on the expense cost actuals on the project are mapped to this contract line.</span></span> |
| <span data-ttu-id="ec354-204">Rēķinā norādītā summa</span><span class="sxs-lookup"><span data-stu-id="ec354-204">Billed Amount</span></span> | <span data-ttu-id="ec354-205">Projekta rindas detalizētā informācija</span><span class="sxs-lookup"><span data-stu-id="ec354-205">Detail of a project-based line</span></span> | <span data-ttu-id="ec354-206">Fiksētas cenas līguma rindai šis lauks tiek atstāts tukšs detalizācijas līmenī un ir redzams tikai līguma rindu līmenī.</span><span class="sxs-lookup"><span data-stu-id="ec354-206">For a fixed price contract line, this field is left blank on the detail level and is only shown at the contract line level.</span></span> <span data-ttu-id="ec354-207">Attiecībā uz laika un materiālu līguma rindu aprēķini tiek pabeigti detalizētās informācijas līmenī.</span><span class="sxs-lookup"><span data-stu-id="ec354-207">For a time and material contract line, calculations are completed at the details level.</span></span> <span data-ttu-id="ec354-208">Detalizētā informācija rāda summu, kas attiecas uz visām rēķina ieņēmumu rindām atbilstoši šai līguma rindai, par kuru ir jāmaksā.</span><span class="sxs-lookup"><span data-stu-id="ec354-208">The details show the sum of the amount on all the billed revenue lines against this contract line that are chargeable.</span></span> |
| <span data-ttu-id="ec354-209">Rēķinā norādītais daudzums</span><span class="sxs-lookup"><span data-stu-id="ec354-209">Billed Quantity</span></span> | <span data-ttu-id="ec354-210">Projekta rindas detalizētā informācija</span><span class="sxs-lookup"><span data-stu-id="ec354-210">Detail of a project-based line</span></span> | <span data-ttu-id="ec354-211">Fiksētas cenas līguma rindai šis lauks tiek atstāts tukšs detalizācijas līmenī un ir redzams tikai līguma rindu līmenī.</span><span class="sxs-lookup"><span data-stu-id="ec354-211">For a fixed price contract line, this field is left blank on the detail level and is only shown at the contract line level.</span></span> <span data-ttu-id="ec354-212">Laika un materiālu līguma rindai aprēķini tiek veikti detalizētas informācijas līmenī par laiku un izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="ec354-212">For a time and material contract line, calculations are completed at the details level for time and expenses.</span></span> <span data-ttu-id="ec354-213">Laiks: stundu summa visās šīs lomas rēķinā norādītajās ieņēmumu pozīcijās attiecībā pret šo līguma rindu, kas ir apmaksājama.</span><span class="sxs-lookup"><span data-stu-id="ec354-213">Time: The sum of the hours on all the billed revenue lines for this role against this contract line that are chargeable.</span></span> <span data-ttu-id="ec354-214">Izmaksas: visi šīs izdevumu kategorijas daudzumi uz projekta izdevumu izmaksu aktuāļiem ir kartēti uz šo līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="ec354-214">Expenses: All quantities for this expense category on the expense cost actuals on the project are mapped to this contract line.</span></span> |
| <span data-ttu-id="ec354-215">Līguma vērtība</span><span class="sxs-lookup"><span data-stu-id="ec354-215">Contract Value</span></span> | <span data-ttu-id="ec354-216">Produktu līnijas</span><span class="sxs-lookup"><span data-stu-id="ec354-216">Product-based lines</span></span> | <span data-ttu-id="ec354-217">Šīs uz produktu balstītās līguma rindas vērtība.</span><span class="sxs-lookup"><span data-stu-id="ec354-217">The contract line value of this product-based contract line.</span></span> |
| <span data-ttu-id="ec354-218">Rēķinā norādītā summa</span><span class="sxs-lookup"><span data-stu-id="ec354-218">Billed Amount</span></span> | <span data-ttu-id="ec354-219">Produktu līnijas</span><span class="sxs-lookup"><span data-stu-id="ec354-219">Product-based lines</span></span> | <span data-ttu-id="ec354-220">Summa visās rēķina rindās šajā uz produktu balstītajā līguma rindā dažādos rēķinos, kas izveidoti šim līgumam.</span><span class="sxs-lookup"><span data-stu-id="ec354-220">The sum of the amounts on all invoice lines against this product-based contract line on various invoices that are created for this contract.</span></span> |
| <span data-ttu-id="ec354-221">Radušās izmaksas</span><span class="sxs-lookup"><span data-stu-id="ec354-221">Cost Incurred</span></span> | <span data-ttu-id="ec354-222">Produktu līnijas</span><span class="sxs-lookup"><span data-stu-id="ec354-222">Product-based lines</span></span> | <span data-ttu-id="ec354-223">Visu uz produktu balstītajā līguma rindā reģistrēto izmaksu faktisko datu summa.</span><span class="sxs-lookup"><span data-stu-id="ec354-223">The sum of all cost actuals logged for the product-based contract line.</span></span> |
| <span data-ttu-id="ec354-224">Bruto peļņa</span><span class="sxs-lookup"><span data-stu-id="ec354-224">Gross Margin</span></span> | <span data-ttu-id="ec354-225">Projektu līnijas</span><span class="sxs-lookup"><span data-stu-id="ec354-225">Project-based lines</span></span> | <span data-ttu-id="ec354-226">Samaksātā summa — izmaksas, kas nav saistītas ar datumu/rēķinu summu</span><span class="sxs-lookup"><span data-stu-id="ec354-226">Billed amount - Cost incurred till date / Billed amount</span></span> |
| <span data-ttu-id="ec354-227">Paredzamā peļņa</span><span class="sxs-lookup"><span data-stu-id="ec354-227">Expected Margin</span></span> | <span data-ttu-id="ec354-228">Produktu līnijas</span><span class="sxs-lookup"><span data-stu-id="ec354-228">Product-based lines</span></span> | <span data-ttu-id="ec354-229">(Līguma rindas vērtība — līguma rindas prognozējamās izmaksas) / līguma rindas vērtība</span><span class="sxs-lookup"><span data-stu-id="ec354-229">(Contract line value - Estimated costs for the contract line) / Contract line value</span></span> |