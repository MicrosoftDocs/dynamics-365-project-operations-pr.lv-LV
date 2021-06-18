---
title: Labojošu projektā balstītu rēķinu izveide
description: Šajā tēmā ir sniegta informācija par labojošiem rēķiniem programmā Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001630"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="fcb7d-103">Labojošu projektā balstītu rēķinu izveide</span><span class="sxs-lookup"><span data-stu-id="fcb7d-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="fcb7d-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="fcb7d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fcb7d-105">Apstiprinātu projekta rēķinu var labot, lai apstrādātu izmaiņas vai kredītus pēc pārrunām ar klientu un projekta vadītāju.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="fcb7d-106">Lai veiktu labojumus apstiprinātā rēķinā, atveriet apstiprināto rēķinu un atlasiet opciju **Labot šo rēķinu**.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="fcb7d-107">Šī atlase nav pieejama, ja vien nav apstiprināts projekta rēķins.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="fcb7d-108">No apstiprinātā rēķina tiek izveidots jauns rēķina melnraksts.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="fcb7d-109">Visa rēķina rindu informācija no iepriekš apstiprināta rēķina tiek iekopēta jaunajā melnrakstā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="fcb7d-110">Tālāk ir apskatīti daži galvenie punkti, kas palīdzēs saprast papildinformāciju par rindas informāciju jaunajā labotajā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="fcb7d-111">Visi daudzumi tiek atjaunināti uz nulli.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-111">All quantities are updated to zero.</span></span> <span data-ttu-id="fcb7d-112">Tiek pieņemts, ka visi rēķinā iekļautie elementi tiek pilnībā kreditēti.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="fcb7d-113">Ja nepieciešams, šos daudzumus var atjaunināt manuāli, lai atspoguļotu daudzumu, kam izrakstīts rēķins, nevis to daudzumu, kas tiek kreditēts.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="fcb7d-114">Pamatojoties uz ievadīto daudzumu, lietojumprogramma aprēķina kreditēto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="fcb7d-115">Šī summa tiek atspoguļota faktiskajos datos, kas tiek izveidoti, kad tiek apstiprināts pareizais rēķins.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="fcb7d-116">Ja veicat izmaiņas nodokļu summā, ir jāievada atbilstošā nodokļu summa, nevis kreditētā nodokļu summa.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="fcb7d-117">Pagrieziena punktu korekcijas vienmēr tiek apstrādātas kā pilni kredīti.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="fcb7d-118">Honorārus vai avansa summas var labot, ja klientam izrakstīts rēķins par nepareizu summu.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="fcb7d-119">Honorāru un avansu saskaņošanu var labot, ja ir izmantota nepareiza summa, lai salīdzinātu ar iepriekš apstiprināta rēķina maksu.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fcb7d-120">Rēķina rindas informācijai, kas ir labojumi citās jau iekļautās rēķinā iekļautās izmaksās, lauks **Labojums** ir iestatīts **Jā**.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="fcb7d-121">Rēķiniem, kam ir labotas rēķina rindas detaļas, ir lauks **Ir labojumi**, kas arī ir iestatīts uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="fcb7d-122">Faktiskie dati, kas izveidoti, apstiprinot labotu rēķinu</span><span class="sxs-lookup"><span data-stu-id="fcb7d-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="fcb7d-123">Tālāk sniegtajā tabulā ir uzskaitīti faktiskie dati, kas tiek izveidoti, apstiprinot labojošo rēķinu.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="fcb7d-124">
                    <strong>Scenārijs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fcb7d-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="fcb7d-125">
                    <strong>Pēc apstiprināšanas izveidotie faktiskie dati</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fcb7d-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="fcb7d-126">Apstipriniet izrakstīta avansa vai honorāra korekciju.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fcb7d-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-127">Rēķinā neiekļautās pārdošanas atsaukšana honorāram vai avansam, kas tika izveidots saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="fcb7d-128">Šī summa ir pozitīva, jo tā ir paredzēta, lai atceltu negatīvo summu, kas tika izveidota tad, kad tika izrakstīts rēķins par honorāru vai avansu.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-129">Rēķinā iekļautās pārdošanas atsaukšanas faktiskie dati tiek izveidoti par summu honorārā vai avansā, lai atsauktu sākotnējo rēķinā iekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-130">Tiek izveidoti jauni rēķinā iekļautās pārdošanas faktiskie dati ar labotu summu honorāra vai avansa labotajā rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-131">Rēķinā neiekļautas pārdošanas faktiskie dati par negatīvu summu labotām honorāra vai avansa rēķina rindām, kas tiks izmantotas saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="fcb7d-132">Iepriekš saskaņota honorāra vai avansa labošanas apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-133">Rēķinā neiekļautās pārdošanas atsaukšana honorāram vai avansam, kas tika izveidots saskaņošanai.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="fcb7d-134">Šī summa ir pozitīva un ir paredzēta, lai atceltu negatīvo summu, kas tika izveidota tad, kad notika iepriekšējā saskaņošana.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-135">Rēķinā iekļautās pārdošanas atsaukšanas faktiskie dati par summu iepriekšējā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-136">Tiek izveidoti jauni rēķinā iekļautās pārdošanas faktiskie dati ar labotu honorāra summu, kas tiek izmantota labotajā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-137">Rēķinā neiekļautas pārdošanas faktiskie dati ar negatīvu summu no labotā atlikušā honorāra vai avansa, kas tiks izmantots saskaņošanai turpmākos rēķinos.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fcb7d-138">Pilna iepriekš rēķinā izrakstīta laika darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-139">Rēķinā iekļautās pārdošanas atsaukšana stundām un summai sākotnējā rēķina rindā laikam.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-140">Rēķinā neiekļautās pārdošanas faktiskie dati par stundām un summu sākotnējā rēķina rindā laikam.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="fcb7d-141">Daļēja kredīta iekļaušana rēķinā par laika darījumu.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-142">Rēķinā iekļautās pārdošanas atsaukšana stundām un summai, kas iekļauta sākotnējā rēķina rindā laikam.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-143">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa stundām un summu rediģētā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-144">Jaunas rēķinā neiekļautas pārdošanas faktiskie dati, kas ir iekasējama par atlikušajām stundām un summu pēc laboto summu atvilkšanas rēķina rindu informācijā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fcb7d-145">Pilna iepriekš rēķinā izrakstīta izdevumu darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-146">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-147">Jaunas rēķinā neiekļautās pārdošanas faktiskie dati par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="fcb7d-148">Daļēja iepriekš rēķinā izrakstīta izdevumu darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-149">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā par izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-150">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa daudzumu un summu labotā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-151">Jaunas rēķinā neiekļautas pārdošanas faktiskie dati, kas ir iekasējama par atlikušo daudzumu un summu pēc laboto summu atvilkšanas rēķina rindu informācijā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fcb7d-152">Pilna iepriekš rēķinā izrakstīta maksas darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-153">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā maksai.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-154">Jaunas rēķinā neiekļautās pārdošanas faktiskie dati par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā maksai.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fcb7d-155">Daļēja iepriekš rēķinā izrakstīta maksas darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-156">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā par maksu.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-157">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa daudzumu un summu rediģētā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="fcb7d-158">Pilna iepriekš rēķinā izrakstīta atskaites punkta kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-159">Rēķinā iekļautās pārdošanas atsaukšana summai sākotnējā rēķina rindā atskaites punktam.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="fcb7d-160">Rēķina statuss atskaites punktā tiek atjaunināts no <b>Klienta rēķins iegrāmatots</b> uz <b>Gatavs rēķina izrakstīšanai</b>.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="fcb7d-161">Daļēja iepriekš rēķinā izrakstīta atskaites punkta kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="fcb7d-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="fcb7d-162">Neatbalsta</span><span class="sxs-lookup"><span data-stu-id="fcb7d-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
