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
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996620"
---
# <a name="actuals"></a><span data-ttu-id="1d1e8-103">Faktiskie dati</span><span class="sxs-lookup"><span data-stu-id="1d1e8-103">Actuals</span></span> 

<span data-ttu-id="1d1e8-104">_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="1d1e8-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d1e8-105">Faktiskie dati attiecas uz pārskatīto un apstiprināto finanšu un plānošanas norisi projektā.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="1d1e8-106">Tās tiek izveidotas laika, izmaksu, materiālu lietojuma ierakstu, kā arī ierakstu un rēķinu apstiprinājuma rezultātā.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="1d1e8-107">Žurnāla rindu un laika iesniegšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-107">Journal lines and time submission</span></span>

<span data-ttu-id="1d1e8-108">Papildinformāciju par laika ievadīšanu skatiet šeit: [Laika ieraksta pārskats](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d1e8-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="1d1e8-109">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="1d1e8-109">Time and materials</span></span>

<span data-ttu-id="1d1e8-110">Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="1d1e8-111">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-111">Fixed price</span></span>

<span data-ttu-id="1d1e8-112">Kad iesniegts laika ieraksts ir saistīts ar projektu, kas ir kartēts uz fiksētas cenas līguma rindu, sistēma izveido vienu žurnāla rindu – par izmaksām.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="1d1e8-113">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-113">Default pricing</span></span>

<span data-ttu-id="1d1e8-114">Noklusējuma cenu izveides loģika atrodas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="1d1e8-115">Lauka vērtības no laika ieraksta tiek kopētas uz žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="1d1e8-116">Šajās vērtībās ir iekļauts darījuma datums, līguma rinda, uz kuru projekts ir kartēts, un valūtas rezultāts atbilstošajā cenrādī.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="1d1e8-117">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Loma** un **Resursu vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="1d1e8-118">Varat pievienot pielāgotu lauku laika ierakstam.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="1d1e8-119">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="1d1e8-120">Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="1d1e8-121">Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="1d1e8-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="1d1e8-122">Žurnāla rindu un pamata izdevumu iesniegšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="1d1e8-123">Papildinformāciju par izdevumu ievadīšanu skatiet šeit: [Izdevumu pārskats](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d1e8-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="1d1e8-124">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="1d1e8-124">Time and materials</span></span>

<span data-ttu-id="1d1e8-125">Kad iesniegts pamata izdevumu ieraksts ir saistīts ar projektu, kas ir kartēts uz laika un materiālu līguma rindu, sistēma izveido divas žurnāla rindas – vienu par izmaksām un vienu – par rēķinā neiekļauto pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="1d1e8-126">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-126">Fixed price</span></span>

<span data-ttu-id="1d1e8-127">Kad iesniegtais pamata izdevumu ieraksts tiek saistīts ar projektu, kas ir kartēts fiksētas cenas līguma rindā, sistēma izveido vienu žurnāla rindu cenai.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="1d1e8-128">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-128">Default pricing</span></span>

<span data-ttu-id="1d1e8-129">Izdevumu noklusējuma cenu ievadīšanas loģikas pamatā ir izdevumu kategorija.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="1d1e8-130">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="1d1e8-131">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Transakcijas kategorija** un **Vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="1d1e8-132">Tomēr tas darbojas tikai tad, ja cenrāža cenu noteikšanas metode ir **Cena par vienību**.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="1d1e8-133">Ja cenu noteikšanas metode ir **Pašizmaksa** vai **Uzcenojums augstāks par izmaksu**, izmaksu ieraksta izveides laikā ievadītā cena tiek izmantota izmaksām, un cena pārdošanas piedāvājuma rindā tiek aprēķināta, pamatojoties uz cenu noteikšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="1d1e8-134">Izmaksu ierakstam var pievienot pielāgotu lauku.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="1d1e8-135">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="1d1e8-136">Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="1d1e8-137">Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="1d1e8-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="1d1e8-138">Žurnāla rindu un materiālu lietojuma žurnāla iesniegšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="1d1e8-139">Papildinformāciju par izdevumu ierakstu skatiet šeit: [Materiālu lietojuma žurnāls](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="1d1e8-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="1d1e8-140">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="1d1e8-140">Time and materials</span></span>

<span data-ttu-id="1d1e8-141">Kad iesniegts materiālu lietojuma žurnāls ieraksts tiek saistīts ar projektu, kas tiek kartēts ar laika un materiālu līguma rindu, sistēma izveido divas rindu rindas (vienu par izmaksām un vienu par rēķinā neietverto pārdošanu).</span><span class="sxs-lookup"><span data-stu-id="1d1e8-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="1d1e8-142">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-142">Fixed price</span></span>

<span data-ttu-id="1d1e8-143">Kad iesniegtais materiālu lietojuma ieraksts tiek saistīts ar projektu, kas ir kartēts fiksētas cenas līguma rindā, sistēma izveido vienu žurnāla rindu cenai.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="1d1e8-144">Noklusējuma cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-144">Default pricing</span></span>

<span data-ttu-id="1d1e8-145">Materiālu noklusējuma cenu ievadīšanas loģika tiek pamatota uz produktu un vienību kombināciju.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="1d1e8-146">Lai noteiktu atbilstošo cenrādi, tiek izmantots gan transakcijas datums, gan līguma rinda, uz kuru ir kartēts projekts, gan arī valūta.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="1d1e8-147">Lauki, kas ietekmē noklusējuma cenas, piemēram, **Produkta ID** un **Vienība**, tiek izmantoti, lai noteiktu atbilstošu cenu žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="1d1e8-148">Tomēr tas darbojas tikai kataloga produktiem.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-148">However, this only works for catalog products.</span></span> <span data-ttu-id="1d1e8-149">Ierakstāmiem produktiem cena, kas ievadīta, izveidojot materiālu lietojuma žurnāla ierakstu, tiek izmantota izmaksu un pārdošanas cenai raksta rindās.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="1d1e8-150">Ierakstam **Materiālu lietojuma žurnāls** var pievienot pielāgotu lauku.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="1d1e8-151">Ja vēlaties, lai lauka vērtība tiktu izplatīta uz faktiskajiem datiem, izveidojiet lauku tabulās **Faktiskie dati** un **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="1d1e8-152">Lietojiet pielāgotu kodu, lai izplatītu atlasīto lauka vērtību no laika ievades uz faktiskiem līdz žurnāla rindai, izmantojot transakcijas izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="1d1e8-153">Papildinformāciju par transakciju izcelsmi un savienojumiem skatiet rakstā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="1d1e8-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="1d1e8-154">Ierakstu žurnālu izmantošana izmaksu reģistrēšanai</span><span class="sxs-lookup"><span data-stu-id="1d1e8-154">Use entry journals to record costs</span></span>

<span data-ttu-id="1d1e8-155">Varat izmantot ierakstu žurnālus, lai ierakstītu izmaksas vai ieņēmumus materiālu, maksu, laika, izdevumu vai nodokļu transakciju klasēs.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="1d1e8-156">Žurnālus var izmantot šādiem mērķiem:</span><span class="sxs-lookup"><span data-stu-id="1d1e8-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="1d1e8-157">Pārvietojiet transakciju faktiskos datus no citas sistēmas uz Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="1d1e8-158">Reģistrēt izmaksas, kas notikušas citā sistēmā.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="1d1e8-159">Šīs izmaksas var ietvert iegādes vai apakšuzņēmēju izmaksas.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d1e8-160">Programma nevalidē žurnāla rindas tipu vai saistīto cenu, kas ievadīta žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="1d1e8-161">Tādējādi ierakstu žurnālus izmantot faktisko datu izveidei drīkst tikai lietotājs, kas pilnībā apzinās faktisko datu ietekmi uz projekta uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="1d1e8-162">Šī žurnāla veida ietekmes dēļ jums rūpīgi jāizvēlas personas, kurām ir piekļuve ierakstu žurnālu izveidei.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="1d1e8-163">Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem</span><span class="sxs-lookup"><span data-stu-id="1d1e8-163">Record actuals based on project events</span></span>

<span data-ttu-id="1d1e8-164">Project Operations ieraksta finanšu transakcijas, kas notiek projekta laikā.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="1d1e8-165">Šīs transakcijas tiek ierakstītas kā faktiskie dati.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="1d1e8-166">Tālāk esošajās tabulās ir parādīti dažādie faktisko datu tipi, kas tiek izveidoti atkarībā no tā, vai projekts ir laika un materiālu vai fiksētas cenas projekts, atrodas pirmspārdošanas posmā vai arī ir iekšējais projekts.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="1d1e8-167">Resurss pieder tai pašai organizācijas struktūrvienībai, kurai pieder projekta līgumslēdzēja struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="1d1e8-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1d1e8-168">Notikums</span><span class="sxs-lookup"><span data-stu-id="1d1e8-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1d1e8-169">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="1d1e8-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1d1e8-170">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="1d1e8-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1d1e8-171">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="1d1e8-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1d1e8-172">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="1d1e8-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1d1e8-173">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1d1e8-174">Faktiski</span><span class="sxs-lookup"><span data-stu-id="1d1e8-174">Actuals</span></span></th>
<th><span data-ttu-id="1d1e8-175">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-175">Transaction currency</span></span></th>
<th><span data-ttu-id="1d1e8-176">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-176">Fixed price</span></span></th>
<th><span data-ttu-id="1d1e8-177">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d1e8-178">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1d1e8-179">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="1d1e8-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-180">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1d1e8-181">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="1d1e8-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1d1e8-182">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1d1e8-183">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-183">Cost actual</span></span></td>
<td><span data-ttu-id="1d1e8-184">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-185">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-186">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="1d1e8-187">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-188">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-189">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="1d1e8-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1d1e8-190">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1d1e8-191">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1d1e8-192">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-192">Cost actual</span></span></td>
<td><span data-ttu-id="1d1e8-193">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-194">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-195">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-196">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-197">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-198">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="1d1e8-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e8-199">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-200">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="1d1e8-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e8-201">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1d1e8-202">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1d1e8-203">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1d1e8-204">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-205">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="1d1e8-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-206">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-207">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-208">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-209">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-209">Billed sales</span></span></td>
<td><span data-ttu-id="1d1e8-210">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1d1e8-211">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1d1e8-212">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1d1e8-213">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-214">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-215">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-216">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-217">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-218">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="1d1e8-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e8-219">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-220">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="1d1e8-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e8-221">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1d1e8-222">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1d1e8-223">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1d1e8-224">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1d1e8-225">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="1d1e8-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1d1e8-226">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="1d1e8-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1d1e8-227">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e8-228">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e8-229">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-230">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-230">Billed sales</span></span></td>
<td><span data-ttu-id="1d1e8-231">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1d1e8-232">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1d1e8-233">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1d1e8-234">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-235">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="1d1e8-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e8-236">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-237">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="1d1e8-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e8-238">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="1d1e8-239">Resurss pieder organizācijas struktūrvienībai, kas atšķiras no projekta līgumslēdzēja struktūrvienības</span><span class="sxs-lookup"><span data-stu-id="1d1e8-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1d1e8-240">Notikums</span><span class="sxs-lookup"><span data-stu-id="1d1e8-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1d1e8-241">Apmaksājams vai pārdots projekts</span><span class="sxs-lookup"><span data-stu-id="1d1e8-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1d1e8-242">Projekts pirmspārdošanas posmā</span><span class="sxs-lookup"><span data-stu-id="1d1e8-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1d1e8-243">Iekšējais projekts</span><span class="sxs-lookup"><span data-stu-id="1d1e8-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1d1e8-244">Laika un materiālu</span><span class="sxs-lookup"><span data-stu-id="1d1e8-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1d1e8-245">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1d1e8-246">Faktiski</span><span class="sxs-lookup"><span data-stu-id="1d1e8-246">Actuals</span></span></th>
<th><span data-ttu-id="1d1e8-247">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-247">Transaction currency</span></span></th>
<th><span data-ttu-id="1d1e8-248">Fiksētas cenas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-248">Fixed price</span></span></th>
<th><span data-ttu-id="1d1e8-249">Transakcijas valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1d1e8-250">Tiek izveidots laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1d1e8-251">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="1d1e8-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-252">Tiek iesniegts laika ieraksts.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1d1e8-253">Entītijā Faktiskie dati nav nevienas darbības</span><span class="sxs-lookup"><span data-stu-id="1d1e8-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="1d1e8-254">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1d1e8-255">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-255">Cost actual</span></span></td>
<td><span data-ttu-id="1d1e8-256">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1d1e8-257">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1d1e8-258">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1d1e8-259">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1d1e8-260">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-261">Rēķinā neiekļautā faktiskā pārdošana — iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="1d1e8-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1d1e8-262">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-263">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1d1e8-264">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-265">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1d1e8-266">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1d1e8-267">Laiks tiek apstiprināts, un apstiprinājuma laikā netiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1d1e8-268">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-268">Cost actual</span></span></td>
<td><span data-ttu-id="1d1e8-269">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e8-270">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e8-271">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e8-272">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e8-273">Faktiskās izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-274">Resursu struktūrvienības izmaksas</span><span class="sxs-lookup"><span data-stu-id="1d1e8-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1d1e8-275">Resursu struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-276">Starporganizāciju pārdošana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1d1e8-277">Līgumslēdzēja struktūrvienības valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-278">Rēķinā neiekļautā faktiskā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="1d1e8-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e8-279">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-280">Rēķinā neiekļautā faktiskā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="1d1e8-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e8-281">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1d1e8-282">Tiek apstiprināts rēķins, un netiek mainītas vai palielinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1d1e8-283">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1d1e8-284">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-285">Rēķinā iekļautā pārdošana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="1d1e8-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-286">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-287">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1d1e8-288">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-289">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-289">Billed sales</span></span></td>
<td><span data-ttu-id="1d1e8-290">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1d1e8-291">Tiek apstiprināts rēķins, un tiek samazinātas apmaksājamās stundas.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1d1e8-292">Rēķinā neiekļautās pārdošanas atsaukšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1d1e8-293">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-294">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-295">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-296">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1d1e8-297">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-298">Rēķinā iekļautā pārdošana — rēķinā iekļaujams jaunais daudzums</span><span class="sxs-lookup"><span data-stu-id="1d1e8-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e8-299">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-300">Rēķinā iekļautā pārdošana — starpība nav iekļaujama rēķinā</span><span class="sxs-lookup"><span data-stu-id="1d1e8-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e8-301">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1d1e8-302">Rēķins tiek labots, lai palielinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1d1e8-303">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1d1e8-304">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1d1e8-305">Rēķinā iekļautās pārdošanas atsaukšana atskaites punktam</span><span class="sxs-lookup"><span data-stu-id="1d1e8-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1d1e8-306">Atskaites punkta statusa izmaiņas no <strong>Izrakstīts rēķins</strong> uz <strong>Gatavs rēķinam</strong></span><span class="sxs-lookup"><span data-stu-id="1d1e8-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1d1e8-307">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e8-308">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1d1e8-309">Nav piemērojams</span><span class="sxs-lookup"><span data-stu-id="1d1e8-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-310">Rēķinā iekļautā pārdošana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-310">Billed sales</span></span></td>
<td><span data-ttu-id="1d1e8-311">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1d1e8-312">Rēķins tiek labots, lai samazinātu rēķinā iekļaujamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="1d1e8-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1d1e8-313">Rēķinā iekļautā pārdošana — atsaukšana</span><span class="sxs-lookup"><span data-stu-id="1d1e8-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1d1e8-314">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-315">Rēķinā iekļautā pārdošana jaunajam daudzumam</span><span class="sxs-lookup"><span data-stu-id="1d1e8-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1d1e8-316">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d1e8-317">Rēķinā neiekļautā pārdošana — rēķinā iekļaujama starpība</span><span class="sxs-lookup"><span data-stu-id="1d1e8-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1d1e8-318">Projekta līguma valūta</span><span class="sxs-lookup"><span data-stu-id="1d1e8-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
