---
title: Resursu prasības ir redzamas resursiem.
description: Šajā tēmā ir sniegta informācija par rezervācijas nosaukumu resursiem attiecībā uz vispārējo resursu prasībām.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d7ff58ec08661adc702867c6c26805a74a3637c9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125907"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="8173b-103">Resursu prasības ir redzamas resursiem.</span><span class="sxs-lookup"><span data-stu-id="8173b-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8173b-104">Varat rezervēt nosauktu resursu, lai aizstātu vispārējo resursu, kam ir nepieciešama resursa prasība.</span><span class="sxs-lookup"><span data-stu-id="8173b-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="8173b-105">Project Service Automation (PSA) lapā **Projekti** noklikšķiniet uz cilnes **Darba grupa**.</span><span class="sxs-lookup"><span data-stu-id="8173b-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="8173b-106">Atlasiet vispārējo resursu, kam sarakstā ir resursu prasības, un pēc tam noklikšķiniet uz **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="8173b-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="8173b-107">Vai arī atveriet resursu prasības pēc tam noklikšķiniet uz **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="8173b-107">Or, open the resource requirement and then click **Book**.</span></span>


![Vispārēja darba grupas dalībnieka rezervēšana](media/RM-how-to-14.png)


3. <span data-ttu-id="8173b-109">Lapā **Plānošanas palīgs** atlasiet nosauktu resursu, lai grāmatotu savu projekta darba grupu, un pēc tam noklikšķiniet uz **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="8173b-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Vispārēja darba grupas locekļa rezervēšana, izmantojot plānošanas palīgu](media/RM-how-to-15.png)

<span data-ttu-id="8173b-111">Kad rezervēšana ir pabeigta un izpildīta ar nosauktu resursu, vispārējais resurss tiek aizstāts ar nosaukto resursu.</span><span class="sxs-lookup"><span data-stu-id="8173b-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Nosauktais darba grupas dalībnieks, kas aizstāj vispārējo darba grupas dalībnieku](media/RM-how-to-16.png)

<span data-ttu-id="8173b-113">Plāna piešķires tiek atjauninātas, izmantojot arī nosaukto resursu.</span><span class="sxs-lookup"><span data-stu-id="8173b-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Projekta uzdevumiem piešķirtais nosauktais darba grupas dalībnieks](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="8173b-115">Vispārēja resursa izpilde ar vairākiem nosauktiem resursiem</span><span class="sxs-lookup"><span data-stu-id="8173b-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="8173b-116">Prasības attiecībā uz vispārējo resursu ar vairākiem nosauktiem resursiem izpilde ir līdzīga viena nosaukta resursa piešķiršanai.</span><span class="sxs-lookup"><span data-stu-id="8173b-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="8173b-117">Piemēram, ir uzdevums, kura ilgums ir piecas dienas un 120 stundu ilga darba intensitāte.</span><span class="sxs-lookup"><span data-stu-id="8173b-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="8173b-118">Šo uzdevumu nevar izpildīt viens resurss, kas darbojas tipiskā astoņu stundu dienā vairāk nekā piecu dienu nedēļā.</span><span class="sxs-lookup"><span data-stu-id="8173b-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Uzdevums, kam nepieciešamas 120 stundu ilgs darbs piecu dienu laikā](media/RM-how-to-21.png)

<span data-ttu-id="8173b-120">Šī prasība attiecas uz 120 stundām robotikas inženierijā piecu dienu laikā, kas ir 24 stundas diennaktī.</span><span class="sxs-lookup"><span data-stu-id="8173b-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Dienas prasības](media/RM-how-to-22.png)

<span data-ttu-id="8173b-122">Tas ir piemērs, kad ir nepieciešami vairāki resursi, lai izpildītu vispārējo resursu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="8173b-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="8173b-123">Lai izpildītu prasību, jums jārezervē vairāki resursi.</span><span class="sxs-lookup"><span data-stu-id="8173b-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Lai izpildītu prasību, ir jārezervē vairāki resursi.](media/RM-how-to-23.png)

<span data-ttu-id="8173b-125">Galvenā atšķirība šajā scenārijā ir tāda, ka vispārējais resurss paliek uzdevumam piešķirtajā darba grupā un rezervētie resursa darba grupas dalībnieki netiek piešķirti kā šīs pozīcijas daļa.</span><span class="sxs-lookup"><span data-stu-id="8173b-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="8173b-126">Projekta vadītājs var piešķirt darbu atbilstoši nosauktajiem resursiem.</span><span class="sxs-lookup"><span data-stu-id="8173b-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="8173b-127">Skats **Saskaņošana** var palīdzēt projekta vadītājam sadalīt rezervācijas vairākos resursos uz uzdevumu piešķirēm.</span><span class="sxs-lookup"><span data-stu-id="8173b-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="8173b-128">Tas netiek darīts automātiski, jo jebkurš scenārijs, kas ir sarežģītāks par iepriekš minēto vienkāršo piemēru, piemēram, ja jums ir vairāku uzdevumu kopums, kas veido šo prasību, aktivitāte ir jāuzņemas sistēmai, lai jūs to varētu izmantot kā projekta vadītājs.</span><span class="sxs-lookup"><span data-stu-id="8173b-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="8173b-129">Tā kā sistēma nevar saprast nolūku, pastāv iespēja, ka pieņēmumi būs citādi, nekā paredzēts, radīsies nepareizs vai neparedzams rezultāts.</span><span class="sxs-lookup"><span data-stu-id="8173b-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="8173b-130">Prognozējamais rezultāts ir tāds, ka vispārējais resurss paliek piešķirts, kamēr projekta vadītājs apzināti neveido uzdevumus ar skata **Saskaņošana** palīdzību.</span><span class="sxs-lookup"><span data-stu-id="8173b-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


