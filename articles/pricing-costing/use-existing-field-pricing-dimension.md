---
title: Project Operations lauki kā cenu kategorijas
description: Šajā tēmā ir sniegta informācija par lauku kā cenu noteikšanas dimensiju izmantošanu programmā Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119247"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="1639f-103">Project Operations lauki kā cenu kategorijas</span><span class="sxs-lookup"><span data-stu-id="1639f-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="1639f-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="1639f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1639f-105">Entitījai **Faktiskās vērtības** ir daudzi lauki, kurus var izmantot kā cenu noteikšanas dimensijas resursos balstītai cenu noteikšanai.</span><span class="sxs-lookup"><span data-stu-id="1639f-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="1639f-106">Piemēram, viens kopīgs lauks ir **Rezervējamais resurss**.</span><span class="sxs-lookup"><span data-stu-id="1639f-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="1639f-107">Mazāki uzņēmumi, kuriem ir mazāk par 20-30 apmaksājamo resursu, var secināt, ka ir vienkāršāk, kad katram resursam ir savas norēķinu un izmaksu likmes.</span><span class="sxs-lookup"><span data-stu-id="1639f-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="1639f-108">Taču, augot apmaksājamajam darbaspēkam, resursiem raksturīgo likmju uzturēšana var kļūt nereāla.</span><span class="sxs-lookup"><span data-stu-id="1639f-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="1639f-109">Resursiem saņemot paaugstinājumu, iegūstot vairāk pieredzes vai jaunas prasmes, resursu izmaksu un apmaksas likmes sāk atšķirties.</span><span class="sxs-lookup"><span data-stu-id="1639f-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="1639f-110">Vēl viens piemērs ir darījuma kategorija.</span><span class="sxs-lookup"><span data-stu-id="1639f-110">Another example is that of transaction category.</span></span> <span data-ttu-id="1639f-111">Klienti un Īstenotāji ir izmantojuši darījuma kategoriju, lai klasificētu darbu un izmantotu lauku cenai un izmaksām, balstoties uz darba kategoriju.</span><span class="sxs-lookup"><span data-stu-id="1639f-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
