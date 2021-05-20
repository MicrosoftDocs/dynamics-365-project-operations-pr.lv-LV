---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 19, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949148"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="52ac4-103">Project Service Automation atjauninājumu izlaidums 19, V3</span><span class="sxs-lookup"><span data-stu-id="52ac4-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="52ac4-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="52ac4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="52ac4-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="52ac4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="52ac4-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="52ac4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="52ac4-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="52ac4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="52ac4-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="52ac4-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="52ac4-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 19.</span><span class="sxs-lookup"><span data-stu-id="52ac4-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="52ac4-110">Šīs versijas būvējuma numurs ir V3.10.30.41, un tā ir vispārīgi pieejama, izmantojot 2020. gada maija pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="52ac4-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="52ac4-111">Atjauninājumu izlaidums 19</span><span class="sxs-lookup"><span data-stu-id="52ac4-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="52ac4-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="52ac4-112">Bug fixes</span></span>

<span data-ttu-id="52ac4-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="52ac4-113">**Time and Expense**</span></span>

<span data-ttu-id="52ac4-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="52ac4-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="52ac4-115">No laika ierakstu importēšanas atvasinātās kļūdas netiek pareizi apstrādātas.</span><span class="sxs-lookup"><span data-stu-id="52ac4-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="52ac4-116">Laika ierakstu režģis neatbalsta lauka **Tikai datums** darbību.</span><span class="sxs-lookup"><span data-stu-id="52ac4-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="52ac4-117">Projekta resursi projektā nevar izveidot izdevumus.</span><span class="sxs-lookup"><span data-stu-id="52ac4-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="52ac4-118">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="52ac4-118">**Project Management**</span></span>

<span data-ttu-id="52ac4-119">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="52ac4-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="52ac4-120">Otrā līmeņa atvasinātais uzdevums izraisa nepareizu ieguldījuma galīgo izmaksu novērtējumu pabeigšanas (EAC) aprēķināšanā.</span><span class="sxs-lookup"><span data-stu-id="52ac4-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="52ac4-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="52ac4-121">**Sales**</span></span>

<span data-ttu-id="52ac4-122">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="52ac4-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="52ac4-123">Darbība **Pārrēķināšana** nestrādā ar izdevumu līguma rindu detaļām vai piedāvājuma rindu detaļām.</span><span class="sxs-lookup"><span data-stu-id="52ac4-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="52ac4-124">Izdevumu aplēsēm trūkst opcijas **Atjaunināt cenas**.</span><span class="sxs-lookup"><span data-stu-id="52ac4-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="52ac4-125">Klienti nevar atlasīt pielāgotus līguma statusa iemeslus lapā **Projekta līgums**.</span><span class="sxs-lookup"><span data-stu-id="52ac4-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="52ac4-126">Veidojot pielāgotu cenrādi no piedāvājuma, klienti pieredz pasliktinātu darbību.</span><span class="sxs-lookup"><span data-stu-id="52ac4-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="52ac4-127">Klienti pieredz nekonsekvenci, izmantojot noklusējuma **vienību** lapās **Piedāvājumu rindu informācija** un **Līgumu rindu informācija**.</span><span class="sxs-lookup"><span data-stu-id="52ac4-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="52ac4-128">Rēķinā neiekļaujamo darbību kategorijas elementu pievienošana rēķinā iekļaujamā līguma rindai, neievēro darbību kategorijas norēķinu veidu **Rēķinā neiekļaujams**.</span><span class="sxs-lookup"><span data-stu-id="52ac4-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="52ac4-129">Klienti nevar izmantot tikko pievienotās lomas un kategoriju iepriekš izveidotiem līgumiem.</span><span class="sxs-lookup"><span data-stu-id="52ac4-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="52ac4-130">Klienti pieredz pasliktinātu darbību Nevajadzīgi izgūt failā PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="52ac4-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="52ac4-131">Lomas, kas sarakstā **Resursu kategorijas** ir iestatītas kā rēķinā neiekļaujamas, jāpievieno cilnei **Rēķinā iekļaujamās lomas** kā **Rēķinā neiekļaujamās** projekta līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="52ac4-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="52ac4-132">Klient var pieredzēt pasliktinātu darbību, veidojot projektu, jo **GetBookableResourceIdFromUser** izgūst visas rezervējamo resursu kolonnas, nevis tikai primāro ID.</span><span class="sxs-lookup"><span data-stu-id="52ac4-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="52ac4-133">Entītijai **TransactionType** trūkst pirms validācijas atjauninājuma spraudnis, lai neļautu lietotājiem ievadīt **Vienības** un **UnitGroups**, kas transakciju tipiem nav derīgas.</span><span class="sxs-lookup"><span data-stu-id="52ac4-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="52ac4-134">Darbība **Noņemt** laika ieraksta importēšanai nedarbojas.</span><span class="sxs-lookup"><span data-stu-id="52ac4-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]