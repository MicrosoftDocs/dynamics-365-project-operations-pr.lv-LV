---
title: Izdevumu ievade (Lite)
description: Šajā tēmā sniegta informācija par to, kā strādāt ar izdevumu ierakstu Lite izvietošanā.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965838"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="7d0bd-103">Izdevumu ievade (Lite)</span><span class="sxs-lookup"><span data-stu-id="7d0bd-103">Expense entry (lite)</span></span>

<span data-ttu-id="7d0bd-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="7d0bd-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7d0bd-105">Basic vai Lite izmaksu pārvaldība ir iespēja ierakstīt vienkāršus izdevumus.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="7d0bd-106">Varat ierakstīt izmaksas projektam, un pēc tam projekta apstiprinātājs tos pārskatīs un apstiprinās.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="7d0bd-107">Papildinformāciju par izdevumu iespējām risinājumā Dynamics 365 Project Operations, skatiet šeit: [Izdevumu pārskats](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7d0bd-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="7d0bd-108">Pamata izdevuma fiksēšana</span><span class="sxs-lookup"><span data-stu-id="7d0bd-108">Capture a basic expense</span></span>

<span data-ttu-id="7d0bd-109">Varat fiksēt savus izdevumus, lai tos varētu iesniegt apstiprinātājam.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="7d0bd-110">Atveriet sadaļu **Izdevumi** un atlasiet vienumu **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="7d0bd-111">Lapā **Jauns izdevums** ievadiet nepieciešamo informāciju par izdevumu un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="7d0bd-112">Pamata izdevuma iesniegšana</span><span class="sxs-lookup"><span data-stu-id="7d0bd-112">Submit a basic expense</span></span>

<span data-ttu-id="7d0bd-113">Kad esat pabeidzis visu savu izdevumu fiksēšanu un esat gatavs tos virzīt apstiprināšanai, tie ir jāiesniedz.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="7d0bd-114">Atveriet sadaļu **Izdevumi** un atlasiet kādu izdevumu.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="7d0bd-115">Vai arī atlasiet visus izdevumus, izmantojot izvēles rūtiņu galvenē.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="7d0bd-116">Atlasiet **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-116">Select **Submit**.</span></span> <span data-ttu-id="7d0bd-117">Sistēma apstrādā atlasītos ierakstus un pēc tam izveido izmaksu apstiprināšanas pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="7d0bd-118">Pamata izdevuma atsaukšana</span><span class="sxs-lookup"><span data-stu-id="7d0bd-118">Recall a basic expense</span></span>

<span data-ttu-id="7d0bd-119">Ja esat kļūdaini iesniedzis izdevumu, varat to atsaukt.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="7d0bd-120">Laiks, kas nepieciešams izdevuma ieraksta atsaukšanai, atkarīgs no tā apstiprinājuma posma.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="7d0bd-121">Ja apstiprinātājs vēl nav apstiprinājis ierakstu, atsaukšana var notikt nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="7d0bd-122">Tomēr, ja ieraksts jau ir apstiprināts, apstiprinātājam tiek lūgts apstiprināt atsaukumu un mainīt darījumus.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="7d0bd-123">Atveriet sadaļu **Izdevumi** un pēc tam izmaksu sarakstā atlasiet atsaucamo izdevumu.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="7d0bd-124">Atlasiet **Atsaukt**.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-124">Select **Recall**.</span></span> <span data-ttu-id="7d0bd-125">Ja izdevuma ieraksts vēl nav apstiprināts, sistēma to atsauc nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="7d0bd-126">Ja izdevuma ieraksts jau ir apstiprināts, tiek izveidots atsaukšanas pieprasījums, lai paziņotu apstiprinātājam par to, ka jūs vēlaties mainīt izdevumus.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="7d0bd-127">Pēc tam apstiprinātājs apstiprinās, ka var veikt atsaukšanu, un ieraksts tiks atgriezts.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="7d0bd-128">Pamata izdevuma dzēšana</span><span class="sxs-lookup"><span data-stu-id="7d0bd-128">Delete a basic expense</span></span>

<span data-ttu-id="7d0bd-129">Izdevumus, kas vēl nav iesniegti, var dzēst.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="7d0bd-130">Lai dzēstu izdevumu, kas jau ir iesniegts, tas vispirms ir jāatsauc.</span><span class="sxs-lookup"><span data-stu-id="7d0bd-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d0bd-131">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="7d0bd-131">See also</span></span>

- [<span data-ttu-id="7d0bd-132">Apstiprinājumu pārskats</span><span class="sxs-lookup"><span data-stu-id="7d0bd-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
