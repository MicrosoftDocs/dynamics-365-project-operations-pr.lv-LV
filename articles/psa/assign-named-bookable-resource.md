---
title: Nosaukto rezervējamo resursu rezervēšana projekta darba grupai un uzdevumu piešķiršana
description: Šajā tēmā ir sniegta informācija par to, kā rezervēt nosauktos resursus projekta darba grupām un piešķirt tās uzdevumiem.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: e0f3957936e699fb2a9f570b9789924c55e12cc2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009355"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="218bd-103">Nosaukto rezervējamo resursu rezervēšana projekta darba grupai un uzdevumu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="218bd-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="218bd-104">Projekta darba grupai varat pievienot nosauktu resursu, to tieši rezervējot darba grupai.</span><span class="sxs-lookup"><span data-stu-id="218bd-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="218bd-105">Lai to paveiktu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="218bd-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="218bd-106">Programmā Project Service Automation dodieties uz sadaļu **Projekti** un atveriet projektu, kam veicat rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="218bd-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="218bd-107">Lapas **Projekts** cilnē **Darba grupa** noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="218bd-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Darba grupas dalībnieka pievienošana no darba grupas cilnes](media/RM-how-to-1.png)

3. <span data-ttu-id="218bd-109">Dialoglodziņā **Ātrā izveide: projekta darba grupas dalībnieks** atlasiet rezervējamo resursu.</span><span class="sxs-lookup"><span data-stu-id="218bd-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="218bd-110">Lauks **Loma** tiks aizpildīts ar resursa noklusējuma lomu, ja tam tā ir piešķirta.</span><span class="sxs-lookup"><span data-stu-id="218bd-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="218bd-111">Ja nepieciešams, lomu var mainīt.</span><span class="sxs-lookup"><span data-stu-id="218bd-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="218bd-112">Atlasiet, no kura datuma līdz kuram resurss būs nepieciešams, un atlasiet resursa noslodzes piešķiršanas metodi.</span><span class="sxs-lookup"><span data-stu-id="218bd-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="218bd-113">Ja vēlaties, lai darba grupas dalībnieks būtu projekta apstiprinātājs, atlasiet **Jā** laukā **Projekta apstiprinātājs**.</span><span class="sxs-lookup"><span data-stu-id="218bd-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="218bd-114">Tas nozīmē, ka darba grupas dalībnieks var apstiprināt šim projektam iesniegtos laika un izdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="218bd-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="218bd-115">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="218bd-115">Click **Save**.</span></span>

![Darba grupas dalībnieka pievienošana ātrās izveides veidlapā](media/RM-how-to-2.png)


<span data-ttu-id="218bd-117">Tagad rezervēto resursu varat piešķirt projekta uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="218bd-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="218bd-118">Lapā **Projekts** noklikšķiniet uz cilnes **Grafiks**, lai jaunajam resursam piešķirtu uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="218bd-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="218bd-119">Resursu atlasītājā, kas palaists no uzdevumu režģa lauka **Resursi**, tiks parādīti darba grupas dalībnieki, kurus varat atlasīt.</span><span class="sxs-lookup"><span data-stu-id="218bd-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Darba grupas dalībnieka piešķiršana uzdevumam grafika cilnē](media/RM-how-to-3.png)

<span data-ttu-id="218bd-121">Project Service Automation (PSA) 3. versijā resursu rezervācijas un uzdevumu piešķires nav cieši savienotas.</span><span class="sxs-lookup"><span data-stu-id="218bd-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="218bd-122">Tas nozīmē, ka tad, kad grafikā izmantojat resursu atlasītāju, darba grupas dalībniekiem varat piešķirt uzdevumus ar stundu skaitu, kas pārsniedz to rezervācijas projektā.</span><span class="sxs-lookup"><span data-stu-id="218bd-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="218bd-123">Atšķirības starp darba grupas dalībnieku rezervācijām un piešķirēm varat skatīt cilnē **Darba grupa** vai cilnē **Resursu saskaņošana**. Atšķirības starp resursu rezervācijām un piešķirēm varat saskaņot arī detalizētākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="218bd-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Cilne Resursu saskaņošana](media/RM-how-to-4.png)

<span data-ttu-id="218bd-125">Varat arī izmantot resursu atlasītāju cilnē **Grafiks**, lai meklētu un atlasītu rezervējamos resursus, kas vēl nav daļa no projekta darba grupas.</span><span class="sxs-lookup"><span data-stu-id="218bd-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="218bd-126">Tie tiek parādīti resursu atlasītājā kā **Citi resursi**.</span><span class="sxs-lookup"><span data-stu-id="218bd-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Darba grupā neiekļauta dalībnieka resursa piešķiršana uzdevumam](media/RM-how-to-5.png)

<span data-ttu-id="218bd-128">Veicot šo darbību, resurss tiek pievienots projekta darba grupai un piešķirts uzdevumam, taču netiek ģenerētas rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="218bd-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Darba grupas dalībnieks ar piešķirēm un bez rezervācijām](media/RM-how-to-6.png)

<span data-ttu-id="218bd-130">Varat izmantot cilnes **Saskaņošana** rezervācijas paplašināšanas iespēju vai vienumu **Plānošanas panelis**, lai rezervētu resursa noslodzi uz projektā.</span><span class="sxs-lookup"><span data-stu-id="218bd-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Rezervāciju paplašināšana darba grupas dalībniekam resursu saskaņošanas cilnē](media/RM-how-to-7.png)

<span data-ttu-id="218bd-132">Pēc tam, kad darba grupas dalībnieks ir rezervēts projektā, varat izmantot rezervāciju uzturēšanas iespēju vai vienumu Plānošanas panelis, lai tiešā veidā pārvaldītu to rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="218bd-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]