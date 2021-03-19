---
title: Ar apstiprinātiem laika un izdevumu ierakstiem izveidoto faktisko ierakstu lielapjoma korekcija
description: Šajā tēmā ir paskaidrots, kā administrators var veikt vienu vai vairākus iepriekš apstiprinātu laika vai izdevumu ierakstu labojumus, ja norēķini nav pabeigti.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 17d6648840e27a4e573985af2cdd74c4adf878e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290908"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="e98ec-103">Ar apstiprinātiem laika un izdevumu ierakstiem izveidoto faktisko ierakstu lielapjoma korekcija</span><span class="sxs-lookup"><span data-stu-id="e98ec-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e98ec-104">Dažreiz laiks vai izdevumu ieraksts var būt ievadīts nepareizi.</span><span class="sxs-lookup"><span data-stu-id="e98ec-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="e98ec-105">Piemēram, konsultants var atlasīt nepareizu datumu, kad tiek izveidots laika ieraksts, vai arī var apmainīt vietām skaitļus, kad tiek ievadīti izdevumi.</span><span class="sxs-lookup"><span data-stu-id="e98ec-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="e98ec-106">Ja konsultants nevar koriģēt iesniegtos ierakstus, administrators var tieši labot projekta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e98ec-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="e98ec-107">Lai izpildītu šajā tēmā aprakstītās procedūras, jums ir nepieciešamas administratora atļaujas.</span><span class="sxs-lookup"><span data-stu-id="e98ec-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="e98ec-108">Apstiprinātu laika ierakstu labošana</span><span class="sxs-lookup"><span data-stu-id="e98ec-108">Correct approved time entries</span></span>     

<span data-ttu-id="e98ec-109">Izpildiet tālāk aprakstītās darbības, lai labotu vienu vai vairākus projekta laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="e98ec-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="e98ec-110">Apgabalā **Pārdošana** atlasiet **Transakcijas** un pēc tam atlasiet **Apstiprinātais laiks**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="e98ec-111">Sarakstā **Apstiprinātais laiks** atrodiet un atlasiet vienu vai vairākus koriģējamos apstiprinātos laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="e98ec-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="e98ec-112">Lai atrastu saistītos ierakstus, varat izmantot filtru.</span><span class="sxs-lookup"><span data-stu-id="e98ec-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="e98ec-113">Piemēram, varat filtrēt pēc projekta ID un atlasīt visus apstiprinātos laika ierakstus ar attiecīgo projekta ID.</span><span class="sxs-lookup"><span data-stu-id="e98ec-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="e98ec-114">Atlasiet **Labot ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-114">Select **Correct entries**.</span></span> <span data-ttu-id="e98ec-115">Automātiski tiek izveidots jauns labojumu žurnāls, kuram tiek piešķirts tips **Laika korekcija**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="e98ec-116">Atlasītie ieraksti tiek pievienoti žurnālam.</span><span class="sxs-lookup"><span data-stu-id="e98ec-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="e98ec-117">Lapā **Jaunais žurnāls** ievadiet labojumu žurnāla **Aprakstu** un pēc tam atlasiet cilni **Laika ierakstu korekcijas**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="e98ec-118">Sadaļā **Jaunas vērtības laika ierakstiem** atjauniniet laukus ar pareizo informāciju, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="e98ec-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="e98ec-119">Piemēram, var mainīt piešķirto projektu vai rezervējamo resursu.</span><span class="sxs-lookup"><span data-stu-id="e98ec-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="e98ec-120">Atlasiet **Priekšskatīt**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-120">Select **Preview**.</span></span> <span data-ttu-id="e98ec-121">Dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="e98ec-122">Cilnē **Žurnāla rindas** varat skatīt sākotnējo faktisko ierakstu sarakstu, kas ir saistīti ar atlasītajiem laika ierakstiem, kuri tika apvērsti, un labotajām atbilstošajām rindām, kas tika izveidotas.</span><span class="sxs-lookup"><span data-stu-id="e98ec-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="e98ec-123">Ja ir jāveic papildu labojumi, atkārtojiet 5. un 6. darbību.</span><span class="sxs-lookup"><span data-stu-id="e98ec-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="e98ec-124">Visiem koriģētajiem faktiskajiem ierakstiem ir tādas pašas vērtības, kādas atlasījāt sadaļā **Jaunas vērtības laika ierakstiem**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="e98ec-125">Ja labojumi tiek parādīti, kā paredzēts, atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="e98ec-126">Dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="e98ec-127">Atgriezieties apgabalā **Pārdošana**, atlasiet lapu **Projekti** un pēc tam atveriet projektu, kura laika ierakstus tikko labojāt.</span><span class="sxs-lookup"><span data-stu-id="e98ec-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="e98ec-128">Lapas **Projekti** cilnē **Faktiskās vērtības** skatiet veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="e98ec-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="e98ec-129">Ja cilne **Faktiskās vērtības** nav redzama, atlasiet **Saistīts** > **Faktiskās vērtības**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="e98ec-130">Sarakstā **Faktiskais saistītais skats** ir redzams, ka joprojām tiek parādīti apvērstie sākotnējie laika ieraksti, kā arī atbilstošie koriģētie laika ieraksti.</span><span class="sxs-lookup"><span data-stu-id="e98ec-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="e98ec-131">Piemēram, tālāk redzamajā grafikā ir divi rindas elementi ar daudzumu 8,00, kam ir debets kolonnā Summa.</span><span class="sxs-lookup"><span data-stu-id="e98ec-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="e98ec-132">Turklāt ir divi rindas elementi ar daudzumu 8,00, kam ir kredīta summas kolonnā Summa.</span><span class="sxs-lookup"><span data-stu-id="e98ec-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="e98ec-133">Šīs korekcijas ienes daudzumu nulle.</span><span class="sxs-lookup"><span data-stu-id="e98ec-133">These corrections bring the quantity to zero.</span></span>

![Faktiskais saistīto skatu saraksts](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="e98ec-135">Apstiprinātu izdevumu ierakstu labošana</span><span class="sxs-lookup"><span data-stu-id="e98ec-135">Correct approved expense entries</span></span>

<span data-ttu-id="e98ec-136">Izpildiet tālāk aprakstītās darbības, lai labotu vienu vai vairākus izdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="e98ec-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="e98ec-137">Apgabala **Pārdošana** sadaļas **Transakcijas** kreisās puses navigācijas rūtī atlasiet **Apstiprinātie izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="e98ec-138">Sarakstā **Apstiprinātie izdevumi** atlasiet koriģējamo projektu un pēc tam atlasiet **Labot ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="e98ec-139">Automātiski tiek izveidots jauns labojumu žurnāls, kuram tiek piešķirts tips **Izdevumu korekcija**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="e98ec-140">Lapā **Jauns žurnāls** ievadiet labojuma **Aprakstu** un sadaļas **Jaunas vērtības izdevumiem** cilnē **Izdevumu korekcija** atlasiet tos datu laukus, ko vēlaties labot atlasītajām izdevumu rindām.</span><span class="sxs-lookup"><span data-stu-id="e98ec-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="e98ec-141">Piemēram, varat piešķirt izdevumus citam vienumam **Projekts** vai labot vienumus **Izdevumu kategorija**, **Izdevumu datums** vai **Rezervējams resurss**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="e98ec-142">Atlasiet **Priekšskatīt**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-142">Select **Preview**.</span></span> <span data-ttu-id="e98ec-143">Dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="e98ec-144">Pārbaudiet cilnē **Žurnāla rindas** veiktos labojumus. Varat skatīt sākotnējo faktisko ierakstu sarakstu, kas ir saistīti ar atlasītajiem izdevumu ierakstiem, kuri tika apvērsti, un labotajām atbilstošajām rindām, kas tika izveidotas.</span><span class="sxs-lookup"><span data-stu-id="e98ec-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="e98ec-145">Ja labotās vērtības tiek parādītas, kā paredzēts, atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="e98ec-146">Dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="e98ec-147">Ja vērtības netiek rādītas, kā paredzēts, atlasiet **Atcelt**, lai atgrieztos sarakstā **Apstiprinātie izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="e98ec-148">Atkārtojiet 2.–5. darbību.</span><span class="sxs-lookup"><span data-stu-id="e98ec-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="e98ec-149">Koriģētajiem faktiskajiem ierakstiem ir tādas pašas vērtības, kādas atlasījāt sadaļā **Jaunas vērtības izdevumiem**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="e98ec-150">Kad apstiprināsiet labojumu žurnālu, pārejiet atpakaļ uz atjaunināto projektu vai projektiem, lai skatītu veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="e98ec-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="e98ec-151">Cilnes **Faktiskās vērtības** projekta lapā pārskatiet skatu **Faktiskais saistītais skats**.</span><span class="sxs-lookup"><span data-stu-id="e98ec-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="e98ec-152">Tiek parādīti sākotnējie ieraksti un labotie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="e98ec-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="e98ec-153">Tālāk redzamajā attēlā ir parādītas izdevumu ieraksta sākotnējās summas un atbilstošās koriģētās izmaksu ierakstu summas.</span><span class="sxs-lookup"><span data-stu-id="e98ec-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Izdevumu ieraksta sākotnējās summas](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]