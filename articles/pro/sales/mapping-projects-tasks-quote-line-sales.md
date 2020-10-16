---
title: Projektu un uzdevumu kartēšana par projekta piedāvājuma rindu
description: Šajā tēmā ir sniegta informācija par to, kā kartēt projektus un uzdevumus uz projekta uzdevuma rindu.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 6b396ccf5e76230a42a2f933a3aaa5b8149790bb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/06/2020
ms.locfileid: "3964916"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="b1262-103">Projektu un uzdevumu kartēšana par projekta piedāvājuma rindu</span><span class="sxs-lookup"><span data-stu-id="b1262-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="b1262-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="b1262-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b1262-105">Projekta piedāvājumu rindās var kartēt tāda projekta specifiskos uzdevumus, kas jau ir saistīts ar piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="b1262-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="b1262-106">Kartējot uzdevumus uz piedāvājuma rindu, tālāk minētie vienumi, kas tika definēti piedāvājuma rindā, tiek lietoti tikai šiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="b1262-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="b1262-107">Rēķinu izrakstīšanas metode</span><span class="sxs-lookup"><span data-stu-id="b1262-107">Billing method</span></span>
- <span data-ttu-id="b1262-108">Maksas iekasēšanas opcijas</span><span class="sxs-lookup"><span data-stu-id="b1262-108">Chargeability options</span></span>
- <span data-ttu-id="b1262-109">Nepārsniedzamie ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="b1262-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="b1262-110">Klienti</span><span class="sxs-lookup"><span data-stu-id="b1262-110">Customers</span></span>

<span data-ttu-id="b1262-111">Piemēram, jums var būt projekts, kurā viena fāze ir fiksēta cena un visas pārējās fāzes ir laiks un materiāli.</span><span class="sxs-lookup"><span data-stu-id="b1262-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="b1262-112">Šajā gadījumā pirmo fāzi un visus tās pakārtotos uzdevumus var saistīt ar šīs fāzes piedāvājuma rindu ar fiksētas cenas norēķinu metodi.</span><span class="sxs-lookup"><span data-stu-id="b1262-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="b1262-113">Pēc tam var saistīt visas pārējās fāzes ar laika un materiālu piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="b1262-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="b1262-114">Uzdevumu saistīšana ar projekta piedāvājuma rindām</span><span class="sxs-lookup"><span data-stu-id="b1262-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="b1262-115">Uzdevumus var saistīt ar piedāvājuma rindām no tālāk minētajām atrašanās vietām.</span><span class="sxs-lookup"><span data-stu-id="b1262-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="b1262-116">Lapa **Projekts** > Cilne **Uzdevuma norēķini** (optimāli)</span><span class="sxs-lookup"><span data-stu-id="b1262-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="b1262-117">Lapa **Piedāvājuma rinda** > Cilne **Apmaksājamie uzdevumi**</span><span class="sxs-lookup"><span data-stu-id="b1262-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="b1262-118">No lapas Projekts</span><span class="sxs-lookup"><span data-stu-id="b1262-118">From the Project page</span></span>

<span data-ttu-id="b1262-119">Lapā **Projekts** tiek nodrošināta optimāla pieredze uzdevumu saistīšanai ar piedāvājuma rindām.</span><span class="sxs-lookup"><span data-stu-id="b1262-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="b1262-120">Šo lapu var izmantot, lai atlasītu vairākus uzdevumus un saistītu tos visus, kā arī to pakārtotos uzdevumus, ar atlasīto piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="b1262-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="b1262-121">Projekta piedāvājuma rindas cilnē **Vispārīgi** pārbaudiet, vai lauks **Projekts** ir aizpildīts.</span><span class="sxs-lookup"><span data-stu-id="b1262-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="b1262-122">Laukā **Iekļautie uzdevumi** atlasiet **Tikai atlasītie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="b1262-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="b1262-123">Saglabājiet projekta piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="b1262-123">Save the project-based quote line.</span></span> <span data-ttu-id="b1262-124">Kad veidlapa tiek atsvaidzināta, tiek parādīta cilne **Apmaksājamie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="b1262-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="b1262-125">Cilnē **Vispārīgi** atlasiet projekta saiti laukā **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="b1262-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="b1262-126">Lapā **Projekts** atlasiet cilni **Uzdevuma norēķini**.</span><span class="sxs-lookup"><span data-stu-id="b1262-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="b1262-127">Otrajā režģī, kas attiecas uz konkrētu uzdevumu norēķinu iestatīšanu, atlasiet vienu vai vairākus uzdevumus un pēc tam atlasiet **Saistīt piedāvājuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="b1262-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="b1262-128">Parādītajā dialoga lapā atlasiet piedāvājuma rindu, kurā ir redzamas piedāvājumā iekļautās projekta piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="b1262-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="b1262-129">Laukā **Norēķinu tips** norādiet, vai šie uzdevumi ir apmaksājami vai neapmaksājami.</span><span class="sxs-lookup"><span data-stu-id="b1262-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="b1262-130">Atzīmējiet izvēles rūtiņu, lai norādītu, vai saistībā ir jāiekļauj atlasīto uzdevumu pakārtotie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="b1262-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="b1262-131">Atzīmējot rūtiņu, atlasīto uzdevumu pakārotie uzdevumi tiek saistīti ar piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="b1262-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="b1262-132">Atlasiet **Labi**, lai aizvērtu dialogu.</span><span class="sxs-lookup"><span data-stu-id="b1262-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="b1262-133">No piedāvājuma rindas lapas</span><span class="sxs-lookup"><span data-stu-id="b1262-133">From the Quote line page</span></span>

<span data-ttu-id="b1262-134">Projekta uzdevumus var saistīt ar piedāvājuma rindām no cilnes **Apmaksājamie uzdevumi** lapā **Piedāvājuma rinda**.</span><span class="sxs-lookup"><span data-stu-id="b1262-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="b1262-135">Vislabākā vieta projekta uzdevumu saistīšanai ar piedāvājuma rindām ir cilnē **Uzdevuma norēķini** lapā **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="b1262-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="b1262-136">Ja uzdevumi tiek saistīti no cilnes **Apmaksājamie uzdevumi** lapā **Piedāvājuma rindas**, tad katrs projekts ir jāsaista manuāli.</span><span class="sxs-lookup"><span data-stu-id="b1262-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="b1262-137">Projekta piedāvājuma rindas cilnē **Vispārīgi** pārbaudiet, vai laukā **Projekts** ir atlasīts projekts.</span><span class="sxs-lookup"><span data-stu-id="b1262-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="b1262-138">Laukā **Iekļautie uzdevumi** atlasiet **Tikai atlasītie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="b1262-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="b1262-139">Saglabājiet projekta piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="b1262-139">Save the project-based quote line.</span></span> <span data-ttu-id="b1262-140">Kad veidlapa tiek atsvaidzināta, tiek parādīta cilne **Apmaksājamie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="b1262-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="b1262-141">Cilnē **Apmaksājamie uzdevumi** atlasiet **Pievienot piedāvājuma rindas uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="b1262-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="b1262-142">Lapas **Piedāvājuma rindas uzdevums** laukā **Uzdevumi** atlasiet uzdevumu un laukā **Norēķinu tips** atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b1262-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="b1262-143">Aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="b1262-143">Close the page.</span></span> <span data-ttu-id="b1262-144">Atlasītais uzdevums tagad ir saistīts ar piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="b1262-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="b1262-145">Uzdevumu atsaistīšana no projekta piedāvājuma rindām</span><span class="sxs-lookup"><span data-stu-id="b1262-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="b1262-146">No lapas Projekts</span><span class="sxs-lookup"><span data-stu-id="b1262-146">From the Project page</span></span>

<span data-ttu-id="b1262-147">Šī metode nodrošina efektīvāko veidu, kā atsaistīt uzdevumus no piedāvājuma rindām.</span><span class="sxs-lookup"><span data-stu-id="b1262-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="b1262-148">Var atlasīt vairākus uzdevumus un atsaistīt tos visus, kā arī to pakārtotos uzdevumus, no atlasītās piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="b1262-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="b1262-149">Projekta piedāvājuma rindas cilnes **Vispārīgi** laukā **Projekts** atlasiet projekta saiti.</span><span class="sxs-lookup"><span data-stu-id="b1262-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="b1262-150">Lapā **Projekts** atlasiet cilni **Uzdevuma norēķini**.</span><span class="sxs-lookup"><span data-stu-id="b1262-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="b1262-151">Otrajā režģī, kas attiecas uz konkrētu uzdevumu norēķinu iestatīšanu, atlasiet vienu vai vairākus uzdevumus un pēc tam atlasiet **Atsaistīt piedāvājuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="b1262-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="b1262-152">Parādītajā dialoga lapā atlasiet piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="b1262-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="b1262-153">Atzīmējiet izvēles rūtiņu, lai norādītu, vai saistība ir jāatceļ arī atlasīto uzdevumu pakārtotajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="b1262-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="b1262-154">Atzīmējot rūtiņu, atlasīto uzdevumu pakārotie uzdevumi tiek atsaistīti no piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="b1262-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="b1262-155">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b1262-155">Select **OK**.</span></span> <span data-ttu-id="b1262-156">Brīdinājuma ziņojums informē, ka, noņemot šo saistību, visi iepriekš ierakstītie faktiskie dati uzdevumā var tikt atcelti.</span><span class="sxs-lookup"><span data-stu-id="b1262-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="b1262-157">Noklikšķiniet **Labi**, lai turpinātu un noņemtu saistību starp uzdevumu un projekta piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="b1262-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="b1262-158">No piedāvājuma rindas lapas</span><span class="sxs-lookup"><span data-stu-id="b1262-158">From the Quote line page</span></span>

<span data-ttu-id="b1262-159">Projekta uzdevumus var arī atsaistīt no piedāvājuma rindām no cilnes **Apmaksājamie uzdevumi** lapā **Piedāvājuma rinda**.</span><span class="sxs-lookup"><span data-stu-id="b1262-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="b1262-160">Cilnē **Apmaksājamie uzdevumi** atlasiet **Dzēst piedāvājuma rindas uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="b1262-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="b1262-161">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b1262-161">Select **OK**.</span></span> <span data-ttu-id="b1262-162">Brīdinājuma ziņojums informē, ka, noņemot šo saistību, visi iepriekš ierakstītie faktiskie dati uzdevumā var tikt atcelti.</span><span class="sxs-lookup"><span data-stu-id="b1262-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="b1262-163">Noklikšķiniet **Labi**, lai turpinātu un noņemtu saistību starp uzdevumu un projekta piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="b1262-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="b1262-164">Šī procedūra nedzēš uzdevumu no projekta.</span><span class="sxs-lookup"><span data-stu-id="b1262-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="b1262-165">Tā tikai noņem uzdevuma saistību no projekta piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="b1262-165">It only removes the task association from the project-based quote line.</span></span>
