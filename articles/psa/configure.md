---
title: Project Service Automation konfigurēšana
description: Darbības, kas ir jāveic, lai konfigurētu programmu Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129192"
---
# <a name="configure-project-service"></a><span data-ttu-id="5cb13-103">Project Service konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5cb13-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="5cb13-104">Pirms [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automatizācijas iespēju izmantošanas pakalpojumā [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] kontu, projektu un resursu pārvaldībai ir jāizpilda dažas konfigurācijas darbības, lai nodrošinātu, ka [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] risinājums atbilst jūsu organizācijas vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="5cb13-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="5cb13-105">Šīs darbības ir aprakstītas tālāk.</span><span class="sxs-lookup"><span data-stu-id="5cb13-105">These steps include:</span></span>  
  
-   <span data-ttu-id="5cb13-106">[Laika vienību iestatīšana](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="5cb13-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="5cb13-107">Konfigurējiet produktu katalogā laika vienības, kuras tiks izmantotas kā plānošanas un rēķinu izrakstīšanas projektu bāze.</span><span class="sxs-lookup"><span data-stu-id="5cb13-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="5cb13-108">[Valūtu un maiņas kursu iestatīšana](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="5cb13-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="5cb13-109">Iestatiet projektos izmantojamās valūtas.</span><span class="sxs-lookup"><span data-stu-id="5cb13-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="5cb13-110">[Struktūrvienību izveide](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="5cb13-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="5cb13-111">Iestatiet grupas, kuras jūsu uzņēmums izmanto biznesa sadalīšanai pēc ģeogrāfiskās atrašanās vietas, biznesa funkcijas vai cita loģiska dalījuma.</span><span class="sxs-lookup"><span data-stu-id="5cb13-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="5cb13-112">[Rēķinu biežumu iestatīšana](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="5cb13-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="5cb13-113">Iestatiet laika periodus, kurus vēlaties izmantot, izrakstot rēķinus jūsu klientiem.</span><span class="sxs-lookup"><span data-stu-id="5cb13-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="5cb13-114">[Transakciju kategoriju konfigurēšana](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="5cb13-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="5cb13-115">Iestatiet transakciju kategorijas, pēc kurām jūsu konsultanti var noteikt apmaksājamu un neapmaksājamu izdevumu apmaksu.</span><span class="sxs-lookup"><span data-stu-id="5cb13-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="5cb13-116">[Izdevumu kategoriju konfigurēšana](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="5cb13-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="5cb13-117">Iestatiet kategorijas, pēc kurām jūsu konsultanti var noteikt apmaksājamu un neapmaksājamu izdevumu apmaksu.</span><span class="sxs-lookup"><span data-stu-id="5cb13-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="5cb13-118">[Preču kataloga vienumu izveide](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="5cb13-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="5cb13-119">Pievienojiet preču katalogam pārdotos produktus, piemēram, programmatūras licences.</span><span class="sxs-lookup"><span data-stu-id="5cb13-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="5cb13-120">[Cenrāža izveide](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="5cb13-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="5cb13-121">Konfigurējiet dažādus cenrāžus atkarībā no tā, cik lielu maksu vēlaties noteikt saviem klientiem par katru viņu projektam nepieciešamo lomu.</span><span class="sxs-lookup"><span data-stu-id="5cb13-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="5cb13-122">[Resursu iestatīšana](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="5cb13-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="5cb13-123">Pievienojiet prasmes, kompetences, resursu lomas un citus resursu datus, kas nepieciešami jūsu projektiem.</span><span class="sxs-lookup"><span data-stu-id="5cb13-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="5cb13-124">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="5cb13-124">See Also</span></span>  
 <span data-ttu-id="5cb13-125">[Pārskats par Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="5cb13-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="5cb13-126">[Project Service Automation konfigurēšana](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="5cb13-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="5cb13-127">[Uzņēmumu pārvaldnieka rokasgrāmata](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="5cb13-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="5cb13-128">[Projekta vadītāja rokasgrāmata](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="5cb13-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="5cb13-129">[Resursu pārvaldnieka rokasgrāmata](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="5cb13-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="5cb13-130">Laika, izmaksu un sadarbības ceļvedis</span><span class="sxs-lookup"><span data-stu-id="5cb13-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
