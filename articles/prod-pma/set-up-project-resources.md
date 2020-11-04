---
title: Projekta resursu iestatīšana
description: Šajā tēmā sniegta informācija par projekta resursu iestatīšanu vai pieprasīšanu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080616"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="7c1c7-103">Projekta resursu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7c1c7-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c1c7-104">Ir jāiestata kalendārs un tas jāsaista ar darbinieku vai darba ņēmēju.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="7c1c7-105">Tiek izmantots kalendārs, lai ieplānotu projektu un projektam rezervēto resursu darba laiku.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="7c1c7-106">Kalendāra iestatīšanas laikā projekta vadītāji var resursu optimizācijas ietvaros veikt resursu pielāgošanu.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="7c1c7-107">Atkarībā no kalendāra grafika resursiem var piemērot ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="7c1c7-108">Kalendāru varat iestatīt lapā **Kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="7c1c7-109">Iestatot darba ņēmēju kā projekta resursu, varat izvēlēties no darba ņēmējiem, kuri strādā uzņēmumā, kuram iestatāt resursus.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="7c1c7-110">Vai arī varat atlasīt darba ņēmējus no citiem savas organizācijas uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="7c1c7-111">Šie darba ņēmēji ir pazīstami kā starpuzņēmumu resursi.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="7c1c7-112">Tālāk aprakstītajās procedūrās ir paskaidrots, kā jūsu uzņēmumā iestatīt darba ņēmēju kā projekta resursu un kā iestatīt starpuzņēmumu projekta resursu.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="7c1c7-113">Darba ņēmēja kā projekta resursa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7c1c7-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="7c1c7-114">Lapas **Darba ņēmēji** sarakstā **Darba ņēmēji** atlasiet darba ņēmēju, kuru pievienojat kā projekta resursu, un atveriet darba ņēmēja ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="7c1c7-115">Darbību rūtī atlasiet **Projekts**&gt; **Iestatīšana** &gt; **Projekta iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="7c1c7-116">Atlasiet kalendāru un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="7c1c7-117">Resursam noklusējuma projektus var arī norādīt kā iepriekšējas piešķiršanas tipu.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="7c1c7-118">Iepriekšējo piešķiri var izmantot, ja resursu pārvaldnieks vai projekta vadītājs iepriekš zina, ar kuriem resursiem projekts strādās.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="7c1c7-119">Iepriekšējo piešķiri var arī balstīt projekta sponsora vai klienta pieprasījumā.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="7c1c7-120">Lai iepriekš piešķirtu projektu, lapas **Piešķirt projektu** cilnes **Projekti** sarakstā **Atlikušie projekti** atlasiet atbilstošo projektu.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="7c1c7-121">Starpuzņēmumu resursa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7c1c7-121">Set up an intercompany resource</span></span>

<span data-ttu-id="7c1c7-122">Iestatot darba ņēmēju kā starpuzņēmumu resursu, iestatīšana ir jāizpilda gan gan patapinošajam uzņēmumam, gan uzņēmumam, kas aizņemas.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="7c1c7-123">Patapinošajā uzņēmumā</span><span class="sxs-lookup"><span data-stu-id="7c1c7-123">In the lending company</span></span>

1. <span data-ttu-id="7c1c7-124">Risinājumā Finance pārbaudiet, vai ir atlasīts patapinošais uzņēmums, un pēc tam izpildiet iepriekšējā sadaļā "Darba ņēmēja kā projekta resursa iestatīšana" aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="7c1c7-125">Lapā **Starpuzņēmumu uzskaite** atlasiet **Jauna**.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="7c1c7-126">Laukā **Juridiskās personas ID** atlasiet patapinošo uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="7c1c7-127">Atbilstoši aizpildiet atlikušos laukus un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="7c1c7-128">Lapā **Pārnest cenu** atlasiet **Jauna**.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="7c1c7-129">Laukā **Juridiskā persona, kas aizņemas** atlasiet atbilstošo uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="7c1c7-130">Lai patapinātu uzņēmumam, kas aizņemas, tikai to resursu, kuru izveidojāt šīs sadaļas sākumā, laukā **Resurss** atlasiet izveidotā resursa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="7c1c7-131">Lai uzņēmumam, kas aizņemas, varētu būt pieejami visi patapinošā uzņēmuma resursi, atstājiet lauku **Resurss** tukšu.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="7c1c7-132">Lapas **Projekta pārvaldības un uzskaites parametri** cilnē **Starpuzņēmumu** iestatiet opciju **Iespējot starpuzņēmumu resursu plānošanu un darba laika uzskaites tabulas** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="7c1c7-133">Uzņēmumā, kas aizņemas</span><span class="sxs-lookup"><span data-stu-id="7c1c7-133">In the borrowing company</span></span>

- <span data-ttu-id="7c1c7-134">Lapas **Resursu saraksts** meklēšanas filtrā ievadiet patapinošajam uzņēmumam izveidotā resursa nosaukumu, lai apstiprinātu, ka nosaukums tiek iekļauts uzņēmuma, kas aizņemas, resursu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="7c1c7-135">Projekta resursu pieprasīšana</span><span class="sxs-lookup"><span data-stu-id="7c1c7-135">Request project resources</span></span>
<span data-ttu-id="7c1c7-136">Projekta resursa plānošanas funkcionalitāte tikai ļauj resursu pārvaldniekiem izplatīt personāla resursus iesaistēm vai projektiem.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="7c1c7-137">Lai iespējotu šo funkcionalitāti, izpildiet tālāk norādītos uzdevumus vai pārbaudiet, vai tie ir izpildīti:</span><span class="sxs-lookup"><span data-stu-id="7c1c7-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="7c1c7-138">Iestatiet numuru secības.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-138">Set up number sequences.</span></span>
- <span data-ttu-id="7c1c7-139">Iestatiet projekta vadības un uzskaites darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="7c1c7-140">Iespējojiet resursa pieprasījumu darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-140">Enable resource request workflows.</span></span>

<span data-ttu-id="7c1c7-141">Pēc tam, kad ir izpildīti iepriekšējie uzdevumi, jūs varat pēc nepieciešamības izpildīt šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="7c1c7-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="7c1c7-142">Izveidot resursa pieprasījumu no vieglās rezervācijas resursa.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="7c1c7-143">Uzraudzīt resursu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-143">Monitor resource requests.</span></span>
- <span data-ttu-id="7c1c7-144">Izpildīt resursu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="7c1c7-145">Pieprasīt personāla resursu no WBS.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="7c1c7-146">Rezervēt resursus projektam bez personāla resursa pieprasīšanas.</span><span class="sxs-lookup"><span data-stu-id="7c1c7-146">Book resources to a project without having a request for a staffed resource.</span></span>
