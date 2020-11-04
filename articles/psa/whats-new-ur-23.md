---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 23, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 23, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080391"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="aecf2-103">Project Service Automation atjauninājumu izlaidums 23, V3</span><span class="sxs-lookup"><span data-stu-id="aecf2-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="aecf2-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="aecf2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="aecf2-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="aecf2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="aecf2-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="aecf2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="aecf2-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="aecf2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="aecf2-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="aecf2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="aecf2-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 23.</span><span class="sxs-lookup"><span data-stu-id="aecf2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="aecf2-110">Šīs versijas būvējuma numurs ir V 3.10.34.30, un tas parasti ir pieejams, izmantojot 2020. gada augusta pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="aecf2-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="aecf2-111">Atjauninājumu izlaidums 23</span><span class="sxs-lookup"><span data-stu-id="aecf2-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="aecf2-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="aecf2-112">Bug fixes</span></span>

<span data-ttu-id="aecf2-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="aecf2-113">**Time and Expense**</span></span>

<span data-ttu-id="aecf2-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="aecf2-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="aecf2-115">Lai nodrošinātu jēgpilnu izņēmumu, apstrādājiet maksimālo/minimālo gadījumu ar vienumu **Projekta darba grupas dalībnieka dzēšana**.</span><span class="sxs-lookup"><span data-stu-id="aecf2-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="aecf2-116">Piešķīruma importēšanas rezultāti tukšā noņemšanas ekrānā.</span><span class="sxs-lookup"><span data-stu-id="aecf2-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="aecf2-117">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="aecf2-117">**Resource Management**</span></span>

<span data-ttu-id="aecf2-118">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="aecf2-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="aecf2-119">**Resursu lietojuma režģa resursu kartē** tiek parādīti nepareizi dati, ja laika skala pārsniedz piecas dienas.</span><span class="sxs-lookup"><span data-stu-id="aecf2-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="aecf2-120">Kad klienti izveido rezervējamu resursu, spraudnis periodiski automātiski nepievieno resursu Microsoft Office 365 grupai.</span><span class="sxs-lookup"><span data-stu-id="aecf2-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="aecf2-121">**Saskaņošana** skatā **Nedēļas** vai **Mēneša** skatā tiek parādītas nepareizas manuālas kontūras.</span><span class="sxs-lookup"><span data-stu-id="aecf2-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="aecf2-122">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="aecf2-122">**Project Management**</span></span>

<span data-ttu-id="aecf2-123">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="aecf2-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="aecf2-124">Pārāk liels entītiju **RetrieveMultiple for usersettings** skaits izraisa pasliktinātu projekta apstiprinājumu un citu operāciju veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="aecf2-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="aecf2-125">**Uzdevumu plānošanas** režģa resursu uzmeklēšana ir ierobežota, parādot tikai piecus darba grupas dalībniekus no projekta darba grupas.</span><span class="sxs-lookup"><span data-stu-id="aecf2-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="aecf2-126">**Uzdevumu plānošanas** režģa resursu uzmeklēšana nefiltrē neaktīvos resursus.</span><span class="sxs-lookup"><span data-stu-id="aecf2-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="aecf2-127">Manuālais režīms nedarbojas kā paredzēts projekta plānošanas darba sadalījuma struktūrā.</span><span class="sxs-lookup"><span data-stu-id="aecf2-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="aecf2-128">**Uzdevumu plānošanas** režģī tiek rādītas **Neaktīvas transakciju kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="aecf2-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="aecf2-129">Režģī **Resursu piešķiršana** tiek veikta nepareiza noapaļošana, kad uzdevumam ir vairāki piešķīrumi.</span><span class="sxs-lookup"><span data-stu-id="aecf2-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="aecf2-130">Viena uzdevuma plānoto izmaksu un faktisko izmaksu noapaļošanas vērtības atšķiras.</span><span class="sxs-lookup"><span data-stu-id="aecf2-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="aecf2-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="aecf2-131">**Sales**</span></span>

<span data-ttu-id="aecf2-132">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="aecf2-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="aecf2-133">Veicot dubultklikšķi uz **Visu transakciju kategoriju ienese** , tiek izveidotas vairākas rindas.</span><span class="sxs-lookup"><span data-stu-id="aecf2-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
