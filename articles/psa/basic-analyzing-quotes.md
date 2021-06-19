---
title: Projekta piedāvājumu analīze
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumu analīzi.
author: rumant
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
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012460"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="7e1aa-103">Projekta piedāvājumu analīze</span><span class="sxs-lookup"><span data-stu-id="7e1aa-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7e1aa-104">Dynamics 365 Project Service Automation analizē projekta piedāvājumus, lai novērtētu ienesīgumu.</span><span class="sxs-lookup"><span data-stu-id="7e1aa-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="7e1aa-105">Programma analizē arī to, cik labi piedāvājums atbilst klienta vēlmēm attiecībā uz piegādes datumu vai izpildes datumu, kā arī budžetu.</span><span class="sxs-lookup"><span data-stu-id="7e1aa-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="7e1aa-106">Ienesīguma analīze</span><span class="sxs-lookup"><span data-stu-id="7e1aa-106">Profitability analysis</span></span>

<span data-ttu-id="7e1aa-107">Project Service Automation analizē ienesīgumu, izmantojot bruto peļņu un koriģēto bruto peļņu.</span><span class="sxs-lookup"><span data-stu-id="7e1aa-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="7e1aa-108">Bruto peļņas tiek aprēķinātas, izmantojot tālāk norādīto formulu.</span><span class="sxs-lookup"><span data-stu-id="7e1aa-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="7e1aa-109">Koriģētā bruto peļņa tiek aprēķināta, izmantojot tālāk norādīto formulu.</span><span class="sxs-lookup"><span data-stu-id="7e1aa-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="7e1aa-110">Ja bruto peļņas un koriģētās bruto peļņas vērtības ievērojami atšķiras, liela daļa darba piedāvājumā ir klasificēta kā rēķinā neiekļaujama.</span><span class="sxs-lookup"><span data-stu-id="7e1aa-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="7e1aa-111">Klientu vēlmju analīze</span><span class="sxs-lookup"><span data-stu-id="7e1aa-111">Analysis of customer expectations</span></span>

<span data-ttu-id="7e1aa-112">Varat analizēt piedāvājumus un ģenerēt klientu vēlmju diagrammas attiecībā uz grafiku un budžetu, ja tālāk esošajos laukos ievadāt vērtības.</span><span class="sxs-lookup"><span data-stu-id="7e1aa-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="7e1aa-113">Lauks **Pieprasītais piegādes datums** piedāvājuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="7e1aa-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="7e1aa-114">Katras piedāvājuma rindas lauks **Klienta budžets** (uz projektu balstītām rindām un uz preci balstītām rindām).</span><span class="sxs-lookup"><span data-stu-id="7e1aa-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="7e1aa-115">Klienta vēlmju analīze par grafiku tiek veikta, salīdzinot piedāvājuma rindu detaļu vēlāko beigu datumu ar pieprasīto piegādes datumu visās piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="7e1aa-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="7e1aa-116">Klienta vēlmju analīze par budžetu tiek veikta, salīdzinot klienta kopējā budžeta summu ar piedāvāto summu visās piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="7e1aa-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]