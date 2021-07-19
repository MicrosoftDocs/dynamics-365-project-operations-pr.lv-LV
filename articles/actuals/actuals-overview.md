---
title: Pašreizējās
description: Šajā tēmā ir sniegta informācija par to, kā veikt darbības ar faktiskajiem darbiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368620"
---
# <a name="actuals"></a><span data-ttu-id="10fbf-103">Faktiskie dati</span><span class="sxs-lookup"><span data-stu-id="10fbf-103">Actuals</span></span> 

<span data-ttu-id="10fbf-104">_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="10fbf-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="10fbf-105">Faktiskie dati attiecas uz pārskatīto un apstiprināto finanšu un plānošanas norisi projektā.</span><span class="sxs-lookup"><span data-stu-id="10fbf-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="10fbf-106">Tās tiek izveidotas laika, izmaksu, materiālu lietojuma ierakstu, kā arī ierakstu un rēķinu apstiprinājuma rezultātā.</span><span class="sxs-lookup"><span data-stu-id="10fbf-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="10fbf-107">Žurnāla rindu un laika iesniegšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-107">Journal lines and time submission</span></span>

<span data-ttu-id="10fbf-108">Papildinformāciju par laika ievadīšanu skatiet šeit: [Laika ieraksta pārskats](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="10fbf-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="10fbf-109">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="10fbf-109">Time and materials</span></span>

<span data-ttu-id="10fbf-110">Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="10fbf-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="10fbf-111">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="10fbf-111">Fixed price</span></span>

<span data-ttu-id="10fbf-112">Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz fiksētas cenas līguma rindu, sistēma izveido vienu žurnāla rindu – par izmaksām.</span><span class="sxs-lookup"><span data-stu-id="10fbf-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="10fbf-113">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-113">Default pricing</span></span>

<span data-ttu-id="10fbf-114">Noklusējuma cenu izveides loģika atrodas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="10fbf-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="10fbf-115">Lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="10fbf-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="10fbf-116">Šajās vērtībās ir iekļauts darījuma datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.</span><span class="sxs-lookup"><span data-stu-id="10fbf-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="10fbf-117">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Resursu vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="10fbf-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="10fbf-118">Varat pievienot pielāgotu lauku laika ierakstam.</span><span class="sxs-lookup"><span data-stu-id="10fbf-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="10fbf-119">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="10fbf-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="10fbf-120">Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="10fbf-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="10fbf-121">Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="10fbf-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="10fbf-122">Žurnāla rindu un pamata izdevumu iesniegšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="10fbf-123">Papildinformāciju par izdevumu ievadīšanu skatiet šeit: [Izdevumu pārskats](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="10fbf-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="10fbf-124">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="10fbf-124">Time and materials</span></span>

<span data-ttu-id="10fbf-125">Kad iesniegts pamata izdevumu ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="10fbf-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="10fbf-126">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="10fbf-126">Fixed price</span></span>

<span data-ttu-id="10fbf-127">Kad iesniegtais pamata izdevumu ieraksts tiek saistīts ar projektu, kas ir kartēts fiksētas cenas līguma rindā, sistēma izveido vienu žurnāla rindu cenai.</span><span class="sxs-lookup"><span data-stu-id="10fbf-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="10fbf-128">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-128">Default pricing</span></span>

<span data-ttu-id="10fbf-129">Izdevumu noklusējuma cenu ievadīšanas loģikas pamatā ir izdevumu kategorija.</span><span class="sxs-lookup"><span data-stu-id="10fbf-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="10fbf-130">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="10fbf-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="10fbf-131">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Transakcijas kategorija** un **Vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="10fbf-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="10fbf-132">Tomēr tas darbojas tikai tad, ja cenrāža cenu noteikšanas metode ir **Cena par vienību**.</span><span class="sxs-lookup"><span data-stu-id="10fbf-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="10fbf-133">Ja cenu noteikšanas metode ir **Pašizmaksa** vai **Uzcenojums augstāks par izmaksu**, izmaksu ieraksta izveides laikā ievadītā cena tiek izmantota izmaksām, un cena pārdošanas piedāvājuma rindā tiek aprēķināta, pamatojoties uz cenu noteikšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="10fbf-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="10fbf-134">Izmaksu ierakstam var pievienot pielāgotu lauku.</span><span class="sxs-lookup"><span data-stu-id="10fbf-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="10fbf-135">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="10fbf-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="10fbf-136">Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="10fbf-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="10fbf-137">Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="10fbf-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="10fbf-138">Žurnāla rindu un materiālu lietojuma žurnāla iesniegšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="10fbf-139">Papildinformāciju par izdevumu ierakstu skatiet šeit: [Materiālu lietojuma žurnāls](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="10fbf-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="10fbf-140">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="10fbf-140">Time and materials</span></span>

<span data-ttu-id="10fbf-141">Kad iesniegts materiālu lietojuma žurnāls ieraksts tiek saistīts ar projektu, kas tiek kartēts ar laika un materiālu līguma rindu, sistēma izveido divas rindu rindas (vienu par izmaksām un vienu par rēķinā neietverto pārdošanu).</span><span class="sxs-lookup"><span data-stu-id="10fbf-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="10fbf-142">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="10fbf-142">Fixed price</span></span>

<span data-ttu-id="10fbf-143">Kad iesniegtais materiālu lietojuma ieraksts tiek saistīts ar projektu, kas ir kartēts fiksētas cenas līguma rindā, sistēma izveido vienu žurnāla rindu cenai.</span><span class="sxs-lookup"><span data-stu-id="10fbf-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="10fbf-144">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-144">Default pricing</span></span>

<span data-ttu-id="10fbf-145">Materiālu noklusējuma cenu ievadīšanas loģika tiek pamatota uz produktu un vienību kombināciju.</span><span class="sxs-lookup"><span data-stu-id="10fbf-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="10fbf-146">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="10fbf-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="10fbf-147">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Produkta ID** un **Vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="10fbf-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="10fbf-148">Tomēr tas darbojas tikai kataloga produktiem.</span><span class="sxs-lookup"><span data-stu-id="10fbf-148">However, this only works for catalog products.</span></span> <span data-ttu-id="10fbf-149">Ierakstāmiem produktiem cena, kas ievadīta, izveidojot materiālu lietojuma žurnāla ierakstu, tiek izmantota izmaksu un pārdošanas cenai raksta rindās.</span><span class="sxs-lookup"><span data-stu-id="10fbf-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="10fbf-150">Ierakstam **Materiālu lietojuma žurnāls** var pievienot pielāgotu lauku.</span><span class="sxs-lookup"><span data-stu-id="10fbf-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="10fbf-151">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="10fbf-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="10fbf-152">Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="10fbf-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="10fbf-153">Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="10fbf-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="10fbf-154">Ierakstu žurnālu izmantošana izmaksu reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="10fbf-154">Use entry journals to record costs</span></span>

<span data-ttu-id="10fbf-155">Varat izmantot ierakstu žurnālus, lai ierakstītu izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs.</span><span class="sxs-lookup"><span data-stu-id="10fbf-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="10fbf-156">Žurnālus var izmantot šādiem mērķiem:</span><span class="sxs-lookup"><span data-stu-id="10fbf-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="10fbf-157">Pārvietojiet transakciju faktiskos datus no citas sistēmas uz Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="10fbf-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="10fbf-158">Reģistrēt izmaksas, kas notikušas citā sistēmā.</span><span class="sxs-lookup"><span data-stu-id="10fbf-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="10fbf-159">Šīs izmaksas var ietvert iegādes vai apakšuzņēmēju izmaksas.</span><span class="sxs-lookup"><span data-stu-id="10fbf-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10fbf-160">Programma nevalidē žurnāla rindas tipu vai saistīto cenu, kas ievadīta žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="10fbf-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="10fbf-161">Tādējādi ierakstu žurnālus izmantot faktisko datu izveidei drīkst tikai lietotājs, kas pilnībā apzinās faktisko datu ietekmi uz projekta uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="10fbf-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="10fbf-162">Šī žurnāla veida ietekmes dēļ jums rūpīgi jāizvēlas personas, kurām ir piekļuve ierakstu žurnālu izveidei.</span><span class="sxs-lookup"><span data-stu-id="10fbf-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="10fbf-163">Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem</span><span class="sxs-lookup"><span data-stu-id="10fbf-163">Record actuals based on project events</span></span>

<span data-ttu-id="10fbf-164">Project Operations ieraksta finanšu transakcijas, kas notiek projekta laikā.</span><span class="sxs-lookup"><span data-stu-id="10fbf-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="10fbf-165">Šīs transakcijas tiek ierakstītas kā faktiskie dati.</span><span class="sxs-lookup"><span data-stu-id="10fbf-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="10fbf-166">Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.</span><span class="sxs-lookup"><span data-stu-id="10fbf-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="10fbf-167">Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="10fbf-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="10fbf-168">Notikums</span><span class="sxs-lookup"><span data-stu-id="10fbf-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="10fbf-169">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="10fbf-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="10fbf-170">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="10fbf-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="10fbf-171">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="10fbf-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="10fbf-172">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="10fbf-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="10fbf-173">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="10fbf-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="10fbf-174">Faktiski</span><span class="sxs-lookup"><span data-stu-id="10fbf-174">Actuals</span></span></th>
<th><span data-ttu-id="10fbf-175">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-175">Transaction currency</span></span></th>
<th><span data-ttu-id="10fbf-176">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="10fbf-176">Fixed price</span></span></th>
<th><span data-ttu-id="10fbf-177">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10fbf-178">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="10fbf-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="10fbf-179">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="10fbf-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-180">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="10fbf-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="10fbf-181">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="10fbf-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="10fbf-182">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="10fbf-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="10fbf-183">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-183">Cost actual</span></span></td>
<td><span data-ttu-id="10fbf-184">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-185">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-186">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="10fbf-187">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-188">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-189">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="10fbf-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="10fbf-190">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="10fbf-191">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="10fbf-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="10fbf-192">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-192">Cost actual</span></span></td>
<td><span data-ttu-id="10fbf-193">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-194">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-195">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-196">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-197">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-198">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="10fbf-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="10fbf-199">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-200">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="10fbf-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="10fbf-201">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="10fbf-202">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="10fbf-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="10fbf-203">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="10fbf-204">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-205">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="10fbf-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-206">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-207">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-208">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-209">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="10fbf-209">Billed sales</span></span></td>
<td><span data-ttu-id="10fbf-210">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="10fbf-211">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="10fbf-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="10fbf-212">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="10fbf-213">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-214">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-215">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-216">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-217">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-218">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="10fbf-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="10fbf-219">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-220">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="10fbf-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="10fbf-221">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="10fbf-222">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="10fbf-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="10fbf-223">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="10fbf-224">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="10fbf-225">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="10fbf-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="10fbf-226">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="10fbf-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="10fbf-227">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="10fbf-228">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="10fbf-229">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-230">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="10fbf-230">Billed sales</span></span></td>
<td><span data-ttu-id="10fbf-231">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="10fbf-232">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="10fbf-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="10fbf-233">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="10fbf-234">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-235">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="10fbf-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="10fbf-236">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-237">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="10fbf-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="10fbf-238">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="10fbf-239">Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības</span><span class="sxs-lookup"><span data-stu-id="10fbf-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="10fbf-240">Notikums</span><span class="sxs-lookup"><span data-stu-id="10fbf-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="10fbf-241">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="10fbf-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="10fbf-242">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="10fbf-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="10fbf-243">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="10fbf-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="10fbf-244">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="10fbf-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="10fbf-245">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="10fbf-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="10fbf-246">Faktiski</span><span class="sxs-lookup"><span data-stu-id="10fbf-246">Actuals</span></span></th>
<th><span data-ttu-id="10fbf-247">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-247">Transaction currency</span></span></th>
<th><span data-ttu-id="10fbf-248">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="10fbf-248">Fixed price</span></span></th>
<th><span data-ttu-id="10fbf-249">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10fbf-250">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="10fbf-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="10fbf-251">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="10fbf-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-252">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="10fbf-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="10fbf-253">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="10fbf-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="10fbf-254">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="10fbf-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="10fbf-255">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-255">Cost actual</span></span></td>
<td><span data-ttu-id="10fbf-256">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="10fbf-257">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="10fbf-258">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="10fbf-259">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="10fbf-260">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-261">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="10fbf-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="10fbf-262">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-263">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="10fbf-264">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-265">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="10fbf-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="10fbf-266">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="10fbf-267">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="10fbf-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="10fbf-268">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-268">Cost actual</span></span></td>
<td><span data-ttu-id="10fbf-269">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="10fbf-270">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="10fbf-271">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="10fbf-272">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="10fbf-273">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-274">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="10fbf-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="10fbf-275">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-276">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="10fbf-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="10fbf-277">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-278">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="10fbf-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="10fbf-279">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-280">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="10fbf-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="10fbf-281">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="10fbf-282">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="10fbf-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="10fbf-283">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="10fbf-284">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-285">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="10fbf-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-286">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-287">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="10fbf-288">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-289">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="10fbf-289">Billed sales</span></span></td>
<td><span data-ttu-id="10fbf-290">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="10fbf-291">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="10fbf-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="10fbf-292">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="10fbf-293">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-294">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-295">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-296">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="10fbf-297">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-298">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="10fbf-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="10fbf-299">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-300">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="10fbf-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="10fbf-301">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="10fbf-302">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="10fbf-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="10fbf-303">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="10fbf-304">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="10fbf-305">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="10fbf-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="10fbf-306">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="10fbf-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="10fbf-307">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="10fbf-308">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="10fbf-309">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="10fbf-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-310">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="10fbf-310">Billed sales</span></span></td>
<td><span data-ttu-id="10fbf-311">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="10fbf-312">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="10fbf-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="10fbf-313">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="10fbf-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="10fbf-314">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-315">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="10fbf-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="10fbf-316">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10fbf-317">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="10fbf-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="10fbf-318">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="10fbf-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
