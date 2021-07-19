---
title: Manuāla programmas Project Operations Dataverse ar duālās rakstīšanas atbalstu izvietošana
description: Šajā tēmā izskaidrots, kā manuāli izvietot programmu Project Operations Dataverse, lai tā atbalstītu duālo rakstīšanu.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274017"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="382da-103">Manuāla programmas Project Operations Dataverse ar duālās rakstīšanas atbalstu izvietošana</span><span class="sxs-lookup"><span data-stu-id="382da-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="382da-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="382da-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="382da-105">Šajā tēmā izskaidrots, kā manuāli izvietot Microsoft Dynamics 365 Project Operations programmā Microsoft Dataverse, lai tā atbalstītu duālo rakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="382da-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="382da-106">Project Operations konstatē vides konfigurāciju un pievieno papildu atbalstu attiecībā duālajai rakstīšanai, ja tiek izpildīti priekšnosacījumi.</span><span class="sxs-lookup"><span data-stu-id="382da-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="382da-107">Veicot izvietošanu, izmantojot Microsoft Dynamics Lifecycle Services (LCS), ja ir izpildīti šajā tēmā sniegtie norādījumi, varat izlaist integrācijas Microsoft Power Platform (iepriekš zināma kā Common Data Service vide) izvietošanu.</span><span class="sxs-lookup"><span data-stu-id="382da-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="382da-108">Project Operations izvietošanas procesam Dataverse, lai tas atbalstītu duālo rakstīšanu, jāveic četras galvenās darbības.</span><span class="sxs-lookup"><span data-stu-id="382da-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="382da-109">[Jaunas vides izveide programmā Dataverse, kurā tiek atbalstīta duālā rakstīšana](#create).</span><span class="sxs-lookup"><span data-stu-id="382da-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="382da-110">[Duālās rakstīšanas priekšnosacījumu pievienošana videi](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="382da-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="382da-111">[Programmas Project Operations Dataverse pievienošana](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="382da-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="382da-112">[Vižu saistīšana](#link).</span><span class="sxs-lookup"><span data-stu-id="382da-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="382da-113">Izveidojiet jaunu vidi programmā Dataverse, kurā tiek atbalstīta duālā rakstīšana.</span><span class="sxs-lookup"><span data-stu-id="382da-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="382da-114">Lai pabeigtu šo procedūru, jāpiesakās kā administratoram.</span><span class="sxs-lookup"><span data-stu-id="382da-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="382da-115">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.com) un piesakieties kā administrators.</span><span class="sxs-lookup"><span data-stu-id="382da-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="382da-116">Izveidojiet jaunu vidi un piešķiriet tai nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="382da-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="382da-117">Atlasiet vides tipu.</span><span class="sxs-lookup"><span data-stu-id="382da-117">Select the environment type.</span></span> <span data-ttu-id="382da-118">Ja reģistrējāties izmēģinājumversijas piedāvājumam, atlasiet **Izmēģinājumversija (abonementa)**.</span><span class="sxs-lookup"><span data-stu-id="382da-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="382da-119">Apstipriniet izvietošanas reģionu.</span><span class="sxs-lookup"><span data-stu-id="382da-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="382da-120">Iespējojiet opciju **Izveidot datu bāzi šai videi**.</span><span class="sxs-lookup"><span data-stu-id="382da-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="382da-121">Apstipriniet valodu un pēc tam apstipriniet, ka valūta atbilst jūsu programmu Finance and Operations valūtai.</span><span class="sxs-lookup"><span data-stu-id="382da-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="382da-122">Iespējojiet opciju **Dynamics 365 programmas** un pārliecinieties, ka lauks **Automātiski izvietot šīs programmas** ir iestatīts kā **Neviens**.</span><span class="sxs-lookup"><span data-stu-id="382da-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="382da-123">Ja ir nepieciešama drošības grupa, pievienojiet to.</span><span class="sxs-lookup"><span data-stu-id="382da-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="382da-124">Atlasiet **Saglabāt**, lai izveidotu vidi.</span><span class="sxs-lookup"><span data-stu-id="382da-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="382da-125">Uzgaidiet, līdz izvietošana ir pabeigta un vide sasniedz statusu **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="382da-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="382da-126">Duālās rakstīšanas priekšnosacījumu pievienošana videi</span><span class="sxs-lookup"><span data-stu-id="382da-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="382da-127">Duālās rakstīšanas atbalsts ietver papildu laukus, kas tiek pievienoti galvenajām entītijām, piemēram, entītijai **Uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="382da-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="382da-128">Ja pievienojat satura rakstīšanas atbalstu esošai videi, iespējams, būs jāatjaunina dati, lai iespējotu atbalstu.</span><span class="sxs-lookup"><span data-stu-id="382da-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="382da-129">Informāciju par to, kā veikt datu palaišanu, skatiet sadaļā [Uzņēmuma datu palaišana](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="382da-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="382da-130">Papildinformāciju par duālo rakstīšanu skatiet sadaļā [Duālās rakstīšanas sistēmas prasības](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="382da-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="382da-131">Izpildiet šo procedūru, lai pievienotu videi duālās rakstīšanas priekšnosacījumus.</span><span class="sxs-lookup"><span data-stu-id="382da-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="382da-132">Atveriet tikko izveidoto vidi un pēc tam atveriet **Resurss** \> **Dynamics 365 programmas**.</span><span class="sxs-lookup"><span data-stu-id="382da-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="382da-133">Programmu sarakstā atlasiet **Duālās rakstīšanas pamata risinājums** un instalējiet to.</span><span class="sxs-lookup"><span data-stu-id="382da-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="382da-134">Uzgaidiet, līdz instalēšana ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="382da-134">Wait until the installation is completed.</span></span> <span data-ttu-id="382da-135">Pēc tam programmu sarakstā atlasiet **Duālās rakstīšanas saskaņotais risinājums** un instalējiet to.</span><span class="sxs-lookup"><span data-stu-id="382da-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="382da-136">Programmas Project Operations Dataverse pievienošana</span><span class="sxs-lookup"><span data-stu-id="382da-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="382da-137">Šo procedūru var izpildīt tikai tad, ja pirms Project Operations instalēšanas ir izpildītas iepriekšējās procedūras.</span><span class="sxs-lookup"><span data-stu-id="382da-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="382da-138">Instalācijas laikā sistēma analizē vides konfigurāciju un pievieno atbalstu duālajai rakstīšanai, ja tā ir nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="382da-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="382da-139">Atveriet iepriekš izveidoto vidi un pēc tam atveriet **Resurss** \> **Dynamics 365 programmas**.</span><span class="sxs-lookup"><span data-stu-id="382da-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="382da-140">Programmu sarakstā atlasiet **Microsoft Dynamics 365 Project Operations** un instalējiet to.</span><span class="sxs-lookup"><span data-stu-id="382da-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="382da-141">Vižu saistīšana</span><span class="sxs-lookup"><span data-stu-id="382da-141">Link your environments</span></span>

<span data-ttu-id="382da-142">Kad Dataverse vide ir izvietota, varat iestatīt saiti Finance and Operations programmās.</span><span class="sxs-lookup"><span data-stu-id="382da-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="382da-143">Izpildiet darbības, kas norādītas sadaļā [Duālās rakstīšanas vedņa izmantošana vižu saistīšanai](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="382da-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
