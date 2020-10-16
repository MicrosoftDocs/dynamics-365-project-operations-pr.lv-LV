---
title: Izvietojuma tipi
description: Šajā tēmā ir sniegta informācija, kas jums palīdzēs noteikt pareizo Project Operations izvietošanas tipu savam uzņēmumam.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948968"
---
# <a name="deployment-types"></a><span data-ttu-id="6e54a-103">Izvietojuma tipi</span><span class="sxs-lookup"><span data-stu-id="6e54a-103">Deployment types</span></span>

<span data-ttu-id="6e54a-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="6e54a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e54a-105">Pēc licences iegādes sāciet šeit, lai noteiktu labāko Dynamics 365 Project Operations izvietošanas modeli, izmantojot rīku [Vadītā instalācijas plūsma](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6e54a-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="6e54a-106">Kad būsiet pabeidzis vadīto instalācijas plūsmu, tiksiet novirzīts uz atbilstošo pārvaldības portālu, lai pabeigtu instalēšanu.</span><span class="sxs-lookup"><span data-stu-id="6e54a-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="6e54a-107">Lai pabeigtu instalēšanu, skatiet tālāk sniegto izvietošanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="6e54a-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="6e54a-108">Esošie Dynamics klienti, kas izmanto Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6e54a-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="6e54a-109">Project Operations ietver iespējas, kas piegādātas kopā ar Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6e54a-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="6e54a-110">Nākotnē šiem klientiem tiks izlaists jaunināšanas ceļš.</span><span class="sxs-lookup"><span data-stu-id="6e54a-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="6e54a-111">Esošie Dynamics 365 Finance klienti, kas izmanto Projektu pārvaldību un uzskaiti</span><span class="sxs-lookup"><span data-stu-id="6e54a-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="6e54a-112">Esošie Finance klienti, kas izmanto Projekta pārvaldības un uzskaites funkcionalitāti, var turpināt to lietošanu līdzšinējā veidā.</span><span class="sxs-lookup"><span data-stu-id="6e54a-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="6e54a-113">Skatiet [Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem](#pma).</span><span class="sxs-lookup"><span data-stu-id="6e54a-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="6e54a-114">Project Operations atbalsta vairākas izvietošanas opcijas, lai atbilstu jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="6e54a-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="6e54a-115">Neatkarīgi no tā, vai esat jauns vai esošs Dynamics 365 klients, Project Operations var atbalstīt jūsu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="6e54a-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="6e54a-116">Mūsu [Izvietošanas anketa](https://aka.ms/provisionprojectoperations) palīdzēs noteikt pareizo izvietošanas veidu.</span><span class="sxs-lookup"><span data-stu-id="6e54a-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="6e54a-117">Rezultāti jums palīdzēs sasniegt kādu no tālāk norādītajiem izvietošanas tipiem.</span><span class="sxs-lookup"><span data-stu-id="6e54a-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="6e54a-118">Lite izvietošana — pāriet uz pro forma rēķina izrakstīšanu</span><span class="sxs-lookup"><span data-stu-id="6e54a-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="6e54a-119">Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem</span><span class="sxs-lookup"><span data-stu-id="6e54a-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="6e54a-120">Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="6e54a-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="6e54a-121">Project Operations vienā un tajā pašā vidē atbalsta scenārijus, kas balstīti uz krājumiem un ražošanas pasūtījumiem, un scenārijus, kas ir balstīti uz resursiem/nav balstīti uz krājumiem, izmantojot juridiskās personas līmeņa konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="6e54a-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="6e54a-122">Piemēram, uzņēmums Contoso var izmantot krājumu/ražošanas pasūtījumu iespējas ASV ražošanas objektā (juridiskā persona = Contoso Manufacturing United States) un iespējas, kas ir balstītas uz resursiem/nav balstītas uz krājumiem, savā Contoso Robotics Arms apkalpošanas objektā Lielbritānijā (juridiskā persona = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="6e54a-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="6e54a-123"><a name="lite"><a/>Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu</span><span class="sxs-lookup"><span data-stu-id="6e54a-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="6e54a-124">Lite izvietošana ietver tālāk norādītās iespējas.</span><span class="sxs-lookup"><span data-stu-id="6e54a-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="6e54a-125">Projektu plānošana, izmantojot Microsoft Project tīmeklim</span><span class="sxs-lookup"><span data-stu-id="6e54a-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6e54a-126">Vairākdimensiju izcenojums</span><span class="sxs-lookup"><span data-stu-id="6e54a-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6e54a-127">Vienota resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="6e54a-127">Unified Resource Management</span></span>
- <span data-ttu-id="6e54a-128">Laika izsekošana</span><span class="sxs-lookup"><span data-stu-id="6e54a-128">Time Tracking</span></span>
- <span data-ttu-id="6e54a-129">Pamata izdevumi</span><span class="sxs-lookup"><span data-stu-id="6e54a-129">Basic Expense</span></span>
- <span data-ttu-id="6e54a-130">Rēķina priekšlikums</span><span class="sxs-lookup"><span data-stu-id="6e54a-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6e54a-131">Izvietošanas darbības:</span><span class="sxs-lookup"><span data-stu-id="6e54a-131">Deployment steps:</span></span>
<span data-ttu-id="6e54a-132">Nosakiet labāko Project Operations izvietošanas modeli, izmantojot rīku [Izvietošanas anketa](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6e54a-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6e54a-133">Lai īstenotu šo izvietošanu skatiet informāciju šeit: [Pierakstīšanās priekšskatījuma abonementiem](lite-preview-subscription-sign-up.md) un [Jaunas vides nodrošināšana](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="6e54a-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="6e54a-134"><a name="integrated"><a/>Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem</span><span class="sxs-lookup"><span data-stu-id="6e54a-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="6e54a-135">Project Operations scenāriji, kas balstīti uz resursiem/nav balstīti uz krājumiem, ietver tālāk norādītās iespējas.</span><span class="sxs-lookup"><span data-stu-id="6e54a-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="6e54a-136">Projektu plānošana, izmantojot Microsoft Project tīmeklim</span><span class="sxs-lookup"><span data-stu-id="6e54a-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6e54a-137">Vairākdimensiju izcenojums</span><span class="sxs-lookup"><span data-stu-id="6e54a-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6e54a-138">Vienota resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="6e54a-138">Unified Resource Management</span></span>
- <span data-ttu-id="6e54a-139">Laika izsekošana</span><span class="sxs-lookup"><span data-stu-id="6e54a-139">Time Tracking</span></span>
- <span data-ttu-id="6e54a-140">Pamata izdevumi</span><span class="sxs-lookup"><span data-stu-id="6e54a-140">Basic Expense</span></span>
- <span data-ttu-id="6e54a-141">Pilni izdevumi</span><span class="sxs-lookup"><span data-stu-id="6e54a-141">Full Expense</span></span>
- <span data-ttu-id="6e54a-142">OCR apliecinājums</span><span class="sxs-lookup"><span data-stu-id="6e54a-142">Receipt OCR</span></span>
- <span data-ttu-id="6e54a-143">Pilna rēķinu izrakstīšana</span><span class="sxs-lookup"><span data-stu-id="6e54a-143">Full Invoicing</span></span>
- <span data-ttu-id="6e54a-144">Ieņēmumu atzinība</span><span class="sxs-lookup"><span data-stu-id="6e54a-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6e54a-145">Izvietošanas darbības:</span><span class="sxs-lookup"><span data-stu-id="6e54a-145">Deployment steps:</span></span>
<span data-ttu-id="6e54a-146">Nosakiet labāko Project Operations izvietošanas modeli, izmantojot rīku [Izvietošanas anketa](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6e54a-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6e54a-147">Lai īstenotu šo izvietošanu skatiet informāciju šeit: [Pierakstīšanās priekšskatījuma abonementiem](resource-sign-up-preview-subscription.md) un [Jaunas vides nodrošināšana](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6e54a-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="6e54a-148">Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="6e54a-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="6e54a-149">Projektu plānošana, izmantojot WBS</span><span class="sxs-lookup"><span data-stu-id="6e54a-149">Project planning using WBS</span></span>
- <span data-ttu-id="6e54a-150">Resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="6e54a-150">Resource Management</span></span>
- <span data-ttu-id="6e54a-151">Laika izsekošana</span><span class="sxs-lookup"><span data-stu-id="6e54a-151">Time Tracking</span></span>
- <span data-ttu-id="6e54a-152">Pilni izdevumi</span><span class="sxs-lookup"><span data-stu-id="6e54a-152">Full Expense</span></span>
- <span data-ttu-id="6e54a-153">OCR apliecinājums</span><span class="sxs-lookup"><span data-stu-id="6e54a-153">Receipt OCR</span></span>
- <span data-ttu-id="6e54a-154">Pilna rēķinu izrakstīšana</span><span class="sxs-lookup"><span data-stu-id="6e54a-154">Full Invoicing</span></span>
- <span data-ttu-id="6e54a-155">Ieņēmumu atzinība</span><span class="sxs-lookup"><span data-stu-id="6e54a-155">Revenue Recognition</span></span>
- <span data-ttu-id="6e54a-156">Ražošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="6e54a-156">Production Orders</span></span>
- <span data-ttu-id="6e54a-157">Materiālu atbalsts</span><span class="sxs-lookup"><span data-stu-id="6e54a-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6e54a-158">Izvietošanas darbības:</span><span class="sxs-lookup"><span data-stu-id="6e54a-158">Deployment steps:</span></span>
<span data-ttu-id="6e54a-159">Nosakiet labāko Project Operations izvietošanas modeli, izmantojot rīku [Izvietošanas anketa](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6e54a-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6e54a-160">Lai īstenotu šo izvietošanu skatiet informāciju šeit: [Pierakstīšanās priekšskatījuma abonementiem](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) un [Jaunas vides nodrošināšana](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6e54a-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



