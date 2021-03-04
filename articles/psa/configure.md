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
ms.openlocfilehash: ec5381f91b1fe5198bd93ac8d6015b1fea38738d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146942"
---
# <a name="configure-project-service"></a><span data-ttu-id="44cd4-103">Project Service konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="44cd4-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="44cd4-104">Pirms [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automatizācijas iespēju izmantošanas pakalpojumā [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] kontu, projektu un resursu pārvaldībai ir jāizpilda dažas konfigurācijas darbības, lai nodrošinātu, ka [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] risinājums atbilst jūsu organizācijas vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="44cd4-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="44cd4-105">Šīs darbības ir aprakstītas tālāk.</span><span class="sxs-lookup"><span data-stu-id="44cd4-105">These steps include:</span></span>  
  
-   <span data-ttu-id="44cd4-106">[Laika vienību iestatīšana](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="44cd4-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="44cd4-107">Konfigurējiet produktu katalogā laika vienības, kuras tiks izmantotas kā plānošanas un rēķinu izrakstīšanas projektu bāze.</span><span class="sxs-lookup"><span data-stu-id="44cd4-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="44cd4-108">[Valūtu un maiņas kursu iestatīšana](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="44cd4-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="44cd4-109">Iestatiet projektos izmantojamās valūtas.</span><span class="sxs-lookup"><span data-stu-id="44cd4-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="44cd4-110">[Struktūrvienību izveide](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="44cd4-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="44cd4-111">Iestatiet grupas, kuras jūsu uzņēmums izmanto biznesa sadalīšanai pēc ģeogrāfiskās atrašanās vietas, biznesa funkcijas vai cita loģiska dalījuma.</span><span class="sxs-lookup"><span data-stu-id="44cd4-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="44cd4-112">[Rēķinu biežumu iestatīšana](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="44cd4-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="44cd4-113">Iestatiet laika periodus, kurus vēlaties izmantot, izrakstot rēķinus jūsu klientiem.</span><span class="sxs-lookup"><span data-stu-id="44cd4-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="44cd4-114">[Transakciju kategoriju konfigurēšana](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="44cd4-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="44cd4-115">Iestatiet transakciju kategorijas, pēc kurām jūsu konsultanti var noteikt apmaksājamu un neapmaksājamu izdevumu apmaksu.</span><span class="sxs-lookup"><span data-stu-id="44cd4-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="44cd4-116">[Izdevumu kategoriju konfigurēšana](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="44cd4-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="44cd4-117">Iestatiet kategorijas, pēc kurām jūsu konsultanti var noteikt apmaksājamu un neapmaksājamu izdevumu apmaksu.</span><span class="sxs-lookup"><span data-stu-id="44cd4-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="44cd4-118">[Preču kataloga vienumu izveide](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="44cd4-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="44cd4-119">Pievienojiet preču katalogam pārdotos produktus, piemēram, programmatūras licences.</span><span class="sxs-lookup"><span data-stu-id="44cd4-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="44cd4-120">[Cenrāža izveide](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="44cd4-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="44cd4-121">Konfigurējiet dažādus cenrāžus atkarībā no tā, cik lielu maksu vēlaties noteikt saviem klientiem par katru viņu projektam nepieciešamo lomu.</span><span class="sxs-lookup"><span data-stu-id="44cd4-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="44cd4-122">[Resursu iestatīšana](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="44cd4-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="44cd4-123">Pievienojiet prasmes, kompetences, resursu lomas un citus resursu datus, kas nepieciešami jūsu projektiem.</span><span class="sxs-lookup"><span data-stu-id="44cd4-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="44cd4-124">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="44cd4-124">See Also</span></span>  
 <span data-ttu-id="44cd4-125">[Pārskats par Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="44cd4-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="44cd4-126">[Project Service Automation konfigurēšana](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="44cd4-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="44cd4-127">[Uzņēmumu pārvaldnieka rokasgrāmata](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="44cd4-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="44cd4-128">[Projekta vadītāja rokasgrāmata](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="44cd4-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="44cd4-129">[Resursu pārvaldnieka rokasgrāmata](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="44cd4-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="44cd4-130">Laika, izmaksu un sadarbības ceļvedis</span><span class="sxs-lookup"><span data-stu-id="44cd4-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
