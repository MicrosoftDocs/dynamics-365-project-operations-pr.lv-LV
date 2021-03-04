---
title: Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem — Lite
description: Šajā tēmā ir sniegta informācija par izmaksu un pārdošanas likmju iestatīšanu preču katalogā.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764564"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="6dae4-103">Izmaksu un pārdošanas cenu iestatīšana kataloga produktiem — Lite</span><span class="sxs-lookup"><span data-stu-id="6dae4-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="6dae4-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="6dae4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6dae4-105">Cenu noteikšanas iestatīšana preču kataloga vienumiem programmā Dynamics 365 Project Operations ir tāda pati kā pakalpojumā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6dae4-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="6dae4-106">Programmā Project Operations produktus nevar prognozēt vai izmantot projektos, tāpēc produktu kataloga cenas nevajag iestatīt projekta piedāvājumu un līgumu cenu sarakstos.</span><span class="sxs-lookup"><span data-stu-id="6dae4-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="6dae4-107">Lai iestatītu produkta kataloga cenas, izmantojiet piedāvājuma, līguma vai konta lauku **Produkta cena**.</span><span class="sxs-lookup"><span data-stu-id="6dae4-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="6dae4-108">Neiestatiet produkta kataloga cenas projekta cenu sarakstos.</span><span class="sxs-lookup"><span data-stu-id="6dae4-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="6dae4-109">Projekta cenrādis ir pieejams tikai risinājumam Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6dae4-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="6dae4-110">Lietojumprogrammas biznesa loģika kopē cenu sarakstus no piedāvājuma uz līgumu.</span><span class="sxs-lookup"><span data-stu-id="6dae4-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="6dae4-111">Rezultāts ir līgumā noteiktais projekta cenrādis.</span><span class="sxs-lookup"><span data-stu-id="6dae4-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="6dae4-112">Kopēšanas darbība var aizkavēt piedāvājuma veiksmīgu procesu, ja projekta cenrādis piedāvājumā kļūst pārāk liels.</span><span class="sxs-lookup"><span data-stu-id="6dae4-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="6dae4-113">Produktu cenrāži netiek kopēti, lai izveidotu pielāgotus cenrāžus līgumos.</span><span class="sxs-lookup"><span data-stu-id="6dae4-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="6dae4-114">Tā kā netiek veikta kopēšana, piedāvājuma procesa veiktspēja netiek ietekmēta.</span><span class="sxs-lookup"><span data-stu-id="6dae4-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
