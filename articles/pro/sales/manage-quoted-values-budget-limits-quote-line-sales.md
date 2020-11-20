---
title: Projekta piedāvājuma rindas pārskats — Lite
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu rindu izmantošanu projektu darbam. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181101"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="abcee-104">Projekta piedāvājuma rindas pārskats — Lite</span><span class="sxs-lookup"><span data-stu-id="abcee-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="abcee-105">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="abcee-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="abcee-106">Projekta piedāvājumu rindas ir paredzētas, lai palīdzētu aprēķināt projekta darbu iesaistē.</span><span class="sxs-lookup"><span data-stu-id="abcee-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="abcee-107">Projekta piedāvājuma rindas struktūra ir paplašināta projekta aprēķiniem ar tālāk uzskaitītajiem jēdzieniem.</span><span class="sxs-lookup"><span data-stu-id="abcee-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="abcee-108">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="abcee-108">Billing Method</span></span>
- <span data-ttu-id="abcee-109">Projektu un uzdevumu kartēšana</span><span class="sxs-lookup"><span data-stu-id="abcee-109">Project and Task Mapping</span></span>
- <span data-ttu-id="abcee-110">Iekļautās transakciju klases</span><span class="sxs-lookup"><span data-stu-id="abcee-110">Included Transaction classes</span></span>
- <span data-ttu-id="abcee-111">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="abcee-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="abcee-112">Iekasēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="abcee-112">Chargeability setup</span></span>
- <span data-ttu-id="abcee-113">Aprēķins, izmantojot piedāvājuma rindas detaļas</span><span class="sxs-lookup"><span data-stu-id="abcee-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="abcee-114">Piedāvājuma rindas klienti</span><span class="sxs-lookup"><span data-stu-id="abcee-114">Quote line Customers</span></span>

<span data-ttu-id="abcee-115">Tālāk redzamajā tabulā ir sniegta informācija par projekta piedāvājuma rindas cilnes **Vispārīgi** laukiem.</span><span class="sxs-lookup"><span data-stu-id="abcee-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="abcee-116">Šie lauki palīdz izveidot pamatu detalizētam, vispusīgam projekta darba aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="abcee-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="abcee-117">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="abcee-117">**Field**</span></span> | <span data-ttu-id="abcee-118">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="abcee-118">**Description**</span></span> | <span data-ttu-id="abcee-119">**Lejupstraumes ietekme**</span><span class="sxs-lookup"><span data-stu-id="abcee-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="abcee-120">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="abcee-120">Name</span></span> | <span data-ttu-id="abcee-121">Piedāvājuma rindas nosaukums, kas palīdz identificēt aprēķināmā piedāvājuma diskrēto komponentu.</span><span class="sxs-lookup"><span data-stu-id="abcee-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="abcee-122">Pārkopēts uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="abcee-123">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="abcee-123">Billing Method</span></span> | <span data-ttu-id="abcee-124">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no atbilstošā lauka iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="abcee-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="abcee-125">Šajā laukā ir iekļauti divi galvenie līgumu slēgšanas modeļi, kurus atbalsta Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="abcee-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="abcee-126">- fiksēta cena;</span><span class="sxs-lookup"><span data-stu-id="abcee-126">- Fixed price</span></span></br><span data-ttu-id="abcee-127">- laiks un materiāli.</span><span class="sxs-lookup"><span data-stu-id="abcee-127">- Time and material.</span></span>| <span data-ttu-id="abcee-128">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="abcee-129">Project</span><span class="sxs-lookup"><span data-stu-id="abcee-129">Project</span></span> | <span data-ttu-id="abcee-130">Izmantojiet šo neobligāto lauku, lai identificētu projektu, kas tiks izmantots darba veikšanai šajā iesaistē.</span><span class="sxs-lookup"><span data-stu-id="abcee-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="abcee-131">Ja projekts ir kartēts uz piedāvājuma rindu, tas atvieglo apmaksājamo uzdevumu iestatīšanu, kā arī projekta aprēķina ievietošanu piedāvājuma rindā kā piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="abcee-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="abcee-132">Ja projekts netiek kartēts uz projekta piedāvājuma rindu, aprēķins ir jāizveido manuāli, izveidojot katru piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="abcee-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="abcee-133">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="abcee-134">Iekļautie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="abcee-134">Included Tasks</span></span> | <span data-ttu-id="abcee-135">Norāda, vai šī piedāvājuma rinda tiek izmantota visiem atlasītā projekta uzdevumiem vai dažiem no tiem.</span><span class="sxs-lookup"><span data-stu-id="abcee-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="abcee-136">Šim laukam ir šādas iespējamās vērtības:</span><span class="sxs-lookup"><span data-stu-id="abcee-136">This field has the following possible values:</span></span></br><span data-ttu-id="abcee-137">- visi projekta uzdevumi;</span><span class="sxs-lookup"><span data-stu-id="abcee-137">- All project tasks</span></span></br><span data-ttu-id="abcee-138">- tikai atlasītie projekta uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="abcee-138">- Selected project tasks only</span></span></br><span data-ttu-id="abcee-139">Tukša vērtība šajā laukā ir līdzvērtīga opcijai **Visi projekta uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="abcee-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="abcee-140">Ja pēc tam projekta lapā ir atlasīts **Tikai atlasītie projekta uzdevumi**, cilnē **Uzdevumu norēķinu iestatīšana** var atlasīt specifiskus uzdevumus, kurus saistīt ar šo piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="abcee-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="abcee-141">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="abcee-142">Iekļaut laiku</span><span class="sxs-lookup"><span data-stu-id="abcee-142">Include Time</span></span> | <span data-ttu-id="abcee-143">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="abcee-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="abcee-144">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="abcee-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="abcee-145">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="abcee-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="abcee-146">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="abcee-147">Iekļaut izdevumus</span><span class="sxs-lookup"><span data-stu-id="abcee-147">Include Expense</span></span> | <span data-ttu-id="abcee-148">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="abcee-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="abcee-149">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="abcee-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="abcee-150">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="abcee-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="abcee-151">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="abcee-152">Iekļaut maksu</span><span class="sxs-lookup"><span data-stu-id="abcee-152">Include Fee</span></span> | <span data-ttu-id="abcee-153">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="abcee-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="abcee-154">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="abcee-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="abcee-155">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="abcee-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="abcee-156">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="abcee-157">Minētā summa</span><span class="sxs-lookup"><span data-stu-id="abcee-157">Quoted Amount</span></span> | <span data-ttu-id="abcee-158">Šī ir summa, kas tiks piedāvāta klientam par visu darbu, kas prognozēts šajā projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="abcee-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="abcee-159">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no lauka **Klienta budžets** iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="abcee-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="abcee-160">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu summas.</span><span class="sxs-lookup"><span data-stu-id="abcee-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="abcee-161">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="abcee-162">Aprēķinātais nodoklis</span><span class="sxs-lookup"><span data-stu-id="abcee-162">Estimated Tax</span></span> | <span data-ttu-id="abcee-163">Tas ir rediģējams lauks, kas lietotājam ļauj pievienot paredzamo nodokļu summu piedāvājuma rindai.</span><span class="sxs-lookup"><span data-stu-id="abcee-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="abcee-164">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu nodokļu summas.</span><span class="sxs-lookup"><span data-stu-id="abcee-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="abcee-165">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="abcee-166">Piedāvātā summa pēc nodokļa atskaitīšanas</span><span class="sxs-lookup"><span data-stu-id="abcee-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="abcee-167">Šis lauks ir piedāvājuma rindas summa pēc nodokļiem un ir tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="abcee-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="abcee-168">Summu šajā laukā aprēķina kā *Piedāvātā summa + Nodokļi*.</span><span class="sxs-lookup"><span data-stu-id="abcee-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="abcee-169">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="abcee-170">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="abcee-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="abcee-171">Šo lauku var rediģēt, un tas ir pieejams tikai projekta piedāvājuma rindās, kurām ir norēķinu metode **Laiks un materiāli**.</span><span class="sxs-lookup"><span data-stu-id="abcee-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="abcee-172">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="abcee-173">Klienta budžets</span><span class="sxs-lookup"><span data-stu-id="abcee-173">Customer Budget</span></span> | <span data-ttu-id="abcee-174">Šis lauks ir rediģējams un tiek kopēts no atbilstošā lauka iespēju rindā, ja piedāvājums tika izveidots no iespējas.</span><span class="sxs-lookup"><span data-stu-id="abcee-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="abcee-175">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="abcee-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="abcee-176">Validācijas kārtulas laukiem projekta piedāvājumu rindu cilnē Vispārīgi</span><span class="sxs-lookup"><span data-stu-id="abcee-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="abcee-177">**1. kārtula**: ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi**, projekts tiek iekļauts piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="abcee-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="abcee-178">**2. kārtula**: ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut tikai vienā projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="abcee-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="abcee-179">**3. kārtula**: ja lauks **Iekļautie uzdevumi** ir ir iestatīts uz **Tikai atlasītie projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut vairākās projekta piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="abcee-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="abcee-180">**4. kārtula**: ja iespējai ir vairāki piedāvājumi, var būt pieejamas piedāvājumu rindas no dažādiem piedāvājumiem, kas visi attiecas uz vienu un to pašu projektu un ietver to pašu transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="abcee-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="abcee-181">**5. kārtula**: ja piedāvājumi nepieder vienai un tai pašai iespējai, tie nevar ietvert to pašu projektu un transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="abcee-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="abcee-182">
                    <strong>Iespēja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="abcee-183">
                    <strong>Piedāvājums</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="abcee-184">
                    <strong>Piedāvājuma rinda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="abcee-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="abcee-186">
                    <strong>Iekļautie uzdevumi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="abcee-187">
                    <strong>Iekļaut laiku</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="abcee-188">
                    <strong>Iekļaut izdevumus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="abcee-189">
                    <strong>Ietveršana</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="abcee-190">
                    <strong>Maksa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="abcee-191">
                    <strong>Derīgs/Nav derīgs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="abcee-192">
                    <strong>Iemesls</strong>
                </span><span class="sxs-lookup"><span data-stu-id="abcee-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="abcee-193">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-194">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-195">QL1</span><span class="sxs-lookup"><span data-stu-id="abcee-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-196">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-197">Tukša</span><span class="sxs-lookup"><span data-stu-id="abcee-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-198">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-199">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-200">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-201">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="abcee-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-202">2. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="abcee-202">Violation of Rule #2.</span></span> <span data-ttu-id="abcee-203">Laiks, izdevumi un maksas P1 projektā ir ietvertas piedāvājuma rindās — gan QL1, gan QL2.</span><span class="sxs-lookup"><span data-stu-id="abcee-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="abcee-204">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-205">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-206">QL2</span><span class="sxs-lookup"><span data-stu-id="abcee-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-207">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-208">Tukša</span><span class="sxs-lookup"><span data-stu-id="abcee-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-209">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-210">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-211">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-211">Yes</span></span> </p>
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
<span data-ttu-id="abcee-212">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-213">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-214">QL1</span><span class="sxs-lookup"><span data-stu-id="abcee-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-215">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-216">Tukša</span><span class="sxs-lookup"><span data-stu-id="abcee-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-217">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-218">No</span><span class="sxs-lookup"><span data-stu-id="abcee-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-219">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-220">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="abcee-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-221">2. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="abcee-221">Violation of Rule #2.</span></span> <span data-ttu-id="abcee-222">Laiks un maksas P1 projektā ir ietvertas piedāvājuma rindās — gan QL1, gan QL2.</span><span class="sxs-lookup"><span data-stu-id="abcee-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="abcee-223">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-224">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-225">QL2</span><span class="sxs-lookup"><span data-stu-id="abcee-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-226">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-227">Tukša</span><span class="sxs-lookup"><span data-stu-id="abcee-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-228">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-229">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-230">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-230">Yes</span></span> </p>
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
<span data-ttu-id="abcee-231">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-232">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-233">QL1</span><span class="sxs-lookup"><span data-stu-id="abcee-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-234">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-235">Tukša</span><span class="sxs-lookup"><span data-stu-id="abcee-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-236">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-237">No</span><span class="sxs-lookup"><span data-stu-id="abcee-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-238">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-239">Derīgs</span><span class="sxs-lookup"><span data-stu-id="abcee-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="abcee-240">Laiks un maksas P1 projektā ir ietvertas rindā QL1.</span><span class="sxs-lookup"><span data-stu-id="abcee-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="abcee-241">Izdevumi P1 projektā ir ietverti rindā QL2.</span><span class="sxs-lookup"><span data-stu-id="abcee-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="abcee-242">Nepārklājas informācija, kas iekļauta katrā piedāvājuma rindā un ir derīga.</span><span class="sxs-lookup"><span data-stu-id="abcee-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="abcee-243">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-244">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-245">QL2</span><span class="sxs-lookup"><span data-stu-id="abcee-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-246">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-247">Tukša</span><span class="sxs-lookup"><span data-stu-id="abcee-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-248">No</span><span class="sxs-lookup"><span data-stu-id="abcee-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-249">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-250">No</span><span class="sxs-lookup"><span data-stu-id="abcee-250">No</span></span> </p>
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
<span data-ttu-id="abcee-251">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-252">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-253">QL1</span><span class="sxs-lookup"><span data-stu-id="abcee-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-254">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-255">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="abcee-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-256">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-257">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-258">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-259">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="abcee-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-260">Iepriekš norādītās 2. kārtulas pārkāpums</span><span class="sxs-lookup"><span data-stu-id="abcee-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="abcee-261">Q1 iekļauj laiku, izdevumus un maksas P1 projekta uzdevumu apakškopā.</span><span class="sxs-lookup"><span data-stu-id="abcee-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="abcee-262">QL2 ietver laiku, izdevumus un maksas par visu P1 projektu un pārklājas ar to, kas ir iekļauts Q1.</span><span class="sxs-lookup"><span data-stu-id="abcee-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="abcee-263">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-264">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-265">QL2</span><span class="sxs-lookup"><span data-stu-id="abcee-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-266">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-267">Tukša</span><span class="sxs-lookup"><span data-stu-id="abcee-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-268">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-269">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-270">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-270">Yes</span></span> </p>
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
<span data-ttu-id="abcee-271">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-272">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-273">QL1</span><span class="sxs-lookup"><span data-stu-id="abcee-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-274">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-275">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="abcee-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-276">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-277">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-278">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-279">Derīgs</span><span class="sxs-lookup"><span data-stu-id="abcee-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-280">Saskaņā ar iepriekš minēto 3. kārtulu,</span><span class="sxs-lookup"><span data-stu-id="abcee-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="abcee-281">Q1 iekļauj laiku, izdevumus un maksas P1 projekta uzdevumu apakškopā.</span><span class="sxs-lookup"><span data-stu-id="abcee-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="abcee-282">QL2 iekļauj laiku, izdevumus un maksas P1 projekta uzdevumu apakškopai.</span><span class="sxs-lookup"><span data-stu-id="abcee-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="abcee-283">Vienīgā papildu validācija ir ap QL1 uzdevumu apakškopu, kas atšķiras no QL2 uzdevumu apakškopas.</span><span class="sxs-lookup"><span data-stu-id="abcee-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="abcee-284">Šādi tiek nodrošināts, ka nav pārklāšanās.</span><span class="sxs-lookup"><span data-stu-id="abcee-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="abcee-285">To veic sistēma, kad tiek saistīti uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="abcee-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="abcee-286">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-287">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-288">QL2</span><span class="sxs-lookup"><span data-stu-id="abcee-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-289">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-290">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="abcee-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-291">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-292">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-293">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-293">Yes</span></span> </p>
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
<span data-ttu-id="abcee-294">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-295">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-296">QL1</span><span class="sxs-lookup"><span data-stu-id="abcee-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-297">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-298">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="abcee-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-299">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-300">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-301">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="abcee-302">Derīgs</span><span class="sxs-lookup"><span data-stu-id="abcee-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-303">Pamatojoties uz 5. kārtulu, Q1 un Q2 ir divi piedāvājumi par vienu un to pašu iespēju, tāpēc tos abus var izmantot vienu un to pašu projekta komponentu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="abcee-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="abcee-304">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-305">2. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-306">QL1</span><span class="sxs-lookup"><span data-stu-id="abcee-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-307">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-308">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="abcee-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-309">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-310">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-311">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-311">Yes</span></span> </p>
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
<span data-ttu-id="abcee-312">O1</span><span class="sxs-lookup"><span data-stu-id="abcee-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-313">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-314">QL1</span><span class="sxs-lookup"><span data-stu-id="abcee-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-315">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-316">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="abcee-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-317">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-318">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-319">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="abcee-320">Derīgs</span><span class="sxs-lookup"><span data-stu-id="abcee-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="abcee-321">Pamatojoties uz 4. kārtulu, Q1 un Q2 ir divi piedāvājumi par dažādām iespējām, tāpēc tos nevar izmantot tā paša projekta vienu un to pašu komponentu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="abcee-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="abcee-322">O2</span><span class="sxs-lookup"><span data-stu-id="abcee-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="abcee-323">1. cet.</span><span class="sxs-lookup"><span data-stu-id="abcee-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-324">QL1</span><span class="sxs-lookup"><span data-stu-id="abcee-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-325">P1</span><span class="sxs-lookup"><span data-stu-id="abcee-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="abcee-326">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="abcee-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-327">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="abcee-328">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="abcee-329">Jā</span><span class="sxs-lookup"><span data-stu-id="abcee-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="abcee-330">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="abcee-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

