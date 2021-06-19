---
title: Rezervēšana/piešķires
description: Šajā tēmā ir sniegta informācija par atšķirībām starp resursu rezervācijām un resursu piešķirēm.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012775"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="3ae68-103">Rezervēšana/piešķires</span><span class="sxs-lookup"><span data-stu-id="3ae68-103">Bookings vs assignments</span></span>

<span data-ttu-id="3ae68-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="3ae68-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3ae68-105">Rezervācijas ir resursu stingra vai viegla piešķiršana projektam.</span><span class="sxs-lookup"><span data-stu-id="3ae68-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="3ae68-106">Stingrās rezervācijas patērē resursu noslodzi.</span><span class="sxs-lookup"><span data-stu-id="3ae68-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="3ae68-107">Rezervācijas ir organizatoriska koncepcija darba grupām, lai tās varētu saprast, kā resursi tiks piesaistīti dažādiem projektiem.</span><span class="sxs-lookup"><span data-stu-id="3ae68-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="3ae68-108">Dynamics 365 Project Operations apskata rezervācija kā projekta līmeņa jēdzienu.</span><span class="sxs-lookup"><span data-stu-id="3ae68-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="3ae68-109">Atšķirībā no rezervācijām piešķires ir resursu piešķiršana projekta uzdevumiem projekta grafikā.</span><span class="sxs-lookup"><span data-stu-id="3ae68-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="3ae68-110">Resursiem var piešķirt nosaukumus, vai tie var būt vispārēji.</span><span class="sxs-lookup"><span data-stu-id="3ae68-110">The resources can be named or generic.</span></span>  <span data-ttu-id="3ae68-111">Ja resursa prasību atvasina no projekta uzdevumu piešķirēm, Project Operations izmanto resursu piešķires darba kontūras, lai veidotu resursa pieprasījuma informācijas kontūras.</span><span class="sxs-lookup"><span data-stu-id="3ae68-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="3ae68-112">Taču netiek saglabāta atsauce uz resursa piešķirēm.</span><span class="sxs-lookup"><span data-stu-id="3ae68-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="3ae68-113">No resursa prasības iegūtu rezervāciju atjauninājumi neatjaunina resursu piešķires.</span><span class="sxs-lookup"><span data-stu-id="3ae68-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="3ae68-114">Parasti resursa rezervācijas summa būs vienāda ar resursa piešķiru summu vienā vai vairākos uzdevumos.</span><span class="sxs-lookup"><span data-stu-id="3ae68-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="3ae68-115">Tomēr Project Operations neparedz šādu atbilstību kā obligātu.</span><span class="sxs-lookup"><span data-stu-id="3ae68-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="3ae68-116">Skats **Saskaņošana** projektu vadītājiem parāda gadījumus, kad resursu rezervācijas neatbilst piešķirēm.</span><span class="sxs-lookup"><span data-stu-id="3ae68-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]