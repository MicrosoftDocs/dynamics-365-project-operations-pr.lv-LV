---
title: Vienības un vienību grupas
description: Šajā tēmā ir sniegta informācija par to, kā izveidot vienības un vienību grupas programmā Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 646e20189efb4aab56972f01a52b1bff19f2e79f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996080"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="20fa5-103">Vienības un vienību grupas</span><span class="sxs-lookup"><span data-stu-id="20fa5-103">Units and unit groups</span></span>

<span data-ttu-id="20fa5-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="20fa5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="20fa5-105">Vienības ir daudzumi vai mērvienības, kādās jūs pārdodat savus produktus vai pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="20fa5-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="20fa5-106">Piemēram, ja pārdodat dārzkopība piederumus, vienības sēklu pārdošanai var būt paciņas, kastes un paletes.</span><span class="sxs-lookup"><span data-stu-id="20fa5-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="20fa5-107">Vienību grupa ir šo atšķirīgo vienību kopums.</span><span class="sxs-lookup"><span data-stu-id="20fa5-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="20fa5-108">Lai izpildītu šīs tēmas darbības, pārliecinieties, ka jums ir piešķirta sistēmas administratora vai Sales Professional pārvaldnieka loma vai līdzvērtīgas atļaujas.</span><span class="sxs-lookup"><span data-stu-id="20fa5-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="20fa5-109">Vienību grupas izveide</span><span class="sxs-lookup"><span data-stu-id="20fa5-109">Create a unit group</span></span>

1. <span data-ttu-id="20fa5-110">Vietnes kartē atlasiet **Vienības**.</span><span class="sxs-lookup"><span data-stu-id="20fa5-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="20fa5-111">Atlasiet **Jauns** un dialoglodziņā **Izveidot vienību grupu** ievadiet vienības nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="20fa5-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="20fa5-112">Laukā **Primātā vienība** ievadiet zemāko kopējo mērvienību, kurā produkts tiks pārdots.</span><span class="sxs-lookup"><span data-stu-id="20fa5-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="20fa5-113">Piemēram, varat ievadīt "gabals" vai "unce".</span><span class="sxs-lookup"><span data-stu-id="20fa5-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="20fa5-114">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="20fa5-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="20fa5-115">Vienību pievienošana vienību grupai</span><span class="sxs-lookup"><span data-stu-id="20fa5-115">Add units to a unit group</span></span>

1. <span data-ttu-id="20fa5-116">Atveriet vienību grupu un cilnē **Saistīti** atlasiet **Vienības**.</span><span class="sxs-lookup"><span data-stu-id="20fa5-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="20fa5-117">Redzēsit, ka primārā vienība jau ir pievienota.</span><span class="sxs-lookup"><span data-stu-id="20fa5-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="20fa5-118">Atlasiet **Pievienot jaunu vienību** un lapas **Ātrā izveide: vienība** laukā **Nosaukums** ievadiet vienības nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="20fa5-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="20fa5-119">Laukā **Daudzums** ievadiet daudzumu, kuru saturēs vienība.</span><span class="sxs-lookup"><span data-stu-id="20fa5-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="20fa5-120">Piemēram, ja logā ir divi gabali, ievadiet "2".</span><span class="sxs-lookup"><span data-stu-id="20fa5-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="20fa5-121">Laukā **Pamatvienība** atlasiet pamatvienību, lai noteiktu vienības zemāko mērvienību.</span><span class="sxs-lookup"><span data-stu-id="20fa5-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="20fa5-122">Piemēram, varat atlasīt "Gabals".</span><span class="sxs-lookup"><span data-stu-id="20fa5-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="20fa5-123">Atlasiet **Saglabāt**:</span><span class="sxs-lookup"><span data-stu-id="20fa5-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]