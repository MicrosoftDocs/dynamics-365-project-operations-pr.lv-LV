---
title: Demonstrācijas datu lietošana Finance mākoņpakalpojumā viesotā vidē
description: Šajā tēmā ir izskaidrots, kā lietot Project Operations demonstrācijas datus Dynamics 365 Finance mākoņpakalpojumā viesotā vidē.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d8a198b3bfd71ae08bc338d17896519b5ffd6b8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000175"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="b0fcd-103">Demonstrācijas datu lietošana Finance mākoņpakalpojumā viesotā vidē</span><span class="sxs-lookup"><span data-stu-id="b0fcd-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="b0fcd-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="b0fcd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0fcd-105">Šī tēma attiecas tikai uz Microsoft Dynamics 365 Finance versiju 10.0.13, un tajā sniegtos norādījumus var izpildīt tikai mākoņpakalpojumā viesotā vidē.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="b0fcd-106">Izpildiet šajā tēmā aprakstītās darbības, **PIRMS** lietojat kvalitātes atjauninājumus videi.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="b0fcd-107">Savā LCS projektā atveriet lapu **Vides informācija**.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="b0fcd-108">Ņemiet vērā, ka tajā ir iekļauta informācija, kas nepieciešama, lai izveidotu savienojumu ar vidi, izmantojot attālās darbvirsmas protokolu (RDP).</span><span class="sxs-lookup"><span data-stu-id="b0fcd-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![ vides informācija](./media/1EnvironmentDetails.png)

<span data-ttu-id="b0fcd-110">Pirmā iezīmēto akreditācijas datu kopa ir lokālā konta akreditācijas dati, un tajā ir ietverta hipersaite uz attālās darbvirsmas savienojumu.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="b0fcd-111">Akreditācijas dati ietver vides administratora lietotājvārdu un paroli.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="b0fcd-112">Otrā akreditācijas datu kopa tiek izmantota, lai šajā vidē pieteiktos programmā SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="b0fcd-113">Izveidojiet attālo savienojumu ar vidi, izmantojot sadaļā **Lokālie konti** esošo hipersaiti, un izmantojiet **Lokālā konta akreditācijas datus**, lai veiktu autentifikāciju.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="b0fcd-114">Dodieties uz **Interneta informācijas pakalpojumi** > **Lietojumprogrammas kopas** > **AOSService** un apturiet pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="b0fcd-115">Jūs pašlaik apturat pakalpojuma darbību, lai varētu turpināt aizstāt SQL datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Apturēt AOS](./media/2StopAOS.png)

4. <span data-ttu-id="b0fcd-117">Dodieties uz **Pakalpojumi** un apturiet šādus divus elementus:</span><span class="sxs-lookup"><span data-stu-id="b0fcd-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="b0fcd-118">Microsoft Dynamics 365 Unified Operations: lielapjoma pārvaldības pakalpojums</span><span class="sxs-lookup"><span data-stu-id="b0fcd-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="b0fcd-119">Microsoft Dynamics 365 Unified Operations: datu importēšanas un eksportēšanas struktūra</span><span class="sxs-lookup"><span data-stu-id="b0fcd-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Apturēt pakalpojumus](./media/3StopServices.png)

5. <span data-ttu-id="b0fcd-121">Atveriet Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="b0fcd-122">Piesakieties, izmantojot SQL Server akreditācijas datus, un izmantojiet LCS lapā **Vides informācija** norādīto axdbadmin lietotājvārdu un paroli.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="b0fcd-124">Objektu pārlūka sadaļā **Datu bāzes** atrodiet **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="b0fcd-125">Datu bāze tiks aizstāta ar jaunu datu bāzi, kas atrodas [lejupielādes centrā](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="b0fcd-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="b0fcd-126">Nokopējiet .zip failu virtuālajā mašīnā, ar ko ir izveidots attālais savienotjums, un izgūstiet .zip saturu.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="b0fcd-127">Programmā SQL Server Management Studio ar peles labo pogu noklikšķiniet uz **AxDB** un pēc tam atlasiet **Uzdevumi** > **Atjaunot** > **Datu bāze**.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Atjaunot datu bāzi](./media/5RestoreDatabase.png)

9. <span data-ttu-id="b0fcd-129">Atlasiet **Avota ierīce** un pārejiet uz failu, kas tika izvilkts no jūsu kopētā .zip faila.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Avota ierīces](./media/6SourceDevice.png)

10. <span data-ttu-id="b0fcd-131">Atlasiet **Opcijas** un pēc tam atlasiet **Pārrakstīt esošo datu bāzi** un **Aizvērt esošos savienojumus ar mērķa datu bāzi**.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="b0fcd-132">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-132">Select **OK**.</span></span>

![Atjaunot iestatījumus](./media/7RestoreSetting.png)

<span data-ttu-id="b0fcd-134">Jūs saņemsit apstiprinājumu par to, ka AXDB atjaunošana izdevās.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="b0fcd-135">Pēc šī apstiprinājuma saņemšanas varat aizvērt SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="b0fcd-136">Dodieties atpakaļ uz **Interneta informācijas pakalpojumi** > **Lietojumprogrammas kopas** > **AOSService** un startējiet AOSService.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="b0fcd-137">Atveriet sadaļu **Pakalpojumi** un startējiet abus iepriekš apturētos pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="b0fcd-138">Atrodiet šajā virtuālajā mašīnā rīku AdminUserProvisioning.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="b0fcd-139">Meklējiet šeit: K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="b0fcd-140">Palaidiet .ext failu, izmantojot savu lietotāja adresi laukā **E-pasta adrese**.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="b0fcd-141">Atlasiet **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-141">Select **Submit**.</span></span>

![Lietotāja ar administratora atļaujām nodrošināšana](./media/8AdminUserProvisioning.png)

<span data-ttu-id="b0fcd-143">Procesa pabeigšanai nepieciešamas dažas minūtes.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="b0fcd-144">Jūs saņemsit apstiprinājuma ziņojumu par to, ka lietotājs ar administratora atļaujām tika veiksmīgi atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="b0fcd-145">Visbeidzot, palaidiet komandu uzvedni kā administrators un veiciet IIS atiestatīšanu</span><span class="sxs-lookup"><span data-stu-id="b0fcd-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS atiestatīšana](./media/9IISReset.png)

18. <span data-ttu-id="b0fcd-147">Aizveriet attālās darbvirsmas sesiju un izmantojiet LCS lapu **Vides informācija**, lai pieteiktos vidē un pārliecinātos, vai tā darbojas, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="b0fcd-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]