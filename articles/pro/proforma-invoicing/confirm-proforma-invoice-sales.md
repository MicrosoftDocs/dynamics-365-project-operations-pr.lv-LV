---
title: Pro formas rēķinu apstiprināšana — Lite
description: Šajā tēmā ir sniegta informācija par proforma rēķinu apstiprināšanu risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176530"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="69ee9-103">Pro formas rēķinu apstiprināšana — Lite</span><span class="sxs-lookup"><span data-stu-id="69ee9-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="69ee9-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="69ee9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="69ee9-105">Pēc tam, kad ir apstiprināts proforma rēķins, projekta rēķina statuss tiek atjaunināts uz **Apstiprināts**.</span><span class="sxs-lookup"><span data-stu-id="69ee9-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="69ee9-106">Kad rēķins ir apstiprināts, tas kļūst tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="69ee9-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="69ee9-107">Turpmāk rēķinu varēs labot tikai tad, ja pastāvēs klienta iniciēti labojumi vai kredīti vai arī rēķins būs atzīmēts kā apmaksāts.</span><span class="sxs-lookup"><span data-stu-id="69ee9-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="69ee9-108">Tālāk sniegtajā tabulā ir uzskaitīti sistēmā izveidotie faktiskie dati.</span><span class="sxs-lookup"><span data-stu-id="69ee9-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="69ee9-109">Šie faktiskie dati tiek izveidoti, kad projekta rēķina melnrakstā pirms apstiprināšanas tiek veiktas noteiktas darbības.</span><span class="sxs-lookup"><span data-stu-id="69ee9-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="69ee9-110">
                    <strong>Scenārijs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69ee9-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="69ee9-111">
                    <strong>Pēc apstiprināšanas izveidotie faktiskie dati</strong>
                </span><span class="sxs-lookup"><span data-stu-id="69ee9-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69ee9-112">Rēķina izrakstīšana par honorāru vai avansu</span><span class="sxs-lookup"><span data-stu-id="69ee9-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-113">Rēķinā iekļautas pārdošanas faktiskie dati ar tipu <strong>Honorārs</strong> tiek izveidoti par avansa vai honorāra summu.</span><span class="sxs-lookup"><span data-stu-id="69ee9-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-114">Rēķinā neiekļautas pārdošanas faktiskie dati par negatīvu summu honorāram vai avansam, kas tiks izmantota saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="69ee9-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69ee9-115">Pēc honorāra vai avansa pilnīgas saskaņošanas rēķinā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-116">Rēķinā neiekļautās pārdošanas atsaukšana honorāram vai avansam, kas tika izveidots saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="69ee9-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="69ee9-117">Šī summa ir pozitīva, jo tā ir paredzēta, lai atceltu negatīvo summu, kas tika izveidota tad, kad tika izrakstīts rēķins par honorāru vai avansu.</span><span class="sxs-lookup"><span data-stu-id="69ee9-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-118">Rēķinā iekļautās pārdošanas faktiskie dati par summu šajā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="69ee9-119">Pēc honorāra vai avansa daļējas saskaņošanas rēķinā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-120">Rēķinā neiekļautās pārdošanas atsaukšana honorāram vai avansam, kas tika izveidots saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="69ee9-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="69ee9-121">Šī summa ir pozitīva, jo tā ir paredzēta, lai atceltu negatīvo summu, kas tika izveidota tad, kad tika izrakstīts rēķins par honorāru vai avansu.</span><span class="sxs-lookup"><span data-stu-id="69ee9-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-122">Rēķinā iekļautās pārdošanas faktiskie dati par summu šajā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-123">Negatīva rēķinā neiekļautas pārdošanas faktiskā summa no atlikušā honorāra vai avansa summas, kas tiks izmantota saskaņošanai turpmākos rēķinos.</span><span class="sxs-lookup"><span data-stu-id="69ee9-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69ee9-124">Rēķina izveide laika darījumam bez labojumiem rēķina melnrakstā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-125">Rēķinā neiekļautās pārdošanas atsaukšana stundām un summai sākotnējā laika apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-126">Rēķinā iekļautās pārdošanas faktiskie dati stundām un summai sākotnējā laika apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="69ee9-127">Rēķina izveide laika darījumam, kas tika rediģēts, lai samazinātu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="69ee9-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-128">Rēķinā neiekļautās pārdošanas atsaukšana stundām un summai sākotnējā laika apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-129">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa stundām un summu rediģētā rēķina rindu informācijā, pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="69ee9-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-130">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas nav iekasējami par atlikušajām stundām un summu pēc laboto ciparu atvilkšanas rediģētā rēķina rindu informācijā, pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="69ee9-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69ee9-131">Rēķina izveide laika darījumam, kas tika rediģēts, lai palielinātu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="69ee9-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-132">Rēķinā neiekļautās pārdošanas atsaukšana stundām un summai sākotnējā laika apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-133">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa stundām un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="69ee9-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69ee9-134">Rēķina izveide izdevumu darījumam bez labojumiem rēķina melnrakstā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-135">Rēķinā neiekļautās pārdošanas atsaukšana daudzumam un summai sākotnējā izdevumu apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-136">Rēķinā iekļautās pārdošanas faktiskie dati daudzumam un summai sākotnējā izdevumu apstiprinājumā</span><span class="sxs-lookup"><span data-stu-id="69ee9-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="69ee9-137">Rēķina izveide izdevumu darījumam, kas tika rediģēts, lai samazinātu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="69ee9-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-138">Rēķinā neiekļautās pārdošanas atsaukšana daudzumam un summai sākotnējā izdevumu apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-139">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama par daudzumu un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="69ee9-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-140">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas nav iekasējami par atlikušo daudzumu un summu pēc laboto ciparu atvilkšanas rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="69ee9-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69ee9-141">Rēķina izveide izdevumu darījumam, kas tika rediģēts, lai palielinātu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="69ee9-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-142">Rēķinā neiekļautās pārdošanas atsaukšana daudzumam un summai sākotnējā izdevumu apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-143">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama par daudzumu un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="69ee9-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="69ee9-144">Maksas iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-145">Rēķinā neiekļautās pārdošanas atsaukšana maksas summai sākotnējā žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-146">Rēķinā iekļautās pārdošanas faktiskie dati daudzumam un summai sākotnējā maksas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="69ee9-147">Atskaites punkta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-148">Rēķinā iekļautās pārdošanas faktiskie dati atskaites punkta summai sākotnējā atskaites punktā projekta līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="69ee9-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="69ee9-149">Rēķina izrakstīšana projekta līguma rindai.</span><span class="sxs-lookup"><span data-stu-id="69ee9-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="69ee9-150">Rēķinā iekļautas pārdošanas faktiskie dati produkta rindai ar daudzumu un summu, kas iegūta no produkta līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="69ee9-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
