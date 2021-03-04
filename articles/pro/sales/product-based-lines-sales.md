---
title: Uz produktiem balstītas iespēju rindas — Lite
description: Šajā tēmā ir sniegta informācija par produktu iespēju rindu vienumiem risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764963"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="92818-103">Uz produktiem balstītas iespēju rindas — Lite</span><span class="sxs-lookup"><span data-stu-id="92818-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="92818-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="92818-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="92818-105">Produktu iespēju rindas ir rindu vienumi iespējā.</span><span class="sxs-lookup"><span data-stu-id="92818-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="92818-106">Šie īpašie rindu elementi ir galīgajā rēķinā, kas tiek nodrošināts klientam.</span><span class="sxs-lookup"><span data-stu-id="92818-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="92818-107">Rēķins neietver citus papildu pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="92818-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="92818-108">Saistītie tēriņi un patēriņš netiek izsekoti neviena saistītā projekta uzdevumos.</span><span class="sxs-lookup"><span data-stu-id="92818-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="92818-109">Produkta rindas var būt kataloga vienumi vai ierakstāmie produkti.</span><span class="sxs-lookup"><span data-stu-id="92818-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="92818-110">Lielākajai daļai funckiju iespējas produktu rindās ir tādas pašas kā lietojumprogrammā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="92818-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="92818-111">Papildinformāciju par produktu iespēju rindām skatiet sadaļā [Produktu pievienošana iespējai](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="92818-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="92818-112">**Klienta budžets** ir jēdziens, kas ir raksturīgs projekta iespēju rindām.</span><span class="sxs-lookup"><span data-stu-id="92818-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="92818-113">Lauks **Klienta budžets** izseko summu, kuru klients vēlas maksāt par preci.</span><span class="sxs-lookup"><span data-stu-id="92818-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="92818-114">Ja iespējas kopsavilkuma ieņēmumu metode ir **Sistēmas aprēķināti**, klienta budžeta vērtības visās iespējas rindās tiek apkopotas, lai aprēķinātu prognozējamos ieņēmumus.</span><span class="sxs-lookup"><span data-stu-id="92818-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 

