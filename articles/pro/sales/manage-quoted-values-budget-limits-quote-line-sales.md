---
title: Projekta piedāvājuma rindas pārskats
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu rindu izmantošanu projektu darbam.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858707"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="0a6a2-103">Projekta balstīta piedāvājuma rindu pārskats</span><span class="sxs-lookup"><span data-stu-id="0a6a2-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="0a6a2-104">_**Attiecas uz:** Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu, Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem_</span><span class="sxs-lookup"><span data-stu-id="0a6a2-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0a6a2-105">Projekta piedāvājumu rindas ir paredzētas, lai palīdzētu aprēķināt projekta darbu iesaistē.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="0a6a2-106">Projekta piedāvājuma rindas struktūra ir paplašināta projekta aprēķiniem ar tālāk uzskaitītajiem jēdzieniem.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="0a6a2-107">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="0a6a2-107">Billing Method</span></span>
- <span data-ttu-id="0a6a2-108">Projektu un uzdevumu kartēšana</span><span class="sxs-lookup"><span data-stu-id="0a6a2-108">Project and Task Mapping</span></span>
- <span data-ttu-id="0a6a2-109">Iekļautās transakciju klases</span><span class="sxs-lookup"><span data-stu-id="0a6a2-109">Included Transaction classes</span></span>
- <span data-ttu-id="0a6a2-110">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="0a6a2-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="0a6a2-111">Iekasēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0a6a2-111">Chargeability setup</span></span>
- <span data-ttu-id="0a6a2-112">Aprēķins, izmantojot piedāvājuma rindas detaļas</span><span class="sxs-lookup"><span data-stu-id="0a6a2-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="0a6a2-113">Piedāvājuma rindas klienti</span><span class="sxs-lookup"><span data-stu-id="0a6a2-113">Quote line Customers</span></span>

<span data-ttu-id="0a6a2-114">Tālāk redzamajā tabulā ir sniegta informācija par projekta piedāvājuma rindas cilnes **Vispārīgi** laukiem.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="0a6a2-115">Šie lauki palīdz izveidot pamatu detalizētam, vispusīgam projekta darba aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="0a6a2-116">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="0a6a2-116">**Field**</span></span> | <span data-ttu-id="0a6a2-117">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="0a6a2-117">**Description**</span></span> | <span data-ttu-id="0a6a2-118">**Lejupstraumes ietekme**</span><span class="sxs-lookup"><span data-stu-id="0a6a2-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0a6a2-119">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="0a6a2-119">Name</span></span> | <span data-ttu-id="0a6a2-120">Piedāvājuma rindas nosaukums, kas palīdz noteikt prognozējamā piedāvājuma komponentu.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="0a6a2-121">Pārkopēts uz projekta līguma rindu, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-122">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="0a6a2-122">Billing Method</span></span> | <span data-ttu-id="0a6a2-123">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no atbilstošā lauka iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="0a6a2-124">Šajā laukā ir divi galvenie līgumu slēgšanas modeļi, kurus Dynamics 365 Project Operations atbalsta:</span><span class="sxs-lookup"><span data-stu-id="0a6a2-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="0a6a2-125">- fiksēta cena;</span><span class="sxs-lookup"><span data-stu-id="0a6a2-125">- Fixed price</span></span></br><span data-ttu-id="0a6a2-126">- laiks un materiāli.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-126">- Time and material.</span></span>| <span data-ttu-id="0a6a2-127">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-128">Project</span><span class="sxs-lookup"><span data-stu-id="0a6a2-128">Project</span></span> | <span data-ttu-id="0a6a2-129">Izmantojiet šo neobligāto lauku, lai identificētu projektu, kas tiks izmantots darba veikšanai šajā iesaistē.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="0a6a2-130">Ja projekts ir kartēts uz piedāvājuma rindu, tas atvieglo apmaksājamo uzdevumu iestatīšanu, kā arī projekta aprēķina ievietošanu piedāvājuma rindā kā piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="0a6a2-131">Ja projekts netiek kartēts uz projekta piedāvājuma rindu, aprēķins ir jāizveido manuāli, izveidojot katru piedāvājuma rindas detaļu.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="0a6a2-132">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="0a6a2-133">Iekļautie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="0a6a2-133">Included Tasks</span></span> | <span data-ttu-id="0a6a2-134">Norāda, vai šī piedāvājuma rinda tiek izmantota visiem atlasītā projekta uzdevumiem vai dažiem no tiem.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="0a6a2-135">Šim laukam ir šādas iespējamās vērtības:</span><span class="sxs-lookup"><span data-stu-id="0a6a2-135">This field has the following possible values:</span></span></br><span data-ttu-id="0a6a2-136">- visi projekta uzdevumi;</span><span class="sxs-lookup"><span data-stu-id="0a6a2-136">- All project tasks</span></span></br><span data-ttu-id="0a6a2-137">- tikai atlasītie projekta uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-137">- Selected project tasks only</span></span></br><span data-ttu-id="0a6a2-138">Tukša vērtība šajā laukā ir līdzvērtīga opcijai **Visi projekta uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="0a6a2-139">Projekta lapā atlasot **Tikai atlas‪ītie projekta uzdevumi**, cilnē **Uzdevuma norēķinu iestatīšana** varat atlasīt noteiktus uzdevumus, lai tos saistītu ar šo piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="0a6a2-140">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-141">Iekļaut laiku</span><span class="sxs-lookup"><span data-stu-id="0a6a2-141">Include Time</span></span> | <span data-ttu-id="0a6a2-142">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā laika transakcijas vai darbaspēka izmaksas tiks iekļautas šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0a6a2-143">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0a6a2-144">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļauti laika darījumi vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0a6a2-145">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-146">Iekļaut izdevumus</span><span class="sxs-lookup"><span data-stu-id="0a6a2-146">Include Expense</span></span> | <span data-ttu-id="0a6a2-147">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā izdevumi tiks iekļauti šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0a6a2-148">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0a6a2-149">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0a6a2-150">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-151">Iekļaut materiālu</span><span class="sxs-lookup"><span data-stu-id="0a6a2-151">Include Material</span></span> | <span data-ttu-id="0a6a2-152">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā materiālu izmaksas tiks iekļautas šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0a6a2-153">Vērtība **Nē** norāda, ka atlasītajā projektā materiālu izmaksas netiks iekļautas šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0a6a2-154">Vērtība **Jā** norāda, ka atlasītajā projektā materiālu izmaksas tiks iekļautas šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0a6a2-155">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-156">Iekļaut maksu</span><span class="sxs-lookup"><span data-stu-id="0a6a2-156">Include Fee</span></span> | <span data-ttu-id="0a6a2-157">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā maksas tiks iekļautas šīs piedāvājuma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0a6a2-158">Vērtība **Nē** norāda, ka šīs piedāvājuma rindas aprēķinā netiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0a6a2-159">Vērtība **Jā** norāda, ka šīs piedāvājuma rindas aprēķinā tiks iekļautas maksas.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0a6a2-160">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-161">Minētā summa</span><span class="sxs-lookup"><span data-stu-id="0a6a2-161">Quoted Amount</span></span> | <span data-ttu-id="0a6a2-162">Šī ir summa, kas klientam tiks piedāvāta par visu šajā projekta piedāvājuma rindā prognozēto darbu.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="0a6a2-163">No iespējas izveidotam piedāvājumam šī vērtība tiek kopēta no lauka **Klienta budžets** iespējas rindā.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="0a6a2-164">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu summas.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="0a6a2-165">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-166">Aprēķinātais nodoklis</span><span class="sxs-lookup"><span data-stu-id="0a6a2-166">Estimated Tax</span></span> | <span data-ttu-id="0a6a2-167">Tas ir rediģējams lauks, kas lietotājam ļauj pievienot paredzamo nodokļu summu piedāvājuma rindai.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="0a6a2-168">Ja projekta piedāvājuma rindā ir rindas detaļas, šis lauks tiek slēgts rediģēšanai un tiek apkopots no piedāvājuma rindas detaļu nodokļu summas.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="0a6a2-169">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-170">Piedāvātā summa pēc nodokļa atskaitīšanas</span><span class="sxs-lookup"><span data-stu-id="0a6a2-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="0a6a2-171">Šis lauks ir piedāvājuma rindas summa pēc nodokļiem un ir tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="0a6a2-172">Summu šajā laukā aprēķina kā *Piedāvātā summa + Nodokļi*.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="0a6a2-173">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-174">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="0a6a2-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="0a6a2-175">Šo lauku var rediģēt, un tas ir pieejams tikai projekta piedāvājuma rindās, kurām ir norēķinu metode **Laiks un materiāli**.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="0a6a2-176">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0a6a2-177">Klienta budžets</span><span class="sxs-lookup"><span data-stu-id="0a6a2-177">Customer Budget</span></span> | <span data-ttu-id="0a6a2-178">Šis lauks ir rediģējams un tiek kopēts no atbilstošā lauka iespēju rindā, ja piedāvājums tika izveidots no iespējas.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="0a6a2-179">Šī vērtība tiek iekopēta projekta līguma rindā, kas tiek izveidota no šīs piedāvājuma rindas, kad piedāvājums ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="0a6a2-180">Validācijas kārtulas laukiem projekta piedāvājumu rindu cilnē Vispārīgi</span><span class="sxs-lookup"><span data-stu-id="0a6a2-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="0a6a2-181">**1. kārtula**: ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi**, projekts tiek iekļauts piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="0a6a2-182">**2. kārtula**: ja lauks **Iekļautie uzdevumi** ir tukšs vai ir iestatīts uz **Visi projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut tikai vienā projekta piedāvājuma rindā.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="0a6a2-183">**3. kārtula**: ja lauks **Iekļautie uzdevumi** ir ir iestatīts uz **Tikai atlasītie projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut vairākās projekta piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="0a6a2-184">**4. kārtula**: ja iespējai ir vairāki piedāvājumi, var būt pieejamas piedāvājumu rindas no dažādiem piedāvājumiem, kas visi attiecas uz vienu un to pašu projektu un ietver to pašu transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="0a6a2-185">**5. kārtula**: ja piedāvājumi nepieder vienai un tai pašai iespējai, tie nevar ietvert to pašu projektu un transakciju klasi.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="0a6a2-186">
                    <strong>Iespēja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="0a6a2-187">
                    <strong>Piedāvājums</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="0a6a2-188">
                    <strong>Piedāvājuma rinda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="0a6a2-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="0a6a2-190">
                    <strong>Iekļautie uzdevumi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="0a6a2-191">
                    <strong>Iekļaut laiku</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="0a6a2-192">
                    <strong>Iekļaut izdevumus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="0a6a2-193">
                    <strong>Iekļaut materiālu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="0a6a2-194">
                    <strong>Iekļaut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="0a6a2-195">
                    <strong>Maksa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="0a6a2-196">
                    <strong>Derīgs/Nav derīgs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="0a6a2-197">
                    <strong>Iemesls</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0a6a2-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="0a6a2-198">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-199">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-200">QL1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-201">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-202">Tukša</span><span class="sxs-lookup"><span data-stu-id="0a6a2-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-203">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-204">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-205">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-206">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-207">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-208">2. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-208">Violation of Rule #2.</span></span> <span data-ttu-id="0a6a2-209">Laiks, izdevumi un maksas P1 projektā ir ietvertas piedāvājuma rindā QL1 un QL2.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="0a6a2-210">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-211">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-212">QL2</span><span class="sxs-lookup"><span data-stu-id="0a6a2-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-213">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-214">Tukša</span><span class="sxs-lookup"><span data-stu-id="0a6a2-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-215">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-216">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-217">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-218">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-218">Yes</span></span> </p>
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
<span data-ttu-id="0a6a2-219">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-220">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-221">QL1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-222">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-223">Tukša</span><span class="sxs-lookup"><span data-stu-id="0a6a2-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-224">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-225">Nr.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-226">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-227">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-228">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-229">2. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-229">Violation of Rule #2.</span></span> <span data-ttu-id="0a6a2-230">Laiks, materiāli un maksas P1 projektā ir ietvertas piedāvājuma rindā QL1 un QL2.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="0a6a2-231">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-232">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-233">QL2</span><span class="sxs-lookup"><span data-stu-id="0a6a2-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-234">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-235">Tukša</span><span class="sxs-lookup"><span data-stu-id="0a6a2-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-236">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-237">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-238">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-239">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-239">Yes</span></span> </p>
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
<span data-ttu-id="0a6a2-240">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-241">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-242">QL1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-243">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-244">Tukša</span><span class="sxs-lookup"><span data-stu-id="0a6a2-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-245">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-246">Nr.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-247">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-248">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-249">Derīgs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-250">Laiks, materiāli un maksas P1 projektā ir ietvertas rindā QL1.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="0a6a2-251">Izdevumi P1 projektā ir ietverti rindā QL2.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="0a6a2-252">Latrā piedāvājuma rindā ietvertās vērtības nepārklājas, tāpēc ir derīgas.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="0a6a2-253">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-254">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-255">QL2</span><span class="sxs-lookup"><span data-stu-id="0a6a2-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-256">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-257">Tukša</span><span class="sxs-lookup"><span data-stu-id="0a6a2-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-258">Nr.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-259">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-260">Nr.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-261">Nr.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-261">No</span></span> </p>
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
<span data-ttu-id="0a6a2-262">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-263">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-264">QL1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-265">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-266">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="0a6a2-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-267">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-268">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-269">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-270">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-271">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-272">2. kārtulas pārkāpums</span><span class="sxs-lookup"><span data-stu-id="0a6a2-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="0a6a2-273">Q1 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai</span><span class="sxs-lookup"><span data-stu-id="0a6a2-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="0a6a2-274">QL2 ietver laiku, izdevumus un maksas par visu projektu P1 un tāpēc pārklājas ar to, kas ir iekļauts Q1.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="0a6a2-275">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-276">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-277">QL2</span><span class="sxs-lookup"><span data-stu-id="0a6a2-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-278">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-279">Tukša</span><span class="sxs-lookup"><span data-stu-id="0a6a2-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-280">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-281">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-282">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-283">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-283">Yes</span></span> </p>
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
<span data-ttu-id="0a6a2-284">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-285">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-286">QL1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-287">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-288">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="0a6a2-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-289">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-290">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-291">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-292">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-293">Derīgs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-294">Atbilstoši 3. kārtulai</span><span class="sxs-lookup"><span data-stu-id="0a6a2-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="0a6a2-295">Q1 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0a6a2-296">QL2 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0a6a2-297">Vienīgā papildu validācija attiecas uz QL1 uzdevumu apakškopu, kas atšķiras no QL2 uzdevumu apakškopas, lai nodrošinātu nepārklāšanos.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="0a6a2-298">To veic sistēma, kad tiek saistīti uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="0a6a2-299">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-300">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-301">QL2</span><span class="sxs-lookup"><span data-stu-id="0a6a2-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-302">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-303">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="0a6a2-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-304">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-305">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-306">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-307">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-307">Yes</span></span> </p>
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
<span data-ttu-id="0a6a2-308">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-309">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-310">QL1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-311">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-312">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-313">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-314">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-315">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-316">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-317">Derīgs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-318">Atbilstoši 5. kārtulai Q1 un Q2 ir divi piedāvājumi par vienu un to pašu iespēju, tādēļ abi tie var novērtēt vienu un to pašu projekta komponentu.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="0a6a2-319">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-320">2. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-321">QL1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-322">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-323">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-324">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-325">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-326">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-327">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-327">Yes</span></span> </p>
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
<span data-ttu-id="0a6a2-328">O1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-329">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-330">QL1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-331">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-332">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-333">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-334">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-335">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-336">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-337">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0a6a2-338">Atbilstoši 4. kārtulai Q1 un Q2 ir divi piedāvājumi par atšķirīgām iespējām, tādēļ abi tie nevar novērtēt vienu un to pašu projekta komponentu.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="0a6a2-339">O2</span><span class="sxs-lookup"><span data-stu-id="0a6a2-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="0a6a2-340">1. cet.</span><span class="sxs-lookup"><span data-stu-id="0a6a2-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="0a6a2-341">QL1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-342">P1</span><span class="sxs-lookup"><span data-stu-id="0a6a2-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="0a6a2-343">Visi projekta uzdevumi vai tukšs</span><span class="sxs-lookup"><span data-stu-id="0a6a2-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="0a6a2-344">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="0a6a2-345">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0a6a2-346">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0a6a2-347">Jā</span><span class="sxs-lookup"><span data-stu-id="0a6a2-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
