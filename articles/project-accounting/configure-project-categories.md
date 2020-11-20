---
title: Projekta kategoriju iestatīšana
description: Šajā tēmā ir sniegta informācija par projekta kategoriju iestatīšanu.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131937"
---
# <a name="configure-project-categories"></a><span data-ttu-id="d79cd-103">Projekta kategoriju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d79cd-103">Configure project categories</span></span>

<span data-ttu-id="d79cd-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="d79cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d79cd-105">Project Operations nodrošina robustas ieņēmumu un izdevumu kategorizācijas iespējas projektiem.</span><span class="sxs-lookup"><span data-stu-id="d79cd-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="d79cd-106">Kategorijas nodrošina iespēju ziņot par projekta darījumiem un tos analizēt, kā arī vadīt grāmatošanu virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="d79cd-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="d79cd-107">Tālāk sniegtajā shēmā parādīta korelācija starp darījumu kategorijām, koplietojamām kategorijām un projekta kategorijām.</span><span class="sxs-lookup"><span data-stu-id="d79cd-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="d79cd-108">Darījumu kategorijas ir projekta darījumu pamata grupas.</span><span class="sxs-lookup"><span data-stu-id="d79cd-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="d79cd-109">Šajās grupās ir koplietojamu kategoriju kopums, ko var kopīgot programmās un moduļos.</span><span class="sxs-lookup"><span data-stu-id="d79cd-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="d79cd-110">Konkrētāk — projekta kategorijas ir detalizētākais kategoriju līmenis.</span><span class="sxs-lookup"><span data-stu-id="d79cd-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="d79cd-111">Projekta kategorijas ir noteiktas konkrētai juridiskai personai, modulim un programmai.</span><span class="sxs-lookup"><span data-stu-id="d79cd-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korelācija starp darījumu kategorijām, koplietojamām kategorijām un projekta kategorijām](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="d79cd-113">Transakcijas kategorijas</span><span class="sxs-lookup"><span data-stu-id="d79cd-113">Transaction categories</span></span>

<span data-ttu-id="d79cd-114">Darījumu kategorijas ataino projekta darījumu pamatgrupas, un tās neattiecas uz konkrētu uzņēmuma vai darījumu veidu.</span><span class="sxs-lookup"><span data-stu-id="d79cd-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="d79cd-115">Piemēram, uzņēmums Contoso Robotics" izmanto darījumu kategorijas Projektēšana, Ceļojumi, Uzstādīšana un Apkope, kurās grupē Projekta darījumus.</span><span class="sxs-lookup"><span data-stu-id="d79cd-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="d79cd-116">Darījumu kategorijas tiek definētas Project Operations modulī.</span><span class="sxs-lookup"><span data-stu-id="d79cd-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="d79cd-117">Lai atvērtu veidlapu, dodieties uz **Iestatījumi** \> **Darījumu kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="d79cd-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="d79cd-118">Izveidojiet jaunu darījumu kategoriju, atlasot vienumu **Jauns** vai atlasot **Importēt no Excel**.</span><span class="sxs-lookup"><span data-stu-id="d79cd-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="d79cd-119">Koplietotās kategorijas</span><span class="sxs-lookup"><span data-stu-id="d79cd-119">Shared categories</span></span>

<span data-ttu-id="d79cd-120">Dynamics 365 izmanto Koplietoto kategoriju koncepciju, lai kategorizētu izdevumus dažādās programmās, piemēram, Dynamics 365 Finance, Dynamics 365 Supply Chain un Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d79cd-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="d79cd-121">Katrai izveidotajai Darījumu kategorijai Project Operations automātiski izveido četras saistītas Koplietotās kategorijas: Stundas, Izdevumi, Maksas un Vienums.</span><span class="sxs-lookup"><span data-stu-id="d79cd-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="d79cd-122">Varat pārskatīt un pielāgot koplietotās kategorijas, atverot **Projektu pārvaldība un uzskaite** \> **Iestatīšana** \> **Kategorijas** \> **Koplietotās kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="d79cd-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="d79cd-123">Projektu kategorijas</span><span class="sxs-lookup"><span data-stu-id="d79cd-123">Project categories</span></span>

<span data-ttu-id="d79cd-124">Projekta kategorijas ir detalizētākais kategoriju konfigurācijas līmenis, un tās ir jākonfigurē Projekta grāmatvedim atsevišķi un katram uzņēmumam individuāli.</span><span class="sxs-lookup"><span data-stu-id="d79cd-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="d79cd-125">Dodieties uz **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Kategorijas** \> **Projekta kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="d79cd-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="d79cd-126">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d79cd-126">Select **New**.</span></span>
3. <span data-ttu-id="d79cd-127">Atlasiet tās Koplietotās kategorijas **Kategorijas ID**, ko izveidojāt iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="d79cd-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="d79cd-128">Project Operations ļauj izmantot tikai tās koplietotās kategorijas, kas ir saistītas ar darījumu kategorijām.</span><span class="sxs-lookup"><span data-stu-id="d79cd-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="d79cd-129">Atlasiet kategoriju grupu.</span><span class="sxs-lookup"><span data-stu-id="d79cd-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="d79cd-130">Kategoriju grupas</span><span class="sxs-lookup"><span data-stu-id="d79cd-130">Category groups</span></span>

<span data-ttu-id="d79cd-131">Kategoriju grupas izmanto, lai kopīgotu rekvizītus, galvenokārt grāmatošanas profilus, starp saistītām Projekta kategorijām.</span><span class="sxs-lookup"><span data-stu-id="d79cd-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="d79cd-132">Katram darījuma veidam ir jābūt vismaz vienai kategoriju grupai, un katrai projekta kategorijai ir piešķirta grupa.</span><span class="sxs-lookup"><span data-stu-id="d79cd-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="d79cd-133">Grāmatojumu specifikācijas risinājumā Project Operations tiek definētas, izmantojot projekta izmaksu un ieņēmumu profila kārtulas, projekta kategorijas +un kategoriju grupas.</span><span class="sxs-lookup"><span data-stu-id="d79cd-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="d79cd-134">Kategoriju grupas varat iestatīt, dodoties uz sadaļu **Projektu pārvaldība un uzskaite** \> **Iestatīšana** \> **Kategorijas** \> **Kategoriju grupas**.</span><span class="sxs-lookup"><span data-stu-id="d79cd-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
