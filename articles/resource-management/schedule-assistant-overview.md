---
title: Plānošanas asistenta pārskats
description: Šajā tēmā ir sniegta informācija par darbu ar plānošanas palīgu resursu rezervēšanai.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080300"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="d9012-103">Plānošanas asistenta pārskats</span><span class="sxs-lookup"><span data-stu-id="d9012-103">Schedule assistant overview</span></span>

<span data-ttu-id="d9012-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="d9012-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d9012-105">Plānošanas palīgu izmanto resursu rezervēšanai, pamatojoties uz projekta vadītāja definētajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="d9012-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="d9012-106">Plānošanas palīgs paļaujas uz parametriem, kas norādīti resursa prasībā, lai atrastu resursu.</span><span class="sxs-lookup"><span data-stu-id="d9012-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="d9012-107">Plānošanas palīgs iesaka resursus, kas atbilst atbilstošām prasībām, piemēram, piemēram, laika logiem vai vajadzīgajām prasmēm.</span><span class="sxs-lookup"><span data-stu-id="d9012-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="d9012-108">Kad ir identificēti piemēroti resursi, resurss vai projekta vadītājs var rezervēt resursu darbam.</span><span class="sxs-lookup"><span data-stu-id="d9012-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d9012-109">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="d9012-109">Prerequisites</span></span>

<span data-ttu-id="d9012-110">Plānošanas palīgs ir risinājuma Universal Resource Scheduling daļa.</span><span class="sxs-lookup"><span data-stu-id="d9012-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="d9012-111">Šis risinājums ir iekļauts un instalēts kopā ar Dynamics 365 Project Operations, Dynamics 365 Field Service un Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="d9012-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="d9012-112">Prasības un atbilstošu resursu meklēšana</span><span class="sxs-lookup"><span data-stu-id="d9012-112">Matching requirements and resources</span></span>

<span data-ttu-id="d9012-113">Ģenerētas resursa prasības pamatā ir tāda informācija kā:</span><span class="sxs-lookup"><span data-stu-id="d9012-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="d9012-114">Īpašības</span><span class="sxs-lookup"><span data-stu-id="d9012-114">Characteristics</span></span>
-   <span data-ttu-id="d9012-115">Lomas</span><span class="sxs-lookup"><span data-stu-id="d9012-115">Roles</span></span>
-   <span data-ttu-id="d9012-116">Struktūrvienības</span><span class="sxs-lookup"><span data-stu-id="d9012-116">Business units</span></span>
-   <span data-ttu-id="d9012-117">Resursu preferences</span><span class="sxs-lookup"><span data-stu-id="d9012-117">Resource preferences</span></span>
-   <span data-ttu-id="d9012-118">Darba kontūras</span><span class="sxs-lookup"><span data-stu-id="d9012-118">Effort contours</span></span>
-   <span data-ttu-id="d9012-119">Laika josla</span><span class="sxs-lookup"><span data-stu-id="d9012-119">Time zone</span></span>

<span data-ttu-id="d9012-120">Plānošanas palīgs izmanto šo informāciju, lai filtrētu resursus.</span><span class="sxs-lookup"><span data-stu-id="d9012-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="d9012-121">Plānošanas palīga palaišana</span><span class="sxs-lookup"><span data-stu-id="d9012-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="d9012-122">Plānošanas palīgu var palaist divos veidos.</span><span class="sxs-lookup"><span data-stu-id="d9012-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="d9012-123">Ja izmantojat hibrīda režīmu, darba grupas dalībnieku režģī varat atlasīt jebkuru darba grupas dalībnieku ar neizpildītu resursa prasību un pēc tam atlasīt **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="d9012-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="d9012-124">Ja izmantojat centrālo režīmu, resursu pārvaldnieks atrod un atlasa resursu.</span><span class="sxs-lookup"><span data-stu-id="d9012-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="d9012-125">Plānošanas palīga filtri</span><span class="sxs-lookup"><span data-stu-id="d9012-125">Schedule assistant filters</span></span>

<span data-ttu-id="d9012-126">Pēc plānošanas palīga palaišanas resursa prasības informācija tiek parādīta kā filtrētas vērtības kreisajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="d9012-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="d9012-127">Resursu pārvaldnieks vai projekta vadītājs var precīzi regulēt rezultātus, pielāgojot filtrus, lai apmierinātu plānošanas vajadzības.</span><span class="sxs-lookup"><span data-stu-id="d9012-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="d9012-128">Filtrēšanas rūtī tiek rādītas ar darbu saistītas opcijas, tostarp:</span><span class="sxs-lookup"><span data-stu-id="d9012-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="d9012-129">Darba sākums un beigas</span><span class="sxs-lookup"><span data-stu-id="d9012-129">Work start and end</span></span>
-   <span data-ttu-id="d9012-130">Īpašības</span><span class="sxs-lookup"><span data-stu-id="d9012-130">Characteristics</span></span>
-   <span data-ttu-id="d9012-131">Lomas</span><span class="sxs-lookup"><span data-stu-id="d9012-131">Roles</span></span>
-   <span data-ttu-id="d9012-132">Organizācijas vienības</span><span class="sxs-lookup"><span data-stu-id="d9012-132">Organizational units</span></span>
-   <span data-ttu-id="d9012-133">Resursu uzņēmums</span><span class="sxs-lookup"><span data-stu-id="d9012-133">Resourcing company</span></span>
-   <span data-ttu-id="d9012-134">Resursu tipi</span><span class="sxs-lookup"><span data-stu-id="d9012-134">Resource types</span></span>
-   <span data-ttu-id="d9012-135">Vēlamie resursi</span><span class="sxs-lookup"><span data-stu-id="d9012-135">Preferred resources</span></span>
