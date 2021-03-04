---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 28, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150632"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="544cf-103">Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 28, V3</span><span class="sxs-lookup"><span data-stu-id="544cf-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="544cf-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="544cf-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="544cf-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="544cf-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="544cf-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="544cf-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="544cf-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="544cf-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="544cf-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="544cf-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="544cf-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājumu laidiens 28. Šīs versijas būves numurs ir V3.10.46.32, un tā parasti ir pieejama, izmantojot 2021. gada janvāra pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="544cf-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="544cf-110">Atjauninājumu izlaidums 28</span><span class="sxs-lookup"><span data-stu-id="544cf-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="544cf-111">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="544cf-111">Bug fixes</span></span>

<span data-ttu-id="544cf-112">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="544cf-112">**Time and Expense**</span></span>

<span data-ttu-id="544cf-113">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="544cf-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="544cf-114">Lietotāji var izmantot **Lielapjoma rediģēšanu**, lai atjauninātu apstiprinātos un iesūtītos laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="544cf-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="544cf-115">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="544cf-115">**Project Management**</span></span>

<span data-ttu-id="544cf-116">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="544cf-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="544cf-117">Gadījumos, kad uzdevuma GUID interpretē kā numuru, uzdevumus nevar atvērt rediģēšanai, izmantojot **Rediģēt uzdevumu** lentē, kas atrodas lapā **Darba sadalījuma struktūra**.</span><span class="sxs-lookup"><span data-stu-id="544cf-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="544cf-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="544cf-118">**Sales**</span></span>

<span data-ttu-id="544cf-119">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="544cf-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="544cf-120">Kad tiek izsaukts spraudnis **GetEstimatesForProject**, tiek ģenerēts nulles atsauces izņēmums.</span><span class="sxs-lookup"><span data-stu-id="544cf-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="544cf-121">**Atzīmēt gatavu rēķinam** atskaites punkta režģī tikai daļēji atjaunina atribūtus, izņemot atribūtu **InvoiceStatus**, kurš tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="544cf-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

