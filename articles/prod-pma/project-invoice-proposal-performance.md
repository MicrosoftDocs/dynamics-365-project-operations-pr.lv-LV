---
title: Projekta rēķina priekšlikuma izpilde
description: Šajā tēmā ir sniegta informācija par veiktspējas uzlabojumiem projekta rēķinu priekšlikumiem.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573568"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="7ad1b-103">Projekta rēķina priekšlikuma izpilde</span><span class="sxs-lookup"><span data-stu-id="7ad1b-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="7ad1b-104">Izveidojot jaunu rēķinu, kas tiek iekļauts rēķinā, palielināts projektu un apakšprojektu skaits, var rasties veiktspējas problēmas.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="7ad1b-105">Lai uzlabotu veiktspēju, ir pieejams līdzeklis, kas samazina laiku, kas nepieciešams, lai izveidotu jaunu rēķinu par iegrāmatotajām projekta transakcijām.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="7ad1b-106">Projekta rēķinu priekšlikumu veiktspējas uzlabošanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="7ad1b-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="7ad1b-107">Lai iespējotu projekta rēķinu priekšlikumu uzlabošanas līdzekli, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="7ad1b-108">Atveriet **Līdzekļu pārvaldība** > **Visi**.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="7ad1b-109">Līdzekļu sarakstā atrodiet **Projektu rēķinu priekšlikumu veiktspējas uzlabošana**.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="7ad1b-110">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="7ad1b-111">Atsvaidziniet pārlūkprogrammu un pēc tam izveidojiet jaunu rēķina priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="7ad1b-112">Projekta rēķinu priekšlikumu veiktspējas uzlabošanas izslēgšana</span><span class="sxs-lookup"><span data-stu-id="7ad1b-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="7ad1b-113">Lai izslēgtu projekta rēķinu priekšlikumu uzlabošanas līdzekli, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="7ad1b-114">Atveriet **Līdzekļu pārvaldība** > **Visi**.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="7ad1b-115">Līdzekļu sarakstā atrodiet **Projektu rēķinu priekšlikumu veiktspējas uzlabošana**.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="7ad1b-116">Atlasiet **Atspējot**.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="7ad1b-117">Atsvaidziniet pārlūkprogrammu.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="7ad1b-118">Rēķinu priekšlikumu veiktspēju nevar lietot, ja ir iespējotas norēķinu kārtulas vai tiek palaisti pakešu procesi.</span><span class="sxs-lookup"><span data-stu-id="7ad1b-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
