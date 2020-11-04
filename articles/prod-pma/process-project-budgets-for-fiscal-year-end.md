---
title: Projekta budžeta pārcelšana finanšu gada beigās
description: Šis raksts sniedz inoformation par to, kā pārnest atlikušās budžeta summas uz nākamajiem gadiem un izveidot budžeta reģistra detaļas.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080577"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="9c533-103">Projekta budžeta pārcelšana finanšu gada beigās</span><span class="sxs-lookup"><span data-stu-id="9c533-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c533-104">Strādājot ar vairāku gadu projektu, finanšu gada beigās var būt atlikums budžetā.</span><span class="sxs-lookup"><span data-stu-id="9c533-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="9c533-105">Atlikušās budžeta summas var pārcelt uz nākamo gadu un izveidot budžeta reģistra informāciju par summām saistītajos virsgrāmatas kontos.</span><span class="sxs-lookup"><span data-stu-id="9c533-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="9c533-106">Lai pārnestu atlikušās summas, pārskatiet un analizējiet atlikušās budžeta summas.</span><span class="sxs-lookup"><span data-stu-id="9c533-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="9c533-107">Atlikušo budžeta summu pārskatīšana un analīze</span><span class="sxs-lookup"><span data-stu-id="9c533-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="9c533-108">Izpildiet tālāk aprakstītās darbības, lai pārskatītu gada beigu budžeta summas projektiem, bet neveiktu summas pārcelšanu.</span><span class="sxs-lookup"><span data-stu-id="9c533-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="9c533-109">Dodieties uz **Projekta pārvaldība un uzskaite** > **Periodisks** > **Budžeti** > **Pārcelt budžetus**.</span><span class="sxs-lookup"><span data-stu-id="9c533-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="9c533-110">Lapas **Projekta budžeta pārcelšanas process** cilnē **Gada beigu opcijas** pārbaudiet, vai nav iespējota opcija **Pārcelt atlikušās projekta budžeta summas**.</span><span class="sxs-lookup"><span data-stu-id="9c533-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="9c533-111">Cilnes **Parametri** laukā **Projekta budžeta gads** atlasiet finanšu gadu, kuram vēlaties skatīt atlikušo budžeta summu.</span><span class="sxs-lookup"><span data-stu-id="9c533-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="9c533-112">Laukā **Aktuālais finanšu gads** atlasiet finanšu gadu, kuram vēlaties skatīt atlikušo budžeta summu.</span><span class="sxs-lookup"><span data-stu-id="9c533-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="9c533-113">Laukā **No prognozes modeļa** atlasiet **Atlikušais budžets**.</span><span class="sxs-lookup"><span data-stu-id="9c533-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="9c533-114">Lai iekļautu projektus, kas atbilst atlasītajiem kritērijiem, bet kuriem nav atlikušā budžeta, atlasiet **Rādīt nulli atlikušo**.</span><span class="sxs-lookup"><span data-stu-id="9c533-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="9c533-115">Cilnē **Atlasīt budžetus** atlasiet **Izgūt visus budžetus** , lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem, un pēc tam atlasiet **Apstrādāt**.</span><span class="sxs-lookup"><span data-stu-id="9c533-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="9c533-116">Lai noformētu datu bāzes vaicājumu, kas ielādē noteiktu budžetu kopu rūtī, atlasiet **Izgūt atlasītos budžetus**.</span><span class="sxs-lookup"><span data-stu-id="9c533-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="9c533-117">Lai iegūtu papildinformāciju par noteiktu rindu rūtī, atlasiet rindu un pēc tam atlasiet opciju **Skatīt budžeta detaļas** vai **Skatīt kontus**.</span><span class="sxs-lookup"><span data-stu-id="9c533-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="9c533-118">Paliekošo budžeta summu pārcelšana</span><span class="sxs-lookup"><span data-stu-id="9c533-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="9c533-119">Apstrādājot atlikušās budžeta summas, var izveidot darbības virsgrāmatā tām summām, kuras tiek pārceltas.</span><span class="sxs-lookup"><span data-stu-id="9c533-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="9c533-120">Lai izveidotu virsgrāmatas transakcijas, veiciet sadaļā [Budžeta summu pārcelšana un virsgrāmatas transakciju izveide](#carry-forward) norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9c533-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="9c533-121">Budžeta summas, kas tiek pārceltas, tiek pārvietotas uz budžeta modeli, kas ir atlasīts lapā **Budžeta modeļi** kā pārcēluma prognozes modelis.</span><span class="sxs-lookup"><span data-stu-id="9c533-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="9c533-122">Budžeta summu pārcelšana un virsgrāmatas transakciju izveide</span><span class="sxs-lookup"><span data-stu-id="9c533-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="9c533-123">Atlasiet **Projekta pārvaldība un uzskaite** > **Periodisks** > **Budžeti** > **Pārcelt budžetus**.</span><span class="sxs-lookup"><span data-stu-id="9c533-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="9c533-124">Lapā **Projekta budžeta pārcelšanas process** atlasiet **Gada beigas** un pēc tam iespējojiet **Pārcelt atlikušās projekta budžeta summas** un **Izveidot budžeta reģistra ierakstus virsgrāmatā**.</span><span class="sxs-lookup"><span data-stu-id="9c533-124">On the **Project budget carry-forward process** page, select **Year-end** , and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="9c533-125">Cilnes **Parametri** lauku grupā **Projekta parametri** atlasiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9c533-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="9c533-126">**Projekta budžeta gads** : atlasiet tā finanšu gada sākumu, kuram vēlaties skatīt atlikušās budžeta summas.</span><span class="sxs-lookup"><span data-stu-id="9c533-126">**Project budget year** : Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="9c533-127">**Peļņa un zaudējumi** : izveidojiet peļņas un zaudējumu transakciju virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="9c533-127">**Profit and loss** : Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="9c533-128">**NP** : izveidojiet Nepabeigtie projekti (NP) transakcijas virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="9c533-128">**WIP** : Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="9c533-129">**Alga** : izveidojiet algu sadalījuma transakcijas virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="9c533-129">**Payroll** : Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="9c533-130">Lauku grupā **Virsgrāmata** norādiet šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="9c533-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="9c533-131">Laukā **Aktuālais finanšu gads** atlasiet finanšu gadu, uz kuru jāpārceļ atlikušās projektu budžeta summas..</span><span class="sxs-lookup"><span data-stu-id="9c533-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="9c533-132">Noklusējuma vērtība ir viens gads pēc vērtības laukā **Projekta budžeta gads**.</span><span class="sxs-lookup"><span data-stu-id="9c533-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="9c533-133">Laukā **Pārcelšanas periods** atlasiet periodu, kuram vēlaties izveidot budžeta reģistra detalizētu informāciju virsgrāmatai.</span><span class="sxs-lookup"><span data-stu-id="9c533-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="9c533-134">Parasti tas ir sākuma finanšu gada pirmais periods.</span><span class="sxs-lookup"><span data-stu-id="9c533-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="9c533-135">Lauku grupā **Kopēt no/uz** norādiet šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="9c533-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="9c533-136">Laukā **No prognozes modeļa** atlasiet projekta budžeta prognožu modeli, kas saistīts ar atlikušajām budžeta summām, kuras vēlaties pārsūtīt projektiem.</span><span class="sxs-lookup"><span data-stu-id="9c533-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="9c533-137">Laukā **Uz virsgrāmatas budžeta modeli** atlasiet virsgrāmatas budžeta modeli, kas saistīts ar budžeta summām, kuras vēlaties pārcelt uz virsgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="9c533-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="9c533-138">Atlasiet **Pārsūtīt pārdošanas valūtu** , lai izmantotu projekta pārdošanas valūtu virsgrāmatas transakcijām, kas tiek izveidotas, pārsūtot projektu budžeta summas.</span><span class="sxs-lookup"><span data-stu-id="9c533-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="9c533-139">Ja opcija nav atlasīta, darbības izmanto uzskaites valūtu.</span><span class="sxs-lookup"><span data-stu-id="9c533-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="9c533-140">Atlasiet **Rādīt nulli atlikušo** , lai iekļautu projektus, kuriem nav atlikušo budžeta summu, bet kuri atbilst citiem kritērijiem, kas atlasīti apakšējā rūtī redzamajos projektos.</span><span class="sxs-lookup"><span data-stu-id="9c533-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="9c533-141">Cilnē **Atlasīt budžetus** atlasiet **Izgūt visus budžetus** , lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="9c533-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="9c533-142">Ja vēlaties izveidot datu bāzes vaicājumu, kas ielādē noteiktu projektu budžetu kopu rūtī, atlasiet **Izgūt atlasītos budžetus**.</span><span class="sxs-lookup"><span data-stu-id="9c533-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="9c533-143">Katram projektam, kuru vēlaties apstrādāt, atlasiet opciju projekta rindas sākumā.</span><span class="sxs-lookup"><span data-stu-id="9c533-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="9c533-144">Lai atlasītu visus vai lielāko daļu projektu, atzīmējiet atlases rūtiņu augšējā augšējā kreisajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="9c533-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="9c533-145">Lai izslēgtu jebkura projekta apstrādi, noņemiet atzīmi šim projektam.</span><span class="sxs-lookup"><span data-stu-id="9c533-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="9c533-146">Lai pārceltu atlikušo budžeta summu atlasītajiem projektiem uz atlasīto finanšu gadu un izveidotu budžeta reģistra detaļas virsgrāmatā, atlasiet **Apstrādāt**.</span><span class="sxs-lookup"><span data-stu-id="9c533-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="9c533-147">Budžeta summu pārcelšana, neveidojot virsgrāmatas darbības</span><span class="sxs-lookup"><span data-stu-id="9c533-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="9c533-148">Dodieties uz **Projekta pārvaldība un uzskaite** > **Periodisks** > **Budžeti** > **Pārcelt budžetus**.</span><span class="sxs-lookup"><span data-stu-id="9c533-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="9c533-149">Lapas **Projekta budžeta pārcelšanas process** laukā **Gada beigu opcijas** atlasiet opciju **Pārcelt atlikušās projekta budžeta summas**.</span><span class="sxs-lookup"><span data-stu-id="9c533-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="9c533-150">Grupas **Parametri** laukā **Projekta budžeta gads** atlasiet finanšu gadu, kuram vēlaties skatīt atlikušo budžeta summu.</span><span class="sxs-lookup"><span data-stu-id="9c533-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="9c533-151">Grupā **Kopēt no/uz** norādiet šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="9c533-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="9c533-152">Laukā **No prognozes modeļa** atlasiet projekta budžeta prognožu modeli, kas ir saistīts ar atlikušajām budžeta summām, kuras vēlaties pārcelt projektiem.</span><span class="sxs-lookup"><span data-stu-id="9c533-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="9c533-153">Atlasiet **Rādīt nulli atlikušo** ,lai iekļautu projektus, kuriem nav atlikušo budžeta summu, bet kuri atbilst citiem atlasītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="9c533-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="9c533-154">Grupā **Atlasīt budžetus** atlasiet **Izgūt visus budžetus** , lai ielādētu visus budžetus, kas atbilst atlasītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="9c533-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="9c533-155">Lai noformētu datu bāzes vaicājumu, kas ielādē noteiktu projektu budžetu kopu rūtī, atlasiet **Izgūt atlasītos budžetus**.</span><span class="sxs-lookup"><span data-stu-id="9c533-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="9c533-156">Katram projektam, kuru vēlaties apstrādāt, atlasiet opciju projekta rindas sākumā.</span><span class="sxs-lookup"><span data-stu-id="9c533-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="9c533-157">Atlasiet **Apstrādāt** , lai atlasītajiem projektiem pārceltu atlikušās budžeta summas atlasītajam finanšu gadam.</span><span class="sxs-lookup"><span data-stu-id="9c533-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

