---
title: Labotie rēķini — Lite
description: Šajā tēmā ir sniegta informācija par labotiem rēķiniem projekta operācijās.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274242"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="4a192-103">Labotie rēķini — Lite</span><span class="sxs-lookup"><span data-stu-id="4a192-103">Corrected invoices - lite</span></span>

<span data-ttu-id="4a192-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="4a192-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4a192-105">Apstiprinātu projekta rēķinu var labot, lai apstrādātu izmaiņas vai kredītus pēc pārrunām ar klientu un projekta vadītāju.</span><span class="sxs-lookup"><span data-stu-id="4a192-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="4a192-106">Lai veiktu labojumus apstiprinātā rēķinā, atveriet apstiprināto rēķinu un atlasiet opciju **Labot šo rēķinu**.</span><span class="sxs-lookup"><span data-stu-id="4a192-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="4a192-107">Šī atlase nav pieejama, ja vien nav apstiprināts projekta rēķins.</span><span class="sxs-lookup"><span data-stu-id="4a192-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="4a192-108">No apstiprinātā rēķina tiek izveidots jauns rēķina melnraksts.</span><span class="sxs-lookup"><span data-stu-id="4a192-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="4a192-109">Visa rēķina rindu informācija no iepriekš apstiprināta rēķina tiek iekopēta jaunajā melnrakstā.</span><span class="sxs-lookup"><span data-stu-id="4a192-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="4a192-110">Lūk, daži no galvenajiem punktiem, lai izprastu rindu informāciju jaunajā labotajā rēķinā:</span><span class="sxs-lookup"><span data-stu-id="4a192-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="4a192-111">Visi daudzumi tiek atjaunināti uz nulli.</span><span class="sxs-lookup"><span data-stu-id="4a192-111">All quantities are updated to zero.</span></span> <span data-ttu-id="4a192-112">Lietojumprogramma pieņem, ka visi rēķinā iekļautie elementi tiek pilnībā kreditēti.</span><span class="sxs-lookup"><span data-stu-id="4a192-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="4a192-113">Ja nepieciešams, šos daudzumus var atjaunināt manuāli, lai atspoguļotu daudzumu, kam izrakstīts rēķins, nevis to daudzumu, kas tiek kreditēts.</span><span class="sxs-lookup"><span data-stu-id="4a192-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="4a192-114">Pamatojoties uz ievadīto daudzumu, lietojumprogramma aprēķina kreditēto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="4a192-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="4a192-115">Šī summa tiek atspoguļota faktiskajos datos, kas tiek izveidoti, kad tiek apstiprināts pareizais rēķins.</span><span class="sxs-lookup"><span data-stu-id="4a192-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="4a192-116">Ja veicat izmaiņas nodokļu summā, ir jāievada atbilstošā nodokļu summa, nevis kreditētā nodokļu summa.</span><span class="sxs-lookup"><span data-stu-id="4a192-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="4a192-117">Iepriekš apstiprinātas ar produktu saistītas līguma rindas netiek pārkopētas.</span><span class="sxs-lookup"><span data-stu-id="4a192-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="4a192-118">Netiek atbalstīta korekciju apstrādi, izmantojot produkta projekta rēķinu.</span><span class="sxs-lookup"><span data-stu-id="4a192-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="4a192-119">Pagrieziena punktu korekcijas vienmēr tiek apstrādātas kā pilni kredīti.</span><span class="sxs-lookup"><span data-stu-id="4a192-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="4a192-120">Honorārus vai avansa summas var labot, ja klientam izrakstīts rēķins par nepareizu summu.</span><span class="sxs-lookup"><span data-stu-id="4a192-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="4a192-121">Honorāru un avansu saskaņošanu var labot, ja ir izmantota nepareiza summa, lai salīdzinātu ar iepriekš apstiprināta rēķina maksu.</span><span class="sxs-lookup"><span data-stu-id="4a192-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a192-122">Rēķina rindas informācija, kas ir korekcija citām jau rēķinā izrakstītām izmaksām, kam lauks **Korekcija** ir iestatīts uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4a192-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="4a192-123">Rēķiniem, kam ir labotas rēķina rindas detaļas, ir lauks **Ir labojumi**, kas arī ir iestatīts uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4a192-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="4a192-124">Faktiskie dati, kas izveidoti, apstiprinot labotu rēķinu:</span><span class="sxs-lookup"><span data-stu-id="4a192-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="4a192-125">Tālāk ir sniegti faktiskie dati, ko izveidoja lietojumprogramma pēc labojuma apstiprināšanas, balstoties uz operācijām, kas veiktas labotā rēķina melnrakstā pirms apstiprināšanas.</span><span class="sxs-lookup"><span data-stu-id="4a192-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="4a192-126">
                    <strong>Scenārijs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4a192-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="4a192-127">
                    <strong>Pēc apstiprināšanas izveidotie faktiskie dati</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4a192-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="4a192-128">Apstipriniet izrakstīta avansa vai honorāra korekciju.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4a192-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-129">Rēķinā neiekļautās pārdošanas atsaukšana honorāram vai avansam, kas tika izveidots saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="4a192-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="4a192-130">Šī summa ir pozitīva, jo tā ir paredzēta, lai atceltu negatīvo summu, kas tika izveidota tad, kad tika izrakstīts rēķins par honorāru vai avansu.</span><span class="sxs-lookup"><span data-stu-id="4a192-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-131">Rēķinā iekļautās pārdošanas atsaukšanas faktiskie dati tiek izveidoti par summu honorārā vai avansā, lai atsauktu sākotnējo rēķinā iekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="4a192-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-132">Tiek izveidoti jauni rēķinā iekļautās pārdošanas faktiskie dati ar labotu summu honorāra vai avansa labotajā rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="4a192-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-133">Rēķinā neiekļautas pārdošanas faktiskie dati par negatīvu summu labotām honorāra vai avansa rēķina rindām, kas tiks izmantotas saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="4a192-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="4a192-134">Iepriekš saskaņota honorāra vai avansa labošanas apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="4a192-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-135">Rēķinā neiekļautās pārdošanas atsaukšana honorāram vai avansam, kas tika izveidots saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="4a192-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="4a192-136">Šī summa ir pozitīva un ir paredzēta, lai atceltu negatīvo summu, kas tika izveidota tad, kad notika iepriekšējā saskaņošana.</span><span class="sxs-lookup"><span data-stu-id="4a192-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-137">Rēķinā iekļautās pārdošanas atsaukšanas faktiskie dati par summu iepriekšējā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4a192-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-138">Tiek izveidoti jauni rēķinā iekļautās pārdošanas faktiskie dati ar labotu honorāra summu, kas tiek izmantota labotajā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4a192-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-139">Rēķinā neiekļautas pārdošanas faktiskie dati ar negatīvu summu no labotā atlikušā honorāra vai avansa, kas tiks izmantots saskaņošanai turpmākos rēķinos.</span><span class="sxs-lookup"><span data-stu-id="4a192-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4a192-140">Pilna iepriekš rēķinā izrakstīta laika darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4a192-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-141">Rēķinā iekļautās pārdošanas atsaukšana stundām un summai sākotnējā rēķina rindā laikam.</span><span class="sxs-lookup"><span data-stu-id="4a192-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-142">Rēķinā neiekļautās pārdošanas faktiskie dati par stundām un summu sākotnējā rēķina rindā laikam.</span><span class="sxs-lookup"><span data-stu-id="4a192-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4a192-143">Daļēja kredīta iekļaušana rēķinā par laika darījumu.</span><span class="sxs-lookup"><span data-stu-id="4a192-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-144">Rēķinā iekļautās pārdošanas atsaukšana stundām un summai, kas iekļauta sākotnējā rēķina rindā laikam.</span><span class="sxs-lookup"><span data-stu-id="4a192-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-145">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa stundām un summu rediģētā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="4a192-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-146">Jaunas rēķinā neiekļautas pārdošanas faktiskie dati, kas ir iekasējama par atlikušajām stundām un summu pēc laboto summu atvilkšanas rēķina rindu informācijā.</span><span class="sxs-lookup"><span data-stu-id="4a192-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4a192-147">Pilna iepriekš rēķinā izrakstīta izdevumu darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4a192-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-148">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="4a192-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-149">Jaunas rēķinā neiekļautās pārdošanas faktiskie dati par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="4a192-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4a192-150">Daļēja iepriekš rēķinā izrakstīta izdevumu darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4a192-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-151">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā par izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="4a192-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-152">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa daudzumu un summu labotā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="4a192-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-153">Jaunas rēķinā neiekļautas pārdošanas faktiskie dati, kas ir iekasējama par atlikušo daudzumu un summu pēc laboto summu atvilkšanas rēķina rindu informācijā.</span><span class="sxs-lookup"><span data-stu-id="4a192-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4a192-154">Pilna iepriekš rēķinā izrakstīta maksas darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4a192-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-155">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā maksai.</span><span class="sxs-lookup"><span data-stu-id="4a192-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-156">Jaunas rēķinā neiekļautās pārdošanas faktiskie dati par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā maksai.</span><span class="sxs-lookup"><span data-stu-id="4a192-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4a192-157">Daļēja iepriekš rēķinā izrakstīta maksas darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4a192-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-158">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā par maksu.</span><span class="sxs-lookup"><span data-stu-id="4a192-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-159">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa daudzumu un summu rediģētā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="4a192-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4a192-160">Pilna iepriekš rēķinā izrakstīta atskaites punkta kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4a192-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-161">Rēķinā iekļautās pārdošanas atsaukšana summai sākotnējā rēķina rindā atskaites punktam.</span><span class="sxs-lookup"><span data-stu-id="4a192-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="4a192-162">Projekta līguma rindā ietvertā atskaites punkta rēķins vai norēķinu statuss tiek atjaunināts uz **Gatavs rēķina izrakstīšanai**.</span><span class="sxs-lookup"><span data-stu-id="4a192-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4a192-163">Daļēja iepriekš rēķinā izrakstīta atskaites punkta kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4a192-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-164">Neatbalsta</span><span class="sxs-lookup"><span data-stu-id="4a192-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4a192-165">Kredīti un labojumi, kas iepriekš rēķinā iekļauti produkta līguma rindā.</span><span class="sxs-lookup"><span data-stu-id="4a192-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4a192-166">Neatbalsta</span><span class="sxs-lookup"><span data-stu-id="4a192-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]