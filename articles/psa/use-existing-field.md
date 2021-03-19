---
title: Izmantojiet esošu programmas Project Service lauku kā cenu noteikšanas dimensiju
description: Šajā tēmā ir sniegta informācija par esošu Project Service lauku izmantošanu kā cenu noteikšanas dimensijas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281577"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="63a51-103">Izmantojiet esošu programmas Project Service lauku kā cenu noteikšanas dimensiju</span><span class="sxs-lookup"><span data-stu-id="63a51-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="63a51-104">Project Service Automation (PSA) ir daudzi lauki entītijā **Faktiskās vērtības**, ko var izmantot kā cenu noteikšanas dimensijas uz resursiem balstītai cenu noteikšanai projektu organizācijās.</span><span class="sxs-lookup"><span data-stu-id="63a51-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="63a51-105">Piemēram, viens kopīgs lauks ir **Rezervējamais resurss**.</span><span class="sxs-lookup"><span data-stu-id="63a51-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="63a51-106">Mazāki uzņēmumi, kuriem ir mazāk par 20-30 apmaksājamo resursu, var secināt, ka ir vienkāršāk, kad katram resursam ir savas norēķinu un izmaksu likmes.</span><span class="sxs-lookup"><span data-stu-id="63a51-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="63a51-107">Tomēr, tā kā apmaksājamais darbaspēks pieaug, konkrētas likmes var kļūt nereāli uzturēt, jo resursu izmaksas un norēķinu likmes sāk mainīties, kad resursi tiek paaugstināti, iegūst vairāk pieredzes vai iegūst dažādu prasmju kopumu.</span><span class="sxs-lookup"><span data-stu-id="63a51-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="63a51-108">Tā kā šī pieeja joprojām darbojas noteikta lieluma uzņēmumiem, skatiet tēmu [Rezervējamā resursa izmantošana kā cenas noteikšanas dimensiju](bookable-resource-pricing-dimension.md), lai saprastu, kā esošu Project Service lauku var izmantot kā cenas noteikšanas dimensiju.</span><span class="sxs-lookup"><span data-stu-id="63a51-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="63a51-109">Vēl viens piemērs ir darījuma kategorija.</span><span class="sxs-lookup"><span data-stu-id="63a51-109">Another example is that of transaction category.</span></span> <span data-ttu-id="63a51-110">Klienti un Īstenotāji ir izmantojuši darījuma kategoriju programmā PSA, lai klasificētu darbu un izmantotu lauku cenai un izmaksām, balstoties uz darba kategoriju.</span><span class="sxs-lookup"><span data-stu-id="63a51-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="63a51-111">Plašākai informācijai skatiet [Transakcijas kategorijas izmantošana kā cenas noteikšanas dimensiju](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="63a51-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]