---
title: Kredītkaršu darījumu importēšana un uzturēšana
description: Šajā tēmā paskaidrots, kā importēt un uzturēt izdevumu kredītkaršu transakcijas. Šos darījumus var iestatīt tā, lai tie tiktu automātiski importēti pēc periodiska grafika, vai arī tos var importēt manuāli pēc nepieciešamības.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080597"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="1f2f9-104">Kredītkaršu darījumu importēšana un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="1f2f9-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f2f9-105">Ar izdevumiem saistītas kredītkaršu transakcijas var iestatīt tā, lai tās tiek automātiski importētas periodiskā grafikā.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="1f2f9-106">Transakcijas var arī manuāli importēt pēc to nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="1f2f9-107">Kredītkaršu transakcijas tiek importētas, izmantojot kredītkaršu transakciju datu entitīju.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="1f2f9-108">Papildinformāciju par datu entītijām skatiet rakstā [Datu entītijas](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="1f2f9-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="1f2f9-109">Kredītkaršu transakciju importēšana</span><span class="sxs-lookup"><span data-stu-id="1f2f9-109">Import credit card transactions</span></span>

1. <span data-ttu-id="1f2f9-110">Lapā **Kredītkaršu transakcijas** atlasiet **Importēt transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="1f2f9-111">Ja datu pārvaldību atverat pirmoreiz, sistēmai ir jāatjaunina datu entitīju saraksts, iekams varat turpināt darbu.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="1f2f9-112">Laukā **Nosaukums** ievadiet importēšanas darba unikālo aprakstu.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="1f2f9-113">Laukā **Avotdatu formāts** atlasiet formātu failam, kas satur importējamās kredītkaršu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="1f2f9-114">Atlasiet **Augšupielādēt** un pēc tam atrodiet un atlasiet importējamo failu.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-114">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="1f2f9-115">Kad faila augšupielāde ir pabeigta, validējiet kredītkaršu transakcijas faila kartēšanu un kredītkaršu transakciju datu entitījas kolonnas, elementā atzīmējot saiti **Skatīt karti**.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="1f2f9-116">Ja ir kartēšanas kļūdas vai ja jums ir jāmaina kartējums, veiciet kartēšanas kļūdas vai nu cilnē **Kartēšanas vizualizācija** vai **Kartēšanas informācija**.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="1f2f9-117">Lai automatizētu kredītkaršu transakcijas, atlasiet **Izveidot periodisku datu uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="1f2f9-118">Pēc tam varat iestatīt periodiskumu, kas nosaka, cik bieži kredītkaršu transakcijas vajadzētu importēt.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="1f2f9-119">Kad esat pabeidzis, noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="1f2f9-120">Lai tūlīt importētu atlasīto failu, atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="1f2f9-121">Ja importēšanas laikā rodas kļūdas, varat skatīt izpildes žurnālu vai sagatavošanas posmu datus, lai redzētu kļūdas, kuras jānovērš, lai garantētu sekmīgu importēšanu.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="1f2f9-122">Ja ir jāimportē vairāk nekā viens faila formāts, ir jāizveido atsevišķi importēšanas uzdevumi katram formāta veidam.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="1f2f9-123">Kredītkaršu transakciju atkārtota piešķiršana darbiniekiem, ar kuriem pārtrauktas darba attiecības</span><span class="sxs-lookup"><span data-stu-id="1f2f9-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="1f2f9-124">Pēc tam, kad ir pārtraukts darbinieka ieraksts, darbinieka Active Directory Domain Services (AD DS) konts tiek atspējots.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="1f2f9-125">Taču var būt aktīvas kredītkaršu transakcijas, kurām joprojām jāpiešķir izdevumi un kuras jāatlīdzina.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="1f2f9-126">Lapā **Kredītkaršu transakcijas** varat atkārtoti piešķirt darbinieku jebkurai kredītkaršu transakcijai, ja ir pārtrauktas darba attiecības ar saistīto darbinieku.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="1f2f9-127">Atlasiet vienu vai vairākas kredītkaršu transakcijas un pēc tam atlasiet **Piešķirt transakcijas atkārtoti**.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="1f2f9-128">Pēc tam varat atlasīt citu darbinieku, kuram piešķirt kredītkaršu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="1f2f9-129">Pēc kredītkaršu transakciju atkārtotas piešķires tās var atlasīt izdevumu atskaitei un apmaksāt, izmantojot ierasto izdevumu atskaites atlīdzināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="1f2f9-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>