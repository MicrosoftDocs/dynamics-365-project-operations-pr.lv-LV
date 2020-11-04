---
title: Projekta pārdošanas pasūtījumi laika un materiālu projektiem
description: Šajā tēmā izskaidrots, kā izveidot projektā balstītus pārdošanas pasūtījumus laika un materiālu projektiem.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080429"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="c031d-103">Projekta pārdošanas pasūtījumi laika un materiālu projektiem</span><span class="sxs-lookup"><span data-stu-id="c031d-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c031d-104">Šajā tēmā aprakstīts, kā izveidot pārdošanas pasūtījumu projektam.</span><span class="sxs-lookup"><span data-stu-id="c031d-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="c031d-105">Pārdošanas pasūtījumus var izveidot vienīgi projektiem ar veidu **laiks un materiāli**.</span><span class="sxs-lookup"><span data-stu-id="c031d-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="c031d-106">Ja laika un materiālu projektam projekta līgumā ir vairāki finansējuma avoti, ir jāiespējo parametrs **Atļaut pārdošanas pasūtījumus projektiem ar vairākiem finansējuma avotiem** lapā **Projekta pārvaldības un uzskaites parametri**.</span><span class="sxs-lookup"><span data-stu-id="c031d-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="c031d-107">Atbalsts projekta pārdošanas pasūtījumiem ar vairākiem finansējuma avotiem ir pieejams sākot ar programmas laidienu 10.0.2 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="c031d-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="c031d-108">Parametrs projekta pārdošanas pasūtījumu ar vairākiem finansējuma avotiem iespējošanai tiks noņemts 2020. gada aprīļa laidiena vilnī, pēc kura šī funkcionalitāte būs iespējota vienmēr.</span><span class="sxs-lookup"><span data-stu-id="c031d-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="c031d-109">Projektā balstītus pārdošanas pasūtījumus varat izveidot divos veidos:</span><span class="sxs-lookup"><span data-stu-id="c031d-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="c031d-110">Dodieties uz pašu projektu.</span><span class="sxs-lookup"><span data-stu-id="c031d-110">Go to the project itself.</span></span> <span data-ttu-id="c031d-111">Darbību rūtī atlasiet **Pārvaldīt > Elementu uzdevumi > Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="c031d-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="c031d-112">Projekta informācija pēc noklusējuma būs no projekta pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="c031d-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="c031d-113">Ja projekta līgumam ir vairāk nekā viens finansējuma avots, būs nepieciešams atlasīt finansējuma avotu, lai iestatītu pārdošanas pasūtījuma klientu.</span><span class="sxs-lookup"><span data-stu-id="c031d-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="c031d-114">Ja projektam ir tikai viens finansējuma avots, klients tiks iestatīts automātiski.</span><span class="sxs-lookup"><span data-stu-id="c031d-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="c031d-115">Dodieties uz saraksta lapu **Visi pārdošanas pasūtījumi** un izveidojiet jaunu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c031d-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="c031d-116">Pārdošanas pasūtījumam vajadzēs atlasīt projektu.</span><span class="sxs-lookup"><span data-stu-id="c031d-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="c031d-117">Kad projekts ir atlasīts, klients tiks iestatīts no finansējuma avota vai arī vajadzēs atlasīt finansējuma avotu, ja projekta līgumam ir vairāki finansējuma avoti.</span><span class="sxs-lookup"><span data-stu-id="c031d-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

