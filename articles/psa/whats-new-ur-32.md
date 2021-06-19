---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 32, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129675"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="52870-103">Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 32, V3</span><span class="sxs-lookup"><span data-stu-id="52870-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="52870-104">Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="52870-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="52870-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="52870-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="52870-106">Tas ir saderīgs ar Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="52870-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="52870-107">Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="52870-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="52870-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="52870-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="52870-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 32.</span><span class="sxs-lookup"><span data-stu-id="52870-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="52870-110">Šīs versijas būvējuma numurs ir V3.10.53.108, un tas parasti ir pieejams, izmantojot 2021. gada jūnija pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="52870-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="52870-111">Atjauninājumu izlaidums 32</span><span class="sxs-lookup"><span data-stu-id="52870-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="52870-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="52870-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="52870-113">VispārīgI</span><span class="sxs-lookup"><span data-stu-id="52870-113">General</span></span>

- <span data-ttu-id="52870-114">Ja neizdodas veikt lielu jaunināšanu, ir jābloķē tikai galvenie lietojumprogrammas ieejas punkti, lai nodrošinātu, ka koplietojamās entītijas joprojām ir pieejamas.</span><span class="sxs-lookup"><span data-stu-id="52870-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="52870-115">Laiks un izdevumi</span><span class="sxs-lookup"><span data-stu-id="52870-115">Time and Expense</span></span>

<span data-ttu-id="52870-116">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="52870-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="52870-117">**TimeEntriesImportFromResourceAssignment** nesatur resursu piešķiršanas kontūru sadaļas sākuma un beigu laikus.</span><span class="sxs-lookup"><span data-stu-id="52870-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="52870-118">Atlasot **Atvērt ierakstu** režģī **Laika ieraksts**, var nebūt atļauts atlasīt citas veidlapas.</span><span class="sxs-lookup"><span data-stu-id="52870-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="52870-119">Importējot piešķires laika ierakstos, klienta koda vaicājums var ģenerēt garu URL, kas izraisa vaicājuma kļūmi.</span><span class="sxs-lookup"><span data-stu-id="52870-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="52870-120">Režģī **Laika ieraksts**, dzēšot no šūnas vērtību, fokuss nepaliek režģī.</span><span class="sxs-lookup"><span data-stu-id="52870-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="52870-121">Poga **Noraidīt** ir noņemta no skata **Apstrādē esošie apstiprinājumi** mūsdienīgiem apstiprinājumiem.</span><span class="sxs-lookup"><span data-stu-id="52870-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="52870-122">Laika ierakstu lielapjoma apstiprinājuma stabilitāti un veiktspēju ietekmē savstarpēja bloķēšana, un nespēja atbilstoši apstrādāt pielāgojumus, kas ir saistīti ar entītiju **Laika ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="52870-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="52870-123">Projektu plānošana</span><span class="sxs-lookup"><span data-stu-id="52870-123">Project Planning</span></span>

- <span data-ttu-id="52870-124">Atjauninot projektu, kuram laukā **Līgumslēdzēja vienība** ir vērtība Null, tiek ģenerēts nulles atsauces izņēmums.</span><span class="sxs-lookup"><span data-stu-id="52870-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="52870-125">Funkcija **Atsvaidzināt projekta kopsummas** nepareizi aprēķina projektā atlikušās izmaksas un atlikušos pārdošanas darījumus.</span><span class="sxs-lookup"><span data-stu-id="52870-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="52870-126">Lieki cenu noteikšanas aprēķini ietekmē veiktspēju, kas saistīta ar resursu piešķiršanas kontūru atjauninājumiem.</span><span class="sxs-lookup"><span data-stu-id="52870-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="52870-127">Resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="52870-127">Resource Management</span></span>

<span data-ttu-id="52870-128">Ir novērsta šāda problēma:</span><span class="sxs-lookup"><span data-stu-id="52870-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="52870-129">Ja rezervējama resursa kalendāra noslodze pārsniedz 1, funkcija Project Service Automation nepareizi atpazīst noslodzi kā 0 (nulli).</span><span class="sxs-lookup"><span data-stu-id="52870-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="52870-130">Tāpēc plānošanas skatā rodas bezgalīga cilpa.</span><span class="sxs-lookup"><span data-stu-id="52870-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="52870-131">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="52870-131">Sales</span></span>

<span data-ttu-id="52870-132">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="52870-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="52870-133">Kad tiek izveidota žurnāla rinda, kurā ir pielāgots transakciju tips, rodas šāds nulles atsauces izņēmums: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="52870-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="52870-134">Lomas un kategorijas, kas tiek deaktivizētas pirms piedāvājuma kopēšanas, nedrīkst pievienot tikko nokopētā piedāvājuma rēķinā iekļaujamajām lomām un kategorijām.</span><span class="sxs-lookup"><span data-stu-id="52870-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="52870-135">Dokumenta datums un uzskaites datums nav saskaņoti ar sākuma datumu, kas ir norādīts tieši melnraksta rēķinā izveidotajā rēķina rindas informācijā.</span><span class="sxs-lookup"><span data-stu-id="52870-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="52870-136">Scenārijos, kas ir saistīti ar lomu un kategoriju deaktivizēšanu pirms piedāvājuma kopēšanas, tiek ģenerēti nulles atsauces izņēmumi.</span><span class="sxs-lookup"><span data-stu-id="52870-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="52870-137">Darbība **Atjaunināt cenas** lapā **Projekti** neatjaunina izdevumu aprēķinus un materiālu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="52870-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
