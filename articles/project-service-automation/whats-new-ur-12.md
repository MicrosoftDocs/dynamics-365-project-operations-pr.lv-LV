---
title: Kas jauns Project Service Automation atjauninājuma izlaidumā 12, 3. versijā
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 12, 3. versijā
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753486"
---
# <a name="project-service-automation-v3-update-release-12"></a><span data-ttu-id="def1b-103">Project Service Automation atjauninājuma izlaidums 12, versija 3</span><span class="sxs-lookup"><span data-stu-id="def1b-103">Project Service Automation V3, Update Release 12</span></span>
<span data-ttu-id="def1b-104">Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="def1b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="def1b-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="def1b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="def1b-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="def1b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="def1b-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="def1b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="def1b-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="def1b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="def1b-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 12.</span><span class="sxs-lookup"><span data-stu-id="def1b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="def1b-110">Šai versijai ir būvējuma numurs V3.10.2.34, un tas parasti ir pieejams, izmantojot pašatjauninājumu 2019. gada oktobrī.</span><span class="sxs-lookup"><span data-stu-id="def1b-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="def1b-111">Atjauninājumu izlaidums 12</span><span class="sxs-lookup"><span data-stu-id="def1b-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="def1b-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="def1b-112">Bug fixes</span></span>

- <span data-ttu-id="def1b-113">Laiks un izdevumi</span><span class="sxs-lookup"><span data-stu-id="def1b-113">Time and Expense</span></span>

    - <span data-ttu-id="def1b-114">Novērsts: laika ieraksta kļūdu ziņojumapmaiņa ir atjaunināta ar atbilstošāku kontekstu.</span><span class="sxs-lookup"><span data-stu-id="def1b-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="def1b-115">Novērsts: laika ievadņu režģis un grafiks pareizi parāda vertikālo ritjoslu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="def1b-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="def1b-116">Novērsts: iesniegtus izdevumu un laika ierakstus nevar apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="def1b-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="def1b-117">Novērsts: apstiprinājuma atcelšanas apstiprinājuma dialoglodziņš ir labots, lai atspoguļotu apstiprinājuma statusu, ja tas ir mainīts no **Apstiprināts** uz **Iesniegts**.</span><span class="sxs-lookup"><span data-stu-id="def1b-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="def1b-118">Novērsts **:** Cena **,** vienība un **daudzums** lauki tagad tiek bloķēti izdevumu ierakstā pēc tā apstiprināšanas.</span><span class="sxs-lookup"><span data-stu-id="def1b-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="def1b-119">Projekta pārvaldība</span><span class="sxs-lookup"><span data-stu-id="def1b-119">Project Management</span></span>

    - <span data-ttu-id="def1b-120">Novērsts : **Jauna** darbība **Darba grupas** dalībnieka galvenajā veidlapā ir noņemta.</span><span class="sxs-lookup"><span data-stu-id="def1b-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="def1b-121">Novērsts: resursu piešķires ir atjauninātas uz kontu neprecīzām noapaļošanas kļūdām, kas izraisa uzdevuma beigu datuma maiņu.</span><span class="sxs-lookup"><span data-stu-id="def1b-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="def1b-122">Novērsts: uzdevumu režģī attiecīgās servera puses kļūdas tiks rādītas lietotājam.</span><span class="sxs-lookup"><span data-stu-id="def1b-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="def1b-123">Novērsts: darba grupas dalībnieka vārds tagad atveido uzdevumu lietotāju, nevis amata nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="def1b-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="def1b-124">Resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="def1b-124">Resource Management</span></span>

    - <span data-ttu-id="def1b-125">Novērsts: resursa prasību informācija projektiem, kas izveidoti no veidnes, tagad izmanto projekta kalendāru.</span><span class="sxs-lookup"><span data-stu-id="def1b-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="def1b-126">Novērsts: prasmes un kompetences, kas tagad ir noklusētas no lomu pamatdatiem līdz šai lomai izveidotajām resursu prasībām.</span><span class="sxs-lookup"><span data-stu-id="def1b-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="def1b-127">Sales</span><span class="sxs-lookup"><span data-stu-id="def1b-127">Sales</span></span>

    - <span data-ttu-id="def1b-128">Novērsts: **līguma galvenajā** veidlapā tiek dublēti atrasto objektu ID.</span><span class="sxs-lookup"><span data-stu-id="def1b-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="def1b-129">Novērsts: loģika ir atjaunināta, lai būtu redzama cilne **Piedāvājuma analīze**, lai tā parādītu cilnes metadatu iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="def1b-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="def1b-130">Novērsts: faktiskā ieraksta uzskaites datums tagad ir no laika/izdevumu ieraksta datuma, nevis apstiprinājuma datuma.</span><span class="sxs-lookup"><span data-stu-id="def1b-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
