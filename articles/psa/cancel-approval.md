---
title: Iepriekš apstiprināto laika un izdevumu ierakstu atcelšana
description: Šajā tēmā ir sniegta informācija par to, kā atcelt apstiprinātu projekta laiku un izmaksu darbību.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0ea816040570cc8f6ddf3c5ec8a74ac092fc68b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080619"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="90cc1-103">Iepriekš apstiprināto laika vai izdevumu ierakstu atcelšana</span><span class="sxs-lookup"><span data-stu-id="90cc1-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="90cc1-104">Jaunākajā Dynamics 365 Project Service Automation versijā apstiprinātāji var atcelt iepriekš apstiprinātos laika vai izdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="90cc1-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="90cc1-105">Iepriekš apstiprinātā laika vai izdevuma ieraksta atcelšana</span><span class="sxs-lookup"><span data-stu-id="90cc1-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="90cc1-106">Lai atceltu iepriekš apstiprināto laika vai izdevumu ievadi, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="90cc1-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="90cc1-107">Atveriet sadaļu **Projekti** \> **Mani darbi** \> **Apstiprinājumi**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="90cc1-108">Lapas **Apstiprinājumi** sarakstā mainiet skatu uz **Mani jaunākie apstiprinājumi.**</span><span class="sxs-lookup"><span data-stu-id="90cc1-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="90cc1-109">Tiek parādīts iepriekš apstiprināto laika un izdevumu ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="90cc1-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="90cc1-110">Atlasiet vienu vai vairākus ierakstus un pēc tam atlasiet **Atcelt apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="90cc1-111">Tiek parādīts brīdinājuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="90cc1-111">You receive a warning message.</span></span>
4. <span data-ttu-id="90cc1-112">Lai atceltu lejupielādi, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="90cc1-113">Laika atcelšanas un izdevumu ieraksta apstiprinājuma ietekme</span><span class="sxs-lookup"><span data-stu-id="90cc1-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="90cc1-114">Kad apstiprinājums tiek atcelts, tam ir gan operacionāla, gan finansiālā ietekme.</span><span class="sxs-lookup"><span data-stu-id="90cc1-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="90cc1-115">Operacionāla ietekme</span><span class="sxs-lookup"><span data-stu-id="90cc1-115">Operational impact</span></span>

<span data-ttu-id="90cc1-116">Kad apstiprinājums ir atcelts, operacionālajā pusē ieraksta statuss tiek atiestatīts uz **Melnraksts** un apstiprinājums vairs netiek rādīts skatā **Mani jaunākie apstiprinājumi**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft** , and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="90cc1-117">Tā vietā atceltā apstiprināšana tiek parādīta vai nu skata **Apstiprinājuma laika ieraksti** , vai skata **Apstiprinājuma izdevumu ieraksti** atkarībā no tā, vai tas ir laika ieraksts vai izdevumu ieraksts.</span><span class="sxs-lookup"><span data-stu-id="90cc1-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="90cc1-118">Turklāt saistītā laika vai izdevumu ieraksta statuss tiek mainīts uz **Iesniegts** , lai saistītais ieraksts atbilstu apstiprinājumam, kura statuss ir **Melnraksts.**</span><span class="sxs-lookup"><span data-stu-id="90cc1-118">Additionally, the status of the related time or expense entry is changed to **Submitted** , so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="90cc1-119">Kā apstiprinātājs var rediģēt dažus apstiprinājuma laukus, kam statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="90cc1-120">Šajos laukos ir iekļauti skati **Norēķinu veids** un **Apmaksas stundas laika ierakstiem**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="90cc1-121">Pēc izmaiņu veikšanas varat vēlreiz apstiprināt ieraksta apstiprināšanu.</span><span class="sxs-lookup"><span data-stu-id="90cc1-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="90cc1-122">Varat arī noraidīt ierakstu.</span><span class="sxs-lookup"><span data-stu-id="90cc1-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="90cc1-123">Ja noraidāt laika ieraksta apstiprinājumu, ieraksta statuss tiek mainīts uz **Atgriezts.**</span><span class="sxs-lookup"><span data-stu-id="90cc1-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="90cc1-124">Ja noraidāt izdevumu ievadi, ieraksta statuss tiek mainīts uz **Atgriezts**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="90cc1-125">Funkcionāli gan atgrieztie, gan noraidītie ieraksti izturēsies vienādi ar ierakstu, kura statuss ir **Melnraksts**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="90cc1-126">Projekta darba grupas dalībnieks var veikt jebkādas nepieciešamās izmaiņas ierakstā un pēc tam to atkārtoti iesniegt apstiprināšanai vai dzēst pavisam.</span><span class="sxs-lookup"><span data-stu-id="90cc1-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="90cc1-127">Finansiālā ietekme</span><span class="sxs-lookup"><span data-stu-id="90cc1-127">Financial impact</span></span>

<span data-ttu-id="90cc1-128">Projekts tiek ietekmēts arī finansiāli, kad apstiprinājums ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="90cc1-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="90cc1-129">Pirmkārt, atbilstošās izmaksu un pārdošanas faktiskās vērtības tiek atjauninātas šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="90cc1-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="90cc1-130">Pielāgošanas statuss ir iestatīts uz **Pielāgots**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="90cc1-131">Pielāgošanas statuss ir iestatīts uz **Atcelts**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="90cc1-132">Tālāk tiek izveidotas anulēšanas ievadnes tabulā Esošie.</span><span class="sxs-lookup"><span data-stu-id="90cc1-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="90cc1-133">Lai izveidotu atgrieztos ierakstus, sistēma pārkopē lauka vērtības no sākotnējiem esošajiem.</span><span class="sxs-lookup"><span data-stu-id="90cc1-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="90cc1-134">Vienīgās vērtības, kas nav pārkopētas, ir daudzuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="90cc1-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="90cc1-135">Šīs vērtības tiek atgrieztas.</span><span class="sxs-lookup"><span data-stu-id="90cc1-135">These values are reversed instead.</span></span> <span data-ttu-id="90cc1-136">Atgrieztie esošie tiek izveidoti gan sadaļā **Izmaksas** , **gan Nerēķina pārdošana** esošajos izdevumos.</span><span class="sxs-lookup"><span data-stu-id="90cc1-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="90cc1-137">Atgriezto esošo lauks **Pielāgojuma statuss** ir iestatīts uz **Nav pielāgojams** un norēķinu statuss ir iestatīts uz **Atcelts**.</span><span class="sxs-lookup"><span data-stu-id="90cc1-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable** , and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="90cc1-138">Pēc šo izmaiņu veikšanas summa, kas tiek ierakstīta kā projektā patērētā summa un projektā gūtie ieņēmumi, kļūs lielāka par to summu, ko veido šie faktiskie.</span><span class="sxs-lookup"><span data-stu-id="90cc1-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
