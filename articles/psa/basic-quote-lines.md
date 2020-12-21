---
title: Piedāvājumi un piedāvājumu rindas
description: Šajā tēmā ir sniegta informācija par piedāvājumiem un piedāvājumu rindām.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 509bc089e69ec234ddfdecb789c2e446286da82b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129462"
---
# <a name="quotes-and-quote-lines"></a><span data-ttu-id="09342-103">Piedāvājumi un piedāvājumu rindas</span><span class="sxs-lookup"><span data-stu-id="09342-103">Quotes and quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="09342-104">Programmā Dynamics 365 Project Service Automation ir divu tipu piedāvājumi: projekta piedāvājumi un pārdošanas piedāvājumi.</span><span class="sxs-lookup"><span data-stu-id="09342-104">In Dynamics 365 Project Service Automation, there are two types of quotes: project quotes and sales quotes.</span></span> <span data-ttu-id="09342-105">Šie divi tipi atšķiras tālāk norādītajos divos veidos.</span><span class="sxs-lookup"><span data-stu-id="09342-105">The two types differ in the following ways:</span></span>

- <span data-ttu-id="09342-106">Pārdošanas piedāvājumā rindas elementiem ir tikai viens režģis.</span><span class="sxs-lookup"><span data-stu-id="09342-106">On a sales quote, there is only one grid for line items.</span></span> <span data-ttu-id="09342-107">Projekta piedāvājumā ir divi režģi rindas elementiem: viens ir paredzēts projekta rindām, bet otrs ir paredzēts preču rindām.</span><span class="sxs-lookup"><span data-stu-id="09342-107">On a project quote, there are two grids for line items: one for project lines and one for product lines.</span></span>
- <span data-ttu-id="09342-108">Pārdošanas piedāvājums atbalsta aktivizēšanu un pārskatījumus.</span><span class="sxs-lookup"><span data-stu-id="09342-108">A sales quote supports activation and revisions.</span></span> <span data-ttu-id="09342-109">Projekta piedāvājums neatbalsta šos procesus.</span><span class="sxs-lookup"><span data-stu-id="09342-109">A project quote doesn’t support those processes.</span></span>
- <span data-ttu-id="09342-110">Pārdošanas piedāvājumam var pievienot vairākus pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="09342-110">You can attach multiple orders to a sales quote.</span></span> <span data-ttu-id="09342-111">Projekta piedāvājumam var pievienot tikai vienu projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="09342-111">You can attach only one project contract to a project quote.</span></span>
- <span data-ttu-id="09342-112">Varat iegūt pārdošanas piedāvājumu un saglabāt saistīto iespēju atvērtu.</span><span class="sxs-lookup"><span data-stu-id="09342-112">You can win a sales quote and keep the related opportunity open.</span></span> <span data-ttu-id="09342-113">Pēc tam, kad projekta piedāvājums ir iegūts, saistītā iespēja tiek slēgta.</span><span class="sxs-lookup"><span data-stu-id="09342-113">After a project quote is won, the related opportunity is closed.</span></span>
- <span data-ttu-id="09342-114">Pārdošanas piedāvājumā nav iekļauti daži lauki un koncepcijas, kas ir iekļauti projekta piedāvājumā.</span><span class="sxs-lookup"><span data-stu-id="09342-114">A sales quote doesn't include some fields and concepts that are included on a project quote has fields.</span></span> <span data-ttu-id="09342-115">Šie lauki ir, piemēram, **Līgumslēdzēja struktūrvienība**, **Uzņēmumu pārvaldnieks** un **Rēķina saņēmēja kontaktpersonas vārds**.</span><span class="sxs-lookup"><span data-stu-id="09342-115">The fields include **Contracting Unit**, **Account Manager**, and **Bill to Contact Name**.</span></span>  
- <span data-ttu-id="09342-116">Pārdošanas piedāvājumus un projekta piedāvājumus norāda arī opciju kopas lauks ar nosaukumu **Tips**.</span><span class="sxs-lookup"><span data-stu-id="09342-116">Sales quotes and project quotes are also identified by an option set–based field that is named **Type**.</span></span> <span data-ttu-id="09342-117">Pārdošanas piedāvājumā šim laukam ir vērtība **Balstīts uz elementu**.</span><span class="sxs-lookup"><span data-stu-id="09342-117">For a sales quote, this field has the value **Item-based**.</span></span> <span data-ttu-id="09342-118">Projekta piedāvājumā tam ir vērtība **Balstīts uz darbu**.</span><span class="sxs-lookup"><span data-stu-id="09342-118">For a project quote, it has the value **Work-based**.</span></span>

<span data-ttu-id="09342-119">Šajā tēmā tiks izklāstīta detalizēta informācija par projekta piedāvājumiem.</span><span class="sxs-lookup"><span data-stu-id="09342-119">This topic will focus on the details of project quotes.</span></span>

<span data-ttu-id="09342-120">Projekta piedāvājumam programmā PSA var būt vairāki rindas elementi vai piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="09342-120">A project quote in PSA can have multiple line items or quote lines.</span></span> <span data-ttu-id="09342-121">Projekta piedāvājumā ir divi režģi rindas elementiem.</span><span class="sxs-lookup"><span data-stu-id="09342-121">In fact, a project quote has two grids for line items.</span></span> <span data-ttu-id="09342-122">Viens režģis ir paredzēts uz projektu balstītām rindām, kas nodrošina detalizētus novērtējumus.</span><span class="sxs-lookup"><span data-stu-id="09342-122">One grid is for project-based lines that allow for detailed estimations.</span></span> <span data-ttu-id="09342-123">Otrs režģis ir paredzēts uz preci balstītām rindām, kas izmanto vienkāršu vienības cenas un uz daudzumu balstītu metodi.</span><span class="sxs-lookup"><span data-stu-id="09342-123">The other grid is for product-based lines that use a simple unit price and quantity-based approach.</span></span>

- <span data-ttu-id="09342-124">**Balstīts uz projektu** — summa (piedāvātā vērtība) tiek noteikta pēc tam, kad ir novērtēts, cik daudz darba ir nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="09342-124">**Project-based** – The amount (quoted value) is determined after you estimate how much work is required.</span></span> <span data-ttu-id="09342-125">Varat novērtēt darbu augstā līmenī vai arī var novērtēt to tieši kā rindas detaļas zem katras piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="09342-125">You can estimate work at a high level, or you can estimate it directly as line details below each quote line.</span></span> <span data-ttu-id="09342-126">Visbeidzot, varat novērtēt darbu, pamatojoties uz augšupejošiem novērtējumiem, izmantojot projektu un projekta plānu.</span><span class="sxs-lookup"><span data-stu-id="09342-126">Finally, you can estimate work based on ground-up estimates, by using a project and project plan.</span></span> <span data-ttu-id="09342-127">Uz projektu balstītas piedāvājuma rindas ir atrodamas tikai uz projektu balstītos piedāvājumos, kas izveidoti, izmantojot Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="09342-127">Project-based quote lines are found only in project-based quotes that are created by using Project Service Automation.</span></span> <span data-ttu-id="09342-128">Šī tipa piedāvājuma rinda ir pielāgota programmā Microsoft Dynamics 365 Sales pieejamo ierakstāmo piedāvājuma rindu forma.</span><span class="sxs-lookup"><span data-stu-id="09342-128">This type of quote line is a customized form of the write-in quote lines that are available in Microsoft Dynamics 365 Sales.</span></span>
- <span data-ttu-id="09342-129">**Balstīts uz preci** — summa (piedāvātā vērtība) tiek noteikta, pamatojoties uz pārdoto vienību daudzumu un preces vienības pārdošanas cenu.</span><span class="sxs-lookup"><span data-stu-id="09342-129">**Product-based** – The amount (quoted value) is determined based on the quantity of units that is sold and the product's unit sales price.</span></span> <span data-ttu-id="09342-130">Prece uz preci balstītā rindā var būt iegūta no Sales preču kataloga vai arī tā var būt jūsu definētā prece.</span><span class="sxs-lookup"><span data-stu-id="09342-130">The product on a product-based line can come from a product catalog in Sales, or it can be a product that you define.</span></span> <span data-ttu-id="09342-131">Šī tipa piedāvājuma rinda ir pieejama arī uz projektu balstītos piedāvājumos, kas izveidoti, izmantojot PSA.</span><span class="sxs-lookup"><span data-stu-id="09342-131">This type of quote line is also available on project-based quotes that are created by using PSA.</span></span>

<span data-ttu-id="09342-132">Piedāvājumā ietvertā summa ir uz preci balstīto rindu un uz projektu balstīto rindu kopsumma.</span><span class="sxs-lookup"><span data-stu-id="09342-132">The amount on a quote is the total across the product-based lines and the project-based lines.</span></span>

> [!NOTE]
> <span data-ttu-id="09342-133">Piedāvājumi un piedāvājuma rindas programmā PSA nav obligātas.</span><span class="sxs-lookup"><span data-stu-id="09342-133">Quotes and quote lines aren't required in PSA.</span></span> <span data-ttu-id="09342-134">Projekta procesu var sākt ar projekta līgumu (pārdotais projekts).</span><span class="sxs-lookup"><span data-stu-id="09342-134">You can start the project process with a project contract (sold project).</span></span> <span data-ttu-id="09342-135">Tomēr vienmēr ir nepieciešama iespēja neatkarīgi no tā, vai sākat darbu ar piedāvājumu vai projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="09342-135">However, an opportunity is always required, regardless of whether you start with a quote or a project contract.</span></span>

## <a name="project-based-quote-lines"></a><span data-ttu-id="09342-136">Uz projektu balstītas piedāvājuma rindas</span><span class="sxs-lookup"><span data-stu-id="09342-136">Project-based quote lines</span></span>

<span data-ttu-id="09342-137">Uz projektu balstītai piedāvājuma rindai programmā PSA ir tālāk norādītās norēķinu metodes.</span><span class="sxs-lookup"><span data-stu-id="09342-137">A project-based quote line in PSA has the following billing methods:</span></span>

- <span data-ttu-id="09342-138">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="09342-138">Time and material</span></span>
- <span data-ttu-id="09342-139">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="09342-139">Fixed price</span></span>

### <a name="time-and-material"></a><span data-ttu-id="09342-140">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="09342-140">Time and material</span></span>

<span data-ttu-id="09342-141">Laika un materiālu norēķinu metodes pamatā ir patēriņš.</span><span class="sxs-lookup"><span data-stu-id="09342-141">The Time and material billing method is based on consumption.</span></span> <span data-ttu-id="09342-142">Kad atlasāt šo norēķinu metodi, klientam tiek izrakstīts rēķins par projekta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="09342-142">When you select this billing method, the customer is invoiced as the project incurs costs.</span></span> <span data-ttu-id="09342-143">Rēķini tiek izveidoti periodiski, pamatojoties uz datumu.</span><span class="sxs-lookup"><span data-stu-id="09342-143">Invoices are created on a date-based periodic frequency.</span></span> <span data-ttu-id="09342-144">Pārdošanas procesa laikā laika un materiālu komponenta piedāvātā vērtība klientam sniedz tikai galīgo izmaksu novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="09342-144">During the sales process, the quoted value of a time-and-material component gives only an estimate of the final cost to the customer.</span></span> <span data-ttu-id="09342-145">Kreditors neuzņemas saistības izpildīt projektu precīzi atbilstoši piedāvātajai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="09342-145">The vendor doesn't commit itself to completing the project at exactly the quoted value.</span></span> <span data-ttu-id="09342-146">Laika un materiālu komponenti palielina klienta risku.</span><span class="sxs-lookup"><span data-stu-id="09342-146">Time-and-material components increase the customer's risk.</span></span> <span data-ttu-id="09342-147">Klienti, iespējams, vēlēsies apspiest papildu klauzulas par nepārsniegšanu, lai samazinātu to risku.</span><span class="sxs-lookup"><span data-stu-id="09342-147">Customers might want to negotiate additional not-to-exceed clauses to minimize their risk.</span></span> <span data-ttu-id="09342-148">PSA neatbalsta klauzulu par nepārsniegšanu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="09342-148">PSA doesn't support setting not-to-exceed clauses.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="09342-149">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="09342-149">Fixed price</span></span>

<span data-ttu-id="09342-150">Izmantojot fiksētas cenas norēķinu metodi, kreditors apņemas nodrošināt projektu klientam par fiksētu samaksu.</span><span class="sxs-lookup"><span data-stu-id="09342-150">In the Fixed price billing method, a vendor commits itself to delivering the project at a fixed cost to the customer.</span></span> <span data-ttu-id="09342-151">Klientam tiek izrakstīts rēķins par fiksētas cenas piedāvājuma rindas piedāvāto vērtību neatkarīgi no izmaksām, kas kreditoram rodas, nodrošinot šo piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="09342-151">The customer is billed the quoted value of the fixed-price quote line, regardless of the costs that the vendor incurs to deliver that quote line.</span></span> <span data-ttu-id="09342-152">Rēķins par fiksētas cenas piedāvājuma rindas vērtību tiek izrakstīts vienā no tālāk norādītajiem veidiem.</span><span class="sxs-lookup"><span data-stu-id="09342-152">The fixed-price quote line value is billed in one of the following ways:</span></span> 

- <span data-ttu-id="09342-153">Kā vienreizējās izmaksas summa projekta sākumā vai beigās vai tad, kad ir sasniegts projekta atskaites punkts.</span><span class="sxs-lookup"><span data-stu-id="09342-153">As a lump-sum amount at the start or end of the project, or when a project milestone is reached.</span></span> 
- <span data-ttu-id="09342-154">No datuma atkarīgos intervālos, veicot vienlīdzīgus piedāvājuma rindas fiksētās vērtības maksājumus.</span><span class="sxs-lookup"><span data-stu-id="09342-154">At a date-based frequency of equal installments of the fixed value on the quote line.</span></span> <span data-ttu-id="09342-155">Šie maksājumi ir pazīstami kā periodiskie atskaites punkti.</span><span class="sxs-lookup"><span data-stu-id="09342-155">These installments are known as periodic milestones.</span></span>
- <span data-ttu-id="09342-156">Maksājumi, kam ir naudas vērtība, tiek saskaņoti ar darba norisi vai konkrētiem projektā sasniegtiem atskaites punktiem.</span><span class="sxs-lookup"><span data-stu-id="09342-156">In installments that have a monetary value that is aligned with the progress of work or specific milestones that are achieved on the project.</span></span> <span data-ttu-id="09342-157">Šajā gadījumā katra maksājuma vērtība var atšķirties, bet tiem kopā ir jāveido piedāvājuma rindas fiksētā vērtība.</span><span class="sxs-lookup"><span data-stu-id="09342-157">In this case, the value of each installment can differ, but they must all add up to the fixed value on the quote line.</span></span>

<span data-ttu-id="09342-158">PSA atbalsta visus trīs rēķinu grafiku tipus fiksētas cenas piedāvājuma rindām.</span><span class="sxs-lookup"><span data-stu-id="09342-158">PSA supports all three types of invoice schedules for fixed-price quote lines.</span></span>

## <a name="transaction-classification"></a><span data-ttu-id="09342-159">Transakciju klasifikācija</span><span class="sxs-lookup"><span data-stu-id="09342-159">Transaction classification</span></span>

<span data-ttu-id="09342-160">Profesionālo pakalpojumu organizācijas parasti sniedz piedāvājumus un izraksta rēķinus saviem klientiem, izmantojot izmaksu klasifikāciju.</span><span class="sxs-lookup"><span data-stu-id="09342-160">Professional service organizations typically quote and invoice their customers by classification of costs.</span></span> <span data-ttu-id="09342-161">Programmā PSA izmaksas tiek apzīmētas ar tālāk norādītajām transakciju klasifikācijām.</span><span class="sxs-lookup"><span data-stu-id="09342-161">In PSA, costs are represented by the following transaction classifications:</span></span>

- <span data-ttu-id="09342-162">**Laiks** — šī klasifikācija norāda darba vai cilvēkresursu laika izmaksas projektā.</span><span class="sxs-lookup"><span data-stu-id="09342-162">**Time** – This classification represents the cost of labor or human resources' time on a project.</span></span>
- <span data-ttu-id="09342-163">**Izdevumi** — šī klasifikācija norāda visus pārējos izdevumus projektā.</span><span class="sxs-lookup"><span data-stu-id="09342-163">**Expense**: – This classification represents all other kinds of expenses on a project.</span></span> <span data-ttu-id="09342-164">Tā kā izdevumus var plaši klasificēt, lielākā daļā organizāciju izveido apakškategorijas, piemēram, ceļojumi, automašīnu īre, viesnīca vai biroja preces.</span><span class="sxs-lookup"><span data-stu-id="09342-164">Because expenses can be broadly classified, most organizations create subcategories, such as travel, car rental, hotel, or office supplies.</span></span>
- <span data-ttu-id="09342-165">**Maksa** — šī klasifikācija norāda dažādas pieskaitāmās izmaksas, soda naudas un citas no klienta iekasējamās maksas.</span><span class="sxs-lookup"><span data-stu-id="09342-165">**Fee** – This classification represents miscellaneous overhead, penalties, and other items that are charged to the customer.</span></span> 
- <span data-ttu-id="09342-166">**Nodoklis** — šī klasifikācija norāda nodokļu summas, ko lietotāji pievieno, ievadot izdevumus.</span><span class="sxs-lookup"><span data-stu-id="09342-166">**Tax** – This classification represents tax amounts that users add while they enter expenses.</span></span>
- <span data-ttu-id="09342-167">**Materiālu transakcija** — šī klasifikācija norāda faktiskās vērtības no preču rindām apstiprinātā projekta rēķinā.</span><span class="sxs-lookup"><span data-stu-id="09342-167">**Material transaction** – This classification represents actuals from product lines on a confirmed project invoice.</span></span>
- <span data-ttu-id="09342-168">**Atskaites punkts** — šo klasifikāciju izmanto fiksētas cenas norēķinu loģika programmā PSA.</span><span class="sxs-lookup"><span data-stu-id="09342-168">**Milestone** – This classification is used by the fixed-price billing logic in PSA.</span></span>

<span data-ttu-id="09342-169">Vienu vai vairākas no šīm transakciju klasifikācijām var saistīt ar katru piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="09342-169">One or more of these transaction classifications can be associated with each quote line.</span></span> <span data-ttu-id="09342-170">Pēc tam, kad piedāvājums ir iegūts, kartējums starp transakciju klasifikāciju un piedāvājuma rindu tiek pārsūtīts uz līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="09342-170">After a quote is won, the mapping between transaction classification and quote line is transferred to the contract line.</span></span>
 
> ![Ekrānuzņēmums ar transakciju tipu kartēšanu uz piedāvājuma un līguma rindām](media/basic-guide-5.png)
  
<span data-ttu-id="09342-172">Piedāvājumā var būt ietvertas, piemēram, tālāk norādītās divas piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="09342-172">For example, a quote might contain the following two quote lines:</span></span> 
- <span data-ttu-id="09342-173">Konsultāciju darbs, kas izmanto laika un materiālu norēķinu metodi, kurā ir piemērojamas laika un maksu transakciju klasifikācijas.</span><span class="sxs-lookup"><span data-stu-id="09342-173">Consulting work that uses a Time and material billing method where time and fee transaction classifications are applicable.</span></span> <span data-ttu-id="09342-174">Piemēram, par visām projekta parauga **Dynamics AX ieviešana** laika un maksu transakcijām rēķins klientam tiek izrakstīts, pamatojoties uz patērēto laiku un materiāliem.</span><span class="sxs-lookup"><span data-stu-id="09342-174">For example, all time and fee transactions for the **Dynamics AX Implementation** example project are invoiced to the customer based on the time and materials that are used.</span></span> 
- <span data-ttu-id="09342-175">Saistītie ceļa izdevumi, kas izmanto fiksētu cenas norēķinu metodi.</span><span class="sxs-lookup"><span data-stu-id="09342-175">Related travel expenses that use a Fixed price billing method.</span></span> <span data-ttu-id="09342-176">Piemēram, par visiem projekta parauga **Dynamics AX ieviešana** ceļa izdevumiem rēķins tiek izrakstīts, izmantojot fiksētu naudas vērtību.</span><span class="sxs-lookup"><span data-stu-id="09342-176">For example, all travel expenses for the **Dynamics AX Implementation** example project are invoiced at a fixed monetary value.</span></span>

> [!NOTE]
> <span data-ttu-id="09342-177">Projekta un transakciju klasifikāciju **Laiks**, **Izdevumi** un **Maksa** kombinācijai, kas saistīta ar piedāvājuma rindu vai līguma rindu, ir jābūt unikālai.</span><span class="sxs-lookup"><span data-stu-id="09342-177">The combination of the project and transaction classifications of **Time**, **Expense**, and **Fee** that are associated with a quote line or contract line must be unique.</span></span> <span data-ttu-id="09342-178">Ja viena un tā pati projekta un transakciju klases kombinācija būs saistīta ar vairāk nekā vienu līguma rindu vai piedāvājuma rindu, PSA nedarbosies pareizi.</span><span class="sxs-lookup"><span data-stu-id="09342-178">If the same combination of project and transaction class is associated with more than one contract line or quote line, PSA won't work correctly.</span></span>

## <a name="billing-types"></a><span data-ttu-id="09342-179">Norēķinu tipi</span><span class="sxs-lookup"><span data-stu-id="09342-179">Billing types</span></span>

<span data-ttu-id="09342-180">Lauks **Norēķinu tips** definē rēķinā iekļaujamības koncepciju programmā PSA.</span><span class="sxs-lookup"><span data-stu-id="09342-180">The **Billing Type** field defines the concept of chargeability in PSA.</span></span> <span data-ttu-id="09342-181">Tas ir opciju kopa ar tālāk norādītajām iespējamajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="09342-181">It's an option set that has the following possible values:</span></span>

- <span data-ttu-id="09342-182">**Rēķinā iekļaujams** — izmaksas, kas tiek uzkrātas, izmantojot šo lomu/kategoriju, ir tiešās izmaksas, kas virza projekta izpildi, un klientam ir jāmaksā par šo darbu.</span><span class="sxs-lookup"><span data-stu-id="09342-182">**Chargeable** – The cost that is accrued by this role/category is a direct cost that drives project execution, and the customer will pay for this work.</span></span> <span data-ttu-id="09342-183">Maksājumu var administrēt kā laika un materiālu vai fiksētas cenas apmaksu.</span><span class="sxs-lookup"><span data-stu-id="09342-183">The payment can be administered as a time-and-material or fixed-price arrangement.</span></span> <span data-ttu-id="09342-184">Tomēr darbinieks, kas veltīs šo laiku, saņems atbilstošo kredītu par savu apmaksājamo izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="09342-184">However, the employee who spends this time will receive the corresponding credit for his or her billable utilization.</span></span>
- <span data-ttu-id="09342-185">**Rēķinā iekļaujams** — izmaksas, kas tiek uzkrātas, izmantojot šo lomu/kategoriju, ir tiešās izmaksas, kas virza projekta izpildi, lai gan klients šo faktu neatzīst un nevēlas maksāt par šo darbu.</span><span class="sxs-lookup"><span data-stu-id="09342-185">**Non-chargeable** – The cost that is accrued by this role/category is considered a direct cost that drives project execution, even though the customer doesn't recognize this fact and won't pay for this work.</span></span> <span data-ttu-id="09342-186">Darbinieks, kas veltīs šo laiku, nesaņems atbilstošo kredītu par savu apmaksājamo izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="09342-186">The employee who spends this time won't be credited with billable utilization for it.</span></span>
- <span data-ttu-id="09342-187">**Bezmaksas** — izmaksas, kas tiek uzkrātas, izmantojot šo lomu/kategoriju, ir tiešās izmaksas, kas virza projekta izpildi, un klients atzīst šo faktu.</span><span class="sxs-lookup"><span data-stu-id="09342-187">**Complimentary** – The cost that is accrued by this role/category is considered a direct cost that drives project execution, and the customer recognizes this fact.</span></span> <span data-ttu-id="09342-188">Darbinieks, kas veltīs šo laiku, saņems kredītu par savu apmaksājamo izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="09342-188">The employee who spends this time will be credited for billable utilization for it.</span></span> <span data-ttu-id="09342-189">Taču šīs izmaksas netiks iekasētas no klienta.</span><span class="sxs-lookup"><span data-stu-id="09342-189">However, this cost isn't charged to the customer.</span></span>
- <span data-ttu-id="09342-190">**Nav pieejams** — izmaksas, kas rodas iekšējos projektos un kam nav nepieciešama ieņēmumu izsekošana, tiek izsekotas, izmantojot šo opciju.</span><span class="sxs-lookup"><span data-stu-id="09342-190">**Not available** – The costs that are incurred on internal projects that don't require revenue tracking are tracked by using this option.</span></span>

## <a name="invoice-schedule"></a><span data-ttu-id="09342-191">Rēķina izrakstīšanas grafiks</span><span class="sxs-lookup"><span data-stu-id="09342-191">Invoice schedule</span></span>

<span data-ttu-id="09342-192">Rēķina izrakstīšanas grafiks ir datumu sērija, kas attiecas uz rēķinu izrakstīšanu projektā.</span><span class="sxs-lookup"><span data-stu-id="09342-192">An invoice schedule is a series of dates when invoicing for a project occurs.</span></span> <span data-ttu-id="09342-193">Pēc izvēles varat izveidot rēķina izrakstīšanas grafiku piedāvājuma rindā programmā PSA.</span><span class="sxs-lookup"><span data-stu-id="09342-193">You can optionally create an invoice schedule on a quote line in PSA.</span></span> <span data-ttu-id="09342-194">Katrai piedāvājuma rindai var būt savs rēķina izrakstīšanas grafiks.</span><span class="sxs-lookup"><span data-stu-id="09342-194">Each quote line can have its own invoice schedule.</span></span> <span data-ttu-id="09342-195">Lai izveidotu rēķina izrakstīšanas grafiku, ir jānorāda tālāk norādītās atribūtu vērtības.</span><span class="sxs-lookup"><span data-stu-id="09342-195">To create an invoice schedule, you must provide the following attribute values:</span></span>

- <span data-ttu-id="09342-196">Rēķina perioda sākuma datums</span><span class="sxs-lookup"><span data-stu-id="09342-196">A billing start date</span></span> 
- <span data-ttu-id="09342-197">Piegādes datums, kas norāda rēķina perioda beigu datumu projektā</span><span class="sxs-lookup"><span data-stu-id="09342-197">A delivery date that represents the billing end date on the project</span></span>
- <span data-ttu-id="09342-198">Rēķinu izrakstīšanas biežums</span><span class="sxs-lookup"><span data-stu-id="09342-198">An invoice frequency</span></span>

<span data-ttu-id="09342-199">PSA izmanto šīs trīs atribūtu vērtības, lai ģenerētu varbūtēju datumu kopu, kam izveidot rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="09342-199">PSA uses these three attribute values to generate a tentative set of dates to establish invoicing on.</span></span>

## <a name="invoice-frequency"></a><span data-ttu-id="09342-200">Rēķinu izrakstīšanas biežums</span><span class="sxs-lookup"><span data-stu-id="09342-200">Invoice frequency</span></span>

<span data-ttu-id="09342-201">Rēķinu izrakstīšanas biežums ir entītija, kas glabā atribūtu vērtības, kuras palīdz izteikt rēķinu izveides biežumu.</span><span class="sxs-lookup"><span data-stu-id="09342-201">Invoice frequency is an entity that stores attribute values that help express the frequency of invoice creation.</span></span> <span data-ttu-id="09342-202">Tālāk norādītie atribūti izsaka vai definē rēķinu izrakstīšanas biežuma entītiju.</span><span class="sxs-lookup"><span data-stu-id="09342-202">The following attributes express or define the Invoice frequency entity:</span></span>

- <span data-ttu-id="09342-203">**Periods** — tiek atbalstīti mēneša, divu nedēļu un nedēļas periodi.</span><span class="sxs-lookup"><span data-stu-id="09342-203">**Period** - Monthly, biweekly, and weekly periods are supported.</span></span> 
- <span data-ttu-id="09342-204">**Izpildes katrā periodā** — nedēļas un divu nedēļas periodiem var definēt tikai vienu izpildi katrā periodā.</span><span class="sxs-lookup"><span data-stu-id="09342-204">**Runs per period** - For weekly and biweekly periods, you can define only one run per period.</span></span> <span data-ttu-id="09342-205">Mēneša periodiem var definēt no vienas līdz četrām izpildēm katrā periodā.</span><span class="sxs-lookup"><span data-stu-id="09342-205">For monthly periods, you can define between one and four runs per period.</span></span> 
- <span data-ttu-id="09342-206">**Izpildes dienas** — dienas, kurās jāveic rēķinu izrakstīšana.</span><span class="sxs-lookup"><span data-stu-id="09342-206">**Days of run** – The days when invoicing should be run.</span></span> <span data-ttu-id="09342-207">Šo atribūtu var konfigurēt divos veidos.</span><span class="sxs-lookup"><span data-stu-id="09342-207">You can configure this attribute in two ways:</span></span>
  - <span data-ttu-id="09342-208">**Darbadienas** — varat, piemēram, norādīt, ka rēķini tiek izrakstīti katru pirmdienu vai katru otro pirmdienu.</span><span class="sxs-lookup"><span data-stu-id="09342-208">**Weekdays** - For example, you can specify that invoicing is run every Monday or every second Monday.</span></span> <span data-ttu-id="09342-209">Klienti, kuriem jāiestata rēķinu izrakstīšana darbadienā, var dod priekšroku šāda veida konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="09342-209">Customers who must set invoicing to run on a working day might prefer this kind of configuration..</span></span> 
  - <span data-ttu-id="09342-210">**Kalendārās dienas** — varat, piemēram, norādīt, ka rēķini tiek izrakstīti katra mēneša septītajā un divdesmit pirmajā dienā.</span><span class="sxs-lookup"><span data-stu-id="09342-210">**Calendar days** - For example, you can specify that invoicing is run on the seventh and twenty-first days of every month.</span></span> <span data-ttu-id="09342-211">Dažas organizācijas var izvēlēties šāda veida konfigurāciju, jo tā palīdz garantēt, ka rēķini tiek izrakstīti, izmantojot fiksētu grafiku katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="09342-211">Some organizations might prefer this kind of configuration, because it helps guarantee that invoicing in run on a fixed schedule every month.</span></span>
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a><span data-ttu-id="09342-212">Fiksētas cenas piedāvājuma rindas rēķina izrakstīšanas grafiks</span><span class="sxs-lookup"><span data-stu-id="09342-212">Invoice schedule for a fixed-price quote line</span></span>

<span data-ttu-id="09342-213">Fiksētas cenas piedāvājuma rindai varat izmantot režģi **Rēķina izrakstīšanas grafiks**, lai izveidotu rēķina izrakstīšanas atskaites punktus, kas ir līdzvērtīgi piedāvājuma rindas vērtībai.</span><span class="sxs-lookup"><span data-stu-id="09342-213">For a fixed-price quote line, you can use the **Invoice Schedule** grid to create billing milestones that equal the value of the quote line.</span></span>

- <span data-ttu-id="09342-214">Lai izveidotu rēķina izrakstīšanas atskaites punktus, kas ir vienādi sadalīti, atlasiet rēķinu izrakstīšanas biežumu, piedāvājuma rindā ievadiet rēķina perioda sākuma datumu un atlasiet piedāvājumam opciju **Pieprasītais pabeigšanas datums** piedāvājuma virsraksta sadaļā **Kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="09342-214">To create billing milestones that are equally divided, select an invoice frequency, enter the billing start date on the quote line, and select **Requested Completion Date** for the quote in the **Summary** section of the quote header.</span></span> <span data-ttu-id="09342-215">Pēc tam atlasiet opciju **Izveidot periodiskus atskaites punktus**, lai izveidotu vienādi sadalītus atskaites punktus, pamatojoties uz atlasīto rēķinu izrakstīšanas biežumu.</span><span class="sxs-lookup"><span data-stu-id="09342-215">Then select **Generate Periodic Milestones** to create equally split milestones based on the selected invoice frequency.</span></span> 
- <span data-ttu-id="09342-216">Lai izveidotu vienreizējās izmaksas rēķina izrakstīšanas atskaites punktu, izveidojiet atskaites punktu un pēc tam ievadiet piedāvājuma rindas vērtību kā atskaites punkta summu.</span><span class="sxs-lookup"><span data-stu-id="09342-216">To create a lump-sum billing milestone, create a milestone, and then enter the quote line value as the milestone amount.</span></span>
- <span data-ttu-id="09342-217">Lai izveidotu rēķinu izrakstīšanas atskaites punktus, kuru pamatā ir noteikti uzdevumi projekta plānā, izveidojiet atskaites punktu un kartējiet to uz projekta grafika elementu rēķina izrakstīšanas atskaites punkta UI.</span><span class="sxs-lookup"><span data-stu-id="09342-217">To create billing milestones that are based on specific tasks in the project plan, create a milestone, and map it to the project's schedule element in the billing milestone UI.</span></span>