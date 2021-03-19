---
title: Piedāvāto resursu pārskats
description: Šajā tēmā ir sniegta informācija par to, kā piedāvāt projekta resursus.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279282"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="0334e-103">Piedāvāto resursu pārskats</span><span class="sxs-lookup"><span data-stu-id="0334e-103">Review proposed resources</span></span>

<span data-ttu-id="0334e-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="0334e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0334e-105">Resursu vadītāji var piedāvāt resursu projektu vadītājam, izmantojot resursu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="0334e-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="0334e-106">Pieprasījumu režģī vai pašā pieprasījumā atlasiet opciju **Atrast resursus**.</span><span class="sxs-lookup"><span data-stu-id="0334e-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="0334e-107">Lapā **Plānošanas palīgs** atlasiet resursu un pēc tam rūtī **Izveidot resursu rezervāciju**, laukā **Rezervācijas statuss** atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="0334e-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="0334e-108">Tiek veikti šādi statusa atjauninājumi:</span><span class="sxs-lookup"><span data-stu-id="0334e-108">The following status updates occur:</span></span>

- <span data-ttu-id="0334e-109">Lapā **Plānošanas palīgs** statusa indikatori tiek atjaunināti, lai norādītu, ka rezervācija ir piedāvāta, nevis stingri rezervēta.</span><span class="sxs-lookup"><span data-stu-id="0334e-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="0334e-110">Resursa pieprasījumā statuss tiek mainīts uz **Nepieciešama pārskatīšana**.</span><span class="sxs-lookup"><span data-stu-id="0334e-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="0334e-111">Projekta cilnē **Darba grupa** vērtība vispārējā darba grupas dalībnieka vienumam **Pieprasījuma statuss** ir mainīta uz **Nepieciešama pārskatīšana**.</span><span class="sxs-lookup"><span data-stu-id="0334e-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="0334e-112">Projekta vadītājs var pieņemt vai noraidīt piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="0334e-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="0334e-113">Kad resursu vadītāji apstrādā resursu pieprasījumus, viņi var izmantot jebkuru no tālāk minētajām metodēm.</span><span class="sxs-lookup"><span data-stu-id="0334e-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="0334e-114">Piedāvāt vairākus resursus, lai apmierinātu pieprasījumu, ja nepieciešamo stundu izpildei nav pieejams viens resurss.</span><span class="sxs-lookup"><span data-stu-id="0334e-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="0334e-115">Piedāvātās stundas tiek sadalītas starp vairākiem resursiem, kas var apmierināt nepieciešamo stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="0334e-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="0334e-116">Šādā gadījumā stundas nevar pārklāties.</span><span class="sxs-lookup"><span data-stu-id="0334e-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="0334e-117">Piedāvāt mazāk resursu, nekā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="0334e-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="0334e-118">Šādā gadījumā paredzētā resursa noslodze ir mazāka nekā prasītāja norādītais nepieciešamo stundu laiks.</span><span class="sxs-lookup"><span data-stu-id="0334e-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="0334e-119">Tāpēc, kad prasītājs pieņem piedāvātos resursus, tiek izveidota neizpildīta resursa vajadzība, lai norādītu atlikušo pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="0334e-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="0334e-120">Rezervēt vairākus resursus, lai apmierinātu pieprasījumu, ja darba izpildei nav pieejams viens resurss.</span><span class="sxs-lookup"><span data-stu-id="0334e-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="0334e-121">Rezervēt mazāk resursu, nekā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="0334e-121">Book fewer resources than are required.</span></span> <span data-ttu-id="0334e-122">Šādā gadījumā rezervēto stundu skaits ir mazāks par nepieciešamo stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="0334e-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="0334e-123">Sistēma palīdz piedāvāt resursus, nevis rezervācijas, lai pieprasītājs varētu pārbaudīt un sekot līdzi atlikušajām vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="0334e-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="0334e-124">Resursu pieejamība</span><span class="sxs-lookup"><span data-stu-id="0334e-124">Resource availability</span></span>

<span data-ttu-id="0334e-125">Ir ļoti svarīgi, lai resursu vadītāji varētu apskatīt resursu pieejamību un atjaunināt rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="0334e-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="0334e-126">Dažos gadījumos nav oficiāla pieprasījuma (resursa pieprasījuma), bet resursu vadītājam ir jāreaģē uz neplānotu pieprasījumu, kas rodas, izmantojot tādus kanālus kā e-pasts, tālruņa saruna vai tūlītējais ziņojums.</span><span class="sxs-lookup"><span data-stu-id="0334e-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="0334e-127">Resursu vadītāji izmanto plānošanas paneli, lai atjauninātu resursus un rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="0334e-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="0334e-128">Resursa darba stundas tiek izmantotas par pamatu resursa pieejamības aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="0334e-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="0334e-129">Resursu rezervēšana patērē resursu noslodzi.</span><span class="sxs-lookup"><span data-stu-id="0334e-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="0334e-130">Plānošanas panelī tiek izmantotas krāsas un ēnojums, lai norādītu rezervācijas, pieejamību un rezervēšanas pārsniegšanu, kā arī rezervāciju statusu.</span><span class="sxs-lookup"><span data-stu-id="0334e-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="0334e-131">Iestatījums plānošanas paneļa iestatījumos ļauj rādīt apzīmējumus.</span><span class="sxs-lookup"><span data-stu-id="0334e-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="0334e-132">Ja blakus atsevišķiem rezervējamiem resursiem plānošanas panelī tiek parādīta pa labi vērsta bultiņa, resursu var izvērst, lai skatītu detalizētu informāciju par darbu, kuram attiecīgais resurss ir rezervēts.</span><span class="sxs-lookup"><span data-stu-id="0334e-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="0334e-133">Tā kā Dynamics 365 Project Operations izmanto programmu Universal Resource Scheduling, ja ir instalēts arī risinājums Dynamics 365 Field Service, varat skatīt detalizētu informāciju par resursu rezervācijām projektiem, darba pasūtījumiem un citām entītijām, uz kurām esat paplašinājis plānošanu.</span><span class="sxs-lookup"><span data-stu-id="0334e-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="0334e-134">Lai skatītu papildinformāciju par atsevišķu resursu, ar peles labo pogu noklikšķiniet uz tā, lai atvērtu resursa karti.</span><span class="sxs-lookup"><span data-stu-id="0334e-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]