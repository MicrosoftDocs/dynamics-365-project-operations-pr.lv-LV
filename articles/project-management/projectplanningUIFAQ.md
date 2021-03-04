---
title: Problēmu novēršana, strādājot ar uzdevuma režģi
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kura ir nepieciešama, strādājot uzdevumu režģī.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031546"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="6b147-103">Problēmu novēršana, strādājot ar uzdevuma režģi</span><span class="sxs-lookup"><span data-stu-id="6b147-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="6b147-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="6b147-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6b147-105">Šajā tēmā aprakstīts, kā novērst problēmas, ar kurām, iespējams, saskarsities, strādājot ar izmaksu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="6b147-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="6b147-106">Sīkfaili iespējoti</span><span class="sxs-lookup"><span data-stu-id="6b147-106">Enable cookies</span></span>

<span data-ttu-id="6b147-107">Project Operations ir nepieciešams, lai būtu iespējoti trešo pušu sīkfaili, lai atveidotu darba sadalījuma struktūru.</span><span class="sxs-lookup"><span data-stu-id="6b147-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="6b147-108">Ja nav iespējoti trešo pušu sīkfaili, jūs redzēsit nevis uzdevumus, bet gan tukšu lapu, ja lapā **Projekts** atlasīsit cilni **Uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="6b147-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Tukša cilne, ja nav iespējoti trešo pušu sīkfaili](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="6b147-110">Risinājums</span><span class="sxs-lookup"><span data-stu-id="6b147-110">Workaround</span></span>
<span data-ttu-id="6b147-111">Microsoft Edge vai Google Chrome pārlūkiem šīs procedūras izklāsta, kā atjaunināt pārlūka iestatījumu, lai iespējotu trešo pušu sīkfailus.</span><span class="sxs-lookup"><span data-stu-id="6b147-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="6b147-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6b147-112">Microsoft Edge</span></span>

1. <span data-ttu-id="6b147-113">Atveriet pārlūkprogrammu Edge.</span><span class="sxs-lookup"><span data-stu-id="6b147-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="6b147-114">Augšējā labajā stūrī atlasiet **daudzpunkti** (...) un pēc tam atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="6b147-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="6b147-115">Sadaļā **Sīkfaili un vietnes atļaujas** atlasiet **Sīkfaili un vietnes dati**.</span><span class="sxs-lookup"><span data-stu-id="6b147-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="6b147-116">Izslēdziet opciju **Bloķēt trešās puses sīkfailus**.</span><span class="sxs-lookup"><span data-stu-id="6b147-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="6b147-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="6b147-117">Google Chrome</span></span>

1. <span data-ttu-id="6b147-118">Atveriet pārlūkprogrammu Chrome.</span><span class="sxs-lookup"><span data-stu-id="6b147-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="6b147-119">Augšējā labajā stūrī atlasiet trīs vertikālus punktus un pēc tam atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="6b147-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="6b147-120">Sadaļā **Privātums un drošība** atlasiet **Sīkfaili un citi vietnes dati**.</span><span class="sxs-lookup"><span data-stu-id="6b147-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="6b147-121">Atlasiet **Atļaut visus sīkfailus**.</span><span class="sxs-lookup"><span data-stu-id="6b147-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b147-122">Ja bloķējat trešo pušu sīkfailus, tiks bloķēti visi sīkfaili un vietnes dati no citām vietnēm pat, ja vietne ir atļauta jūsu izņēmumu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="6b147-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="6b147-123">PEX galapunkts</span><span class="sxs-lookup"><span data-stu-id="6b147-123">PEX Endpoint</span></span>

<span data-ttu-id="6b147-124">Project Operations vajadzībām projekta parametrs norāda uz PEX galapunktu.</span><span class="sxs-lookup"><span data-stu-id="6b147-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="6b147-125">Šis galapunkts ir nepieciešams, lai sazinātos ar servisu, kas tiek izmantots darba sadalījuma struktūras atveidošanas nolūkam.</span><span class="sxs-lookup"><span data-stu-id="6b147-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="6b147-126">Ja parametrs nav iespējots, saņemsit kļūdu "Projekta parametrs nav derīgs".</span><span class="sxs-lookup"><span data-stu-id="6b147-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="6b147-127">Risinājums</span><span class="sxs-lookup"><span data-stu-id="6b147-127">Workaround</span></span>
 ![Projekta parametra lauks PEX galapunkts](media/projectparameter.png)

1. <span data-ttu-id="6b147-129">Pievienojiet **PEX galapunkta** lauku **Projekta parametru** lapai.</span><span class="sxs-lookup"><span data-stu-id="6b147-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="6b147-130">Atjauniniet lauku ar šādu vērtību: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="6b147-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="6b147-131">Noņemiet lauku no **Projekta parametru** lapas.</span><span class="sxs-lookup"><span data-stu-id="6b147-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="6b147-132">Projekta atļaujas tīmeklī</span><span class="sxs-lookup"><span data-stu-id="6b147-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="6b147-133">Project Operations ir atkarīgs no ārēja plānošanas servisa.</span><span class="sxs-lookup"><span data-stu-id="6b147-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="6b147-134">Šim servisam ir nepieciešams, ka lietotājam ir piešķiras vairākas lomas lasīt un rakstīt entitījās, kas saistītas ar darba sadalījuma struktūru.</span><span class="sxs-lookup"><span data-stu-id="6b147-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="6b147-135">Šīs entitījas ietver projekta uzdevumus, resursu piešķiri un uzdevumu atkarības.</span><span class="sxs-lookup"><span data-stu-id="6b147-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="6b147-136">Ja lietotājs nevar atveidot darba sadalījuma struktūru, dodoties uz cilni **Uzdevumi**, tas visdrīzāk ir tāpēc, ka nav iespējots Project Operations projekts.</span><span class="sxs-lookup"><span data-stu-id="6b147-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="6b147-137">Lietotājs var saņemt vai nu drošības lomas kļūdu vai kļūdu, kas saistīta ar piekļuves liegumu.</span><span class="sxs-lookup"><span data-stu-id="6b147-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="6b147-138">Risinājums</span><span class="sxs-lookup"><span data-stu-id="6b147-138">Workaround</span></span>

1. <span data-ttu-id="6b147-139">Dodieties uz **Iestatījumi > Drošība > Lietotāji > Programmas lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="6b147-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Lietojumprogrammas lasītājs](media/applicationuser.jpg)
   
2. <span data-ttu-id="6b147-141">Veiciet dubultklikšķi uz lietojumprogrammas lietotāja ieraksta, lai pārbaudītu tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="6b147-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="6b147-142">Lietotājam ir piekļuve projektam.</span><span class="sxs-lookup"><span data-stu-id="6b147-142">The user has access to the project.</span></span> <span data-ttu-id="6b147-143">Šo pārbaudi parasti veic, nodrošinot, ka lietotājam ir drošības loma **Projekta vadītājs**.</span><span class="sxs-lookup"><span data-stu-id="6b147-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="6b147-144">Microsoft Project lietojumprogrammas lietotājs pastāv un ir pareizi konfigurēts.</span><span class="sxs-lookup"><span data-stu-id="6b147-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="6b147-145">Ja šis lietotājs nepastāv, varat izveidot jauna lietotāja ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6b147-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="6b147-146">Atlasiet **Jauni lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="6b147-146">Select **New Users**.</span></span> <span data-ttu-id="6b147-147">Mainiet ievades veidlapu uz **Lietojumprogrammas lietotājs** un pēc tam pievienojiet **Lietojumprogrammas ID**.</span><span class="sxs-lookup"><span data-stu-id="6b147-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Lietojumprogrammas lietotāja informācija](media/applicationuserdetails.jpg)

4. <span data-ttu-id="6b147-149">Pārbaudiet, vai lietotājam ir piešķirta pareizā licence un vai serviss ir iespējots licences servisa plānu informācijā.</span><span class="sxs-lookup"><span data-stu-id="6b147-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="6b147-150">Pārbaudiet, vai lietotājs var atvērt project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="6b147-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="6b147-151">Ar projekta parametriem pārbaudiet, vai sistēma norāda uz pareizo projekta galapunktu.</span><span class="sxs-lookup"><span data-stu-id="6b147-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="6b147-152">Pārbaudiet, vai ir izveidots projekta lietojumprogrammas lietotājs.</span><span class="sxs-lookup"><span data-stu-id="6b147-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="6b147-153">Piemērojiet lietotājam šādas drošības lomas:</span><span class="sxs-lookup"><span data-stu-id="6b147-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="6b147-154">Dataverse lietotājs</span><span class="sxs-lookup"><span data-stu-id="6b147-154">Dataverse User</span></span>
  - <span data-ttu-id="6b147-155">Project Operations sistēma</span><span class="sxs-lookup"><span data-stu-id="6b147-155">Project Operations System</span></span>
  - <span data-ttu-id="6b147-156">Projekta sistēma</span><span class="sxs-lookup"><span data-stu-id="6b147-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="6b147-157">Kļūda, atjauninot darba sadalījuma struktūru</span><span class="sxs-lookup"><span data-stu-id="6b147-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="6b147-158">Ja darba sadalījuma struktūrai tiek izdarīts viens vai vairāki atjauninājumi, izmaiņas beigās neizdodas un netiek saglabātas.</span><span class="sxs-lookup"><span data-stu-id="6b147-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="6b147-159">Grafika režģī rodas kļūda, ziņojot ka "Jūsu veiktās pēdējās izmaiņas nevarēja saglabāt."</span><span class="sxs-lookup"><span data-stu-id="6b147-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="6b147-160">Risinājums</span><span class="sxs-lookup"><span data-stu-id="6b147-160">Workaround</span></span>

1. <span data-ttu-id="6b147-161">Pārbaudiet, vai lietotājam ir piešķirta pareizā licence un vai serviss ir iespējots licences servisa plānu informācijā.</span><span class="sxs-lookup"><span data-stu-id="6b147-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="6b147-162">Pārbaudiet, vai lietotājs var atvērt project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="6b147-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="6b147-163">Pārbaudiet, vai sistēma norāda uz pareizo projekta galapunktu.</span><span class="sxs-lookup"><span data-stu-id="6b147-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="6b147-164">Pārbaudiet, vai ir izveidots projekta lietojumprogrammas lietotājs.</span><span class="sxs-lookup"><span data-stu-id="6b147-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="6b147-165">Piemērojiet lietotājam šādas drošības lomas:</span><span class="sxs-lookup"><span data-stu-id="6b147-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="6b147-166">Dataverse lietotājs vai Base lietotājs</span><span class="sxs-lookup"><span data-stu-id="6b147-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="6b147-167">Project Operations sistēma</span><span class="sxs-lookup"><span data-stu-id="6b147-167">Project Operations System</span></span>
  - <span data-ttu-id="6b147-168">Projekta sistēma</span><span class="sxs-lookup"><span data-stu-id="6b147-168">Project System</span></span>
  - <span data-ttu-id="6b147-169">Project Operations duālās rakstīšanas sistēma (Šī loma ir nepieciešama, ja izvietojat Project Operations resursu/nekrājumu scenāriju.)</span><span class="sxs-lookup"><span data-stu-id="6b147-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
