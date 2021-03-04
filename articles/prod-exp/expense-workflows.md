---
title: Izdevumu pārvaldības darbplūsmu iestatīšana
description: Varat iestatīt darbplūsmas procesu, lai pārskatītu komandējumu un izdevumu dokumentus.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3235d12499c68a52f9d1c7e118e7bc91dc3a0a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960526"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="23e0c-103">Izdevumu pārvaldības darbplūsmu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="23e0c-103">Set up Expense management workflows</span></span>

<span data-ttu-id="23e0c-104">Varat iestatīt darbplūsmas procesu, kas tiek izmantots, lai pārskatītu komandējumu un izdevumu dokumentus.</span><span class="sxs-lookup"><span data-stu-id="23e0c-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="23e0c-105">Dokumenti, kuriem var definēt darbplūsmas, ietver izdevumu atskaites, komandējumu pieprasījumus un avansa pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="23e0c-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="23e0c-106">Darbplūsma atspoguļo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="23e0c-106">A workflow represents a business process.</span></span> <span data-ttu-id="23e0c-107">Tas definē, kā dokuments pārvietojas sistēmā, un norāda, kam ir jāizpilda uzdevums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="23e0c-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="23e0c-108">Darbplūsmas sistēmas lietošanai jūsu organizācijā ir vairākas priekšrocības:</span><span class="sxs-lookup"><span data-stu-id="23e0c-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="23e0c-109">**Konsekventi procesi** — jūs varat definēt konkrētu dokumentu apstiprināšanas procesu, piemēram, iegādes pieprasījumus un izdevumu atskaites.</span><span class="sxs-lookup"><span data-stu-id="23e0c-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="23e0c-110">Darbplūsmas sistēmas lietošana palīdz nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti konsekventi un efektīvi.</span><span class="sxs-lookup"><span data-stu-id="23e0c-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="23e0c-111">Procesa redzamība — varat izsekot konkrētās darbplūsmas instances statusam, vēsturei un veiktspējas metrikai.</span><span class="sxs-lookup"><span data-stu-id="23e0c-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="23e0c-112">Tādējādi varat noteikt, vai darbplūsmā vajadzētu veikt izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="23e0c-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="23e0c-113">Centralizēts darba saraksts — lietotāji var skatīt centralizētu darba sarakstu, lai skatītu darbplūsmu uzdevumus un tiem piešķirtos apstiprinājumus.</span><span class="sxs-lookup"><span data-stu-id="23e0c-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="23e0c-114">**Darbplūsmu veidi, ko var izveidot**</span><span class="sxs-lookup"><span data-stu-id="23e0c-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="23e0c-115">Šajā tabulā uzskaitīti darbplūsmu veidi, kurus varat izveidot sadaļā **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="23e0c-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="23e0c-116"><strong>Tips</strong></span><span class="sxs-lookup"><span data-stu-id="23e0c-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="23e0c-117"><strong>Izmantojiet šo veidu, lai</strong></span><span class="sxs-lookup"><span data-stu-id="23e0c-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="23e0c-118"><strong>Izdevumu atskaite</strong></span><span class="sxs-lookup"><span data-stu-id="23e0c-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="23e0c-119">Izveidojiet izdevumu atskaišu apstiprināšanas darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="23e0c-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="23e0c-120"><strong>Izdevumu atskaišu automātiska publicēšana</strong></span><span class="sxs-lookup"><span data-stu-id="23e0c-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="23e0c-121">Izveidojiet automātiskas publicēšanas darbplūsmas izdevumu atskaitēm.</span><span class="sxs-lookup"><span data-stu-id="23e0c-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="23e0c-122"><strong>Izdevumu rindas elements</strong></span><span class="sxs-lookup"><span data-stu-id="23e0c-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="23e0c-123">Izveidojiet apstiprināšanas darbplūsmas rindas elementiem izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="23e0c-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="23e0c-124"><strong>Izdevumu rindas elementa automātiska publicēšana</strong></span><span class="sxs-lookup"><span data-stu-id="23e0c-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="23e0c-125">Izveidojiet automātiskas publicēšanas darbplūsmas rindas elementiem izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="23e0c-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="23e0c-126"><strong>Ceļojuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="23e0c-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="23e0c-127">Izveidojiet apstiprināšanas darbplūsmas komandējumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="23e0c-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="23e0c-128"><strong>Avansa maksājuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="23e0c-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="23e0c-129">Izveidojiet apstiprināšanas darbplūsmas avansa maksājumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="23e0c-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="23e0c-130"><strong>PVN atmaksa</strong></span><span class="sxs-lookup"><span data-stu-id="23e0c-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="23e0c-131">Izveidojiet apstiprināšanas darbplūsmas pievienotās vērtības nodokļa (PVN) atmaksai.</span><span class="sxs-lookup"><span data-stu-id="23e0c-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

