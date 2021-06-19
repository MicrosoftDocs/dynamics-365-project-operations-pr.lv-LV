---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 26, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 26, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6aafe66fe8c63dc886455a36e93f32d4a581d5cc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005575"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="19c66-103">Project Service Automation atjauninājumu izlaidums 26, V3</span><span class="sxs-lookup"><span data-stu-id="19c66-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="19c66-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="19c66-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="19c66-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="19c66-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="19c66-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="19c66-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="19c66-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="19c66-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="19c66-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="19c66-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="19c66-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 26, V3.</span><span class="sxs-lookup"><span data-stu-id="19c66-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="19c66-110">Šīs versijas būvējuma numurs ir V3.10.44.59, un tā ir pieejama 2020. gada decembra pašatjauninājumā.</span><span class="sxs-lookup"><span data-stu-id="19c66-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="19c66-111">Atjauninājumu izlaidums 26</span><span class="sxs-lookup"><span data-stu-id="19c66-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="19c66-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="19c66-112">Bug fixes</span></span>

<span data-ttu-id="19c66-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="19c66-113">**Time and Expense**</span></span>

<span data-ttu-id="19c66-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="19c66-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="19c66-115">Lietotāji var mainīt uzdevumu apstiprinātā/iesniegtā laika ierakstā.</span><span class="sxs-lookup"><span data-stu-id="19c66-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="19c66-116">Kļūda “Objekta atsauce nav piesaistīta”, saglabājot laika ierakstu.</span><span class="sxs-lookup"><span data-stu-id="19c66-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="19c66-117">Importējot laika ierakstu no resursu piešķirēm, tiek izveidoti laika ieraksti ar nepareizajām datuma un laika vērtībām.</span><span class="sxs-lookup"><span data-stu-id="19c66-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="19c66-118">Instalējot programmas Project Service Automation un Field Service, programmas Field Service komandjoslā laika ierakstiem divas reizes tiek parādīta poga **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="19c66-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="19c66-119">Šūnu atjauninājumi **Atļaut vienību** un **Vienību grupa** tagad darbojas režģī **Izdevumu tāmes**.</span><span class="sxs-lookup"><span data-stu-id="19c66-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="19c66-120">Veidlapā **Laika ieraksta atjaunināšanas rediģēšana** ir ietverts vienums **Laika skala**.</span><span class="sxs-lookup"><span data-stu-id="19c66-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="19c66-121">Laiku apstiprināšana ar projektu nesaistītiem laika ierakstiem bloķē sistēmu, meklējot projekta apstiprinātāja lomu.</span><span class="sxs-lookup"><span data-stu-id="19c66-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="19c66-122">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="19c66-122">**Resource Management**</span></span>

<span data-ttu-id="19c66-123">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="19c66-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="19c66-124">Pievienota validācija spraudnī **PostProjectCreate**, lai pirms izveidošanas pārbaudītu primāro prasību.</span><span class="sxs-lookup"><span data-stu-id="19c66-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="19c66-125">Ātrās izveides veidlapa **Projekta grupas dalībnieks** parāda atsauces izņēmumu Null, ja no veidlapas ir izņemti lauki.</span><span class="sxs-lookup"><span data-stu-id="19c66-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="19c66-126">Prasību ģenerēšana 12 stundām, kas pārsniedz 1 gadu, būs nesekmīga.</span><span class="sxs-lookup"><span data-stu-id="19c66-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="19c66-127">Uzlabots kļūdas ziņojums par atsauces izņēmumu Null resursu prasības izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="19c66-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="19c66-128">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="19c66-128">**Project Management**</span></span>

<span data-ttu-id="19c66-129">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="19c66-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="19c66-130">Uzlabota validācija, lai risinātu atsauces izņēmumu Null, kas ģenerēts spraudnī **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="19c66-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="19c66-131">Projekti, ko publicē Microsoft Project darbvirsmas pievienojumprogramma, dzēš nepiešķirtās piešķires.</span><span class="sxs-lookup"><span data-stu-id="19c66-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="19c66-132">Pievienota jauna validācija, ja uzdevuma projekta atsauce nav derīga atsauces izņēmuma Null dēļ spraudnī **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="19c66-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="19c66-133">Team Member režģī nav redzamas atšķirīgas piešķires darba grupas dalībnieka ierakstā.</span><span class="sxs-lookup"><span data-stu-id="19c66-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="19c66-134">Pievienota jauna validācija un kļūdu ziņojumi atsauces izņēmuma Null dēļ spraudnī **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="19c66-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="19c66-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="19c66-135">**Sales**</span></span>

<span data-ttu-id="19c66-136">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="19c66-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="19c66-137">Atlasot projekta rindu piedāvājumā vai līgumā, pogai **Ieteikums** jābūt redzamai tikai tad, ja tiek atlasīta ar esošu produktu saistīta produkta rinda.</span><span class="sxs-lookup"><span data-stu-id="19c66-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="19c66-138">Nošķiriet atļauju **Create_Product** no atļaujas **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="19c66-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="19c66-139">Izdzēšot rēķina rindu, tiek izraisīta **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** atsauces Null kļūme.</span><span class="sxs-lookup"><span data-stu-id="19c66-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]