---
title: Korekciju žurnālu izveide un apstiprināšana
description: Šajā tēmā ir sniegta informācija par to, kā izveidot un apstiprināt labojumu žurnālu.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 855593df1ea14827f06961dda5b4becd2fa75c18
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080441"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="8ec5a-103">Korekciju žurnālu izveide un apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="8ec5a-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="8ec5a-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="8ec5a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8ec5a-105">Dažreiz laiks vai izdevumu ieraksts var būt ievadīts nepareizi.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="8ec5a-106">Piemēram, konsultants var atlasīt nepareizu datumu, kad tiek izveidots laika ieraksts, vai arī var apmainīt vietām skaitļus, kad tiek ievadīti izdevumi.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="8ec5a-107">Ja konsultants nevar koriģēt iesniegtos ierakstus, administrators var tieši labot projekta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="8ec5a-108">Lai izpildītu šajā tēmā aprakstītās procedūras, jums ir nepieciešamas administratora atļaujas.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="8ec5a-109">Apstiprinātu laika ierakstu labošana</span><span class="sxs-lookup"><span data-stu-id="8ec5a-109">Correct approved time entries</span></span>     

<span data-ttu-id="8ec5a-110">Izpildiet tālāk aprakstītās darbības, lai labotu vienu vai vairākus projekta laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="8ec5a-111">Apgabalā **Pārdošana** atlasiet **Transakcijas** un pēc tam atlasiet **Apstiprinātais laiks**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-111">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="8ec5a-112">Sarakstā **Apstiprinātais laiks** atrodiet un atlasiet vienu vai vairākus koriģējamos apstiprinātos laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="8ec5a-113">Lai atrastu saistītos ierakstus, varat izmantot filtru.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="8ec5a-114">Piemēram, varat filtrēt pēc projekta ID un atlasīt visus apstiprinātos laika ierakstus ar attiecīgo projekta ID.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="8ec5a-115">Atlasiet **Labot ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-115">Select **Correct entries**.</span></span> <span data-ttu-id="8ec5a-116">Automātiski tiek izveidots jauns labojumu žurnāls, kuram tiek piešķirts tips **Laika korekcija**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="8ec5a-117">Atlasītie ieraksti tiek pievienoti žurnālam.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="8ec5a-118">Lapā **Jaunais žurnāls** ievadiet labojumu žurnāla **Aprakstu** un pēc tam atlasiet cilni **Laika ierakstu korekcijas**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="8ec5a-119">Sadaļā **Jaunas vērtības laika ierakstiem** atjauniniet laukus ar pareizo informāciju, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="8ec5a-120">Piemēram, var mainīt piešķirto projektu vai rezervējamo resursu.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="8ec5a-121">Atlasiet **Priekšskatīt**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-121">Select **Preview**.</span></span> <span data-ttu-id="8ec5a-122">Dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="8ec5a-123">Cilnē **Žurnāla rindas** varat skatīt sākotnējo faktisko ierakstu sarakstu, kas ir saistīti ar atlasītajiem laika ierakstiem, kuri tika apvērsti, un labotajām atbilstošajām rindām, kas tika izveidotas.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="8ec5a-124">Ja ir jāveic papildu labojumi, atkārtojiet 5. un 6. darbību.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="8ec5a-125">Visiem koriģētajiem faktiskajiem ierakstiem ir tādas pašas vērtības, kādas atlasījāt sadaļā **Jaunas vērtības laika ierakstiem**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="8ec5a-126">Ja labojumi tiek parādīti, kā paredzēts, atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="8ec5a-127">Dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="8ec5a-128">Atgriezieties apgabalā **Pārdošana** , atlasiet lapu **Projekti** un pēc tam atveriet projektu, kura laika ierakstus tikko labojāt.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-128">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="8ec5a-129">Lapas **Projekti** cilnē **Faktiskās vērtības** skatiet veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="8ec5a-130">Ja cilne **Faktiskās vērtības** nav redzama, atlasiet **Saistīts** > **Faktiskās vērtības**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="8ec5a-131">Sarakstā **Faktiskais saistītais skats** ir redzams, ka joprojām tiek parādīti apvērstie sākotnējie laika ieraksti, kā arī atbilstošie koriģētie laika ieraksti.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="8ec5a-132">Piemēram, tālāk redzamajā grafikā ir divi rindas elementi ar daudzumu 8,00, kam ir debets kolonnā Summa.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="8ec5a-133">Turklāt ir divi rindas elementi ar daudzumu 8,00, kam ir kredīta summas kolonnā Summa.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="8ec5a-134">Šīs korekcijas ienes daudzumu nulle.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="8ec5a-135">Apstiprinātu izdevumu ierakstu labošana</span><span class="sxs-lookup"><span data-stu-id="8ec5a-135">Correct approved expense entries</span></span>

<span data-ttu-id="8ec5a-136">Izpildiet tālāk aprakstītās darbības, lai labotu vienu vai vairākus izdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="8ec5a-137">Apgabala **Pārdošana** sadaļas **Transakcijas** kreisās puses navigācijas rūtī atlasiet **Apstiprinātie izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="8ec5a-138">Sarakstā **Apstiprinātie izdevumi** atlasiet koriģējamo projektu un pēc tam atlasiet **Labot ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="8ec5a-139">Automātiski tiek izveidots jauns labojumu žurnāls, kuram tiek piešķirts tips **Izdevumu korekcija**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="8ec5a-140">Lapā **Jauns žurnāls** ievadiet labojuma **Aprakstu** un sadaļas **Jaunas vērtības izdevumiem** cilnē **Izdevumu korekcija** atlasiet tos datu laukus, ko vēlaties labot atlasītajām izdevumu rindām.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="8ec5a-141">Piemēram, varat piešķirt izdevumus citam vienumam **Projekts** vai labot vienumus **Izdevumu kategorija** , **Izdevumu datums** vai **Rezervējams resurss**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="8ec5a-142">Atlasiet **Priekšskatīt**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-142">Select **Preview**.</span></span> <span data-ttu-id="8ec5a-143">Dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="8ec5a-144">Pārbaudiet cilnē **Žurnāla rindas** veiktos labojumus. Varat skatīt sākotnējo faktisko ierakstu sarakstu, kas ir saistīti ar atlasītajiem izdevumu ierakstiem, kuri tika apvērsti, un labotajām atbilstošajām rindām, kas tika izveidotas.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="8ec5a-145">Ja labotās vērtības tiek parādītas, kā paredzēts, atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="8ec5a-146">Dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="8ec5a-147">Ja vērtības netiek rādītas, kā paredzēts, atlasiet **Atcelt** , lai atgrieztos sarakstā **Apstiprinātie izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="8ec5a-148">Atkārtojiet 2.–5. darbību.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="8ec5a-149">Koriģētajiem faktiskajiem ierakstiem ir tādas pašas vērtības, kādas atlasījāt sadaļā **Jaunas vērtības izdevumiem**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="8ec5a-150">Kad apstiprināsiet labojumu žurnālu, pārejiet atpakaļ uz atjaunināto projektu vai projektiem, lai skatītu veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="8ec5a-151">Cilnes **Faktiskās vērtības** projekta lapā pārskatiet skatu **Faktiskais saistītais skats**.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="8ec5a-152">Tiek parādīti sākotnējie ieraksti un labotie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="8ec5a-153">Tālāk redzamajā attēlā ir parādītas izdevumu ieraksta sākotnējās summas un atbilstošās koriģētās izmaksu ierakstu summas.</span><span class="sxs-lookup"><span data-stu-id="8ec5a-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


