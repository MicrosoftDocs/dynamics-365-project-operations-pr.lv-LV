---
title: Project Service Automation konfigurēšana
description: Darbības, kas ir jāveic, lai konfigurētu programmu Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753469"
---
# <a name="configure-project-service"></a><span data-ttu-id="85551-103">Project Service konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="85551-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="85551-104">Pirms [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automatizācijas iespēju izmantošanas pakalpojumā [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] kontu, projektu un resursu pārvaldībai ir jāizpilda dažas konfigurācijas darbības, lai nodrošinātu, ka [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] risinājums atbilst jūsu organizācijas vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="85551-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="85551-105">Šīs darbības ir aprakstītas tālāk.</span><span class="sxs-lookup"><span data-stu-id="85551-105">These steps include:</span></span>  
  
-   <span data-ttu-id="85551-106">[Laika vienību iestatīšana](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="85551-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="85551-107">Konfigurējiet produktu katalogā laika vienības, kuras tiks izmantotas kā plānošanas un rēķinu izrakstīšanas projektu bāze.</span><span class="sxs-lookup"><span data-stu-id="85551-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="85551-108">[Valūtu un maiņas kursu iestatīšana](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="85551-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="85551-109">Iestatiet projektos izmantojamās valūtas.</span><span class="sxs-lookup"><span data-stu-id="85551-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="85551-110">[Struktūrvienību izveide](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="85551-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="85551-111">Iestatiet grupas, kuras jūsu uzņēmums izmanto biznesa sadalīšanai pēc ģeogrāfiskās atrašanās vietas, biznesa funkcijas vai cita loģiska dalījuma.</span><span class="sxs-lookup"><span data-stu-id="85551-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="85551-112">[Rēķinu biežumu iestatīšana](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="85551-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="85551-113">Iestatiet laika periodus, kurus vēlaties izmantot, izrakstot rēķinus jūsu klientiem.</span><span class="sxs-lookup"><span data-stu-id="85551-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="85551-114">[Transakciju kategoriju konfigurēšana](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="85551-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="85551-115">Iestatiet transakciju kategorijas, pēc kurām jūsu konsultanti var noteikt apmaksājamu un neapmaksājamu izdevumu apmaksu.</span><span class="sxs-lookup"><span data-stu-id="85551-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="85551-116">[Izdevumu kategoriju konfigurēšana](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="85551-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="85551-117">Iestatiet kategorijas, pēc kurām jūsu konsultanti var noteikt apmaksājamu un neapmaksājamu izdevumu apmaksu.</span><span class="sxs-lookup"><span data-stu-id="85551-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="85551-118">[Preču kataloga vienumu izveide](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="85551-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="85551-119">Pievienojiet preču katalogam pārdotos produktus, piemēram, programmatūras licences.</span><span class="sxs-lookup"><span data-stu-id="85551-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="85551-120">[Cenrāža izveide](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="85551-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="85551-121">Konfigurējiet dažādus cenrāžus atkarībā no tā, cik lielu maksu vēlaties noteikt saviem klientiem par katru viņu projektam nepieciešamo lomu.</span><span class="sxs-lookup"><span data-stu-id="85551-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="85551-122">[Resursu iestatīšana](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="85551-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="85551-123">Pievienojiet prasmes, kompetences, resursu lomas un citus resursu datus, kas nepieciešami jūsu projektiem.</span><span class="sxs-lookup"><span data-stu-id="85551-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="85551-124">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="85551-124">See Also</span></span>  
 <span data-ttu-id="85551-125">[Pārskats par Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="85551-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="85551-126">[Project Service Automation konfigurēšana](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="85551-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="85551-127">[Uzņēmumu pārvaldnieka rokasgrāmata](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="85551-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="85551-128">[Projekta vadītāja rokasgrāmata](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="85551-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="85551-129">[Resursu pārvaldnieka rokasgrāmata](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="85551-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="85551-130">Laika, izmaksu un sadarbības ceļvedis</span><span class="sxs-lookup"><span data-stu-id="85551-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
