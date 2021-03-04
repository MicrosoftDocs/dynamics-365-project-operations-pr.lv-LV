---
title: Nepabeigtās rēķinu izrakstīšanas pārskatīšana projektiem un projektu līgumiem
description: Šajā tēmā ir sniegta informācija par to, kā apskatīt laiku, izdevumus un produktu rezerves, un kā tās atzīmēt kā gatavus rēķina izrakstīšanai.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150497"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="c99d3-103">Nepabeigtās rēķinu izrakstīšanas pārskatīšana projektiem un projektu līgumiem</span><span class="sxs-lookup"><span data-stu-id="c99d3-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c99d3-104">Kad transakcija ir sagatavota, lai izveidotu un apstrādātu rēķinu, transakcijai jābūt atzīmētai **Gatavs rēķina izrakstīšanai**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="c99d3-105">Šajā tēmā ir apraksti transakciju tipi, ko var izveidot.</span><span class="sxs-lookup"><span data-stu-id="c99d3-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="c99d3-106">Nepabeigtās laika un materiālu rēķinu izrakstīšanas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="c99d3-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="c99d3-107">Kad projektam tiek iesniegts un apstiprināts laika vai izdevumu ieraksts, PSA izveido projekta faktiskās vērtības.</span><span class="sxs-lookup"><span data-stu-id="c99d3-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="c99d3-108">Ja projekta un transakciju klases kombinācija ir kartēta uz līguma rindu laika un materiālu projektam, tad, apstiprinot ierakstu, tiek izveidotas divas faktiskās vērtības:</span><span class="sxs-lookup"><span data-stu-id="c99d3-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="c99d3-109">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="c99d3-109">Cost actual</span></span> 
- <span data-ttu-id="c99d3-110">Rēķinā neiekļautā faktiskā pārdošana</span><span class="sxs-lookup"><span data-stu-id="c99d3-110">Unbilled sales actual</span></span>

<span data-ttu-id="c99d3-111">Rēķinā neiekļautā faktiskā pārdošana norāda nepabeigto rēķinu izrakstīšanu, un tās rēķinu izrakstīšanas statuss ir jāiestata kā **Gatavs rēķina izrakstīšanai**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="c99d3-112">Kad tiek izveidots projekta rēķins, rēķinā neiekļautā faktiskā pārdošana, kas atzīmēta kā **Gatavs rēķina izrakstīšanai**, tiek kopēta kā rēķina rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="c99d3-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="c99d3-113">Lai pārskatītu nepabeigto rēķinu izrakstīšanu par laiku un materiāliem, atveriet sadaļu **Pārdošana** \> **Rēķinu izrakstīšana** \> **Nepabeigtā rēķinu izrakstīšana par laiku un materiālu**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="c99d3-114">Atlasiet visus rēķinos neiekļautos faktiskos pārdošanas datus, kas ir gatavi rēķina izrakstīšanai, un pēc tam atlasiet **Gatavs rēķina izrakstīšanai**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="c99d3-115">Šo faktisko datu norēķinu statuss tiek mainīts uz **Gatavs rēķina izrakstīšanai**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Nepabeigtā rēķinu izrakstīšana par laiku un materiālu](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="c99d3-117">Nepabeigto preču rēķinu izrakstīšanas pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="c99d3-117">Review the product billing backlog</span></span>

<span data-ttu-id="c99d3-118">Programmā PSA, ja projekta līgumam ir uz produktu balstītas līguma rindas, šīs rindas tiek ņemtas vērā rēķinu izrakstīšanai, kad projekta līgumam tiek izveidots rēķins.</span><span class="sxs-lookup"><span data-stu-id="c99d3-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="c99d3-119">Jebkurš produkts, kuram ir līguma rindas, kas ir atzīmētas kā **Gatavs rēķina izrakstīšanai**, tiek kopēts uz projekta rēķinu kā projekta rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="c99d3-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="c99d3-120">Lai pārskatītu nepabeigto rēķinu izrakstīšanu par produktiem, atveriet sadaļu **Pārdošana** \> **Rēķinu izrakstīšana** \> **Nepabeigtā rēķinu izrakstīšana par produktiem**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="c99d3-121">Atlasiet visas uz produktu balstītās līguma rindas, kas ir gatavas rēķina izrakstīšanai, un pēc tam atlasiet **Gatavs rēķina izrakstīšanai**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="c99d3-122">Šo rindu norēķinu statuss tiek mainīts uz **Gatavs rēķina izrakstīšanai**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Nepabeigtā rēķinu izrakstīšana par produktiem](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="c99d3-124">Rēķinu izrakstīšanas atskaites punktu pārskatīšana attiecībā uz fiksētas cenas līgumiem</span><span class="sxs-lookup"><span data-stu-id="c99d3-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="c99d3-125">Katrai projekta līguma rindai, kurai ir fiksētas cenas rēķina izrakstīšanas metode, ir jādefinē līguma atskaites punkti.</span><span class="sxs-lookup"><span data-stu-id="c99d3-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="c99d3-126">Šos līguma atskaites punktus var iekļaut rēķinā tikai tad, ja tie ir atzīmēti kā **Gatavs rēķina izrakstīšanai**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="c99d3-127">Lai pārskatītu rēķinu izrakstīšanas atskaites punktus, atveriet sadaļu **Pārdošana** \> **Rēķinu izrakstīšana** \> **Fiksētas cenas atskaites punkti**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="c99d3-128">Atlasiet atskaites punktus, kas ir gatavi rēķina izrakstīšanai, un pēc tam atlasiet **Gatavs rēķina izrakstīšanai**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="c99d3-129">Šo atskaites punktu norēķinu statuss tiek mainīts uz **Gatavs rēķina izrakstīšanai**.</span><span class="sxs-lookup"><span data-stu-id="c99d3-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Fiksētas cenas atskaites punkti](media/FPBacklog.png)
