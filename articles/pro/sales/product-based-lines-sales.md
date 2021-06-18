---
title: Uz produktiem balstītas iespēju rindas — Lite
description: Šajā tēmā ir sniegta informācija par produktu iespēju rindu vienumiem risinājumā Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7865da682ae607f017bf59ce1ae1addc9fefa60b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994505"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="72244-103">Uz produktiem balstītas iespēju rindas — Lite</span><span class="sxs-lookup"><span data-stu-id="72244-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="72244-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="72244-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="72244-105">Produktu iespēju rindas ir rindu vienumi iespējā.</span><span class="sxs-lookup"><span data-stu-id="72244-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="72244-106">Šie īpašie rindu elementi ir galīgajā rēķinā, kas tiek nodrošināts klientam.</span><span class="sxs-lookup"><span data-stu-id="72244-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="72244-107">Rēķins neietver citus papildu pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="72244-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="72244-108">Saistītie tēriņi un patēriņš netiek izsekoti neviena saistītā projekta uzdevumos.</span><span class="sxs-lookup"><span data-stu-id="72244-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="72244-109">Produkta rindas var būt kataloga vienumi vai ierakstāmie produkti.</span><span class="sxs-lookup"><span data-stu-id="72244-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="72244-110">Lielākajai daļai funckiju iespējas produktu rindās ir tādas pašas kā lietojumprogrammā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="72244-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="72244-111">Papildinformāciju par produktu iespēju rindām skatiet sadaļā [Produktu pievienošana iespējai](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="72244-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="72244-112">**Klienta budžets** ir jēdziens, kas ir raksturīgs projekta iespēju rindām.</span><span class="sxs-lookup"><span data-stu-id="72244-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="72244-113">Lauks **Klienta budžets** izseko summu, kuru klients vēlas maksāt par preci.</span><span class="sxs-lookup"><span data-stu-id="72244-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="72244-114">Ja iespējas kopsavilkuma ieņēmumu metode ir **Sistēmas aprēķināti**, klienta budžeta vērtības visās iespējas rindās tiek apkopotas, lai aprēķinātu prognozējamos ieņēmumus.</span><span class="sxs-lookup"><span data-stu-id="72244-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]