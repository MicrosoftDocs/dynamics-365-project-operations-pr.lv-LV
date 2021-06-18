---
title: Projekta piedāvājuma rindu pārskats
description: Šajā tēmā ir sniegta informācija par projekta piedāvājuma rindu izmantošanu projekta darbā.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 72feb791e48c9bacd4a0b7ea5cd77ddc8eb5f514
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996305"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="67f23-103">Projekta piedāvājuma rindu pārskats</span><span class="sxs-lookup"><span data-stu-id="67f23-103">Project quote lines overview</span></span>

<span data-ttu-id="67f23-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="67f23-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="67f23-105">Projekta piedāvājumu rindas ir paredzētas, lai palīdzētu aprēķināt projekta darbu iesaistē.</span><span class="sxs-lookup"><span data-stu-id="67f23-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="67f23-106">Projekta piedāvājuma rindas struktūra ir paplašināta projekta aprēķiniem ar tālāk uzskaitītajiem jēdzieniem.</span><span class="sxs-lookup"><span data-stu-id="67f23-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="67f23-107">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="67f23-107">Billing Method</span></span>
- <span data-ttu-id="67f23-108">Projekta kartēšana</span><span class="sxs-lookup"><span data-stu-id="67f23-108">Project Mapping</span></span>
- <span data-ttu-id="67f23-109">Iekļautās transakciju klases</span><span class="sxs-lookup"><span data-stu-id="67f23-109">Included Transaction classes</span></span>
- <span data-ttu-id="67f23-110">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="67f23-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="67f23-111">Iekasēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="67f23-111">Chargeability setup</span></span>
- <span data-ttu-id="67f23-112">Aprēķins, izmantojot piedāvājuma rindas detaļas</span><span class="sxs-lookup"><span data-stu-id="67f23-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="67f23-113">Piedāvājuma rindas klienti</span><span class="sxs-lookup"><span data-stu-id="67f23-113">Quote line Customers</span></span>

<span data-ttu-id="67f23-114">Tālāk redzamajā tabulā ir sniegta informācija par projekta piedāvājuma rindas cilnes **Vispārīgi** laukiem.</span><span class="sxs-lookup"><span data-stu-id="67f23-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="67f23-115">Šie lauki palīdz izveidot pamatu detalizētam, vispusīgam projekta darba aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="67f23-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="67f23-116">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="67f23-116">**Field**</span></span> | <span data-ttu-id="67f23-117">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="67f23-117">**Description**</span></span> | <span data-ttu-id="67f23-118">**Lejupstraumes ietekme**</span><span class="sxs-lookup"><span data-stu-id="67f23-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="67f23-119">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="67f23-119">Name</span></span> | <span data-ttu-id="67f23-120">Piedāvājuma rindas nosaukums, kas palīdz identificēt aprēķināmā piedāvājuma diskrēto komponentu.</span><span class="sxs-lookup"><span data-stu-id="67f23-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="67f23-121">Pārkopēts uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="67f23-122">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="67f23-122">Billing Method</span></span> | <span data-ttu-id="67f23-123">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no atbilstošā lauka iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="67f23-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="67f23-124">Šajā laukā ir divi galvenie līgumu slēgšanas modeļi, kurus Dynamics 365 Project Operations atbalsta:</span><span class="sxs-lookup"><span data-stu-id="67f23-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="67f23-125">- fiksēta cena;</span><span class="sxs-lookup"><span data-stu-id="67f23-125">- Fixed price</span></span></br><span data-ttu-id="67f23-126">- laiks un materiāli.</span><span class="sxs-lookup"><span data-stu-id="67f23-126">- Time and material.</span></span>| <span data-ttu-id="67f23-127">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="67f23-128">Project</span><span class="sxs-lookup"><span data-stu-id="67f23-128">Project</span></span> | <span data-ttu-id="67f23-129">Izmantojiet šo neobligāto lauku, lai identificētu projektu, kas tiks izmantots darba veikšanai šajā iesaistē.</span><span class="sxs-lookup"><span data-stu-id="67f23-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="67f23-130">Ja projekts ir kartēts uz piedāvājuma rindu, tas atvieglo apmaksājamo uzdevumu iestatīšanu, kā arī projekta aprēķina ievietošanu piedāvājuma rindā kā piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="67f23-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="67f23-131">Ja projekts netiek kartēts uz projekta piedāvājuma rindu, aprēķins ir jāizveido manuāli, izveidojot katru piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="67f23-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="67f23-132">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="67f23-133">Iekļaut laiku</span><span class="sxs-lookup"><span data-stu-id="67f23-133">Include Time</span></span> | <span data-ttu-id="67f23-134">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="67f23-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="67f23-135">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="67f23-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="67f23-136">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="67f23-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="67f23-137">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="67f23-138">Iekļaut izdevumus</span><span class="sxs-lookup"><span data-stu-id="67f23-138">Include Expense</span></span> | <span data-ttu-id="67f23-139">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="67f23-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="67f23-140">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="67f23-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="67f23-141">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="67f23-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="67f23-142">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="67f23-143">Iekļaut maksu</span><span class="sxs-lookup"><span data-stu-id="67f23-143">Include Fee</span></span> | <span data-ttu-id="67f23-144">Karodziņš **Jā**/**Nē** norāda, vai atlasītajā projektā šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="67f23-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="67f23-145">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="67f23-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="67f23-146">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="67f23-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="67f23-147">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="67f23-148">Minētā summa</span><span class="sxs-lookup"><span data-stu-id="67f23-148">Quoted Amount</span></span> | <span data-ttu-id="67f23-149">Šī ir summa, kas tiks piedāvāta klientam par visu darbu, kas prognozēts šajā projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="67f23-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="67f23-150">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no lauka **Klienta budžets** iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="67f23-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="67f23-151">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu summas.</span><span class="sxs-lookup"><span data-stu-id="67f23-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="67f23-152">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="67f23-153">Aprēķinātais nodoklis</span><span class="sxs-lookup"><span data-stu-id="67f23-153">Estimated Tax</span></span> | <span data-ttu-id="67f23-154">Tas ir rediģējams lauks, kas lietotājam ļauj pievienot paredzamo nodokļu summu piedāvājuma rindai.</span><span class="sxs-lookup"><span data-stu-id="67f23-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="67f23-155">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu nodokļu summas.</span><span class="sxs-lookup"><span data-stu-id="67f23-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="67f23-156">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="67f23-157">Piedāvātā summa pēc nodokļa atskaitīšanas</span><span class="sxs-lookup"><span data-stu-id="67f23-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="67f23-158">Šis lauks ir piedāvājuma rindas summa pēc nodokļiem un ir tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="67f23-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="67f23-159">Summu šajā laukā aprēķina kā *Piedāvātā summa + Nodokļi*.</span><span class="sxs-lookup"><span data-stu-id="67f23-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="67f23-160">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="67f23-161">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="67f23-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="67f23-162">Šo lauku var rediģēt, un tas ir pieejams tikai projekta piedāvājuma rindās, kurām ir norēķinu metode **Laiks un materiāli**.</span><span class="sxs-lookup"><span data-stu-id="67f23-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="67f23-163">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="67f23-164">Klienta budžets</span><span class="sxs-lookup"><span data-stu-id="67f23-164">Customer Budget</span></span> | <span data-ttu-id="67f23-165">Šis lauks ir rediģējams un tiek kopēts no atbilstošā lauka iespēju rindā, ja piedāvājums tika izveidots no iespējas.</span><span class="sxs-lookup"><span data-stu-id="67f23-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="67f23-166">Šī vērtība tiek pārkopēta uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="67f23-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="67f23-167">Validācijas kārtulas laukiem projekta piedāvājumu rindu cilnē Vispārīgi</span><span class="sxs-lookup"><span data-stu-id="67f23-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="67f23-168">**1. kārtula**: noteiktu transakciju klasi atlasītajā projektā var iekļaut tikai vienā projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="67f23-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="67f23-169">**2. kārtula**: ja iespējai ir vairāki piedāvājumi, var būt pieejamas piedāvājumu rindas no dažādiem piedāvājumiem, kas visi attiecas uz vienu un to pašu projektu un ietver to pašu transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="67f23-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="67f23-170">**3. kārtula**: ja piedāvājumi nepieder vienai un tai pašai iespējai, tie nevar ietvert to pašu projektu un transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="67f23-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="67f23-171">
                    <strong>Iespēja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="67f23-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="67f23-172">
                    <strong>Piedāvājums</strong>
                </span><span class="sxs-lookup"><span data-stu-id="67f23-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="67f23-173">
                    <strong>Piedāvājuma rinda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="67f23-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="67f23-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="67f23-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="67f23-175">
                    <strong>Iekļaut laiku</strong>
                </span><span class="sxs-lookup"><span data-stu-id="67f23-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="67f23-176">
                    <strong>Iekļaut izdevumus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="67f23-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="67f23-177">
                    <strong>Ietveršana</strong>
                </span><span class="sxs-lookup"><span data-stu-id="67f23-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="67f23-178">
                    <strong>maksa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="67f23-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="67f23-179">
                    <strong>Derīgs/Nav derīgs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="67f23-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="67f23-180">
                    <strong>Iemesls</strong>
                </span><span class="sxs-lookup"><span data-stu-id="67f23-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="67f23-181">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-182">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-183">QL1</span><span class="sxs-lookup"><span data-stu-id="67f23-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-184">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-185">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-186">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-187">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="67f23-188">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="67f23-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="67f23-189">1. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="67f23-189">Violation of Rule #1.</span></span> <span data-ttu-id="67f23-190">Laiks, izdevumi un maksas P1 projektā ir ietvertas abās piedāvājuma rindās — gan QL1, gan QL2.</span><span class="sxs-lookup"><span data-stu-id="67f23-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="67f23-191">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-192">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-193">QL2</span><span class="sxs-lookup"><span data-stu-id="67f23-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-194">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-195">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-196">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-197">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-197">Yes</span></span> </p>
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
<span data-ttu-id="67f23-198">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-199">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-200">QL1</span><span class="sxs-lookup"><span data-stu-id="67f23-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-201">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-202">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-203">No</span><span class="sxs-lookup"><span data-stu-id="67f23-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-204">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="67f23-205">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="67f23-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="67f23-206">1. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="67f23-206">Violation of Rule #1.</span></span> <span data-ttu-id="67f23-207">Laiks un maksas P1 projektā ir ietvertas abās piedāvājuma rindās — gan QL1, gan QL2.</span><span class="sxs-lookup"><span data-stu-id="67f23-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="67f23-208">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-209">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-210">QL2</span><span class="sxs-lookup"><span data-stu-id="67f23-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-211">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-212">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-213">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-214">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-214">Yes</span></span> </p>
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
<span data-ttu-id="67f23-215">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-216">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-217">QL1</span><span class="sxs-lookup"><span data-stu-id="67f23-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-218">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-219">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-220">No</span><span class="sxs-lookup"><span data-stu-id="67f23-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-221">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="67f23-222">Derīgs</span><span class="sxs-lookup"><span data-stu-id="67f23-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="67f23-223">Laiks un maksas P1 projektā ir ietvertas rindā QL1.</span><span class="sxs-lookup"><span data-stu-id="67f23-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="67f23-224">Izdevumi P1 projektā ir ietverti rindā QL2.</span><span class="sxs-lookup"><span data-stu-id="67f23-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="67f23-225">Nepārklājas informācija, kas iekļauta katrā piedāvājuma rindā, tāpēc tā ir derīga.</span><span class="sxs-lookup"><span data-stu-id="67f23-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="67f23-226">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-227">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-228">QL2</span><span class="sxs-lookup"><span data-stu-id="67f23-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-229">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-230">No</span><span class="sxs-lookup"><span data-stu-id="67f23-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-231">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-232">No</span><span class="sxs-lookup"><span data-stu-id="67f23-232">No</span></span> </p>
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
<span data-ttu-id="67f23-233">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-234">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-235">QL1</span><span class="sxs-lookup"><span data-stu-id="67f23-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-236">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-237">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-238">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-239">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="67f23-240">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="67f23-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="67f23-241">Iepriekš norādītās 1. kārtulas pārkāpums</span><span class="sxs-lookup"><span data-stu-id="67f23-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="67f23-242">Q1 ietver laiku, izdevumus un maksas par visu P1 projektu.</span><span class="sxs-lookup"><span data-stu-id="67f23-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="67f23-243">QL2 ietver laiku, izdevumus un maksas par visu P1 projektu un pārklājas ar to, kas ir iekļauts Q1.</span><span class="sxs-lookup"><span data-stu-id="67f23-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="67f23-244">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-245">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-246">QL2</span><span class="sxs-lookup"><span data-stu-id="67f23-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-247">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-248">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-249">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-250">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-250">Yes</span></span> </p>
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
<span data-ttu-id="67f23-251">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-252">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-253">QL1</span><span class="sxs-lookup"><span data-stu-id="67f23-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-254">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-255">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-256">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-257">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="67f23-258">Derīgs</span><span class="sxs-lookup"><span data-stu-id="67f23-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="67f23-259">Pamatojoties uz 2. kārtulu, Q1 un Q2 ir divi piedāvājumi par vienu un to pašu iespēju, tāpēc tos abus var izmantot vienu un to pašu projekta komponentu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="67f23-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="67f23-260">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-261">2. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-262">QL1 uz Q2</span><span class="sxs-lookup"><span data-stu-id="67f23-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-263">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-264">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-265">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-266">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-266">Yes</span></span> </p>
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
<span data-ttu-id="67f23-267">O1</span><span class="sxs-lookup"><span data-stu-id="67f23-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-268">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-269">QL1</span><span class="sxs-lookup"><span data-stu-id="67f23-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-270">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-271">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-272">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-273">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="67f23-274">Derīgs</span><span class="sxs-lookup"><span data-stu-id="67f23-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="67f23-275">Pamatojoties uz 3. kārtulu, Q1 un Q2 ir divi piedāvājumi par dažādām iespējām, tāpēc tos nevar izmantot tā paša projekta vienu un to pašu komponentu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="67f23-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="67f23-276">O2</span><span class="sxs-lookup"><span data-stu-id="67f23-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="67f23-277">1. cet.</span><span class="sxs-lookup"><span data-stu-id="67f23-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-278">QL1</span><span class="sxs-lookup"><span data-stu-id="67f23-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-279">P1</span><span class="sxs-lookup"><span data-stu-id="67f23-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-280">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="67f23-281">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="67f23-282">Jā</span><span class="sxs-lookup"><span data-stu-id="67f23-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="67f23-283">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="67f23-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
