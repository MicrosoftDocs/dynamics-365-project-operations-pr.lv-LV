---
title: Kāpēc cena pēc noklusējuma ir nulle par faktiskajām izmaksām?
description: Novērsiet problēmu, kāpēc cena par faktiskajām izmaksām tiek pēc noklusējuma iestatīta uz 0.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285854"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="e4493-103">Kāpēc izdevumu izmaksu faktiskajos datos šī cena pēc noklusējuma ir nulle</span><span class="sxs-lookup"><span data-stu-id="e4493-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e4493-104">Šis bieži uzdoto jautājumu raksts attiecas uz faktiskajām izmaksām, ja transakcijas klase ir iestatīta uz Izdevumi un transakcijas tips ir iestatīts uz Izmaksas.</span><span class="sxs-lookup"><span data-stu-id="e4493-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="e4493-105">Izmaksu likmju problēmu novēršana faktiskajās izmaksās</span><span class="sxs-lookup"><span data-stu-id="e4493-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="e4493-106">Atveriet saistīto izdevumu ierakstu un pārliecinieties, vai izdevumu ieraksta laukā ir summa.</span><span class="sxs-lookup"><span data-stu-id="e4493-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="e4493-107">Ja sākotnējo izdevumu ieraksta summas lauks ir tukšs, esat atradis problēmu.</span><span class="sxs-lookup"><span data-stu-id="e4493-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="e4493-108">Lai atrisinātu šo problēmu, atkārtoti izveidojiet izdevumu ierakstu ar derīgu summu un apstipriniet to.</span><span class="sxs-lookup"><span data-stu-id="e4493-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]