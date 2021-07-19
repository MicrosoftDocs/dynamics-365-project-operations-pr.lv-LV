---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 33, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334569"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="6961e-103">Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 33, V3</span><span class="sxs-lookup"><span data-stu-id="6961e-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6961e-104">Ar prieku izziņojam jaunāko programmas Microsoft Dynamics 365 Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="6961e-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="6961e-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="6961e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6961e-106">Tas ir saderīgs ar Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6961e-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6961e-107">Lai atjauninātu šo laidienu, apmeklējiet Dynamics 365 tiešsaistes risinājumu lapas administrēšanas centru un instalējiet atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="6961e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="6961e-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6961e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6961e-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 33.</span><span class="sxs-lookup"><span data-stu-id="6961e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="6961e-110">Šai versijai būvējuma numurs ir V3.10.54.98, un tā ir vispārīgi pieejama ar pašatjauninājumu 2021. gada jūlijā.</span><span class="sxs-lookup"><span data-stu-id="6961e-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="6961e-111">Atjauninājumu izlaidums 33</span><span class="sxs-lookup"><span data-stu-id="6961e-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6961e-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="6961e-112">Bug fixes</span></span>

<span data-ttu-id="6961e-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="6961e-113">**Time and Expense**</span></span>

<span data-ttu-id="6961e-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="6961e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="6961e-115">Divi bloķēti lauki, **msdyn_description** un **msdyn_externaldescription** var rediģēt pēc iesniegšanas.</span><span class="sxs-lookup"><span data-stu-id="6961e-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="6961e-116">Kļūdas ziņojums tiek parādīts, izveidojot izmaksas, kas nav saistītas ar projektu.</span><span class="sxs-lookup"><span data-stu-id="6961e-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="6961e-117">Izveidojot laika ierakstu, resursa loma pēc noklusējuma tiek aktivizēta kā neaktīva loma.</span><span class="sxs-lookup"><span data-stu-id="6961e-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="6961e-118">Netiek dzēstas žurnāla rindas, kas saistītas ar atsauktiem un dzēstiem izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="6961e-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="6961e-119">**Laika ieraksta ātrās izveides formā** atjauniniet **Projekta uzdevumu saraksta** skatu, lai mainītu pēc noklusējuma parādīto datumu uz uzdevuma sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="6961e-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="6961e-120">Izveidojot laika ierakstu no rezervējamā resursa cilnes **Saistīts**, pierakstītajam lietotājam, nevis galvenajam rezervējamam resursam laika ieraksts tiek izveidots nepareizi.</span><span class="sxs-lookup"><span data-stu-id="6961e-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="6961e-121">Jauni lauki tiek pievienoti dialoglodziņam **Lielapjoma apstiprinājuma MDD**.</span><span class="sxs-lookup"><span data-stu-id="6961e-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="6961e-122">**Projektu plānošana**</span><span class="sxs-lookup"><span data-stu-id="6961e-122">**Project planning**</span></span>

<span data-ttu-id="6961e-123">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="6961e-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="6961e-124">Lēna projekta izveides veiktspēja, lietojot projekta darba stundu veidnes sarežģītos kalendāros.</span><span class="sxs-lookup"><span data-stu-id="6961e-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="6961e-125">Ja sākuma datums ir lielāks par beigu datumu, kopēšanas projekta veidnē tiek rādīta kļūda, jo katra lauka laika komponents atšķiras.</span><span class="sxs-lookup"><span data-stu-id="6961e-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="6961e-126">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="6961e-126">**Resource management**</span></span>

<span data-ttu-id="6961e-127">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="6961e-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="6961e-128">Resursu lietojuma vaicājumā tiek izmantots nepareizs parametrs, bet XML rada nepareizus filtrēšanas rezultātus **Resursu lietojuma** režģī.</span><span class="sxs-lookup"><span data-stu-id="6961e-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="6961e-129">Apstiprinājums **Rezervāciju pagarināšana** parāda nepareizu rezervāciju beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="6961e-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="6961e-130">**Pārdošana**</span><span class="sxs-lookup"><span data-stu-id="6961e-130">**Sales**</span></span>

<span data-ttu-id="6961e-131">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="6961e-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="6961e-132">Rodas kļūdas ziņojums, ja kategorijas cena tiek izveidota ar trūkstošām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="6961e-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="6961e-133">Rodas kļūdas ziņojums, ja līguma rindas atskaites punkts tiek izveidots bez pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="6961e-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
