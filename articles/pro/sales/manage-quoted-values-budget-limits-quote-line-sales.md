---
title: Projekta piedāvājuma rindas (Pro)
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu rindu izmantošanu projektu darbam. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080374"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="71c1a-104">Projekta piedāvājuma rindas (Pro)</span><span class="sxs-lookup"><span data-stu-id="71c1a-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="71c1a-105">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="71c1a-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="71c1a-106">Projekta piedāvājumu rindas ir paredzētas, lai palīdzētu aprēķināt projekta darbu iesaistē.</span><span class="sxs-lookup"><span data-stu-id="71c1a-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="71c1a-107">Projekta piedāvājuma rindas struktūra ir paplašināta projekta aprēķiniem ar tālāk uzskaitītajiem jēdzieniem.</span><span class="sxs-lookup"><span data-stu-id="71c1a-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="71c1a-108">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="71c1a-108">Billing Method</span></span>
- <span data-ttu-id="71c1a-109">Projektu un uzdevumu kartēšana</span><span class="sxs-lookup"><span data-stu-id="71c1a-109">Project and Task Mapping</span></span>
- <span data-ttu-id="71c1a-110">Iekļautās transakciju klases</span><span class="sxs-lookup"><span data-stu-id="71c1a-110">Included Transaction classes</span></span>
- <span data-ttu-id="71c1a-111">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="71c1a-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="71c1a-112">Iekasēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="71c1a-112">Chargeability setup</span></span>
- <span data-ttu-id="71c1a-113">Aprēķins, izmantojot piedāvājuma rindas detaļas</span><span class="sxs-lookup"><span data-stu-id="71c1a-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="71c1a-114">Piedāvājuma rindas klienti</span><span class="sxs-lookup"><span data-stu-id="71c1a-114">Quote line Customers</span></span>

<span data-ttu-id="71c1a-115">Tālāk redzamajā tabulā ir sniegta informācija par projekta piedāvājuma rindas cilnes **Vispārīgi** laukiem.</span><span class="sxs-lookup"><span data-stu-id="71c1a-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="71c1a-116">Šie lauki palīdz izveidot pamatu detalizētam, vispusīgam projekta darba aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="71c1a-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="71c1a-117">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="71c1a-117">**Field**</span></span> | <span data-ttu-id="71c1a-118">**Atbilstība, mērķis un norādes**</span><span class="sxs-lookup"><span data-stu-id="71c1a-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="71c1a-119">**Lejupstraumes ietekme**</span><span class="sxs-lookup"><span data-stu-id="71c1a-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="71c1a-120">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="71c1a-120">Name</span></span> | <span data-ttu-id="71c1a-121">Piedāvājuma rindas nosaukums, kas palīdz identificēt aprēķināmā piedāvājuma diskrēto komponentu.</span><span class="sxs-lookup"><span data-stu-id="71c1a-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="71c1a-122">Pārkopēts uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71c1a-123">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="71c1a-123">Billing Method</span></span> | <span data-ttu-id="71c1a-124">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no atbilstošā lauka iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="71c1a-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="71c1a-125">Šajā laukā ir iekļauti divi galvenie līgumu slēgšanas modeļi, kurus atbalsta Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="71c1a-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="71c1a-126">- fiksēta cena;</span><span class="sxs-lookup"><span data-stu-id="71c1a-126">- Fixed price</span></span></br><span data-ttu-id="71c1a-127">- laiks un materiāli.</span><span class="sxs-lookup"><span data-stu-id="71c1a-127">- Time and material.</span></span>| <span data-ttu-id="71c1a-128">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71c1a-129">Project</span><span class="sxs-lookup"><span data-stu-id="71c1a-129">Project</span></span> | <span data-ttu-id="71c1a-130">Izmantojiet šo neobligāto lauku, lai identificētu projektu, kas tiks izmantots darba veikšanai šajā iesaistē.</span><span class="sxs-lookup"><span data-stu-id="71c1a-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="71c1a-131">Ja projekts ir kartēts uz piedāvājuma rindu, tas atvieglo apmaksājamo uzdevumu iestatīšanu, kā arī projekta aprēķina ievietošanu piedāvājuma rindā kā piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="71c1a-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="71c1a-132">Ja projekts netiek kartēts uz projekta piedāvājuma rindu, aprēķins ir jāizveido manuāli, izveidojot katru piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="71c1a-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="71c1a-133">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="71c1a-134">Iekļautie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="71c1a-134">Included Tasks</span></span> | <span data-ttu-id="71c1a-135">Norāda, vai šī piedāvājuma rinda tiek izmantota visiem atlasītā projekta uzdevumiem vai dažiem no tiem.</span><span class="sxs-lookup"><span data-stu-id="71c1a-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="71c1a-136">Šim laukam ir šādas iespējamās vērtības:</span><span class="sxs-lookup"><span data-stu-id="71c1a-136">This field has the following possible values:</span></span></br><span data-ttu-id="71c1a-137">- visi projekta uzdevumi;</span><span class="sxs-lookup"><span data-stu-id="71c1a-137">- All project tasks</span></span></br><span data-ttu-id="71c1a-138">- tikai atlasītie projekta uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="71c1a-138">- Selected project tasks only</span></span></br><span data-ttu-id="71c1a-139">Tukša vērtība šajā laukā ir līdzvērtīga opcijai **Visi projekta uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="71c1a-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="71c1a-140">Ja pēc tam projekta lapā ir atlasīts **Tikai atlasītie projekta uzdevumi** , cilnē **Uzdevumu norēķinu iestatīšana** var atlasīt specifiskus uzdevumus, kurus saistīt ar šo piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="71c1a-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="71c1a-141">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71c1a-142">Iekļaut laiku</span><span class="sxs-lookup"><span data-stu-id="71c1a-142">Include Time</span></span> | <span data-ttu-id="71c1a-143">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="71c1a-144">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="71c1a-145">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="71c1a-146">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71c1a-147">Iekļaut izdevumus</span><span class="sxs-lookup"><span data-stu-id="71c1a-147">Include Expense</span></span> | <span data-ttu-id="71c1a-148">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="71c1a-149">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="71c1a-150">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="71c1a-151">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71c1a-152">Iekļaut maksu</span><span class="sxs-lookup"><span data-stu-id="71c1a-152">Include Fee</span></span> | <span data-ttu-id="71c1a-153">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="71c1a-154">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="71c1a-155">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="71c1a-156">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71c1a-157">Minētā summa</span><span class="sxs-lookup"><span data-stu-id="71c1a-157">Quoted Amount</span></span> | <span data-ttu-id="71c1a-158">Šī ir summa, kas tiks piedāvāta klientam par visu darbu, kas prognozēts šajā projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="71c1a-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="71c1a-159">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no lauka **Klienta budžets** iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="71c1a-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="71c1a-160">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu summas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="71c1a-161">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71c1a-162">Aprēķinātais nodoklis</span><span class="sxs-lookup"><span data-stu-id="71c1a-162">Estimated Tax</span></span> | <span data-ttu-id="71c1a-163">Tas ir rediģējams lauks, kas lietotājam ļauj pievienot paredzamo nodokļu summu piedāvājuma rindai.</span><span class="sxs-lookup"><span data-stu-id="71c1a-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="71c1a-164">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu nodokļu summas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="71c1a-165">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71c1a-166">Piedāvātā summa pēc nodokļa atskaitīšanas</span><span class="sxs-lookup"><span data-stu-id="71c1a-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="71c1a-167">Šis lauks ir piedāvājuma rindas summa pēc nodokļiem un ir tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="71c1a-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="71c1a-168">Summu šajā laukā aprēķina kā *Piedāvātā summa + Nodokļi*.</span><span class="sxs-lookup"><span data-stu-id="71c1a-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="71c1a-169">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71c1a-170">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="71c1a-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="71c1a-171">Šo lauku var rediģēt, un tas ir pieejams tikai projekta piedāvājuma rindās, kurām ir norēķinu metode **Laiks un materiāli**.</span><span class="sxs-lookup"><span data-stu-id="71c1a-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="71c1a-172">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71c1a-173">Klienta budžets</span><span class="sxs-lookup"><span data-stu-id="71c1a-173">Customer Budget</span></span> | <span data-ttu-id="71c1a-174">Šis lauks ir rediģējams un tiek kopēts no atbilstošā lauka iespēju rindā, ja piedāvājums tika izveidots no iespējas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="71c1a-175">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="71c1a-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="71c1a-176">Validācijas kārtulas laukiem projekta piedāvājumu rindu cilnē Vispārīgi</span><span class="sxs-lookup"><span data-stu-id="71c1a-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="71c1a-177">**1. kārtula** : ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi** , projekts tiek iekļauts piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="71c1a-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="71c1a-178">**2. kārtula** : ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi** , projektu un noteiktu transakciju klasi var iekļaut tikai vienā projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="71c1a-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="71c1a-179">**3. kārtula** : ja lauks **Iekļautie uzdevumi** ir ir iestatīts uz **Tikai atlasītie projekta uzdevumi** , projektu un noteiktu transakciju klasi var iekļaut vairākās projekta piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="71c1a-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="71c1a-180">**4. kārtula** : ja iespējai ir vairāki piedāvājumi, var būt pieejamas piedāvājumu rindas no dažādiem piedāvājumiem, kas visi attiecas uz vienu un to pašu projektu un ietver to pašu transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="71c1a-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="71c1a-181">**5. kārtula** : ja piedāvājumi nepieder vienai un tai pašai iespējai, tie nevar ietvert to pašu projektu un transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="71c1a-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="71c1a-182">
                    <strong>Iespēja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="71c1a-183">
                    <strong>Piedāvājums</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="71c1a-184">
                    <strong>Piedāvājuma rinda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="71c1a-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="71c1a-186">
                    <strong>Iekļautie uzdevumi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="71c1a-187">
                    <strong>Iekļaut laiku</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="71c1a-188">
                    <strong>Iekļaut izdevumus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="71c1a-189">
                    <strong>Ietveršana</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="71c1a-190">
                    <strong>Maksa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="71c1a-191">
                    <strong>Derīgs/Nav derīgs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="71c1a-192">
                    <strong>Iemesls</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71c1a-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-193">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-194">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-195">QL1</span><span class="sxs-lookup"><span data-stu-id="71c1a-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-196">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-197">Tukša</span><span class="sxs-lookup"><span data-stu-id="71c1a-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-198">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-199">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-200">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-201">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="71c1a-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-202">2. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="71c1a-202">Violation of Rule #2.</span></span> <span data-ttu-id="71c1a-203">Laiks, izdevumi un maksas P1 projektā ir ietvertas piedāvājuma rindās — gan QL1, gan QL2.</span><span class="sxs-lookup"><span data-stu-id="71c1a-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-204">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-205">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-206">QL2</span><span class="sxs-lookup"><span data-stu-id="71c1a-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-207">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-208">Tukša</span><span class="sxs-lookup"><span data-stu-id="71c1a-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-209">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-210">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-211">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-212">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-213">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-214">QL1</span><span class="sxs-lookup"><span data-stu-id="71c1a-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-215">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-216">Tukša</span><span class="sxs-lookup"><span data-stu-id="71c1a-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-217">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-218">No</span><span class="sxs-lookup"><span data-stu-id="71c1a-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-219">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-220">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="71c1a-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-221">2. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="71c1a-221">Violation of Rule #2.</span></span> <span data-ttu-id="71c1a-222">Laiks un maksas P1 projektā ir ietvertas piedāvājuma rindās — gan QL1, gan QL2.</span><span class="sxs-lookup"><span data-stu-id="71c1a-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-223">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-224">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-225">QL2</span><span class="sxs-lookup"><span data-stu-id="71c1a-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-226">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-227">Tukša</span><span class="sxs-lookup"><span data-stu-id="71c1a-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-228">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-229">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-230">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-231">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-232">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-233">QL1</span><span class="sxs-lookup"><span data-stu-id="71c1a-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-234">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-235">Tukša</span><span class="sxs-lookup"><span data-stu-id="71c1a-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-236">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-237">No</span><span class="sxs-lookup"><span data-stu-id="71c1a-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-238">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-239">Derīgs</span><span class="sxs-lookup"><span data-stu-id="71c1a-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="71c1a-240">Laiks un maksas P1 projektā ir ietvertas rindā QL1.</span><span class="sxs-lookup"><span data-stu-id="71c1a-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="71c1a-241">Izdevumi P1 projektā ir ietverti rindā QL2.</span><span class="sxs-lookup"><span data-stu-id="71c1a-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="71c1a-242">Nepārklājas informācija, kas iekļauta katrā piedāvājuma rindā un ir derīga.</span><span class="sxs-lookup"><span data-stu-id="71c1a-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-243">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-244">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-245">QL2</span><span class="sxs-lookup"><span data-stu-id="71c1a-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-246">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-247">Tukša</span><span class="sxs-lookup"><span data-stu-id="71c1a-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-248">No</span><span class="sxs-lookup"><span data-stu-id="71c1a-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-249">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-250">No</span><span class="sxs-lookup"><span data-stu-id="71c1a-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-251">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-252">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-253">QL1</span><span class="sxs-lookup"><span data-stu-id="71c1a-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-254">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-255">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="71c1a-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-256">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-257">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-258">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-259">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="71c1a-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-260">Iepriekš norādītās 2. kārtulas pārkāpums</span><span class="sxs-lookup"><span data-stu-id="71c1a-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="71c1a-261">Q1 iekļauj laiku, izdevumus un maksas P1 projekta uzdevumu apakškopā.</span><span class="sxs-lookup"><span data-stu-id="71c1a-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="71c1a-262">QL2 ietver laiku, izdevumus un maksas par visu P1 projektu un pārklājas ar to, kas ir iekļauts Q1.</span><span class="sxs-lookup"><span data-stu-id="71c1a-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-263">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-264">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-265">QL2</span><span class="sxs-lookup"><span data-stu-id="71c1a-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-266">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-267">Tukša</span><span class="sxs-lookup"><span data-stu-id="71c1a-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-268">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-269">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-270">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-271">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-272">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-273">QL1</span><span class="sxs-lookup"><span data-stu-id="71c1a-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-274">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-275">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="71c1a-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-276">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-277">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-278">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-279">Derīgs</span><span class="sxs-lookup"><span data-stu-id="71c1a-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-280">Saskaņā ar iepriekš minēto 3. kārtulu,</span><span class="sxs-lookup"><span data-stu-id="71c1a-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="71c1a-281">Q1 iekļauj laiku, izdevumus un maksas P1 projekta uzdevumu apakškopā.</span><span class="sxs-lookup"><span data-stu-id="71c1a-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="71c1a-282">QL2 iekļauj laiku, izdevumus un maksas P1 projekta uzdevumu apakškopai.</span><span class="sxs-lookup"><span data-stu-id="71c1a-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="71c1a-283">Vienīgā papildu validācija ir ap QL1 uzdevumu apakškopu, kas atšķiras no QL2 uzdevumu apakškopas.</span><span class="sxs-lookup"><span data-stu-id="71c1a-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="71c1a-284">Šādi tiek nodrošināts, ka nav pārklāšanās.</span><span class="sxs-lookup"><span data-stu-id="71c1a-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="71c1a-285">To veic sistēma, kad tiek saistīti uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="71c1a-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-286">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-287">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-288">QL2</span><span class="sxs-lookup"><span data-stu-id="71c1a-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-289">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-290">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="71c1a-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-291">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-292">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-293">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-294">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-295">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-296">QL1</span><span class="sxs-lookup"><span data-stu-id="71c1a-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-297">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-298">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="71c1a-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-299">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-300">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-301">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="71c1a-302">Derīgs</span><span class="sxs-lookup"><span data-stu-id="71c1a-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-303">Pamatojoties uz 5. kārtulu, Q1 un Q2 ir divi piedāvājumi par vienu un to pašu iespēju, tāpēc tos abus var izmantot vienu un to pašu projekta komponentu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="71c1a-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-304">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-305">2. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-306">QL1</span><span class="sxs-lookup"><span data-stu-id="71c1a-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-307">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-308">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="71c1a-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-309">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-310">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-311">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-312">O1</span><span class="sxs-lookup"><span data-stu-id="71c1a-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-313">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-314">QL1</span><span class="sxs-lookup"><span data-stu-id="71c1a-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-315">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-316">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="71c1a-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-317">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-318">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-319">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="71c1a-320">Derīgs</span><span class="sxs-lookup"><span data-stu-id="71c1a-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71c1a-321">Pamatojoties uz 4. kārtulu, Q1 un Q2 ir divi piedāvājumi par dažādām iespējām, tāpēc tos nevar izmantot tā paša projekta vienu un to pašu komponentu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="71c1a-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="71c1a-322">O2</span><span class="sxs-lookup"><span data-stu-id="71c1a-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71c1a-323">1. cet.</span><span class="sxs-lookup"><span data-stu-id="71c1a-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-324">QL1</span><span class="sxs-lookup"><span data-stu-id="71c1a-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-325">P1</span><span class="sxs-lookup"><span data-stu-id="71c1a-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="71c1a-326">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="71c1a-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-327">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="71c1a-328">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="71c1a-329">Jā</span><span class="sxs-lookup"><span data-stu-id="71c1a-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="71c1a-330">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="71c1a-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

