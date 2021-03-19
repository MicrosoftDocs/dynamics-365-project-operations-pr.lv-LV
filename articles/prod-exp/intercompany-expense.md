---
title: Starpuzņēmumu izdevumi
description: Šajā tēmā sniegta informācija par to, kā izmantot starpuzņēmumu izdevumus, lai piešķirtu darbinieka izdevumus juridiskai entitījai, kurai tika izpildīts darbs.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271542"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="7002e-103">Starpuzņēmumu izdevumi</span><span class="sxs-lookup"><span data-stu-id="7002e-103">Intercompany expenses</span></span>

<span data-ttu-id="7002e-104">Darba ņēmējs, ko organizācijā nodarbina viena juridiska persona, var veikt darbu citai juridiskai personai tajā pašā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="7002e-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="7002e-105">Varat izmantot starpuzņēmumu izdevumus, lai piešķirtu darbinieka izdevumus juridiskai entitījai, kurai tika izpildīts darbs.</span><span class="sxs-lookup"><span data-stu-id="7002e-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="7002e-106">Juridiska persona, kas nodarbina darba ņēmēju, tiek saukta par juridisku personu-aizdevēju.</span><span class="sxs-lookup"><span data-stu-id="7002e-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="7002e-107">Juridiskā persona, kurai darba ņēmējs uzkrāj izdevumus, tiek saukta par aizņemošo juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="7002e-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="7002e-108">Lai darbinieks varētu izveidot un iesniegt starpuzņēmumu izdevumus, ir jāiespējo starpuzņēmumu izdevumu rindas.</span><span class="sxs-lookup"><span data-stu-id="7002e-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="7002e-109">Aizdevuma juridiskajā entitījā lapā **Izdevumu pārvaldes parametri** atlasiet **Atļaut starpuzņēmumu izdevumu rindas**.</span><span class="sxs-lookup"><span data-stu-id="7002e-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="7002e-110">Starpuzņēmumu izmaksu nodokļu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="7002e-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7002e-111">Pirms varat izmantot nodokļu grupas, kuras jūsu izdevumu atskaitē ir saistītas ar aizdevuma (avota) juridisko entitīju, nevis aizņēmuma (mērķa) juridisko entitīju, ir jāiespējo funkcionalitāte Virsgrāmatas pārdošanas nodokļu iestatīšanas skatā.</span><span class="sxs-lookup"><span data-stu-id="7002e-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="7002e-112">Ja parametrs **Juridiska entitīja starpuzņēmumu nodokļu izlikšanai** ir iestatīts uz **Avots** un **Piemērot pārdošanas nodokļu piemērošanas kārtulas** ir iestatīts uz **Nē**, tiek izmantota aizņēmuma juridiskās entitījas nodokļu kombinācija.</span><span class="sxs-lookup"><span data-stu-id="7002e-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="7002e-113">Ja viens un tas pats parametrs ir iestatīts uz **Mērķis**, tiks izmantota juridiskās personas-aizņēmēja nodokļu kombinācija.</span><span class="sxs-lookup"><span data-stu-id="7002e-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="7002e-114">Ja juridiskajām personām ASV parametrs ir iestatīts uz **Avots**, jaunajā lapā **Virsgrāmatas grāmatošanas grupas** ir jākonfigurē arī lauks **Pārdošanas nodokļa parāds**.</span><span class="sxs-lookup"><span data-stu-id="7002e-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="7002e-115">Grāmatvedības programma izmantos šajā laukā ietverto informāciju, lai iegūtu ar nodokļiem saistītu uzskaites ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7002e-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="7002e-116">Darbība ir konsekventa izdevumu rindām, kas iegrāmatotas ar projektu vai bez tā.</span><span class="sxs-lookup"><span data-stu-id="7002e-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]