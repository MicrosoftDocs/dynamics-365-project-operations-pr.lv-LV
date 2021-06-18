---
title: Darba stundu veidnes izveide
description: Šajā tēmā ir aprakstīts, kā izveidot darba stundu veidni programmā Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997205"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="29a95-103">Darba stundu veidnes izveide (Project Service)</span><span class="sxs-lookup"><span data-stu-id="29a95-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="29a95-104">Lai izveidotu un pārvaldītu projektu, projektam jālieto kalendāra veidne.</span><span class="sxs-lookup"><span data-stu-id="29a95-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="29a95-105">Kalendāra veidne definē šādus projekta atribūtus:</span><span class="sxs-lookup"><span data-stu-id="29a95-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="29a95-106">darba stundas, ieskaitot sākuma un beigu laiku;</span><span class="sxs-lookup"><span data-stu-id="29a95-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="29a95-107">darba dienas;</span><span class="sxs-lookup"><span data-stu-id="29a95-107">Working days</span></span>
- <span data-ttu-id="29a95-108">kalendāra izņēmumi, piemēram, brīvdienas.</span><span class="sxs-lookup"><span data-stu-id="29a95-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="29a95-109">Projektam lietotā kalendāra veidne ir organizācijas iestatījumos definētās kalendāra veidnes kopija.</span><span class="sxs-lookup"><span data-stu-id="29a95-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="29a95-110">Ja maināt kalendāra veidni, šīs izmaiņas netiek attiecinātas uz projekta darba laiku.</span><span class="sxs-lookup"><span data-stu-id="29a95-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="29a95-111">Lai mainītu projekta darba laiku, jālieto jauna veidne.</span><span class="sxs-lookup"><span data-stu-id="29a95-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="29a95-112">Lai organizācijai izveidotu kalendāra veidni, ir divas galvenās prasības:</span><span class="sxs-lookup"><span data-stu-id="29a95-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="29a95-113">definējiet veidnes vēlamo darba laiku, izmantojot jaunu vai esošu rezervējamu resursu;</span><span class="sxs-lookup"><span data-stu-id="29a95-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="29a95-114">izveidojiet jaunu kalendāra veidni un saistiet to ar rezervējamo resursu.</span><span class="sxs-lookup"><span data-stu-id="29a95-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="29a95-115">**Veidnes darba laiku definēšana**</span><span class="sxs-lookup"><span data-stu-id="29a95-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="29a95-116">Atveriet sadaļu **Resursi** \> **Resursi.**</span><span class="sxs-lookup"><span data-stu-id="29a95-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="29a95-117">Izveidojiet jaunu resursu atsaucei kalendāra veidnē vai atlasiet esošu resursu.</span><span class="sxs-lookup"><span data-stu-id="29a95-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="29a95-118">Atlasiet resursa cilni **Darba stundas** un izpildiet sadaļā [Resursa darba stundu iestatīšana](/dynamics365/field-service/set-work-hours-resource.md) sniegtos norādījumus, lai konfigurētu kalendāra kārtulas.</span><span class="sxs-lookup"><span data-stu-id="29a95-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="29a95-119">**Jaunas kalendāra veidnes izveide**</span><span class="sxs-lookup"><span data-stu-id="29a95-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="29a95-120">Pārejiet uz **Iestatījumi** \> **Kalendāra veidne**.</span><span class="sxs-lookup"><span data-stu-id="29a95-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="29a95-121">Atlasiet **Jauns** un ievadiet nosaukumu, aprakstu un veidnes resursu.</span><span class="sxs-lookup"><span data-stu-id="29a95-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="29a95-122">Ja kalendārā ir atsauce uz resursu, ar šo kalendāra veidni tiek saistīta resursa kalendāra kopija.</span><span class="sxs-lookup"><span data-stu-id="29a95-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="29a95-123">Ja tiek mainītas kopētās veidnes darba stundas, šīs izmaiņas netiek attiecinātas uz kalendāra veidni.</span><span class="sxs-lookup"><span data-stu-id="29a95-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="29a95-124">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="29a95-124">See Also</span></span>  
 [<span data-ttu-id="29a95-125">Resursu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="29a95-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
