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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948658"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="0818a-103">Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 29, V3</span><span class="sxs-lookup"><span data-stu-id="0818a-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0818a-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="0818a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0818a-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="0818a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0818a-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="0818a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0818a-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="0818a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="0818a-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0818a-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0818a-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 29.</span><span class="sxs-lookup"><span data-stu-id="0818a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="0818a-110">Šīs versijas būvējuma numurs ir V3.10.47.7, un tas parasti ir pieejams, izmantojot 2021. gada februāra pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="0818a-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="0818a-111">Atjauninājumu izlaidums 29</span><span class="sxs-lookup"><span data-stu-id="0818a-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0818a-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="0818a-112">Bug fixes</span></span>

<span data-ttu-id="0818a-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="0818a-113">**Time and Expense**</span></span>

<span data-ttu-id="0818a-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="0818a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="0818a-115">Laika ierakstu režģī lietotāji nevar redzēt darba stundas, kas reģistrētas dienās, kuras nav darba dienas.</span><span class="sxs-lookup"><span data-stu-id="0818a-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="0818a-116">Apstiprinātos izdevumu ierakstus var rediģēt režģī.</span><span class="sxs-lookup"><span data-stu-id="0818a-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="0818a-117">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="0818a-117">**Project Management**</span></span>

<span data-ttu-id="0818a-118">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="0818a-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="0818a-119">Trūkst validācijas loģikas, lai nodrošinātu, ka resursu piešķiršanas darba stundas nevar būt negatīvas.</span><span class="sxs-lookup"><span data-stu-id="0818a-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="0818a-120">Pielāgotā darbība **AssignResourcesForTask** atjaunina visus laukus, nevis tikai mainītos laukus.</span><span class="sxs-lookup"><span data-stu-id="0818a-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="0818a-121">Kopējot projektu vidē ar spraudņiem vai darbplūsmām, kas reģistrētas notikumā **CreateProject**, **msdyn_bulkgenerationstatus** atribūta atjaunināšana **CopyWBSToProject** neizdodas.</span><span class="sxs-lookup"><span data-stu-id="0818a-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="0818a-122">Izvēršot projekta kalendāru, darbdienas netiek kārtotas augošā secībā, kas izraisa dažu projekta uzdevumu atjauninājumu kļūmi.</span><span class="sxs-lookup"><span data-stu-id="0818a-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="0818a-123">Mainot projekta vadītāju esošā projektā, tiek aktivizēta organizācijas vienības noklusējuma loģika.</span><span class="sxs-lookup"><span data-stu-id="0818a-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="0818a-124">**Pārdošana**</span><span class="sxs-lookup"><span data-stu-id="0818a-124">**Sales**</span></span>

<span data-ttu-id="0818a-125">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="0818a-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="0818a-126">Lapas **Līgums** cilnes **Līguma izpilde** inicializēšanas laikā neizdodas, ja nav līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="0818a-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>