---
title: Azure abonementa pievienošana LCS projektam
description: Šajā tēmā ir sniegta informācija par to, kā pievienot Azure abonementu LCS projektam.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad1ddd69cbb8db7780b8277a7ed7533d3ea3d053
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289918"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="c5f02-103">Azure abonementa pievienošana LCS projektam</span><span class="sxs-lookup"><span data-stu-id="c5f02-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="c5f02-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="c5f02-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c5f02-105">Mākoņpakalpojumā viesotas vides ir jāizvieto, izmantojot esošu Azure abonementu.</span><span class="sxs-lookup"><span data-stu-id="c5f02-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="c5f02-106">Šajā tēmā ir izskaidrots, kā pievienot esošu Azure abonementu LCS projektam.</span><span class="sxs-lookup"><span data-stu-id="c5f02-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="c5f02-107">Administratora piekrišanas piešķiršana</span><span class="sxs-lookup"><span data-stu-id="c5f02-107">Grant admin consent</span></span>

1. <span data-ttu-id="c5f02-108">Sava LCS projekta sadaļā **Vides** atlasiet **Microsoft Azure iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="c5f02-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Microsoft Azure iestatījumi](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="c5f02-110">Lapas **Projekta iestatījumi** cilnē **Azure savienotāji** atlasiet **Autorizēt**.</span><span class="sxs-lookup"><span data-stu-id="c5f02-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="c5f02-111">Tas ļauj izvietot vides šajā projektā.</span><span class="sxs-lookup"><span data-stu-id="c5f02-111">This allows environments to be deployed to this project.</span></span>

![Azure savienotāji](./media/2AzureConnectors.png)

3. <span data-ttu-id="c5f02-113">Vēlreiz atlasiet **Autorizēt**, lai sniegtu administratora piekrišanu.</span><span class="sxs-lookup"><span data-stu-id="c5f02-113">Select **Authorize** again to provide admin consent.</span></span>

![Administratora piekrišanas piešķiršana](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="c5f02-115">Piekrītiet atļauju pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="c5f02-115">Accept the permissions request.</span></span>

![Piekrist atļaujas pieprasījumam](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="c5f02-117">Autorizācija tagad ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="c5f02-117">The authorization is now complete.</span></span> 

![Autorizācija ir veiksmīga](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="c5f02-119">Piekļuves sniegšana pakalpojumam Dynamics Deployment Services jūsu Azure abonementam</span><span class="sxs-lookup"><span data-stu-id="c5f02-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="c5f02-120">Dodieties uz [Microsoft Azure norēķini](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) un atlasiet savu abonementu.</span><span class="sxs-lookup"><span data-stu-id="c5f02-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="c5f02-121">Pakalpojumam Dynamics Deployment Services ir nepieciešama piekļuve šim abonementam, lai varētu izvietot vides.</span><span class="sxs-lookup"><span data-stu-id="c5f02-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure abonementa informācija](./media/6AzureSubscription.png)

2. <span data-ttu-id="c5f02-123">Navigācijas rūtī atlasiet **Piekļuves kontrole (IAM)** un pēc tam atlasiet **Pievienot lomas piešķiri**.</span><span class="sxs-lookup"><span data-stu-id="c5f02-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="c5f02-124">Labajā pusē esošajā slīdnī atlasiet **Līdzstrādnieka loma** un piedāvātajā sarakstā atrodiet un atlasiet **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="c5f02-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="c5f02-125">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c5f02-125">Select **Save**.</span></span>

![Piekļuve abonementam](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="c5f02-127">Abonementa savienotāja pievienošana LCS projektam</span><span class="sxs-lookup"><span data-stu-id="c5f02-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="c5f02-128">Sava LCS projekta lapā **Microsoft Azure iestatījumi** atlasiet **Pievienot**, lai pievienotu jaunu savienotāju.</span><span class="sxs-lookup"><span data-stu-id="c5f02-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="c5f02-129">Ievadiet sava Azure abonementa ID.</span><span class="sxs-lookup"><span data-stu-id="c5f02-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="c5f02-130">Sava Azure abonementa ID varat atrast [Azure portāla](https://ms.portal.azure.com/) sadaļā **Iestatījumi** ekrāna apakšējā kreisajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="c5f02-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="c5f02-131">Laukā **Konfigurēt Azure Resource Manager izmantošanu** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c5f02-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="c5f02-132">Pārliecinieties, vai Azure abonementa AAD nomnieka domēns atbilst jūsu izmantotajam Azure abonementam, kam pieder domēns, un atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="c5f02-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="c5f02-133">Ekrānā **Microsoft Azure iestatīšana** atlasiet **Tālāk**, lai apstiprinātu.</span><span class="sxs-lookup"><span data-stu-id="c5f02-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="c5f02-134">Ja šajā ekrānā tiek parādīts kļūdas ziņojums, atgriezieties šīs tēmas sadaļā [Piekļuves sniegšana pakalpojumam Dynamics Deployment Services jūsu Azure abonementam](#provide) un pārliecinieties, vai esat izpildījis visas darbības.</span><span class="sxs-lookup"><span data-stu-id="c5f02-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="c5f02-135">Lejupielādējiet Azure pārvaldības sertifikātu lokālā mapē savā datorā un pēc tam augšupielādējiet to Azure pārvaldības portālā, atverot **Iestatījumi** > **Pārvaldības sertifikāti**.</span><span class="sxs-lookup"><span data-stu-id="c5f02-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="c5f02-136">Šis sertifikāts ļaus LCS sazināties ar Azure jūsu vārdā.</span><span class="sxs-lookup"><span data-stu-id="c5f02-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="c5f02-137">Ja lietotājam ir piekļuve abonementam, varat izlaist šo darbību.</span><span class="sxs-lookup"><span data-stu-id="c5f02-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="c5f02-138">Atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="c5f02-138">Select  **Next**.</span></span>
8. <span data-ttu-id="c5f02-139">Atlasiet Azure reģionu, kurā veikt izvietošanu, un atlasiet datu centru, kas atrodas tuvu vietai, kurā plānojat lietot šo sistēmu.</span><span class="sxs-lookup"><span data-stu-id="c5f02-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="c5f02-140">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="c5f02-140">Select  **Connect**.</span></span>

<span data-ttu-id="c5f02-141">Esat veiksmīgi pievienojis savu Azure abonementu.</span><span class="sxs-lookup"><span data-stu-id="c5f02-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="c5f02-142">Tagad varat izvietot Dynamics 365 Finance mākoņpakalpojumā viesotas vides.</span><span class="sxs-lookup"><span data-stu-id="c5f02-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]