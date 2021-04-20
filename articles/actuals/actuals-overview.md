---
title: Pašreizējās
description: Šajā tēmā ir sniegta informācija par to, kā veikt darbības ar faktiskajiem darbiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852553"
---
# <a name="actuals"></a><span data-ttu-id="dd534-103">Faktiskie dati</span><span class="sxs-lookup"><span data-stu-id="dd534-103">Actuals</span></span> 

<span data-ttu-id="dd534-104">_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="dd534-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dd534-105">Faktiskie dati attiecas uz pārskatīto un apstiprināto finanšu un plānošanas norisi projektā.</span><span class="sxs-lookup"><span data-stu-id="dd534-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="dd534-106">Tās tiek izveidotas laika, izmaksu, materiālu lietojuma ierakstu, kā arī ierakstu un rēķinu apstiprinājuma rezultātā.</span><span class="sxs-lookup"><span data-stu-id="dd534-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="dd534-107">Žurnāla rindu un laika iesniegšana</span><span class="sxs-lookup"><span data-stu-id="dd534-107">Journal lines and time submission</span></span>

<span data-ttu-id="dd534-108">Papildinformāciju par laika ievadīšanu skatiet šeit: [Laika ieraksta pārskats](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dd534-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="dd534-109">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="dd534-109">Time and materials</span></span>

<span data-ttu-id="dd534-110">Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="dd534-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="dd534-111">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="dd534-111">Fixed price</span></span>

<span data-ttu-id="dd534-112">Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz fiksētas cenas līguma rindu, sistēma izveido vienu žurnāla rindu – par izmaksām.</span><span class="sxs-lookup"><span data-stu-id="dd534-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="dd534-113">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="dd534-113">Default pricing</span></span>

<span data-ttu-id="dd534-114">Noklusējuma cenu izveides loģika atrodas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="dd534-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="dd534-115">Lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="dd534-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="dd534-116">Šajās vērtībās ir iekļauts darījuma datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.</span><span class="sxs-lookup"><span data-stu-id="dd534-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="dd534-117">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Resursu vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="dd534-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="dd534-118">Varat pievienot pielāgotu lauku laika ierakstam.</span><span class="sxs-lookup"><span data-stu-id="dd534-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="dd534-119">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="dd534-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="dd534-120">Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="dd534-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="dd534-121">Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="dd534-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="dd534-122">Žurnāla rindu un pamata izdevumu iesniegšana</span><span class="sxs-lookup"><span data-stu-id="dd534-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="dd534-123">Papildinformāciju par izdevumu ievadīšanu skatiet šeit: [Izdevumu pārskats](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dd534-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="dd534-124">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="dd534-124">Time and materials</span></span>

<span data-ttu-id="dd534-125">Kad iesniegts pamata izdevumu ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="dd534-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="dd534-126">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="dd534-126">Fixed price</span></span>

<span data-ttu-id="dd534-127">Kad iesniegtais pamata izdevumu ieraksts tiek saistīts ar projektu, kas ir kartēts fiksētas cenas līguma rindā, sistēma izveido vienu žurnāla rindu cenai.</span><span class="sxs-lookup"><span data-stu-id="dd534-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="dd534-128">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="dd534-128">Default pricing</span></span>

<span data-ttu-id="dd534-129">Izdevumu noklusējuma cenu ievadīšanas loģikas pamatā ir izdevumu kategorija.</span><span class="sxs-lookup"><span data-stu-id="dd534-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="dd534-130">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="dd534-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="dd534-131">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Transakcijas kategorija** un **Vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="dd534-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="dd534-132">Tomēr tas darbojas tikai tad, ja cenrāža cenu noteikšanas metode ir **Cena par vienību**.</span><span class="sxs-lookup"><span data-stu-id="dd534-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="dd534-133">Ja cenu noteikšanas metode ir **Pašizmaksa** vai **Uzcenojums augstāks par izmaksu**, izmaksu ieraksta izveides laikā ievadītā cena tiek izmantota izmaksām, un cena pārdošanas piedāvājuma rindā tiek aprēķināta, pamatojoties uz cenu noteikšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="dd534-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="dd534-134">Izmaksu ierakstam var pievienot pielāgotu lauku.</span><span class="sxs-lookup"><span data-stu-id="dd534-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="dd534-135">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="dd534-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="dd534-136">Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="dd534-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="dd534-137">Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="dd534-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="dd534-138">Žurnāla rindu un materiālu lietojuma žurnāla iesniegšana</span><span class="sxs-lookup"><span data-stu-id="dd534-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="dd534-139">Papildinformāciju par izdevumu ierakstu skatiet šeit: [Materiālu lietojuma žurnāls](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="dd534-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="dd534-140">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="dd534-140">Time and materials</span></span>

<span data-ttu-id="dd534-141">Kad iesniegts materiālu lietojuma žurnāls ieraksts tiek saistīts ar projektu, kas tiek kartēts ar laika un materiālu līguma rindu, sistēma izveido divas rindu rindas (vienu par izmaksām un vienu par rēķinā neietverto pārdošanu).</span><span class="sxs-lookup"><span data-stu-id="dd534-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="dd534-142">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="dd534-142">Fixed price</span></span>

<span data-ttu-id="dd534-143">Kad iesniegtais materiālu lietojuma ieraksts tiek saistīts ar projektu, kas ir kartēts fiksētas cenas līguma rindā, sistēma izveido vienu žurnāla rindu cenai.</span><span class="sxs-lookup"><span data-stu-id="dd534-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="dd534-144">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="dd534-144">Default pricing</span></span>

<span data-ttu-id="dd534-145">Materiālu noklusējuma cenu ievadīšanas loģika tiek pamatota uz produktu un vienību kombināciju.</span><span class="sxs-lookup"><span data-stu-id="dd534-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="dd534-146">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="dd534-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="dd534-147">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Produkta ID** un **Vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="dd534-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="dd534-148">Tomēr tas darbojas tikai kataloga produktiem.</span><span class="sxs-lookup"><span data-stu-id="dd534-148">However, this only works for catalog products.</span></span> <span data-ttu-id="dd534-149">Ierakstāmiem produktiem cena, kas ievadīta, izveidojot materiālu lietojuma žurnāla ierakstu, tiek izmantota izmaksu un pārdošanas cenai raksta rindās.</span><span class="sxs-lookup"><span data-stu-id="dd534-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="dd534-150">Ierakstam **Materiālu lietojuma žurnāls** var pievienot pielāgotu lauku.</span><span class="sxs-lookup"><span data-stu-id="dd534-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="dd534-151">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="dd534-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="dd534-152">Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="dd534-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="dd534-153">Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="dd534-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="dd534-154">Ierakstu žurnālu izmantošana izmaksu reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="dd534-154">Use entry journals to record costs</span></span>

<span data-ttu-id="dd534-155">Varat izmantot ierakstu žurnālus, lai ierakstītu izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs.</span><span class="sxs-lookup"><span data-stu-id="dd534-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="dd534-156">Žurnālus var izmantot šādiem mērķiem:</span><span class="sxs-lookup"><span data-stu-id="dd534-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="dd534-157">Pārvietojiet transakciju faktiskos datus no citas sistēmas uz Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="dd534-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="dd534-158">Reģistrēt izmaksas, kas notikušas citā sistēmā.</span><span class="sxs-lookup"><span data-stu-id="dd534-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="dd534-159">Šīs izmaksas var ietvert iegādes vai apakšuzņēmēju izmaksas.</span><span class="sxs-lookup"><span data-stu-id="dd534-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd534-160">Programma nevalidē žurnāla rindas tipu vai saistīto cenu, kas ievadīta žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="dd534-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="dd534-161">Tādējādi ierakstu žurnālus izmantot faktisko datu izveidei drīkst tikai lietotājs, kas pilnībā apzinās faktisko datu ietekmi uz projekta uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="dd534-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="dd534-162">Šī žurnāla veida ietekmes dēļ jums rūpīgi jāizvēlas personas, kurām ir piekļuve ierakstu žurnālu izveidei.</span><span class="sxs-lookup"><span data-stu-id="dd534-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="dd534-163">Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem</span><span class="sxs-lookup"><span data-stu-id="dd534-163">Record actuals based on project events</span></span>

<span data-ttu-id="dd534-164">Project Operations ieraksta finanšu transakcijas, kas notiek projekta laikā.</span><span class="sxs-lookup"><span data-stu-id="dd534-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="dd534-165">Šīs transakcijas tiek ierakstītas kā faktiskie dati.</span><span class="sxs-lookup"><span data-stu-id="dd534-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="dd534-166">Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.</span><span class="sxs-lookup"><span data-stu-id="dd534-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="dd534-167">Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="dd534-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="dd534-168">Notikums</span><span class="sxs-lookup"><span data-stu-id="dd534-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="dd534-169">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="dd534-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="dd534-170">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="dd534-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="dd534-171">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="dd534-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="dd534-172">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="dd534-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="dd534-173">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="dd534-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="dd534-174">Faktiski</span><span class="sxs-lookup"><span data-stu-id="dd534-174">Actuals</span></span></th>
<th><span data-ttu-id="dd534-175">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-175">Transaction currency</span></span></th>
<th><span data-ttu-id="dd534-176">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="dd534-176">Fixed price</span></span></th>
<th><span data-ttu-id="dd534-177">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd534-178">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="dd534-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="dd534-179">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="dd534-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-180">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="dd534-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="dd534-181">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="dd534-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="dd534-182">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="dd534-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="dd534-183">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-183">Cost actual</span></span></td>
<td><span data-ttu-id="dd534-184">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-185">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-186">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="dd534-187">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-188">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-189">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="dd534-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="dd534-190">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="dd534-191">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="dd534-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="dd534-192">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-192">Cost actual</span></span></td>
<td><span data-ttu-id="dd534-193">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-194">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-195">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-196">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-197">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-198">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="dd534-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="dd534-199">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-200">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="dd534-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd534-201">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="dd534-202">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="dd534-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="dd534-203">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="dd534-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="dd534-204">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-205">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="dd534-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-206">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-207">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-208">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-209">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="dd534-209">Billed sales</span></span></td>
<td><span data-ttu-id="dd534-210">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="dd534-211">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="dd534-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="dd534-212">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="dd534-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="dd534-213">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-214">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-215">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-216">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-217">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-218">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="dd534-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="dd534-219">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-220">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="dd534-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd534-221">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="dd534-222">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="dd534-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="dd534-223">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="dd534-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="dd534-224">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="dd534-225">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="dd534-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="dd534-226">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="dd534-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="dd534-227">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="dd534-228">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="dd534-229">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-230">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="dd534-230">Billed sales</span></span></td>
<td><span data-ttu-id="dd534-231">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="dd534-232">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="dd534-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="dd534-233">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="dd534-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="dd534-234">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-235">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="dd534-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="dd534-236">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-237">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="dd534-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd534-238">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="dd534-239">Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības</span><span class="sxs-lookup"><span data-stu-id="dd534-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="dd534-240">Notikums</span><span class="sxs-lookup"><span data-stu-id="dd534-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="dd534-241">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="dd534-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="dd534-242">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="dd534-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="dd534-243">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="dd534-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="dd534-244">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="dd534-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="dd534-245">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="dd534-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="dd534-246">Faktiski</span><span class="sxs-lookup"><span data-stu-id="dd534-246">Actuals</span></span></th>
<th><span data-ttu-id="dd534-247">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-247">Transaction currency</span></span></th>
<th><span data-ttu-id="dd534-248">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="dd534-248">Fixed price</span></span></th>
<th><span data-ttu-id="dd534-249">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd534-250">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="dd534-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="dd534-251">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="dd534-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-252">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="dd534-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="dd534-253">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="dd534-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="dd534-254">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="dd534-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="dd534-255">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-255">Cost actual</span></span></td>
<td><span data-ttu-id="dd534-256">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="dd534-257">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="dd534-258">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="dd534-259">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="dd534-260">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-261">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="dd534-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="dd534-262">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-263">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="dd534-264">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-265">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="dd534-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="dd534-266">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="dd534-267">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="dd534-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="dd534-268">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-268">Cost actual</span></span></td>
<td><span data-ttu-id="dd534-269">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="dd534-270">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="dd534-271">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="dd534-272">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="dd534-273">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-274">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="dd534-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="dd534-275">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-276">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="dd534-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="dd534-277">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-278">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="dd534-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="dd534-279">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-280">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="dd534-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd534-281">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="dd534-282">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="dd534-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="dd534-283">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="dd534-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="dd534-284">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-285">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="dd534-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-286">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-287">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="dd534-288">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-289">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="dd534-289">Billed sales</span></span></td>
<td><span data-ttu-id="dd534-290">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="dd534-291">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="dd534-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="dd534-292">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="dd534-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="dd534-293">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-294">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-295">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-296">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd534-297">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-298">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="dd534-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="dd534-299">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-300">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="dd534-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd534-301">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="dd534-302">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="dd534-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="dd534-303">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="dd534-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="dd534-304">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="dd534-305">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="dd534-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="dd534-306">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="dd534-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="dd534-307">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="dd534-308">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="dd534-309">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="dd534-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-310">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="dd534-310">Billed sales</span></span></td>
<td><span data-ttu-id="dd534-311">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="dd534-312">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="dd534-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="dd534-313">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="dd534-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="dd534-314">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-315">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="dd534-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="dd534-316">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd534-317">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="dd534-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd534-318">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="dd534-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
