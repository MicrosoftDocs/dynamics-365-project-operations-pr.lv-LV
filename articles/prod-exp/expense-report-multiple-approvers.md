---
title: Vairāki apstiprinātāji izdevumu atskaitē
description: Šajā tēmā sniegta informācija par izdevumu atskaitēm, kurām ir nepieciešams vairāku personu apstiprinājums.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960616"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="7ae24-103">Vairāki apstiprinātāji izdevumu atskaitē</span><span class="sxs-lookup"><span data-stu-id="7ae24-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="7ae24-104">Atkarībā no jūsu organizācijas izdevumu apstiprināšanas politikas, iespējams, izdevumu atskaiti, ko iesniedz darbinieks, vajadzēs apstiprināt vairāk nekā vienai personai.</span><span class="sxs-lookup"><span data-stu-id="7ae24-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="7ae24-105">Iestatot darbplūsmas procesu izdevumu atskaites apstiprināšanai, varat pievienot darbplūsmas elementus, kas ietver uzdevumus vai darbības vienam vai vairākiem izdevumu atskaišu apstiprinātājiem.</span><span class="sxs-lookup"><span data-stu-id="7ae24-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="7ae24-106">Piemēram, iespējams, būs nepieciešams, ka visas izdevumu atskaites vispirms apstiprina darbinieka, kurš iesniedza atskaiti, vadītājs un pēc tam to apstiprina kreditoru koordinators.</span><span class="sxs-lookup"><span data-stu-id="7ae24-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="7ae24-107">Ja nolemjat, ka ir nepieciešami vairāki izdevumu atskaišu apstiprinātaji, jebkurā no šiem veidiem varat pievienot darbplūsmu elementus:</span><span class="sxs-lookup"><span data-stu-id="7ae24-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="7ae24-108">Pievienojiet vienu apstiprināšanas elementu, kam ir viena darbība.</span><span class="sxs-lookup"><span data-stu-id="7ae24-108">Add one approval element that has one step.</span></span> <span data-ttu-id="7ae24-109">Piemēram, šai darbībai var būt nepieciešams, ka izdevumu atskaiti piešķir lietotāju grupai un ka to apstiprina 50 procenti lietotāja grupas dalībnieku.</span><span class="sxs-lookup"><span data-stu-id="7ae24-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="7ae24-110">Pievienojiet vienu apstiprināšanas elementu, kam ir vairākas darbības.</span><span class="sxs-lookup"><span data-stu-id="7ae24-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="7ae24-111">Piemēram, apstiprināšanas elementam var būt vairākas darbības:</span><span class="sxs-lookup"><span data-stu-id="7ae24-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="7ae24-112">Izdevumu atskaites iesniedzēja pārvaldnieks to apstiprina.</span><span class="sxs-lookup"><span data-stu-id="7ae24-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="7ae24-113">Kreditoru darbinieks pārbauda kvītis un izdevumu atskaišu elementus.</span><span class="sxs-lookup"><span data-stu-id="7ae24-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="7ae24-114">Budžeta īpašnieks apstiprina izdevumu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="7ae24-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="7ae24-115">Pievienojiet vairākus apstiprināšanas elementus, no kuriem katram ir viena darbība.</span><span class="sxs-lookup"><span data-stu-id="7ae24-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="7ae24-116">Piemēram, katrai no šīm darbībām varat pievienot atsevišķu apstiprināšanas elementu:</span><span class="sxs-lookup"><span data-stu-id="7ae24-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="7ae24-117">Darbinieka vadītajs apstiprina izdevumu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="7ae24-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="7ae24-118">Budžeta īpašnieks apstiprina izdevumu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="7ae24-118">The budget owner approves the expense report.</span></span>
