---
title: Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem — Lite
description: Šajā tēmā ir sniegta informācija par izmaksu un pārdošanas likmju iestatīšanu preču katalogā.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176710"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="3de5a-103">Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem — Lite</span><span class="sxs-lookup"><span data-stu-id="3de5a-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="3de5a-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="3de5a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3de5a-105">Cenu iestatīšana preču kataloga vienumiem risinājumā Dynamics 365 Project Operations ir tāda pati kā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="3de5a-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="3de5a-106">Tā kā produktus nevar novērtēt vai izmantot projektiem risinājumā Project Operations,, preču kataloga cenas nav jāiestata projekta cenrāžiem piedāvājumiem un līgumiem.</span><span class="sxs-lookup"><span data-stu-id="3de5a-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="3de5a-107">Preču kataloga cenas ir jāiestata piedāvājuma, līguma vai konta laukā **Produkta cena**.</span><span class="sxs-lookup"><span data-stu-id="3de5a-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="3de5a-108">Neiestatiet preču kataloga cenas šo entītiju projektu cenrāžos.</span><span class="sxs-lookup"><span data-stu-id="3de5a-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="3de5a-109">Projekta cenrādis ir pieejams tikai risinājumam Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3de5a-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="3de5a-110">Pastāv ar piedāvājumu saistīta biznesa loģika, kas kopē cenrāžus no piedāvājuma uz līgumu.</span><span class="sxs-lookup"><span data-stu-id="3de5a-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="3de5a-111">Rezultāts ir līgumā noteiktais projekta cenrādis.</span><span class="sxs-lookup"><span data-stu-id="3de5a-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="3de5a-112">Kopēšanas darbība var aizkavēt piedāvājuma veiksmīgu procesu, ja projekta cenrādis piedāvājumā kļūst pārāk liels.</span><span class="sxs-lookup"><span data-stu-id="3de5a-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="3de5a-113">Produktu cenrāži netiek kopēti, lai izveidotu pielāgotus cenrāžus līgumos.</span><span class="sxs-lookup"><span data-stu-id="3de5a-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="3de5a-114">Tas nozīmē, ka produktu cenrāži neietekmēs piedāvājuma veiksmīgu izpildi.</span><span class="sxs-lookup"><span data-stu-id="3de5a-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
