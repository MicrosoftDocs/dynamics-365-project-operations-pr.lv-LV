---
title: Jaunas vides nodrošināšana
description: Šajā tēmā ir sniegta informācija par to, kā nodrošināt jaunu Project Operations vidi.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 044a942a068b33318b98041cc94944d90c1d63c3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121182"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="43b7b-103">Jaunas vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="43b7b-103">Provision a new environment</span></span>

<span data-ttu-id="43b7b-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="43b7b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="43b7b-105">Šajā tēmā ir sniegta informācija par to, kā nodrošināt jaunu Dynamics 365 Project Operations vidi scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.</span><span class="sxs-lookup"><span data-stu-id="43b7b-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="43b7b-106">Project Operations automatizētās nodrošināšanas iespējošana LCS projektā</span><span class="sxs-lookup"><span data-stu-id="43b7b-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="43b7b-107">Veiciet tālāk norādītās darbības, lai iespējotu Project Operations automatizētās nodrošināšanas plūsmu savam LCS projektam.</span><span class="sxs-lookup"><span data-stu-id="43b7b-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="43b7b-108">Dodieties uz [LCS](https://lcs.dynamics.com/v2) un atlasiet elementu **Priekšskatījuma līdzekļa pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="43b7b-109">Sarakstā **Priekšskatījuma līdzeklis** atlasiet **Project Operations līdzeklis** un pēc tam atlasiet **Priekšskatījuma līdzeklis iespējots**, lai iespējotu programmu Project Operations.</span><span class="sxs-lookup"><span data-stu-id="43b7b-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="43b7b-110">Šī darbība tiek veikta tikai viereiz katrā LCS projektā.</span><span class="sxs-lookup"><span data-stu-id="43b7b-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="43b7b-111">Project Operations vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="43b7b-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="43b7b-112">Atveriet jaunu Dynamics 365 Finance [demonstrācijas vidi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) vai [smilškastes/ražošanas vides](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) izvietojumu.</span><span class="sxs-lookup"><span data-stu-id="43b7b-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="43b7b-113">Veiciet vednī **Vidnes nodrošināšana** norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="43b7b-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="43b7b-114">Pārliecinieties, vai atlasītā lietojumprogrammas versija ir 10.0.13 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="43b7b-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="43b7b-115">Lai nodrošinātu Project Operations, sadaļā **Papildu iestatījumi** atlasiet **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="43b7b-116">Iespējojiet **Common Data Service iestatījumu**, atlasot **Jā**, un pēc tam ievadiet informāciju obligātajos laukos:</span><span class="sxs-lookup"><span data-stu-id="43b7b-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="43b7b-117">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="43b7b-117">Name</span></span>
  - <span data-ttu-id="43b7b-118">Reģions</span><span class="sxs-lookup"><span data-stu-id="43b7b-118">Region</span></span>
  - <span data-ttu-id="43b7b-119">Valoda</span><span class="sxs-lookup"><span data-stu-id="43b7b-119">Language</span></span>
  - <span data-ttu-id="43b7b-120">Valūta</span><span class="sxs-lookup"><span data-stu-id="43b7b-120">Currency</span></span>
 
5. <span data-ttu-id="43b7b-121">Laukā **Common Data Service veidne** atlasiet **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="43b7b-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="43b7b-122">Atlasiet vides tipu savam izvietojumam.</span><span class="sxs-lookup"><span data-stu-id="43b7b-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="43b7b-123">Abonementam atbilstošs izmēģinājums ļaus jums izvietot CDS vidi 30 dienas.</span><span class="sxs-lookup"><span data-stu-id="43b7b-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Izvietošanas iestatījumi](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="43b7b-125">Atlasiet **Piekrist**, lai apstiprinātu pakalpojuma noteikumus, un pēc tam atlasiet **Gatavs**, lai atgrieztos izvietošanas iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="43b7b-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Izvietošanas piekrišana](./media/2DeploymentConsent.png)

7. <span data-ttu-id="43b7b-127">Aizpildiet pārējos obligātos laukus vednī un apstipriniet izvietošanu.</span><span class="sxs-lookup"><span data-stu-id="43b7b-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="43b7b-128">Vides nodrošināšanas laiks atškiras atkarībā no vides tipa.</span><span class="sxs-lookup"><span data-stu-id="43b7b-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="43b7b-129">Nodrošināšana var ilgt līdz sešām stundām.</span><span class="sxs-lookup"><span data-stu-id="43b7b-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="43b7b-130">Pēc veiksmīgas izvietošanas pabeigšanas vide tiks rādīta kā **Izvietota**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="43b7b-131">Lai apstiprinātu, ka vide ir veiksmīgi izvietota, atlasiet **Pieteikties** un piesakieties vidē, lai apstiprinātu.</span><span class="sxs-lookup"><span data-stu-id="43b7b-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ vides informācija](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="43b7b-133">Project Operations Finance demonstrācijas datu lietošana (neobligāta darbība)</span><span class="sxs-lookup"><span data-stu-id="43b7b-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="43b7b-134">Lietojiet Project Operations Finance demonstrācijas datus 10.0.13 pakalpojuma laidiena mākoņpakalpojumā viesotajā vidē, kā aprakstīts [šajā rakstā](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="43b7b-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="43b7b-135">Atjauninājumu lietošana Finance vidē</span><span class="sxs-lookup"><span data-stu-id="43b7b-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="43b7b-136">Programmai Project Operations ir nepieciešama Finance vide ar lietojumprogrammas versiju **10.0.13 (10.0.569.20009)** vai jaunāku versiju.</span><span class="sxs-lookup"><span data-stu-id="43b7b-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="43b7b-137">Lai saņemtu šo versiju, iespējams, jūsu Finance videi būs jālieto kvalitātes atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="43b7b-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="43b7b-138">LCS lapas **Vides informācija** sadaļā **Pieejamie atjauninājumi** atlasiet **Skatīt atjauninājumu**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Skatīt atjauninājumus](./media/5ViewUpdates.png)

2. <span data-ttu-id="43b7b-140">Lapā **Binārie atjauninājumi** atlasiet **Saglabāt pakotni.**</span><span class="sxs-lookup"><span data-stu-id="43b7b-140">On the **Binary updates** page, select **Save package.**</span></span>

![Saglabāt pakotni](./media/6SavePackage.png)

3. <span data-ttu-id="43b7b-142">Noklikšķiniet uz **Atlasīt visu** un pēc tam atlasiet **Saglabāt pakotni**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-142">Click **Select all** and then select **Save package**.</span></span>

![Atjauninājumu pārskatīšana un saglabāšana](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="43b7b-144">Ievadiet pakotnes nosaukumu un aprakstu un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="43b7b-145">Atkarībā no interneta savienojuma šis process var ilgt zināmu laiku.</span><span class="sxs-lookup"><span data-stu-id="43b7b-145">Depending on the internet connection, this process might take some time.</span></span>

![Pakotnes augšupielāde līdzekļu bibliotēkā](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="43b7b-147">Pēc tam, kad pakotne ir saglabāta, atlasiet **Gatavs** un saglabājiet šo pakotni sava LCS projekta līdzekļu bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="43b7b-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="43b7b-148">Pakotnes saglabāšana un validēšana var aizņemt aptuveni 15 minūtes.</span><span class="sxs-lookup"><span data-stu-id="43b7b-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="43b7b-149">Lai lietotu atjauninājumu, pārejiet uz LCS lapu **Vides informācija** un atlasiet **Uzturēt** > **Lietot atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Uzturēt vides](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="43b7b-151">Atjauninājumu sarakstā atlasiet izveidoto pakotni un atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Lietot atjauninājumus](./media/10ApplyUpdates.png)

<span data-ttu-id="43b7b-153">Vide apkalpošana aizņems zināmu laiku.</span><span class="sxs-lookup"><span data-stu-id="43b7b-153">Environment servicing will take some time.</span></span> <span data-ttu-id="43b7b-154">Pēc pabeigšanas vide atgriezīsies izvietotā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="43b7b-154">After it is complete, the environment will return to a deployed state.</span></span>

![Izvietota vide](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="43b7b-156">Duālās rakstīšanas savienojuma izveide</span><span class="sxs-lookup"><span data-stu-id="43b7b-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="43b7b-157">Savā LCS projektā dodieties uz lapu **Vides informācija**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="43b7b-158">Sadaļā **Common Data Service vides informācija** atlasiet **Saite uz CDS programmām**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="43b7b-159">Pēc tam, kad saite ir izveidota, vēlreiz atlasiet **Saite uz CDS programmām**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="43b7b-160">Jūs tiksit novirzīts uz duālo rakstīšanu risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="43b7b-160">You will be redirected to Dual Write in Finance.</span></span>

![Saite uz CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="43b7b-162">Atlasiet **Lietot risinājumu**, lai piekļūtu entītijām, kas tiks kartētas integrācijā.</span><span class="sxs-lookup"><span data-stu-id="43b7b-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Lietot risinājumu](./media/13ApplySolutions.png)

5. <span data-ttu-id="43b7b-164">Atlasiet abus risinājumus — **Dynamics 365 Finance and Operations duālās rakstīšanas entītiju kartējumu** un **Dynamics 365 Project Operations duālās rakstīšanas entītiju kartējumu** un pēc tam atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Apstiprināt risinājumus](./media/14ConfirmSolutions.png)

<span data-ttu-id="43b7b-166">Pēc risinājumu lietošanas duālās rakstīšanas entītijas tiek lietotas videi.</span><span class="sxs-lookup"><span data-stu-id="43b7b-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Risinājumu lietošana](./media/15ApplyingSolutions.png)

<span data-ttu-id="43b7b-168">Pēc entītiju lietošanas visi pieejamie kartējumi ir uzskaitīti vidē.</span><span class="sxs-lookup"><span data-stu-id="43b7b-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Duālās rakstīšanas kartējumi](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="43b7b-170">Pēc atjaunināšanas atsvaidziniet datu entītijas</span><span class="sxs-lookup"><span data-stu-id="43b7b-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="43b7b-171">Risinājumā Finance dodieties uz darbvietu **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-171">In Finance, go to the **Data management** workspace.</span></span>

![Datu pārvaldības darbvieta](./media/16DataManagement.png)

2. <span data-ttu-id="43b7b-173">Atlasiet elementu **Struktūras parametri**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-173">Select the **Framework parameters** tile.</span></span>

![Struktūras parametri](./media/17FrameworkParameters.png)

3. <span data-ttu-id="43b7b-175">Lapā **Entītiju iestatījumi** atlasiet **Atsvaidzināt entītiju sarakstu**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Atsvaidzināt entītiju sarakstu](./media/18RefreshEntityList.png)

<span data-ttu-id="43b7b-177">Atsvaidzināšana aizņems aptuveni 20 minūtes.</span><span class="sxs-lookup"><span data-stu-id="43b7b-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="43b7b-178">Kad tā būs pabeigta, saņemsit brīdinājumu.</span><span class="sxs-lookup"><span data-stu-id="43b7b-178">You will receive an alert when it is complete.</span></span>

![Atsvaidzināšanas apstiprināšana](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="43b7b-180">Project Operations duālās rakstīšanas kartējumu palaišana</span><span class="sxs-lookup"><span data-stu-id="43b7b-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="43b7b-181">Savā LCS projektā dodieties uz lapu **Vides informācija**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="43b7b-182">Sadaļā **Common Data Service vides informācija** atlasiet **Saite uz CDS programmām.**</span><span class="sxs-lookup"><span data-stu-id="43b7b-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="43b7b-183">Pēc saites atlasīšanas tiksit novirzīts uz entītiju sarakstu kartējumos.</span><span class="sxs-lookup"><span data-stu-id="43b7b-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="43b7b-184">Startējiet kartējumus, kā aprakstīts tālāk redzamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="43b7b-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="43b7b-185">Noteikti izpildiet darbības parādītajā secībā.</span><span class="sxs-lookup"><span data-stu-id="43b7b-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="43b7b-186">**Entītiju kartējums**</span><span class="sxs-lookup"><span data-stu-id="43b7b-186">**Entity Map**</span></span> | <span data-ttu-id="43b7b-187">**Atsvaidzināt entītiju**</span><span class="sxs-lookup"><span data-stu-id="43b7b-187">**Refresh entity**</span></span> | <span data-ttu-id="43b7b-188">**Sākotnējā sinhronizācija**</span><span class="sxs-lookup"><span data-stu-id="43b7b-188">**Initial sync**</span></span> | <span data-ttu-id="43b7b-189">**Sākotnējās sinhronizācijas šablons**</span><span class="sxs-lookup"><span data-stu-id="43b7b-189">**Master for initial sync**</span></span> | <span data-ttu-id="43b7b-190">**Palaist priekšnosacījumus**</span><span class="sxs-lookup"><span data-stu-id="43b7b-190">**Run prerequisites**</span></span> | <span data-ttu-id="43b7b-191">**Priekšnosacījumu sākotnējā sinhronizācija**</span><span class="sxs-lookup"><span data-stu-id="43b7b-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="43b7b-192">**Projekta resursu lomas visiem uzņēmumiem (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="43b7b-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="43b7b-193">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-193">No</span></span> | <span data-ttu-id="43b7b-194">Jā</span><span class="sxs-lookup"><span data-stu-id="43b7b-194">Yes</span></span> | <span data-ttu-id="43b7b-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="43b7b-195">Common Data Service</span></span> | <span data-ttu-id="43b7b-196">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-196">No</span></span> | <span data-ttu-id="43b7b-197">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-197">N\A</span></span> |
| <span data-ttu-id="43b7b-198">**Juridiskas personas (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="43b7b-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="43b7b-199">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-199">No</span></span> | <span data-ttu-id="43b7b-200">Jā</span><span class="sxs-lookup"><span data-stu-id="43b7b-200">Yes</span></span> | <span data-ttu-id="43b7b-201">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="43b7b-201">Finance and Operations apps</span></span> | <span data-ttu-id="43b7b-202">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-202">No</span></span> | <span data-ttu-id="43b7b-203">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-203">N\A</span></span> |
| <span data-ttu-id="43b7b-204">**Project Operations integrācijas faktiskie dati (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="43b7b-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="43b7b-205">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-205">No</span></span> | <span data-ttu-id="43b7b-206">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-206">No</span></span> | <span data-ttu-id="43b7b-207">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-207">N\A</span></span> | <span data-ttu-id="43b7b-208">Jā</span><span class="sxs-lookup"><span data-stu-id="43b7b-208">Yes</span></span> | <span data-ttu-id="43b7b-209">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-209">No</span></span> |
| <span data-ttu-id="43b7b-210">**Projekta līguma rindas (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="43b7b-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="43b7b-211">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-211">No</span></span> | <span data-ttu-id="43b7b-212">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-212">No</span></span> | <span data-ttu-id="43b7b-213">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-213">N\A</span></span> | <span data-ttu-id="43b7b-214">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-214">No</span></span> | <span data-ttu-id="43b7b-215">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-215">No</span></span> |
| <span data-ttu-id="43b7b-216">**Integrāciju entitīja projekta transakciju relācijām (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="43b7b-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="43b7b-217">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-217">No</span></span> | <span data-ttu-id="43b7b-218">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-218">No</span></span> | <span data-ttu-id="43b7b-219">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-219">N\A</span></span> | <span data-ttu-id="43b7b-220">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-220">No</span></span> | <span data-ttu-id="43b7b-221">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-221">N\A</span></span> |
| <span data-ttu-id="43b7b-222">**Project Operations integrācijas līguma rindu atskaites punkti (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="43b7b-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="43b7b-223">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-223">No</span></span> | <span data-ttu-id="43b7b-224">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-224">No</span></span> | <span data-ttu-id="43b7b-225">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-225">N\A</span></span> | <span data-ttu-id="43b7b-226">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-226">No</span></span> | <span data-ttu-id="43b7b-227">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-227">N\A</span></span> |
| <span data-ttu-id="43b7b-228">**Project Operations integrācijas entītija izdevumu aprēķiniem (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="43b7b-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="43b7b-229">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-229">No</span></span> | <span data-ttu-id="43b7b-230">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-230">No</span></span> | <span data-ttu-id="43b7b-231">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-231">N\A</span></span> | <span data-ttu-id="43b7b-232">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-232">No</span></span> | <span data-ttu-id="43b7b-233">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-233">N\A</span></span> |
| <span data-ttu-id="43b7b-234">**Project Operations integrācijas projekta izdevumu kategorijas eksporta entītija (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="43b7b-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="43b7b-235">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-235">No</span></span> | <span data-ttu-id="43b7b-236">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-236">No</span></span> | <span data-ttu-id="43b7b-237">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-237">N\A</span></span> | <span data-ttu-id="43b7b-238">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-238">No</span></span> | <span data-ttu-id="43b7b-239">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-239">N\A</span></span> |
| <span data-ttu-id="43b7b-240">**Project Operations integrācijas projekta izdevumu eksporta entītija (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="43b7b-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="43b7b-241">Jā</span><span class="sxs-lookup"><span data-stu-id="43b7b-241">Yes</span></span> | <span data-ttu-id="43b7b-242">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-242">No</span></span> | <span data-ttu-id="43b7b-243">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-243">N\A</span></span> | <span data-ttu-id="43b7b-244">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-244">No</span></span> | <span data-ttu-id="43b7b-245">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-245">N\A</span></span> |
| <span data-ttu-id="43b7b-246">**Project Operations integrācijas entītija stundu aprēķiniem (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="43b7b-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="43b7b-247">Jā</span><span class="sxs-lookup"><span data-stu-id="43b7b-247">Yes</span></span> | <span data-ttu-id="43b7b-248">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-248">No</span></span> | <span data-ttu-id="43b7b-249">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-249">N\A</span></span> | <span data-ttu-id="43b7b-250">No</span><span class="sxs-lookup"><span data-stu-id="43b7b-250">No</span></span> | <span data-ttu-id="43b7b-251">N/A</span><span class="sxs-lookup"><span data-stu-id="43b7b-251">N\A</span></span> |


4. <span data-ttu-id="43b7b-252">Lai atsvaidzinātu entītiju, atlasiet kartējuma nosaukumu un pēc tam atlasiet **Atsvaidzināt entītijas**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Atsvaidzināt kartējumu](./media/20RefreshMapping.png)

5. <span data-ttu-id="43b7b-254">Kad atsvaidzināšana ir pabeigta, palaidiet karti.</span><span class="sxs-lookup"><span data-stu-id="43b7b-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="43b7b-255">Pirms nākamā kartējuma iespējošanas pārliecinieties, vai kartējumam tabulā ir statuss **Darbojas**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="43b7b-256">Kartējumu ar lielāku priekšnosacījumu skaitu palaišana var aizņemt zināmu laiku.</span><span class="sxs-lookup"><span data-stu-id="43b7b-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="43b7b-257">Lai palaistu kartējumu ar priekšnosacījumiem, iespējojiet pārslēgšanas pogu **Rādīt saistītos entītiju kartējumus**.</span><span class="sxs-lookup"><span data-stu-id="43b7b-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="43b7b-258">Ja tabulā redzams, ka vienumam **Priekšnosacījumu sākotnējā sinhronizācija** ir vērtība **Nē**, pirms palaišanas pārbaudiet, vai **Sākotnējās sinhronizācijas** karodziņš ir **Izslēgts** visos priekšnosacījumu kartējumos.</span><span class="sxs-lookup"><span data-stu-id="43b7b-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Palaist kartējumu](./media/21RunMap.png)

6. <span data-ttu-id="43b7b-260">Pārbaudiet, vai visiem ar projektu saistītajiem kartējumiem ir statuss Darbojas.</span><span class="sxs-lookup"><span data-stu-id="43b7b-260">Validate all project related maps are in the running state.</span></span>

![Visi kartējumi darbojas](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="43b7b-262">Konfigurācijas datu lietošana pakalpojumā CDS lietojumprogrammai Project Operations (izvēles)</span><span class="sxs-lookup"><span data-stu-id="43b7b-262">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="43b7b-263">Ja esat lietojis demonstrācijas datus finanšu vidē, skatiet sadaļu [Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service risinājumam Project Operations](resource-apply-pro-setup-config-data.md), lai lietotu demonstrācijas datus CDS vidē.</span><span class="sxs-lookup"><span data-stu-id="43b7b-263">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="43b7b-264">Jūsu Project Operations vide tagad ir nodrošināta un konfigurēta.</span><span class="sxs-lookup"><span data-stu-id="43b7b-264">Your Project Operations environment is now provisioned and configured.</span></span> 
