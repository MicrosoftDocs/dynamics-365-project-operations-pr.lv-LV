---
title: Ad hoc avansa izveide līgumā
description: Šajā tēmā ir sniegta informācija par līguma avansa izveidi pēc nepieciešamības.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f0a6391a3bf6dd39d21504a6f286e4ff1954183
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273606"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a><span data-ttu-id="4ae85-103">Ad hoc avansa izveide līgumā</span><span class="sxs-lookup"><span data-stu-id="4ae85-103">Creating an ad hoc advance on a contract</span></span>

<span data-ttu-id="4ae85-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="4ae85-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4ae85-105">Microsoft Dynamics 365 Project Operations atbalsta rēķinu izrakstīšanas scenārijus, kuros ir iesaistīti priekšapmaksas un avansa maksājumi.</span><span class="sxs-lookup"><span data-stu-id="4ae85-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="4ae85-106">Process, lai izmantotu **Avansus**, lietojot **Project Operations**, ir līdzīgs **Honorāra** līgumiem.</span><span class="sxs-lookup"><span data-stu-id="4ae85-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="4ae85-107">Izpildiet tālāk aprakstītās darbības, lai klientam izrakstītu avansa rēķinu.</span><span class="sxs-lookup"><span data-stu-id="4ae85-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="4ae85-108">Atveriet lapu **Projekta līgums** un pēc tam atlasiet cilni **Avansi un honorāri**.</span><span class="sxs-lookup"><span data-stu-id="4ae85-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="4ae85-109">Apakšrežģī, kurā ir uzskaitīti visi iepriekš ierakstītie avansa maksājumi un priekšapmaksas, atlasiet **+ Jauns projekta līguma honorārs**.</span><span class="sxs-lookup"><span data-stu-id="4ae85-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="4ae85-110">Tiek atvērta **Ātrās izveides** veidlapa, lai ierakstītu priekšapmaksu vai avansu.</span><span class="sxs-lookup"><span data-stu-id="4ae85-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="4ae85-111">Tālāk esošajā tabulā ir uzskaitīti avansa reģistrēšanas lauki un apsvērumi, kas jāņem vērā, izveidojot jaunus.</span><span class="sxs-lookup"><span data-stu-id="4ae85-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="4ae85-112">Lauks</span><span class="sxs-lookup"><span data-stu-id="4ae85-112">Field</span></span> | <span data-ttu-id="4ae85-113">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4ae85-113">Description</span></span> | <span data-ttu-id="4ae85-114">Lejupstraumes ietekme</span><span class="sxs-lookup"><span data-stu-id="4ae85-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="4ae85-115">**Projekta līguma klients**</span><span class="sxs-lookup"><span data-stu-id="4ae85-115">**Project Contract Customer**</span></span> | <span data-ttu-id="4ae85-116">Šajā laukā ir norādīts, kuram līgumā paredzētajam klientam tiks izrakstīts rēķins par šo avansu.</span><span class="sxs-lookup"><span data-stu-id="4ae85-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="4ae85-117">Ja līgumā ir vairāki klienti un katram no tiem vēlaties izrakstīt rēķinu par noteiktu honorāru vai avansa summu, izveidojiet avansu katram klientam atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="4ae85-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="4ae85-118">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="4ae85-118">**Description**</span></span> | <span data-ttu-id="4ae85-119">Avansa mērķa vai laika apraksts, lai palīdzētu identificēt šo avansu.</span><span class="sxs-lookup"><span data-stu-id="4ae85-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="4ae85-120">Šis apraksts tiek parādīts šī avansa rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="4ae85-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="4ae85-121">**Summa**</span><span class="sxs-lookup"><span data-stu-id="4ae85-121">**Amount**</span></span> | <span data-ttu-id="4ae85-122">Priekšapmaksas vai avansa summa.</span><span class="sxs-lookup"><span data-stu-id="4ae85-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="4ae85-123">Šī summa tiek parādīta šī avansa rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="4ae85-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="4ae85-124">**Rēķina datums**</span><span class="sxs-lookup"><span data-stu-id="4ae85-124">**Invoice Date**</span></span> | <span data-ttu-id="4ae85-125">Datums, kurā klientam tiek izrakstīts rēķins par avansu.</span><span class="sxs-lookup"><span data-stu-id="4ae85-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="4ae85-126">Šis ir automātiskā rēķina izveides procesa datums, kad šim avansam tika izveidota rēķina rinda.</span><span class="sxs-lookup"><span data-stu-id="4ae85-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="4ae85-127">**Rēķina statuss**</span><span class="sxs-lookup"><span data-stu-id="4ae85-127">**Invoice Status**</span></span> | <span data-ttu-id="4ae85-128">Tas ir opciju iestatījums, kas norāda, vai šis avanss ir pievienots šī klienta rēķina melnrakstam.</span><span class="sxs-lookup"><span data-stu-id="4ae85-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="4ae85-129">Iespējamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="4ae85-129">The possible values are:</span></span></br><span data-ttu-id="4ae85-130">- **Nav gatavs rēķina izrakstīšanai**</span><span class="sxs-lookup"><span data-stu-id="4ae85-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="4ae85-131">- **Gatavs rēķina izrakstīšanai**</span><span class="sxs-lookup"><span data-stu-id="4ae85-131">- **Ready to invoice**</span></span> | <span data-ttu-id="4ae85-132">Kad avansa maksājums vai priekšapmaksa ir atzīmēta kā **Gatava rēķina izrakstīšanai**, tas tiek pievienots kā rindas laiks rēķina melnrakstā.</span><span class="sxs-lookup"><span data-stu-id="4ae85-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="4ae85-133">Tikai pilnīgi izrakstīts avanss var tikt izmantots, lai sasaistītu projekta izmaksas nākamajam rēķina periodam.</span><span class="sxs-lookup"><span data-stu-id="4ae85-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="4ae85-134">Ātrās izveides dialoglodziņā atlasiet **Saglabāt un aizvērt**, lai ierakstītu avansu vai priekšapmaksu.</span><span class="sxs-lookup"><span data-stu-id="4ae85-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]