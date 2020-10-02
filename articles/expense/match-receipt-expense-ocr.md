---
title: Saskaņot ieejas plūsmu ar izdevumiem, izmantojot OCR
description: Šajā tēmā ir sniegta informācija par rakstzīmju optiskās atpazīšanas (OCR) apstrādi kvītīm.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897010"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="3bf4b-103">Saskaņot ieejas plūsmu ar izdevumiem, izmantojot OCR</span><span class="sxs-lookup"><span data-stu-id="3bf4b-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="3bf4b-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="3bf4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3bf4b-105">Izdevumu ievade ir uzlabota, ieviešot rakstzīmju optiskās atpazīšanas (OCR) apstrādi kvītīm.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="3bf4b-106">Šī funkcionalitāte ir paredzēta, lai uzlabotu lietotāju pieredzi, veidojot izdevumu atskaites.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="3bf4b-107">Galvenie līdzekļi</span><span class="sxs-lookup"><span data-stu-id="3bf4b-107">Key features</span></span>

- <span data-ttu-id="3bf4b-108">Sistēma no kvītīm izgūst tirgotāja nosaukumu, datumu un kopējo summu.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="3bf4b-109">Sistēma centīsies saskaņot nepievienotās kvītis nepievienotām izdevumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="3bf4b-110">Varat izveidot manuāli ievadītās izdevumu transakcijas no kvītīm.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="3bf4b-111">Kvīšu pievienošana izdevumu atskaitei</span><span class="sxs-lookup"><span data-stu-id="3bf4b-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="3bf4b-112">Lai automātiski pievienotu kvītis, kas ietver kredītkaršu transakcijas, kad ir izveidota izdevumu atskaite, izpildiet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="3bf4b-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="3bf4b-113">Atveriet **Izdevumu pārvaldības** darbvietu.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="3bf4b-114">Cilnē **Kvītis** pārliecinieties, ka pastāv nepievienotas kvītis.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="3bf4b-115">Kvītis varat arī augšupielādēt cilnē **Kvītis**.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="3bf4b-116">Cilnē **Izdevumi** pārliecinieties, ka pastāv nepievienoti izdevumi.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="3bf4b-117">Parasti izdevumu administrators importē šos izdevumus no kredītkartes nodrošinātāja.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="3bf4b-118">Atlasiet **Jauna izdevumu atskaite**.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-118">Select **New expense report**.</span></span> <span data-ttu-id="3bf4b-119">Ņemiet vērā, ka, veidojot izdevumu atskaiti, varat iekļaut arī izdevumus un kvītis.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="3bf4b-120">Ja pievienojat gan izdevumus, gan kvītis, tiek aktivizēta automātiska kvīšu saskaņošana ar izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="3bf4b-121">Kvīšu izveide vai saskaņošana ar izdevumu atskaiti</span><span class="sxs-lookup"><span data-stu-id="3bf4b-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="3bf4b-122">Lai izveidotu izdevumu vai to saskaņotu no kvīts, izpildiet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="3bf4b-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="3bf4b-123">Izdevumu atskaites cilnē **Kvītis** pievienojiet kvīti, atlasot **Pievienot kvītis**.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="3bf4b-124">Zem augšupielādētā kvīts attēla ņemiet vērā opcijas **Izveidot** un **Saskaņot**.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="3bf4b-125">Atlasiet **Izveidot**, lai izveidotu manuāli ievadīto izdevumu transakciju un aizpildītu no kvīts izvilktās vērtības.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="3bf4b-126">Atlasot **Saskaņot**, sistēma cenšas saskaņot esošu izdevumu ar kvīti.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="3bf4b-127">Instalēšana</span><span class="sxs-lookup"><span data-stu-id="3bf4b-127">Installation</span></span>

<span data-ttu-id="3bf4b-128">Lai izmantotu šīs papildu izdevumu iespējas, instalējiet Izdevumu Pārvaldības Pakalpojums pievienojumprogrammu Microsoft programmai Dynamics 365 Finance un ieslēdziet līdzekļus savā instancē.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="3bf4b-129">Jūs varat piekļūt pievienojumprogrammai no sava projekta Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3bf4b-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="3bf4b-130">Pierakstieties LCS un atveriet vēlamo vidi.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="3bf4b-131">Pārejiet uz **Pilna informācija**.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="3bf4b-132">Atlasiet **Uzturēt** vai ritiniet uz leju līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="3bf4b-133">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="3bf4b-134">Atlasiet **Izdevumu Pārvaldības Pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="3bf4b-135">Izpildiet instalēšanas rokasgrāmatas norādījumus un piekrītiet noteikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="3bf4b-136">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-136">Select **Install**.</span></span>

<span data-ttu-id="3bf4b-137">**Līdzekļu pārvaldības** darbvietā ieslēdziet šādus līdzekļus:</span><span class="sxs-lookup"><span data-stu-id="3bf4b-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="3bf4b-138">Atjaunotas izdevumu atskaites</span><span class="sxs-lookup"><span data-stu-id="3bf4b-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="3bf4b-139">Izdevumu automātiska saskaņošana un izveide no kvīts</span><span class="sxs-lookup"><span data-stu-id="3bf4b-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="3bf4b-140">Ieslēdzot šos līdzekļus, notiek šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="3bf4b-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="3bf4b-141">Esošā **Izdevumu pārvaldības** darbvieta tiek aizstāta ar jauno darbvietu.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="3bf4b-142">Tiek pievienota jauns izvēlnes vienums izdevumu lauka redzamībai.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="3bf4b-143">Joprojām varat atvērt kādreizējo **Izdevumu atskaišu** lapu, dodoties uz **Izdevumu pārvaldība > Mani izdevumi > Izdevumu atskaites**.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="3bf4b-144">Darbplūsmas un visi apstiprinājumi joprojām aizved uz esošo izdevumu atskaišu lapu.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="3bf4b-145">Kvītis apstrādās ar Microsoft Azure Cognitive Services, bet metadati tiks izvilkti un pievienoti.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="3bf4b-146">Tiek pievienota opcija, kas ļauj izveidot izdevumu atskaiti, kas ietver saskaņotas nepievienotās kvītis.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="3bf4b-147">Opcija, kas tiek pievienota izdevumu atskaitēm, ļauj izveidot izdevumu rindu no kvīts vai mēģina saskaņot esošu kvīti ar esošu izdevumu rindu.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="3bf4b-148">Bieži uzdotie jautājumi</span><span class="sxs-lookup"><span data-stu-id="3bf4b-148">Frequently asked questions</span></span>

<span data-ttu-id="3bf4b-149">**Vai Microsoft savos modeļos izmanto manus datus?**</span><span class="sxs-lookup"><span data-stu-id="3bf4b-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="3bf4b-150">Nē, Microsoft ir iebūvēts vispārīgās algoritmiskās mācīšanās modelis, lai apstrādātu kvītis.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="3bf4b-151">Šis modelis netiek balstīts jūsu augšupielādētajās kvītīs.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="3bf4b-152">**Kur šis līdzeklis ir pieejams un kur to apstrādā?**</span><span class="sxs-lookup"><span data-stu-id="3bf4b-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="3bf4b-153">Pašlaik tiek atbalstītas Amerikas Savienotās Valstis.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="3bf4b-154">**Kur nonāk manas kvītis?**</span><span class="sxs-lookup"><span data-stu-id="3bf4b-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="3bf4b-155">Finance sazinās ar Cognitive Services, lai izvilktu lauka datus.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="3bf4b-156">Cognitive Services paturēs jūsu kvīts kopiju 24 stundas, kamēr notiek apstrāde.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="3bf4b-157">Pēc apstrādes pabeigšanas Cognitive Services kvīti dzēsīs.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="3bf4b-158">Kvītis joprojām tiek glabātas Finance.</span><span class="sxs-lookup"><span data-stu-id="3bf4b-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="3bf4b-159">Papildinformāciju skatiet rakstā [Kvīšu izpratnes veicināšana ar Form Recognizer jauno iespēju](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="3bf4b-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
