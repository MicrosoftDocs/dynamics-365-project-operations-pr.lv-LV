---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 13, V3
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 13, 3. versijā
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
ms.openlocfilehash: 7287054c470a44ed1fdc243018ec935fe21a6c4f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147257"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="9e49e-103">Project Service Automation atjauninājumu izlaidums 13, V3</span><span class="sxs-lookup"><span data-stu-id="9e49e-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9e49e-104">Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="9e49e-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="9e49e-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="9e49e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9e49e-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="9e49e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9e49e-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="9e49e-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="9e49e-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9e49e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9e49e-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 13.</span><span class="sxs-lookup"><span data-stu-id="9e49e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="9e49e-110">Šai versijai ir būvējuma numurs V3.10.3.18 , un tas ir pieejams šādā grafikā:</span><span class="sxs-lookup"><span data-stu-id="9e49e-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="9e49e-111">**Vispārēja pieejamība (pašatjauninājums):** 2019. gada novembris</span><span class="sxs-lookup"><span data-stu-id="9e49e-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="9e49e-112">**Automātiskais atjauninājums:** 2019. gada decembris</span><span class="sxs-lookup"><span data-stu-id="9e49e-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="9e49e-113">Atjauninājumu izlaidums 13</span><span class="sxs-lookup"><span data-stu-id="9e49e-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="9e49e-114">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="9e49e-114">Bug fixes</span></span>

- <span data-ttu-id="9e49e-115">Laiks un izdevumi</span><span class="sxs-lookup"><span data-stu-id="9e49e-115">Time and Expense</span></span>

     - <span data-ttu-id="9e49e-116">Novērsts: meklēšanas funkcionalitāte lapā **Izmaksu apstiprinājums** nedarbojas, meklējot pēc izdevumu mērķa.</span><span class="sxs-lookup"><span data-stu-id="9e49e-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="9e49e-117">Resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="9e49e-117">Resource Management</span></span>

     - <span data-ttu-id="9e49e-118">Novērsts: skaitļi saskaņošanā ir atjaunināti, lai būtu pareizi pamatoti.</span><span class="sxs-lookup"><span data-stu-id="9e49e-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="9e49e-119">Novērsts: nosauktos resursus uzdevumiem nevar tikt piešķirti cilnē **Plānot**.</span><span class="sxs-lookup"><span data-stu-id="9e49e-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="9e49e-120">Projekta pārvaldība</span><span class="sxs-lookup"><span data-stu-id="9e49e-120">Project Management</span></span>

     - <span data-ttu-id="9e49e-121">Novērsts: nulles atsauces izņēmums, piešķirot darba grupas dalībnieku, kad **TransactionType** trūkst **Vienību** un **DefaultGroup** iestatījuma informācijas.</span><span class="sxs-lookup"><span data-stu-id="9e49e-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="9e49e-122">Sales</span><span class="sxs-lookup"><span data-stu-id="9e49e-122">Sales</span></span>

     - <span data-ttu-id="9e49e-123">Novērsts: transakciju tipu ierakstu dublikāts atgriež kļūdu, kad ir izveidoti lomu cenrāža ieraksti.</span><span class="sxs-lookup"><span data-stu-id="9e49e-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="9e49e-124">Novērsts: papildu pogas opcijām **Jauna iespēja**, **Piedāvājums**, **Pasūtījuma rinda** un **Pievienot produktu** ir redzamas komandās Iespējām, Piedāvājumiem, Pasūtījuma produktiem un projekta rindu apakšrežģim.</span><span class="sxs-lookup"><span data-stu-id="9e49e-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


