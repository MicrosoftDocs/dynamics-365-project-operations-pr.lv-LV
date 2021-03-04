---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 25, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143770"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="17e9f-103">Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 25, V3</span><span class="sxs-lookup"><span data-stu-id="17e9f-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="17e9f-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="17e9f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="17e9f-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="17e9f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="17e9f-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="17e9f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="17e9f-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="17e9f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="17e9f-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="17e9f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="17e9f-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājumu izlaidums 25. Šīs versijas būves numurs ir V 3.10.43.76, un tā parasti ir pieejama, izmantojot 2020. gada oktobra pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="17e9f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="17e9f-110">Atjauninājumu izlaidums 25</span><span class="sxs-lookup"><span data-stu-id="17e9f-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="17e9f-111">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="17e9f-111">Bug fixes</span></span>

<span data-ttu-id="17e9f-112">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="17e9f-112">**Time and Expense**</span></span>

<span data-ttu-id="17e9f-113">Ir novērsta šāda problēma:</span><span class="sxs-lookup"><span data-stu-id="17e9f-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="17e9f-114">Laika ievadīšanas diagramma, kurā parādīti papildu dati, pamatojoties uz pārāk lielu intervāla izgūšanu.</span><span class="sxs-lookup"><span data-stu-id="17e9f-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="17e9f-115">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="17e9f-115">**Resource Management**</span></span>

<span data-ttu-id="17e9f-116">Ir novērsta šāda problēma:</span><span class="sxs-lookup"><span data-stu-id="17e9f-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="17e9f-117">Pievienots pakotnes izvietošanas kods, lai izlaistu Universal Resource Scheduling ielāpa importēšanu, ja jau pastāv augstāks versijas ielāps.</span><span class="sxs-lookup"><span data-stu-id="17e9f-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="17e9f-118">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="17e9f-118">**Project Management**</span></span>

<span data-ttu-id="17e9f-119">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="17e9f-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="17e9f-120">Izlabotas noapaļošanas un valūtas kursa neatbilstības, kā rezultātā projekta izsekošanas tīklā ir nepareizi plānotas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17e9f-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="17e9f-121">Atbalstiet iespēju veidlapā **Projekts** parādīt divus vai vairākus reakcijas režģus.</span><span class="sxs-lookup"><span data-stu-id="17e9f-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="17e9f-122">Sniegta validācija, lai risinātu iespēju piešķirt uzdevumu pēc kalendāra beigu datuma, kā rezultātā resursu piešķiršana neizdevās.</span><span class="sxs-lookup"><span data-stu-id="17e9f-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="17e9f-123">Uzlabota kļūdu apstrāde, lai risinātu atsauces Null izņēmumu, kas ģenerēts no tālāk minētajām opcijām:</span><span class="sxs-lookup"><span data-stu-id="17e9f-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="17e9f-124">**PreValidateProjectTeamMemberCreate** spraudnis</span><span class="sxs-lookup"><span data-stu-id="17e9f-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="17e9f-125">**PreValidateProjectTaskCreate**, kad projekta uzdevums ir izveidots bez saistīta projekta</span><span class="sxs-lookup"><span data-stu-id="17e9f-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="17e9f-126">**PreProjectTeamMemberCreate** spraudnis</span><span class="sxs-lookup"><span data-stu-id="17e9f-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="17e9f-127">**PostProjectTeamMemberDelete** spraudnis</span><span class="sxs-lookup"><span data-stu-id="17e9f-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="17e9f-128">**PreValidateProjectTaskDelete** spraudnis</span><span class="sxs-lookup"><span data-stu-id="17e9f-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="17e9f-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="17e9f-129">**Sales**</span></span>

<span data-ttu-id="17e9f-130">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="17e9f-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="17e9f-131">Uzlabota kļūdu apstrāde, lai risinātu atsauces Null izņēmumus, kas ģenerēti no **Projekta kopēšana: aprēķina palīga resursu pārvaldību**.</span><span class="sxs-lookup"><span data-stu-id="17e9f-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="17e9f-132">**Nav gatavs rēķina izveidei** sadaļā **Laika un materiālu rēķinu izrakstīšanas rezerve** nenotīra norēķinu statusu.</span><span class="sxs-lookup"><span data-stu-id="17e9f-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="17e9f-133">Labotas nepareizi nosauktas pogas **Cenas** cilnēs **Lomas cena** un **Kataloga vienumi**.</span><span class="sxs-lookup"><span data-stu-id="17e9f-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
