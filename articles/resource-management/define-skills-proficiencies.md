---
title: Prasmju un metodiku definēšana
description: Šajā tēmā sniegta informācija par to, kā iestatīt kvalifikācijas modeļus, lai novērtētu resursus.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015340"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="f3b9d-103">Prasmju un metodiku definēšana</span><span class="sxs-lookup"><span data-stu-id="f3b9d-103">Define skills and proficiencies</span></span>

<span data-ttu-id="f3b9d-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="f3b9d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f3b9d-105">Prasmes ir resursu īpašības, kas tiek kopīgotas programmā Dynamics 365 Project Operations un attiecīgajos gadījumos programmā Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="f3b9d-106">Lai uzturētu prasmju krātuvi programmā Project Operations, atveriet sadaļu **Resursi** \> **Resursu prasmes**.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="f3b9d-107">Kvalifikācijas modeļu izmantošana, lai vērtētu resursus</span><span class="sxs-lookup"><span data-stu-id="f3b9d-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="f3b9d-108">Resursu prasmes vērtē atbilstoši kvalifikācijas modeļiem.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="f3b9d-109">Atsevišķi vērtējumi ir iekļauti kvalifikācijas modelī.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="f3b9d-110">Lai izveidotu kvalifikācijas modeli, atveriet sadaļu **Resurss** \> **Kvalifikācijas modeļi** un pēc tam atlasiet vienumu **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="f3b9d-111">Jaunajā vērtējuma modelī norādiet minimālo vērtējuma vērtību, maksimālo novērtējuma vērtību un novērtēto entītiju.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="f3b9d-112">Apakšrežģī **Vērtējuma vērtības** var definēt dažādas vērtējuma vērtības no minimālās līdz maksimālajai.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="f3b9d-113">Šīs vērtējuma vērtības tiek rādītas vienumu **Resursu prasības**, **Plānošanas panelis** un **Plānošanas palīgs** filtros.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]