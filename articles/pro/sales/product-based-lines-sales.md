---
title: Uz produktiem balstītas iespēju rindas
description: Šajā tēmā ir sniegta informācija par produktu iespēju rindu vienumiem risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080370"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="63c85-103">Uz produktiem balstītas iespēju rindas</span><span class="sxs-lookup"><span data-stu-id="63c85-103">Product-based opportunity lines</span></span>

<span data-ttu-id="63c85-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="63c85-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="63c85-105">Produktu iespēju rindas ir rindu vienumi iespējā.</span><span class="sxs-lookup"><span data-stu-id="63c85-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="63c85-106">Šīs rindas klientam tiek nodrošinātas kā atsevišķi rindas vienumi eventuālajā rēķinā bez citiem pievienotās vērtības pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="63c85-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="63c85-107">Saistītie tēriņi un patēriņš netiek izsekoti neviena saistītā projekta uzdevumos.</span><span class="sxs-lookup"><span data-stu-id="63c85-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="63c85-108">Produkta rindas var būt kataloga vienumi vai ierakstāmie produkti.</span><span class="sxs-lookup"><span data-stu-id="63c85-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="63c85-109">Lielākajai daļai funckiju iespējas produktu rindās ir tādas pašas kā lietojumprogrammā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="63c85-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="63c85-110">Papildinformāciju par produktu iespēju rindām skatiet sadaļā [Produktu pievienošana iespējai](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="63c85-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="63c85-111">Viena koncepcija saistībā ar produktu iespējas rindām, kas ir specifiska projektu iespējām, ir **Klienta budžets**.</span><span class="sxs-lookup"><span data-stu-id="63c85-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="63c85-112">Izmantojiet šo lauku, lai izsekotu summu, ko klients ir gatavs maksāt par rindas vienumu.</span><span class="sxs-lookup"><span data-stu-id="63c85-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="63c85-113">Ja iespējas kopsavilkuma ieņēmumu metode ir iestatīta kā **Aprēķināja sistēma** , tad klientu budžeta vērtības starp produkta un projekta rindām tiek apkopotas, lai aprēķinātu prognozējamos ieņēmumus.</span><span class="sxs-lookup"><span data-stu-id="63c85-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
