---
title: Produktu izmaksu aprēķina līgumu rindas — Lite
description: Šajā tēmā ir sniegta informācija par izveidi
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177250"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="d17d0-103">Produktu izmaksu aprēķina līgumu rindas — Lite</span><span class="sxs-lookup"><span data-stu-id="d17d0-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="d17d0-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="d17d0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d17d0-105">Produkta līguma rindas risinājumā Dynamics 365 Project Operations iekļauj lauku **Izmaksas**, kas saglabā produkta izmaksas lejupstraumes ienesīguma aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="d17d0-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="d17d0-106">Ja kataloga precei ir izveidota produkta līguma rinda, produkta līguma rindas izmaksas pēc noklusējuma tiek ņemtas no preču kataloga lauka **Standarta izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="d17d0-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="d17d0-107">Preču kataloga lauks **Standarta izmaksas** tiek iestatīts Organizācijas pamatvalūtā.</span><span class="sxs-lookup"><span data-stu-id="d17d0-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="d17d0-108">Ja tiek atjaunotas vienības izmaksas līguma rindā, tās tiek konvertētas līguma pārdošanas valūtā.</span><span class="sxs-lookup"><span data-stu-id="d17d0-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="d17d0-109">Vienības izmaksas produkta līguma rindā</span><span class="sxs-lookup"><span data-stu-id="d17d0-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="d17d0-110">Vienības izmaksas produkta līguma rindā pieļauj atsevišķas produktu izmaksas katras vienības pārdošanas gadījumam.</span><span class="sxs-lookup"><span data-stu-id="d17d0-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="d17d0-111">Lai gan ne vienmēr nepieciešams, ir dažas situācijas, kurās piegādātājs var piešķirt klientam atlaidi par produkta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="d17d0-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="d17d0-112">Tālāk ir aprakstīts ieteicamais scenārijs.</span><span class="sxs-lookup"><span data-stu-id="d17d0-112">Consider the following scenario:</span></span>

<span data-ttu-id="d17d0-113">Uzņēmums Fabrikam Robotics uzstāda robotu rokas korporācijas Adatum konveijeros.</span><span class="sxs-lookup"><span data-stu-id="d17d0-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="d17d0-114">Uzņēmums Fabrikam nodrošina uzstādīšanas pakalpojumus, taču robotu rokas tiek iegādātas no uzņēmuma Trey Research.</span><span class="sxs-lookup"><span data-stu-id="d17d0-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="d17d0-115">Ja robotu roku uzstādīšana korporācijā Adatum paver jaunu nozares vertikāli uzņēmumam Trey Research, uzņēmums varētu šim darījumam piedāvāt īpašu atlaidi uzņēmumam Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="d17d0-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="d17d0-116">Šajā gadījumā Fabrikam izveido produkta līguma rindu robotu rokām un ievada vienības pašizmaksu šim līgumam, kas atšķiras no Trey Research robota roku standarta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="d17d0-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
