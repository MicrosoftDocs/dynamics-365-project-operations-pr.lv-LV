---
title: Microsoft Project klienta integrācija
description: Projekta grafika plānošana un uzturēšana var būt sarežģīta, tāpēc projektu vadītājiem ir jāizmanto rīki, kas viņiem palīdz pārvaldīt šo uzdevumu. Integrācija ar Microsoft Project Client sniedz atbalstu, lai atvērtu un pārvaldītu projekta darba sadalījuma struktūru.
author: Yowelle
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 032d726bb6206c563b573f30d13fe2697a13c949
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999455"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="e0c72-104">Microsoft Project klienta integrācija</span><span class="sxs-lookup"><span data-stu-id="e0c72-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0c72-105">Projekta grafika plānošana un uzturēšana var būt sarežģīta, tāpēc projektu vadītājiem ir jāizmanto rīki, kas viņiem palīdz pārvaldīt šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="e0c72-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="e0c72-106">Integrācija ar Microsoft Project Client sniedz atbalstu, lai atvērtu un pārvaldītu projekta darba sadalījuma struktūru.</span><span class="sxs-lookup"><span data-stu-id="e0c72-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="e0c72-107">Projekta vadītājs var publicēt jebkādas izmaiņas atpakaļ Dynamics 365 Finance projekta darba sadalījuma struktūrā.</span><span class="sxs-lookup"><span data-stu-id="e0c72-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="e0c72-108">Ja izmantojat jūlija atjauninājumu (versija 10.0.4), ir jāinstalē KB 4054797 un 4055884.</span><span class="sxs-lookup"><span data-stu-id="e0c72-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="e0c72-109">Microsoft Project Client pievienojumprogrammas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e0c72-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="e0c72-110">Lai iespējotu integrēšanu ar programmu Microsoft Project Client, lietotāja klienta Microsoft Project lietojumprogrammā ir jābūt instalētai Microsoft Dynamics 365 pievienojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="e0c72-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="e0c72-111">To var izdarīt, atverot **Projekta pārvaldības darbvietu**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="e0c72-112">•  Noklikšķiniet uz **Konfigurēt projekta klienta pievienojumprogrammu** no darbvietas sadaļas **Saites** > **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="e0c72-113">•  Noklikšķiniet uz **Atvērt** un pēc tam noklikšķiniet uz **Palaist**, kad tiek parādīta uzvedne.</span><span class="sxs-lookup"><span data-stu-id="e0c72-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="e0c72-114">Esoša melnraksta darba sadalījuma struktūras atvēršana un rediģēšana programmā Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="e0c72-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="e0c72-115">Ja projektā programmā Dynamics 365 Finance jau ir izveidota darba sadalījuma struktūra, darba sadalījuma struktūru var atvērt Microsoft Project Client lietojumprogrammā, ja darba sadalījuma struktūrai ir melnraksta statuss.</span><span class="sxs-lookup"><span data-stu-id="e0c72-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="e0c72-116">Lai atvērtu no **Projekta** lapas, noklikšķiniet uz **Atvērt programmā Microsoft Project** saites cilnē **Plāns**. Šo lapu var arī atvērt no Microsoft Project Client programmas, **Microsoft Dynamics 365** cilnē noklikšķinot **Atvērt**. Sarakstā atlasiet **Juridiska persona** un **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="e0c72-117">Ja izmantojat Internet Explorer kā pārlūkprogrammu, noklikšķiniet uz **Saglabāt**, lai manuāli atvērtu no atrašanās vietas, kurā fails tiek lejupielādēts.</span><span class="sxs-lookup"><span data-stu-id="e0c72-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="e0c72-118">Vai noklikšķiniet uz **Saglabāt un atvērt**, lai šo failu atvērtu programmā Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="e0c72-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="e0c72-119">Saglabājot nepārdēvējiet failu.</span><span class="sxs-lookup"><span data-stu-id="e0c72-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="e0c72-120">Pirms veicat faila labojumus, izmantojot Microsoft Project Client, no tā ir jāizrakstās. Cilnē  **Microsoft Dynamics 365** noklikšķiniet uz **Izrakstīt**. Tādējādi citi lietotāji nevarēs vienlaikus rediģēt darba sadalījuma struktūru no Finance.</span><span class="sxs-lookup"><span data-stu-id="e0c72-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="e0c72-121">Lai pēc labojumu veikšanas publicētu darba sadalījuma struktūru, cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Atzīmēties**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="e0c72-122">Ja projektam programmā Finance jau ir pievienota projekta komanda, resursu saraksts tiks aizpildīts ar darba grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="e0c72-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="e0c72-123">Ja projektam vēl nav pievienota projekta darba grupa, varat atlasīt resursus un veidot komandu programmā Microsoft Project Client, noklikšķinot uz pogas **Resursi** cilnē **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="e0c72-124">Atzīmēšanās procesa ietvaros uz Finance tiks atpakaļ sinhronizēti šādi dati:</span><span class="sxs-lookup"><span data-stu-id="e0c72-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="e0c72-125">•   Uzdevuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="e0c72-125">•   Task name</span></span>

<span data-ttu-id="e0c72-126">•   Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="e0c72-126">•   Start date</span></span>

<span data-ttu-id="e0c72-127">•   Beigu datums</span><span class="sxs-lookup"><span data-stu-id="e0c72-127">•   Finish date</span></span>

<span data-ttu-id="e0c72-128">•   Pirmstecīgie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="e0c72-128">•   Predecessors</span></span>

<span data-ttu-id="e0c72-129">•   Resursa nosaukumi</span><span class="sxs-lookup"><span data-stu-id="e0c72-129">•   Resource names</span></span>

<span data-ttu-id="e0c72-130">•   Kategorija</span><span class="sxs-lookup"><span data-stu-id="e0c72-130">•   Category</span></span>

<span data-ttu-id="e0c72-131">•   Resursa kategorija</span><span class="sxs-lookup"><span data-stu-id="e0c72-131">•   Resource category</span></span>

<span data-ttu-id="e0c72-132">•   Darba laiks</span><span class="sxs-lookup"><span data-stu-id="e0c72-132">•   Work hours</span></span>

<span data-ttu-id="e0c72-133">•   Piezīmes</span><span class="sxs-lookup"><span data-stu-id="e0c72-133">•   Notes</span></span>

<span data-ttu-id="e0c72-134">•   Prioritāte</span><span class="sxs-lookup"><span data-stu-id="e0c72-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="e0c72-135">Ja savam Microsoft Project Client failam pievienojat citas kolonnas, tās netiks saglabātas failā un netiks rādītas, failu atkārtoti atverot.</span><span class="sxs-lookup"><span data-stu-id="e0c72-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="e0c72-136">Darba sadalījuma struktūras izveide esošam projektam, izmantojot Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="e0c72-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="e0c72-137">Lai izveidotu jaunu darba sadalījuma struktūru, izmantojot Microsoft Project Client, veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="e0c72-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="e0c72-138">Atveriet Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="e0c72-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="e0c72-139">**Microsoft Dynamics 365** cilnē noklikšķiniet uz **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="e0c72-140">Atlasiet projekta **Juridisko personu**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="e0c72-141">Atlasiet **Projektu**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="e0c72-142">**Microsoft Dynamics 365** cilnē noklikšķiniet uz **Izrakstīt**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="e0c72-143">Kad esat gatavs publicēt programmā Finance, noklikšķiniet uz **Atzīmēties** cilnē **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="e0c72-144">Aizstājiet esošu darba sadalījuma struktūru esošam projektam, izmantojot Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="e0c72-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="e0c72-145">Lai izveidotu jaunu darba sadalījuma struktūru, izmantojot Microsoft Project Client, un aizstātu esošu darba sadalījuma struktūru esošam projektam, veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="e0c72-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="e0c72-146">Atveriet Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="e0c72-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="e0c72-147">Izveidojiet grafiku programmā Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="e0c72-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="e0c72-148">Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Saglabāt izmaiņas** > **Aizstāt esošu projektu**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="e0c72-149">Atlasiet projekta **Juridisko personu**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="e0c72-150">Atlasiet **Projektu**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="e0c72-151">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="e0c72-152">Jauna projekta izveide no Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="e0c72-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="e0c72-153">Atveriet Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="e0c72-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="e0c72-154">Izveidojiet grafiku programmā Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="e0c72-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="e0c72-155">Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Saglabāt izmaiņas** > **Saglabāt jaunā projektā**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="e0c72-156">Atlasiet projekta **Juridisko personu**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="e0c72-157">Ja nepieciešams, ievadiet **Projekta ID**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="e0c72-158">Ievadiet **Projekta nosaukumu**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="e0c72-159">Atlasiet **Projekta veidu**, **Projekta grupu** un **Projekta līguma ID**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="e0c72-160">Varat arī izveidot jaunu projekta līgumu, noklikšķinot uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="e0c72-161">Atlasiet **Kalendāru**, ko izmantot resursu piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="e0c72-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="e0c72-162">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e0c72-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]