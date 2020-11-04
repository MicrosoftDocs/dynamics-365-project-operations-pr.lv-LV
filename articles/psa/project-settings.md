---
title: Projekta iestatījumi
description: Šajā tēmā ir sniegta informācija par projekta pārvaldības iestatījumiem.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080607"
---
# <a name="project-settings"></a><span data-ttu-id="f60e0-103">Projekta iestatījumi</span><span class="sxs-lookup"><span data-stu-id="f60e0-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f60e0-104">Lai piekļūtu projekta plānošanas līdzekļiem, izmantojiet tālāk norādītos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="f60e0-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="f60e0-105">Darba veidne</span><span class="sxs-lookup"><span data-stu-id="f60e0-105">Work template</span></span>

<span data-ttu-id="f60e0-106">Lai izveidotu projekta grafiku, jums ir jāizveido projekta kalendāra veidne, kas nosaka darba stundu skaitu vienā dienā un visus uzņēmuma slēgšanas gadījumus.</span><span class="sxs-lookup"><span data-stu-id="f60e0-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="f60e0-107">Lai izveidotu projekta kalendāra veidni, jums ir jāsasaista darba veidne un lauks **Kalendāra veidne** šim projektam.</span><span class="sxs-lookup"><span data-stu-id="f60e0-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="f60e0-108">Lai izveidotu darba veidni, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f60e0-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="f60e0-109">Programmatūras PSA kreisajā navigācijas rūtī noklikšķiniet uz **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="f60e0-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="f60e0-110">Saraksta lapā **Resursi** atveriet lietotāja ierakstu un pēc tam atlasiet vienumu **Rādīt darba stundas**.</span><span class="sxs-lookup"><span data-stu-id="f60e0-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f60e0-111">Pārliecinieties, ka pārlūkprogrammas lapā ir atļauti uznirstošie elementi.</span><span class="sxs-lookup"><span data-stu-id="f60e0-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="f60e0-112">Šādi jūs varat apskatīt attiecīgajam resursam iestatītās darba stundas.</span><span class="sxs-lookup"><span data-stu-id="f60e0-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="f60e0-113">Cilnē **Mēneša skats** noklikšķiniet uz **Iestatīt**.</span><span class="sxs-lookup"><span data-stu-id="f60e0-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="f60e0-114">Tiek parādīts saraksts ar trīs opcijām:</span><span class="sxs-lookup"><span data-stu-id="f60e0-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="f60e0-115">Jauns nedēļas grafiks</span><span class="sxs-lookup"><span data-stu-id="f60e0-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="f60e0-116">Darba grafiks vienai dienai</span><span class="sxs-lookup"><span data-stu-id="f60e0-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="f60e0-117">Brīvais laiks</span><span class="sxs-lookup"><span data-stu-id="f60e0-117">Time Off</span></span>

> ![Iestatīšanas opcijas](media/project-13.png)

4. <span data-ttu-id="f60e0-119">Atlasiet **Jauns nedēļas grafiks** un pēc tam iestatiet opcijas šī resursa grafikam.</span><span class="sxs-lookup"><span data-stu-id="f60e0-119">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="f60e0-120">Varat iestatīt periodisku nedēļas grafiku, dienas stundu parametrus, uzņēmuma slēgšanas gadījumus un citus rādītājus.</span><span class="sxs-lookup"><span data-stu-id="f60e0-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="f60e0-121">Iestatiet datumu diapazonu, atlasiet **Saglabāt** un pēc tam noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="f60e0-121">Set the date range, select **Save** , and then click **Close**.</span></span> 
6. <span data-ttu-id="f60e0-122">Atgriezieties saraksta lapā **Resursi** un atlasiet resursu, kuram iestatījāt darba stundas.</span><span class="sxs-lookup"><span data-stu-id="f60e0-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="f60e0-123">Atlasiet **Iestatīt kalendāru kā** , lai iestatītu darba veidni.</span><span class="sxs-lookup"><span data-stu-id="f60e0-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="f60e0-124">Dialoglodziņā **Darba veidne** ievadiet nosaukumu šai darba veidnei un pēc tam atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="f60e0-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="f60e0-125">Tagad šo darba veidni varat sasaistīt ar projekta kalendāra veidni.</span><span class="sxs-lookup"><span data-stu-id="f60e0-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="f60e0-126">Resursu lomas</span><span class="sxs-lookup"><span data-stu-id="f60e0-126">Resource roles</span></span>

<span data-ttu-id="f60e0-127">Termins *resursa loma* attiecas uz prasmju, kompetenču un sertifikāciju kopu, kas personai ir nepieciešams, lai projektā varētu veikt noteiktu uzdevumu kopu.</span><span class="sxs-lookup"><span data-stu-id="f60e0-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="f60e0-128">Programmatūra PSA ļauj jums noteikt izmaksas un norēķinus resursa laikam, pamatojoties uz lomu, ar kādu šis resurss ir saistīts.</span><span class="sxs-lookup"><span data-stu-id="f60e0-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="f60e0-129">Katrai organizācijai ir jāiestata šīs lomas, izmantojot kreiso navigāciju izvēlnē **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="f60e0-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="f60e0-130">Katrai organizācijai šīs lomas ir jāiestata lapā **Aktīvās resursu kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="f60e0-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="f60e0-131">Lai atvērtu šo lapu, kreisajā navigācijas rūtī atlasiet **Resurss lomas**.</span><span class="sxs-lookup"><span data-stu-id="f60e0-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="f60e0-132">Cenrāži</span><span class="sxs-lookup"><span data-stu-id="f60e0-132">Price lists</span></span>

<span data-ttu-id="f60e0-133">Cenrāži ļauj jums iestatīt izmaksas un pārdošanas cenas resursu lomām, izmaksu kategorijām, produktiem un citiem elementiem kādā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="f60e0-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="f60e0-134">Pirms iestatāt finanšu tāmes darbam, kurš ir jāizpilda kādam projektam, jums ir jāizveido dublējuma izmaksu un pārdošanas cenrādis.</span><span class="sxs-lookup"><span data-stu-id="f60e0-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="f60e0-135">Parametru sadaļā jums ir jāiestata arī noklusējuma izmaksu un pārdošanas cenrādis, kas attiecas uz visiem šajā organizācijā izveidotajiem projektiem.</span><span class="sxs-lookup"><span data-stu-id="f60e0-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="f60e0-136">Lapā **Aktīvie projektu parametri** pārliecinieties, ka iestatāt noklusējuma izmaksu un pārdošanas cenrādi.</span><span class="sxs-lookup"><span data-stu-id="f60e0-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
