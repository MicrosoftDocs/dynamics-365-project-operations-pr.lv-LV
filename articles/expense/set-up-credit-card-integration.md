---
title: Kredītkaršu iesniegšanas iestatīšana
description: Šajā tēmā paskaidrots, kā importēt un uzturēt izdevumu kredītkaršu transakcijas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276177"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="4a2ee-103">Kredītkaršu iesniegšanas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4a2ee-103">Set up credit card integration</span></span>

<span data-ttu-id="4a2ee-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="4a2ee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4a2ee-105">Ar izdevumiem saistītas kredītkaršu transakcijas var iestatīt tā, lai tās tiek automātiski importētas periodiskā grafikā.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="4a2ee-106">Transakcijas var arī manuāli importēt pēc to nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="4a2ee-107">Kredītkaršu transakcijas tiek importētas, izmantojot kredītkaršu transakciju datu entitīju.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="4a2ee-108">Kredītkaršu transakciju importēšana</span><span class="sxs-lookup"><span data-stu-id="4a2ee-108">Import credit card transactions</span></span>

1. <span data-ttu-id="4a2ee-109">Lapā **Kredītkaršu transakcijas** atlasiet **Importēt transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="4a2ee-110">Ja datu pārvaldību atverat pirmoreiz, sistēmai ir jāatjaunina datu entitīju saraksts, iekams varat turpināt darbu.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="4a2ee-111">Laukā **Nosaukums** ievadiet importēšanas darba unikālo aprakstu.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="4a2ee-112">Laukā **Avotdatu formāts** atlasiet formātu failam, kas satur importējamās kredītkaršu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="4a2ee-113">Atlasiet **Augšupielādēt** un pēc tam atrodiet un atlasiet importējamo failu.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="4a2ee-114">Kad faila augšupielāde ir pabeigta, validējiet kredītkaršu transakcijas faila kartēšanu un kredītkaršu transakciju datu entitījas kolonnas, elementā atzīmējot saiti **Skatīt karti**.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="4a2ee-115">Ja ir kartēšanas kļūdas vai ja jums ir jāmaina kartējums, veiciet kartēšanas kļūdas vai nu cilnē **Kartēšanas vizualizācija** vai **Kartēšanas informācija**.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="4a2ee-116">Lai automatizētu kredītkaršu transakcijas, atlasiet **Izveidot periodisku datu uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="4a2ee-117">Pēc tam varat iestatīt periodiskumu, kas nosaka, cik bieži kredītkaršu transakcijas vajadzētu importēt.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="4a2ee-118">Kad esat pabeidzis, noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="4a2ee-119">Lai tūlīt importētu atlasīto failu, atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="4a2ee-120">Ja importēšanas laikā rodas kļūdas, varat skatīt izpildes žurnālu vai sagatavošanas posmu datus, lai redzētu kļūdas, kuras jānovērš, lai garantētu sekmīgu importēšanu.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="4a2ee-121">Ja ir jāimportē vairāk nekā viens faila formāts, ir jāizveido atsevišķi importēšanas uzdevumi katram formāta veidam.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="4a2ee-122">Kredītkaršu transakciju atkārtota piešķiršana darbiniekiem, ar kuriem pārtrauktas darba attiecības</span><span class="sxs-lookup"><span data-stu-id="4a2ee-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="4a2ee-123">Pēc tam, kad ir pārtraukts darbinieka ieraksts, darbinieka Active Directory Domain Services (AD DS) konts tiek atspējots.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="4a2ee-124">Taču var būt aktīvas kredītkaršu transakcijas, kurām joprojām jāpiešķir izdevumi un kuras jāatlīdzina.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="4a2ee-125">Lapā **Kredītkaršu transakcijas** varat atkārtoti piešķirt darbinieku jebkurai kredītkaršu transakcijai, ja ir pārtrauktas darba attiecības ar saistīto darbinieku.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="4a2ee-126">Atlasiet vienu vai vairākas kredītkaršu transakcijas un pēc tam atlasiet **Piešķirt transakcijas atkārtoti**.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="4a2ee-127">Pēc tam varat atlasīt citu darbinieku, kuram piešķirt kredītkaršu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="4a2ee-128">Pēc kredītkaršu transakciju atkārtotas piešķires tās var atlasīt izdevumu atskaitei un apmaksāt, izmantojot ierasto izdevumu atskaites atlīdzināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="4a2ee-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]