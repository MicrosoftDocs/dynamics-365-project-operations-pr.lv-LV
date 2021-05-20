---
title: Projekta iespēju pārvaldība
description: Šajā tēmā ir sniegta informācija par to, kā strādāt ar iespējām, kas ir saistītas ar projektiem.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948429"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="ffed7-103">Projekta iespēju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="ffed7-103">Manage project-based opportunities</span></span>

<span data-ttu-id="ffed7-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="ffed7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ffed7-105">Uzņēmumiem, kas strādā ar projektiem, piegādes operācijas parasti ir izvērstas vairākās valstīs un ģeogrāfiskajās atrašanās vietās.</span><span class="sxs-lookup"><span data-stu-id="ffed7-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="ffed7-106">Projekta izpildes un piegādes izmaksas var mainīties atkarībā no tā, kāda ģeogrāfiskā vieta vai nodaļa pārvalda piegādi.</span><span class="sxs-lookup"><span data-stu-id="ffed7-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="ffed7-107">Savukārt tas var ietekmēt darījuma uzcenojumu.</span><span class="sxs-lookup"><span data-stu-id="ffed7-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="ffed7-108">Projekta pakalpojumu piegāde parasti ietver daudz cilvēkresursu nodaļas laika, ievērojamas izmaksas par ceļojumiem, materiālu izmaksas un citus izdevumus.</span><span class="sxs-lookup"><span data-stu-id="ffed7-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="ffed7-109">Projekta iespējas programmā ir Dynamics 365 Project Operations izstrādātas ar paplašinājumiem programmai Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="ffed7-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="ffed7-110">Šajā tēmā ir sniegta detalizēta informācija par dažādiem laukiem un biznesa loģiku, kas ir iekļauta papildu funkcionalitātē un kas ir nepieciešama uzņēmumiem, kas strādā projektiem, lai pārvaldītu projektu iespējas.</span><span class="sxs-lookup"><span data-stu-id="ffed7-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="ffed7-111">Visu projekta iespēju skatīšana</span><span class="sxs-lookup"><span data-stu-id="ffed7-111">View all project-based opportunities</span></span>

<span data-ttu-id="ffed7-112">Visu projekta iespēju sarakstu var redzēt lapā **Iespēju saraksts**.</span><span class="sxs-lookup"><span data-stu-id="ffed7-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="ffed7-113">Dodieties uz **Pārdošana** > **Iespējas**.</span><span class="sxs-lookup"><span data-stu-id="ffed7-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="ffed7-114">Izmantojiet **skatu pārslēdzēju**, lai atlasītu citus iespēju filtrētos skatus.</span><span class="sxs-lookup"><span data-stu-id="ffed7-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="ffed7-115">Varat izveidot savus skatus, kuros ir pielāgoti filtrēšanas kritēriji, lai konfigurētu šos skatus un navigācijas opcijas.</span><span class="sxs-lookup"><span data-stu-id="ffed7-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="ffed7-116">Projekta iespējas var tikt izveidotas vai dzēstas šajā saraksta lapā vai detalizētās informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="ffed7-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="ffed7-117">Biznesa procesa plūsma projektu darījumiem</span><span class="sxs-lookup"><span data-stu-id="ffed7-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="ffed7-118">Project Operations projekta darījumiem atbalsta tālāk norādītās biznesa procesu plūsmas.</span><span class="sxs-lookup"><span data-stu-id="ffed7-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="ffed7-119">Interesenta–iespējas biznesa process</span><span class="sxs-lookup"><span data-stu-id="ffed7-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="ffed7-120">Iespējas pārdošanas process</span><span class="sxs-lookup"><span data-stu-id="ffed7-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="ffed7-121">Interesenta–iespējas biznesa process</span><span class="sxs-lookup"><span data-stu-id="ffed7-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="ffed7-122">Interesenta–iespējas biznesa process atbalsta tālāk uzskaitītos posmus.</span><span class="sxs-lookup"><span data-stu-id="ffed7-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="ffed7-123">Posms</span><span class="sxs-lookup"><span data-stu-id="ffed7-123">Stage</span></span> | <span data-ttu-id="ffed7-124">Kartēta entītija</span><span class="sxs-lookup"><span data-stu-id="ffed7-124">Mapped entity</span></span> | <span data-ttu-id="ffed7-125">Funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="ffed7-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ffed7-126">Kvalificēt</span><span class="sxs-lookup"><span data-stu-id="ffed7-126">Qualify</span></span> | <span data-ttu-id="ffed7-127">Interesenti</span><span class="sxs-lookup"><span data-stu-id="ffed7-127">Lead</span></span> | <span data-ttu-id="ffed7-128">Kvalificējiet interesentu, lai izveidotu uzņēmumu, kontaktpersonu un/vai iespēju.</span><span class="sxs-lookup"><span data-stu-id="ffed7-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="ffed7-129">Izstrādāt</span><span class="sxs-lookup"><span data-stu-id="ffed7-129">Develop</span></span> | <span data-ttu-id="ffed7-130">Iespēja</span><span class="sxs-lookup"><span data-stu-id="ffed7-130">Opportunity</span></span> | <span data-ttu-id="ffed7-131">Izstrādājiet iespēju, lai pievienotu papildinformāciju par attiecīgo darbu, galvenajām iesaistītajām personām un konkurenci.</span><span class="sxs-lookup"><span data-stu-id="ffed7-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="ffed7-132">Piedāvāt</span><span class="sxs-lookup"><span data-stu-id="ffed7-132">Propose</span></span> | <span data-ttu-id="ffed7-133">Iespēja</span><span class="sxs-lookup"><span data-stu-id="ffed7-133">Opportunity</span></span> | <span data-ttu-id="ffed7-134">Izstrādājiet priekšlikumu un saņemiet apstiprinājumu no iekšējās pārbaudes darba grupas.</span><span class="sxs-lookup"><span data-stu-id="ffed7-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="ffed7-135">Aizvēršana</span><span class="sxs-lookup"><span data-stu-id="ffed7-135">Close</span></span> | <span data-ttu-id="ffed7-136">Iespēja</span><span class="sxs-lookup"><span data-stu-id="ffed7-136">Opportunity</span></span> | <span data-ttu-id="ffed7-137">Iegūstiet iespēju, lai noslēgtu darījumu.</span><span class="sxs-lookup"><span data-stu-id="ffed7-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="ffed7-138">Iespējas pārdošanas process</span><span class="sxs-lookup"><span data-stu-id="ffed7-138">Opportunity sales process</span></span>
<span data-ttu-id="ffed7-139">Iespējas pārdošanas process risinājumā Project Operations ir iespēju pārdošanas procesa biznesa plūsmas paplašinājums pārdošanas lietojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="ffed7-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="ffed7-140">Šis biznesa process ir izstrādāts, lai atbalstītu tālāk minētos projekta iespējas posmus.</span><span class="sxs-lookup"><span data-stu-id="ffed7-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="ffed7-141">Posms</span><span class="sxs-lookup"><span data-stu-id="ffed7-141">Stage</span></span> | <span data-ttu-id="ffed7-142">Kartēta entītija</span><span class="sxs-lookup"><span data-stu-id="ffed7-142">Mapped entity</span></span> | <span data-ttu-id="ffed7-143">Funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="ffed7-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ffed7-144">Kvalificēt</span><span class="sxs-lookup"><span data-stu-id="ffed7-144">Qualify</span></span> | <span data-ttu-id="ffed7-145">Iespēja</span><span class="sxs-lookup"><span data-stu-id="ffed7-145">Opportunity</span></span> | <span data-ttu-id="ffed7-146">Kvalificējiet interesentu, lai izveidotu uzņēmumu, kontaktpersonu un/vai iespēju.</span><span class="sxs-lookup"><span data-stu-id="ffed7-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="ffed7-147">Piedāvāt</span><span class="sxs-lookup"><span data-stu-id="ffed7-147">Propose</span></span> | <span data-ttu-id="ffed7-148">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="ffed7-148">Quote</span></span> | <span data-ttu-id="ffed7-149">Izstrādājiet priekšlikumu, izmantojot projekta piedāvājumus, un saņemiet apstiprinājumu no iekšējās pārbaudes darba grupas.</span><span class="sxs-lookup"><span data-stu-id="ffed7-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="ffed7-150">Līgums</span><span class="sxs-lookup"><span data-stu-id="ffed7-150">Contract</span></span> | <span data-ttu-id="ffed7-151">Projekta līgums</span><span class="sxs-lookup"><span data-stu-id="ffed7-151">Project Contract</span></span> | <span data-ttu-id="ffed7-152">Iegūstiet piedāvājumu, lai izveidotu līgumu un sāktu projekta izpildi un piegādi.</span><span class="sxs-lookup"><span data-stu-id="ffed7-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="ffed7-153">Aizvēršana</span><span class="sxs-lookup"><span data-stu-id="ffed7-153">Close</span></span> | <span data-ttu-id="ffed7-154">Projekta līgums</span><span class="sxs-lookup"><span data-stu-id="ffed7-154">Project Contract</span></span> | <span data-ttu-id="ffed7-155">Sekmīgi pabeidziet darbu un slēdziet projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="ffed7-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="ffed7-156">Ja jūsu projekta darījums sākās ar interesentu, interesenta–iespējas biznesa process ir prioritārs.</span><span class="sxs-lookup"><span data-stu-id="ffed7-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="ffed7-157">Ja jūsu projekta darījums sākās ar iespēju, iespējas pārdošanas process ir prioritārs.</span><span class="sxs-lookup"><span data-stu-id="ffed7-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="ffed7-158">Varat rediģēt produktu biznesa procesa plūsmu vai izveidot savas biznesa procesa plūsmas, lai izsekotu pārdošanas procesam.</span><span class="sxs-lookup"><span data-stu-id="ffed7-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="ffed7-159">Papildinformāciju par biznesa procesu plūsmu skatiet rakstā [Biznesa procesu plūsmu pārskats](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span><span class="sxs-lookup"><span data-stu-id="ffed7-159">For more information about the business process flow, see [Business process flows overview](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]