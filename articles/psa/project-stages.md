---
title: Projekta posmu tipi
description: Šajā tēmā ir sniegta informācija par projekta posmiem.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: aa423979a794b07a8bd27440f47a29480b74b518
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123071"
---
# <a name="project-stage-types"></a><span data-ttu-id="38327-103">Projekta posmu tipi</span><span class="sxs-lookup"><span data-stu-id="38327-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="38327-104">Projekta posmi ir izstrādāti, lai atspoguļotu projekta statusu tā norises laikā.</span><span class="sxs-lookup"><span data-stu-id="38327-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="38327-105">Pielāgojumus var izmantot, lai automātiski atjauninātu posmus ar biznesa procesa plūsmām, Power Automate vai spraudņu paplašinājumiem.</span><span class="sxs-lookup"><span data-stu-id="38327-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="38327-106">Noklusējuma BPF ir definēti šādi posmi:</span><span class="sxs-lookup"><span data-stu-id="38327-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="38327-107">Jaunas</span><span class="sxs-lookup"><span data-stu-id="38327-107">New</span></span>
- <span data-ttu-id="38327-108">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="38327-108">Quote</span></span>
- <span data-ttu-id="38327-109">Plāns</span><span class="sxs-lookup"><span data-stu-id="38327-109">Plan</span></span>
- <span data-ttu-id="38327-110">Sniegt</span><span class="sxs-lookup"><span data-stu-id="38327-110">Deliver</span></span>
- <span data-ttu-id="38327-111">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="38327-111">Complete</span></span>
- <span data-ttu-id="38327-112">Aizvērt</span><span class="sxs-lookup"><span data-stu-id="38327-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="38327-113">Jauns</span><span class="sxs-lookup"><span data-stu-id="38327-113">New</span></span>

<span data-ttu-id="38327-114">Kad veidojat projektu, šī projekta posms tiek iestatīts uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="38327-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="38327-115">Ja projekts tika izveidots no veidnes, tam var būt grafika, tāmes un darba grupas dati.</span><span class="sxs-lookup"><span data-stu-id="38327-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="38327-116">Pretējā gadījumā tas ir tikai vispārīgas projekta aprises, un atlikušie komponenti ir jāievada.</span><span class="sxs-lookup"><span data-stu-id="38327-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="38327-117">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="38327-117">Quote</span></span>

<span data-ttu-id="38327-118">Kad projektu saistāt ar piedāvājumu vai kad projektu izveidojat no piedāvājuma, projekta posms tiek iestatīts uz **Piedāvājums** un tiek atjaunināti arī prognozētie sākuma un beigu datumi.</span><span class="sxs-lookup"><span data-stu-id="38327-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="38327-119">Kamēr projekts ir posmā **Piedāvājums**, lapas **Projekta entītija** cilnē **Pārdošana** tiek rādīta detalizēta informācija par šo piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="38327-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="38327-120">Plāns</span><span class="sxs-lookup"><span data-stu-id="38327-120">Plan</span></span>

<span data-ttu-id="38327-121">Kad iegūstat piedāvājumu, kurš ir saistīts ar projektu, un kad šis projekts tiek pārvietots uz fāzi **Līgums**, projekta posms tiek atjaunināts uz **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="38327-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="38327-122">Kamēr projekts ir posmā **Plāns**, lapā **Projekta entītija** tiek rādīta detalizēta informācija par šo līgumu.</span><span class="sxs-lookup"><span data-stu-id="38327-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="38327-123">Sniegt</span><span class="sxs-lookup"><span data-stu-id="38327-123">Deliver</span></span>

<span data-ttu-id="38327-124">Kad projekta plāns ir pabeigts un esat gatavs sākt pašu projektu, projektu vadītājam ir jāatjaunina projekta posms uz **Sniegt**, lai parādītu, ka projekts ir sācies.</span><span class="sxs-lookup"><span data-stu-id="38327-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="38327-125">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="38327-125">Complete</span></span> 

<span data-ttu-id="38327-126">Kad darbs pie projekta ir pabeigts, projektu vadītājs var atjaunināt posmu uz **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="38327-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="38327-127">Atjauninot projekta posmu uz **Pabeigts**, projektu vadītājs norāda, ka darbs ir 100-procentīgi pabeigts, bet projekts tiek paturēts atvērts, lai varētu ierakstīt visus gaidošos laika vai izdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="38327-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="38327-128">Aizvērt</span><span class="sxs-lookup"><span data-stu-id="38327-128">Close</span></span>

<span data-ttu-id="38327-129">Kad visas transakcijas projektam ir ierakstītas, projektu vadītājs var atjaunināt posmu uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="38327-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="38327-130">Šajā brīdī nekādas transakcijas vairs nevar ierakstīt, un projekts ir iestatīts uz tikai lasāmu.</span><span class="sxs-lookup"><span data-stu-id="38327-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>