---
title: Izveidot jaunu projektu
description: Šajā tēmā ir sniegta informācija par to, kā izveidot jaunu projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270732"
---
# <a name="create-a-new-project"></a><span data-ttu-id="39a5a-103">Izveidot jaunu projektu</span><span class="sxs-lookup"><span data-stu-id="39a5a-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39a5a-104">Lai izveidotu jaunu projektu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="39a5a-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="39a5a-105">Lapā **Projektu pārvaldība** atlasiet **Jauns projekts** un ievadiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="39a5a-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="39a5a-106">**Projekta veids:** Laiks un materiāls</span><span class="sxs-lookup"><span data-stu-id="39a5a-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="39a5a-107">**Projekta nosaukums:** XYZ Jaunināšanas fāze 2</span><span class="sxs-lookup"><span data-stu-id="39a5a-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="39a5a-108">**Projekta grupa:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="39a5a-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="39a5a-109">**Projekta līguma ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="39a5a-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="39a5a-110">Atlasiet **Izveidot projektu**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="39a5a-111">Resursa piešķiršana projektam</span><span class="sxs-lookup"><span data-stu-id="39a5a-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="39a5a-112">Lapas **Darba ņēmēji** sarakstā **Darba ņēmēji** atlasiet darba ņēmēja ierakstu, kuram iepriekš iestatījāt kompetences, un atveriet darba ņēmēja ierakstu.</span><span class="sxs-lookup"><span data-stu-id="39a5a-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="39a5a-113">Darbību rūts cilnes **Projekts** grupā **Kompetences** atlasiet **Piešķirt projektus**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="39a5a-114">Lapas **Resursu validācijas projekta piešķire** cilnē **Projekti**, laukā **Pievienot projektu atlasītajiem projektiem** filtrējiet projektu **XYZ Jaunināšanas fāze 2**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="39a5a-115">Rūtī **Atlikušie projekti** atlasiet projektu un pēc tam atlasiet bulttaustiņu, lai to pievienotu rūtij **Atlasītie projekti**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="39a5a-116">Varat arī pēc nepieciešamības resursam piešķirt kategorijas.</span><span class="sxs-lookup"><span data-stu-id="39a5a-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="39a5a-117">Kategorijas veids ir vai nu **Izmaksas** vai **Ieņēmumi**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="39a5a-118">Kategorijas veidu nosaka jūsu organizācija.</span><span class="sxs-lookup"><span data-stu-id="39a5a-118">The category type is determined by your organization.</span></span> <span data-ttu-id="39a5a-119">Ja resursam netiek piešķirtas kategorijas, Finance uzmeklē noklusējuma kategoriju izmaksu un ieņēmumu stundu cenām.</span><span class="sxs-lookup"><span data-stu-id="39a5a-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="39a5a-120">Projekta resursu un lomu raksturlielumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="39a5a-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="39a5a-121">Projekta vadītājs var izmantot projekta resursu funkcionalitāti, lai izveidotu projektam nepieciešamās lomas.</span><span class="sxs-lookup"><span data-stu-id="39a5a-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="39a5a-122">Lomas var izmantot, ja apstiprinātie resursi joprojām nav zināmi, kad resursi tiek rezervēti.</span><span class="sxs-lookup"><span data-stu-id="39a5a-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="39a5a-123">Lomas var īslaicīgi rezervēt kā plānotos resursu, lai varat turpināt projekta plānošanas posmus.</span><span class="sxs-lookup"><span data-stu-id="39a5a-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="39a5a-124">[![Lomas piemērs](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="39a5a-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="39a5a-125">**Scenārijs:** Contoso nolīga, lai pabeigtu laika un materiālu projektu, kam ir apstiprināta projekta privilēģija.</span><span class="sxs-lookup"><span data-stu-id="39a5a-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="39a5a-126">Jaunākais projekta vadītājs joprojām izpilda projekta tvērumu.</span><span class="sxs-lookup"><span data-stu-id="39a5a-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="39a5a-127">Resursu pārvaldnieks pašlaik identificē konkrētus resursus, kuri tiks rezervēti darbam projektā.</span><span class="sxs-lookup"><span data-stu-id="39a5a-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="39a5a-128">Projekta būtiskā rakstura dēļ projekta sponsors pieprasīja Vecāko projekta pārvaldnieku kā vienu no lomām.</span><span class="sxs-lookup"><span data-stu-id="39a5a-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="39a5a-129">Resursu pārvaldniekam ir jāiegūst jaunais resurss un jādefinē loma sistēmā gadījumā, ja jaunākajam projekta pārvaldniekam projekta plānošanas laikā ir nepieciešama resursa informācija.</span><span class="sxs-lookup"><span data-stu-id="39a5a-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="39a5a-130">Tālāk minētajās darbībās parādīts, kā resursu pārvaldnieks var iestatīt vecākā projekta vadītāja lomu un ar to saistīt resursa raksturlielumus.</span><span class="sxs-lookup"><span data-stu-id="39a5a-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="39a5a-131">Pēc tam lomu var izmantot, lai meklētu pieejamos resursus, kuri atbilst nepieciešamajām resursu kompetencēm.</span><span class="sxs-lookup"><span data-stu-id="39a5a-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="39a5a-132">Lapā **Lomu iestatīšana** atlasiet **Jauna** un ievadiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="39a5a-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="39a5a-133">**Lomas ID:** Vecākais projekta vadītājs</span><span class="sxs-lookup"><span data-stu-id="39a5a-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="39a5a-134">**Apraksts:** Vecākais projekta vadītājs</span><span class="sxs-lookup"><span data-stu-id="39a5a-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="39a5a-135">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-135">Select **Create**.</span></span>
3. <span data-ttu-id="39a5a-136">Atlasiet lomu **Vecākais projekta vadītājs** un pēc tam atlasiet **Konfigurēt raksturlielumus**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="39a5a-137">Laukā **Raksturlielumu veids** atlasiet **Prasme**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="39a5a-138">Laukā **Pieejamie raksturlielumi** ievadiet meklējamo prasmi.</span><span class="sxs-lookup"><span data-stu-id="39a5a-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="39a5a-139">Laukā **Raksturlieluma veids** atlasiet **Sertifikāts**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="39a5a-140">Laukā **Pieejamie raksturlielumi** ievadiet meklējamo sertifikāta veidu.</span><span class="sxs-lookup"><span data-stu-id="39a5a-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="39a5a-141">Projekta resursa piešķiršana projektam</span><span class="sxs-lookup"><span data-stu-id="39a5a-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="39a5a-142">Lapā **Visi projekti** atlasiet projektu **XYZ Jaunināšanas fāze 2**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="39a5a-143">Cilnē **Projekta komanda un plānošana** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="39a5a-144">Laukā **Loma** atlasiet **Darba grupas dalībnieks**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="39a5a-145">Atlasiet **Rezervēt no kalendāra**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="39a5a-146">Lapā **Resursu pieejamība** atlasiet **Skatīt iestatījumus**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="39a5a-147">Lapā **Pielāgot skata iestatījumus** ievadiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="39a5a-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="39a5a-148">**Datu diapazona skata formāts:** Diena</span><span class="sxs-lookup"><span data-stu-id="39a5a-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="39a5a-149">**Rādīt pieejamības aprakstus:** Jā</span><span class="sxs-lookup"><span data-stu-id="39a5a-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="39a5a-150">**Rādīt atlikušo noslodzi:** Jā</span><span class="sxs-lookup"><span data-stu-id="39a5a-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="39a5a-151">Resursu sarakstā atlasiet resursu.</span><span class="sxs-lookup"><span data-stu-id="39a5a-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="39a5a-152">Atlasiet **Stingrā rezervācija** un **Pilnā noslodze**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="39a5a-153">Resursa piešķiršana noklusējuma lomai</span><span class="sxs-lookup"><span data-stu-id="39a5a-153">Assign a resource to a default role</span></span>

<span data-ttu-id="39a5a-154">Lai palīdzētu, projekta vai resursa pārvaldnieki var sīkāk skatīt resursus, kurus var rezervēt projektam.</span><span class="sxs-lookup"><span data-stu-id="39a5a-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="39a5a-155">Noklusējuma lomu varat saistīt ar esošu resursu vai nesen iegūtu resursu.</span><span class="sxs-lookup"><span data-stu-id="39a5a-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="39a5a-156">Piemēram, kad tika nolīgts Daniels, viņam bija pieredze un prasmes biznesa analītiķa lomas pildīšanai.</span><span class="sxs-lookup"><span data-stu-id="39a5a-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="39a5a-157">Resursu pārvaldnieks šo lomu piešķīra kā Daniela noklusējuma lomu.</span><span class="sxs-lookup"><span data-stu-id="39a5a-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="39a5a-158">Tāpēc resursu pārvaldnieks pievienoja Danielu to biznesa analītiķu kopai, kuri ir pieejami darbam ar projektiem.</span><span class="sxs-lookup"><span data-stu-id="39a5a-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="39a5a-159">Resursa rezervācijas laikā projektu pārvaldnieki var filtrēt darbam ar projektiem pieejamos lomu resursus.</span><span class="sxs-lookup"><span data-stu-id="39a5a-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="39a5a-160">Šo informāciju viņi var izmantot kā vienu kritēriju, resursu izpildes laikā veicot daudzkritēriju lēmumu analīzi.</span><span class="sxs-lookup"><span data-stu-id="39a5a-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="39a5a-161">Viņi var arī pievienot filtram citus resursa raksturlielumus, lai meklētu resursus, kam ir īpašas prasmes, izglītība un pieredze attiecībā uz konkrēto projektu.</span><span class="sxs-lookup"><span data-stu-id="39a5a-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="39a5a-162">**Scenārijs:** Tika sākts apstiprināts projekts, un projekta plānošanas posmā vecākā projekta vadītāja loma tika rezervēta kā plānots resurss.</span><span class="sxs-lookup"><span data-stu-id="39a5a-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="39a5a-163">Resursu pārvaldnieks tagad ir ieguvis resursu, lai izpildītu vecākā projekta vadītāja lomu.</span><span class="sxs-lookup"><span data-stu-id="39a5a-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="39a5a-164">Lapā **Resursu saraksts** atlasiet **Daniels Goldšmits**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="39a5a-165">Lapā **Resursa loma** atlasiet **Jauna** un ievadiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="39a5a-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="39a5a-166">**Stājas spēka:** Ievadiet pašreizējo datumu.</span><span class="sxs-lookup"><span data-stu-id="39a5a-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="39a5a-167">**Derīguma beigu datums:** Ievadiet **Nekad**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="39a5a-168">**Loma:** Ievadiet **Vecākais projekta vadītājs**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="39a5a-169">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="39a5a-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="39a5a-170">Cilnē **Kompetences** pievienojiet prasmi **ProjectMgmt** un sertifikātu **PMP**.</span><span class="sxs-lookup"><span data-stu-id="39a5a-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]