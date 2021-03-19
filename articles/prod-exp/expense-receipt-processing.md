---
title: Izdevumu kvīšu apstrāde
description: Šajā tēmā ir sniegta informācija par rakstzīmju optiskās atpazīšanas (OCR) apstrādi kvītīm. Šis līdzeklis ir paredzēts, lai uzlabotu lietotāju pieredzi, veidojot izdevumu atskaites risinājumā Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271812"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="a80c5-104">Izdevumu kvīšu apstrāde</span><span class="sxs-lookup"><span data-stu-id="a80c5-104">Expense receipt processing</span></span>

<span data-ttu-id="a80c5-105">Izdevumu ievade ir uzlabota, ieviešot rakstzīmju optiskās atpazīšanas (OCR) apstrādi kvītīm.</span><span class="sxs-lookup"><span data-stu-id="a80c5-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="a80c5-106">Šis līdzeklis ir paredzēts, lai uzlabotu lietotāju pieredzi, veidojot izdevumu atskaites.</span><span class="sxs-lookup"><span data-stu-id="a80c5-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="a80c5-107">Galvenie līdzekļi</span><span class="sxs-lookup"><span data-stu-id="a80c5-107">Key features</span></span>

- <span data-ttu-id="a80c5-108">No kvītīm tiek izgūts tirgotāja nosaukums, datums un kopējā summa.</span><span class="sxs-lookup"><span data-stu-id="a80c5-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="a80c5-109">Līdzeklis mēģina saskaņot nepievienotās kvītis nepievienotām izdevumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="a80c5-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="a80c5-110">Lietotāji var izveidot manuāli ievadītās izdevumu transakcijas no kvītīm.</span><span class="sxs-lookup"><span data-stu-id="a80c5-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="a80c5-111">Lietošanas piemēri</span><span class="sxs-lookup"><span data-stu-id="a80c5-111">Usage examples</span></span>

<span data-ttu-id="a80c5-112">Lai automātiski pievienotu kvītis, kas ietver kredītkaršu transakcijas, kad ir izveidota izdevumu atskaite, izpildiet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="a80c5-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="a80c5-113">Atveriet **Izdevumu pārvaldības** darbvietu.</span><span class="sxs-lookup"><span data-stu-id="a80c5-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="a80c5-114">Cilnē **Kvītis** pārliecinieties, ka pastāv nepievienotas kvītis.</span><span class="sxs-lookup"><span data-stu-id="a80c5-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="a80c5-115">Kvītis varat arī augšupielādēt cilnē **Kvītis**.</span><span class="sxs-lookup"><span data-stu-id="a80c5-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="a80c5-116">Cilnē **Izdevumi** pārliecinieties, ka pastāv nepievienoti izdevumi.</span><span class="sxs-lookup"><span data-stu-id="a80c5-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="a80c5-117">Parasti izdevumu administrators importē šos izdevumus no kredītkartes nodrošinātāja.</span><span class="sxs-lookup"><span data-stu-id="a80c5-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="a80c5-118">Atlasiet **Jauna izdevumu atskaite**.</span><span class="sxs-lookup"><span data-stu-id="a80c5-118">Select **New expense report**.</span></span> <span data-ttu-id="a80c5-119">Ņemiet vērā, ka, veidojot izdevumu atskaiti, varat iekļaut arī izdevumus un kvītis.</span><span class="sxs-lookup"><span data-stu-id="a80c5-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="a80c5-120">Ja pievienojat gan izdevumus, gan kvītis, tiek aktivizēta automātiska kvīšu saskaņošana ar izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="a80c5-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="a80c5-121">Lai izveidotu izdevumu vai to saskaņotu no kvīts, izpildiet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="a80c5-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="a80c5-122">Izdevumu atskaites cilnē **Kvītis** pievienojiet kvīti, atlasot **Pievienot kvītis**.</span><span class="sxs-lookup"><span data-stu-id="a80c5-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="a80c5-123">Zem augšupielādētā kvīts attēla ņemiet vērā opcijas **Izveidot** un **Saskaņot**.</span><span class="sxs-lookup"><span data-stu-id="a80c5-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="a80c5-124">Atlasiet **Izveidot**, lai izveidotu manuāli ievadīto izdevumu transakciju un aizpildītu no kvīts izvilktās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a80c5-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="a80c5-125">Atlasot **Saskaņot**, sistēma cenšas saskaņot esošu izdevumu ar kvīti.</span><span class="sxs-lookup"><span data-stu-id="a80c5-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="a80c5-126">Instalēšana</span><span class="sxs-lookup"><span data-stu-id="a80c5-126">Installation</span></span>

<span data-ttu-id="a80c5-127">Šis līdzeklis darbojas kopā ar līdzekli **Uzlabotas izdevumu atskaites**, lai vienkāršotu izmaksu pieredzi.</span><span class="sxs-lookup"><span data-stu-id="a80c5-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="a80c5-128">Šis līdzeklis ir pieejams vismaz 2. līmeņa vidēm, kas ir smilškastes un ražošanas instances.</span><span class="sxs-lookup"><span data-stu-id="a80c5-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="a80c5-129">Lai izmantotu šīs papildu izdevumu iespējas, instalējiet Izdevumu Pārvaldības Pakalpojums pievienojumprogrammu Microsoft programmai Dynamics 365 Finance un ieslēdziet līdzekļus savā instancē.</span><span class="sxs-lookup"><span data-stu-id="a80c5-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="a80c5-130">Jūs varat piekļūt pievienojumprogrammai no sava projekta Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a80c5-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="a80c5-131">Pierakstieties LCS un atveriet vēlamo vidi.</span><span class="sxs-lookup"><span data-stu-id="a80c5-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="a80c5-132">Pārejiet uz **Pilna informācija**.</span><span class="sxs-lookup"><span data-stu-id="a80c5-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="a80c5-133">Atlasiet **Uzturēt** vai ritiniet uz leju līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="a80c5-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="a80c5-134">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="a80c5-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="a80c5-135">Atlasiet **Izdevumu Pārvaldības Pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="a80c5-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="a80c5-136">Izpildiet instalēšanas rokasgrāmatas norādījumus un piekrītiet noteikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="a80c5-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="a80c5-137">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="a80c5-137">Select **Install**.</span></span>

<span data-ttu-id="a80c5-138">**Līdzekļu pārvaldības** darbvietā ieslēdziet šādus līdzekļus:</span><span class="sxs-lookup"><span data-stu-id="a80c5-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="a80c5-139">Atjaunotas izdevumu atskaites</span><span class="sxs-lookup"><span data-stu-id="a80c5-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="a80c5-140">Izdevumu automātiska saskaņošana un izveide no kvīts</span><span class="sxs-lookup"><span data-stu-id="a80c5-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="a80c5-141">Ieslēdzot šos līdzekļus, notiek šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="a80c5-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="a80c5-142">Esošā **Izdevumu pārvaldības** darbvieta tiek aizstāta ar jauno darbvietu.</span><span class="sxs-lookup"><span data-stu-id="a80c5-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="a80c5-143">Tiek pievienota jauns izvēlnes vienums izdevumu lauka redzamībai.</span><span class="sxs-lookup"><span data-stu-id="a80c5-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="a80c5-144">Joprojām varat atvērt kādreizējo **Izdevumu atskaišu** lapu, dodoties uz **Izdevumu pārvaldība > Mani izdevumi > Izdevumu atskaites**.</span><span class="sxs-lookup"><span data-stu-id="a80c5-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="a80c5-145">Darbplūsmas un visi apstiprinājumi joprojām aizved uz esošo izdevumu atskaišu lapu.</span><span class="sxs-lookup"><span data-stu-id="a80c5-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="a80c5-146">Kvītis apstrādās ar Microsoft Azure Cognitive Services, bet metadati tiks izvilkti un pievienoti.</span><span class="sxs-lookup"><span data-stu-id="a80c5-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="a80c5-147">Tiek pievienota opcija, kas ļauj izveidot izdevumu atskaiti, kas ietver saskaņotas nepievienotās kvītis.</span><span class="sxs-lookup"><span data-stu-id="a80c5-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="a80c5-148">Opcija, kas tiek pievienota izdevumu atskaitēm, ļauj izveidot izdevumu rindu no kvīts vai mēģina saskaņot esošu kvīti ar esošu izdevumu rindu.</span><span class="sxs-lookup"><span data-stu-id="a80c5-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="a80c5-149">Lai iegūtu papildinformāciju par līdzekli Uzlabotas izmaksu atskaites, skatiet rakstu [I Uzlabotas izmaksu atskaites](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="a80c5-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="a80c5-150">Bieži uzdotie jautājumi</span><span class="sxs-lookup"><span data-stu-id="a80c5-150">Frequently asked questions</span></span>

<span data-ttu-id="a80c5-151">**Vai Microsoft savos modeļos izmanto manus datus?**</span><span class="sxs-lookup"><span data-stu-id="a80c5-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="a80c5-152">Nē, Microsoft ir iebūvēts vispārīgās algoritmiskās mācīšanās modelis, lai apstrādātu kvītis.</span><span class="sxs-lookup"><span data-stu-id="a80c5-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="a80c5-153">Šis modelis netiek balstīts jūsu augšupielādētajās kvītīs.</span><span class="sxs-lookup"><span data-stu-id="a80c5-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="a80c5-154">**Kur šis līdzeklis ir pieejams un kur to apstrādā?**</span><span class="sxs-lookup"><span data-stu-id="a80c5-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="a80c5-155">Pašlaik tiek atbalstītas Amerikas Savienotās Valstis.</span><span class="sxs-lookup"><span data-stu-id="a80c5-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="a80c5-156">**Kur nonāk manas kvītis?**</span><span class="sxs-lookup"><span data-stu-id="a80c5-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="a80c5-157">Finance sazinās ar Cognitive Services, lai izvilktu lauka datus.</span><span class="sxs-lookup"><span data-stu-id="a80c5-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="a80c5-158">Cognitive Services paturēs jūsu kvīts kopiju 24 stundas, kamēr notiek apstrāde.</span><span class="sxs-lookup"><span data-stu-id="a80c5-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="a80c5-159">Pēc apstrādes pabeigšanas Cognitive Services kvīti dzēsīs.</span><span class="sxs-lookup"><span data-stu-id="a80c5-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="a80c5-160">Kvītis joprojām tiek glabātas Finance.</span><span class="sxs-lookup"><span data-stu-id="a80c5-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="a80c5-161">Papildinformāciju skatiet rakstā [Kvīšu izpratnes veicināšana ar Form Recognizer jauno iespēju](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="a80c5-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]