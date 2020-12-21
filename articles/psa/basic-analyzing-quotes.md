---
title: Projekta piedāvājumu analīze
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu analīzi.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 6ed900620f92e76d293f6b533b101be94b25cff3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127032"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="d089f-103">Projekta piedāvājumu analīze</span><span class="sxs-lookup"><span data-stu-id="d089f-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d089f-104">Dynamics 365 Project Service Automation analizē projekta piedāvājumus, lai novērtētu ienesīgumu.</span><span class="sxs-lookup"><span data-stu-id="d089f-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="d089f-105">Programma analizē arī to, cik labi piedāvājums atbilst klienta vēlmēm attiecībā uz piegādes datumu vai izpildes datumu, kā arī budžetu.</span><span class="sxs-lookup"><span data-stu-id="d089f-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="d089f-106">Ienesīguma analīze</span><span class="sxs-lookup"><span data-stu-id="d089f-106">Profitability analysis</span></span>

<span data-ttu-id="d089f-107">Project Service Automation analizē ienesīgumu, izmantojot bruto peļņu un koriģēto bruto peļņu.</span><span class="sxs-lookup"><span data-stu-id="d089f-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="d089f-108">Bruto peļņas tiek aprēķinātas, izmantojot tālāk norādīto formulu.</span><span class="sxs-lookup"><span data-stu-id="d089f-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="d089f-109">Koriģētā bruto peļņa tiek aprēķināta, izmantojot tālāk norādīto formulu.</span><span class="sxs-lookup"><span data-stu-id="d089f-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="d089f-110">Ja bruto peļņas un koriģētās bruto peļņas vērtības ievērojami atšķiras, liela daļa darba piedāvājumā ir klasificēta kā rēķinā neiekļaujama.</span><span class="sxs-lookup"><span data-stu-id="d089f-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="d089f-111">Klientu vēlmju analīze</span><span class="sxs-lookup"><span data-stu-id="d089f-111">Analysis of customer expectations</span></span>

<span data-ttu-id="d089f-112">Varat analizēt piedāvājumus un ģenerēt klientu vēlmju diagrammas attiecībā uz grafiku un budžetu, ja tālāk esošajos laukos ievadāt vērtības.</span><span class="sxs-lookup"><span data-stu-id="d089f-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="d089f-113">Lauks **Pieprasītais piegādes datums** piedāvājuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="d089f-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="d089f-114">Katras piedāvājuma rindas lauks **Klienta budžets** (uz projektu balstītām rindām un uz preci balstītām rindām).</span><span class="sxs-lookup"><span data-stu-id="d089f-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="d089f-115">Klienta vēlmju analīze par grafiku tiek veikta, salīdzinot piedāvājuma rindu detaļu vēlāko beigu datumu ar pieprasīto piegādes datumu visās piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="d089f-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="d089f-116">Klienta vēlmju analīze par budžetu tiek veikta, salīdzinot klienta kopējā budžeta summu ar piedāvāto summu visās piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="d089f-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>