---
title: Projekta rēķina priekšlikuma izpilde
description: Šajā tēmā ir sniegta informācija par veiktspējas uzlabojumiem projekta rēķinu priekšlikumiem.
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
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
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920311"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="dec3d-103">Projekta rēķina priekšlikuma izpilde</span><span class="sxs-lookup"><span data-stu-id="dec3d-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dec3d-104">Izveidojot jaunu rēķinu, kas tiek iekļauts rēķinā, palielināts projektu un apakšprojektu skaits, var rasties veiktspējas problēmas.</span><span class="sxs-lookup"><span data-stu-id="dec3d-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="dec3d-105">Lai uzlabotu veiktspēju, ir pieejams līdzeklis, kas samazina laiku, kas nepieciešams, lai izveidotu jaunu rēķinu par iegrāmatotajām projekta transakcijām.</span><span class="sxs-lookup"><span data-stu-id="dec3d-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="dec3d-106">Projekta rēķinu priekšlikumu veiktspējas uzlabošanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="dec3d-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="dec3d-107">Lai iespējotu projekta rēķinu priekšlikumu uzlabošanas līdzekli, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="dec3d-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="dec3d-108">Atveriet **Līdzekļu pārvaldība** > **Visi**.</span><span class="sxs-lookup"><span data-stu-id="dec3d-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="dec3d-109">Līdzekļu sarakstā atrodiet **Projektu rēķinu priekšlikumu veiktspējas uzlabošana**.</span><span class="sxs-lookup"><span data-stu-id="dec3d-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="dec3d-110">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="dec3d-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="dec3d-111">Atsvaidziniet pārlūkprogrammu un pēc tam izveidojiet jaunu rēķina priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="dec3d-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="dec3d-112">Projekta rēķinu priekšlikumu veiktspējas uzlabošanas izslēgšana</span><span class="sxs-lookup"><span data-stu-id="dec3d-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="dec3d-113">Lai izslēgtu projekta rēķinu priekšlikumu uzlabošanas līdzekli, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="dec3d-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="dec3d-114">Atveriet **Līdzekļu pārvaldība** > **Visi**.</span><span class="sxs-lookup"><span data-stu-id="dec3d-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="dec3d-115">Līdzekļu sarakstā atrodiet **Projektu rēķinu priekšlikumu veiktspējas uzlabošana**.</span><span class="sxs-lookup"><span data-stu-id="dec3d-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="dec3d-116">Atlasiet **Atspējot**.</span><span class="sxs-lookup"><span data-stu-id="dec3d-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="dec3d-117">Atsvaidziniet pārlūkprogrammu.</span><span class="sxs-lookup"><span data-stu-id="dec3d-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="dec3d-118">Rēķinu priekšlikumu veiktspēju nevar lietot, ja ir iespējotas norēķinu kārtulas vai tiek palaisti pakešu procesi.</span><span class="sxs-lookup"><span data-stu-id="dec3d-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
