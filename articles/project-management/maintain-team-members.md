---
title: Darba grupas dalībnieku uzturēšana
description: Šajā tēmā ir sniegta informācija par nosaukto resursu rezervēšanu projekta darba grupām un to piešķiršanu uzdevumiem.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961905"
---
# <a name="maintain-team-members"></a><span data-ttu-id="26636-103">Darba grupas dalībnieku uzturēšana</span><span class="sxs-lookup"><span data-stu-id="26636-103">Maintain team members</span></span>

<span data-ttu-id="26636-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="26636-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="26636-105">Projekta darba grupai varat pievienot nosauktu resursu, to tieši rezervējot darba grupai.</span><span class="sxs-lookup"><span data-stu-id="26636-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="26636-106">Programmā Dynamics 365 Project Operations dodieties uz sadaļu **Projekti** un atveriet projektu, kam veicat rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="26636-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="26636-107">Lapas **Projekts** cilnē **Darba grupa** atlasiet vienumu **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="26636-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="26636-108">Dialoglodziņā **Ātrā izveide: projekta darba grupas dalībnieks** atlasiet rezervējamo resursu.</span><span class="sxs-lookup"><span data-stu-id="26636-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="26636-109">Lauks **Loma** tiks aizpildīts ar resursa noklusējuma lomu, ja tam tā ir piešķirta.</span><span class="sxs-lookup"><span data-stu-id="26636-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="26636-110">Lomu var mainīt.</span><span class="sxs-lookup"><span data-stu-id="26636-110">You can change the role.</span></span> 
4. <span data-ttu-id="26636-111">Atlasiet, no kura datuma līdz kuram resurss būs nepieciešams, un atlasiet resursa noslodzes piešķiršanas metodi.</span><span class="sxs-lookup"><span data-stu-id="26636-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="26636-112">Ja vēlaties, lai darba grupas dalībnieks būtu projekta apstiprinātājs, atlasiet **Jā** laukā **Projekta apstiprinātājs**.</span><span class="sxs-lookup"><span data-stu-id="26636-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="26636-113">Darba grupas dalībnieks var apstiprināt šim projektam iesniegtos laika un izdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="26636-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="26636-114">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="26636-114">Select **Save**.</span></span>

<span data-ttu-id="26636-115">Tagad rezervēto resursu varat piešķirt projekta uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="26636-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="26636-116">Lapas **Projekts** cilnē **Grafiks** piešķiriet jaunajam resursam uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="26636-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="26636-117">Resursu atlasītājā, kas palaists no uzdevumu režģa lauka **Resursi**, tiks parādīti darba grupas dalībnieki, kurus varat atlasīt.</span><span class="sxs-lookup"><span data-stu-id="26636-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="26636-118">Programmā Project Operations resursu rezervēšana un uzdevumu piešķires nav cieši savienotas.</span><span class="sxs-lookup"><span data-stu-id="26636-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="26636-119">Kad grafikā izmantojat resursu atlasītāju, darba grupas dalībniekiem varat piešķirt uzdevumus ar stundu skaitu, kas pārsniedz to rezervācijas projektā.</span><span class="sxs-lookup"><span data-stu-id="26636-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="26636-120">Darba grupas dalībnieku rezervācijas un piešķiru atšķirības tiek rādītas cilnēs **Darba grupa** un **Resursu saskaņošana**.</span><span class="sxs-lookup"><span data-stu-id="26636-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="26636-121">Varat arī saskaņot resursu rezervāciju un piešķiru atšķirības detalizētākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="26636-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="26636-122">Izmantojiet izmantot resursu atlasītāju cilnē **Grafiks**, lai meklētu un atlasītu rezervējamos resursus, kas vēl nav daļa no projekta darba grupas.</span><span class="sxs-lookup"><span data-stu-id="26636-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="26636-123">Šie resursi tiek parādīti resursu atlasītājā kā **Citi resursi**.</span><span class="sxs-lookup"><span data-stu-id="26636-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="26636-124">Veicot atlasi, resurss tiek pievienots projekta darba grupai un piešķirts uzdevumam, taču netiek ģenerētas rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="26636-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="26636-125">Varat izmantot cilnes **Saskaņošana** rezervācijas paplašināšanas iespēju vai vienumu **Plānošanas panelis**, lai rezervētu resursa noslodzi uz projektā.</span><span class="sxs-lookup"><span data-stu-id="26636-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="26636-126">Pēc tam, kad darba grupas dalībnieks ir rezervēts projektā, varat izmantot opcijas **Uzturēt rezervācijas** vai vienumu **Plānošanas panelis**, lai tiešā veidā pārvaldītu to rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="26636-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
