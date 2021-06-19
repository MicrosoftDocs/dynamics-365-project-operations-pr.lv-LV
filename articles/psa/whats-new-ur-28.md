---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 28, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 28, V3.
author: ruhercul
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010525"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="cc5df-103">Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 28, V3</span><span class="sxs-lookup"><span data-stu-id="cc5df-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cc5df-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="cc5df-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cc5df-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="cc5df-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cc5df-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="cc5df-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cc5df-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="cc5df-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cc5df-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cc5df-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cc5df-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājumu laidiens 28. Šīs versijas būves numurs ir V3.10.46.32, un tā parasti ir pieejama, izmantojot 2021. gada janvāra pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="cc5df-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="cc5df-110">Atjauninājumu izlaidums 28</span><span class="sxs-lookup"><span data-stu-id="cc5df-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cc5df-111">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="cc5df-111">Bug fixes</span></span>

<span data-ttu-id="cc5df-112">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="cc5df-112">**Time and Expense**</span></span>

<span data-ttu-id="cc5df-113">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="cc5df-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc5df-114">Lietotāji var izmantot **Lielapjoma rediģēšanu**, lai atjauninātu apstiprinātos un iesūtītos laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="cc5df-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="cc5df-115">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="cc5df-115">**Project Management**</span></span>

<span data-ttu-id="cc5df-116">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="cc5df-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc5df-117">Gadījumos, kad uzdevuma GUID interpretē kā numuru, uzdevumus nevar atvērt rediģēšanai, izmantojot **Rediģēt uzdevumu** lentē, kas atrodas lapā **Darba sadalījuma struktūra**.</span><span class="sxs-lookup"><span data-stu-id="cc5df-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="cc5df-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cc5df-118">**Sales**</span></span>

<span data-ttu-id="cc5df-119">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="cc5df-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc5df-120">Kad tiek izsaukts spraudnis **GetEstimatesForProject**, tiek ģenerēts nulles atsauces izņēmums.</span><span class="sxs-lookup"><span data-stu-id="cc5df-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="cc5df-121">**Atzīmēt gatavu rēķinam** atskaites punkta režģī tikai daļēji atjaunina atribūtus, izņemot atribūtu **InvoiceStatus**, kurš tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="cc5df-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]