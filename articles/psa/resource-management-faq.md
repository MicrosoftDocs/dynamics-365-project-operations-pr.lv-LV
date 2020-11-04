---
title: Bieži uzdotie jautājumi par resursu pārvaldību
description: Šajā tēmā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par resursu pārvaldību.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080655"
---
# <a name="resource-management-faq"></a><span data-ttu-id="52155-103">Bieži uzdotie jautājumi par resursu pārvaldību</span><span class="sxs-lookup"><span data-stu-id="52155-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="52155-104">Kāda ir atšķirība starp darba grupas dalībnieku un resursu vajadzību?</span><span class="sxs-lookup"><span data-stu-id="52155-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="52155-105">Projekta darba grupas dalībniekam var piešķirt uzdevumus, to var rezervēt, tam var pārsniegt rezervācijas, kā arī to var iestatīt kā apstiprinātāju.</span><span class="sxs-lookup"><span data-stu-id="52155-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="52155-106">Resursa vajadzība var pastāvēt bez projekta darba grupas dalībnieka kā pieprasījuma melnraksts.</span><span class="sxs-lookup"><span data-stu-id="52155-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="52155-107">Kāda ir atšķirība starp piedāvātajām un viegli rezervētajām stundām?</span><span class="sxs-lookup"><span data-stu-id="52155-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="52155-108">Piedāvātās stundas un viegli rezervētās stundas atšķiras to redzamības ziņā.</span><span class="sxs-lookup"><span data-stu-id="52155-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="52155-109">Piedāvātās stundas ir redzamas tikai resursu vadītājiem un projektu vadītājam, kas uzsāka pieprasījumu, izmantojot resursa pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="52155-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="52155-110">Viegli rezervētās stundas ir redzamas ikvienam, kas var piekļūt plānošanas panelim.</span><span class="sxs-lookup"><span data-stu-id="52155-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="52155-111">Kā var redzēt viegli rezervētās stundas resursiem darba grupā?</span><span class="sxs-lookup"><span data-stu-id="52155-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="52155-112">Vieglās rezervācijas var veikt, rezervējot resursa vajadzību.</span><span class="sxs-lookup"><span data-stu-id="52155-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="52155-113">Resursi, kas ir viegli rezervēti projekta darba grupā, tiek parādīti kā darba grupas dalībnieki, kuriem ir viegli rezervētas stundas.</span><span class="sxs-lookup"><span data-stu-id="52155-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="52155-114">Tie parādās arī plānošanas panelī.</span><span class="sxs-lookup"><span data-stu-id="52155-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="52155-115">Kā mainīt nepieciešamās stundas un sākuma un beigu datumus attiecībā uz resursu (vispārēju vai nosauktu), kuru esmu rezervējis?</span><span class="sxs-lookup"><span data-stu-id="52155-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="52155-116">Kad resursi ir rezervēti, atlasiet opciju **Uzturēt rezervācijas** , lai veiktu vajadzīgās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="52155-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="52155-117">Kādus resursu tipus atbalsta Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="52155-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="52155-118">**Lietotājs** un **Kontaktpersona** ir vienīgie resursu tipi, kuri tiek atbalstīti programmā Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="52155-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="52155-119">Lai gan var izveidot citus resursu tipus (piemēram, **Aprīkojums** un **Grupa** ), tiem netiek atbalstīta visaptveroša lietošana.</span><span class="sxs-lookup"><span data-stu-id="52155-119">Although you can create other types of resources (for example, **Equipment** and **Group** ), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="52155-120">Kāda ir atšķirība starp piešķiri un rezervāciju?</span><span class="sxs-lookup"><span data-stu-id="52155-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="52155-121">Piešķires ir resursu piešķiršana projekta uzdevumiem projekta grafikā.</span><span class="sxs-lookup"><span data-stu-id="52155-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="52155-122">Resursi var būt vai reāli vai vispārēji.</span><span class="sxs-lookup"><span data-stu-id="52155-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="52155-123">Rezervācijas ir resursu stingra vai viegla piešķiršana projektam.</span><span class="sxs-lookup"><span data-stu-id="52155-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="52155-124">Stingrās rezervācijas patērē resursu noslodzi.</span><span class="sxs-lookup"><span data-stu-id="52155-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="52155-125">Ideālā gadījumā attiecībā uz reāliem resursiem rezervācijām būtu jāatbilst piešķirēm, jo tās neatšķiras.</span><span class="sxs-lookup"><span data-stu-id="52155-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="52155-126">Tomēr PSA neparedz obligātu šādu atbilstību.</span><span class="sxs-lookup"><span data-stu-id="52155-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="52155-127">Saskaņošanas skats norāda projekta vadītājiem gadījumus, kad resursu rezervācijas neatbilst piešķirēm.</span><span class="sxs-lookup"><span data-stu-id="52155-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
