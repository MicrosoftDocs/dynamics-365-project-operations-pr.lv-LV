---
title: Kredītkaršu iesniegšanas iestatīšana
description: Šajā tēmā izskaidrots, kā strādāt ar izmaksi kredītkartes transakcijām.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866692"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="a90a8-103">Kredītkaršu iesniegšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a90a8-103">Set up credit card integration</span></span>

<span data-ttu-id="a90a8-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="a90a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a90a8-105">Ar izdevumiem saistītas kredītkaršu transakcijas var iestatīt tā, lai tās tiek automātiski importētas periodiskā grafikā.</span><span class="sxs-lookup"><span data-stu-id="a90a8-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="a90a8-106">Transakcijas var arī manuāli importēt pēc to nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="a90a8-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="a90a8-107">Kredītkaršu transakcijas tiek importētas, izmantojot kredītkaršu transakciju datu entitīju.</span><span class="sxs-lookup"><span data-stu-id="a90a8-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="a90a8-108">Kredītkaršu transakciju importēšana</span><span class="sxs-lookup"><span data-stu-id="a90a8-108">Import credit card transactions</span></span>

<span data-ttu-id="a90a8-109">Lai importētu kredītkartes transakcijas, veiciet šīs darbības:</span><span class="sxs-lookup"><span data-stu-id="a90a8-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="a90a8-110">Lapā **Kredītkaršu transakcijas** atlasiet **Importēt transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="a90a8-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="a90a8-111">Ja datu pārvaldību atverat pirmoreiz, sistēmai ir jāatjaunina datu entitīju saraksts, iekams varat turpināt darbu.</span><span class="sxs-lookup"><span data-stu-id="a90a8-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="a90a8-112">Laukā **Nosaukums** ievadiet unikālu importēšanas uzdevuma aprakstu.</span><span class="sxs-lookup"><span data-stu-id="a90a8-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="a90a8-113">Laukā **Avotdatu formāts** atlasiet formātu failam, kas satur importējamās kredītkaršu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a90a8-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="a90a8-114">Atlasiet **Augšupielādēt** un pēc tam atrodiet un atlasiet importējamo failu.</span><span class="sxs-lookup"><span data-stu-id="a90a8-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="a90a8-115">Kad faila augšupielāde ir pabeigta, validējiet kredītkaršu transakcijas faila kartēšanu un kredītkaršu transakciju datu entitījas kolonnas, elementā atzīmējot saiti **Skatīt karti**.</span><span class="sxs-lookup"><span data-stu-id="a90a8-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="a90a8-116">Ja ir kartēšanas kļūdas vai ja jums ir jāmaina kartējums, veiciet kartēšanas kļūdas vai nu cilnē **Kartēšanas vizualizācija** vai **Kartēšanas informācija**.</span><span class="sxs-lookup"><span data-stu-id="a90a8-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="a90a8-117">Lai automatizētu kredītkaršu transakcijas, atlasiet **Izveidot periodisku datu uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="a90a8-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="a90a8-118">Pēc tam varat iestatīt periodiskumu, kas nosaka, cik bieži kredītkaršu transakcijas vajadzētu importēt.</span><span class="sxs-lookup"><span data-stu-id="a90a8-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="a90a8-119">Kad esat pabeidzis, noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a90a8-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="a90a8-120">Lai tūlīt importētu atlasīto failu, atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="a90a8-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="a90a8-121">Ja importēšanas laikā rodas kļūdas, varat skatīt izpildes žurnālu vai izvietošanas datus, lai redzētu novēršamās kļūdas un nodrošinātu veiksmīgu importēšanu.</span><span class="sxs-lookup"><span data-stu-id="a90a8-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="a90a8-122">Ja ir jāimportē vairāki failu formāti, katram formāta tipam ir jāizveido atsevišķi importēšanas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="a90a8-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="a90a8-123">Kredītkaršu transakciju atkārtota piešķiršana darbiniekiem, ar kuriem pārtrauktas darba attiecības</span><span class="sxs-lookup"><span data-stu-id="a90a8-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="a90a8-124">Pēc tam, kad ir pārtraukts darbinieka ieraksts, darbinieka Active Directory Domain Services (AD DS) konts tiek atspējots.</span><span class="sxs-lookup"><span data-stu-id="a90a8-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="a90a8-125">Taču var būt aktīvas kredītkaršu transakcijas, kurām joprojām jāpiešķir izdevumi un kuras jāatlīdzina.</span><span class="sxs-lookup"><span data-stu-id="a90a8-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="a90a8-126">Lapā **Kredītkartes transakcijas** varat atkārtoti piešķirt darbinieku jebkurai kredītkartes transakcijai, no kuras ir noņemts saistītais darbinieks.</span><span class="sxs-lookup"><span data-stu-id="a90a8-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="a90a8-127">Atlasiet vienu vai vairākas kredītkaršu transakcijas un pēc tam atlasiet **Piešķirt transakcijas atkārtoti**.</span><span class="sxs-lookup"><span data-stu-id="a90a8-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="a90a8-128">Pēc tam varat atlasīt citu darbinieku, kuram piešķirt kredītkaršu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a90a8-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="a90a8-129">Pēc kredītkaršu transakciju atkārtotas piešķires tās var atlasīt izdevumu atskaitei un apmaksāt, izmantojot ierasto izdevumu atskaites atlīdzināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="a90a8-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="a90a8-130">Kredītkartes transakciju dzēšana</span><span class="sxs-lookup"><span data-stu-id="a90a8-130">Delete credit card transactions</span></span> 

<span data-ttu-id="a90a8-131">Dažkārt pēc kredītkartes transakciju importēšanas var būt nepieciešams dzēst noteiktas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="a90a8-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="a90a8-132">Tas var būt tāpēc, ka transakcijām ir dublikāti vai dati nav precīzi.</span><span class="sxs-lookup"><span data-stu-id="a90a8-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="a90a8-133">Administratori var izmantot līdzekli **Dzēst kredītkartes transakcijas**, lai atlasītu un dzēstu kredītkartesthat transakcijas, kas **nav saidtītas** ar izdevumu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="a90a8-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="a90a8-134">Atveriet **Periodiski uzdevumi** > **Dzēst kredītkartes transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="a90a8-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="a90a8-135">Atlasiet **Filtrēt** un norādiet informāciju, lai identificētu iekļaujamos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a90a8-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="a90a8-136">Lai dzēstu ierakstus, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a90a8-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
