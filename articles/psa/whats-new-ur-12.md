---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 12, V3
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 12, 3. versijā
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 58a12ded135712d8194499ce4a9ba9e4e2aa99bd
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949508"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="636c9-103">Project Service Automation atjauninājumu izlaidums 12, V3</span><span class="sxs-lookup"><span data-stu-id="636c9-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="636c9-104">Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="636c9-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="636c9-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="636c9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="636c9-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="636c9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="636c9-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="636c9-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="636c9-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="636c9-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="636c9-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 12.</span><span class="sxs-lookup"><span data-stu-id="636c9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="636c9-110">Šai versijai ir būvējuma numurs V3.10.2.34, un tas parasti ir pieejams, izmantojot pašatjauninājumu 2019. gada oktobrī.</span><span class="sxs-lookup"><span data-stu-id="636c9-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="636c9-111">Atjauninājumu izlaidums 12</span><span class="sxs-lookup"><span data-stu-id="636c9-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="636c9-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="636c9-112">Bug fixes</span></span>

- <span data-ttu-id="636c9-113">Laiks un izdevumi</span><span class="sxs-lookup"><span data-stu-id="636c9-113">Time and Expense</span></span>

    - <span data-ttu-id="636c9-114">Novērsts: laika ieraksta kļūdu ziņojumapmaiņa ir atjaunināta ar atbilstošāku kontekstu.</span><span class="sxs-lookup"><span data-stu-id="636c9-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="636c9-115">Novērsts: laika ievadņu režģis un grafiks pareizi parāda vertikālo ritjoslu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="636c9-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="636c9-116">Novērsts: iesniegtus izdevumu un laika ierakstus nevar apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="636c9-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="636c9-117">Novērsts: apstiprinājuma atcelšanas apstiprinājuma dialoglodziņš ir labots, lai atspoguļotu apstiprinājuma statusu, ja tas ir mainīts no **Apstiprināts** uz **Iesniegts**.</span><span class="sxs-lookup"><span data-stu-id="636c9-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="636c9-118">Novērsts **:** Cena **,** vienība un **daudzums** lauki tagad tiek bloķēti izdevumu ierakstā pēc tā apstiprināšanas.</span><span class="sxs-lookup"><span data-stu-id="636c9-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="636c9-119">Projekta pārvaldība</span><span class="sxs-lookup"><span data-stu-id="636c9-119">Project Management</span></span>

    - <span data-ttu-id="636c9-120">Novērsts : **Jauna** darbība **Darba grupas** dalībnieka galvenajā veidlapā ir noņemta.</span><span class="sxs-lookup"><span data-stu-id="636c9-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="636c9-121">Novērsts: resursu piešķires ir atjauninātas uz kontu neprecīzām noapaļošanas kļūdām, kas izraisa uzdevuma beigu datuma maiņu.</span><span class="sxs-lookup"><span data-stu-id="636c9-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="636c9-122">Novērsts: uzdevumu režģī attiecīgās servera puses kļūdas tiks rādītas lietotājam.</span><span class="sxs-lookup"><span data-stu-id="636c9-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="636c9-123">Novērsts: darba grupas dalībnieka vārds tagad atveido uzdevumu lietotāju, nevis amata nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="636c9-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="636c9-124">Resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="636c9-124">Resource Management</span></span>

    - <span data-ttu-id="636c9-125">Novērsts: resursa prasību informācija projektiem, kas izveidoti no veidnes, tagad izmanto projekta kalendāru.</span><span class="sxs-lookup"><span data-stu-id="636c9-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="636c9-126">Novērsts: prasmes un kompetences, kas tagad ir noklusētas no lomu pamatdatiem līdz šai lomai izveidotajām resursu prasībām.</span><span class="sxs-lookup"><span data-stu-id="636c9-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="636c9-127">Sales</span><span class="sxs-lookup"><span data-stu-id="636c9-127">Sales</span></span>

    - <span data-ttu-id="636c9-128">Novērsts: **līguma galvenajā** veidlapā tiek dublēti atrasto objektu ID.</span><span class="sxs-lookup"><span data-stu-id="636c9-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="636c9-129">Novērsts: loģika ir atjaunināta, lai būtu redzama cilne **Piedāvājuma analīze**, lai tā parādītu cilnes metadatu iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="636c9-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="636c9-130">Novērsts: faktiskā ieraksta uzskaites datums tagad ir no laika/izdevumu ieraksta datuma, nevis apstiprinājuma datuma.</span><span class="sxs-lookup"><span data-stu-id="636c9-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]