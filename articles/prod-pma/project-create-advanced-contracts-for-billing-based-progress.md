---
title: Rēķinu izveidošanas papildu līgumi, pamatojoties uz norisi
description: Šajā tēmā izskaidrots, kā izveidot projekta līgumus, lai varētu ģenerēt klientiem rēķinus, par pamatu izmantojot pabeigtā darba procentus.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999680"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="094d7-103">Rēķinu izveidošanas papildu līgumi, pamatojoties uz norisi</span><span class="sxs-lookup"><span data-stu-id="094d7-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="094d7-104">Šajā tēmā izskaidrots, kā izveidot projekta līgumus, lai varētu izveidot klientiem rēķinus, par pamatu izmantojot pabeigtā darba procentus.</span><span class="sxs-lookup"><span data-stu-id="094d7-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="094d7-105">Rēķina summas automātiski tiek aprēķinātas budžeta darba kategorijām, kas ir iestatītas projektam.</span><span class="sxs-lookup"><span data-stu-id="094d7-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="094d7-106">Rēķina laiks tiek iestatīts, vienojoties par projekta līgumu ar klientu.</span><span class="sxs-lookup"><span data-stu-id="094d7-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="094d7-107">Izmantojiet šajā tēmā norādītās darbības, lai iestatītu līgumu, saistīto projektu un rēķinu noteikumus, kas aprēķina rēķinu summas projektam iestatītajām budžeta kategorijām.</span><span class="sxs-lookup"><span data-stu-id="094d7-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="094d7-108">Pēc tam, kad esat izveidojis līgumu un projektu, varat iestatīt detalizētu informāciju par projektu.</span><span class="sxs-lookup"><span data-stu-id="094d7-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="094d7-109">Piemēram, var definēt aktivitātes un piešķirt darbiniekiem projektu.</span><span class="sxs-lookup"><span data-stu-id="094d7-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="094d7-110">Piemērs</span><span class="sxs-lookup"><span data-stu-id="094d7-110">Example</span></span>

<span data-ttu-id="094d7-111">Jūsu organizācija ir programmatūras izstrādes uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="094d7-111">Your organization is a software development firm.</span></span> <span data-ttu-id="094d7-112">Jūs piekrītat izveidot algu uzskaites pakotni klientam par kopējo maksu 20 000 ASV dolāri (USD).</span><span class="sxs-lookup"><span data-stu-id="094d7-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="094d7-113">Jūsu uzņēmums piekrīt izrakstīt rēķinu klientam, kad pabeigsit noteiktu projekta procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="094d7-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="094d7-114">Darbam iestatiet tālāk norādītās projekta kategorijas, lai tās varētu izmantot norēķinu procesā.</span><span class="sxs-lookup"><span data-stu-id="094d7-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="094d7-115">Vairumtirdzniecība un mazumtirdzniecība; automobiļu un motociklu remonts</span><span class="sxs-lookup"><span data-stu-id="094d7-115">Consulting</span></span>
- <span data-ttu-id="094d7-116">Dizains</span><span class="sxs-lookup"><span data-stu-id="094d7-116">Design</span></span>
- <span data-ttu-id="094d7-117">Instalēšana</span><span class="sxs-lookup"><span data-stu-id="094d7-117">Installation</span></span>

<span data-ttu-id="094d7-118">Jūs iestatāt arī norēķinu kārtulas, kuras automātiski aprēķina rēķina summas par katrai kategorijai izpildīto projekta daļu.</span><span class="sxs-lookup"><span data-stu-id="094d7-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="094d7-119">Budžeta pārvaldnieks izveido budžetu projekta kategorijām.</span><span class="sxs-lookup"><span data-stu-id="094d7-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="094d7-120">Pabeigtā darba apjoms automātiski tiek aprēķināts procentos no faktiskā darba apjoma salīdzinājumā ar budžetā paredzētajām summām.</span><span class="sxs-lookup"><span data-stu-id="094d7-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="094d7-121">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="094d7-121">Prerequisites</span></span>

<span data-ttu-id="094d7-122">Pirms izveidojat projektu, kurā tiek izmantotas norēķinu kārtulas, iestatiet numuru sērijas norēķinu kārtulām un maksas žurnālu, kas tiek izmantots, lai grāmatotu progresa rēķinus.</span><span class="sxs-lookup"><span data-stu-id="094d7-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="094d7-123">Dodieties uz **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Projekta pārvaldības un grāmatvedības parametri**.</span><span class="sxs-lookup"><span data-stu-id="094d7-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="094d7-124">Lapas **Projekta pārvaldība un uzskaites parametri** cilnē **Numuru sērijas** iestatiet to numuru sēriju, ko vēlaties izmantot, veidojot rēķina kārtulas.</span><span class="sxs-lookup"><span data-stu-id="094d7-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="094d7-125">Dodieties uz **Projekta pārvaldība un uzskaite** \> **Žurnāli** \> **Izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="094d7-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="094d7-126">Lapā **Izmaksu žurnāls** atlasiet **Jauns** un ievadiet žurnāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="094d7-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="094d7-127">Līgumu par norises rēķinu izpildi izveide</span><span class="sxs-lookup"><span data-stu-id="094d7-127">Create a contract for progress billings</span></span>

<span data-ttu-id="094d7-128">Veiciet šīs darbības, lai izveidotu projekta līgumu fiksētas cenas projektam.</span><span class="sxs-lookup"><span data-stu-id="094d7-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="094d7-129">Projekta rēķins tiek veidots, kad projektā pabeigtais darbs sasniedz norādīto procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="094d7-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="094d7-130">Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Projekta līgumi**.</span><span class="sxs-lookup"><span data-stu-id="094d7-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="094d7-131">Lapā **Projekta līgumi** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="094d7-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="094d7-132">Dialoglodziņā **Jauns projekta līgums** iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="094d7-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="094d7-133">**Nosaukums**</span><span class="sxs-lookup"><span data-stu-id="094d7-133">**Name**</span></span>
    - <span data-ttu-id="094d7-134">**Finansēšanas veids**</span><span class="sxs-lookup"><span data-stu-id="094d7-134">**Funding type**</span></span>
    - <span data-ttu-id="094d7-135">**Finansējuma avots**</span><span class="sxs-lookup"><span data-stu-id="094d7-135">**Funding source**</span></span>
    - <span data-ttu-id="094d7-136">**Pārdošanas valūta** — pēc noklusējuma šī valūta tiek izmantota klienta rēķiniem, kas saistīti ar šo projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="094d7-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="094d7-137">Taču pārdošanas valūtu var mainīt noteiktam klienta rēķinam.</span><span class="sxs-lookup"><span data-stu-id="094d7-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="094d7-138">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="094d7-138">Select **OK**.</span></span> <span data-ttu-id="094d7-139">Šī informācija tiek kopēta lapā **Projekta līgumi**.</span><span class="sxs-lookup"><span data-stu-id="094d7-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="094d7-140">Lapā **Projekta līgumi** aizpildiet visu nepieciešamo projekta informāciju.</span><span class="sxs-lookup"><span data-stu-id="094d7-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="094d7-141">Projektu par norises rēķinu izpildi izveide</span><span class="sxs-lookup"><span data-stu-id="094d7-141">Create a project for progress billings</span></span>

<span data-ttu-id="094d7-142">Veiciet šīs darbības, lai izveidotu projektu un visus apakšprojektus, kas saistīti ar projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="094d7-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="094d7-143">Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="094d7-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="094d7-144">Lapā **Visi projekti** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="094d7-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="094d7-145">Dialoglodziņa **Jauns projekts** laukā **Projekta tips** atlasiet **Laiks un materiāls**.</span><span class="sxs-lookup"><span data-stu-id="094d7-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="094d7-146">Atlasiet projekta grupu.</span><span class="sxs-lookup"><span data-stu-id="094d7-146">Select a project group.</span></span> <span data-ttu-id="094d7-147">Projekta grupa definē grāmatošanas informāciju grupai piešķirtajiem projektiem.</span><span class="sxs-lookup"><span data-stu-id="094d7-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="094d7-148">Atlasiet **Izveidot projektu**.</span><span class="sxs-lookup"><span data-stu-id="094d7-148">Select **Create project**.</span></span>
6. <span data-ttu-id="094d7-149">Kad projekts ir izveidots, iestatiet projekta posmu **Notiek apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="094d7-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="094d7-150">Budžeta izveide projektam</span><span class="sxs-lookup"><span data-stu-id="094d7-150">Create a budget for a project</span></span>

<span data-ttu-id="094d7-151">Budžeta kategorijas tiek izmantotas, lai automātiski aprēķinātu rēķina summas katrai kategorijai pabeigtā darba procentuālajai daļai.</span><span class="sxs-lookup"><span data-stu-id="094d7-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="094d7-152">Lai izveidotu budžeta kategorijas paredzamajām izmaksām, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="094d7-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="094d7-153">Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="094d7-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="094d7-154">Lapā **Visi projekti** atlasiet vajadzīgo projektu un atveriet to.</span><span class="sxs-lookup"><span data-stu-id="094d7-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="094d7-155">Lapas **Projekti** darbību rūts cilnē **Plāns**, grupā **Budžets** atlasiet vienumu **Projekta budžets**.</span><span class="sxs-lookup"><span data-stu-id="094d7-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="094d7-156">Lapā **Projekta budžets** ievadiet prognozējamās izmaksas katrai projekta kategorijai.</span><span class="sxs-lookup"><span data-stu-id="094d7-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="094d7-157">Norēķinu kārtulu izveide progresa aprēķinam</span><span class="sxs-lookup"><span data-stu-id="094d7-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="094d7-158">Dodieties uz **Projekta pārvaldība un uzskaite** \> **Projekti** \> **Projekta līgumi**.</span><span class="sxs-lookup"><span data-stu-id="094d7-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="094d7-159">Lapā **Projekta līgumi** atlasiet un atveriet projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="094d7-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="094d7-160">Projekta līguma lapā, kopsavilkuma cilnē **Norēķinu kārtulas** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="094d7-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="094d7-161">Lapas **Norēķinu kārtulas** laukā **Rindas tips** atlasiet **Norise**.</span><span class="sxs-lookup"><span data-stu-id="094d7-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="094d7-162">Kopsavilkuma cilnes **Rēķina kārtulas rindas informācijā** laukā **Līguma vērtība** ievadiet līguma kopējo vērtību.</span><span class="sxs-lookup"><span data-stu-id="094d7-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="094d7-163">Laukā **Kategorija** atlasiet kategoriju, uz kuru grāmatot maksājuma darbību.</span><span class="sxs-lookup"><span data-stu-id="094d7-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="094d7-164">Laukā **Projekts** atlasiet projektu, kas izmanto šo norēķinu kārtulu.</span><span class="sxs-lookup"><span data-stu-id="094d7-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="094d7-165">Neobligāti: piešķiriet norēķinu kārtulu papildu projektiem.</span><span class="sxs-lookup"><span data-stu-id="094d7-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="094d7-166">Kopsavilkuma cilnes **Projekts** sadaļā **Pieejamie projekti** atlasiet projektu un pēc tam noklikšķiniet uz labās puses bultiņas, lai pievienotu projektu sadaļā **Atlasītie projekti**.</span><span class="sxs-lookup"><span data-stu-id="094d7-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="094d7-167">Neobligāti: aprēķiniet procentu summu, ko klients ietur no maksājuma rēķinā.</span><span class="sxs-lookup"><span data-stu-id="094d7-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="094d7-168">Attiecībā uz kopsavilkuma cilnes **Maksājuma saglabāšanas nosacījumi** atlasiet finansējuma avotu un pēc tam laukā **Ieturējuma procentuālā vērtība** ievadiet saglabāšanas procentus.</span><span class="sxs-lookup"><span data-stu-id="094d7-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="094d7-169">Lai projekta līgumam izveidotu papildu norēķinu kārtulas, atkārtojiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="094d7-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]