---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643272"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="204da-102">Project Service Automation atjauninājumu izlaidums 26, V3</span><span class="sxs-lookup"><span data-stu-id="204da-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="204da-103">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="204da-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="204da-104">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="204da-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="204da-105">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="204da-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="204da-106">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="204da-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="204da-107">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="204da-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="204da-108">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation, atjauninājuma izlaidumā 26, V3.</span><span class="sxs-lookup"><span data-stu-id="204da-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="204da-109">Šīs versijas būvējuma numurs ir V3.10.44.59, un tā ir pieejama 2020. gada decembra pašatjauninājumā.</span><span class="sxs-lookup"><span data-stu-id="204da-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="204da-110">Atjauninājumu izlaidums 26</span><span class="sxs-lookup"><span data-stu-id="204da-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="204da-111">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="204da-111">Bug fixes</span></span>

<span data-ttu-id="204da-112">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="204da-112">**Time and Expense**</span></span>

<span data-ttu-id="204da-113">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="204da-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="204da-114">Lietotāji var mainīt uzdevumu apstiprinātā/iesniegtā laika ierakstā.</span><span class="sxs-lookup"><span data-stu-id="204da-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="204da-115">Kļūda “Objekta atsauce nav piesaistīta”, saglabājot laika ierakstu.</span><span class="sxs-lookup"><span data-stu-id="204da-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="204da-116">Importējot laika ierakstu no resursu piešķirēm, tiek izveidoti laika ieraksti ar nepareizajām datuma un laika vērtībām.</span><span class="sxs-lookup"><span data-stu-id="204da-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="204da-117">Instalējot programmas Project Service Automation un Field Service, programmas Field Service komandjoslā laika ierakstiem divas reizes tiek parādīta poga **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="204da-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="204da-118">Šūnu atjauninājumi **Atļaut vienību** un **Vienību grupa** tagad darbojas režģī **Izdevumu tāmes**.</span><span class="sxs-lookup"><span data-stu-id="204da-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="204da-119">Veidlapā **Laika ieraksta atjaunināšanas rediģēšana** ir ietverts vienums **Laika skala**.</span><span class="sxs-lookup"><span data-stu-id="204da-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="204da-120">Laiku apstiprināšana ar projektu nesaistītiem laika ierakstiem bloķē sistēmu, meklējot projekta apstiprinātāja lomu.</span><span class="sxs-lookup"><span data-stu-id="204da-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="204da-121">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="204da-121">**Resource Management**</span></span>

<span data-ttu-id="204da-122">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="204da-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="204da-123">Pievienota validācija spraudnī **PostProjectCreate**, lai pirms izveidošanas pārbaudītu primāro prasību.</span><span class="sxs-lookup"><span data-stu-id="204da-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="204da-124">Ātrās izveides veidlapa **Projekta grupas dalībnieks** parāda atsauces izņēmumu Null, ja no veidlapas ir izņemti lauki.</span><span class="sxs-lookup"><span data-stu-id="204da-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="204da-125">Prasību ģenerēšana 12 stundām, kas pārsniedz 1 gadu, būs nesekmīga.</span><span class="sxs-lookup"><span data-stu-id="204da-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="204da-126">Uzlabots kļūdas ziņojums par atsauces izņēmumu Null resursu prasības izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="204da-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="204da-127">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="204da-127">**Project Management**</span></span>

<span data-ttu-id="204da-128">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="204da-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="204da-129">Uzlabota validācija, lai risinātu atsauces izņēmumu Null, kas ģenerēts spraudnī **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="204da-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="204da-130">Projekti, ko publicē Microsoft Project darbvirsmas pievienojumprogramma, dzēš nepiešķirtās piešķires.</span><span class="sxs-lookup"><span data-stu-id="204da-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="204da-131">Pievienota jauna validācija, ja uzdevuma projekta atsauce nav derīga atsauces izņēmuma Null dēļ spraudnī **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="204da-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="204da-132">Team Member režģī nav redzamas atšķirīgas piešķires darba grupas dalībnieka ierakstā.</span><span class="sxs-lookup"><span data-stu-id="204da-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="204da-133">Pievienota jauna validācija un kļūdu ziņojumi atsauces izņēmuma Null dēļ spraudnī **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="204da-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="204da-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="204da-134">**Sales**</span></span>

<span data-ttu-id="204da-135">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="204da-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="204da-136">Atlasot projekta rindu piedāvājumā vai līgumā, pogai **Ieteikums** jābūt redzamai tikai tad, ja tiek atlasīta ar esošu produktu saistīta produkta rinda.</span><span class="sxs-lookup"><span data-stu-id="204da-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="204da-137">Nošķiriet atļauju **Create_Product** no atļaujas **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="204da-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="204da-138">Izdzēšot rēķina rindu, tiek izraisīta **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** atsauces Null kļūme.</span><span class="sxs-lookup"><span data-stu-id="204da-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
