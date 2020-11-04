---
title: Projekta atjaunināšana
description: Šajā tēmā ir sniegta informācija par projektu atjaunināšanu programmā Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080299"
---
# <a name="update-a-project"></a><span data-ttu-id="b1581-103">Projekta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="b1581-103">Update a project</span></span>

<span data-ttu-id="b1581-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="b1581-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b1581-105">Tālāk ir sniegts kopsavilkums par laukiem, ko var atjaunināt projektā pēc tā izveides, kā arī jebkādu spēkā esošu atjauninājumu ietekmi.</span><span class="sxs-lookup"><span data-stu-id="b1581-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="b1581-106">Projekta informācijas lauki</span><span class="sxs-lookup"><span data-stu-id="b1581-106">Project detail fields</span></span>

- <span data-ttu-id="b1581-107">**Nosaukums** : projekta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="b1581-107">**Name** : The title of the project.</span></span>
- <span data-ttu-id="b1581-108">**Apraksts** : projekta pārskats.</span><span class="sxs-lookup"><span data-stu-id="b1581-108">**Description** : An overview of the project.</span></span>
- <span data-ttu-id="b1581-109">**Klients** : uzņēmums, kam tiks nodrošināts projekts.</span><span class="sxs-lookup"><span data-stu-id="b1581-109">**Customer** : The company the project will be delivered to.</span></span>
- <span data-ttu-id="b1581-110">**Kalendāra veidne** : projekta darba laiks.</span><span class="sxs-lookup"><span data-stu-id="b1581-110">**Calendar template** : The working hours of the project.</span></span> <span data-ttu-id="b1581-111">Mainot lauku, tiek pārrēķināts viss grafiks.</span><span class="sxs-lookup"><span data-stu-id="b1581-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="b1581-112">**Valūta** : projekta valūta.</span><span class="sxs-lookup"><span data-stu-id="b1581-112">**Currency** : The currency for the project.</span></span> <span data-ttu-id="b1581-113">Šī lauka pamatā pēc noklusējuma ir līgumslēdzēja vienībai definētā valūta.</span><span class="sxs-lookup"><span data-stu-id="b1581-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="b1581-114">Atjauninot līgumslēdzēja vienību, tiek atjaunināts arī šis lauks.</span><span class="sxs-lookup"><span data-stu-id="b1581-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="b1581-115">**Līgumslēdzēja vienība** : organizācijas struktūrvienība, kas pārstāv uzņēmuma grupu vai nodaļu, kas ir primāri atbildīga par pārdošanas darījuma iegūšanu, kā arī darba un pakalpojumu sniegšanas klientam pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="b1581-115">**Contracting Unit** : The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="b1581-116">**Projekta vadītājs** : projekta darba grupas dalībnieks, kuram ir pilnvaras pārskatīt un apstiprināt laika ierakstus un izdevumus.</span><span class="sxs-lookup"><span data-stu-id="b1581-116">**Project Manager** : The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="b1581-117">Aprēķina lauki</span><span class="sxs-lookup"><span data-stu-id="b1581-117">Estimate fields</span></span>

- <span data-ttu-id="b1581-118">**Plānotais sākuma datums** : datums, kurā sāksies projekts.</span><span class="sxs-lookup"><span data-stu-id="b1581-118">**Estimated Start Date** : The date that the project will begin.</span></span> <span data-ttu-id="b1581-119">Atjauninot šo lauku, visi projekta uzdevumi tiks proporcionāli pārvietoti uz jauno sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="b1581-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="b1581-120">**Beigu datums** : datums, kurā plānots pabeigt projektu.</span><span class="sxs-lookup"><span data-stu-id="b1581-120">**Finish Date** : The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="b1581-121">**Ieguldījums** : paredzamais projekta ieguldījums.</span><span class="sxs-lookup"><span data-stu-id="b1581-121">**Effort** : The estimated effort of the project.</span></span> <span data-ttu-id="b1581-122">Kad projektam ir pievienoti uzdevumi, šis lauks vairs nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="b1581-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="b1581-123">**Novērtētās darba izmaksas** : novērtētās projekta darba izmaksas.</span><span class="sxs-lookup"><span data-stu-id="b1581-123">**Estimated Labor Cost** : The estimated labor cost of the project.</span></span> <span data-ttu-id="b1581-124">Kad projektam ir pievienotas darba izmaksas, šis lauks vairs nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="b1581-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="b1581-125">**Paredzamie izdevumi** : paredzamie projekta izdevumi.</span><span class="sxs-lookup"><span data-stu-id="b1581-125">**Estimated Expenses** : The estimated expenses of the project.</span></span> <span data-ttu-id="b1581-126">Kad projektam ir pievienoti izdevumi, šis lauks vairs nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="b1581-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="b1581-127">Projekta faktisko datu lauki</span><span class="sxs-lookup"><span data-stu-id="b1581-127">Project actual fields</span></span>
- <span data-ttu-id="b1581-128">**Faktiskais sākums** : projekta sākšanas datums.</span><span class="sxs-lookup"><span data-stu-id="b1581-128">**Actual Start** : The date that the project started.</span></span>
- <span data-ttu-id="b1581-129">**Faktiskais beigu laiks** : ir jāatjaunina, kad projekts ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="b1581-129">**Actual Finish** : To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="b1581-130">Projekta statusa lauki</span><span class="sxs-lookup"><span data-stu-id="b1581-130">Project status fields</span></span>

- <span data-ttu-id="b1581-131">**Vispārējais projekta statuss** : projekta vadītāja nodrošinātā vispārējā projekta veselība.</span><span class="sxs-lookup"><span data-stu-id="b1581-131">**Overall Project Status** : The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="b1581-132">**Komentāri** : projekta vadītāja sniegtais apraksts par projekta pašreizējo veselību.</span><span class="sxs-lookup"><span data-stu-id="b1581-132">**Comments** : A narrative regarding the current health of the project provided by the Project manager.</span></span>

