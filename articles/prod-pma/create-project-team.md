---
title: Projekta darba grupas izveide
description: Šajā tēmā ir sniegta informācija par to, kā izveidot un pārvaldīt projekta darba grupas.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d3d39aa28565692bf894ff8d4fc8f8c3c5542d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006205"
---
# <a name="create-a-project-team"></a><span data-ttu-id="f7271-103">Projekta komandas izveide</span><span class="sxs-lookup"><span data-stu-id="f7271-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7271-104">Lai izmantotu projektā iepriekš iestatītās lomas, projekta vadītājam šīs lomas ir jāsaista ar projektu.</span><span class="sxs-lookup"><span data-stu-id="f7271-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="f7271-105">Projektam var piešķirt vairākas lomas.</span><span class="sxs-lookup"><span data-stu-id="f7271-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="f7271-106">Lai izvairītos no pārpratumiem, šīs lomas rezervācijas laikā tiek automātiski apzīmētas.</span><span class="sxs-lookup"><span data-stu-id="f7271-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="f7271-107">Piemēram, ja projekta vadītājam ir nepieciešami trīs programmatūras inženieri, tiek automātiski ģenerētas trīs programmatūras inženieru lomas, kurām ir etiķetes **programmatūras inženieris 1**, **programmatūras inženieris 2** un **programmatūras inženieris 3**.</span><span class="sxs-lookup"><span data-stu-id="f7271-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="f7271-108">Ja lomai tika iepriekš iestatīti lomu raksturlielumi, tās resursa meklēšanas laikā tiek piemērotas kā filtrs.</span><span class="sxs-lookup"><span data-stu-id="f7271-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="f7271-109">Lai precizētu meklēšanu, var pievienot papildu raksturlielumus.</span><span class="sxs-lookup"><span data-stu-id="f7271-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="f7271-110">Lai nodrošinātu labāku skatu uz resursu pieejamību, var arī pielāgot skatīšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="f7271-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="f7271-111">Ir pieejamas opcijas rādīt stundas, dienas, nedēļas, mēneša, ceturkšņa un gada pieejamību.</span><span class="sxs-lookup"><span data-stu-id="f7271-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="f7271-112">Ir arī opcija rādīt pieejamo un atlikušo resursu noslodzi.</span><span class="sxs-lookup"><span data-stu-id="f7271-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="f7271-113">Šī opcija ir noderīga laika pārvaldībā, ja aprēķināt darbībām pieejamo laiku vai resursu pieejamību.</span><span class="sxs-lookup"><span data-stu-id="f7271-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="f7271-114">Projekta vadītājs var lapā atlasīt lomu un pēc tam, ja ir pieejams resurss, kas atbilst prasībai, atlasīt rezervēt resursu lomas izpildei.</span><span class="sxs-lookup"><span data-stu-id="f7271-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="f7271-115">Ņemiet vērā, ka šajā plānošanas posma brīdī resursi jārezervē.</span><span class="sxs-lookup"><span data-stu-id="f7271-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="f7271-116">Izveidojot WBS, varat aizstāt lomas ar projekta personāla resursiem.</span><span class="sxs-lookup"><span data-stu-id="f7271-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="f7271-117">Ja lomas WBS aizstāj ar personāla resursiem, resursa iestatījums automātiski atjaunina projekta darba grupu sarakstu un plānu.</span><span class="sxs-lookup"><span data-stu-id="f7271-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="f7271-118">[![Projekta darba grupu uzskaitījums, kas ietver gan lomas, gan faktiskos resursus](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="f7271-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="f7271-119">Projekta vadītājam ir dažādas opcijas resursa rezervēšanai projektam, piemēram, **Atlikusī noslodze**, **Pilna noslodze**, **Noslodzes daļa** un **Konkretizēt laiku**.</span><span class="sxs-lookup"><span data-stu-id="f7271-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="f7271-120">Šīs rezervācijas opcijas var atcelt jebkurā laikā, ja resursu piešķires mainās.</span><span class="sxs-lookup"><span data-stu-id="f7271-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="f7271-121">Tiek atbalstītas divu veidu rezervācijas:</span><span class="sxs-lookup"><span data-stu-id="f7271-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="f7271-122">**Stingrā rezervācija** — Resursa rezervācija tika apstiprināta darbam ar iesaisti uz konkrēto ilgumu.</span><span class="sxs-lookup"><span data-stu-id="f7271-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="f7271-123">**Vieglā rezervācija** — Resursa rezervācijas tika provizoriski iestatītam darbam ar iesaisti uz konkrēto ilgumu.</span><span class="sxs-lookup"><span data-stu-id="f7271-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="f7271-124">Šajā procedūrā paskaidrots, kā izveidot projekta komandu.</span><span class="sxs-lookup"><span data-stu-id="f7271-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="f7271-125">Projekta komandas izveide</span><span class="sxs-lookup"><span data-stu-id="f7271-125">Create a project team</span></span>

1. <span data-ttu-id="f7271-126">Saraksta lapā **Visi projekti** atlasiet projektu un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="f7271-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="f7271-127">Lauka **Plānot beigu datumu** cilnē **Projekta komanda un plānošana** ievadiet grafika sākuma datumu, pieskaitot vienu mēnesi.</span><span class="sxs-lookup"><span data-stu-id="f7271-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="f7271-128">Piemēram, ja grafika sākuma datums ir 2017. gada 24. jūnijs (24/06/2017), ievadiet **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="f7271-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="f7271-129">Atlasīt **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="f7271-129">Select **Add**.</span></span>
4. <span data-ttu-id="f7271-130">Lauka **Loma** rūtī **Pievienot lomas projektam** atlasiet **Vecākais projektu vadītājs**.</span><span class="sxs-lookup"><span data-stu-id="f7271-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="f7271-131">Atlasiet **Nepieciešamās kompetences**.</span><span class="sxs-lookup"><span data-stu-id="f7271-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="f7271-132">Lapā **Izvēlieties raksturlielumus** pēc noklusējuma tiek atlasīti raksturlielumi, kurus iepriekš iestatījāt vecākā projektu vadītāja lomai.</span><span class="sxs-lookup"><span data-stu-id="f7271-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="f7271-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f7271-133">Select **OK**.</span></span>
7. <span data-ttu-id="f7271-134">Lauka **Resursu skaits** lapā **Pievienot projektam lomas** ievadiet **1**.</span><span class="sxs-lookup"><span data-stu-id="f7271-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="f7271-135">Laukā **Resurss** uzmeklēšana rāda visus resursus, kuriem ir nepieciešamās kompetences.</span><span class="sxs-lookup"><span data-stu-id="f7271-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="f7271-136">Atlasiet **Daniels Goldšmits** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="f7271-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="f7271-137">**Projekta** lapā atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="f7271-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="f7271-138">Lauka **Loma** rūtī **Pievienot lomas projektam** atlasiet **Darba grupas dalībnieks**.</span><span class="sxs-lookup"><span data-stu-id="f7271-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="f7271-139">Laukā **Resursu skaits** ievadiet **5**.</span><span class="sxs-lookup"><span data-stu-id="f7271-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="f7271-140">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="f7271-140">Select **Create**.</span></span>
12. <span data-ttu-id="f7271-141">Lapā **Projekti** atlasiet **Izpildīt resursu**.</span><span class="sxs-lookup"><span data-stu-id="f7271-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="f7271-142">Projekta darba grupu uzraudzība</span><span class="sxs-lookup"><span data-stu-id="f7271-142">Monitor project teams</span></span>
1. <span data-ttu-id="f7271-143">Lapā **Visi projekti** atlasiet projekta **XYZ jaunināšanas fāze 2** saiti **Projekta ID**.</span><span class="sxs-lookup"><span data-stu-id="f7271-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="f7271-144">Kopsavilkuma cilnē **Projekta komanda un plānošana** pārbaudiet, vai uzskaitītie projekta resursi ir pareizi.</span><span class="sxs-lookup"><span data-stu-id="f7271-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]