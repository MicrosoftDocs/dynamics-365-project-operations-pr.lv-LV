---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 24, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 24, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080396"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="e8f5a-103">Project Service Automation atjauninājumu izlaidums 24, V3</span><span class="sxs-lookup"><span data-stu-id="e8f5a-103">Project Service Automation Update Release 24, V3</span></span>

<span data-ttu-id="e8f5a-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e8f5a-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e8f5a-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e8f5a-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e8f5a-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e8f5a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e8f5a-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 24.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="e8f5a-110">Šīs versijas būvējuma numurs ir V 3.10.42.43, un tas parasti ir pieejams, izmantojot 2020. gada oktobra pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="e8f5a-111">Atjauninājumu izlaidums 24</span><span class="sxs-lookup"><span data-stu-id="e8f5a-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e8f5a-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="e8f5a-112">Bug fixes</span></span>

<span data-ttu-id="e8f5a-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e8f5a-113">**Sales**</span></span>

<span data-ttu-id="e8f5a-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e8f5a-115">Problēma, iestatot produktu noklusējuma cenrādi.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="e8f5a-116">Piedāvājumu iegūšanas veiktspēja ir lēna, iebūvētā cenrāža un lomu cenu ierakstu kopijas dēļ.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="e8f5a-117">Pozīcijas **Projekta līgums / Pārdošanas centrs** > **Produkta rindas elements / Pasūtījuma rindas daudzums** tiek automātiski noapaļotas līdz tuvākajam veselajam skaitlim.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="e8f5a-118">Lasot cenrāžus, paaugstiniet līdz sistēmas privilēģijām.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="e8f5a-119">Kopējiet klienta adreses laukus **address1_freighttermscode** un **address1_shippingmethodcode** uz Piedāvājumu/pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="e8f5a-120">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="e8f5a-120">**Time and Expense**</span></span>

<span data-ttu-id="e8f5a-121">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="e8f5a-122">**Laika ievades režģis** neatbalsta **Tikai datums** laika uzvedību.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="e8f5a-123">Vienums **Laika ievade** netiek automātiski atsvaidzināts.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="e8f5a-124">Ir nepieciešama manuāla atsvaidzināšana.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-124">A manual refresh is required.</span></span>
- <span data-ttu-id="e8f5a-125">Nevar importēt laika ierakstus no piešķīruma, ja resursu piešķīrumos ir pārtraukums (0 stundas).</span><span class="sxs-lookup"><span data-stu-id="e8f5a-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="e8f5a-126">Veidojot laika ierakstu, iestatiet sākumu tādu pašu kā **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="e8f5a-127">Atkārtoti iespējojiet laika ievades lielapjoma rediģēšanu.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="e8f5a-128">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="e8f5a-128">**Resource Management**</span></span>

<span data-ttu-id="e8f5a-129">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="e8f5a-130">Mēģinot atjaunināt sekojošu dienu rezervācijas statusu bez prasības, tiek izmests NullRef izņēmums.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="e8f5a-131">Ielādējot **Saskaņošanas skatu** , radās kļūda.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="e8f5a-132">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="e8f5a-132">**Project Management**</span></span>

<span data-ttu-id="e8f5a-133">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="e8f5a-134">**Projekta grafikā** , mainot no **Manuāli** uz **Automātiski** , netiek veikta automātiska saglabāšana.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-134">In the **Project Schedule** , when changing from **Manual** to **Auto** , auto save is not completing.</span></span>
- <span data-ttu-id="e8f5a-135">Izdevumu izmaksām nevajadzētu tikt aprēķintam novirzes virzienā **Projekta izsekošanas režģī**.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="e8f5a-136">Nekonsekventa uzvedība **Novērtējuma tagu** kolonnu ielādes laikā un mainot **Laika sadalījuma** veidu.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="e8f5a-137">Faktiskās izmaksas projektā var neatspoguļot kopējās izmaksas no **Faktiskajām vērtībām**.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="e8f5a-138">**Novērtētais pabeigšanas datums** cilnē **Kopsavilkums** neatbilst **WBS grafikam**.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="e8f5a-139">**Faktisko stundu atjaunināšana** uz pārkaru atkāpes nedarbojas pareizi.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="e8f5a-140">Projekta vadītājs ārpus saknes **BU** nevar izveidot projektu.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="e8f5a-141">Uzdevuma vai kategorijas izmaiņas **Izdevumu novērtējumos** netiek saglabātas.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="e8f5a-142">**Līguma kopija** kopē rēķinu grafikus un izpildes statusu.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="e8f5a-143">Poga **Atsvaidzināt faktiskās vērtības** nepareizi aprēķina kopsavilkuma uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="e8f5a-144">Microsoft Project pievienojumprogramma: FixNull atsauces kļūda, ja kādam darba grupas dalībniekam ir tukša resursu plānošanas vienība.</span><span class="sxs-lookup"><span data-stu-id="e8f5a-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

