---
title: Projekta balstīta līguma rindu pārskats
description: Šajā tēmā ir sniegta informācija par darbu ar projekta līguma rindām.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369925"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="50511-103">Projekta balstīta līguma rindu pārskats</span><span class="sxs-lookup"><span data-stu-id="50511-103">Project-based contract lines overview</span></span>

<span data-ttu-id="50511-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="50511-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="50511-105">Projekta līguma rindas risinājumā Dynamics 365 Project Operations ir izstrādātas, lai ietvertu budžeta un norēķinu līgumus noteiktiem projekta darba komponentiem saistībā ar dalību.</span><span class="sxs-lookup"><span data-stu-id="50511-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="50511-106">Līguma rinda, kuras pamatā ir projekts, tiek paplašināta projekta aplēsēm un norēķinu scenārijiem, izmantojot tālāk norādītos jēdzienus.</span><span class="sxs-lookup"><span data-stu-id="50511-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="50511-107">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="50511-107">Billing method</span></span>
- <span data-ttu-id="50511-108">Projektu un uzdevumu kartēšana</span><span class="sxs-lookup"><span data-stu-id="50511-108">Project and task mapping</span></span>
- <span data-ttu-id="50511-109">Iekļautās transakciju klases</span><span class="sxs-lookup"><span data-stu-id="50511-109">Included transaction classes</span></span>
- <span data-ttu-id="50511-110">Nepārsniedzamais ierobežojums</span><span class="sxs-lookup"><span data-stu-id="50511-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="50511-111">Iekasēšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="50511-111">Chargeability setup</span></span>
- <span data-ttu-id="50511-112">Novērtējumi, izmantojot līgumu rindu informāciju</span><span class="sxs-lookup"><span data-stu-id="50511-112">Estimates using contract line details</span></span>
- <span data-ttu-id="50511-113">Līguma rindas klients</span><span class="sxs-lookup"><span data-stu-id="50511-113">Contract line customers</span></span>

<span data-ttu-id="50511-114">Tālāk sniegtajā tabulā ir iekļauti lauki, kas atrodas projekta līguma rindas cilnē **Vispārīgi**, kas palīdz izveidot pamatu detalizētam, pilnīgi jaunam novērtējumam un rēķinu izrakstīšanas nosacījumiem ar projektu saistītam darbam.</span><span class="sxs-lookup"><span data-stu-id="50511-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="50511-115">Lauks</span><span class="sxs-lookup"><span data-stu-id="50511-115">Field</span></span> | <span data-ttu-id="50511-116">Apraksts</span><span class="sxs-lookup"><span data-stu-id="50511-116">Description</span></span> | <span data-ttu-id="50511-117">Lejupstraumes ietekme</span><span class="sxs-lookup"><span data-stu-id="50511-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="50511-118">**Nosaukums**</span><span class="sxs-lookup"><span data-stu-id="50511-118">**Name**</span></span> | <span data-ttu-id="50511-119">Līguma rindas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="50511-119">Name of the contract line.</span></span> <span data-ttu-id="50511-120">Tas identificē līguma diskrēto komponentu, kas tiek novērtēts.</span><span class="sxs-lookup"><span data-stu-id="50511-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="50511-121">No piedāvājuma izveidotam projekta līgumam šī vērtība tiek kopēta no atbilstošās projekta piedāvājuma rindas vērtības.</span><span class="sxs-lookup"><span data-stu-id="50511-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="50511-122">Nosaukums, kas tiek kopēts uz to projekta rēķina rindu, kura tiek izveidota no šīs līguma rindas, kad tiek izveidots rēķins.</span><span class="sxs-lookup"><span data-stu-id="50511-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="50511-123">**Rēķinu izrakstīšanas metode**</span><span class="sxs-lookup"><span data-stu-id="50511-123">**Billing Method**</span></span> | <span data-ttu-id="50511-124">No piedāvājuma izveidotam projekta līgumam šī vērtība tiek kopēta no atbilstošā piedāvājuma rindas lauka.</span><span class="sxs-lookup"><span data-stu-id="50511-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="50511-125">Tā ir opciju kopa, kas pārstāv divus galvenos līguma modeļus, ko atbalsta Project Operations:</span><span class="sxs-lookup"><span data-stu-id="50511-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="50511-126">- **Fiksēta cena**</span><span class="sxs-lookup"><span data-stu-id="50511-126">- **Fixed Price**</span></span></br><span data-ttu-id="50511-127">- **Laiks un materiāls**</span><span class="sxs-lookup"><span data-stu-id="50511-127">- **Time and Material**</span></span> | <span data-ttu-id="50511-128">Par pamatu izmantojot atsauces līguma rindas norēķinu metodi, tiek veikta faktiskā darbība.</span><span class="sxs-lookup"><span data-stu-id="50511-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="50511-129">Ja līguma rindai, kurai ir atsauce uz faktisko, ir iestatīts laiks un materiālu norēķinu metode, tiek izveidoti izmaksu un rēķinā neiekļauto pārdošanas darījumu faktiskie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="50511-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="50511-130">Ja līguma rindai, kurai ir atsauce uz faktisko, ir fiksētas cenas norēķinu metode, tiek izveidota tikai izmaksu faktiskā summa.</span><span class="sxs-lookup"><span data-stu-id="50511-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="50511-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="50511-131">**Project**</span></span> | <span data-ttu-id="50511-132">Izmantojiet šo lauku, lai norādītu projektu, kas tiks izmantots, lai nodrošinātu darbu šajā piesaistē.</span><span class="sxs-lookup"><span data-stu-id="50511-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="50511-133">Šī vērtība tiks izmantota saistībā ar **ietvertajiem uzdevumiem** un **ietvertajām transakciju klasēm**, lai atrisinātu līguma rindas atsauci uz faktisko vai aprēķināto rindas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="50511-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="50511-134">**Iekļautie uzdevumi**</span><span class="sxs-lookup"><span data-stu-id="50511-134">**Included Tasks**</span></span> | <span data-ttu-id="50511-135">Norāda, vai šajā līguma rindā ir iekļauti visi atlasītā projekta paredzētie projekta uzdevumi vai tikai uzdevumu apakškopa.</span><span class="sxs-lookup"><span data-stu-id="50511-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="50511-136">Tā ir opciju kopa ar tālāk norādītajām iespējamajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="50511-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="50511-137">- **Visi projekta uzdevumi**</span><span class="sxs-lookup"><span data-stu-id="50511-137">- **All Project Tasks**</span></span></br><span data-ttu-id="50511-138">- **Tikai atlasītie projekta uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="50511-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="50511-139">Tukša vērtība šajā laukā ir vienāda ar atlasi **Visi projekta uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="50511-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="50511-140">Ja ir atlasīts vienums **Tikai atlasītie uzdevumi**, varat atlasīt noteiktus uzdevumus un tos saistīt ar šo līguma rindu lapas **Projekts** cilnē **Uzdevumu norēķinu iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="50511-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="50511-141">Šī vērtība tiks izmantota savienojumā ar **Projektu** un **Iekļautajām transakciju klasēm**, lai atrisinātu līguma rindas atsauci faktiskajā vai novērtējuma rindas ierakstā.</span><span class="sxs-lookup"><span data-stu-id="50511-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="50511-142">**Iekļaut laiku**</span><span class="sxs-lookup"><span data-stu-id="50511-142">**Include Time**</span></span> | <span data-ttu-id="50511-143">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā laika transakcijas vai darbaspēka izmaksas tiks iekļautas šīs līguma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="50511-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="50511-144">Vērtība **Nē** norāda, ka šajā līguma rindā netiks iekļautas laika transakcijas vai darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="50511-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="50511-145">Vērtība **Jā** norāda, ka tās tiks iekļautas.</span><span class="sxs-lookup"><span data-stu-id="50511-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="50511-146">Šī vērtība tiek izmantota saistībā ar projektu, lai atrisinātu līguma rindas atsauci uz faktisko vai aprēķināto rindas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="50511-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="50511-147">**Iekļaut izdevumus**</span><span class="sxs-lookup"><span data-stu-id="50511-147">**Include Expense**</span></span> | <span data-ttu-id="50511-148">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā izdevumi tiks iekļauti šīs līguma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="50511-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="50511-149">Vērtība **Nē** norāda, ka šajā līguma rindā netiks iekļautas izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="50511-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="50511-150">Vērtība **Jā** norāda, ka tās tiks iekļautas.</span><span class="sxs-lookup"><span data-stu-id="50511-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="50511-151">Šī vērtība tiek izmantota saistībā ar projektu, lai atrisinātu līguma rindas atsauci uz faktisko vai aprēķināto rindas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="50511-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="50511-152">**Iekļaut materiālus**</span><span class="sxs-lookup"><span data-stu-id="50511-152">**Include Materials**</span></span> | <span data-ttu-id="50511-153">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā materiāli tiks iekļauti šīs līguma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="50511-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="50511-154">Vērtība **Nē** norāda, ka atlasītajā projektā materiālu izmaksas netiks iekļautas šīs līguma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="50511-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="50511-155">Vērtība **Jā** norāda, ka tās tiks iekļautas.</span><span class="sxs-lookup"><span data-stu-id="50511-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="50511-156">Šī vērtība tiek izmantota saistībā ar projektu, lai atrisinātu līguma rindas atsauci uz faktisko vai aprēķināto rindas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="50511-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="50511-157">**Iekļaut maksu**</span><span class="sxs-lookup"><span data-stu-id="50511-157">**Include Fee**</span></span> | <span data-ttu-id="50511-158">Vērtība **Jā**/**Nē** norāda, vai atlasītajā projektā maksas tiks iekļauti šīs līguma rindas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="50511-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="50511-159">Vērtība **Nē** norāda, ka šajā līguma rindā netiks iekļautas papildmaksas.</span><span class="sxs-lookup"><span data-stu-id="50511-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="50511-160">Vērtība **Jā** norāda, ka tās tiks iekļautas.</span><span class="sxs-lookup"><span data-stu-id="50511-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="50511-161">Šī vērtība tiek izmantota saistībā ar projektu, lai atrisinātu līguma rindas atsauci uz faktisko vai aprēķināto rindas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="50511-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="50511-162">**Līgumā paredzētā summa**</span><span class="sxs-lookup"><span data-stu-id="50511-162">**Contracted Amount**</span></span> | <span data-ttu-id="50511-163">Fiksētas cenas līguma rindā šī summa ir vienošanās par vērtību, par kuru klientam tiks izrakstīts rēķins attiecībā uz visiem ar šo līguma rindu saistītajiem darba komponentiem.</span><span class="sxs-lookup"><span data-stu-id="50511-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="50511-164">Laika un materiāla līguma rindā šī summa ir aprēķināta vērtība, par kuru klientam tiks izrakstīts rēķins attiecībā uz visiem ar šo līguma rindu saistītajiem darba komponentiem.</span><span class="sxs-lookup"><span data-stu-id="50511-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="50511-165">No piedāvājuma izveidotam projekta līgumam šī vērtība tiek kopēta no atbilstošā piedāvājuma rindas lauka.</span><span class="sxs-lookup"><span data-stu-id="50511-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="50511-166">Ja projektā, kuras pamatā ir līguma rinda, ir rindu informācija, šis lauks ir slēgts rediģēšanai, un tas tiek apkopots no līguma rindas informācijas summas.</span><span class="sxs-lookup"><span data-stu-id="50511-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="50511-167">Ja līguma rindai ir rindas informācija, šo vērtību var modificēt, mainot summas rindu informācijā.</span><span class="sxs-lookup"><span data-stu-id="50511-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="50511-168">Fiksētas cenas līguma rindā šī vērtība tiek izmantota, lai par periodiskajiem norēķinu atskaites punktiem ģenerētu summu pirms nodokļu nomaksas.</span><span class="sxs-lookup"><span data-stu-id="50511-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="50511-169">**Aprēķinātais nodoklis**</span><span class="sxs-lookup"><span data-stu-id="50511-169">**Estimated Tax**</span></span> | <span data-ttu-id="50511-170">Lietotājs var rediģēt šo lauku, lai ievadītu prognozējamo nodokļu summu līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="50511-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="50511-171">Ja projektā, kuras pamatā ir līguma rinda, ir rindu informācija, šis lauks ir slēgts rediģēšanai, un tas tiek apkopots no līguma rindas informācijas nodokļu summas.</span><span class="sxs-lookup"><span data-stu-id="50511-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="50511-172">Ja līguma rindai ir rindas informācija, šo vērtību var modificēt, mainot nodokļu summas rindu informācijā.</span><span class="sxs-lookup"><span data-stu-id="50511-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="50511-173">Fiksētas cenas līguma rindā šī vērtība tiek izmantota, lai par periodiskajiem norēķinu atskaites punktiem ģenerētu nodokļus.</span><span class="sxs-lookup"><span data-stu-id="50511-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="50511-174">**Līgumā paredzētā summa pēc nodokļa atskaitīšanas**</span><span class="sxs-lookup"><span data-stu-id="50511-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="50511-175">Līguma rindas summa pēc nodokļa atskaitīšanas.</span><span class="sxs-lookup"><span data-stu-id="50511-175">The contract line amount after tax.</span></span> <span data-ttu-id="50511-176">Šis lauks ir tikai lasāms un aprēķināts kā **Līgumā paredzētā summa + nodoklis**.</span><span class="sxs-lookup"><span data-stu-id="50511-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="50511-177">Fiksētas cenas līguma rindā šī vērtība tiek izmantota, lai ģenerētu periodisko norēķinu atskaites punktus.</span><span class="sxs-lookup"><span data-stu-id="50511-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="50511-178">**Nepārsniedzamais ierobežojums**</span><span class="sxs-lookup"><span data-stu-id="50511-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="50511-179">Lietotājs var rediģēt šo lauku, un tas ir pieejams tikai projekta līguma rindās, kurās ir iestatīta laika un materiālu norēķinu metode.</span><span class="sxs-lookup"><span data-stu-id="50511-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="50511-180">Lietotājs var rediģēt šo lauku.</span><span class="sxs-lookup"><span data-stu-id="50511-180">The user can edit this field.</span></span> <span data-ttu-id="50511-181">Kad uz laiku un materiāliem attiecas šī līguma rinda, faktiskais laiks un materiāli norāda faktisko summu attiecībā pret nepārsniedzamo limitu līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="50511-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="50511-182">Šis novērtējums ir pabeigts pēc jau iztērēto un piešķirto summu uzskaites.</span><span class="sxs-lookup"><span data-stu-id="50511-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="50511-183">**Klienta budžets**</span><span class="sxs-lookup"><span data-stu-id="50511-183">**Customer Budget**</span></span> | <span data-ttu-id="50511-184">Ja līgums tika izveidots no piedāvājuma, šis lauks ir rediģējams un ir nokopēts no atbilstošā piedāvājuma rindas lauka.</span><span class="sxs-lookup"><span data-stu-id="50511-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="50511-185">Šis lauks tiek izmantots tikai informācijai, un tam nav pakārtotas nozīmes.</span><span class="sxs-lookup"><span data-stu-id="50511-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="50511-186">Validācijas kārtulas projekta līguma rindu cilnē Vispārīgi norādītajām opcijām</span><span class="sxs-lookup"><span data-stu-id="50511-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="50511-187">1. kārtula: ja lauks **Iekļautie uzdevumi** ir tukšs vai iestatīts kā **Visi projekta uzdevumi**, visi projekta uzdevumi tiek iekļauti līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="50511-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="50511-188">2. kārtula: kad lauks **Iekļautie uzdevumi** ir tukšs vai tieši iestatīts kā **Visiem projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut tikai vienā līguma projekta līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="50511-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="50511-189">3. kārtula: kad lauks **Iekļautie uzdevumi** ir iestatīts kā **Tikai atlasītie projekta uzdevumi**, projektu un noteiktu transakciju klasi var iekļaut vairākās līguma projekta līguma rindās.</span><span class="sxs-lookup"><span data-stu-id="50511-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="50511-190">
                    <strong>Līgums</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50511-191">
                    <strong>Līguma rinda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="50511-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="50511-193">
                    <strong>Iekļautie uzdevumi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="50511-194">
                    <strong>Iekļaut laiku</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="50511-195">
                    <strong>Iekļaut izdevumus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="50511-196">
                    <strong>Iekļaut materiālus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="50511-197">
                    <strong>Iekļaut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="50511-198">
                    <strong>Maksa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="50511-199">
                    <strong>Derīgs/Nav derīgs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="50511-200">
                    <strong>Iemesls</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50511-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="50511-201">C1</span><span class="sxs-lookup"><span data-stu-id="50511-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50511-202">CL1</span><span class="sxs-lookup"><span data-stu-id="50511-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-203">P1</span><span class="sxs-lookup"><span data-stu-id="50511-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="50511-204">Tukša</span><span class="sxs-lookup"><span data-stu-id="50511-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-205">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-206">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-207">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-208">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="50511-209">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="50511-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="50511-210">2. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="50511-210">Violation of Rule #2.</span></span> <span data-ttu-id="50511-211">Laiks, izdevumi un materiāli P1 projektā ir ietverti līguma rindā CL1 un CL2.</span><span class="sxs-lookup"><span data-stu-id="50511-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="50511-212">C1</span><span class="sxs-lookup"><span data-stu-id="50511-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50511-213">CL2</span><span class="sxs-lookup"><span data-stu-id="50511-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-214">P1</span><span class="sxs-lookup"><span data-stu-id="50511-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="50511-215">Tukša</span><span class="sxs-lookup"><span data-stu-id="50511-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-216">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-217">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-218">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-219">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="50511-220">C1</span><span class="sxs-lookup"><span data-stu-id="50511-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50511-221">CL1</span><span class="sxs-lookup"><span data-stu-id="50511-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-222">P1</span><span class="sxs-lookup"><span data-stu-id="50511-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="50511-223">Tukša</span><span class="sxs-lookup"><span data-stu-id="50511-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-224">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-225">Nr.</span><span class="sxs-lookup"><span data-stu-id="50511-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-226">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-227">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="50511-228">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="50511-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="50511-229">2. kārtulas pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="50511-229">Violation of Rule #2.</span></span> <span data-ttu-id="50511-230">Laiks, izdevumi un materiāli P1 projektā ir ietverti līguma rindā CL1 un CL2.</span><span class="sxs-lookup"><span data-stu-id="50511-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="50511-231">C1</span><span class="sxs-lookup"><span data-stu-id="50511-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50511-232">CL2</span><span class="sxs-lookup"><span data-stu-id="50511-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-233">P1</span><span class="sxs-lookup"><span data-stu-id="50511-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="50511-234">Tukša</span><span class="sxs-lookup"><span data-stu-id="50511-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-235">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-236">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-237">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-238">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="50511-239">C1</span><span class="sxs-lookup"><span data-stu-id="50511-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50511-240">CL1</span><span class="sxs-lookup"><span data-stu-id="50511-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-241">P1</span><span class="sxs-lookup"><span data-stu-id="50511-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="50511-242">Tukša</span><span class="sxs-lookup"><span data-stu-id="50511-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-243">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-244">Nr.</span><span class="sxs-lookup"><span data-stu-id="50511-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-245">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-246">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="50511-247">Derīgs</span><span class="sxs-lookup"><span data-stu-id="50511-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="50511-248">Laiks, materiāli un maksas P1 projektā ir ietvertas rindā CL1.</span><span class="sxs-lookup"><span data-stu-id="50511-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="50511-249">Izdevumi P1 projektā ir ietverti rindā CL2.</span><span class="sxs-lookup"><span data-stu-id="50511-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="50511-250">Latrā līguma rindā ietvertās vērtības nepārklājas, tāpēc ir derīgas.</span><span class="sxs-lookup"><span data-stu-id="50511-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="50511-251">C1</span><span class="sxs-lookup"><span data-stu-id="50511-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50511-252">CL2</span><span class="sxs-lookup"><span data-stu-id="50511-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-253">P1</span><span class="sxs-lookup"><span data-stu-id="50511-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="50511-254">Tukša</span><span class="sxs-lookup"><span data-stu-id="50511-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-255">Nr.</span><span class="sxs-lookup"><span data-stu-id="50511-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-256">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-257">Nr.</span><span class="sxs-lookup"><span data-stu-id="50511-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-258">Nr.</span><span class="sxs-lookup"><span data-stu-id="50511-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="50511-259">C1</span><span class="sxs-lookup"><span data-stu-id="50511-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50511-260">CL1</span><span class="sxs-lookup"><span data-stu-id="50511-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-261">P1</span><span class="sxs-lookup"><span data-stu-id="50511-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="50511-262">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="50511-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-263">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-264">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-265">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-266">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="50511-267">Nav derīgs</span><span class="sxs-lookup"><span data-stu-id="50511-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="50511-268">2. kārtulas pārkāpums</span><span class="sxs-lookup"><span data-stu-id="50511-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="50511-269">C1 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.</span><span class="sxs-lookup"><span data-stu-id="50511-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="50511-270">CL2 ietver laiku, materiālus, izdevumus un maksas par visu projektu P1 un tāpēc pārklājas ar to, kas ir iekļauts C1.</span><span class="sxs-lookup"><span data-stu-id="50511-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="50511-271">C1</span><span class="sxs-lookup"><span data-stu-id="50511-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50511-272">CL2</span><span class="sxs-lookup"><span data-stu-id="50511-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-273">P1</span><span class="sxs-lookup"><span data-stu-id="50511-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="50511-274">Tukša</span><span class="sxs-lookup"><span data-stu-id="50511-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-275">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-276">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-277">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-278">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="50511-279">C1</span><span class="sxs-lookup"><span data-stu-id="50511-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50511-280">CL1</span><span class="sxs-lookup"><span data-stu-id="50511-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-281">P1</span><span class="sxs-lookup"><span data-stu-id="50511-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="50511-282">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="50511-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-283">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-284">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-285">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-286">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="50511-287">Derīgs</span><span class="sxs-lookup"><span data-stu-id="50511-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="50511-288">Katrā kārtulā #3</span><span class="sxs-lookup"><span data-stu-id="50511-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="50511-289">C1 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.</span><span class="sxs-lookup"><span data-stu-id="50511-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="50511-290">CL2 ietver laiku, materiālus, izdevumus un maksas projekta P1 uzdevumu apakškopai.</span><span class="sxs-lookup"><span data-stu-id="50511-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="50511-291">Vienīgā papildu validācija attiecas uz CL1 uzdevumu apakškopu, kas atšķiras no CL2 uzdevumu apakškopas, lai nodrošinātu nepārklāšanos.</span><span class="sxs-lookup"><span data-stu-id="50511-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="50511-292">To veic sistēma, kad tiek saistīti uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="50511-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="50511-293">C1</span><span class="sxs-lookup"><span data-stu-id="50511-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50511-294">CL2</span><span class="sxs-lookup"><span data-stu-id="50511-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-295">P1</span><span class="sxs-lookup"><span data-stu-id="50511-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="50511-296">Tikai atlasītie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="50511-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-297">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="50511-298">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-299">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="50511-300">Jā</span><span class="sxs-lookup"><span data-stu-id="50511-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
