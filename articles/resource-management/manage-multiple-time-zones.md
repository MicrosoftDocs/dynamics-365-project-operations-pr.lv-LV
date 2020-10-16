---
title: Laika joslu pārvaldība
description: Izveidojot projektu, tā laika josla ir pamatota uz laika joslu, kas definēta pielietotajā darba stundu veidnē.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961906"
---
# <a name="manage-time-zones"></a><span data-ttu-id="a3051-103">Laika joslu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="a3051-103">Manage time zones</span></span>

<span data-ttu-id="a3051-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="a3051-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="a3051-105">Projekti</span><span class="sxs-lookup"><span data-stu-id="a3051-105">Projects</span></span>

<span data-ttu-id="a3051-106">Izveidojot projektu, laika josla ir pamatota uz laika joslu, kas definēta pielietotajā darba stundu veidnē.</span><span class="sxs-lookup"><span data-stu-id="a3051-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="a3051-107">Veidlapā **Projekts** datumi vienmēr ir relatīvi attiecībā pret tā lietotāja laika joslu, kas ir pieteicies katrā cilnē, izņemot cilnē **Uzdevums**. Skatot darba sadalījuma struktūru, datumi vienmēr tiek rādīti projekta laika joslā.</span><span class="sxs-lookup"><span data-stu-id="a3051-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="a3051-108">Uzdevumi</span><span class="sxs-lookup"><span data-stu-id="a3051-108">Tasks</span></span>

<span data-ttu-id="a3051-109">Izveidojot uzdevumu, sākuma laiks, beigu laiks un stundu skaits dienā tiek kontrolētas pēc projekta darba laika.</span><span class="sxs-lookup"><span data-stu-id="a3051-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="a3051-110">Piemēram, ja uzdevums ir izveidots projektā, kura laika zona ir -8 PST un kurā darba laiks ir no 9.00 līdz 17.00 no pirmdienas līdz piektdienai, jebkurš uzdevums, kas izveidots bez piešķires, pakļaujas projekta kalendāra sākuma laikam un beigu laikam.</span><span class="sxs-lookup"><span data-stu-id="a3051-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="a3051-111">Resursu pārvaldība ar laika zonām</span><span class="sxs-lookup"><span data-stu-id="a3051-111">Manage resources with time zones</span></span>

<span data-ttu-id="a3051-112">Lai iegūtu precīzus un prognozējamus rezultātus, izmantojot opciju **Paplašināt rezervāciju**, ir jāizpilda divi galvenie priekšnosacījumi.</span><span class="sxs-lookup"><span data-stu-id="a3051-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="a3051-113">Lietotājam ir jākonfigurē savas ierīces laika josla tādējādi, lai tā atbilstu tai laika joslai, kas definēta sistēmas iestatījumos **Personalizēšanas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="a3051-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Laika joslu iestatījumi operētājsistēmā Windows 10](media/reconcile-assignments-03.png)

  ![Laika joslu iestatījumi personalizēšanas iestatījumos](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="a3051-116">Rezervējamam resursam ir jābūt vismaz vienai minūtei no darba laika, kas pārklājas ar kontūrām, kas tiek izmantotas pieprasītā paplašinājuma definēšanai.</span><span class="sxs-lookup"><span data-stu-id="a3051-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="a3051-117">Piemēram, tālāk norādītie resursi ar darba laiku no plkst. 9.00 līdz 19.00.</span><span class="sxs-lookup"><span data-stu-id="a3051-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Resursu kontūru salīdzinājums](media/reconcile-assignments-05.png)

<span data-ttu-id="a3051-119">Tālāk sniegtajā tabulā ir norādīts:</span><span class="sxs-lookup"><span data-stu-id="a3051-119">The following table shows:</span></span>

- <span data-ttu-id="a3051-120">Projekta kalendāra veidne</span><span class="sxs-lookup"><span data-stu-id="a3051-120">A project calendar template</span></span>
- <span data-ttu-id="a3051-121">Resurss A: šim resursam ir viens un tas pats kalendārs, un tas atrodas vienā laika joslā ar projektu.</span><span class="sxs-lookup"><span data-stu-id="a3051-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="a3051-122">Rezervācijas sākuma laiks būs 9:00.</span><span class="sxs-lookup"><span data-stu-id="a3051-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="a3051-123">Resurss B: šis resurss atrodas no projekta atšķirīgā laika joslā un darbu sāk plkst. 7.00 savā laika joslā.</span><span class="sxs-lookup"><span data-stu-id="a3051-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="a3051-124">Tomēr rezervācijas tiks sāktas ar 9:00, jo tas ir visagrākais piešķiršanas kontūras sākuma laiks.</span><span class="sxs-lookup"><span data-stu-id="a3051-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="a3051-125">Resursi C un D: resursi atrodas dažādās laika zonās, kas atšķiras gan no viena no otras, gan no projekta laika joslas, un resursu rezervācijas sākas ne agrāk kā to attiecīgie pieejamie sākuma laiki.</span><span class="sxs-lookup"><span data-stu-id="a3051-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="a3051-126">Entītija</span><span class="sxs-lookup"><span data-stu-id="a3051-126">Entity</span></span>  |<span data-ttu-id="a3051-127">Kalendārs</span><span class="sxs-lookup"><span data-stu-id="a3051-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="a3051-128">Projekta kalendāra veidne</span><span class="sxs-lookup"><span data-stu-id="a3051-128">Project calendar template</span></span>   | ![projekta kalendārs](media/reconcile-assignments-06.png) |
|<span data-ttu-id="a3051-130">Resurss A</span><span class="sxs-lookup"><span data-stu-id="a3051-130">Resource A</span></span>  | ![Resursa A kalendārs](media/reconcile-assignments-06.png) |
|<span data-ttu-id="a3051-132">Resurss B</span><span class="sxs-lookup"><span data-stu-id="a3051-132">Resource B</span></span>  |  ![Resursa B kalendārs](media/reconcile-assignments-07.png) |
|<span data-ttu-id="a3051-134">Resurss C</span><span class="sxs-lookup"><span data-stu-id="a3051-134">Resource C</span></span>  |  ![Resursa C kalendārs](media/reconcile-assignments-08.png) |
|<span data-ttu-id="a3051-136">Resurss D</span><span class="sxs-lookup"><span data-stu-id="a3051-136">Resource D</span></span>  | ![Resursa D kalendārs](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="a3051-138">Pārejot uz skatu **Saskaņošana**, tiek parādītas resursu piešķires un tiem saistītie rezervāciju deficīti.</span><span class="sxs-lookup"><span data-stu-id="a3051-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Saskaņošanas skats pirms paplašinājuma](media/reconcile-assignments-10.png)

<span data-ttu-id="a3051-140">Pēc tam, kad katram resursam ir izmantota rezervācijas paplašināšanas funkcija, rezervēšana tiek sekmīgi paplašināta katram resursam, jo katra resursa darba laiks pārklājas ar deficīta kontūrām.</span><span class="sxs-lookup"><span data-stu-id="a3051-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Saskaņošanas skats pēc rezervācijas paplašinājuma](media/reconcile-assignments-11.png) 

<span data-ttu-id="a3051-142">Ievērojiet, ka detalizētākā informācijā par rezervējumiem redzamas rezervāciju sākuma laiku atšķirības.</span><span class="sxs-lookup"><span data-stu-id="a3051-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="a3051-143">Rezervācijas sākas ne agrāk kā piešķires kontūras sākuma laiks un ne agrāk kā resursam pieejamais sākuma laiks.</span><span class="sxs-lookup"><span data-stu-id="a3051-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Jaunas resursa rezervācijas plānošanas panelī](media/reconcile-assignments-12.png)
