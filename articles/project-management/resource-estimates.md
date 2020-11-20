---
title: Resursu aprēķini
description: Šajā tēmā ir sniegta informācija par to, kā programmā Project Operations tiek veikti resursu aprēķini.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127378"
---
# <a name="resource-estimates"></a><span data-ttu-id="98370-103">Resursu aprēķini</span><span class="sxs-lookup"><span data-stu-id="98370-103">Resource estimates</span></span>

<span data-ttu-id="98370-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="98370-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="98370-105">Resursu aprēķini tiek iegūti no laika sadalījuma ieguldījuma, kas tiek definēts darba sadalījuma struktūrā kopā ar piemērojamajām izcenojuma dimensijām.</span><span class="sxs-lookup"><span data-stu-id="98370-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="98370-106">Parasti aprēķins ir **likme/st. par katru komu x stundas.**</span><span class="sxs-lookup"><span data-stu-id="98370-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="98370-107">Katra resursa laika sadalījuma ieguldījums tiek glabāts resursu piešķires ierakstā.</span><span class="sxs-lookup"><span data-stu-id="98370-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="98370-108">Izcenojums tiek glabāts iepriekš definētā cenrādī.</span><span class="sxs-lookup"><span data-stu-id="98370-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="98370-109">Vienību pārvēršana tiek veikta, pamatojoties uz piemērojamo cenrādi.</span><span class="sxs-lookup"><span data-stu-id="98370-109">Unit conversion is applied based on the applicable price list.</span></span>

![Resursu aprēķini](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="98370-111">Noklusējuma izmaksas un izmaksu valūta</span><span class="sxs-lookup"><span data-stu-id="98370-111">Default cost price and cost currency</span></span>

<span data-ttu-id="98370-112">Izmaksas tiek iestatītas uz noklusējumu no organizācijas vienības.</span><span class="sxs-lookup"><span data-stu-id="98370-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="98370-113">Noklusējuma rēķina likme un pārdošanas valūta</span><span class="sxs-lookup"><span data-stu-id="98370-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="98370-114">Pārdošanas cenas tiek lietotas vienreiz katram darījumam.</span><span class="sxs-lookup"><span data-stu-id="98370-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="98370-115">Pārdošanas cenrāža noklusējuma hierarhija ir šāda:</span><span class="sxs-lookup"><span data-stu-id="98370-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="98370-116">Organizācija</span><span class="sxs-lookup"><span data-stu-id="98370-116">Organization</span></span>
2. <span data-ttu-id="98370-117">Klients</span><span class="sxs-lookup"><span data-stu-id="98370-117">Customer</span></span>
3. <span data-ttu-id="98370-118">Piedāvājums/līgums</span><span class="sxs-lookup"><span data-stu-id="98370-118">Quote/contract</span></span>
