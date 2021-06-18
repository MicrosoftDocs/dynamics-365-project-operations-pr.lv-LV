---
title: Projekta piedāvājuma rindas pārskats
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu rindu izmantošanu projektu darbam.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994865"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="38f00-103">Projekta balstīta piedāvājuma rindu pārskats</span><span class="sxs-lookup"><span data-stu-id="38f00-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="38f00-104">_**Attiecas uz:** Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu, Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem_</span><span class="sxs-lookup"><span data-stu-id="38f00-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="38f00-105">Projekta piedāvājumu rindas ir paredzētas, lai palīdzētu aprēķināt projekta darbu iesaistē.</span><span class="sxs-lookup"><span data-stu-id="38f00-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="38f00-106">Projekta piedāvājuma rindas struktūra ir paplašināta projekta aprēķiniem ar tālāk uzskaitītajiem jēdzieniem.</span><span class="sxs-lookup"><span data-stu-id="38f00-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="38f00-107">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="38f00-107">Billing Method</span></span>
- <span data-ttu-id="38f00-108">Projektu un uzdevumu kartēšana</span><span class="sxs-lookup"><span data-stu-id="38f00-108">Project and Task Mapping</span></span>
- <span data-ttu-id="38f00-109">Iekļautās transakciju klases</span><span class="sxs-lookup"><span data-stu-id="38f00-109">Included Transaction classes</span></span>
- <span data-ttu-id="38f00-110">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="38f00-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="38f00-111">Iekasēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="38f00-111">Chargeability setup</span></span>
- <span data-ttu-id="38f00-112">Aprēķins, izmantojot piedāvājuma rindas detaļas</span><span class="sxs-lookup"><span data-stu-id="38f00-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="38f00-113">Piedāvājuma rindas klienti</span><span class="sxs-lookup"><span data-stu-id="38f00-113">Quote line Customers</span></span>

<span data-ttu-id="38f00-114">Tālāk redzamajā tabulā ir sniegta informācija par projekta piedāvājuma rindas cilnes **Vispārīgi** laukiem.</span><span class="sxs-lookup"><span data-stu-id="38f00-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="38f00-115">Šie lauki palīdz izveidot pamatu detalizētam, vispusīgam projekta darba aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="38f00-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="38f00-116">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="38f00-116">**Field**</span></span> | <span data-ttu-id="38f00-117">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="38f00-117">**Description**</span></span> | <span data-ttu-id="38f00-118">**Lejupstraumes ietekme**</span><span class="sxs-lookup"><span data-stu-id="38f00-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="38f00-119">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="38f00-119">Name</span></span> | <span data-ttu-id="38f00-120">Piedāvājuma rindas nosaukums, kas palīdz noteikt prognozējamā piedāvājuma komponentu.</span><span class="sxs-lookup"><span data-stu-id="38f00-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="38f00-121">Pārkopēts uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-122">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="38f00-122">Billing Method</span></span> | <span data-ttu-id="38f00-123">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no atbilstošā lauka iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="38f00-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="38f00-124">Šajā laukā ir divi galvenie līgumu slēgšanas modeļi, kurus Dynamics 365 Project Operations atbalsta:</span><span class="sxs-lookup"><span data-stu-id="38f00-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="38f00-125">- fiksēta cena;</span><span class="sxs-lookup"><span data-stu-id="38f00-125">- Fixed price</span></span></br><span data-ttu-id="38f00-126">- laiks un materiāli.</span><span class="sxs-lookup"><span data-stu-id="38f00-126">- Time and material.</span></span>| <span data-ttu-id="38f00-127">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-128">Project</span><span class="sxs-lookup"><span data-stu-id="38f00-128">Project</span></span> | <span data-ttu-id="38f00-129">Izmantojiet šo neobligāto lauku, lai identificētu projektu, kas tiks izmantots darba veikšanai šajā iesaistē.</span><span class="sxs-lookup"><span data-stu-id="38f00-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="38f00-130">Ja projekts ir kartēts uz piedāvājuma rindu, tas atvieglo apmaksājamo uzdevumu iestatīšanu, kā arī projekta aprēķina ievietošanu piedāvājuma rindā kā piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="38f00-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="38f00-131">Ja projekts netiek kartēts uz projekta piedāvājuma rindu, aprēķins ir jāizveido manuāli, izveidojot katru piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="38f00-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="38f00-132">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="38f00-133">Iekļautie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="38f00-133">Included Tasks</span></span> | <span data-ttu-id="38f00-134">Norāda, vai šī piedāvājuma rinda tiek izmantota visiem atlasītā projekta uzdevumiem vai dažiem no tiem.</span><span class="sxs-lookup"><span data-stu-id="38f00-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="38f00-135">Šim laukam ir šādas iespējamās vērtības:</span><span class="sxs-lookup"><span data-stu-id="38f00-135">This field has the following possible values:</span></span></br><span data-ttu-id="38f00-136">- visi projekta uzdevumi;</span><span class="sxs-lookup"><span data-stu-id="38f00-136">- All project tasks</span></span></br><span data-ttu-id="38f00-137">- tikai atlasītie projekta uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="38f00-137">- Selected project tasks only</span></span></br><span data-ttu-id="38f00-138">Tukša vērtība šajā laukā ir līdzvērtīga opcijai **Visi projekta uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="38f00-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="38f00-139">Projekta lapā atlasot **Tikai atlas‪ītie projekta uzdevumi**, cilnē **Uzdevuma norēķinu iestatīšana** varat atlasīt noteiktus uzdevumus, lai tos saistītu ar šo piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="38f00-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="38f00-140">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-141">Iekļaut laiku</span><span class="sxs-lookup"><span data-stu-id="38f00-141">Include Time</span></span> | <span data-ttu-id="38f00-142">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā laika transakcijas vai darbaspēka izmaksas tiks iekļautas šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="38f00-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="38f00-143">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="38f00-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="38f00-144">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="38f00-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="38f00-145">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-146">Iekļaut izdevumus</span><span class="sxs-lookup"><span data-stu-id="38f00-146">Include Expense</span></span> | <span data-ttu-id="38f00-147">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā izdevumi tiks iekļauti šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="38f00-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="38f00-148">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="38f00-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="38f00-149">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="38f00-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="38f00-150">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-151">Iekļaut materiālu</span><span class="sxs-lookup"><span data-stu-id="38f00-151">Include Material</span></span> | <span data-ttu-id="38f00-152">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā materiālu izmaksas tiks iekļautas šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="38f00-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="38f00-153">Vērtība **Nē** norāda, ka atlasītajā projektā materiālu izmaksas netiks iekļautas šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="38f00-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="38f00-154">Vērtība **Jā** norāda, ka atlasītajā projektā materiālu izmaksas tiks iekļautas šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="38f00-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="38f00-155">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-156">Iekļaut maksu</span><span class="sxs-lookup"><span data-stu-id="38f00-156">Include Fee</span></span> | <span data-ttu-id="38f00-157">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā maksas tiks iekļautas šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="38f00-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="38f00-158">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="38f00-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="38f00-159">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="38f00-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="38f00-160">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-161">Minētā summa</span><span class="sxs-lookup"><span data-stu-id="38f00-161">Quoted Amount</span></span> | <span data-ttu-id="38f00-162">Šī ir summa, kas klientam tiks piedāvāta par visu šajā projekta piedāvājuma rindā prognozēto darbu.</span><span class="sxs-lookup"><span data-stu-id="38f00-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="38f00-163">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no lauka **Klienta budžets** iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="38f00-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="38f00-164">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu summas.</span><span class="sxs-lookup"><span data-stu-id="38f00-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="38f00-165">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-166">Aprēķinātais nodoklis</span><span class="sxs-lookup"><span data-stu-id="38f00-166">Estimated Tax</span></span> | <span data-ttu-id="38f00-167">Tas ir rediģējams lauks, kas lietotājam ļauj pievienot paredzamo nodokļu summu piedāvājuma rindai.</span><span class="sxs-lookup"><span data-stu-id="38f00-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="38f00-168">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu nodokļu summas.</span><span class="sxs-lookup"><span data-stu-id="38f00-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="38f00-169">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-170">Piedāvātā summa pēc nodokļa atskaitīšanas</span><span class="sxs-lookup"><span data-stu-id="38f00-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="38f00-171">Šis lauks ir piedāvājuma rindas summa pēc nodokļiem un ir tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="38f00-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="38f00-172">Summu šajā laukā aprēķina kā *Piedāvātā summa + Nodokļi*.</span><span class="sxs-lookup"><span data-stu-id="38f00-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="38f00-173">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-174">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="38f00-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="38f00-175">Šo lauku var rediģēt, un tas ir pieejams tikai projekta piedāvājuma rindās, kurām ir norēķinu metode **Laiks un materiāli**.</span><span class="sxs-lookup"><span data-stu-id="38f00-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="38f00-176">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38f00-177">Klienta budžets</span><span class="sxs-lookup"><span data-stu-id="38f00-177">Customer Budget</span></span> | <span data-ttu-id="38f00-178">Šis lauks ir rediģējams un tiek kopēts no atbilstošā lauka iespēju rindā, ja piedāvājums tika izveidots no iespējas.</span><span class="sxs-lookup"><span data-stu-id="38f00-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="38f00-179">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="38f00-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="38f00-180">Validācijas kārtulas laukiem projekta piedāvājumu rindu cilnē Vispārīgi</span><span class="sxs-lookup"><span data-stu-id="38f00-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="38f00-181">**1. kārtula**: ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi**, projekts tiek iekļauts piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="38f00-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="38f00-182">**2. kārtula**: ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut tikai vienā projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="38f00-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="38f00-183">**3. kārtula**: ja lauks **Iekļautie uzdevumi** ir ir iestatīts uz **Tikai atlasītie projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut vairākās projekta piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="38f00-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="38f00-184">**4. kārtula**: ja iespējai ir vairāki piedāvājumi, var būt pieejamas piedāvājumu rindas no dažādiem piedāvājumiem, kas visi attiecas uz vienu un to pašu projektu un ietver to pašu transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="38f00-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="38f00-185">**5. kārtula**: ja piedāvājumi nepieder vienai un tai pašai iespējai, tie nevar ietvert to pašu projektu un transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="38f00-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="38f00-186">
                    <strong>Iespēja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="38f00-187">
                    <strong>Piedāvājums</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="38f00-188">
                    <strong>Piedāvājuma rinda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="38f00-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="38f00-190">
                    <strong>Iekļautie uzdevumi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="38f00-191">
                    <strong>Iekļaut laiku</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="38f00-192">
                    <strong>Iekļaut izdevumus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="38f00-193">
                    <strong>Iekļaut materiālu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="38f00-194">
                    <strong>Iekļaut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="38f00-195">
                    <strong>Maksa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="38f00-196">
                    <strong>Derīgs/Nav derīgs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="38f00-197">
                    <strong>Iemesls</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38f00-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-198">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-199">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-200">QL1</span><span class="sxs-lookup"><span data-stu-id="38f00-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-201">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-202">Tukša</span><span class="sxs-lookup"><span data-stu-id="38f00-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-203">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-204">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-205">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-206">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-207">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="38f00-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-208">2. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="38f00-208">Violation of Rule #2.</span></span> <span data-ttu-id="38f00-209">Laiks, izdevumi un maksas P1 projektā ir ietvertas piedāvājuma rindā QL1 un QL2.</span><span class="sxs-lookup"><span data-stu-id="38f00-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-210">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-211">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-212">QL2</span><span class="sxs-lookup"><span data-stu-id="38f00-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-213">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-214">Tukša</span><span class="sxs-lookup"><span data-stu-id="38f00-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-215">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-216">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-217">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-218">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-219">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-220">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-221">QL1</span><span class="sxs-lookup"><span data-stu-id="38f00-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-222">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-223">Tukša</span><span class="sxs-lookup"><span data-stu-id="38f00-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-224">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-225">Nr.</span><span class="sxs-lookup"><span data-stu-id="38f00-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-226">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-227">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-228">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="38f00-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-229">2. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="38f00-229">Violation of Rule #2.</span></span> <span data-ttu-id="38f00-230">Laiks, materiāli un maksas P1 projektā ir ietvertas piedāvājuma rindā QL1 un QL2.</span><span class="sxs-lookup"><span data-stu-id="38f00-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-231">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-232">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-233">QL2</span><span class="sxs-lookup"><span data-stu-id="38f00-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-234">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-235">Tukša</span><span class="sxs-lookup"><span data-stu-id="38f00-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-236">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-237">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-238">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-239">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-240">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-241">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-242">QL1</span><span class="sxs-lookup"><span data-stu-id="38f00-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-243">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-244">Tukša</span><span class="sxs-lookup"><span data-stu-id="38f00-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-245">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-246">Nr.</span><span class="sxs-lookup"><span data-stu-id="38f00-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-247">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-248">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-249">Derīgs</span><span class="sxs-lookup"><span data-stu-id="38f00-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-250">Laiks, materiāli un maksas P1 projektā ir ietvertas rindā QL1.</span><span class="sxs-lookup"><span data-stu-id="38f00-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="38f00-251">Izdevumi P1 projektā ir ietverti rindā QL2.</span><span class="sxs-lookup"><span data-stu-id="38f00-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="38f00-252">Latrā piedāvājuma rindā ietvertās vērtības nepārklājas, tāpēc ir derīgas.</span><span class="sxs-lookup"><span data-stu-id="38f00-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-253">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-254">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-255">QL2</span><span class="sxs-lookup"><span data-stu-id="38f00-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-256">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-257">Tukša</span><span class="sxs-lookup"><span data-stu-id="38f00-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-258">Nr.</span><span class="sxs-lookup"><span data-stu-id="38f00-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-259">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-260">Nr.</span><span class="sxs-lookup"><span data-stu-id="38f00-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-261">Nr.</span><span class="sxs-lookup"><span data-stu-id="38f00-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-262">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-263">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-264">QL1</span><span class="sxs-lookup"><span data-stu-id="38f00-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-265">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-266">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="38f00-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-267">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-268">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-269">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-270">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-271">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="38f00-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-272">2. kārtulas pārkāpums</span><span class="sxs-lookup"><span data-stu-id="38f00-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="38f00-273">Q1 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai</span><span class="sxs-lookup"><span data-stu-id="38f00-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="38f00-274">QL2 ietver laiku, izdevumus un maksas par visu projektu P1 un tāpēc pārklājas ar to, kas ir iekļauts Q1.</span><span class="sxs-lookup"><span data-stu-id="38f00-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-275">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-276">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-277">QL2</span><span class="sxs-lookup"><span data-stu-id="38f00-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-278">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-279">Tukša</span><span class="sxs-lookup"><span data-stu-id="38f00-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-280">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-281">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-282">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-283">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-284">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-285">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-286">QL1</span><span class="sxs-lookup"><span data-stu-id="38f00-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-287">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-288">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="38f00-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-289">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-290">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-291">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-292">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-293">Derīgs</span><span class="sxs-lookup"><span data-stu-id="38f00-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-294">Atbilstoši 3. kārtulai</span><span class="sxs-lookup"><span data-stu-id="38f00-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="38f00-295">Q1 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.</span><span class="sxs-lookup"><span data-stu-id="38f00-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="38f00-296">QL2 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.</span><span class="sxs-lookup"><span data-stu-id="38f00-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="38f00-297">Vienīgā papildu validācija attiecas uz QL1 uzdevumu apakškopu, kas atšķiras no QL2 uzdevumu apakškopas, lai nodrošinātu nepārklāšanos.</span><span class="sxs-lookup"><span data-stu-id="38f00-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="38f00-298">To veic sistēma, kad tiek saistīti uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="38f00-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-299">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-300">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-301">QL2</span><span class="sxs-lookup"><span data-stu-id="38f00-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-302">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-303">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="38f00-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-304">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-305">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-306">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-307">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-308">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-309">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-310">QL1</span><span class="sxs-lookup"><span data-stu-id="38f00-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-311">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-312">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="38f00-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-313">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-314">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-315">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-316">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-317">Derīgs</span><span class="sxs-lookup"><span data-stu-id="38f00-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-318">Atbilstoši 5. kārtulai Q1 un Q2 ir divi piedāvājumi par vienu un to pašu iespēju, tādēļ abi tie var novērtēt vienu un to pašu projekta komponentu.</span><span class="sxs-lookup"><span data-stu-id="38f00-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-319">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-320">2. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-321">QL1</span><span class="sxs-lookup"><span data-stu-id="38f00-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-322">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-323">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="38f00-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-324">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-325">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-326">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-327">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-328">O1</span><span class="sxs-lookup"><span data-stu-id="38f00-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-329">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-330">QL1</span><span class="sxs-lookup"><span data-stu-id="38f00-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-331">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-332">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="38f00-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-333">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-334">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-335">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-336">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-337">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="38f00-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38f00-338">Atbilstoši 4. kārtulai Q1 un Q2 ir divi piedāvājumi par atšķirīgām iespējām, tādēļ abi tie nevar novērtēt vienu un to pašu projekta komponentu.</span><span class="sxs-lookup"><span data-stu-id="38f00-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="38f00-339">O2</span><span class="sxs-lookup"><span data-stu-id="38f00-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="38f00-340">1. cet.</span><span class="sxs-lookup"><span data-stu-id="38f00-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="38f00-341">QL1</span><span class="sxs-lookup"><span data-stu-id="38f00-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-342">P1</span><span class="sxs-lookup"><span data-stu-id="38f00-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="38f00-343">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="38f00-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="38f00-344">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="38f00-345">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="38f00-346">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38f00-347">Jā</span><span class="sxs-lookup"><span data-stu-id="38f00-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
