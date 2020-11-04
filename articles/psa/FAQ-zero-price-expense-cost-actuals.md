---
title: Kāpēc cena pēc noklusējuma ir nulle par faktiskajām izmaksām?
description: Novērsiet problēmu, kāpēc cena par faktiskajām izmaksām tiek pēc noklusējuma iestatīta uz 0.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080465"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="4b3dc-103">Kāpēc cena pēc noklusējuma ir nulle par faktiskajām izmaksām?</span><span class="sxs-lookup"><span data-stu-id="4b3dc-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4b3dc-104">Šis bieži uzdoto jautājumu raksts attiecas uz faktiskajām izmaksām, ja transakcijas klase ir iestatīta uz Izdevumi un transakcijas tips ir iestatīts uz Izmaksas.</span><span class="sxs-lookup"><span data-stu-id="4b3dc-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="4b3dc-105">Izmaksu likmju problēmu novēršana faktiskajās izmaksās</span><span class="sxs-lookup"><span data-stu-id="4b3dc-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="4b3dc-106">Atveriet saistīto izdevumu ierakstu un pārliecinieties, vai izdevumu ieraksta laukā ir summa.</span><span class="sxs-lookup"><span data-stu-id="4b3dc-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="4b3dc-107">Ja sākotnējo izdevumu ieraksta summas lauks ir tukšs, esat atradis problēmu.</span><span class="sxs-lookup"><span data-stu-id="4b3dc-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="4b3dc-108">Lai atrisinātu šo problēmu, atkārtoti izveidojiet izdevumu ierakstu ar derīgu summu un apstipriniet to.</span><span class="sxs-lookup"><span data-stu-id="4b3dc-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
