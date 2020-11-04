---
title: Starpuzņēmumu izdevumi
description: Darba ņēmējs, ko organizācijā nodarbina viena juridiska persona, var veikt darbu citai juridiskai personai tajā pašā organizācijā. Šādā gadījumā var izmantot starpuzņēmumu izmaksu līdzekli, lai darbinieka izdevumus piešķirtu juridiskajai personai, kurai tika veikts darbs.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080595"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="fd6bc-104">Starpuzņēmumu izdevumi</span><span class="sxs-lookup"><span data-stu-id="fd6bc-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd6bc-105">Darba ņēmējs, ko organizācijā nodarbina viena juridiska persona, var veikt darbu citai juridiskai personai tajā pašā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="fd6bc-106">Šādā gadījumā var izmantot starpuzņēmumu izmaksu līdzekli, lai darbinieka izdevumus piešķirtu juridiskajai personai, kurai tika veikts darbs.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="fd6bc-107">Juridiska persona, kas nodarbina darba ņēmēju, tiek saukta par juridisku personu-aizdevēju.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="fd6bc-108">Juridiskā persona, kurai darba ņēmējs uzkrāj izdevumus, tiek saukta par aizņemošo juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="fd6bc-109">Lai darba ņēmējs varētu izveidot un iesniegt izdevumus darbam, kas tiek veikts citai juridiskai personai, juridiskajā personā-aizdevējā, lapā **Izdevumu pārvaldības parametri** atlasiet opciju **Atļaut starpuzņēmumu izmaksu rindas**.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="fd6bc-110">Starpuzņēmumu izmaksu nodokļu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="fd6bc-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd6bc-111">Ja vēlaties izmantot nodokļu grupas, kas saistītas ar (avota) juridisko personu-aizdevēju, nevis (galamērķa) juridisko personu-aizņēmēju savā izdevumu atskaitē, jums tā ir jākonfigurē virsgrāmatas PVN iestatīšanā.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="fd6bc-112">Ja virsgrāmatas parametrs **Juridiskā persona starpuzņēmumu nodokļu grāmatošanai** ir iestatīts kā **Avots** un **Lietot PVN nodokļu kārtulas** ir iestatīts uz **Nē** , tiks izmantota juridiskās personas-aizdevēja nodokļu kombinācija.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="fd6bc-113">Ja viens un tas pats parametrs ir iestatīts uz **Mērķis** , tiks izmantota juridiskās personas-aizņēmēja nodokļu kombinācija.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="fd6bc-114">Ja juridiskajām personām ASV parametrs ir iestatīts uz **Avots** , jaunajā lapā **Virsgrāmatas grāmatošanas grupas** ir jākonfigurē arī lauks **Pārdošanas nodokļa parāds**.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="fd6bc-115">Grāmatvedības programma izmantos šajā laukā ietverto informāciju, lai iegūtu ar nodokļiem saistītu uzskaites ierakstu.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="fd6bc-116">Darbība ir konsekventa izdevumu rindām, kas iegrāmatotas ar projektu vai bez tā.</span><span class="sxs-lookup"><span data-stu-id="fd6bc-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
