---
title: Projekta posmi
description: Šajā tēmā sniegta informācija par projekta posmiem, kas ir pieejami Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286797"
---
# <a name="project-stages"></a><span data-ttu-id="f22b2-103">Projekta posmi</span><span class="sxs-lookup"><span data-stu-id="f22b2-103">Project stages</span></span>

<span data-ttu-id="f22b2-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="f22b2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f22b2-105">Projekta posmi ir izstrādāti, lai atspoguļotu projekta statusu tā norises laikā.</span><span class="sxs-lookup"><span data-stu-id="f22b2-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="f22b2-106">Pielāgojumus var izmantot, lai automātiski atjauninātu posmus ar biznesa procesa plūsmām, Power Automate vai spraudņu paplašinājumiem.</span><span class="sxs-lookup"><span data-stu-id="f22b2-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="f22b2-107">Biznesa procesa plūsmā ir definēti šādi posmi:</span><span class="sxs-lookup"><span data-stu-id="f22b2-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="f22b2-108">Izveidot:</span><span class="sxs-lookup"><span data-stu-id="f22b2-108">New</span></span>
- <span data-ttu-id="f22b2-109">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="f22b2-109">Quote</span></span>
- <span data-ttu-id="f22b2-110">Plāns</span><span class="sxs-lookup"><span data-stu-id="f22b2-110">Plan</span></span>
- <span data-ttu-id="f22b2-111">Piegādāt</span><span class="sxs-lookup"><span data-stu-id="f22b2-111">Deliver</span></span>
- <span data-ttu-id="f22b2-112">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="f22b2-112">Complete</span></span>
- <span data-ttu-id="f22b2-113">Aizvēršana</span><span class="sxs-lookup"><span data-stu-id="f22b2-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="f22b2-114">Izveidot:</span><span class="sxs-lookup"><span data-stu-id="f22b2-114">New</span></span>

<span data-ttu-id="f22b2-115">Kad veidojat projektu, šī projekta posms tiek iestatīts uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f22b2-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="f22b2-116">Ja projekts tika izveidots no veidnes, tam var būt grafika, tāmes un darba grupas dati.</span><span class="sxs-lookup"><span data-stu-id="f22b2-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="f22b2-117">Pretējā gadījumā tās ir vispārīgas projekta aprises, un atlikušie komponenti ir jāievada.</span><span class="sxs-lookup"><span data-stu-id="f22b2-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="f22b2-118">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="f22b2-118">Quote</span></span>

<span data-ttu-id="f22b2-119">Kad projektu saistāt ar piedāvājumu vai kad projektu izveidojat no piedāvājuma, projekta posms tiek iestatīts uz **Piedāvājums** un tiek atjaunināti arī prognozētie sākuma un beigu datumi.</span><span class="sxs-lookup"><span data-stu-id="f22b2-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="f22b2-120">Kamēr projekts ir posmā **Piedāvājums**, lapas **Projekta entītija** cilnē **Pārdošana** tiek rādīta detalizēta informācija par šo piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="f22b2-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="f22b2-121">Plāns</span><span class="sxs-lookup"><span data-stu-id="f22b2-121">Plan</span></span>

<span data-ttu-id="f22b2-122">Kad iegūstat piedāvājumu, kurš ir saistīts ar projektu, un kad šis projekts tiek pārvietots uz fāzi **Līgums**, projekta posms tiek atjaunināts uz **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="f22b2-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="f22b2-123">Kamēr projekts ir posmā **Plāns**, lapā **Projekta entītija** tiek rādīta detalizēta informācija par šo līgumu.</span><span class="sxs-lookup"><span data-stu-id="f22b2-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="f22b2-124">Sniegt</span><span class="sxs-lookup"><span data-stu-id="f22b2-124">Deliver</span></span>

<span data-ttu-id="f22b2-125">Kad projekta plāns ir pabeigts un esat gatavs sākt pašu projektu, projektu vadītājam ir jāatjaunina projekta posms uz **Sniegt**, lai parādītu, ka projekts ir sācies.</span><span class="sxs-lookup"><span data-stu-id="f22b2-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="f22b2-126">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="f22b2-126">Complete</span></span> 

<span data-ttu-id="f22b2-127">Kad darbs pie projekta ir pabeigts, projektu vadītājs var atjaunināt posmu uz **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="f22b2-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="f22b2-128">Atjauninot projekta posmu uz **Pabeigts**, projektu vadītājs norāda, ka darbs ir 100-procentīgi pabeigts, bet projekts tiek paturēts atvērts, lai varētu ierakstīt visus gaidošos laika vai izdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="f22b2-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="f22b2-129">Aizvērt</span><span class="sxs-lookup"><span data-stu-id="f22b2-129">Close</span></span>

<span data-ttu-id="f22b2-130">Kad visas transakcijas projektam ir ierakstītas, projektu vadītājs var atjaunināt posmu uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="f22b2-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="f22b2-131">Šajā brīdī nekādas transakcijas vairs nevar ierakstīt, un projekts ir iestatīts uz tikai lasāmu.</span><span class="sxs-lookup"><span data-stu-id="f22b2-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]