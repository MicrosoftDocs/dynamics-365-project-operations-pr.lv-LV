---
title: Kā es varu "viegli rezervēt" resursus programmas versijā 2.x?
description: Šajā rakstā ir izklāstīts, kā programmā Project Service viegli rezervēt projekta darba grupas dalībniekus.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 18a1176c131e233f62f74dc0dd8a6aa3ee561da5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286032"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="9d086-103">Kā viegli rezervēt resursus tīmekļa programmā (Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="9d086-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9d086-104">Varat eksperimentāli plānot vai viegli rezervēt resursu projekta darba grupai, lai parādītu, ka plānojat piešķirt resursu projektam.</span><span class="sxs-lookup"><span data-stu-id="9d086-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="9d086-105">Vieglās rezervācijas nepatērē resursa pieejamo noslodzi.</span><span class="sxs-lookup"><span data-stu-id="9d086-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="9d086-106">Darba grupas dalībniekus, kas ir viegli rezervēti, nevar piešķirt projekta uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="9d086-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="9d086-107">Tikai resursus ar statusu “Stingri rezervēts” un saistību tipu “Saistīts” var piešķirt uzdevumiem (pieņemot, ka resursam ir pietiekami daudz stingrās rezervācijas stundu, lai segtu piešķiršanu).</span><span class="sxs-lookup"><span data-stu-id="9d086-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="9d086-108">Viegli rezervētie projekta darba grupas dalībnieki tiek parādīti darba grupas dalībnieku režģī, bet viegli rezervētās stundas tiek rādītas kolonnā Vieglā rezervācija.</span><span class="sxs-lookup"><span data-stu-id="9d086-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="9d086-109">Tie parādās arī plānošanas panelī.</span><span class="sxs-lookup"><span data-stu-id="9d086-109">They also show up on the schedule board.</span></span> <span data-ttu-id="9d086-110">Tas nenorāda noslodzes patēriņu, jo vieglā rezervācija nepatērē resursa noslodzi.</span><span class="sxs-lookup"><span data-stu-id="9d086-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="9d086-111">Ir trīs veidi, kā viegli rezervēt darba grupas dalībnieku projektam programmā Project Service version 2.x.</span><span class="sxs-lookup"><span data-stu-id="9d086-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="9d086-112">Jūs varat veikt vieglo rezervāciju plānošanas panelī, izmantot līdzekli Uzturēt rezervācijas vai izveidot vispārēju resursu.</span><span class="sxs-lookup"><span data-stu-id="9d086-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="9d086-113">Šīs metodes ir aprakstītas tālāk.</span><span class="sxs-lookup"><span data-stu-id="9d086-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="9d086-114">Vieglā rezervēšana plānošanas panelī</span><span class="sxs-lookup"><span data-stu-id="9d086-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="9d086-115">Lai veiktu vieglo rezervēšanu plānošanas panelī, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="9d086-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="9d086-116">Atveriet plānošanas paneli.</span><span class="sxs-lookup"><span data-stu-id="9d086-116">Open the schedule board.</span></span>
2. <span data-ttu-id="9d086-117">Plānošanas paneļa rezervēšanas prasību paneļa apakšdaļā atlasiet cilni Projekts.</span><span class="sxs-lookup"><span data-stu-id="9d086-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="9d086-118">Atrodiet projektu, kuram vēlaties viegli rezervēt resursu.</span><span class="sxs-lookup"><span data-stu-id="9d086-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="9d086-119">Ja jums ir daudz projektu, noklikšķiniet uz kolonnas Projekts virsraksta un pēc tam lietojiet filtru, lai atrastu savu projektu.</span><span class="sxs-lookup"><span data-stu-id="9d086-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="9d086-120">Noklikšķiniet uz projekta, pēc tam velciet un nometiet to resursa laika režģī.</span><span class="sxs-lookup"><span data-stu-id="9d086-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="9d086-121">Labajā pusē tiek atvērts panelis Resursa rezervācijas izveide.</span><span class="sxs-lookup"><span data-stu-id="9d086-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="9d086-122">Pielāgojiet sākuma un beigu datumu, atlasiet rezervācijas statusu kā Viegls un iestatiet stundas.</span><span class="sxs-lookup"><span data-stu-id="9d086-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="9d086-123">Noklikšķiniet uz Rezervēt.</span><span class="sxs-lookup"><span data-stu-id="9d086-123">Click Book.</span></span>
7. <span data-ttu-id="9d086-124">Tagad projektā resurss tiks rādīts kā darba grupas dalībnieks ar viegli rezervētam stundām kolonnā Vieglā rezervācija.</span><span class="sxs-lookup"><span data-stu-id="9d086-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="9d086-125">Ņemiet vērā, ka nevarat piešķirt resursam uzdevumus darba sadalījuma struktūrā (WBS), jo resursiem ir jābūt stingri rezervētiem darba grupā, lai to varētu piešķirt.</span><span class="sxs-lookup"><span data-stu-id="9d086-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="9d086-126">Vieglā rezervēšana, izmantojot līdzekli Uzturēt rezervācijas</span><span class="sxs-lookup"><span data-stu-id="9d086-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="9d086-127">Lai veiktu vieglo rezervēšanu, izmantojot līdzekli Uzturēt rezervācijas, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="9d086-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="9d086-128">Darba grupas dalībnieku režģī noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9d086-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="9d086-129">Atlasiet rezervējamo resursu, lomu, sākuma/beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="9d086-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="9d086-130">Atlasiet sadalījuma metodi, kas nav Neviena:</span><span class="sxs-lookup"><span data-stu-id="9d086-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="9d086-131">Pilna noslodze</span><span class="sxs-lookup"><span data-stu-id="9d086-131">Full Capacity</span></span>
- <span data-ttu-id="9d086-132">Noslodzes procentuālā vērtība</span><span class="sxs-lookup"><span data-stu-id="9d086-132">Percentage Capacity</span></span>
- <span data-ttu-id="9d086-133">Sadalīt vienmērīgi pa stundām</span><span class="sxs-lookup"><span data-stu-id="9d086-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="9d086-134">Pa stundām — sākotnējā slodze</span><span class="sxs-lookup"><span data-stu-id="9d086-134">By Hours Front Load</span></span>
4. <span data-ttu-id="9d086-135">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9d086-135">Click Save.</span></span> <span data-ttu-id="9d086-136">Jūs redzēsit resursu darba grupas režģī un stundas, kas norādītas kā Stingras.</span><span class="sxs-lookup"><span data-stu-id="9d086-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="9d086-137">Uzturiet resursa rezervāciju, noklikšķinot uz Uzturēt rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="9d086-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="9d086-138">Kad tiek atvērts plānošanas panelis, izvērsiet resursu, lai parādītu tā rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="9d086-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="9d086-139">TIks parādīta rezervācija, kas norādīta kā Stingra.</span><span class="sxs-lookup"><span data-stu-id="9d086-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="9d086-140">Ar peles labo pogu noklikšķiniet uz rezervācijas, sadaļā Mainīt statusu atlasiet vienumu Vieglā rezervācija un pēc tam atlasiet Viegla.</span><span class="sxs-lookup"><span data-stu-id="9d086-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="9d086-141">Rezervācijas statuss tagad ir Viegla.</span><span class="sxs-lookup"><span data-stu-id="9d086-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="9d086-142">Pēc plānošanas paneļa aizvēršanas redzēsit, ka resursa stundas darba grupas dalībnieku režģī ir mainījušās no Stingra uz Viegla.</span><span class="sxs-lookup"><span data-stu-id="9d086-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="9d086-143">Ņemiet vērā, ka stingri rezervējot resursu darba grupā un pēc tam piešķirot uzdevumus WBS, ja izmantojat līdzekli Uzturēt rezervācijas, lai mainītu statusu no Stingra uz Viegla, šim resursam tiks noņemta uzdevumu piešķire, jo uzdevumiem var piešķirt tikai stingri rezervētos resursus.</span><span class="sxs-lookup"><span data-stu-id="9d086-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="9d086-144">Vieglā rezervācija, izveidojot vispārējo resursu</span><span class="sxs-lookup"><span data-stu-id="9d086-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="9d086-145">Vart izveidot vieglo rezervāciju, izveidojot vispārēju resursu darba grupas dalībnieku, aiizpildot plānošanas panelī vai resursu pieprasījumā un mainot veidu rezervācijas laikā.</span><span class="sxs-lookup"><span data-stu-id="9d086-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="9d086-146">Lai to paveiktu, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="9d086-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="9d086-147">Projekta WBS piešķiriet lomas uzdevumiem, kuriem vēlaties izveidot vispārējos darba grupas dalībiniekus.</span><span class="sxs-lookup"><span data-stu-id="9d086-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="9d086-148">Noklikšķiniet uz Izveidot projekta darba grupu.</span><span class="sxs-lookup"><span data-stu-id="9d086-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="9d086-149">Projekta darba grupas dalībnieku režģī atlasiet vispārējo resursu un noklikšķiniet uz Rezervēt.</span><span class="sxs-lookup"><span data-stu-id="9d086-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="9d086-150">Plānošanas panelī atlasiet resursu, kuru vēlaties rezervēt.</span><span class="sxs-lookup"><span data-stu-id="9d086-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="9d086-151">Plānošanas paneļa panelī Resursa rezervācijas izveide mainiet rezervācijas statusu uz Viegla.</span><span class="sxs-lookup"><span data-stu-id="9d086-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="9d086-152">Noklikšķiniet uz grāmatas Rezervēt un Iziet.</span><span class="sxs-lookup"><span data-stu-id="9d086-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="9d086-153">Pēc plānošanas paneļa aizvēršanas jūs redzēsiet atlasīto resursu pievienotu darba grupai ar viegli rezervētām stundas, kā arī piešķirtām stundām.</span><span class="sxs-lookup"><span data-stu-id="9d086-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="9d086-154">Turklāt tiks rādīts, ka vispārējais resurss paliek darba grupā, norādot, ka uzdevumi ir piešķirti viegli rezervētam darba grupas dalībniekam.</span><span class="sxs-lookup"><span data-stu-id="9d086-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="9d086-155">Kad esat gatavs mainīt izvēles viegli rezervēto darba grupas dalībnieka resursu uz stingri rezervētu darba grupas dalībnieku, lai tam varētu piešķirt uzdevumus, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="9d086-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="9d086-156">Atlasiet resursu un noklikšķiniet uz Uzturēt rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="9d086-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="9d086-157">Kad tiek atvērts plānošanas panelis, izvērsiet resursu, lai parādītu tā rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="9d086-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="9d086-158">Jūs redzēsiet rezervāciju atzīmētu kā Viegla.</span><span class="sxs-lookup"><span data-stu-id="9d086-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="9d086-159">Ar peles labo pogu noklikšķiniet uz rezervācijas, sadaļā Mainīt statusu atlasiet vienumu Stingrā rezervācija un pēc tam atlasiet Stingra.</span><span class="sxs-lookup"><span data-stu-id="9d086-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="9d086-160">Rezervācijas statuss tagad ir Stingra.</span><span class="sxs-lookup"><span data-stu-id="9d086-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="9d086-161">Pēc plānošanas paneļa aizvēršanas redzēsit, ka resursa stundas darba grupas dalībnieku režģī ir mainījušās no Viegla uz Stingra.</span><span class="sxs-lookup"><span data-stu-id="9d086-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="9d086-162">Tagad varat piešķirt resursam uzdevumus (ja piešķiršanai uzdevumam nav līdzinājuma starp stingri rezervētajām stundām un ieguldījuma stundām).</span><span class="sxs-lookup"><span data-stu-id="9d086-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="9d086-163">Ņemiet vērā: ja veicāt vispārējās resursu izpildes darbības iepriekš minētajā 3. punktā, mainot rezervējamā resursa, kurš ir viegli rezervēts, statusu uz Stingrs, vispārējais grupas dalībnieks tiek noņemts no darba grupas.</span><span class="sxs-lookup"><span data-stu-id="9d086-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]