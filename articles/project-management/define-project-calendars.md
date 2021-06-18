---
title: Projekta kalendāru definēšana
description: Šajā tēmā ir sniegta informācija par to, kā projektam lietot kalendāra veidni, lai sekotu līdzi projekta grafikam.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999005"
---
# <a name="define-project-calendars"></a><span data-ttu-id="7b782-103">Projekta kalendāru definēšana</span><span class="sxs-lookup"><span data-stu-id="7b782-103">Define project calendars</span></span>

<span data-ttu-id="7b782-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="7b782-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7b782-105">Lai izveidotu un pārvaldītu projektu, projektam jālieto kalendāra veidne.</span><span class="sxs-lookup"><span data-stu-id="7b782-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="7b782-106">Kalendāra veidne definē šādus projekta atribūtus:</span><span class="sxs-lookup"><span data-stu-id="7b782-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="7b782-107">darba stundas, ieskaitot sākuma un beigu laiku;</span><span class="sxs-lookup"><span data-stu-id="7b782-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="7b782-108">darba dienas;</span><span class="sxs-lookup"><span data-stu-id="7b782-108">Working days</span></span>
- <span data-ttu-id="7b782-109">kalendāra izņēmumi, piemēram, brīvdienas.</span><span class="sxs-lookup"><span data-stu-id="7b782-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="7b782-110">Projektam lietotā kalendāra veidne ir organizācijas iestatījumos definētās kalendāra veidnes kopija.</span><span class="sxs-lookup"><span data-stu-id="7b782-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="7b782-111">Ja maināt kalendāra veidni, šīs izmaiņas netiek attiecinātas uz projekta darba laiku.</span><span class="sxs-lookup"><span data-stu-id="7b782-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="7b782-112">Lai mainītu projekta darba laiku, jālieto jauna veidne.</span><span class="sxs-lookup"><span data-stu-id="7b782-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="7b782-113">Lai organizācijai izveidotu kalendāra veidni, ir divas galvenās prasības:</span><span class="sxs-lookup"><span data-stu-id="7b782-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="7b782-114">definējiet veidnes vēlamo darba laiku, izmantojot jaunu vai esošu rezervējamu resursu;</span><span class="sxs-lookup"><span data-stu-id="7b782-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="7b782-115">izveidojiet jaunu kalendāra veidni un saistiet to ar rezervējamo resursu.</span><span class="sxs-lookup"><span data-stu-id="7b782-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="7b782-116">**Veidnes darba laiku definēšana**</span><span class="sxs-lookup"><span data-stu-id="7b782-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="7b782-117">Atveriet sadaļu **Resursi** \> **Resursi.**</span><span class="sxs-lookup"><span data-stu-id="7b782-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="7b782-118">Izveidojiet jaunu resursu atsaucei kalendāra veidnē vai atlasiet esošu resursu.</span><span class="sxs-lookup"><span data-stu-id="7b782-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="7b782-119">Atlasiet resursa cilni **Darba stundas** un izpildiet sadaļā [Resursa darba stundu iestatīšana](/dynamics365/field-service/set-work-hours-resource.md) sniegtos norādījumus, lai konfigurētu kalendāra kārtulas.</span><span class="sxs-lookup"><span data-stu-id="7b782-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="7b782-120">**Jaunas kalendāra veidnes izveide**</span><span class="sxs-lookup"><span data-stu-id="7b782-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="7b782-121">Pārejiet uz **Iestatījumi** \> **Kalendāra veidne**.</span><span class="sxs-lookup"><span data-stu-id="7b782-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="7b782-122">Atlasiet **Jauns** un ievadiet nosaukumu, aprakstu un veidnes resursu.</span><span class="sxs-lookup"><span data-stu-id="7b782-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="7b782-123">Ja kalendārā ir atsauce uz resursu, ar šo kalendāra veidni tiek saistīta resursa kalendāra kopija.</span><span class="sxs-lookup"><span data-stu-id="7b782-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="7b782-124">Ja tiek mainītas kopētās veidnes darba stundas, šīs izmaiņas netiek attiecinātas uz kalendāra veidni.</span><span class="sxs-lookup"><span data-stu-id="7b782-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="7b782-125">Tagad šo darba veidni varat sasaistīt ar projekta kalendāra veidni.</span><span class="sxs-lookup"><span data-stu-id="7b782-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

