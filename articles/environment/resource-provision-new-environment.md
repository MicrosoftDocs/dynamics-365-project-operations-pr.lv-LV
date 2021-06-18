---
title: Jaunas vides nodrošināšana
description: Šajā tēmā ir sniegta informācija par to, kā nodrošināt jaunu Project Operations vidi.
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d0712d9d5dfc6c35ccd07142ff5948f50e6a254c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995495"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="8426a-103">Jaunas vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="8426a-103">Provision a new environment</span></span>

<span data-ttu-id="8426a-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="8426a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8426a-105">Šajā tēmā ir sniegta informācija par jaunas Dynamics 365 Project Operations vides nodrošināšanu scenārijiem, kas balstīti uz resursiem/bez krājumiem.</span><span class="sxs-lookup"><span data-stu-id="8426a-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="8426a-106">Project Operations automatizētās nodrošināšanas iespējošana LCS projektā</span><span class="sxs-lookup"><span data-stu-id="8426a-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="8426a-107">Veiciet tālāk norādītās darbības, lai iespējotu Project Operations automatizētās nodrošināšanas plūsmu savam LCS projektam.</span><span class="sxs-lookup"><span data-stu-id="8426a-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="8426a-108">Dodieties uz [LCS](https://lcs.dynamics.com/v2) un atlasiet elementu **Priekšskatījuma līdzekļa pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="8426a-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="8426a-109">Sarakstā **Priekšskatījuma līdzeklis** atlasiet **Project Operations līdzeklis** un pēc tam atlasiet **Priekšskatījuma līdzeklis iespējots**, lai iespējotu programmu Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8426a-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="8426a-110">Šī darbība tiek veikta tikai viereiz katrā LCS projektā.</span><span class="sxs-lookup"><span data-stu-id="8426a-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="8426a-111">Project Operations vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="8426a-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="8426a-112">Atveriet jaunu Dynamics 365 Finance [demonstrācijas vidi](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) vai [smilškastes/ražošanas vides](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) izvietojumu.</span><span class="sxs-lookup"><span data-stu-id="8426a-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="8426a-113">Veiciet vednī **Vidnes nodrošināšana** norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8426a-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8426a-114">Pārliecinieties, vai atlasītā lietojumprogrammas versija ir 10.0.13 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="8426a-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="8426a-115">Lai nodrošinātu Project Operations, sadaļā **Papildu iestatījumi** atlasiet **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="8426a-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="8426a-116">Iespējojiet **Common Data Service iestatījumu**, atlasot **Jā**, un pēc tam ievadiet informāciju obligātajos laukos:</span><span class="sxs-lookup"><span data-stu-id="8426a-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="8426a-117">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="8426a-117">Name</span></span>
  - <span data-ttu-id="8426a-118">Reģions</span><span class="sxs-lookup"><span data-stu-id="8426a-118">Region</span></span>
  - <span data-ttu-id="8426a-119">Valoda</span><span class="sxs-lookup"><span data-stu-id="8426a-119">Language</span></span>
  - <span data-ttu-id="8426a-120">Valūta</span><span class="sxs-lookup"><span data-stu-id="8426a-120">Currency</span></span>
 
5. <span data-ttu-id="8426a-121">Laukā **Common Data Service veidne** atlasiet **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="8426a-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="8426a-122">Atlasiet vides tipu savam izvietojumam.</span><span class="sxs-lookup"><span data-stu-id="8426a-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="8426a-123">Abonementam atbilstošs izmēģinājums ļaus jums izvietot CDS vidi 30 dienas.</span><span class="sxs-lookup"><span data-stu-id="8426a-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Izvietošanas iestatījumi](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="8426a-125">Atlasiet **Piekrist**, lai apstiprinātu pakalpojuma noteikumus, un pēc tam atlasiet **Gatavs**, lai atgrieztos izvietošanas iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="8426a-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Izvietošanas piekrišana](./media/2DeploymentConsent.png)

7. <span data-ttu-id="8426a-127">Neobligāti — Piemērojiet videi demonstrācijas datus.</span><span class="sxs-lookup"><span data-stu-id="8426a-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="8426a-128">Dodieties uz **Papildu iestatījumi**, atlasiet **Pielāgot SQL datu bāzes konfigurāciju** un iestatiet **Noteikt datu kopu lietojumprogrammas datu bāzei** uz **Demonstrācija**.</span><span class="sxs-lookup"><span data-stu-id="8426a-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="8426a-129">Aizpildiet pārējos obligātos laukus vednī un apstipriniet izvietošanu.</span><span class="sxs-lookup"><span data-stu-id="8426a-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="8426a-130">Laiks vides nodrošināšanai atšķiras atkarībā no vides veida.</span><span class="sxs-lookup"><span data-stu-id="8426a-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="8426a-131">Nodrošināšana var ilgt līdz sešām stundām.</span><span class="sxs-lookup"><span data-stu-id="8426a-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="8426a-132">Pēc veiksmīgas izvietošanas pabeigšanas vide tiks rādīta kā **Izvietota**.</span><span class="sxs-lookup"><span data-stu-id="8426a-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="8426a-133">Lai apstiprinātu, ka vide ir izvietota sekmīgi, atlasiet **Pieteikties** un piesakieties vidē, lai apstiprinātu.</span><span class="sxs-lookup"><span data-stu-id="8426a-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ vides informācija](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="8426a-135">Atjauninājumu lietošana Finance vidē</span><span class="sxs-lookup"><span data-stu-id="8426a-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="8426a-136">Programmai Project Operations ir nepieciešama Finance vide ar lietojumprogrammas versiju **10.0.13 (10.0.569.20009)** vai jaunāku versiju.</span><span class="sxs-lookup"><span data-stu-id="8426a-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="8426a-137">Lai saņemtu šo versiju, iespējams, jūsu Finance videi būs jālieto kvalitātes atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="8426a-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="8426a-138">LCS lapas **Vides informācija** sadaļā **Pieejamie atjauninājumi** atlasiet **Skatīt atjauninājumu**.</span><span class="sxs-lookup"><span data-stu-id="8426a-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Skatīt atjauninājumus](./media/5ViewUpdates.png)

2. <span data-ttu-id="8426a-140">Lapā **Binārie atjauninājumi** atlasiet **Saglabāt pakotni.**</span><span class="sxs-lookup"><span data-stu-id="8426a-140">On the **Binary updates** page, select **Save package.**</span></span>

![Saglabāt pakotni](./media/6SavePackage.png)

3. <span data-ttu-id="8426a-142">Noklikšķiniet uz **Atlasīt visu** un pēc tam atlasiet **Saglabāt pakotni**.</span><span class="sxs-lookup"><span data-stu-id="8426a-142">Click **Select all** and then select **Save package**.</span></span>

![Atjauninājumu pārskatīšana un saglabāšana](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="8426a-144">Ievadiet pakotnes nosaukumu un aprakstu un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8426a-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="8426a-145">Atkarībā no interneta savienojuma šis process var ilgt zināmu laiku.</span><span class="sxs-lookup"><span data-stu-id="8426a-145">Depending on the internet connection, this process might take some time.</span></span>

![Pakotnes augšupielāde līdzekļu bibliotēkā](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="8426a-147">Pēc tam, kad pakotne ir saglabāta, atlasiet **Gatavs** un saglabājiet šo pakotni sava LCS projekta līdzekļu bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="8426a-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="8426a-148">Pakotnes saglabāšana un validēšana var aizņemt aptuveni 15 minūtes.</span><span class="sxs-lookup"><span data-stu-id="8426a-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="8426a-149">Lai lietotu atjauninājumu, pārejiet uz LCS lapu **Vides informācija** un atlasiet **Uzturēt** > **Lietot atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="8426a-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Uzturēt vides](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="8426a-151">Atjauninājumu sarakstā atlasiet izveidoto pakotni un atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="8426a-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Lietot atjauninājumus](./media/10ApplyUpdates.png)

<span data-ttu-id="8426a-153">Vide apkalpošana aizņems zināmu laiku.</span><span class="sxs-lookup"><span data-stu-id="8426a-153">Environment servicing will take some time.</span></span> <span data-ttu-id="8426a-154">Pēc pabeigšanas vide atgriezīsies izvietotā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="8426a-154">After it is complete, the environment will return to a deployed state.</span></span>

![Izvietota vide](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="8426a-156">Duālās rakstīšanas savienojuma izveide</span><span class="sxs-lookup"><span data-stu-id="8426a-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="8426a-157">Savā LCS projektā dodieties uz lapu **Vides informācija**.</span><span class="sxs-lookup"><span data-stu-id="8426a-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8426a-158">Sadaļā **Common Data Service vides informācija** atlasiet **Saite uz CDS programmām**.</span><span class="sxs-lookup"><span data-stu-id="8426a-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="8426a-159">Pēc tam, kad saite ir izveidota, vēlreiz atlasiet **Saite uz CDS programmām**.</span><span class="sxs-lookup"><span data-stu-id="8426a-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="8426a-160">Jūs tiksit novirzīts uz duālo rakstīšanu risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="8426a-160">You will be redirected to Dual Write in Finance.</span></span>

![Saite uz CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="8426a-162">Atlasiet **Lietot risinājumu**, lai piekļūtu entītijām, kas tiks kartētas integrācijā.</span><span class="sxs-lookup"><span data-stu-id="8426a-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Lietot risinājumu](./media/13ApplySolutions.png)

5. <span data-ttu-id="8426a-164">Atlasiet abus risinājumus — **Dynamics 365 Finance and Operations divkāršās rakstīšanas entītiju kartējums** un **Dynamics 365 Project Operations divkāršās rakstīšanas entītiju kartējumi** un pēc tam atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="8426a-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Apstiprināt risinājumus](./media/14ConfirmSolutions.png)

<span data-ttu-id="8426a-166">Pēc risinājumu lietošanas duālās rakstīšanas entītijas tiek lietotas videi.</span><span class="sxs-lookup"><span data-stu-id="8426a-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Risinājumu lietošana](./media/15ApplyingSolutions.png)

<span data-ttu-id="8426a-168">Pēc entītiju lietošanas visi pieejamie kartējumi ir uzskaitīti vidē.</span><span class="sxs-lookup"><span data-stu-id="8426a-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Duālās rakstīšanas kartējumi](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="8426a-170">Pēc atjaunināšanas atsvaidziniet datu entītijas</span><span class="sxs-lookup"><span data-stu-id="8426a-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="8426a-171">Risinājumā Finance dodieties uz darbvietu **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="8426a-171">In Finance, go to the **Data management** workspace.</span></span>

![Datu pārvaldības darbvieta](./media/16DataManagement.png)

2. <span data-ttu-id="8426a-173">Atlasiet elementu **Struktūras parametri**.</span><span class="sxs-lookup"><span data-stu-id="8426a-173">Select the **Framework parameters** tile.</span></span>

![Struktūras parametri](./media/17FrameworkParameters.png)

3. <span data-ttu-id="8426a-175">Lapā **Entītiju iestatījumi** atlasiet **Atsvaidzināt entītiju sarakstu**.</span><span class="sxs-lookup"><span data-stu-id="8426a-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Atsvaidzināt entītiju sarakstu](./media/18RefreshEntityList.png)

<span data-ttu-id="8426a-177">Atsvaidzināšana aizņems aptuveni 20 minūtes.</span><span class="sxs-lookup"><span data-stu-id="8426a-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="8426a-178">Kad tā būs pabeigta, saņemsit brīdinājumu.</span><span class="sxs-lookup"><span data-stu-id="8426a-178">You will receive an alert when it is complete.</span></span>

![Atsvaidzināšanas apstiprināšana](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="8426a-180">Atjauniniet drošības iestatījumus Dataverse Project Operations</span><span class="sxs-lookup"><span data-stu-id="8426a-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="8426a-181">Dodieties uz Project Operations savā Dataverse vidē.</span><span class="sxs-lookup"><span data-stu-id="8426a-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="8426a-182">Atveriet **Iestatījumi** > **Drošība** > **Drošības lomas**.</span><span class="sxs-lookup"><span data-stu-id="8426a-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="8426a-183">Lapā **Drošības lomas** atlasiet **duālās rakstīšanas programmas lietotājs** un atlasiet cilni **Pielāgotās entitījas**.</span><span class="sxs-lookup"><span data-stu-id="8426a-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="8426a-184">Pārbaudiet, vai lomai ir **Lasīšanas** un **Pievienošanas atļaujas** elementiem:</span><span class="sxs-lookup"><span data-stu-id="8426a-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="8426a-185">**Valūtas maiņās kursa veids**</span><span class="sxs-lookup"><span data-stu-id="8426a-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="8426a-186">**Uzņēmumu tabula**</span><span class="sxs-lookup"><span data-stu-id="8426a-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="8426a-187">**Finanšu kalendārs**</span><span class="sxs-lookup"><span data-stu-id="8426a-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="8426a-188">**Virsgrāmata**</span><span class="sxs-lookup"><span data-stu-id="8426a-188">**Ledger**</span></span>

5. <span data-ttu-id="8426a-189">Pēc drošības lomas atjaunināšanas dodieties uz **Iestatījumi** > **Drošība** > **Darba grupas** un darba grupas skatā **Lokālā uzņēmuma īpašnieks** atlasiet noklusējuma darba grupu.</span><span class="sxs-lookup"><span data-stu-id="8426a-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="8426a-190">Atlasiet **Pārvaldīt lomas** un pārbaudiet, vai šai darba grupai tiek lietota drošības privilēģija **duālās rakstīšanas programmas lietotājs**.</span><span class="sxs-lookup"><span data-stu-id="8426a-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="8426a-191">Project Operations duālās rakstīšanas kartējumu palaišana</span><span class="sxs-lookup"><span data-stu-id="8426a-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="8426a-192">Savā LCS projektā dodieties uz lapu **Vides informācija**.</span><span class="sxs-lookup"><span data-stu-id="8426a-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8426a-193">Sadaļā **Common Data Service vides informācija** atlasiet **Saite uz CDS programmām.**</span><span class="sxs-lookup"><span data-stu-id="8426a-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="8426a-194">Pēc saites atlasīšanas tiksit novirzīts uz entītiju sarakstu kartējumos.</span><span class="sxs-lookup"><span data-stu-id="8426a-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="8426a-195">Startējiet kartējumus, kā aprakstīts tālāk redzamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="8426a-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="8426a-196">Noteikti izpildiet darbības parādītajā secībā.</span><span class="sxs-lookup"><span data-stu-id="8426a-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="8426a-197">**Entītiju kartējums**</span><span class="sxs-lookup"><span data-stu-id="8426a-197">**Entity Map**</span></span> | <span data-ttu-id="8426a-198">**Atsvaidzināt entītiju**</span><span class="sxs-lookup"><span data-stu-id="8426a-198">**Refresh entity**</span></span> | <span data-ttu-id="8426a-199">**Sākotnējā sinhronizācija**</span><span class="sxs-lookup"><span data-stu-id="8426a-199">**Initial sync**</span></span> | <span data-ttu-id="8426a-200">**Sākotnējās sinhronizācijas šablons**</span><span class="sxs-lookup"><span data-stu-id="8426a-200">**Master for initial sync**</span></span> | <span data-ttu-id="8426a-201">**Palaist priekšnosacījumus**</span><span class="sxs-lookup"><span data-stu-id="8426a-201">**Run prerequisites**</span></span> | <span data-ttu-id="8426a-202">**Priekšnosacījumu sākotnējā sinhronizācija**</span><span class="sxs-lookup"><span data-stu-id="8426a-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="8426a-203">**Projekta resursu lomas visiem uzņēmumiem (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="8426a-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="8426a-204">No</span><span class="sxs-lookup"><span data-stu-id="8426a-204">No</span></span> | <span data-ttu-id="8426a-205">Jā</span><span class="sxs-lookup"><span data-stu-id="8426a-205">Yes</span></span> | <span data-ttu-id="8426a-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8426a-206">Common Data Service</span></span> | <span data-ttu-id="8426a-207">No</span><span class="sxs-lookup"><span data-stu-id="8426a-207">No</span></span> | <span data-ttu-id="8426a-208">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-208">N\A</span></span> |
| <span data-ttu-id="8426a-209">**Juridiskas personas (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="8426a-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="8426a-210">No</span><span class="sxs-lookup"><span data-stu-id="8426a-210">No</span></span> | <span data-ttu-id="8426a-211">Jā</span><span class="sxs-lookup"><span data-stu-id="8426a-211">Yes</span></span> | <span data-ttu-id="8426a-212">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="8426a-212">Finance and Operations apps</span></span> | <span data-ttu-id="8426a-213">No</span><span class="sxs-lookup"><span data-stu-id="8426a-213">No</span></span> | <span data-ttu-id="8426a-214">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-214">N\A</span></span> |
| <span data-ttu-id="8426a-215">**Virsgrāmata (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="8426a-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="8426a-216">No</span><span class="sxs-lookup"><span data-stu-id="8426a-216">No</span></span> | <span data-ttu-id="8426a-217">Jā</span><span class="sxs-lookup"><span data-stu-id="8426a-217">Yes</span></span> | <span data-ttu-id="8426a-218">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="8426a-218">Finance and Operations apps</span></span> | <span data-ttu-id="8426a-219">Jā</span><span class="sxs-lookup"><span data-stu-id="8426a-219">Yes</span></span> | <span data-ttu-id="8426a-220">Jā, Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="8426a-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="8426a-221">**Project Operations integrācijas faktiskie dati (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="8426a-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="8426a-222">No</span><span class="sxs-lookup"><span data-stu-id="8426a-222">No</span></span> | <span data-ttu-id="8426a-223">No</span><span class="sxs-lookup"><span data-stu-id="8426a-223">No</span></span> | <span data-ttu-id="8426a-224">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-224">N\A</span></span> | <span data-ttu-id="8426a-225">Jā</span><span class="sxs-lookup"><span data-stu-id="8426a-225">Yes</span></span> | <span data-ttu-id="8426a-226">No</span><span class="sxs-lookup"><span data-stu-id="8426a-226">No</span></span> |
| <span data-ttu-id="8426a-227">**Projekta līguma rindas (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="8426a-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="8426a-228">No</span><span class="sxs-lookup"><span data-stu-id="8426a-228">No</span></span> | <span data-ttu-id="8426a-229">No</span><span class="sxs-lookup"><span data-stu-id="8426a-229">No</span></span> | <span data-ttu-id="8426a-230">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-230">N\A</span></span> | <span data-ttu-id="8426a-231">No</span><span class="sxs-lookup"><span data-stu-id="8426a-231">No</span></span> | <span data-ttu-id="8426a-232">No</span><span class="sxs-lookup"><span data-stu-id="8426a-232">No</span></span> |
| <span data-ttu-id="8426a-233">**Integrāciju entitīja projekta transakciju relācijām (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="8426a-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="8426a-234">No</span><span class="sxs-lookup"><span data-stu-id="8426a-234">No</span></span> | <span data-ttu-id="8426a-235">No</span><span class="sxs-lookup"><span data-stu-id="8426a-235">No</span></span> | <span data-ttu-id="8426a-236">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-236">N\A</span></span> | <span data-ttu-id="8426a-237">No</span><span class="sxs-lookup"><span data-stu-id="8426a-237">No</span></span> | <span data-ttu-id="8426a-238">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-238">N\A</span></span> |
| <span data-ttu-id="8426a-239">**Project Operations integrācijas līguma rindu atskaites punkti (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="8426a-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="8426a-240">No</span><span class="sxs-lookup"><span data-stu-id="8426a-240">No</span></span> | <span data-ttu-id="8426a-241">No</span><span class="sxs-lookup"><span data-stu-id="8426a-241">No</span></span> | <span data-ttu-id="8426a-242">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-242">N\A</span></span> | <span data-ttu-id="8426a-243">No</span><span class="sxs-lookup"><span data-stu-id="8426a-243">No</span></span> | <span data-ttu-id="8426a-244">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-244">N\A</span></span> |
| <span data-ttu-id="8426a-245">**Project Operations integrācijas entītija izdevumu aprēķiniem (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="8426a-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="8426a-246">No</span><span class="sxs-lookup"><span data-stu-id="8426a-246">No</span></span> | <span data-ttu-id="8426a-247">No</span><span class="sxs-lookup"><span data-stu-id="8426a-247">No</span></span> | <span data-ttu-id="8426a-248">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-248">N\A</span></span> | <span data-ttu-id="8426a-249">No</span><span class="sxs-lookup"><span data-stu-id="8426a-249">No</span></span> | <span data-ttu-id="8426a-250">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-250">N\A</span></span> |
| <span data-ttu-id="8426a-251">**Project Operations integrācijas projekta izdevumu kategorijas eksporta entītija (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="8426a-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="8426a-252">No</span><span class="sxs-lookup"><span data-stu-id="8426a-252">No</span></span> | <span data-ttu-id="8426a-253">No</span><span class="sxs-lookup"><span data-stu-id="8426a-253">No</span></span> | <span data-ttu-id="8426a-254">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-254">N\A</span></span> | <span data-ttu-id="8426a-255">No</span><span class="sxs-lookup"><span data-stu-id="8426a-255">No</span></span> | <span data-ttu-id="8426a-256">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-256">N\A</span></span> |
| <span data-ttu-id="8426a-257">**Project Operations integrācijas projekta izdevumu eksporta entītija (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="8426a-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="8426a-258">Jā</span><span class="sxs-lookup"><span data-stu-id="8426a-258">Yes</span></span> | <span data-ttu-id="8426a-259">No</span><span class="sxs-lookup"><span data-stu-id="8426a-259">No</span></span> | <span data-ttu-id="8426a-260">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-260">N\A</span></span> | <span data-ttu-id="8426a-261">No</span><span class="sxs-lookup"><span data-stu-id="8426a-261">No</span></span> | <span data-ttu-id="8426a-262">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-262">N\A</span></span> |
| <span data-ttu-id="8426a-263">**Project Operations integrācijas entītija stundu aprēķiniem (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="8426a-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="8426a-264">Jā</span><span class="sxs-lookup"><span data-stu-id="8426a-264">Yes</span></span> | <span data-ttu-id="8426a-265">No</span><span class="sxs-lookup"><span data-stu-id="8426a-265">No</span></span> | <span data-ttu-id="8426a-266">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-266">N\A</span></span> | <span data-ttu-id="8426a-267">No</span><span class="sxs-lookup"><span data-stu-id="8426a-267">No</span></span> | <span data-ttu-id="8426a-268">N/A</span><span class="sxs-lookup"><span data-stu-id="8426a-268">N\A</span></span> |


4. <span data-ttu-id="8426a-269">Lai atsvaidzinātu entītiju, atlasiet kartējuma nosaukumu un pēc tam atlasiet **Atsvaidzināt entītijas**.</span><span class="sxs-lookup"><span data-stu-id="8426a-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Atsvaidzināt kartējumu](./media/20RefreshMapping.png)

5. <span data-ttu-id="8426a-271">Kad atsvaidzināšana ir pabeigta, palaidiet karti.</span><span class="sxs-lookup"><span data-stu-id="8426a-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="8426a-272">Pirms nākamā kartējuma iespējošanas pārliecinieties, vai kartējumam tabulā ir statuss **Darbojas**.</span><span class="sxs-lookup"><span data-stu-id="8426a-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="8426a-273">Kartējumu ar lielāku priekšnosacījumu skaitu palaišana var aizņemt zināmu laiku.</span><span class="sxs-lookup"><span data-stu-id="8426a-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="8426a-274">Lai palaistu kartējumu ar priekšnosacījumiem, iespējojiet pārslēgšanas pogu **Rādīt saistītos entītiju kartējumus**.</span><span class="sxs-lookup"><span data-stu-id="8426a-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="8426a-275">Ja tabulā redzams, ka vienumam **Priekšnosacījumu sākotnējā sinhronizācija** ir vērtība **Nē**, pirms palaišanas pārbaudiet, vai **Sākotnējās sinhronizācijas** karodziņš ir **Izslēgts** visos priekšnosacījumu kartējumos.</span><span class="sxs-lookup"><span data-stu-id="8426a-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Palaist kartējumu](./media/21RunMap.png)

6. <span data-ttu-id="8426a-277">Pārbaudiet, vai visiem ar projektu saistītajiem kartējumiem ir statuss Darbojas.</span><span class="sxs-lookup"><span data-stu-id="8426a-277">Validate all project related maps are in the running state.</span></span>

![Visi kartējumi darbojas](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="8426a-279">Konfigurācijas datu lietošana pakalpojumā CDS lietojumprogrammai Project Operations (izvēles)</span><span class="sxs-lookup"><span data-stu-id="8426a-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="8426a-280">Ja esat lietojis demonstrācijas datus finanšu vidē, skatiet sadaļu [Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service risinājumam Project Operations](resource-apply-pro-setup-config-data.md), lai lietotu demonstrācijas datus CDS vidē.</span><span class="sxs-lookup"><span data-stu-id="8426a-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="8426a-281">Jūsu Project Operations vide tagad ir nodrošināta un konfigurēta.</span><span class="sxs-lookup"><span data-stu-id="8426a-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]