---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 31, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945544"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="409d6-103">Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 31, V3</span><span class="sxs-lookup"><span data-stu-id="409d6-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="409d6-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="409d6-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="409d6-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="409d6-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="409d6-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="409d6-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="409d6-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="409d6-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="409d6-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="409d6-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="409d6-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 31.</span><span class="sxs-lookup"><span data-stu-id="409d6-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="409d6-110">Šīs versijas būvējuma numurs ir V3.10.52.77, un tā ir vispārīgi pieejama, izmantojot 2021. gada maija pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="409d6-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="409d6-111">Atjauninājumu izlaidums 31</span><span class="sxs-lookup"><span data-stu-id="409d6-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="409d6-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="409d6-112">Bug fixes</span></span>

<span data-ttu-id="409d6-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="409d6-113">**Time and Expense**</span></span>

<span data-ttu-id="409d6-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="409d6-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="409d6-115">Laika ievades vadības komandu pogas lapā **Rezervējams resurss** nebija saprotamas.</span><span class="sxs-lookup"><span data-stu-id="409d6-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="409d6-116">Apstiprinot laika ierakstu, vienumā **Project.SetTrackingFields** tika ģenerēts nulles atsauces izņēmums.</span><span class="sxs-lookup"><span data-stu-id="409d6-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="409d6-117">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="409d6-117">**Resource Management**</span></span>

<span data-ttu-id="409d6-118">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="409d6-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="409d6-119">**Izveidot darba grupas dalībnieku** nepareizi parāda rezervācijas iestatīšanas metadatu iestatījumu vienumam **Noklusējuma rezervācijas iesniegtais statuss**.</span><span class="sxs-lookup"><span data-stu-id="409d6-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="409d6-120">Jauninot no PSA 1.X to 3.X, jaunināšanas process neizdodas posmā **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="409d6-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="409d6-121">**Pārdošana**</span><span class="sxs-lookup"><span data-stu-id="409d6-121">**Sales**</span></span>

<span data-ttu-id="409d6-122">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="409d6-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="409d6-123">Faktisko ieņēmumu summas izsekošanas režģī tiek konvertētas projekta valūtā.</span><span class="sxs-lookup"><span data-stu-id="409d6-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="409d6-124">Nav skaidra valūtas noklusējuma vērtība, izveidojot žurnālu rindas, piedāvājumu rindas un līgumu rindas scenārijos, kuros organizācijas bāzes valūta atšķiras no projekta valūtas.</span><span class="sxs-lookup"><span data-stu-id="409d6-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="409d6-125">Vaicājums **Neapstiprināta labojuma žurnāla validācija** nefiltrē pēc projekta.</span><span class="sxs-lookup"><span data-stu-id="409d6-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="409d6-126">Atlikušais pārdošanas apjoms projektā tiek aprēķināts nepareizi.</span><span class="sxs-lookup"><span data-stu-id="409d6-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="409d6-127">Piedāvājumi, kuru pamatā ir kontaktpersona, neizdodas, kad tie tiek izveidoti bez cenrāža.</span><span class="sxs-lookup"><span data-stu-id="409d6-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="409d6-128">Atlasot **Apstiprināt rēķinu**, vairs netiek rādīts apstrādes skaitītājs.</span><span class="sxs-lookup"><span data-stu-id="409d6-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="409d6-129">Atlasot **Izveidot rēķinu**, vairs netiek rādīts apstrādes skaitītājs.</span><span class="sxs-lookup"><span data-stu-id="409d6-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="409d6-130">Slēdzot piedāvājumu kā zaudētu, netiek atceltas rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="409d6-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







