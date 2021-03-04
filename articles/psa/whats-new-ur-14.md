---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 14, V3
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 14, 3. versijā
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147167"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="6382d-103">Project Service Automation atjauninājumu izlaidums 14, V3</span><span class="sxs-lookup"><span data-stu-id="6382d-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6382d-104">Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="6382d-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="6382d-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="6382d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6382d-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="6382d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6382d-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="6382d-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="6382d-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6382d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6382d-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 14.</span><span class="sxs-lookup"><span data-stu-id="6382d-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="6382d-110">Šai versijai ir kompilācijas numurs V 3.10.4.21, un tas ir pieejams šādā grafikā:</span><span class="sxs-lookup"><span data-stu-id="6382d-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="6382d-111">**Vispārēja pieejamība (pašregulācija):** 2020. gada janvāris</span><span class="sxs-lookup"><span data-stu-id="6382d-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="6382d-112">**Automātiskā atjaunināšana:** 2020. gada februāris</span><span class="sxs-lookup"><span data-stu-id="6382d-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="6382d-113">Atjauninājumu izlaidums 14</span><span class="sxs-lookup"><span data-stu-id="6382d-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="6382d-114">Uzlabojumi</span><span class="sxs-lookup"><span data-stu-id="6382d-114">Enhancements</span></span>

- <span data-ttu-id="6382d-115">Sales</span><span class="sxs-lookup"><span data-stu-id="6382d-115">Sales</span></span>

     - <span data-ttu-id="6382d-116">Pielāgotas lauku vērtības no **Piedāvājuma rindas detalizētā informācija** tiek kopētas **Projekta līgumu rindu detalizētā informācija**, kad piedāvājums tiek **Slēgts kā iegūts**.</span><span class="sxs-lookup"><span data-stu-id="6382d-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="6382d-117">Apstiprinātie projekti var būt **Slēgti kā zaudēti**.</span><span class="sxs-lookup"><span data-stu-id="6382d-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="6382d-118">Resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="6382d-118">Resource Management</span></span>

     - <span data-ttu-id="6382d-119">Pagarinot rezervācijas, lietotājiem tiks piedāvāts apstiprinājuma dialoglodziņš, lai apkopotu rezervācijas rezultātus un nodrošinātu saiti, lai uzturētu rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="6382d-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="6382d-120">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="6382d-120">Bug fixes</span></span>

- <span data-ttu-id="6382d-121">Laiks un izdevumi</span><span class="sxs-lookup"><span data-stu-id="6382d-121">Time and Expense</span></span>

     - <span data-ttu-id="6382d-122">Novērsts: uzlabota lietotāja pieredze kad lietotājs nav atlasījis nevienu ierakstu, kas jālabo.</span><span class="sxs-lookup"><span data-stu-id="6382d-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="6382d-123">Resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="6382d-123">Resource Management</span></span>

     - <span data-ttu-id="6382d-124">Novērsts: resursa vairākkārtēja rezervācija pārsniedz iegrāmatoto resursa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6382d-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="6382d-125">Sales</span><span class="sxs-lookup"><span data-stu-id="6382d-125">Sales</span></span>

     - <span data-ttu-id="6382d-126">Novērsts: kopējā pārdošanas cena netiek aprēķināta, kamēr lietotājs neievada arī izmaksu cenu projekta izdevumu aplēsēm.</span><span class="sxs-lookup"><span data-stu-id="6382d-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="6382d-127">Novērsts: piedāvājuma slēgšana kā **Iegūts** nerodas, ja saistītais projekta līgums nav statusā **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="6382d-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

