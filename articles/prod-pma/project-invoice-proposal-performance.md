---
title: Projekta rēķina priekšlikuma izpilde
description: Šajā tēmā ir sniegta informācija par veiktspējas uzlabojumiem projekta rēķinu priekšlikumiem.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269799"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="b3db7-103">Projekta rēķina priekšlikuma izpilde</span><span class="sxs-lookup"><span data-stu-id="b3db7-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3db7-104">Izveidojot jaunu rēķinu, kas tiek iekļauts rēķinā, palielināts projektu un apakšprojektu skaits, var rasties veiktspējas problēmas.</span><span class="sxs-lookup"><span data-stu-id="b3db7-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="b3db7-105">Lai uzlabotu veiktspēju, ir pieejams līdzeklis, kas samazina laiku, kas nepieciešams, lai izveidotu jaunu rēķinu par iegrāmatotajām projekta transakcijām.</span><span class="sxs-lookup"><span data-stu-id="b3db7-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="b3db7-106">Projekta rēķinu priekšlikumu veiktspējas uzlabošanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="b3db7-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="b3db7-107">Lai iespējotu projekta rēķinu priekšlikumu uzlabošanas līdzekli, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="b3db7-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="b3db7-108">Atveriet **Līdzekļu pārvaldība** > **Visi**.</span><span class="sxs-lookup"><span data-stu-id="b3db7-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="b3db7-109">Līdzekļu sarakstā atrodiet **Projektu rēķinu priekšlikumu veiktspējas uzlabošana**.</span><span class="sxs-lookup"><span data-stu-id="b3db7-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="b3db7-110">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="b3db7-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="b3db7-111">Atsvaidziniet pārlūkprogrammu un pēc tam izveidojiet jaunu rēķina priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="b3db7-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="b3db7-112">Projekta rēķinu priekšlikumu veiktspējas uzlabošanas izslēgšana</span><span class="sxs-lookup"><span data-stu-id="b3db7-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="b3db7-113">Lai izslēgtu projekta rēķinu priekšlikumu uzlabošanas līdzekli, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="b3db7-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="b3db7-114">Atveriet **Līdzekļu pārvaldība** > **Visi**.</span><span class="sxs-lookup"><span data-stu-id="b3db7-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="b3db7-115">Līdzekļu sarakstā atrodiet **Projektu rēķinu priekšlikumu veiktspējas uzlabošana**.</span><span class="sxs-lookup"><span data-stu-id="b3db7-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="b3db7-116">Atlasiet **Atspējot**.</span><span class="sxs-lookup"><span data-stu-id="b3db7-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="b3db7-117">Atsvaidziniet pārlūkprogrammu.</span><span class="sxs-lookup"><span data-stu-id="b3db7-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="b3db7-118">Ja ir iespējotas norēķinu kārtulas, rēķina priekšlikuma veiktspēju nevar lietot.</span><span class="sxs-lookup"><span data-stu-id="b3db7-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="b3db7-119">Pakešveida apstrādes laikā, lai izveidotu rēķina priekšlikumus, apakšuzdevumu skaits sadalīs uzdevumus maksimālā skaitā, pamatojoties uz to līgumu skaitu, kuriem ir transakcijas ar izrakstāmu rēķinu, neatkarīgi no tā, ko ievadījāt.</span><span class="sxs-lookup"><span data-stu-id="b3db7-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="b3db7-120">Piemēram, ja ievadāt **3** kā apakšuzdevumu skaitu rēķina priekšlikuma izveidei partijās un ir tikai divi līgumi ar transakcijām ar izrakstāmu rēķinu, tiek izveidoti tikai divi apakšuzdevumi.</span><span class="sxs-lookup"><span data-stu-id="b3db7-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
