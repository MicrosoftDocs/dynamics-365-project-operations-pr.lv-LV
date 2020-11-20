---
title: Projekta atjaunināšana
description: Šajā tēmā ir sniegta informācija par projektu atjaunināšanu programmā Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131442"
---
# <a name="update-a-project"></a><span data-ttu-id="86e53-103">Projekta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="86e53-103">Update a project</span></span>

<span data-ttu-id="86e53-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="86e53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="86e53-105">Tālāk ir sniegts kopsavilkums par laukiem, ko var atjaunināt projektā pēc tā izveides, kā arī jebkādu spēkā esošu atjauninājumu ietekmi.</span><span class="sxs-lookup"><span data-stu-id="86e53-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="86e53-106">Projekta informācijas lauki</span><span class="sxs-lookup"><span data-stu-id="86e53-106">Project detail fields</span></span>

- <span data-ttu-id="86e53-107">**Nosaukums**: projekta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="86e53-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="86e53-108">**Apraksts**: projekta pārskats.</span><span class="sxs-lookup"><span data-stu-id="86e53-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="86e53-109">**Klients**: uzņēmums, kam tiks nodrošināts projekts.</span><span class="sxs-lookup"><span data-stu-id="86e53-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="86e53-110">**Kalendāra veidne**: projekta darba laiks.</span><span class="sxs-lookup"><span data-stu-id="86e53-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="86e53-111">Mainot lauku, tiek pārrēķināts viss grafiks.</span><span class="sxs-lookup"><span data-stu-id="86e53-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="86e53-112">**Valūta**: projekta valūta.</span><span class="sxs-lookup"><span data-stu-id="86e53-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="86e53-113">Šī lauka pamatā pēc noklusējuma ir līgumslēdzēja vienībai definētā valūta.</span><span class="sxs-lookup"><span data-stu-id="86e53-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="86e53-114">Atjauninot līgumslēdzēja vienību, tiek atjaunināts arī šis lauks.</span><span class="sxs-lookup"><span data-stu-id="86e53-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="86e53-115">**Līgumslēdzēja vienība**: organizācijas struktūrvienība, kas pārstāv uzņēmuma grupu vai nodaļu, kas ir primāri atbildīga par pārdošanas darījuma iegūšanu, kā arī darba un pakalpojumu sniegšanas klientam pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="86e53-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="86e53-116">**Projekta vadītājs**: projekta darba grupas dalībnieks, kuram ir pilnvaras pārskatīt un apstiprināt laika ierakstus un izdevumus.</span><span class="sxs-lookup"><span data-stu-id="86e53-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="86e53-117">Aprēķina lauki</span><span class="sxs-lookup"><span data-stu-id="86e53-117">Estimate fields</span></span>

- <span data-ttu-id="86e53-118">**Plānotais sākuma datums**: datums, kurā sāksies projekts.</span><span class="sxs-lookup"><span data-stu-id="86e53-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="86e53-119">Atjauninot šo lauku, visi projekta uzdevumi tiks proporcionāli pārvietoti uz jauno sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="86e53-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="86e53-120">**Beigu datums**: datums, kurā plānots pabeigt projektu.</span><span class="sxs-lookup"><span data-stu-id="86e53-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="86e53-121">**Ieguldījums**: paredzamais projekta ieguldījums.</span><span class="sxs-lookup"><span data-stu-id="86e53-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="86e53-122">Kad projektam ir pievienoti uzdevumi, šis lauks vairs nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="86e53-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="86e53-123">**Novērtētās darba izmaksas**: novērtētās projekta darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="86e53-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="86e53-124">Kad projektam ir pievienotas darba izmaksas, šis lauks vairs nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="86e53-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="86e53-125">**Paredzamie izdevumi** : paredzamie projekta izdevumi.</span><span class="sxs-lookup"><span data-stu-id="86e53-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="86e53-126">Kad projektam ir pievienoti izdevumi, šis lauks vairs nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="86e53-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="86e53-127">Projekta faktisko datu lauki</span><span class="sxs-lookup"><span data-stu-id="86e53-127">Project actual fields</span></span>
- <span data-ttu-id="86e53-128">**Faktiskais sākums**: projekta sākšanas datums.</span><span class="sxs-lookup"><span data-stu-id="86e53-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="86e53-129">**Faktiskais beigu laiks**: ir jāatjaunina, kad projekts ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="86e53-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="86e53-130">Projekta statusa lauki</span><span class="sxs-lookup"><span data-stu-id="86e53-130">Project status fields</span></span>

- <span data-ttu-id="86e53-131">**Vispārējais projekta statuss**: projekta vadītāja nodrošinātā vispārējā projekta veselība.</span><span class="sxs-lookup"><span data-stu-id="86e53-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="86e53-132">**Komentāri**: projekta vadītāja sniegtais apraksts par projekta pašreizējo veselību.</span><span class="sxs-lookup"><span data-stu-id="86e53-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

