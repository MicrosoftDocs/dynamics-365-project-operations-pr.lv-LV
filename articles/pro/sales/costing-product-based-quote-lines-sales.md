---
title: Cenu noteikšanas produktu piedāvājuma rindas
description: Šajā tēmā ir sniegta informācija par izmaksu piemērošanu produktu piedāvājumu rindai.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080347"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="b3360-103">Cenu noteikšanas produktu piedāvājuma rindas</span><span class="sxs-lookup"><span data-stu-id="b3360-103">Costing product-based quote lines</span></span>

<span data-ttu-id="b3360-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="b3360-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b3360-105">Produktu piedāvājuma rindām risinājumā Dynamics 365 Project Operations ir arī lauks **Izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="b3360-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="b3360-106">Šo lauku izmanto, lai sekotu produkta izmaksām piedāvājuma rindā un lejupstraumes ienesīguma aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="b3360-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="b3360-107">Ja kataloga precei ir izveidota produkta piedāvājuma rinda, produkta piedāvājuma rindas izmaksas pēc noklusējuma tiek ņemta no preču kataloga lauka **Standarta izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="b3360-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="b3360-108">Preču kataloga lauks Standarta izmaksas tiek iestatīts Organizācijas pamatvalūtā.</span><span class="sxs-lookup"><span data-stu-id="b3360-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="b3360-109">Produkta piedāvājuma rindas noklusējuma vienības izmaksas piedāvājumā tiek konvertētas pārdošanas valūtā.</span><span class="sxs-lookup"><span data-stu-id="b3360-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="b3360-110">Vienības izmaksas produktu piedāvājuma rindā</span><span class="sxs-lookup"><span data-stu-id="b3360-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="b3360-111">Produkta piedāvājuma rindas vienības izmaksu mērķis ir tas, lai katrā pārdošanas reizē precei var būt dažādas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="b3360-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="b3360-112">Šis nav tipisks scenārijs, taču reizēm piegādātājs var piemērot preces izmaksu atlaidi atkarībā no galīgās pārdošanas klienta.</span><span class="sxs-lookup"><span data-stu-id="b3360-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="b3360-113">Piemērs.</span><span class="sxs-lookup"><span data-stu-id="b3360-113">For example:</span></span>

<span data-ttu-id="b3360-114">Uzņēmums Fabrikam Robotics uzstāda robotu rokas korporācijas Adatum konveijeros.</span><span class="sxs-lookup"><span data-stu-id="b3360-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="b3360-115">Uzņēmums Fabrikam nodrošina uzstādīšanas pakalpojumus, taču robotu rokas tiek iegādātas no uzņēmuma Trey robotics.</span><span class="sxs-lookup"><span data-stu-id="b3360-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="b3360-116">Ja robotu roku uzstādīšana korporācijā Adatum paver jaunu nozares vertikāli uzņēmuma Trey ražotajām robotu rokām, Trey varētu šim darījumam noteikt īpašu atlaidi uzņēmumam Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="b3360-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="b3360-117">Šajā gadījumā Fabrikam izveidos produkta piedāvājuma rindu “Robotu rokas” un ievadīs šim piedāvājumam īpašas vienības izmaksas.</span><span class="sxs-lookup"><span data-stu-id="b3360-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="b3360-118">Šīs izmaksas atšķiras no Trey ražoto robotu roku standarta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="b3360-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
