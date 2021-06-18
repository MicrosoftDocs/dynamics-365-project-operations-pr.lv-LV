---
title: Projekta atjaunināšana
description: Šajā tēmā ir sniegta informācija par projektu atjaunināšanu programmā Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c07542444b970430d8143a60aad6970305769b22
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993380"
---
# <a name="update-a-project"></a><span data-ttu-id="555cf-103">Projekta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="555cf-103">Update a project</span></span>

<span data-ttu-id="555cf-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="555cf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="555cf-105">Tālāk ir sniegts kopsavilkums par laukiem, ko var atjaunināt projektā pēc tā izveides, kā arī jebkādu spēkā esošu atjauninājumu ietekmi.</span><span class="sxs-lookup"><span data-stu-id="555cf-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="555cf-106">Projekta informācijas lauki</span><span class="sxs-lookup"><span data-stu-id="555cf-106">Project detail fields</span></span>

- <span data-ttu-id="555cf-107">**Nosaukums**: projekta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="555cf-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="555cf-108">**Apraksts**: projekta pārskats.</span><span class="sxs-lookup"><span data-stu-id="555cf-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="555cf-109">**Klients**: uzņēmums, kam tiks nodrošināts projekts.</span><span class="sxs-lookup"><span data-stu-id="555cf-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="555cf-110">**Kalendāra veidne**: projekta darba laiks.</span><span class="sxs-lookup"><span data-stu-id="555cf-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="555cf-111">Mainot lauku, tiek pārrēķināts viss grafiks.</span><span class="sxs-lookup"><span data-stu-id="555cf-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="555cf-112">**Valūta**: projekta valūta.</span><span class="sxs-lookup"><span data-stu-id="555cf-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="555cf-113">Šī lauka pamatā pēc noklusējuma ir līgumslēdzēja vienībai definētā valūta.</span><span class="sxs-lookup"><span data-stu-id="555cf-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="555cf-114">Atjauninot līgumslēdzēja vienību, tiek atjaunināts arī šis lauks.</span><span class="sxs-lookup"><span data-stu-id="555cf-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="555cf-115">**Līgumslēdzēja vienība**: organizācijas struktūrvienība, kas pārstāv uzņēmuma grupu vai nodaļu, kas ir primāri atbildīga par pārdošanas darījuma iegūšanu, kā arī darba un pakalpojumu sniegšanas klientam pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="555cf-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="555cf-116">**Projekta vadītājs**: projekta darba grupas dalībnieks, kuram ir pilnvaras pārskatīt un apstiprināt laika ierakstus un izdevumus.</span><span class="sxs-lookup"><span data-stu-id="555cf-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="555cf-117">Aprēķina lauki</span><span class="sxs-lookup"><span data-stu-id="555cf-117">Estimate fields</span></span>

- <span data-ttu-id="555cf-118">**Plānotais sākuma datums**: datums, kurā sāksies projekts.</span><span class="sxs-lookup"><span data-stu-id="555cf-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="555cf-119">Atjauninot šo lauku, visi projekta uzdevumi tiks proporcionāli pārvietoti uz jauno sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="555cf-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="555cf-120">**Beigu datums**: datums, kurā plānots pabeigt projektu.</span><span class="sxs-lookup"><span data-stu-id="555cf-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="555cf-121">**Ieguldījums**: paredzamais projekta ieguldījums.</span><span class="sxs-lookup"><span data-stu-id="555cf-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="555cf-122">Kad projektam ir pievienoti uzdevumi, šis lauks vairs nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="555cf-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="555cf-123">**Novērtētās darba izmaksas**: novērtētās projekta darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="555cf-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="555cf-124">Kad projektam ir pievienotas darba izmaksas, šis lauks vairs nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="555cf-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="555cf-125">**Paredzamie izdevumi** : paredzamie projekta izdevumi.</span><span class="sxs-lookup"><span data-stu-id="555cf-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="555cf-126">Kad projektam ir pievienoti izdevumi, šis lauks vairs nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="555cf-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="555cf-127">Projekta faktisko datu lauki</span><span class="sxs-lookup"><span data-stu-id="555cf-127">Project actual fields</span></span>
- <span data-ttu-id="555cf-128">**Faktiskais sākums**: projekta sākšanas datums.</span><span class="sxs-lookup"><span data-stu-id="555cf-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="555cf-129">**Faktiskais beigu laiks**: ir jāatjaunina, kad projekts ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="555cf-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="555cf-130">Projekta statusa lauki</span><span class="sxs-lookup"><span data-stu-id="555cf-130">Project status fields</span></span>

- <span data-ttu-id="555cf-131">**Vispārējais projekta statuss**: projekta vadītāja nodrošinātā vispārējā projekta veselība.</span><span class="sxs-lookup"><span data-stu-id="555cf-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="555cf-132">**Komentāri**: projekta vadītāja sniegtais apraksts par projekta pašreizējo veselību.</span><span class="sxs-lookup"><span data-stu-id="555cf-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]