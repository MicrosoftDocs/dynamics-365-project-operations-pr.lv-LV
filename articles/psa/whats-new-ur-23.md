---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 23, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 23, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150047"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="6b9c0-103">Project Service Automation atjauninājumu izlaidums 23, V3</span><span class="sxs-lookup"><span data-stu-id="6b9c0-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6b9c0-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6b9c0-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6b9c0-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6b9c0-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6b9c0-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6b9c0-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6b9c0-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 23.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="6b9c0-110">Šīs versijas būvējuma numurs ir V 3.10.34.30, un tas parasti ir pieejams, izmantojot 2020. gada augusta pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="6b9c0-111">Atjauninājumu izlaidums 23</span><span class="sxs-lookup"><span data-stu-id="6b9c0-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6b9c0-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="6b9c0-112">Bug fixes</span></span>

<span data-ttu-id="6b9c0-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="6b9c0-113">**Time and Expense**</span></span>

<span data-ttu-id="6b9c0-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="6b9c0-115">Lai nodrošinātu jēgpilnu izņēmumu, apstrādājiet maksimālo/minimālo gadījumu ar vienumu **Projekta darba grupas dalībnieka dzēšana**.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="6b9c0-116">Piešķīruma importēšanas rezultāti tukšā noņemšanas ekrānā.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="6b9c0-117">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="6b9c0-117">**Resource Management**</span></span>

<span data-ttu-id="6b9c0-118">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="6b9c0-119">**Resursu lietojuma režģa resursu kartē** tiek parādīti nepareizi dati, ja laika skala pārsniedz piecas dienas.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="6b9c0-120">Kad klienti izveido rezervējamu resursu, spraudnis periodiski automātiski nepievieno resursu Microsoft Office 365 grupai.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="6b9c0-121">**Saskaņošana** skatā **Nedēļas** vai **Mēneša** skatā tiek parādītas nepareizas manuālas kontūras.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="6b9c0-122">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="6b9c0-122">**Project Management**</span></span>

<span data-ttu-id="6b9c0-123">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="6b9c0-124">Pārāk liels entītiju **RetrieveMultiple for usersettings** skaits izraisa pasliktinātu projekta apstiprinājumu un citu operāciju veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="6b9c0-125">**Uzdevumu plānošanas** režģa resursu uzmeklēšana ir ierobežota, parādot tikai piecus darba grupas dalībniekus no projekta darba grupas.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="6b9c0-126">**Uzdevumu plānošanas** režģa resursu uzmeklēšana nefiltrē neaktīvos resursus.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="6b9c0-127">Manuālais režīms nedarbojas kā paredzēts projekta plānošanas darba sadalījuma struktūrā.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="6b9c0-128">**Uzdevumu plānošanas** režģī tiek rādītas **Neaktīvas transakciju kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="6b9c0-129">Režģī **Resursu piešķiršana** tiek veikta nepareiza noapaļošana, kad uzdevumam ir vairāki piešķīrumi.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="6b9c0-130">Viena uzdevuma plānoto izmaksu un faktisko izmaksu noapaļošanas vērtības atšķiras.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="6b9c0-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="6b9c0-131">**Sales**</span></span>

<span data-ttu-id="6b9c0-132">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="6b9c0-133">Veicot dubultklikšķi uz **Visu transakciju kategoriju ienese**, tiek izveidotas vairākas rindas.</span><span class="sxs-lookup"><span data-stu-id="6b9c0-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
