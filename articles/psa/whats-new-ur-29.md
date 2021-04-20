---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 29, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664652"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="e11d2-103">Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 29, V3</span><span class="sxs-lookup"><span data-stu-id="e11d2-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e11d2-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="e11d2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e11d2-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="e11d2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e11d2-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="e11d2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e11d2-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="e11d2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e11d2-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e11d2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e11d2-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 29.</span><span class="sxs-lookup"><span data-stu-id="e11d2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="e11d2-110">Šīs versijas būvējuma numurs ir V3.10.47.7, un tas parasti ir pieejams, izmantojot 2021. gada februāra pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="e11d2-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="e11d2-111">Atjauninājumu izlaidums 29</span><span class="sxs-lookup"><span data-stu-id="e11d2-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e11d2-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="e11d2-112">Bug fixes</span></span>

<span data-ttu-id="e11d2-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="e11d2-113">**Time and Expense**</span></span>

<span data-ttu-id="e11d2-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="e11d2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e11d2-115">Laika ierakstu režģī lietotāji nevar redzēt darba stundas, kas reģistrētas dienās, kuras nav darba dienas.</span><span class="sxs-lookup"><span data-stu-id="e11d2-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="e11d2-116">Apstiprinātos izdevumu ierakstus var rediģēt režģī.</span><span class="sxs-lookup"><span data-stu-id="e11d2-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="e11d2-117">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="e11d2-117">**Project Management**</span></span>

<span data-ttu-id="e11d2-118">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="e11d2-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="e11d2-119">Trūkst validācijas loģikas, lai nodrošinātu, ka resursu piešķiršanas darba stundas nevar būt negatīvas.</span><span class="sxs-lookup"><span data-stu-id="e11d2-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="e11d2-120">Pielāgotā darbība **AssignResourcesForTask** atjaunina visus laukus, nevis tikai mainītos laukus.</span><span class="sxs-lookup"><span data-stu-id="e11d2-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="e11d2-121">Kopējot projektu vidē ar spraudņiem vai darbplūsmām, kas reģistrētas notikumā **CreateProject**, **msdyn_bulkgenerationstatus** atribūta atjaunināšana **CopyWBSToProject** neizdodas.</span><span class="sxs-lookup"><span data-stu-id="e11d2-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="e11d2-122">Izvēršot projekta kalendāru, darbdienas netiek kārtotas augošā secībā, kas izraisa dažu projekta uzdevumu atjauninājumu kļūmi.</span><span class="sxs-lookup"><span data-stu-id="e11d2-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="e11d2-123">Mainot projekta vadītāju esošā projektā, tiek aktivizēta organizācijas vienības noklusējuma loģika.</span><span class="sxs-lookup"><span data-stu-id="e11d2-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="e11d2-124">**Pārdošana**</span><span class="sxs-lookup"><span data-stu-id="e11d2-124">**Sales**</span></span>

<span data-ttu-id="e11d2-125">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="e11d2-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="e11d2-126">Lapas **Līgums** cilnes **Līguma izpilde** inicializēšanas laikā neizdodas, ja nav līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="e11d2-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
