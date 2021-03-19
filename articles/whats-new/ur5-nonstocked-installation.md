---
title: Project Operations atjaunināšana Finance vidē
description: Šajā tēmā sniegta informācija par to, kā atjaunināt Project Operations jūsu Dynamics 365 Finance vidē.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291988"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="d170f-103">Project Operations atjaunināšana Finance vidē</span><span class="sxs-lookup"><span data-stu-id="d170f-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="d170f-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="d170f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="d170f-105">Šajā tēmā sniegta informācija par to, kā atjaunināt Dynamics 365 Project Operations jūsu Dynamics 365 Finance vidē.</span><span class="sxs-lookup"><span data-stu-id="d170f-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="d170f-106">Lai atjauninātu Project Operations uz 5. atjauninājumu (UR5): ir nepieciešams veikt trīs procedūras:</span><span class="sxs-lookup"><span data-stu-id="d170f-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="d170f-107">Importējiet pakotni jūsu iepriekšējā priekšskatījuma projektā</span><span class="sxs-lookup"><span data-stu-id="d170f-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="d170f-108">Lietojiet atjauninājumu</span><span class="sxs-lookup"><span data-stu-id="d170f-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="d170f-109">Atjauniniet Dataverse vidi</span><span class="sxs-lookup"><span data-stu-id="d170f-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="d170f-110">Importējiet pakotni savā LCS projektā</span><span class="sxs-lookup"><span data-stu-id="d170f-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="d170f-111">Piesakieties [Lifecycle Services (LCS)](https://lcs.dynamics.com/) kā projekta īpašnieks vai vides vadītājs.</span><span class="sxs-lookup"><span data-stu-id="d170f-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="d170f-112">Projektu sarakstā atlasiet savu LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="d170f-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="d170f-113">Lapā **Projekts**, grupā **Vides** atveriet vidi, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="d170f-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="d170f-114">Pārbaudiet, vai vide darbojas.</span><span class="sxs-lookup"><span data-stu-id="d170f-114">Verify that the environment is running.</span></span> <span data-ttu-id="d170f-115">Ja tā nav sāknēta, sāknējiet vidi.</span><span class="sxs-lookup"><span data-stu-id="d170f-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="d170f-116">Sadaļas **Pieejami atjauninājumi** sadaļā **Jauns laidiens** atlasiet **Skatīt atjauninājumu** 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="d170f-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Skatīt atjaunināšanas pogu](media/view-update.png)

6. <span data-ttu-id="d170f-118">Lapā **Binārie atjauninājumi** atlasiet **Saglabāt pakotni**.</span><span class="sxs-lookup"><span data-stu-id="d170f-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="d170f-119">Lapā **Pārskatīt un saglabāt atjauninājumus** atlasiet **Saglabāt pakotni**.</span><span class="sxs-lookup"><span data-stu-id="d170f-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="d170f-120">Rūtī **Saglabāt pakotni līdzekļu bibliotēkā**, kura tiek atvērta, ievadiet pakotnes nosaukumu un pēc tam atlasiet **Saglabāt pakotni**.</span><span class="sxs-lookup"><span data-stu-id="d170f-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="d170f-121">Kad LCS ir pabeidzis pakotnes saglabāšanu, tiek iespējota poga **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="d170f-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="d170f-122">Atlasiet **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="d170f-122">Select **Done**.</span></span> <span data-ttu-id="d170f-123">LCS pārbaudīs pakotni.</span><span class="sxs-lookup"><span data-stu-id="d170f-123">LCS will verify the package.</span></span> <span data-ttu-id="d170f-124">Pārbaude var ilgt dažas minūtes vai līdz pat vienu stundu.</span><span class="sxs-lookup"><span data-stu-id="d170f-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="d170f-125">Lietojiet pakotnes atjauninājumu</span><span class="sxs-lookup"><span data-stu-id="d170f-125">Apply the package update</span></span>

1. <span data-ttu-id="d170f-126">LCS lapā **Vides informācija** atlasiet **Uzturēt** > **Lietot atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="d170f-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="d170f-127">Sarakstā atlasiet pakotni, kuru saglabājāt iepriekš un pēc tam atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="d170f-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="d170f-128">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties izvietot pakotni.</span><span class="sxs-lookup"><span data-stu-id="d170f-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Apstipriniet pakotnes izvietošanas dialoglodziņu](media/confirm-package-deployment.png)

4. <span data-ttu-id="d170f-130">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atjaunināt lietojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="d170f-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Apstipriniet lietojumprogrammas atjaunināšanas dialoglodziņu](media/confirm-application-update.png)

<span data-ttu-id="d170f-132">Tiks sākta izvietošana un lietojumprogrammas atjaunināšana.</span><span class="sxs-lookup"><span data-stu-id="d170f-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="d170f-133">Lapas **Vides informācija** augšējā labajā stūrī vides statuss tiks atjaunināts uz **Apkalpošana**.</span><span class="sxs-lookup"><span data-stu-id="d170f-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="d170f-134">Atjaunināšana tiks pabeigta pēc aptuveni divām stundām.</span><span class="sxs-lookup"><span data-stu-id="d170f-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="d170f-135">Lietojumprogrammas laidiena informācija tiks atjaunināta uz  **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** un vides statuss tiks atjaunināts uz **Izvietota**.</span><span class="sxs-lookup"><span data-stu-id="d170f-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="d170f-136">Atjauniniet savu Dataverse vidi</span><span class="sxs-lookup"><span data-stu-id="d170f-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="d170f-137">Pierakstieties [Power Platform administrēšanas centrā](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="d170f-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="d170f-138">Sarakstā atrodiet un atveriet vidi, kuru izmantojāt, lai instalētu Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d170f-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="d170f-139">Lapā **Vides** atlasiet **Resurss** > **Dynamics 365 lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="d170f-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="d170f-140">Sarakstā atrodiet **Microsoft Dynamics 365 Project Operations** un kolonnā **Statuss** atlasiet **Pieejamais atjauninājums**.</span><span class="sxs-lookup"><span data-stu-id="d170f-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="d170f-141">Atzīmējiet izvēles rūtiņu **Piekrītu servisa nosacījumiem** un pēc tam atlasiet **Atjaunināt**.</span><span class="sxs-lookup"><span data-stu-id="d170f-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="d170f-142">Tiks instalēta risinājuma jaunākā versija.</span><span class="sxs-lookup"><span data-stu-id="d170f-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="d170f-143">Pēc instalēšanas pabeigšanas būs uzinstalēta versija 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="d170f-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="d170f-144">Jaunu līdzekļu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d170f-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="d170f-145">Duālās rakstīšanas kartēšanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="d170f-145">Enable dual-write mapping</span></span>

<span data-ttu-id="d170f-146">Pēc tam, kad pabeidzat atjaunināšanu Finance un Dataverse vidēs, varat iespējot nepieciešamos duālās rakstīšanas kartējumus.</span><span class="sxs-lookup"><span data-stu-id="d170f-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="d170f-147">Izpildiet šīs procedūras, lai iespējotu duālās rakstīšanas kartējumus.</span><span class="sxs-lookup"><span data-stu-id="d170f-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="d170f-148">Atjauniniet drošības iestatījumus Customer Engagement vidē</span><span class="sxs-lookup"><span data-stu-id="d170f-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="d170f-149">Atsvaidziniet datu vienības</span><span class="sxs-lookup"><span data-stu-id="d170f-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="d170f-150">Atjauniniet un palaidiet duālās rakstīšanas kartējumus</span><span class="sxs-lookup"><span data-stu-id="d170f-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="d170f-151">Atjauniniet drošības iestatījumus Dataverse vidē</span><span class="sxs-lookup"><span data-stu-id="d170f-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="d170f-152">Kā daļa no UR5 atjaunināšanas ir nepieciešami šādi entitīju drošības privilēģiju atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="d170f-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="d170f-153">Savā Dataverse vidē dodieties uz **Iestatījumi** un grupā **Sistēma** atlasiet **Drošība**.</span><span class="sxs-lookup"><span data-stu-id="d170f-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse vides iestatījumi](media/Picture21.png)

2. <span data-ttu-id="d170f-155">Atlasiet **Drošības lomas**.</span><span class="sxs-lookup"><span data-stu-id="d170f-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="d170f-156">Lomu sarakstā atlasiet **duālās rakstīšanas programmas lietotājs** un atlasiet cilni **Pielāgotās entitījas**.</span><span class="sxs-lookup"><span data-stu-id="d170f-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="d170f-157">Pārbaudiet, vai lomai ir **Lasīšanas** un **Pievienošanas atļaujas** elementiem:</span><span class="sxs-lookup"><span data-stu-id="d170f-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="d170f-158">**Valūtas maiņās kursa veids**</span><span class="sxs-lookup"><span data-stu-id="d170f-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="d170f-159">**Uzņēmumu tabula**</span><span class="sxs-lookup"><span data-stu-id="d170f-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="d170f-160">**Finanšu kalendārs**</span><span class="sxs-lookup"><span data-stu-id="d170f-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="d170f-161">**Virsgrāmata**</span><span class="sxs-lookup"><span data-stu-id="d170f-161">**Ledger**</span></span>

5. <span data-ttu-id="d170f-162">Pēc drošības lomas atjaunināšanas dodieties uz **Iestatījumi** > **Drošība** > **Darba grupas**.</span><span class="sxs-lookup"><span data-stu-id="d170f-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="d170f-163">Pārbaudiet, vai darba grupai tiek lietota loma **duālās rakstīšanas programmas lietotājs**.</span><span class="sxs-lookup"><span data-stu-id="d170f-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="d170f-164">Atsvaidziniet datu entitījas no atjauninājuma</span><span class="sxs-lookup"><span data-stu-id="d170f-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="d170f-165">Finance vidē atveriet **Datu pārvaldības** darbvietu un pēc tam atveriet lapu **Struktūras parametri**.</span><span class="sxs-lookup"><span data-stu-id="d170f-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="d170f-166">Cilnē **Entitījas iestatījumi** atlasiet **Atsvaidzināt entitīju sarakstu**.</span><span class="sxs-lookup"><span data-stu-id="d170f-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="d170f-167">Lai apstiprinātu entitījas atsvaidzināšanu atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="d170f-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="d170f-168">Šī procesa pabeigšanai būs nepieciešamas aptuveni 20 minūtes.</span><span class="sxs-lookup"><span data-stu-id="d170f-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="d170f-169">Kad atsvaidzināšana būs pabeigta, jūs saņemsit ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="d170f-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="d170f-170">Duālās rakstīšanas kartējumu atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="d170f-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="d170f-171">Darbvietā **Datu pārvaldība** atlasiet **Duālā rakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="d170f-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="d170f-172">Atlasiet **Lietot risinājumus**, atlasiet sarakstā abus risinājumus un pēc tam atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="d170f-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="d170f-173">Lapā **Duālā rakstīšana** attlasiet šādus tabulu kartējumus, pēc tam atlasiet **Apturēt**.</span><span class="sxs-lookup"><span data-stu-id="d170f-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="d170f-174">**Project Operations integrācijas faktiskie dati (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="d170f-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="d170f-175">**Project Operations integrācijas projekta izmaksu kategorijas (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="d170f-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="d170f-176">**Project Operations integrācijas faktisko datu projekta izmaksu eksporta entitīja (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="d170f-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="d170f-177">Lapā **Tabulas kartes versija** lietojiet jauno kartes versiju katrai no trim entitījām.</span><span class="sxs-lookup"><span data-stu-id="d170f-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="d170f-178">Lapā **Duālā rakstīšana** atlasiet palaišanu, lai restartētu kartes.</span><span class="sxs-lookup"><span data-stu-id="d170f-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="d170f-179">Karšu sarakstā atlasiet karti **Virsgrāmata (msdyn_ledgers)** ar visiem priekšnosacījumiem un atzīmējiet izvēles rūtiņu **Sākotnējā sinhronizācija**.</span><span class="sxs-lookup"><span data-stu-id="d170f-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="d170f-180">Laukā **Sākotnējās sinhronizācijas šablons** atlasiet **Finance and Operations lietojumprogrammas** un pēc tam atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="d170f-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Virsgrāmatas kartes sinhronizācija](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]