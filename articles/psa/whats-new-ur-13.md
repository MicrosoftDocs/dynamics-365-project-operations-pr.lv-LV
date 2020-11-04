---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 13, V3
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 13, 3. versijā
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080404"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="793b2-103">Project Service Automation atjauninājumu izlaidums 13, V3</span><span class="sxs-lookup"><span data-stu-id="793b2-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="793b2-104">Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="793b2-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="793b2-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="793b2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="793b2-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="793b2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="793b2-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="793b2-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="793b2-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="793b2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="793b2-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 13.</span><span class="sxs-lookup"><span data-stu-id="793b2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="793b2-110">Šai versijai ir būvējuma numurs V3.10.3.18 , un tas ir pieejams šādā grafikā:</span><span class="sxs-lookup"><span data-stu-id="793b2-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="793b2-111">**Vispārēja pieejamība (pašatjauninājums):** 2019. gada novembris</span><span class="sxs-lookup"><span data-stu-id="793b2-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="793b2-112">**Automātiskais atjauninājums:** 2019. gada decembris</span><span class="sxs-lookup"><span data-stu-id="793b2-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="793b2-113">Atjauninājumu izlaidums 13</span><span class="sxs-lookup"><span data-stu-id="793b2-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="793b2-114">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="793b2-114">Bug fixes</span></span>

- <span data-ttu-id="793b2-115">Laiks un izdevumi</span><span class="sxs-lookup"><span data-stu-id="793b2-115">Time and Expense</span></span>

     - <span data-ttu-id="793b2-116">Novērsts: meklēšanas funkcionalitāte lapā **Izmaksu apstiprinājums** nedarbojas, meklējot pēc izdevumu mērķa.</span><span class="sxs-lookup"><span data-stu-id="793b2-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="793b2-117">Resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="793b2-117">Resource Management</span></span>

     - <span data-ttu-id="793b2-118">Novērsts: skaitļi saskaņošanā ir atjaunināti, lai būtu pareizi pamatoti.</span><span class="sxs-lookup"><span data-stu-id="793b2-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="793b2-119">Novērsts: nosauktos resursus uzdevumiem nevar tikt piešķirti cilnē **Plānot**.</span><span class="sxs-lookup"><span data-stu-id="793b2-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="793b2-120">Projekta pārvaldība</span><span class="sxs-lookup"><span data-stu-id="793b2-120">Project Management</span></span>

     - <span data-ttu-id="793b2-121">Novērsts: nulles atsauces izņēmums, piešķirot darba grupas dalībnieku, kad **TransactionType** trūkst **Vienību** un **DefaultGroup** iestatījuma informācijas.</span><span class="sxs-lookup"><span data-stu-id="793b2-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="793b2-122">Sales</span><span class="sxs-lookup"><span data-stu-id="793b2-122">Sales</span></span>

     - <span data-ttu-id="793b2-123">Novērsts: transakciju tipu ierakstu dublikāts atgriež kļūdu, kad ir izveidoti lomu cenrāža ieraksti.</span><span class="sxs-lookup"><span data-stu-id="793b2-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="793b2-124">Novērsts: papildu pogas **Jaunas iespējas** , **Piedāvājums** , **Pasūtījuma rinda** un **Produkta pievienošana** ir redzamas komandu, piedāvājumu, pasūtījumu produktu un no projekta rindu apakšrežģa komandas.</span><span class="sxs-lookup"><span data-stu-id="793b2-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


