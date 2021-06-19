---
title: Laboti projektu rēķini
description: Šajā tēmā ir sniegta informācija par labotu rēķinu izveidi un apstiprināšanu programmā Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012280"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="97d1d-103">Laboti projektu rēķini</span><span class="sxs-lookup"><span data-stu-id="97d1d-103">Corrective project-based invoices</span></span>

<span data-ttu-id="97d1d-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="97d1d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="97d1d-105">Apstiprinātu projekta rēķinu var labot, lai apstrādātu izmaiņas vai kredītus pēc pārrunām ar klientu un projekta vadītāju.</span><span class="sxs-lookup"><span data-stu-id="97d1d-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="97d1d-106">Lai veiktu labojumus apstiprinātā rēķinā, atveriet apstiprināto rēķinu un atlasiet opciju **Labot šo rēķinu**.</span><span class="sxs-lookup"><span data-stu-id="97d1d-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="97d1d-107">Šī atlase nav pieejama, ja vien netiek apstiprināts projekta rēķins vai projekta rēķinā nav avansu vai honorāru, kā arī honorāru vai avansu saskaņošanas.</span><span class="sxs-lookup"><span data-stu-id="97d1d-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="97d1d-108">No apstiprinātā rēķina tiek izveidots jauns rēķina melnraksts.</span><span class="sxs-lookup"><span data-stu-id="97d1d-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="97d1d-109">Visa rēķina rindu informācija no iepriekš apstiprināta rēķina tiek iekopēta jaunajā melnrakstā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="97d1d-110">Lūk, daži no galvenajiem punktiem, lai izprastu rindu informāciju jaunajā labotajā rēķinā:</span><span class="sxs-lookup"><span data-stu-id="97d1d-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="97d1d-111">Visi daudzumi tiek atjaunināti uz nulli.</span><span class="sxs-lookup"><span data-stu-id="97d1d-111">All quantities are updated to zero.</span></span> <span data-ttu-id="97d1d-112">Dynamics 365 Project Operations pieņem, ka visi rēķinā iekļautie elementi tiek pilnībā kreditēti.</span><span class="sxs-lookup"><span data-stu-id="97d1d-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="97d1d-113">Ja nepieciešams, šos daudzumus var atjaunināt manuāli, lai atspoguļotu daudzumu, kam izrakstīts rēķins, nevis to daudzumu, kas tiek kreditēts.</span><span class="sxs-lookup"><span data-stu-id="97d1d-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="97d1d-114">Pamatojoties uz ievadīto daudzumu, lietojumprogramma aprēķina kreditēto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="97d1d-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="97d1d-115">Šī summa tiek atspoguļota faktiskajos datos, kas tiek izveidoti, kad tiek apstiprināts pareizais rēķins.</span><span class="sxs-lookup"><span data-stu-id="97d1d-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="97d1d-116">Ja veicat izmaiņas nodokļu summā, ir jāievada atbilstošā nodokļu summa, nevis kreditētā nodokļu summa.</span><span class="sxs-lookup"><span data-stu-id="97d1d-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="97d1d-117">Pagrieziena punktu korekcijas vienmēr tiek apstrādātas kā pilni kredīti.</span><span class="sxs-lookup"><span data-stu-id="97d1d-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="97d1d-118">Rēķina rindas informācijai, kas ir labojumi citās jau iekļautās rēķinā iekļautās izmaksās, lauks **Labojums** ir iestatīts **Jā**.</span><span class="sxs-lookup"><span data-stu-id="97d1d-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="97d1d-119">Rēķiniem ar labotu rindas informāciju lauks **Ir labojumi** ir iestatīts **Jā**.</span><span class="sxs-lookup"><span data-stu-id="97d1d-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="97d1d-120">Faktiskie dati, kas izveidoti, apstiprinot labotu rēķinu</span><span class="sxs-lookup"><span data-stu-id="97d1d-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="97d1d-121">Tālāk sniegtajā tabulā ir uzskaitīti faktiskie dati, kas tiek izveidoti, apstiprinot labojošo rēķinu.</span><span class="sxs-lookup"><span data-stu-id="97d1d-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="97d1d-122">
                    <strong>Scenārijs</strong>
                </span><span class="sxs-lookup"><span data-stu-id="97d1d-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="97d1d-123">
                    <strong>Pēc apstiprināšanas izveidotie faktiskie dati</strong>
                </span><span class="sxs-lookup"><span data-stu-id="97d1d-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="97d1d-124">Pilna iepriekš rēķinā izrakstīta laika darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-125">Rēķinā iekļautās pārdošanas atsaukšana stundām un summai sākotnējā rēķina rindā laikam.</span><span class="sxs-lookup"><span data-stu-id="97d1d-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-126">Rēķinā neiekļautās pārdošanas faktiskie dati par stundām un summu sākotnējā rēķina rindā laikam.</span><span class="sxs-lookup"><span data-stu-id="97d1d-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="97d1d-127">Daļēja kredīta iekļaušana rēķinā par laika darījumu.</span><span class="sxs-lookup"><span data-stu-id="97d1d-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-128">Rēķinā iekļautās pārdošanas atsaukšana stundām un summai, kas iekļauta sākotnējā rēķina rindā laikam.</span><span class="sxs-lookup"><span data-stu-id="97d1d-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-129">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa stundām un summu rediģētā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="97d1d-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-130">Jaunas rēķinā neiekļautas pārdošanas faktiskie dati, kas ir iekasējama par atlikušajām stundām un summu pēc laboto summu atvilkšanas rēķina rindu informācijā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="97d1d-131">Pilna iepriekš rēķinā izrakstīta izdevumu darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-132">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="97d1d-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-133">Jaunas rēķinā neiekļautās pārdošanas faktiskie dati par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="97d1d-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="97d1d-134">Daļēja iepriekš rēķinā izrakstīta izdevumu darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-135">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā par izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="97d1d-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-136">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa daudzumu un summu labotā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="97d1d-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-137">Jaunas rēķinā neiekļautas pārdošanas faktiskie dati, kas ir iekasējama par atlikušo daudzumu un summu pēc laboto summu atvilkšanas rēķina rindu informācijā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="97d1d-138">Rēķina izrakstīšana par pilnu kredītu iepriekš rēķinā ietvertai materiālu transakcijai.</span><span class="sxs-lookup"><span data-stu-id="97d1d-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-139">Rēķinā ietvertas pārdošanas atsaukšana par sākotnējā rēķina materiāla rindas informācijā norādīto daudzumu un summu.</span><span class="sxs-lookup"><span data-stu-id="97d1d-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-140">Jauna rēķinā neietverta pārdošanas vērtība par sākotnējā rēķina materiāla rindas informācijā norādīto daudzumu un summu.</span><span class="sxs-lookup"><span data-stu-id="97d1d-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="97d1d-141">Rēķina izrakstīšana par daļēju kredītu materiālu transakcijai.</span><span class="sxs-lookup"><span data-stu-id="97d1d-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-142">Rēķinā ietvertas pārdošanas atsaukšana par sākotnējā rēķina materiāla rindas informācijā norādīto iekasēto daudzumu un summu.</span><span class="sxs-lookup"><span data-stu-id="97d1d-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-143">Jauna rēķinā neietverta pārdošanas faktiskā vērtība, par ko var iekasēt maksu par daudzumu un summu rediģētās rēķina rindas detalizētajai informācijai, kā arī par faktisko pārdošanas apjomu, par kuru izrakstīts rēķins.</span><span class="sxs-lookup"><span data-stu-id="97d1d-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-144">Jaunas rēķinā neiekļautas pārdošanas faktiskie dati, kas ir iekasējama par atlikušo daudzumu un summu pēc laboto summu atvilkšanas rēķina rindu informācijā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="97d1d-145">Pilna iepriekš rēķinā izrakstīta maksas darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-146">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā maksai.</span><span class="sxs-lookup"><span data-stu-id="97d1d-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-147">Jaunas rēķinā neiekļautās pārdošanas faktiskie dati par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā maksai.</span><span class="sxs-lookup"><span data-stu-id="97d1d-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="97d1d-148">Daļēja iepriekš rēķinā izrakstīta maksas darījuma kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-149">Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā par maksu.</span><span class="sxs-lookup"><span data-stu-id="97d1d-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-150">Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa daudzumu un summu rediģētā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="97d1d-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="97d1d-151">Pilna iepriekš rēķinā izrakstīta atskaites punkta kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-152">Rēķinā iekļautās pārdošanas atsaukšana summai sākotnējā rēķina rindā atskaites punktam.</span><span class="sxs-lookup"><span data-stu-id="97d1d-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="97d1d-153">Rēķina statuss atskaites punktā tiek atjaunināts no <b>Klienta rēķins iegrāmatots</b> uz <b>Gatavs rēķina izrakstīšanai</b>.</span><span class="sxs-lookup"><span data-stu-id="97d1d-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="97d1d-154">Daļēja iepriekš rēķinā izrakstīta atskaites punkta kredīta iekļaušana rēķinā.</span><span class="sxs-lookup"><span data-stu-id="97d1d-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="97d1d-155">Šāds scenārijs netiek atbalstīts.</span><span class="sxs-lookup"><span data-stu-id="97d1d-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
