---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 16, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 16, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 1f3bb4442ce1d06807f264003c930dbbee19a5c7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280902"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="a1274-103">Project Service Automation atjauninājumu izlaidums 16, V3</span><span class="sxs-lookup"><span data-stu-id="a1274-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a1274-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="a1274-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a1274-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="a1274-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="a1274-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="a1274-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a1274-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="a1274-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="a1274-108">Lai iegūtu papildinformācijum, skatiet rakstu [Vēlama risinājuma instalēšana un atjaunināšana](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="a1274-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="a1274-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 16.</span><span class="sxs-lookup"><span data-stu-id="a1274-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="a1274-110">Šīs versijas būvējuma numurs ir V3.10.6.34, un tas parasti ir pieejams, izmantojot 2020. gada janvāra pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="a1274-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="a1274-111">Atjauninājumu izlaidums 16</span><span class="sxs-lookup"><span data-stu-id="a1274-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a1274-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="a1274-112">Bug fixes</span></span>

-   <span data-ttu-id="a1274-113">Laiks un izdevumi</span><span class="sxs-lookup"><span data-stu-id="a1274-113">Time and Expense</span></span>

    -   <span data-ttu-id="a1274-114">Izlabots: lietotāji, kuri mēģina iesniegt apstiprināšanai dzēstus laika un izdevumu ierakstus, tagad saņems atbilstošus kļūdu ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="a1274-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="a1274-115">Projekta pārvaldība</span><span class="sxs-lookup"><span data-stu-id="a1274-115">Project Management</span></span>

    -   <span data-ttu-id="a1274-116">Izlabots: darba grupas dalībniekiem veidnēs definētās resursu struktūrvienības tiek ievērotas, un veidnes tiek lietotas jaunajā projektā.</span><span class="sxs-lookup"><span data-stu-id="a1274-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="a1274-117">Izlabots: uzlabots ieraksta īpašumtiesību atkārtotas piešķiršanas process.</span><span class="sxs-lookup"><span data-stu-id="a1274-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="a1274-118">Izlabots: projektus, kas tiek kopēti, nevarēs kopēt, kamēr netiks pabeigtas visas kopēšanas darbības.</span><span class="sxs-lookup"><span data-stu-id="a1274-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="a1274-119">Resursu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="a1274-119">Resource Management</span></span>

    -   <span data-ttu-id="a1274-120">Izlabots: paplašinātā rezervācija tagad pareizi apstrādā īsus periodus un vairs neveido nulles stundas ilgākiem rezervējumiem.</span><span class="sxs-lookup"><span data-stu-id="a1274-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="a1274-121">Izlabots: saskaņošanas skats tagad tiek atveidots, kad projekta laika josla ir +5:30 GMT, bet lietotāja laiks AOne ir atšķirīgs.</span><span class="sxs-lookup"><span data-stu-id="a1274-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="a1274-122">Sales</span><span class="sxs-lookup"><span data-stu-id="a1274-122">Sales</span></span>

    -   <span data-ttu-id="a1274-123">Izlabots: ja tiek noņemts līguma rindā kartētais projekts un tiek kartēts jauns projekts, jaunā projekta faktiskie ieraksti netiek atkārtoti novērtēti, pamatojoties uz līguma rindā definētajām rēķina un cenu kārtulām.</span><span class="sxs-lookup"><span data-stu-id="a1274-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="a1274-124">Šajā izlaidumā tas tika novērsts.</span><span class="sxs-lookup"><span data-stu-id="a1274-124">This has been fixed in this release.</span></span> <span data-ttu-id="a1274-125">Jaunajā kartētajā projektā cenas un faktiskie ieraksti tiks apgriezti un atkārtoti izveidoti, pamatojoties uz līguma rindas cenu un norēķinu kārtulām.</span><span class="sxs-lookup"><span data-stu-id="a1274-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="a1274-126">Nekartētā projekta faktiskie ieraksti arī tiks atkārtoti novērtēti un atkārtoti izveidoti.</span><span class="sxs-lookup"><span data-stu-id="a1274-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="a1274-127">Izlabots: papildu validācija tika pievienota novērtējuma rindas laukam **Summa**, lai nodrošinātu, ka nav iekļautas nulles vērtības.</span><span class="sxs-lookup"><span data-stu-id="a1274-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="a1274-128">Izlabots: ja tika atjaunināti faktiskie projekta vērtības, projekta galvenajā veidlapā tika pievienota poga Atsvaidzināt, lai lietotāji varētu atkārtoti sinhronizēt faktiskās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a1274-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="a1274-129">Izlabots: ja lietotājs jauninās no versijas 2.X uz 3.X, tiks atļauti projekti ar vērtību NULL projekta nosaukumā.</span><span class="sxs-lookup"><span data-stu-id="a1274-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]