---
title: Projektu veidnes
description: Šajā tēmā ir sniegta informācija par to, kā ātrai projekta iestatīšanai var izmantot projektu veidnes.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123031"
---
# <a name="project-templates"></a><span data-ttu-id="4a63f-103">Projektu veidnes</span><span class="sxs-lookup"><span data-stu-id="4a63f-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4a63f-104">Projekta veidne ir iepriekš definēta struktūra, kas palīdz ātri un ērti uzsākt projektu.</span><span class="sxs-lookup"><span data-stu-id="4a63f-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="4a63f-105">Iepriekš definētu veidni varat izmantot, lai jaunu projektu izveidotu ar vienu klikšķi.</span><span class="sxs-lookup"><span data-stu-id="4a63f-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="4a63f-106">Attiecībā uz projektiem jums ir jādefinē projektu veidņu priekšnosacījumi.</span><span class="sxs-lookup"><span data-stu-id="4a63f-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="4a63f-107">Katrai projekta veidnei jums ir jādefinē projekta kalendārs, un organizācijā ir jābūt iepriekš definētām lomām un cenrāžiem, lai veidnes komponentiem būtu noderīgi dati.</span><span class="sxs-lookup"><span data-stu-id="4a63f-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="4a63f-108">Projekta veidne sastāv no trīs komponentiem: grafika, projekta tāmēm un projekta darba grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="4a63f-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="4a63f-109">Plānot</span><span class="sxs-lookup"><span data-stu-id="4a63f-109">Schedule</span></span>

<span data-ttu-id="4a63f-110">Grafikam projekta veidnē ir tāda pati elementu kopa kā grafikam projektā.</span><span class="sxs-lookup"><span data-stu-id="4a63f-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="4a63f-111">Varat izveidot uzdevumu hierarhiju, saistīt lomas uzdevumiem, noteikt grafika atribūtus un iestatīt atkarības.</span><span class="sxs-lookup"><span data-stu-id="4a63f-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="4a63f-112">Grafiks projekta veidnē atbalsta arī uzdevumu režīmus katram uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="4a63f-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="4a63f-113">Līdz ar to tas atbalsta plānošanas programmu.</span><span class="sxs-lookup"><span data-stu-id="4a63f-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="4a63f-114">Jums ir nepieciešams projektu sasaistīt ar kādu projekta kalendāru.</span><span class="sxs-lookup"><span data-stu-id="4a63f-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="4a63f-115">Kad veidojat darbu grafiku, nav nekādas atšķirības starp projekta veidni un projektu.</span><span class="sxs-lookup"><span data-stu-id="4a63f-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="4a63f-116">Projekta tāmes</span><span class="sxs-lookup"><span data-stu-id="4a63f-116">Project estimates</span></span>

<span data-ttu-id="4a63f-117">Projekta tāmes projekta veidnē darbojas tāpat kā projekta tāmes projektā.</span><span class="sxs-lookup"><span data-stu-id="4a63f-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="4a63f-118">Taču izmaksu un pārdošanas cenas tiek izgūtas no noklusējuma izmaksu un pārdošanas cenrāžiem, kas ir definēti parametros.</span><span class="sxs-lookup"><span data-stu-id="4a63f-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="4a63f-119">Projekta izveidošana no veidnes</span><span class="sxs-lookup"><span data-stu-id="4a63f-119">Creating a project from a template</span></span>
 
<span data-ttu-id="4a63f-120">Projektu var izveidot no projekta veidnes vairākos tālāk norādītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="4a63f-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="4a63f-121">Kad veidojat projektu no piedāvājuma, varat atlasīt projekta veidni dialoglodziņā **Ātrā izveide: Projekts**.</span><span class="sxs-lookup"><span data-stu-id="4a63f-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Dialoglodziņš Ātrā izveide: Projekts](media/project-11.png)

- <span data-ttu-id="4a63f-123">Kad projektu veidojat, atlasot vienumu **Jauns projekts**, pirms ieraksta saglabāšanas tiek parādīta lapa **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="4a63f-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="4a63f-124">Laukā **Izvēlēties veidni** atlasiet vienu no organizācijā esošajām iepriekš definētajām veidnēm.</span><span class="sxs-lookup"><span data-stu-id="4a63f-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="4a63f-125">Izmantojiet vienumu **Izveidot projektu no veidnes** lapā **Veidnes entītija**.</span><span class="sxs-lookup"><span data-stu-id="4a63f-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="4a63f-126">Veidnes komponentu kopēšana uz projektu</span><span class="sxs-lookup"><span data-stu-id="4a63f-126">Copying components of template to project</span></span>

<span data-ttu-id="4a63f-127">Kad projekta veidnes komponentus kopējat uz projektu, atkarībā no projektā izmantotajiem iestatījumiem var rasties dažas pārlabošanas.</span><span class="sxs-lookup"><span data-stu-id="4a63f-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="4a63f-128">Grafika kopēšana</span><span class="sxs-lookup"><span data-stu-id="4a63f-128">Copying the schedule</span></span>

<span data-ttu-id="4a63f-129">Kad grafiku kopējat no projekta veidnes, ja projektam ir citāds projekta kalendārs nekā veidnei, uzdevumu grafikam tiek izmantotas darba stundas no projekta kalendāra.</span><span class="sxs-lookup"><span data-stu-id="4a63f-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="4a63f-130">Šādi grafiks tiek pielāgots atbalstoši pamatā izmantotajam projekta kalendāram.</span><span class="sxs-lookup"><span data-stu-id="4a63f-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="4a63f-131">Līdzīgi arī pirmajam uzdevumam grafikā tiek izmantots projekta sākuma datums, bet pārējās hierarhijas grafiks tiek atjaunināts, pamatojoties uz veidnē norādīto ilgumu un atkarībām.</span><span class="sxs-lookup"><span data-stu-id="4a63f-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="4a63f-132">Projekta tāmju kopēšana</span><span class="sxs-lookup"><span data-stu-id="4a63f-132">Copying project estimates</span></span> 

<span data-ttu-id="4a63f-133">Kad kopēšanu veicat starp projekta tāmju rindām, cenrāži tiek atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="4a63f-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="4a63f-134">Izmaksu cenrādim šie atjauninājumi ir balstīti uz projekta īpašnieka struktūrvienību.</span><span class="sxs-lookup"><span data-stu-id="4a63f-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="4a63f-135">Pārdošanas cenrādim tie ir balstīti uz klientu.</span><span class="sxs-lookup"><span data-stu-id="4a63f-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="4a63f-136">Projektiem, kas ir saistīti ar pārdošanas entītiju, vienības izmaksu un pārdošanas cenas tiek noteiktas, pamatojoties uz šiem cenrāžiem.</span><span class="sxs-lookup"><span data-stu-id="4a63f-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="4a63f-137">Projekta darba grupas kopēšana</span><span class="sxs-lookup"><span data-stu-id="4a63f-137">Copying a project team</span></span>

<span data-ttu-id="4a63f-138">Kad projekta darba grupa tiek kopēta no projekta veidnes uz projektu, tiek kopēti vispārējie resursi kopā ar veidnē definētajām prasmēm un kvalifikācijām.</span><span class="sxs-lookup"><span data-stu-id="4a63f-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="4a63f-139">Arī vispārējo resursu piešķires tiek paturētas tādas, kādas tās bija projekta veidnē.</span><span class="sxs-lookup"><span data-stu-id="4a63f-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="4a63f-140">Nosauktie resursi projektu veidnēs netiek atbalstīti.</span><span class="sxs-lookup"><span data-stu-id="4a63f-140">Named resources aren't supported in project templates.</span></span>
