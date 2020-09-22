---
title: Kas jauns Project Service Automation atjauninājuma izlaidumā 13, 3. versijā
description: Šajā tēmā ir sniegta informācija par to, kas jauns Project Service Automation atjauninājuma izlaidumā 13, 3. versijā
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753485"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="80b43-103">Project Service Automation atjauninājuma izlaidums 13, 3. versija</span><span class="sxs-lookup"><span data-stu-id="80b43-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="80b43-104">Mēs priecājamies paziņot par jaunāko programmas Dynamics 365 Project Service Automation (PSA) lietojumprogrammas atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="80b43-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="80b43-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="80b43-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="80b43-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="80b43-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="80b43-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="80b43-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="80b43-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="80b43-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="80b43-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 13.</span><span class="sxs-lookup"><span data-stu-id="80b43-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="80b43-110">Šai versijai ir būvējuma numurs V3.10.3.18 , un tas ir pieejams šādā grafikā:</span><span class="sxs-lookup"><span data-stu-id="80b43-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="80b43-111">**Vispārēja pieejamība (pašatjauninājums):** 2019. gada novembris</span><span class="sxs-lookup"><span data-stu-id="80b43-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="80b43-112">**Automātiskais atjauninājums:** 2019. gada decembris</span><span class="sxs-lookup"><span data-stu-id="80b43-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="80b43-113">Atjauninājumu izlaidums 13</span><span class="sxs-lookup"><span data-stu-id="80b43-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="80b43-114">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="80b43-114">Bug fixes</span></span>

- <span data-ttu-id="80b43-115">Laiks un izdevumi</span><span class="sxs-lookup"><span data-stu-id="80b43-115">Time and Expense</span></span>

     - <span data-ttu-id="80b43-116">Novērsts: meklēšanas funkcionalitāte lapā **Izmaksu apstiprinājums** nedarbojas, meklējot pēc izdevumu mērķa.</span><span class="sxs-lookup"><span data-stu-id="80b43-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="80b43-117">Resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="80b43-117">Resource Management</span></span>

     - <span data-ttu-id="80b43-118">Novērsts: skaitļi saskaņošanā ir atjaunināti, lai būtu pareizi pamatoti.</span><span class="sxs-lookup"><span data-stu-id="80b43-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="80b43-119">Novērsts: nosauktos resursus uzdevumiem nevar tikt piešķirti cilnē **Plānot**.</span><span class="sxs-lookup"><span data-stu-id="80b43-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="80b43-120">Projekta pārvaldība</span><span class="sxs-lookup"><span data-stu-id="80b43-120">Project Management</span></span>

     - <span data-ttu-id="80b43-121">Novērsts: nulles atsauces izņēmums, piešķirot darba grupas dalībnieku, kad **TransactionType** trūkst **Vienību** un **DefaultGroup**iestatījuma informācijas.</span><span class="sxs-lookup"><span data-stu-id="80b43-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="80b43-122">Sales</span><span class="sxs-lookup"><span data-stu-id="80b43-122">Sales</span></span>

     - <span data-ttu-id="80b43-123">Novērsts: transakciju tipu ierakstu dublikāts atgriež kļūdu, kad ir izveidoti lomu cenrāža ieraksti.</span><span class="sxs-lookup"><span data-stu-id="80b43-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="80b43-124">Novērsts: papildu pogas **Jaunas iespējas**, **Piedāvājums**, **Pasūtījuma rinda**un **Produkta pievienošana** ir redzamas komandu, piedāvājumu, pasūtījumu produktu un no projekta rindu apakšrežģa komandas.</span><span class="sxs-lookup"><span data-stu-id="80b43-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


