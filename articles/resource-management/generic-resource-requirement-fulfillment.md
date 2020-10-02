---
title: Vispārējo resursu prasību izpilde
description: Šajā tēmā ir sniegta informācija par rezervācijas nosaukumu resursiem attiecībā uz vispārējo resursu prasībām.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897595"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="dcd5f-103">Vispārējo resursu prasību izpilde</span><span class="sxs-lookup"><span data-stu-id="dcd5f-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="dcd5f-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="dcd5f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dcd5f-105">Varat rezervēt nosauktu resursu, lai aizstātu vispārējo resursu, kam ir nepieciešama resursa prasība.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="dcd5f-106">Lapā **Projekti** atlasiet cilni **Darba grupa**.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="dcd5f-107">Atlasiet vispārējo resursu, kam sarakstā ir resursu prasības, un pēc tam atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="dcd5f-108">Vai arī atveriet resursu prasības pēc tam atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="dcd5f-109">Lapā **Plānošanas palīgs** atlasiet nosauktu resursu, lai grāmatotu savu projekta darba grupu, un pēc tam atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="dcd5f-110">Kad rezervēšana ir pabeigta un izpildīta ar nosauktu resursu, vispārējais resurss tiek aizstāts ar nosaukto resursu.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="dcd5f-111">Plāna piešķires tiek atjauninātas, izmantojot arī nosaukto resursu.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="dcd5f-112">Vispārēja resursa izpilde ar vairākiem nosauktiem resursiem</span><span class="sxs-lookup"><span data-stu-id="dcd5f-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="dcd5f-113">Prasības attiecībā uz vispārējo resursu ar vairākiem nosauktiem resursiem izpilde ir līdzīga viena nosaukta resursa piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="dcd5f-114">Piemēram, ir uzdevums, kura ilgums ir piecas dienas un 120 stundu ilga darba intensitāte.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="dcd5f-115">Šo uzdevumu nevar izpildīt viens resurss, kas darbojas tipiskā astoņu stundu dienā vairāk nekā piecu dienu nedēļā.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="dcd5f-116">Šī prasība attiecas uz 120 stundām robotikas inženierijā piecu dienu laikā, kas ir 24 stundas diennaktī.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="dcd5f-117">Tas ir piemērs, kad ir nepieciešami vairāki resursi, lai izpildītu vispārējo resursu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="dcd5f-118">Lai izpildītu prasību, jums jārezervē vairāki resursi.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="dcd5f-119">Galvenā atšķirība šajā scenārijā ir tāda, ka vispārējais resurss paliek uzdevumam piešķirtajā darba grupā un rezervētie resursa darba grupas dalībnieki netiek piešķirti kā šīs pozīcijas daļa.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="dcd5f-120">Projekta vadītājs var piešķirt darbu atbilstoši nosauktajiem resursiem.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="dcd5f-121">Skats **Saskaņošana** var palīdzēt projekta vadītājam sadalīt rezervācijas vairākos resursos uz uzdevumu piešķirēm.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="dcd5f-122">Tas netiek darīts automātiski, jo jebkurš scenārijs, kas ir sarežģītāks par iepriekš minēto vienkāršo piemēru, piemēram, ja jums ir vairāku uzdevumu kopums, kas veido šo prasību, vai aktivitāte ir jāuzņemas sistēmai, lai jūs to varētu izmantot kā projekta vadītājs.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="dcd5f-123">Tā kā sistēma nevar saprast nolūku, pieņēmumi, iespējams, būs citādi, nekā paredzēts, un radīsies nepareizs vai neparedzams rezultāts.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="dcd5f-124">Prognozējamais rezultāts ir tāds, ka vispārējais resurss paliek piešķirts, kamēr projekta vadītājs apzināti neveido uzdevumus ar skata **Saskaņošana** palīdzību.</span><span class="sxs-lookup"><span data-stu-id="dcd5f-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


