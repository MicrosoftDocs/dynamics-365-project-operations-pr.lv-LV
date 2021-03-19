---
title: Paplašinātā piedāvājumu sniegšana, izcenojums un rēķinu izrakstīšana
description: Šajā tēmā ir sniegta informācija par piedāvājumu sniegšanu, rēķinu izrakstīšanu un izcenojumu programmā Project Service Automation.
author: kfend
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 2/14/2019
ms.topic: article
ms.author: kfend
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c4674aba1d152289c78a202f9da1f710e28f9960
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275232"
---
# <a name="advanced-quoting-pricing-and-billing-guide"></a><span data-ttu-id="6d02b-103">Paplašinātā piedāvājumu sniegšanas, cenu noteikšanas un rēķinu izrakstīšanas rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="6d02b-103">Advanced quoting, pricing, and billing guide</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6d02b-104">Spēja atrast pareizos resursus īstajā laikā, rezervēt šos resursus projektiem, kā arī uzturēt resursu izmantojumu palīdz organizācijām sasniegt ieņēmumu un klientu apmierinātības mērķus.</span><span class="sxs-lookup"><span data-stu-id="6d02b-104">The ability to find the right resources at the right time, book those resources on projects, and keep resources utilized helps organizations meet revenue targets and customer satisfaction goals.</span></span> 

<span data-ttu-id="6d02b-105">PDF saite, kas iepriekš bija šajā tēmā, ir noņemta, un saturs ir pārvietots uz tālāk norādītajām tēmām.</span><span class="sxs-lookup"><span data-stu-id="6d02b-105">The PDF link that was previously in this topic has been removed and the content has been moved to the following topics:</span></span>

- [<span data-ttu-id="6d02b-106">Piedāvājumu sniegšana, izcenojums un rēķinu izrakstīšana</span><span class="sxs-lookup"><span data-stu-id="6d02b-106">Quoting, pricing, and billing</span></span>](../quote-bill-price.md)
- [<span data-ttu-id="6d02b-107">Pārdošanas procesi</span><span class="sxs-lookup"><span data-stu-id="6d02b-107">Sales processes</span></span>](../basic-sales-process.md)
- [<span data-ttu-id="6d02b-108">Piedāvājumi un piedāvājumu rindas</span><span class="sxs-lookup"><span data-stu-id="6d02b-108">Quotes and quote lines</span></span>](../basic-quote-lines.md)
- [<span data-ttu-id="6d02b-109">Uz preci balstītas piedāvājumu rindas</span><span class="sxs-lookup"><span data-stu-id="6d02b-109">Product-based quote lines</span></span>](../product-based-quote-lines.md)
- [<span data-ttu-id="6d02b-110">Cenas noteikšana</span><span class="sxs-lookup"><span data-stu-id="6d02b-110">Pricing</span></span>](../basic-pricing.md)
- [<span data-ttu-id="6d02b-111">Preču kataloga cenas</span><span class="sxs-lookup"><span data-stu-id="6d02b-111">Product catalog pricing</span></span>](../product-catalog-pricing.md)
- [<span data-ttu-id="6d02b-112">Biznesa transakcijas</span><span class="sxs-lookup"><span data-stu-id="6d02b-112">Business transactions</span></span>](../basic-business-transactions.md)
- [<span data-ttu-id="6d02b-113">Novērtējumi</span><span class="sxs-lookup"><span data-stu-id="6d02b-113">Estimates</span></span>](../estimates.md)
- [<span data-ttu-id="6d02b-114">Faktiski</span><span class="sxs-lookup"><span data-stu-id="6d02b-114">Actuals</span></span>](../actuals.md)
- [<span data-ttu-id="6d02b-115">Projektu piedāvājumu analizēšana</span><span class="sxs-lookup"><span data-stu-id="6d02b-115">Analyzing project quotes</span></span>](../basic-analyzing-quotes.md)
- [<span data-ttu-id="6d02b-116">Organizācijas struktūrvienības</span><span class="sxs-lookup"><span data-stu-id="6d02b-116">Organizational units</span></span>](../advanced-organizational.md)
- [<span data-ttu-id="6d02b-117">Vienību grupas un vienības</span><span class="sxs-lookup"><span data-stu-id="6d02b-117">Unit groups and units</span></span>](../advanced-units.md)
- [<span data-ttu-id="6d02b-118">Vairāku valūtu scenāriji</span><span class="sxs-lookup"><span data-stu-id="6d02b-118">Multi-currency scenarios</span></span>](../advanced-currency.md)
- [<span data-ttu-id="6d02b-119">Faktisko datu ierakstīšana</span><span class="sxs-lookup"><span data-stu-id="6d02b-119">Recording actuals</span></span>](../advanced-actuals.md)

> [!NOTE]
> <span data-ttu-id="6d02b-120">Šī tēma tiks noņemta turpmākā dokumentācijas atjauninājumā.</span><span class="sxs-lookup"><span data-stu-id="6d02b-120">This topic will be removed in a future documentation update.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]