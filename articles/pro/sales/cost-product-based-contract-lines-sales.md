---
title: Produktu izmaksu aprēķina līgumu rindas — Lite
description: Šajā tēmā ir sniegta informācija par izveidi
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764468"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="0bf42-103">Produktu izmaksu aprēķina līgumu rindas — Lite</span><span class="sxs-lookup"><span data-stu-id="0bf42-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="0bf42-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="0bf42-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0bf42-105">Produktu līgumu rindas programmā Dynamics 365 Project Operations ietver **Izmaksu** lauku, kurā tiek glabātas produkta izmaksas lejupstraumes ienesīguma aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="0bf42-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="0bf42-106">Kad kataloga produktam tiek izveidota produkta līguma rinda, rindas izmaksu noklusējuma vērtība tiek iegūta no produktu kataloga lauka **Standarta izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="0bf42-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="0bf42-107">Preču kataloga lauks **Standarta izmaksas** tiek iestatīts Organizācijas pamatvalūtā.</span><span class="sxs-lookup"><span data-stu-id="0bf42-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="0bf42-108">Ja tiek atjaunotas vienības izmaksas līguma rindā, tās tiek konvertētas līguma pārdošanas valūtā.</span><span class="sxs-lookup"><span data-stu-id="0bf42-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="0bf42-109">Vienības izmaksas produkta līguma rindā</span><span class="sxs-lookup"><span data-stu-id="0bf42-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="0bf42-110">Vienības izmaksas produkta līguma rindā pieļauj atsevišķas produktu izmaksas katras vienības pārdošanas gadījumam.</span><span class="sxs-lookup"><span data-stu-id="0bf42-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="0bf42-111">Lai gan ne vienmēr nepieciešams, ir dažas situācijas, kurās piegādātājs var piešķirt klientam atlaidi par produkta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="0bf42-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="0bf42-112">Tālāk ir aprakstīts ieteicamais scenārijs.</span><span class="sxs-lookup"><span data-stu-id="0bf42-112">Consider the following scenario:</span></span>

<span data-ttu-id="0bf42-113">Uzņēmums Fabrikam Robotics uzstāda robotu rokas korporācijas Adatum konveijeros.</span><span class="sxs-lookup"><span data-stu-id="0bf42-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="0bf42-114">Fabrikam nodrošina instalēšanas pakalpojumus, bet robotu rokas ir no Trey Research.</span><span class="sxs-lookup"><span data-stu-id="0bf42-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="0bf42-115">Ja robotu roku uzstādīšana korporācijā Adatum paver jaunu nozares vertikāli uzņēmumam Trey Research, uzņēmums varētu šim darījumam piedāvāt īpašu atlaidi uzņēmumam Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="0bf42-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="0bf42-116">Šajā gadījumā Fabrikam izveidot produkta līguma rindu robotu rokām.</span><span class="sxs-lookup"><span data-stu-id="0bf42-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="0bf42-117">Šim līgumam tiek ievadīta vienības cena.</span><span class="sxs-lookup"><span data-stu-id="0bf42-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="0bf42-118">Šī cena atšķiras no Trey Research robotu roku cenas.</span><span class="sxs-lookup"><span data-stu-id="0bf42-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
