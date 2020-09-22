---
title: Projektu līgumi
description: Šajā tēmā ir sniegti projektu līgumu piemēri, ko var izveidot dažādu veidu projektiem un finansējuma avotiem, kā arī to, kā pārvaldīt līgumus un izrakstīt rēķinus projektu klientiem.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753516"
---
# <a name="project-contracts"></a><span data-ttu-id="55a2e-103">Projektu līgumi</span><span class="sxs-lookup"><span data-stu-id="55a2e-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55a2e-104">Šajā rakstā ir sniegti projektu līgumu piemēri, ko var izveidot dažādu veidu projektiem un finansējuma avotiem, kā arī to, kā pārvaldīt līgumus un izrakstīt rēķinus projektu klientiem.</span><span class="sxs-lookup"><span data-stu-id="55a2e-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="55a2e-105">Projekta līgumam izveidotā projekta tips nosaka metodi, kas tiek izmantota, lai izrakstītu rēķinus projekta klientiem.</span><span class="sxs-lookup"><span data-stu-id="55a2e-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="55a2e-106">Var mainīt projekta līgumu un saistīto projektu, bet nevar mainīt projekta tipu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="55a2e-107">Izmantojot projekta līgumu, vienlaicīgi var izrakstīt rēķinu par vienu vai vairākiem projektiem.</span><span class="sxs-lookup"><span data-stu-id="55a2e-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="55a2e-108">Projekta līgums arī palīdz garantēt konsekventu rēķinu izrakstīšanas procedūru katram apakšprojektam projekta struktūrā.</span><span class="sxs-lookup"><span data-stu-id="55a2e-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="55a2e-109">Katram projektam, kam tiks izrakstīts rēķins, jābūt saistītam ar projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="55a2e-110">Projekta līguma iestatījumi attiecas uz visiem projektiem un apakšprojektiem, kas ir saistīti ar šo projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="55a2e-111">Projekta līgumā var norādīt vienu vai vairākus finansējuma avotus.</span><span class="sxs-lookup"><span data-stu-id="55a2e-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="55a2e-112">Tāpēc varat sadalīt rēķinu starp vairākiem finansētājiem, iestatīt finansējuma ierobežojumus, lai finansējuma avoti netiktu izrakstīti lielāki par noteiktu summu, un konfigurēt finansēšanas kārtulas izdevumu segšanai.</span><span class="sxs-lookup"><span data-stu-id="55a2e-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="55a2e-113">Projekta līgumu finansēšana</span><span class="sxs-lookup"><span data-stu-id="55a2e-113">Funding for project contracts</span></span>
<span data-ttu-id="55a2e-114">Dažos projekta līgumos ir norādīts, ka vairākas puses kopīgi atbild par projekta izmaksu finansēšanu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="55a2e-115">Lūk, daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="55a2e-115">Here are some examples:</span></span>

-   <span data-ttu-id="55a2e-116">Liels klients, kam ir vairākas nodaļas, pieprasa, lai projekta finansējums tiktu sadalīts pēc nodaļas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="55a2e-117">Jūsu uzņēmums koplieto liela projekta izmaksas ar ārēju organizāciju.</span><span class="sxs-lookup"><span data-stu-id="55a2e-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="55a2e-118">Ceļu projektu kopīgi finansē divas pašvaldības.</span><span class="sxs-lookup"><span data-stu-id="55a2e-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="55a2e-119">Tilta projektu finansē valsts dotācija un privāta korporācija.</span><span class="sxs-lookup"><span data-stu-id="55a2e-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="55a2e-120">Programmā Dynamics 365 Finance varat sadalīt rēķinu par vienu transakciju vai veselu projektu, izmantojot vairākus klientus, dotācijas vai organizācijas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="55a2e-121">Projektos, kuriem ir vairāki finansētāji, visas puses, kas sniedz ieguldījumu avansā finansēta projekta finansēšanā, sauc par finansējuma avotiem.</span><span class="sxs-lookup"><span data-stu-id="55a2e-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="55a2e-122">Pēc tam, kad klients, organizācija vai dotācija ir definēta kā finansējuma avots, to var piešķirt vienai vai vairākām finansēšanas kārtulām.</span><span class="sxs-lookup"><span data-stu-id="55a2e-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="55a2e-123">Finansēšanas kārtulas satur kritērijus, kas nosaka, kā maksas tiek piešķirtas dažādiem projekta finansējuma avotiem.</span><span class="sxs-lookup"><span data-stu-id="55a2e-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="55a2e-124">Tā kā uzkrātās preces, piemēram, tās, kas tiek iekļautas pirkuma pieprasījumos un pirkuma pasūtījumos, nevar sadalīt, izmaksu summu dalīšanas laikā nevar sadalīt vairāku finansējuma avotu starpā.</span><span class="sxs-lookup"><span data-stu-id="55a2e-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="55a2e-125">Tāpēc finansējuma avota vērtība joprojām ir 0 (nulle), līdz tiek iegrāmatota krājumu izejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="55a2e-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="55a2e-126">Kad krājuma izejas plūsma ir iegrāmatota, izmaksu summa tiek sadalīta atbilstoši projekta sadalījuma kārtulām.</span><span class="sxs-lookup"><span data-stu-id="55a2e-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="55a2e-127">Tālāk ir norādītas dažas darbības, ko varat veikt, lai atvieglotu rēķinu sadalīšanu starp vairākiem finansējuma avotiem:</span><span class="sxs-lookup"><span data-stu-id="55a2e-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="55a2e-128">Norādiet, ka visas projektā ievadītās darbības izmanto tādu pašu pārdošanas valūtu, kāda ir projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="55a2e-129">Iestatiet finansējuma ierobežojumus, lai finansējuma avotam netiktu izrakstīts rēķins, kas nav lielāks par noteiktu projekta summu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="55a2e-130">Konfigurējiet finansējuma kārtulas un finansējuma ierobežojumus katram darba ņēmējam, precei, kategorijai, kategoriju grupai un transakciju veidam (vai visiem transakciju veidiem).</span><span class="sxs-lookup"><span data-stu-id="55a2e-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="55a2e-131">Atlasiet neobligātu sākumu un beigu datumu, lai definētu periodu, kurā ir derīga katra finansējuma kārtula.</span><span class="sxs-lookup"><span data-stu-id="55a2e-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="55a2e-132">Norādiet procentus, par kuriem atbild katrs finansējuma avots.</span><span class="sxs-lookup"><span data-stu-id="55a2e-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="55a2e-133">Norādiet finansējuma avotu, kas ir atbildīgs par starpību noapaļošanu, kuras izraisa finansējuma piešķiršanas aprēķini.</span><span class="sxs-lookup"><span data-stu-id="55a2e-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="55a2e-134">Iestatiet kārtulas, kas nosaka, kā ārējiem klientiem tiek izrakstīti rēķini par projekta izmaksām un kā tās tiek iekasētas no iekšējām organizācijām.</span><span class="sxs-lookup"><span data-stu-id="55a2e-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="55a2e-135">Ierakstiet transakcijas aizturētā finansējuma kontā, līdz var iegūt papildu finansējumu, vai līdz izlemjat šīs izmaksas segt iekšēji.</span><span class="sxs-lookup"><span data-stu-id="55a2e-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="55a2e-136">Lai noteiktu, kuru nodokļu grupu saistīt ar transakciju, projekts tiek meklēts nodokļu grupas piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="55a2e-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="55a2e-137">Ja projekta līmenī nav veikts nodokļu grupas piešķīrums, tiek meklēts projekta līgums.</span><span class="sxs-lookup"><span data-stu-id="55a2e-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="55a2e-138">Piemērs: Vairāki finansējuma avoti (vienkārši)</span><span class="sxs-lookup"><span data-stu-id="55a2e-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="55a2e-139">Tālāk sniegtajā tabulā ir sniegti scenāriji, kā pārvaldīt finansējuma sadali starp vairākiem finansējuma avotiem.</span><span class="sxs-lookup"><span data-stu-id="55a2e-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="55a2e-140">Šie scenāriji ir balstīti šādos pieņēmumos:</span><span class="sxs-lookup"><span data-stu-id="55a2e-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="55a2e-141">Prioritārie iestatījumi tiek iedalīti līdzekļu piešķiršanā, pirms tiek piemēroti citi finansējuma kārtulas kritēriji.</span><span class="sxs-lookup"><span data-stu-id="55a2e-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="55a2e-142">Nav norādīts datumu diapazons, lai definētu periodu d, kurā ir derīga finansējuma kārtula.</span><span class="sxs-lookup"><span data-stu-id="55a2e-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55a2e-143"><strong>Scenārijs</strong></span><span class="sxs-lookup"><span data-stu-id="55a2e-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="55a2e-144"><strong>Finansējuma avots</strong></span><span class="sxs-lookup"><span data-stu-id="55a2e-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="55a2e-145"><strong>Piešķīruma procenti</strong></span><span class="sxs-lookup"><span data-stu-id="55a2e-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="55a2e-146"><strong>Piešķīruma prioritāte</strong></span><span class="sxs-lookup"><span data-stu-id="55a2e-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a2e-147">Jūs vēlaties piešķirt izmaksas vienam finansējuma avotam, kamēr nav iztērēti tā līdzekļi, piešķirt izmaksas otram finansējuma avotam, kamēr tā līdzekļi nav izsmelti, un visbeidzot piešķirt atlikušās izmaksas trešajam finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="55a2e-148">Finansējuma　avots　1</span><span class="sxs-lookup"><span data-stu-id="55a2e-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="55a2e-149">Finansējuma　avots　2</span><span class="sxs-lookup"><span data-stu-id="55a2e-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="55a2e-150">Finansējuma　avots　3</span><span class="sxs-lookup"><span data-stu-id="55a2e-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55a2e-151">100%</span><span class="sxs-lookup"><span data-stu-id="55a2e-151">100%</span></span></li>
<li><span data-ttu-id="55a2e-152">100%</span><span class="sxs-lookup"><span data-stu-id="55a2e-152">100%</span></span></li>
<li><span data-ttu-id="55a2e-153">100%</span><span class="sxs-lookup"><span data-stu-id="55a2e-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55a2e-154">1</span><span class="sxs-lookup"><span data-stu-id="55a2e-154">1</span></span></li>
<li><span data-ttu-id="55a2e-155">2</span><span class="sxs-lookup"><span data-stu-id="55a2e-155">2</span></span></li>
<li><span data-ttu-id="55a2e-156">3</span><span class="sxs-lookup"><span data-stu-id="55a2e-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a2e-157">Jūs vēlaties piešķirt 75 procentus no izmaksām vienam finansējuma avotam un 25% otram finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="55a2e-158">Ja kāds no šiem finansējuma avotiem ir izsmelts, jūs vēlaties samaksāt atlikušās izmaksas no trešā finansējuma avota.</span><span class="sxs-lookup"><span data-stu-id="55a2e-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="55a2e-159">Finansējuma　avots　1</span><span class="sxs-lookup"><span data-stu-id="55a2e-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="55a2e-160">Finansējuma　avots　2</span><span class="sxs-lookup"><span data-stu-id="55a2e-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="55a2e-161">Finansējuma　avots　3</span><span class="sxs-lookup"><span data-stu-id="55a2e-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55a2e-162">75%</span><span class="sxs-lookup"><span data-stu-id="55a2e-162">75%</span></span></li>
<li><span data-ttu-id="55a2e-163">25%</span><span class="sxs-lookup"><span data-stu-id="55a2e-163">25%</span></span></li>
<li><span data-ttu-id="55a2e-164">100%</span><span class="sxs-lookup"><span data-stu-id="55a2e-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55a2e-165">1</span><span class="sxs-lookup"><span data-stu-id="55a2e-165">1</span></span></li>
<li><span data-ttu-id="55a2e-166">1</span><span class="sxs-lookup"><span data-stu-id="55a2e-166">1</span></span></li>
<li><span data-ttu-id="55a2e-167">2</span><span class="sxs-lookup"><span data-stu-id="55a2e-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a2e-168">Jūs vēlaties piešķirt 75 procentus no izmaksām vienam finansējuma avotam un 25% otram finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="55a2e-169">Ja kāds no šiem finansējuma avotiem ir izsmelts, jūs vēlaties sadalīt atlikušās izmaksas starp trešo finansējuma avotu un ceturto finansējuma avotu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="55a2e-170">Finansējuma　avots　1</span><span class="sxs-lookup"><span data-stu-id="55a2e-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="55a2e-171">Finansējuma　avots　2</span><span class="sxs-lookup"><span data-stu-id="55a2e-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="55a2e-172">Finansējuma　avots　3</span><span class="sxs-lookup"><span data-stu-id="55a2e-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="55a2e-173">Finansējuma　avots　4</span><span class="sxs-lookup"><span data-stu-id="55a2e-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55a2e-174">75%</span><span class="sxs-lookup"><span data-stu-id="55a2e-174">75%</span></span></li>
<li><span data-ttu-id="55a2e-175">25%</span><span class="sxs-lookup"><span data-stu-id="55a2e-175">25%</span></span></li>
<li><span data-ttu-id="55a2e-176">50%</span><span class="sxs-lookup"><span data-stu-id="55a2e-176">50%</span></span></li>
<li><span data-ttu-id="55a2e-177">50%</span><span class="sxs-lookup"><span data-stu-id="55a2e-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55a2e-178">1</span><span class="sxs-lookup"><span data-stu-id="55a2e-178">1</span></span></li>
<li><span data-ttu-id="55a2e-179">1</span><span class="sxs-lookup"><span data-stu-id="55a2e-179">1</span></span></li>
<li><span data-ttu-id="55a2e-180">2</span><span class="sxs-lookup"><span data-stu-id="55a2e-180">2</span></span></li>
<li><span data-ttu-id="55a2e-181">2</span><span class="sxs-lookup"><span data-stu-id="55a2e-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a2e-182">Jūs vēlaties piešķirt pirmos 25 procentus no izmaksām vienam finansējuma avotam un pārējo — otram finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="55a2e-183">Finansējuma　avots　1</span><span class="sxs-lookup"><span data-stu-id="55a2e-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="55a2e-184">Finansējuma　avots　2</span><span class="sxs-lookup"><span data-stu-id="55a2e-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55a2e-185">25%</span><span class="sxs-lookup"><span data-stu-id="55a2e-185">25%</span></span></li>
<li><span data-ttu-id="55a2e-186">100%</span><span class="sxs-lookup"><span data-stu-id="55a2e-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55a2e-187">1</span><span class="sxs-lookup"><span data-stu-id="55a2e-187">1</span></span></li>
<li><span data-ttu-id="55a2e-188">2</span><span class="sxs-lookup"><span data-stu-id="55a2e-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="55a2e-189">Piemērs: Vairāki finansējuma avoti (sarežģīti)</span><span class="sxs-lookup"><span data-stu-id="55a2e-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="55a2e-190">Jums ir trīs finansējuma avoti, kurus vēlaties izmantot šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="55a2e-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="55a2e-191">Izmantot finansējuma avotu 2 un finansējuma avotu 3 vienlīdzīgi, līdz ir izsmelts finansējuma avots 2.</span><span class="sxs-lookup"><span data-stu-id="55a2e-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="55a2e-192">Turpināt izmantot finansējuma avotu 3, līdz tas ir izsmelts.</span><span class="sxs-lookup"><span data-stu-id="55a2e-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="55a2e-193">Pēc tam, kad ir izsmelts finansējuma avots 3, lietot finansējuma avotu 1.</span><span class="sxs-lookup"><span data-stu-id="55a2e-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="55a2e-194">Lai sasniegtu šo mērķi, jums ir jārīkojas šādi:</span><span class="sxs-lookup"><span data-stu-id="55a2e-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="55a2e-195">Iestatiet finansējuma avota 2 un finansējuma avota 3 finansējuma ierobežojumus uz to atbilstošajām summām.</span><span class="sxs-lookup"><span data-stu-id="55a2e-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="55a2e-196">Izveidojiet šādas finansējuma kārtulas:</span><span class="sxs-lookup"><span data-stu-id="55a2e-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="55a2e-197">1. kārtula (1. prioritāte): piešķirt 50 procentus transakciju finansējuma avotam 2 un 50 procentus finansējuma avotam 3.</span><span class="sxs-lookup"><span data-stu-id="55a2e-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="55a2e-198">2. kārtula (2. prioritāte): piešķirt 100 procentus transakciju finansējuma avotam 3.</span><span class="sxs-lookup"><span data-stu-id="55a2e-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="55a2e-199">3. kārtula (3. prioritāte): piešķirt 100 procentus transakciju finansējuma avotam 1.</span><span class="sxs-lookup"><span data-stu-id="55a2e-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="55a2e-200">Šāds iestatījums darbojas, jo transakcijas tiek pārbaudītas iepretim kārtulām un ierobežojumiem, lai noteiktu, vai kāds no tiem ir piemērojams transakcijai.</span><span class="sxs-lookup"><span data-stu-id="55a2e-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="55a2e-201">Ja transakcijai nav piemērojamas konkrētas kārtulas vai ierobežojumi, ir spēkā Visu transakciju kārtula.</span><span class="sxs-lookup"><span data-stu-id="55a2e-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="55a2e-202">Visu transakciju kārtula atbilst visām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="55a2e-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="55a2e-203">Ja tiek atrasta kārtula, kura atbilst transakcijai, vispirms tiek piemērota šai kārtulai piešķirtie procenti, taču vienīgi pēc tam, kad atbilstības tiek pārbaudītas attiecībā pret jebkādiem iestatītiem ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="55a2e-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="55a2e-204">Ja ir sasniegts ierobežojums un ir izsmelti finansējuma avota līdzekļi, ar finansējuma ierobežojumu saistītā finansējuma kārtula netiek ņemta vērā un programma pārbauda nākamo spēkā esošo kārtulu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="55a2e-205">Dažos gadījumos saskaņā ar kārtulu var piešķirt tikai daļu no transakcijas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="55a2e-206">Tas var notikt tādēļ, ka, piešķirot transakciju, ir sasniegts ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="55a2e-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="55a2e-207">Šādā gadījumā atbilstoši šai kārtulai tiek piešķirta tikai konkrēta summa, piemēram, 50% katram finansējuma avotam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="55a2e-208">Šāda situācija ir 1. kārtulā, kura aprakstīta iepriekš šajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="55a2e-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="55a2e-209">Atlikums tiek sadalīts atbilstoši secības nākamajām kārtulām.</span><span class="sxs-lookup"><span data-stu-id="55a2e-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="55a2e-210">Tālāk sniegtajā tabulā šis scenārijs ir apskatīts sīkāk.</span><span class="sxs-lookup"><span data-stu-id="55a2e-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55a2e-211"><strong>Fokuss</strong></span><span class="sxs-lookup"><span data-stu-id="55a2e-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="55a2e-212"><strong>Detalizēta informācija</strong></span><span class="sxs-lookup"><span data-stu-id="55a2e-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a2e-213">Finansēšanas kārtulas</span><span class="sxs-lookup"><span data-stu-id="55a2e-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="55a2e-214">1. kārtula (1. prioritāte): visas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="55a2e-215">Piešķirt finansējuma avotu 2 pie 50% un finansējuma avotu 3 pie 50%.</span><span class="sxs-lookup"><span data-stu-id="55a2e-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="55a2e-216">2. kārtula (2. prioritāte): visas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="55a2e-217">Piešķirt finansējuma avotu 3 pie 100%.</span><span class="sxs-lookup"><span data-stu-id="55a2e-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="55a2e-218">3. kārtula (2. prioritāte): visas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="55a2e-219">Piešķirt finansējuma avotu 1 pie 100%.</span><span class="sxs-lookup"><span data-stu-id="55a2e-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a2e-220">Finansējuma ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="55a2e-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="55a2e-221">Finansējuma avota 1 ierobežojums = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="55a2e-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="55a2e-222">Finansējuma avota 2 ierobežojums = 500,00</span><span class="sxs-lookup"><span data-stu-id="55a2e-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="55a2e-223">Finansējuma avota 3 ierobežojums = 750,00</span><span class="sxs-lookup"><span data-stu-id="55a2e-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a2e-224">Transakcija 1</span><span class="sxs-lookup"><span data-stu-id="55a2e-224">Transaction 1</span></span></td>
<td><span data-ttu-id="55a2e-225"><strong>Transakcijas summa:</strong> 100,00<strong>Finansējums: </strong> Transakcija tiek izmaksāta atbilstoši vienīgi 1. kārtulai, jo transakcija tiek pilnībā izmaksāta pēc 1. kārtulas piemērošanas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="55a2e-226">Transakciju finansē vienlīdzīgi starp finansēšanas avotu 2 un finansēšanas avotu 3.</span><span class="sxs-lookup"><span data-stu-id="55a2e-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="55a2e-227">Finansējuma avots 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="55a2e-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="55a2e-228">Finansējuma avots 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="55a2e-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a2e-229">Transakcija 2</span><span class="sxs-lookup"><span data-stu-id="55a2e-229">Transaction 2</span></span></td>
<td><span data-ttu-id="55a2e-230"><strong>Transakcijas summa:</strong> 5 000,00<strong>Finansējums:</strong> Transakcija tiek izmaksāta atbilstoši visām trim kārtulām.</span><span class="sxs-lookup"><span data-stu-id="55a2e-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="55a2e-231"><strong>1. kārtula</strong>
</span><span class="sxs-lookup"><span data-stu-id="55a2e-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="55a2e-232">Finansējuma avots 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="55a2e-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="55a2e-233">Finansējuma avots 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="55a2e-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="55a2e-234">
<strong>2. kārtula</strong>
</span><span class="sxs-lookup"><span data-stu-id="55a2e-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="55a2e-235">Finansējuma avots 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="55a2e-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="55a2e-236">
<strong>3. kārtula</strong>
</span><span class="sxs-lookup"><span data-stu-id="55a2e-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="55a2e-237">Finansējuma avots 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="55a2e-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a2e-238">Katram finansējuma avotam sadalītie kopējie līdzekļi</span><span class="sxs-lookup"><span data-stu-id="55a2e-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="55a2e-239">Finansējuma avots 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="55a2e-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="55a2e-240">Finansējuma avots 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="55a2e-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="55a2e-241">Finansējuma avots 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="55a2e-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="55a2e-242">Norēķinu kārtulas</span><span class="sxs-lookup"><span data-stu-id="55a2e-242">Billing rules</span></span>
<span data-ttu-id="55a2e-243">Ar klientu vienojoties par projekta līgumu, jūs definējat, kā un kad izrakstīsit klientam rēķinu par projektā ieguldīto darbu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="55a2e-244">Pēc projekta līguma un projekta iestatīšanas varat projektam iestatīt norēķinu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="55a2e-245">Norēķinu kārtulas balstās projekta nosacījumos, kuri tiek konkretizēti projekta līgumā.</span><span class="sxs-lookup"><span data-stu-id="55a2e-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="55a2e-246">Norēķinu kārtulas, kuras varat izveidot, ir atkarīgas no projekta līguma nosacījumiem un projekta veida, piemēram, laika un materiāla vai fiksētas maksas, kuru saistāt ar norēķinu kārtulu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="55a2e-247">Projekta līgumam var izveidot vairāk nekā vienu norēķinu kārtulu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="55a2e-248">Varat arī piešķirt norēķinu kārtulu vairākiem projektiem, kas ir saistīti ar to pašu projekta līgumu un kuriem ir līdzīgi norēķinu nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="55a2e-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="55a2e-249">Varat iestatīt šādus norēķinu kārtulu veidus:</span><span class="sxs-lookup"><span data-stu-id="55a2e-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="55a2e-250">**Piegādes vienība** — Izrakstiet klientam rēķinu pēc tam, kad izpildāt piegādes vienību.</span><span class="sxs-lookup"><span data-stu-id="55a2e-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="55a2e-251">Piegādes vienības tiek definētas līgumā.</span><span class="sxs-lookup"><span data-stu-id="55a2e-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="55a2e-252">**Norise** — Izrakstiet klientam rēķinu, kad pabeidzat noteiktu projekta daļu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="55a2e-253">Varat iestatīt norēķinu kārtulu, lai tiktu aprēķināts izpildītā darba īpatsvars, vai varat manuāli aprēķināt izpildītā darba īpatsvaru un summu, par kuru klientam izrakstīt rēķinu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="55a2e-254">**Atskaites punkts** — Izrakstiet klientam rēķinu par pilno projekta atskaites punkta summu, kad šis atskaites punkts ir sasniegts.</span><span class="sxs-lookup"><span data-stu-id="55a2e-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="55a2e-255">**Maksa** — Izrakstiet klientam rēķinu par saviem pakalpojumiem, plus pārvaldības maksu, kas parasti ir procents no pakalpojumu izmaksām.</span><span class="sxs-lookup"><span data-stu-id="55a2e-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="55a2e-256">**Laiks un materiāls** — Izrakstiet klientam rēķinu par projektam izlietotā laika un materiālu vērtību.</span><span class="sxs-lookup"><span data-stu-id="55a2e-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="55a2e-257">Visiem norēķinu kārtulu veidiem varat norādīt ieturējumu procentus, kas tiek atskaitīti no klienta rēķiniem, līdz projekts sasniedz noteiktu posmu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="55a2e-258">Maksājuma ieturējumu procenti ir norādīti projekta līgumā.</span><span class="sxs-lookup"><span data-stu-id="55a2e-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="55a2e-259">Summu aprēķina, pamatojoties uz un atņemot no klienta rēķina rindu kopējās vērtības.</span><span class="sxs-lookup"><span data-stu-id="55a2e-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="55a2e-260">Norēķinu kārtulām **Laiks un materiāls** un **Progress** varat piešķirt maksas kategorijas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="55a2e-261">Maksas kategorijas norāda uz transakcijām, kuras vajadzētu iekļaut klientu rēķinos.</span><span class="sxs-lookup"><span data-stu-id="55a2e-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="55a2e-262">Kad esat gatavi klientam izrakstīt rēķinu, šī projekta rēķina summa tiek aprēķināta, balstoties norēķinu kārtulās un tiek ģenerēts projekta rēķina piedāvājums.</span><span class="sxs-lookup"><span data-stu-id="55a2e-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="55a2e-263">Šajās sadaļās ir sniegti piemēri, kas parāda, kā iestatīt un pārvaldīt projekta norēķinu kārtulas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="55a2e-264">Piemērs: Izveidojiet norēķinu kārtulu, kas ir balstīta piegādāto vienību skaitā</span><span class="sxs-lookup"><span data-stu-id="55a2e-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="55a2e-265">Jūsu organizācija noslēdz līgumu, lai klienta darbiniekiem nodrošinātu kopumā piecus apmācību kursus, kas izmaksā 10 000 par vienu kursu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="55a2e-266">Pēc katra kursa jūs klientam izrakstāt rēķinu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="55a2e-267">Iestatot līguma norēķinu kārtulas, jūs izmantojat šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="55a2e-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="55a2e-268">Piegādes vienība ir viens mācību kurss.</span><span class="sxs-lookup"><span data-stu-id="55a2e-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="55a2e-269">Vienības cena ir 10 000 par vienu mācību kursu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="55a2e-270">Kopējais vienību skaits ir pieci mācību kursi.</span><span class="sxs-lookup"><span data-stu-id="55a2e-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="55a2e-271">Kad ir izpildīts viens mācību kurss, varat izveidot rēķinu par 10 000 — par pirmo piegādāto vienību — un rēķinu nosūtīt klientam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="55a2e-272">Piemērs: Izveidojiet norēķinu kārtulu, kura balstās konkrētos projekta izpildes procentos (manuāls aprēķins)</span><span class="sxs-lookup"><span data-stu-id="55a2e-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="55a2e-273">Jūsu organizācija — programmatūras konsultāciju uzņēmums — noslēdz ar klientu līgumu, lai izstrādātu daļu no klienta izstrādāta produkta.</span><span class="sxs-lookup"><span data-stu-id="55a2e-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="55a2e-274">Jūsu organizācija piekrīt programmatūras kodu piegādāt sešu mēnešu laikā.</span><span class="sxs-lookup"><span data-stu-id="55a2e-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="55a2e-275">Klients piekrīt par darbu jūsu organizācijai izmaksāt kopumā 100 000.</span><span class="sxs-lookup"><span data-stu-id="55a2e-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="55a2e-276">Jūs izveidojat norēķinu kārtulu, lai klientam izrakstītu rēķinu, pamatojoties uz projektā izpildītā darba procentiem, kā norādīts līgumā.</span><span class="sxs-lookup"><span data-stu-id="55a2e-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="55a2e-277">Pirmā mēneša beigās jūs tiekaties ar klientu, lai noteiktu, kāda daļa darba ir izpildīta.</span><span class="sxs-lookup"><span data-stu-id="55a2e-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="55a2e-278">Pēc tam, kad jūs un klients izskata projektu, jūs izlemjat, ka ir izpildīti 15 procenti darba.</span><span class="sxs-lookup"><span data-stu-id="55a2e-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="55a2e-279">Jūs izrakstāt rēķinu par 15 000 (15 procenti no 100 000) un to nosūtāt klientam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="55a2e-280">Piemērs: Izveidojiet norēķinu kārtulu, kura balstās konkrētos projekta izpildes procentos (automātisks aprēķins)</span><span class="sxs-lookup"><span data-stu-id="55a2e-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="55a2e-281">Jūsu organizācija — programmatūras izstrādes uzņēmums — piekrīt klientam izstrādāt izmaksas uzskaites pakotni par 30 000.</span><span class="sxs-lookup"><span data-stu-id="55a2e-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="55a2e-282">Klients piekrīt maksāt jūsu organizācijai, pamatojoties uz izpildītā darba daļu procentos.</span><span class="sxs-lookup"><span data-stu-id="55a2e-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="55a2e-283">Saskaņā ar jūsu aplēsēm projekta izmaksas ir 20 000.</span><span class="sxs-lookup"><span data-stu-id="55a2e-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="55a2e-284">Projekta līgumā ir norādītas tās darba kategorijas, kuras izmantojat norēķinu procesā.</span><span class="sxs-lookup"><span data-stu-id="55a2e-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="55a2e-285">Jūs iestatāt norēķinu kārtulas, kuras automātiski aprēķina rēķina summas par katrai kategorijai izpildīto darba daļu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="55a2e-286">Jūs iestatāt budžetu katrai kategorijai:</span><span class="sxs-lookup"><span data-stu-id="55a2e-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="55a2e-287">**Izstrāde** – izmaksas ir 15 000 un ieņēmumi 20 000</span><span class="sxs-lookup"><span data-stu-id="55a2e-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="55a2e-288">**Instalēšana** – izmaksas ir 5 000 un ieņēmumi 10 000</span><span class="sxs-lookup"><span data-stu-id="55a2e-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="55a2e-289">Klientam izrakstot rēķinu pirmoreiz, rēķina summa tiek aprēķināta automātiski, pamatojoties uz šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="55a2e-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="55a2e-290">Pēc mēneša projekta darbinieks iesniedz projekta laika uzskaites tabulu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="55a2e-291">Darbinieka laika izmaksas ir 5000 par izstrādi un 1000 par instalēšanu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="55a2e-292">No izstrādes darba ir pabeigti 33 procenti (5000 faktiskās izmaksas / 15 000 budžeta izmaksas), bet no instalēšanas darba ir izpildīti 20 procenti (1000 faktiskās izmaksas / 5000 budžeta izmaksas).</span><span class="sxs-lookup"><span data-stu-id="55a2e-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="55a2e-293">Automātiski tiek aprēķināta rēķina summa 8667 apmērā (33 procenti no 20 000 + 20 procenti no 10 000).</span><span class="sxs-lookup"><span data-stu-id="55a2e-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="55a2e-294">Jūs izrakstāt rēķinu par 8667 un to nosūtāt klientam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="55a2e-295">Piemērs: Izveidojiet norēķinu kārtulu, kas ir balstīta noteiktos atskaites punktos</span><span class="sxs-lookup"><span data-stu-id="55a2e-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="55a2e-296">Jūsu organizācija — pārvaldības konsultāciju uzņēmums — piekrīt veikt tirgus izpēti klienta produktam, kuru klients plāno tirgot.</span><span class="sxs-lookup"><span data-stu-id="55a2e-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="55a2e-297">Klients piekrīt izmantot jūsu pakalpojumus uz trim mēnešiem — sākot ar martu — un piekrīt jūsu organizācijai samaksāt 50 000.</span><span class="sxs-lookup"><span data-stu-id="55a2e-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="55a2e-298">Projektam ir trīs atskaites punkti:</span><span class="sxs-lookup"><span data-stu-id="55a2e-298">The project has three milestones:</span></span>

-   <span data-ttu-id="55a2e-299">1. atskaites punkts: Patērētāju datu ievākšana — 31. marts.</span><span class="sxs-lookup"><span data-stu-id="55a2e-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="55a2e-300">2. atskaites punkts: Patērētāju datu analīze — 30. aprīlis</span><span class="sxs-lookup"><span data-stu-id="55a2e-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="55a2e-301">3. atskaites punkts: Produkta ilgtspējas priekšlikuma prezentācija — 31. maijs</span><span class="sxs-lookup"><span data-stu-id="55a2e-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="55a2e-302">Klients piekrīt samaksāt jūsu organizācijai 10 000 par pirmo atskaites punktu, 20 000 par otro atskaites punktu un 20 000 par trešo atskaites punktu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="55a2e-303">Izveidojot projekta līgumu, jūs piekrītat izrakstīt klientam rēķinu atbilstoši izpildītajam atskaites punktam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="55a2e-304">Norēķinu kārtula ietver šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="55a2e-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="55a2e-305">Projekta atskaites punktu definēšana.</span><span class="sxs-lookup"><span data-stu-id="55a2e-305">Define the project milestones.</span></span>
-   <span data-ttu-id="55a2e-306">Klienta rēķinā izrakstāmās summas definēšana, kad ir izpildīts katrs atskaites punkts.</span><span class="sxs-lookup"><span data-stu-id="55a2e-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="55a2e-307">Kad 31. martā ir izpildīts pirmais atskaites punkts, jūs atzīmējat šo atskaites punktu kā izpildītu un pēc tam izrakstāt rēķinu par 10 000, un to nosūtat klientam.</span><span class="sxs-lookup"><span data-stu-id="55a2e-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="55a2e-308">Atskaites punktam nav iespējams izrakstīt rēķinu, iekams nav atzīmēta atskaites punkta izpilde.</span><span class="sxs-lookup"><span data-stu-id="55a2e-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="55a2e-309">Piemērs: Izveidojiet norēķinu kārtulu, kas ir balstīta pakalpojumos un pārvaldības maksā</span><span class="sxs-lookup"><span data-stu-id="55a2e-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="55a2e-310">Jūsu organizācija — pārvaldības konsultāciju uzņēmums — piekrīt veikt tirgus izpēti, lai novērtētu ilgtspēju produktam, kuru izstrādā jūsu klients — mazumtirdzniecības uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="55a2e-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="55a2e-311">Līguma noteikumos norādīts, ka jūs sniegsit savu trīs labāko pārvaldības konsultantu pakalpojumus, kuri veiks izpēti, pamatojoties uz laiku un materiāliem.</span><span class="sxs-lookup"><span data-stu-id="55a2e-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="55a2e-312">Klients piekrīt maksāt 100 par stundu un 10 procentu pārvaldības maksu par projektam aprēķinātajām konsultāciju stundām.</span><span class="sxs-lookup"><span data-stu-id="55a2e-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="55a2e-313">Iestatot projekta līgumu, izveidojiet norēķinu kārtulu, lai projektam aprēķinātajām konsultāciju stundām pieskaitītu 10 procentu pārvaldības maksu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="55a2e-314">Klientam izrakstot rēķinu, no klienta tiek iekasēta 10 procentu pārvaldības maksa un konsultāciju laika izmaksas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="55a2e-315">Piemēram, ja trīs konsultanti projektā kopumā nostrādāja 200 stundu, tiek izrakstīts rēķins par 22 000, pamatojoties uz šādiem aprēķiniem:</span><span class="sxs-lookup"><span data-stu-id="55a2e-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="55a2e-316">200 stundas ar likmi 100 par stundu = 20 000</span><span class="sxs-lookup"><span data-stu-id="55a2e-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="55a2e-317">10 procentu pārvaldības maksa = 2000</span><span class="sxs-lookup"><span data-stu-id="55a2e-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="55a2e-318">Kopējā rēķina summa = 22 000</span><span class="sxs-lookup"><span data-stu-id="55a2e-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="55a2e-319">Ja klientam maksas ir apliekamas ar nodokli un jūs projekta līgumā atlasāt pārdošanas nodokļu grupu, pārdošanas nodokļu grupa automātiski tiek ievadīta maksu norēķinu kārtulā.</span><span class="sxs-lookup"><span data-stu-id="55a2e-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="55a2e-320">Piemērs: Izveidojiet norēķinu kārtulu laika un materiālu vērtībai</span><span class="sxs-lookup"><span data-stu-id="55a2e-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="55a2e-321">Jūsu organizācija — programmatūras konsultāciju uzņēmums — piekrīt nodrošināt piecus tehniskos konsultantus, kas nākamos sešus mēnešus klientam strādās ar programmatūras izstrādes projektu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="55a2e-322">Klients piekrīt maksāt 150 par katru konsultāciju stundu plus biroja preču izmaksas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="55a2e-323">Katra mēneša beigās jūsu organizācija klientam nosūta rēķinu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="55a2e-324">Iestatot projekta līgumu, jūs piekrītat katru mēnesi izrakstīt klientam rēķinu par projekta laiku un materiāliem.</span><span class="sxs-lookup"><span data-stu-id="55a2e-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="55a2e-325">Jūs izveidojat norēķinu kārtulu, kas ietver šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="55a2e-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="55a2e-326">Līguma periods ir seši mēneši.</span><span class="sxs-lookup"><span data-stu-id="55a2e-326">The contract period is six months.</span></span>
-   <span data-ttu-id="55a2e-327">Konsultāciju laiks tiek aprēķināts ar likmi 150 par stundu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="55a2e-328">Biroja preces tiek izrakstītas pie izmaksām, bet projekta kopējās izmaksas nedrīkst pārsniegt 10 000.</span><span class="sxs-lookup"><span data-stu-id="55a2e-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="55a2e-329">Projekta laikā jūs katra kalendārā mēneša beigās izveidojat klienta rēķinu.</span><span class="sxs-lookup"><span data-stu-id="55a2e-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="55a2e-330">Pirmajā mēnesī projekta konsultanti fiksē kopumā 800 darba stundas.</span><span class="sxs-lookup"><span data-stu-id="55a2e-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="55a2e-331">Projektā aprēķināto biroja preču izmaksas ir 2000.</span><span class="sxs-lookup"><span data-stu-id="55a2e-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="55a2e-332">Tāpēc mēneša beigās tiek izrakstīts rēķins par 122 000, kas tiek aprēķināts kā 800 stundas ar likmi 150 par stundu, plus 2000 par biroja precēm.</span><span class="sxs-lookup"><span data-stu-id="55a2e-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



