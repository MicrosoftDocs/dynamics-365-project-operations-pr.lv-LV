---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 18, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 3a6d3ee21ecf742b2253132f3d3cc1cb2b57af75
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119877"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="19d1f-103">Project Service Automation atjauninājumu izlaidums 18, V3</span><span class="sxs-lookup"><span data-stu-id="19d1f-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="19d1f-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="19d1f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="19d1f-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="19d1f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="19d1f-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="19d1f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="19d1f-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="19d1f-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="19d1f-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="19d1f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="19d1f-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 18.</span><span class="sxs-lookup"><span data-stu-id="19d1f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="19d1f-110">Šīs versijas būvējuma numurs ir V 3.10.8.12, un tā ir vispārīgi pieejama, izmantojot 2020. gada aprīļa pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="19d1f-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="19d1f-111">Atjauninājumu izlaidums 18</span><span class="sxs-lookup"><span data-stu-id="19d1f-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="19d1f-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="19d1f-112">Bug fixes</span></span>

<span data-ttu-id="19d1f-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="19d1f-113">**Time and Expense**</span></span>

- <span data-ttu-id="19d1f-114">Izlabots: plūsmās **Atsaukums**, **Pieprasījums** un **Atcelšanas apstiprinājums** rodas izņēmumi ar neskaidriem kļūdu ziņojumiem.</span><span class="sxs-lookup"><span data-stu-id="19d1f-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="19d1f-115">Izlabots: ja **Atcelšanas apstiprinājums** netiek piemērots izdevumiem, netiek parādīta atbilstoša kļūda.</span><span class="sxs-lookup"><span data-stu-id="19d1f-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="19d1f-116">Izlabots: laika ievadnes režģis nepareizi apstrādā brīvdienas Austrālijā pēc ziemas/vasaras laika (DST) maiņas oktobrī.</span><span class="sxs-lookup"><span data-stu-id="19d1f-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="19d1f-117">Izlabots: nepareiza noklusējuma loģika neļauj iesniegt izdevumus.</span><span class="sxs-lookup"><span data-stu-id="19d1f-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="19d1f-118">Izlabots: ja neizdodas laika ieraksta apstiprinājums, apstiprinājums paliek stāvoklī **Gaida**.</span><span class="sxs-lookup"><span data-stu-id="19d1f-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="19d1f-119">Izlabots: SQL kļūdas lielapjoma apstiprinājumos (strupsaķere/taimauts).</span><span class="sxs-lookup"><span data-stu-id="19d1f-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="19d1f-120">Izlabots: būtiskas veiktspējas problēmas lietotāju pieredzē, ko izraisa darba grupu dalībnieku atjaunināšana laika ierakstu apstiprināšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="19d1f-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="19d1f-121">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="19d1f-121">**Project Management**</span></span>

- <span data-ttu-id="19d1f-122">Izlabots: laika zonas paziņojums ir pārvietots no **saskaņošanas** skata uz **projekta** galveno veidlapu.</span><span class="sxs-lookup"><span data-stu-id="19d1f-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="19d1f-123">Izlabots: kalendāra veidne netiek pareizi iestatīta uz noklusējumu, atverot jaunu projekta veidlapu.</span><span class="sxs-lookup"><span data-stu-id="19d1f-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="19d1f-124">Izlabots: uz chromium bāzes izstrādātām pārlūkprogrammām lietotāji nevar viegli atlasīt pirmstecīgos uzdevumus dzēšanai.</span><span class="sxs-lookup"><span data-stu-id="19d1f-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="19d1f-125">Izlabots: projekta izveide vai kopēšana **no tukšas veidnes** ielādē nesaistītus uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="19d1f-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="19d1f-126">Izlabots: noteiktos lietojuprogrammas Edge gadījumos, jauna piešķīruma no uzdevumu režģa izveidošanas laikā tiek izveidoti dublikāta ieraksti.</span><span class="sxs-lookup"><span data-stu-id="19d1f-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="19d1f-127">Izlabots: manuālajā režīmā lietotāji nevar atjaunināt uzdevumu sākuma datumus, lai tie būtu vēlāki par pašreiz saglabātajiem datumiem.</span><span class="sxs-lookup"><span data-stu-id="19d1f-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="19d1f-128">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="19d1f-128">**Resource Management**</span></span>

- <span data-ttu-id="19d1f-129">Izlabots: **saskaņošanas** skata kopsummas rinda nepareizi aprēķina rezervācijas dispersiju pēc rezervācijas pagarināšanas.</span><span class="sxs-lookup"><span data-stu-id="19d1f-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="19d1f-130">Izlabots: **saskaņošanas** skats nepareizi parāda resursu piešķīrumus, ja rezervācijas resursam ir kalendārs, kas neatbilst projekta kalendāram.</span><span class="sxs-lookup"><span data-stu-id="19d1f-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="19d1f-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="19d1f-131">**Sales**</span></span>

- <span data-ttu-id="19d1f-132">Izlabots: ja laika ieraksti tiek atkārtoti apstiprināti (**Apstiprināt > Atcelt >** apstiprināt vēlreiz), tiek izveidots rēķinā neiekļaujams dublikāts.</span><span class="sxs-lookup"><span data-stu-id="19d1f-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>