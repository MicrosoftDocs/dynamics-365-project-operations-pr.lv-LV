---
title: Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem
description: Šajā tēmā ir sniegta informācija par izmaksu un pārdošanas likmju iestatīšanu preču katalogā.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080511"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="355f2-103">Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem</span><span class="sxs-lookup"><span data-stu-id="355f2-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="355f2-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="355f2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="355f2-105">Cenu iestatīšana preču kataloga vienumiem risinājumā Dynamics 365 Project Operations ir tāda pati kā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="355f2-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="355f2-106">Tā kā produktus nevar novērtēt vai izmantot projektiem risinājumā Project Operations,, preču kataloga cenas nav jāiestata projekta cenrāžiem piedāvājumiem un līgumiem.</span><span class="sxs-lookup"><span data-stu-id="355f2-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="355f2-107">Preču kataloga cenas ir jāiestata piedāvājuma, līguma vai konta laukā **Produkta cena**.</span><span class="sxs-lookup"><span data-stu-id="355f2-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="355f2-108">Neiestatiet preču kataloga cenas šo entītiju projektu cenrāžos.</span><span class="sxs-lookup"><span data-stu-id="355f2-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="355f2-109">Projekta cenrādis ir pieejams tikai risinājumam Project Operations.</span><span class="sxs-lookup"><span data-stu-id="355f2-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="355f2-110">Pastāv ar piedāvājumu saistīta biznesa loģika, kas kopē cenrāžus no piedāvājuma uz līgumu.</span><span class="sxs-lookup"><span data-stu-id="355f2-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="355f2-111">Rezultāts ir līgumā noteiktais projekta cenrādis.</span><span class="sxs-lookup"><span data-stu-id="355f2-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="355f2-112">Kopēšanas darbība var aizkavēt piedāvājuma veiksmīgu procesu, ja projekta cenrādis piedāvājumā kļūst pārāk liels.</span><span class="sxs-lookup"><span data-stu-id="355f2-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="355f2-113">Produktu cenrāži netiek kopēti, lai izveidotu pielāgotus cenrāžus līgumos.</span><span class="sxs-lookup"><span data-stu-id="355f2-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="355f2-114">Tas nozīmē, ka produktu cenrāži neietekmēs piedāvājuma veiksmīgu izpildi.</span><span class="sxs-lookup"><span data-stu-id="355f2-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
