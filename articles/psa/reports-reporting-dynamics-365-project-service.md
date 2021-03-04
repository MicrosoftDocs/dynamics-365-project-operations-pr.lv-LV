---
title: Atskaišu veidošanas sākumlapa
description: Šajā tēmā ir sniegta informācija par atskaišu veidošanu programmā Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 25486b0c153842cab4331f27eea4872f848bea50
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147707"
---
# <a name="reporting-home-page"></a><span data-ttu-id="f00a1-103">Atskaišu veidošanas sākumlapa</span><span class="sxs-lookup"><span data-stu-id="f00a1-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f00a1-104">Microsoft Dynamics 365 Project Service Automation ļauj projekta organizācijām efektīvi pārvaldīt savas biznesa operācijas.</span><span class="sxs-lookup"><span data-stu-id="f00a1-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="f00a1-105">Jebkurā projektā darba grupas dalībniekiem ir jāpārvalda iespēja, jāizveido darba piedāvājums un plāns, jānodrošina resursi projektiem, jāpārvalda darbs atbilstoši plānam, jāizraksta rēķins par darbu un pēc tam jādara viss, lai pabeigtu projektu.</span><span class="sxs-lookup"><span data-stu-id="f00a1-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="f00a1-106">Iespēja ziņot par operācijām ir būtiska, lai noteiktu organizācijas veselību un veiktu nepieciešamās korektīvās darbības.</span><span class="sxs-lookup"><span data-stu-id="f00a1-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="f00a1-107">PSA izmanto Microsoft Dynamics 365 atskaišu izveides metodes un tehnoloģijas visu atskaišu izveidei.</span><span class="sxs-lookup"><span data-stu-id="f00a1-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="f00a1-108">Papildinformāciju par atskaišu izveides iespējām skatiet: [Atskaišu rakstīšanas rokasgrāmata, Dynamics 365 Customer Engagement (on-premises)versija 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="f00a1-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="f00a1-109">Atskaites vednis</span><span class="sxs-lookup"><span data-stu-id="f00a1-109">Report Wizard</span></span>

<span data-ttu-id="f00a1-110">Atskaites vednis ļauj lietotājiem, kas nav izstrādātāji, izveidot vienkāršas atskaites.</span><span class="sxs-lookup"><span data-stu-id="f00a1-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="f00a1-111">Tā kā lietojumprogramma ir izveidota uz esošas platformas, lietošanas pieredze ir tāda pati kā pieredze, kas ir dokumentēta sadaļā [Atskaites izveide vai rediģēšana, izmantojot Atskaites vedni](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="f00a1-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="f00a1-112">Taču būs jāizmanto risinājumam Project Service Automation raksturīgās entītijas.</span><span class="sxs-lookup"><span data-stu-id="f00a1-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="f00a1-113">Pielāgotas SQL Server atskaišu izveides pakalpojumu atskaites</span><span class="sxs-lookup"><span data-stu-id="f00a1-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="f00a1-114">Ja uzņēmumam ir nepieciešama noteikta atskaite, ko nevar izveidot, izmantojot Atskaites vedni, varat izveidot pielāgotu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="f00a1-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="f00a1-115">Ir jābūt instalētam pakalpojumam Microsoft Visual Studio kopā ar atbilstošajiem Microsoft SQL Server Data Tools un atskaišu autorēšanas paplašinājumiem.</span><span class="sxs-lookup"><span data-stu-id="f00a1-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="f00a1-116">Papildinformāciju par rīkiem un versijām skatiet sadaļā [Atskaišu izstrādes vide, izmantojot SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="f00a1-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="f00a1-117">Informāciju par to, kā izveidot pielāgotu atskaiti, skatiet sadaļā [Jaunas atskaites izveide, izmantojot SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="f00a1-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="f00a1-118">Power BI ieskatu lietojumprogrammas</span><span class="sxs-lookup"><span data-stu-id="f00a1-118">Power BI insights apps</span></span>

<span data-ttu-id="f00a1-119">Microsoft Power BI un Dynamics 365 kopā nodrošina efektīvu veidu, kā strādāt ar datiem, izmantojot ieskatu programmas.</span><span class="sxs-lookup"><span data-stu-id="f00a1-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="f00a1-120">Informāciju par ieskatu programmu pieejamību skatiet lapā [Power BI ieskatu programmas](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="f00a1-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="f00a1-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f00a1-121">Additional resources</span></span>
<span data-ttu-id="f00a1-122">Papildinformāciju par atskaišu izveidi risinājumā PSA skatiet šādās tēmās:</span><span class="sxs-lookup"><span data-stu-id="f00a1-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="f00a1-123">Darbs ar Project Service datu modeli</span><span class="sxs-lookup"><span data-stu-id="f00a1-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="f00a1-124">Informācijas paneļi</span><span class="sxs-lookup"><span data-stu-id="f00a1-124">Dashboards</span></span>](reports-dashboards.md)

