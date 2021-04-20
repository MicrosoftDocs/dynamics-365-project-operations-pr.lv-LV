---
title: Pro formas projekta rēķina apstiprināšana
description: Šajā tēmā ir sniegta informācija par proformas projekta rēķinu apstiprinājumu programmā Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 144c1b6a49951af8be0c619f41808e7617e59c92
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867095"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="6e53f-103">Pro formas projekta rēķina apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="6e53f-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="6e53f-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="6e53f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6e53f-105">Pēc tam, kad ir apstiprināts proforma rēķins, projekta rēķina statuss tiek atjaunināts uz **Apstiprināts**.</span><span class="sxs-lookup"><span data-stu-id="6e53f-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="6e53f-106">Kad rēķins ir apstiprināts, tas kļūst tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="6e53f-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="6e53f-107">Turpmāk rēķinu var labot tikai tad, ja ir veiktas klientam ierosinātas korekcijas vai kredīti.</span><span class="sxs-lookup"><span data-stu-id="6e53f-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="6e53f-108">Tālāk sniegtajā tabulā ir uzskaitīti sistēmā izveidotie faktiskie dati.</span><span class="sxs-lookup"><span data-stu-id="6e53f-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="6e53f-109">Šie faktiskie dati tiek izveidoti, kad projekta rēķina melnrakstā pirms apstiprināšanas tiek veiktas noteiktas darbības.</span><span class="sxs-lookup"><span data-stu-id="6e53f-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="6e53f-110">
                    <strong>Scenārijs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e53f-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="6e53f-111">
                    <strong>Pēc apstiprināšanas izveidotie faktiskie dati</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6e53f-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6e53f-112">Rēķina izrakstīšana par honorāru vai avansu</span><span class="sxs-lookup"><span data-stu-id="6e53f-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-113">Rēķinā iekļautas pārdošanas faktiskie dati ar tipu <strong>Honorārs</strong> tiek izveidoti par avansa vai honorāra summu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-114">Rēķinā neiekļautas pārdošanas faktiskie dati par negatīvu summu honorāram vai avansam, kas tiks izmantota saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="6e53f-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6e53f-115">Pēc honorāra vai avansa pilnīgas saskaņošanas rēķinā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-116">Rēķinā neiekļautās pārdošanas atsaukšana honorāram vai avansam, kas tika izveidots saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="6e53f-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="6e53f-117">Šī summa ir pozitīva, jo tā ir paredzēta, lai atceltu negatīvo summu, kas tika izveidota tad, kad tika izrakstīts rēķins par honorāru vai avansu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-118">Rēķinā iekļautās pārdošanas faktiskie dati par summu šajā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6e53f-119">Pēc honorāra vai avansa daļējas saskaņošanas rēķinā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-120">Rēķinā neiekļautās pārdošanas atsaukšana honorāram vai avansam, kas tika izveidots saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="6e53f-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="6e53f-121">Šī summa ir pozitīva, jo tā ir paredzēta, lai atceltu negatīvo summu, kas tika izveidota tad, kad tika izrakstīts rēķins par honorāru vai avansu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-122">Rēķinā iekļautās pārdošanas faktiskie dati par summu šajā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-123">Negatīva rēķinā neiekļautas pārdošanas faktiskā summa no atlikušā honorāra vai avansa summas, kas tiks izmantota saskaņošanai turpmākos rēķinos.</span><span class="sxs-lookup"><span data-stu-id="6e53f-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6e53f-124">Rēķina izveide laika darījumam bez labojumiem rēķina melnrakstā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-125">Rēķinā neiekļautās pārdošanas atsaukšana stundām un summai sākotnējā laika apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-126">Rēķinā iekļautās pārdošanas faktiskie dati stundām un summai sākotnējā laika apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6e53f-127">Rēķina izveide laika darījumam, kas tika rediģēts, lai samazinātu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-128">Rēķinā neiekļautās pārdošanas atsaukšana stundām un summai sākotnējā laika apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-129">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa stundām un summu rediģētā rēķina rindu informācijā, pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="6e53f-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-130">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas nav iekasējami par atlikušajām stundām un summu pēc laboto ciparu atvilkšanas rediģētā rēķina rindu informācijā, pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="6e53f-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6e53f-131">Rēķina izveide laika darījumam, kas tika rediģēts, lai palielinātu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-132">Rēķinā neiekļautās pārdošanas atsaukšana stundām un summai sākotnējā laika apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-133">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa stundām un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="6e53f-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6e53f-134">Rēķina izveide izdevumu darījumam bez labojumiem rēķina melnrakstā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-135">Rēķinā neiekļautās pārdošanas atsaukšana daudzumam un summai sākotnējā izdevumu apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-136">Rēķinā iekļautās pārdošanas faktiskie dati daudzumam un summai sākotnējā izdevumu apstiprinājumā</span><span class="sxs-lookup"><span data-stu-id="6e53f-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6e53f-137">Rēķina izveide izdevumu darījumam, kas tika rediģēts, lai samazinātu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-138">Rēķinā neiekļautās pārdošanas atsaukšana daudzumam un summai sākotnējā izdevumu apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-139">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama par daudzumu un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="6e53f-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-140">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas nav iekasējami par atlikušo daudzumu un summu pēc laboto ciparu atvilkšanas rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="6e53f-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6e53f-141">Rēķina izveide izdevumu darījumam, kas tika rediģēts, lai palielinātu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-142">Rēķinā neiekļautās pārdošanas atsaukšana daudzumam un summai sākotnējā izdevumu apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-143">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama par daudzumu un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="6e53f-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6e53f-144">Materiāla transakcijas bez labojumiem ietveršana melnraksta rēķinā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-145">Rēķinā neiekļautās pārdošanas atsaukšana par sākotnējā materiālu lietojuma apstiprināšanā norādīto daudzumu un summu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-146">Rēķinā iekļautā pārdošanas vērtība par sākotnējā materiālu lietojuma apstiprināšanā norādīto daudzumu un summu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6e53f-147">Tādas materiālu transakcijas ietveršana rēķinā, kas tika rediģēta, lai samazinātu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-148">Rēķinā neiekļautās pārdošanas atsaukšana par sākotnējā laika apstiprināšanā norādīto daudzumu un summu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-149">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama par daudzumu un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="6e53f-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-150">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas nav iekasējami par atlikušo daudzumu un summu pēc laboto ciparu atvilkšanas rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="6e53f-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6e53f-151">Tādas materiālu transakcijas ietveršana rēķinā, kas tika rediģēta, lai palielinātu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-152">Rēķinā neiekļautās pārdošanas atsaukšana par sākotnējā materiālu lietojuma apstiprināšanā norādīto daudzumu un summu.</span><span class="sxs-lookup"><span data-stu-id="6e53f-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-153">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama par daudzumu un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="6e53f-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6e53f-154">Maksas iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-155">Rēķinā neiekļautās pārdošanas atsaukšana maksas summai sākotnējā žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-156">Rēķinā iekļautās pārdošanas faktiskie dati daudzumam un summai sākotnējā maksas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6e53f-157">Atskaites punkta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-158">Rēķinā iekļautās pārdošanas faktiskie dati atskaites punkta summai sākotnējā atskaites punktā projekta līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="6e53f-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6e53f-159">Rēķina izrakstīšana projekta līguma rindai.</span><span class="sxs-lookup"><span data-stu-id="6e53f-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6e53f-160">Rēķinā iekļautas pārdošanas faktiskie dati produkta rindai ar daudzumu un summu, kas iegūta no produkta līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="6e53f-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
