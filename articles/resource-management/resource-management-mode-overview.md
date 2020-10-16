---
title: Resursu pārvaldības režīma pārskats
description: Šajā tēmā ir sniegta informācija par resursu pārvaldības funkcionalitāti programmā Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930100"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="a7e4d-103">Resursu pārvaldības režīma pārskats</span><span class="sxs-lookup"><span data-stu-id="a7e4d-103">Resource management modes overview</span></span>

<span data-ttu-id="a7e4d-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="a7e4d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a7e4d-105">Dynamics 365 Project Operations atbalsta divus režīmus, lai jūs varētu izpildīt vispārējo rezervācijas plūsmu.</span><span class="sxs-lookup"><span data-stu-id="a7e4d-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="a7e4d-106">Pārvaldības režīms tiek definēts kā projekta parametrs, un to var modificēt, ja jūsu uzņēmumam ir nepieciešamas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="a7e4d-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="a7e4d-107">Centrālais režīms</span><span class="sxs-lookup"><span data-stu-id="a7e4d-107">Central mode</span></span>
<span data-ttu-id="a7e4d-108">Organizācijām, kas centralizē resursu piešķiršanu projektiem, centrālais režīms nodrošina veidu, kā projekta vadītāji var definēt resursu prasības projekta līmenī.</span><span class="sxs-lookup"><span data-stu-id="a7e4d-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="a7e4d-109">Resursu prasību izpilde tiek deleģēta resursu pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="a7e4d-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="a7e4d-110">Projekta vadītāji var pieņemt vai noraidīt resursus, ko piedāvā resursu pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="a7e4d-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centrālais režīms](./media/resource-management-central.png)

<span data-ttu-id="a7e4d-112">Lai pārvaldītu resursus, izmantojot centrālo režīmu, skatiet:</span><span class="sxs-lookup"><span data-stu-id="a7e4d-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="a7e4d-113">Vispārīgu grāmatojamu resursu piešķiršana uzdevumam un resursu vajadzību ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="a7e4d-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="a7e4d-114">Rezervēt nosauktos resursus no resursu vajadzībām</span><span class="sxs-lookup"><span data-stu-id="a7e4d-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="a7e4d-115">Submit a resource request</span><span class="sxs-lookup"><span data-stu-id="a7e4d-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="a7e4d-116">Resursa pieprasījuma izpilde</span><span class="sxs-lookup"><span data-stu-id="a7e4d-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="a7e4d-117">Piedāvātā projekta resursa pieņemšana vai noraidīšana, izmantojot resursa pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="a7e4d-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="a7e4d-118">Hibrīda režīms</span><span class="sxs-lookup"><span data-stu-id="a7e4d-118">Hybrid mode</span></span>
<span data-ttu-id="a7e4d-119">Organizācijām, kurām ir nepieciešama elastība attiecībā uz resursu piešķiršanu, hibrīda režīms sniedz iespēju gan projekta vadītājiem, gan resursu pārvaldniekiem rezervēt resursus.</span><span class="sxs-lookup"><span data-stu-id="a7e4d-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hibrīda režīms](./media/resource-management-hybrid.png)

<span data-ttu-id="a7e4d-121">Papildus atbalstītajam centrālā režīma procesam skatiet šīs tēmas, lai pārvaldītu visas citas atbalstītās rezervācijas plūsmas hibrīda režīmā:</span><span class="sxs-lookup"><span data-stu-id="a7e4d-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="a7e4d-122">Resursa rezervēšana tieši projektam:</span><span class="sxs-lookup"><span data-stu-id="a7e4d-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="a7e4d-123">Nosaukto rezervējamo resursu rezervēšana projekta darba grupai un uzdevumu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="a7e4d-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="a7e4d-124">Resursa rezervēšana no resursa prasības:</span><span class="sxs-lookup"><span data-stu-id="a7e4d-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="a7e4d-125">Vispārīgu grāmatojamu resursu piešķiršana uzdevumam un resursu vajadzību ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="a7e4d-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="a7e4d-126">Rezervēt nosauktos resursus no resursu vajadzībām</span><span class="sxs-lookup"><span data-stu-id="a7e4d-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
