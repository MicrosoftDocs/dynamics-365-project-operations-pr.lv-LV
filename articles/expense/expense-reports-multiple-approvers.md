---
title: Izdevumu atskaites un vairāki apstiprinātāji
description: Šajā tēmā sniegta informācija par izdevumu atskaitēm, kurām ir nepieciešams vairāk nekā vienas personas apstiprinājums.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897100"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="494d3-103">Izdevumu atskaites un vairāki apstiprinātāji</span><span class="sxs-lookup"><span data-stu-id="494d3-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="494d3-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="494d3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="494d3-105">Atkarībā no jūsu organizācijas izdevumu apstiprināšanas politikas, iespējams, izdevumu atskaiti vajadzēs apstiprināt vairāk nekā vienai personai.</span><span class="sxs-lookup"><span data-stu-id="494d3-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="494d3-106">Iestatot darbplūsmas procesu izdevumu atskaites apstiprināšanai, varat pievienot darbplūsmas elementus, kas ietver uzdevumus vai darbības vienam vai vairākiem izdevumu atskaišu apstiprinātājiem.</span><span class="sxs-lookup"><span data-stu-id="494d3-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="494d3-107">Piemēram, iespējams, būs nepieciešams, ka visas izdevumu atskaites apstiprina divas atsevišķas personas — atskaites iesniedzēja vadītājs un kreditoru koordinators.</span><span class="sxs-lookup"><span data-stu-id="494d3-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="494d3-108">Ja nolemjat, ka ir nepieciešami vairāki izdevumu atskaišu apstiprinātaji, jebkurā no šiem veidiem varat pievienot darbplūsmu elementus:</span><span class="sxs-lookup"><span data-stu-id="494d3-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="494d3-109">Pievienojiet vienu apstiprināšanas elementu, kam ir viena darbība.</span><span class="sxs-lookup"><span data-stu-id="494d3-109">Add one approval element that has one step.</span></span> <span data-ttu-id="494d3-110">Piemēram, šai darbībai var būt nepieciešams, ka izdevumu atskaiti piešķir lietotāju grupai un ka to apstiprina 50 procenti lietotāja grupas dalībnieku.</span><span class="sxs-lookup"><span data-stu-id="494d3-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="494d3-111">Pievienojiet vienu apstiprināšanas elementu, kam ir vairākas darbības.</span><span class="sxs-lookup"><span data-stu-id="494d3-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="494d3-112">Piemēram, apstiprināšanas elementam var būt vairākas darbības:</span><span class="sxs-lookup"><span data-stu-id="494d3-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="494d3-113">Izdevumu atskaites iesniedzēja pārvaldnieks to apstiprina.</span><span class="sxs-lookup"><span data-stu-id="494d3-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="494d3-114">Kreditoru darbinieks pārbauda kvītis un izdevumu atskaišu elementus.</span><span class="sxs-lookup"><span data-stu-id="494d3-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="494d3-115">Budžeta īpašnieks apstiprina izdevumu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="494d3-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="494d3-116">Pievienojiet vairākus apstiprināšanas elementus, no kuriem katram ir viena darbība.</span><span class="sxs-lookup"><span data-stu-id="494d3-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="494d3-117">Piemēram, katrai no šīm darbībām varat pievienot atsevišķu apstiprināšanas elementu:</span><span class="sxs-lookup"><span data-stu-id="494d3-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="494d3-118">Darbinieka vadītajs apstiprina izdevumu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="494d3-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="494d3-119">Budžeta īpašnieks apstiprina izdevumu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="494d3-119">The budget owner approves the expense report.</span></span>
