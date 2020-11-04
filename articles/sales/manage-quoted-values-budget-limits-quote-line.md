---
title: Projekta piedāvājuma rindas
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu rindu izmantošanu projektu darbam.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080311"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="e2861-103">Projekta piedāvājuma rindas</span><span class="sxs-lookup"><span data-stu-id="e2861-103">Project-based quote lines</span></span>

<span data-ttu-id="e2861-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="e2861-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e2861-105">Projekta piedāvājumu rindas ir paredzētas, lai palīdzētu aprēķināt projekta darbu iesaistē.</span><span class="sxs-lookup"><span data-stu-id="e2861-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="e2861-106">Projekta piedāvājuma rindas struktūra ir paplašināta projekta aprēķiniem ar tālāk uzskaitītajiem jēdzieniem.</span><span class="sxs-lookup"><span data-stu-id="e2861-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="e2861-107">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="e2861-107">Billing Method</span></span>
- <span data-ttu-id="e2861-108">Projekta kartēšana</span><span class="sxs-lookup"><span data-stu-id="e2861-108">Project Mapping</span></span>
- <span data-ttu-id="e2861-109">Iekļautās transakciju klases</span><span class="sxs-lookup"><span data-stu-id="e2861-109">Included Transaction classes</span></span>
- <span data-ttu-id="e2861-110">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="e2861-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="e2861-111">Iekasēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e2861-111">Chargeability setup</span></span>
- <span data-ttu-id="e2861-112">Aprēķins, izmantojot piedāvājuma rindas detaļas</span><span class="sxs-lookup"><span data-stu-id="e2861-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="e2861-113">Piedāvājuma rindas klienti</span><span class="sxs-lookup"><span data-stu-id="e2861-113">Quote line Customers</span></span>

<span data-ttu-id="e2861-114">Tālāk redzamajā tabulā ir sniegta informācija par projekta piedāvājuma rindas cilnes **Vispārīgi** laukiem.</span><span class="sxs-lookup"><span data-stu-id="e2861-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="e2861-115">Šie lauki palīdz izveidot pamatu detalizētam, vispusīgam projekta darba aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="e2861-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="e2861-116">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="e2861-116">**Field**</span></span> | <span data-ttu-id="e2861-117">**Atbilstība, mērķis un norādes**</span><span class="sxs-lookup"><span data-stu-id="e2861-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="e2861-118">**Lejupstraumes ietekme**</span><span class="sxs-lookup"><span data-stu-id="e2861-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e2861-119">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="e2861-119">Name</span></span> | <span data-ttu-id="e2861-120">Piedāvājuma rindas nosaukums, kas palīdz identificēt aprēķināmā piedāvājuma diskrēto komponentu.</span><span class="sxs-lookup"><span data-stu-id="e2861-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="e2861-121">Pārkopēts uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e2861-122">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="e2861-122">Billing Method</span></span> | <span data-ttu-id="e2861-123">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no atbilstošā lauka iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="e2861-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="e2861-124">Šajā laukā ir iekļauti divi galvenie līgumu slēgšanas modeļi, kurus atbalsta Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="e2861-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="e2861-125">- fiksēta cena;</span><span class="sxs-lookup"><span data-stu-id="e2861-125">- Fixed price</span></span></br><span data-ttu-id="e2861-126">- laiks un materiāli.</span><span class="sxs-lookup"><span data-stu-id="e2861-126">- Time and material.</span></span>| <span data-ttu-id="e2861-127">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e2861-128">Project</span><span class="sxs-lookup"><span data-stu-id="e2861-128">Project</span></span> | <span data-ttu-id="e2861-129">Izmantojiet šo neobligāto lauku, lai identificētu projektu, kas tiks izmantots darba veikšanai šajā iesaistē.</span><span class="sxs-lookup"><span data-stu-id="e2861-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="e2861-130">Ja projekts ir kartēts uz piedāvājuma rindu, tas atvieglo apmaksājamo uzdevumu iestatīšanu, kā arī projekta aprēķina ievietošanu piedāvājuma rindā kā piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="e2861-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="e2861-131">Ja projekts netiek kartēts uz projekta piedāvājuma rindu, aprēķins ir jāizveido manuāli, izveidojot katru piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="e2861-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="e2861-132">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e2861-133">Iekļaut laiku</span><span class="sxs-lookup"><span data-stu-id="e2861-133">Include Time</span></span> | <span data-ttu-id="e2861-134">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e2861-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e2861-135">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e2861-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e2861-136">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e2861-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e2861-137">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e2861-138">Iekļaut izdevumus</span><span class="sxs-lookup"><span data-stu-id="e2861-138">Include Expense</span></span> | <span data-ttu-id="e2861-139">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e2861-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e2861-140">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e2861-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e2861-141">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e2861-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e2861-142">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e2861-143">Iekļaut maksu</span><span class="sxs-lookup"><span data-stu-id="e2861-143">Include Fee</span></span> | <span data-ttu-id="e2861-144">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="e2861-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e2861-145">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="e2861-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e2861-146">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="e2861-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e2861-147">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e2861-148">Minētā summa</span><span class="sxs-lookup"><span data-stu-id="e2861-148">Quoted Amount</span></span> | <span data-ttu-id="e2861-149">Šī ir summa, kas tiks piedāvāta klientam par visu darbu, kas prognozēts šajā projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="e2861-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="e2861-150">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no lauka **Klienta budžets** iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="e2861-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="e2861-151">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu summas.</span><span class="sxs-lookup"><span data-stu-id="e2861-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="e2861-152">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e2861-153">Aprēķinātais nodoklis</span><span class="sxs-lookup"><span data-stu-id="e2861-153">Estimated Tax</span></span> | <span data-ttu-id="e2861-154">Tas ir rediģējams lauks, kas lietotājam ļauj pievienot paredzamo nodokļu summu piedāvājuma rindai.</span><span class="sxs-lookup"><span data-stu-id="e2861-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="e2861-155">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu nodokļu summas.</span><span class="sxs-lookup"><span data-stu-id="e2861-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="e2861-156">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e2861-157">Piedāvātā summa pēc nodokļa atskaitīšanas</span><span class="sxs-lookup"><span data-stu-id="e2861-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="e2861-158">Šis lauks ir piedāvājuma rindas summa pēc nodokļiem un ir tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="e2861-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="e2861-159">Summu šajā laukā aprēķina kā *Piedāvātā summa + Nodokļi*.</span><span class="sxs-lookup"><span data-stu-id="e2861-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="e2861-160">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e2861-161">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="e2861-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="e2861-162">Šo lauku var rediģēt, un tas ir pieejams tikai projekta piedāvājuma rindās, kurām ir norēķinu metode **Laiks un materiāli**.</span><span class="sxs-lookup"><span data-stu-id="e2861-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="e2861-163">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e2861-164">Klienta budžets</span><span class="sxs-lookup"><span data-stu-id="e2861-164">Customer Budget</span></span> | <span data-ttu-id="e2861-165">Šis lauks ir rediģējams un tiek kopēts no atbilstošā lauka iespēju rindā, ja piedāvājums tika izveidots no iespējas.</span><span class="sxs-lookup"><span data-stu-id="e2861-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="e2861-166">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="e2861-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="e2861-167">Validācijas kārtulas laukiem projekta piedāvājumu rindu cilnē Vispārīgi</span><span class="sxs-lookup"><span data-stu-id="e2861-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="e2861-168">**1. kārtula** : noteiktu transakciju klasi atlasītajā projektā var iekļaut tikai vienā projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="e2861-168">**Rule 1** : A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="e2861-169">**2. kārtula** : ja iespējai ir vairāki piedāvājumi, var būt pieejamas piedāvājumu rindas no dažādiem piedāvājumiem, kas visi attiecas uz vienu un to pašu projektu un ietver to pašu transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="e2861-169">**Rule 2** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="e2861-170">**3. kārtula** : ja piedāvājumi nepieder vienai un tai pašai iespējai, tie nevar ietvert to pašu projektu un transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="e2861-170">**Rule 3** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="e2861-171">
                    <strong>Iespēja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2861-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="e2861-172">
                    <strong>Piedāvājums</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2861-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e2861-173">
                    <strong>Piedāvājuma rinda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2861-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e2861-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2861-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="e2861-175">
                    <strong>Iekļaut laiku</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2861-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="e2861-176">
                    <strong>Iekļaut izdevumus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2861-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e2861-177">
                    <strong>Ietveršana</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2861-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="e2861-178">
                    <strong>maksa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2861-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="e2861-179">
                    <strong>Derīgs/Nav derīgs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2861-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="e2861-180">
                    <strong>Iemesls</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2861-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e2861-181">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-182">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-183">QL1</span><span class="sxs-lookup"><span data-stu-id="e2861-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-184">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-185">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-186">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-187">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2861-188">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="e2861-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2861-189">1. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="e2861-189">Violation of Rule #1.</span></span> <span data-ttu-id="e2861-190">Laiks, izdevumi un maksas P1 projektā ir ietvertas abās piedāvājuma rindās — gan QL1, gan QL2.</span><span class="sxs-lookup"><span data-stu-id="e2861-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e2861-191">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-192">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-193">QL2</span><span class="sxs-lookup"><span data-stu-id="e2861-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-194">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-195">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-196">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-197">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-197">Yes</span></span> </p>
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
<span data-ttu-id="e2861-198">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-199">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-200">QL1</span><span class="sxs-lookup"><span data-stu-id="e2861-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-201">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-202">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-203">No</span><span class="sxs-lookup"><span data-stu-id="e2861-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-204">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2861-205">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="e2861-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2861-206">1. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="e2861-206">Violation of Rule #1.</span></span> <span data-ttu-id="e2861-207">Laiks un maksas P1 projektā ir ietvertas abās piedāvājuma rindās — gan QL1, gan QL2.</span><span class="sxs-lookup"><span data-stu-id="e2861-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e2861-208">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-209">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-210">QL2</span><span class="sxs-lookup"><span data-stu-id="e2861-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-211">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-212">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-213">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-214">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-214">Yes</span></span> </p>
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
<span data-ttu-id="e2861-215">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-216">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-217">QL1</span><span class="sxs-lookup"><span data-stu-id="e2861-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-218">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-219">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-220">No</span><span class="sxs-lookup"><span data-stu-id="e2861-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-221">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2861-222">Derīgs</span><span class="sxs-lookup"><span data-stu-id="e2861-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="e2861-223">Laiks un maksas P1 projektā ir ietvertas rindā QL1.</span><span class="sxs-lookup"><span data-stu-id="e2861-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="e2861-224">Izdevumi P1 projektā ir ietverti rindā QL2.</span><span class="sxs-lookup"><span data-stu-id="e2861-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="e2861-225">Nepārklājas informācija, kas iekļauta katrā piedāvājuma rindā, tāpēc tā ir derīga.</span><span class="sxs-lookup"><span data-stu-id="e2861-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e2861-226">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-227">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-228">QL2</span><span class="sxs-lookup"><span data-stu-id="e2861-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-229">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-230">No</span><span class="sxs-lookup"><span data-stu-id="e2861-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-231">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-232">No</span><span class="sxs-lookup"><span data-stu-id="e2861-232">No</span></span> </p>
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
<span data-ttu-id="e2861-233">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-234">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-235">QL1</span><span class="sxs-lookup"><span data-stu-id="e2861-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-236">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-237">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-238">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-239">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2861-240">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="e2861-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2861-241">Iepriekš norādītās 1. kārtulas pārkāpums</span><span class="sxs-lookup"><span data-stu-id="e2861-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="e2861-242">Q1 ietver laiku, izdevumus un maksas par visu P1 projektu.</span><span class="sxs-lookup"><span data-stu-id="e2861-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e2861-243">QL2 ietver laiku, izdevumus un maksas par visu P1 projektu un pārklājas ar to, kas ir iekļauts Q1.</span><span class="sxs-lookup"><span data-stu-id="e2861-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e2861-244">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-245">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-246">QL2</span><span class="sxs-lookup"><span data-stu-id="e2861-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-247">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-248">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-249">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-250">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-250">Yes</span></span> </p>
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
<span data-ttu-id="e2861-251">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-252">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-253">QL1</span><span class="sxs-lookup"><span data-stu-id="e2861-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-254">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-255">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-256">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-257">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e2861-258">Derīgs</span><span class="sxs-lookup"><span data-stu-id="e2861-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2861-259">Pamatojoties uz 2. kārtulu, Q1 un Q2 ir divi piedāvājumi par vienu un to pašu iespēju, tāpēc tos abus var izmantot vienu un to pašu projekta komponentu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="e2861-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e2861-260">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-261">2. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-262">QL1 uz Q2</span><span class="sxs-lookup"><span data-stu-id="e2861-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-263">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-264">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-265">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-266">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-266">Yes</span></span> </p>
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
<span data-ttu-id="e2861-267">O1</span><span class="sxs-lookup"><span data-stu-id="e2861-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-268">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-269">QL1</span><span class="sxs-lookup"><span data-stu-id="e2861-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-270">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-271">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-272">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-273">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e2861-274">Derīgs</span><span class="sxs-lookup"><span data-stu-id="e2861-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2861-275">Pamatojoties uz 3. kārtulu, Q1 un Q2 ir divi piedāvājumi par dažādām iespējām, tāpēc tos nevar izmantot tā paša projekta vienu un to pašu komponentu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="e2861-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e2861-276">O2</span><span class="sxs-lookup"><span data-stu-id="e2861-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e2861-277">1. cet.</span><span class="sxs-lookup"><span data-stu-id="e2861-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-278">QL1</span><span class="sxs-lookup"><span data-stu-id="e2861-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-279">P1</span><span class="sxs-lookup"><span data-stu-id="e2861-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-280">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e2861-281">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e2861-282">Jā</span><span class="sxs-lookup"><span data-stu-id="e2861-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e2861-283">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="e2861-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

