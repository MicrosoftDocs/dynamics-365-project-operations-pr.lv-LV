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
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080598"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="d7aa2-103">Izdevumu pārvaldības darbplūsmu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d7aa2-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7aa2-104">Varat iestatīt darbplūsmas procesu, kas tiek izmantots, lai pārskatītu komandējumu un izdevumu dokumentus.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="d7aa2-105">Dokumenti, kuriem var definēt darbplūsmas, ietver izdevumu atskaites, komandējumu pieprasījumus un avansa pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="d7aa2-106">Darbplūsma atspoguļo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-106">A workflow represents a business process.</span></span> <span data-ttu-id="d7aa2-107">Tas definē, kā dokuments pārvietojas sistēmā, un norāda, kam ir jāizpilda uzdevums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="d7aa2-108">Darbplūsmas sistēmas lietošanai jūsu organizācijā ir vairākas priekšrocības:</span><span class="sxs-lookup"><span data-stu-id="d7aa2-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="d7aa2-109">**Konsekventi procesi**  — jūs varat definēt konkrētu dokumentu apstiprināšanas procesu, piemēram, iegādes pieprasījumus un izdevumu atskaites.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="d7aa2-110">Darbplūsmas sistēmas lietošana palīdz nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti konsekventi un efektīvi.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="d7aa2-111">Procesa redzamība — varat izsekot konkrētās darbplūsmas instances statusam, vēsturei un veiktspējas metrikai.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="d7aa2-112">Tādējādi varat noteikt, vai darbplūsmā vajadzētu veikt izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="d7aa2-113">Centralizēts darba saraksts — lietotāji var skatīt centralizētu darba sarakstu, lai skatītu darbplūsmu uzdevumus un tiem piešķirtos apstiprinājumus.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="d7aa2-114">**Darbplūsmu veidi, ko var izveidot**</span><span class="sxs-lookup"><span data-stu-id="d7aa2-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="d7aa2-115">Šajā tabulā uzskaitīti darbplūsmu veidi, kurus varat izveidot sadaļā **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="d7aa2-116"><strong>Tips</strong></span><span class="sxs-lookup"><span data-stu-id="d7aa2-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="d7aa2-117"><strong>Izmantojiet šo veidu, lai</strong></span><span class="sxs-lookup"><span data-stu-id="d7aa2-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="d7aa2-118"><strong>Izdevumu atskaite</strong></span><span class="sxs-lookup"><span data-stu-id="d7aa2-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="d7aa2-119">Izveidojiet izdevumu atskaišu apstiprināšanas darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="d7aa2-120"><strong>Izdevumu atskaišu automātiska publicēšana</strong></span><span class="sxs-lookup"><span data-stu-id="d7aa2-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="d7aa2-121">Izveidojiet automātiskas publicēšanas darbplūsmas izdevumu atskaitēm.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="d7aa2-122"><strong>Izdevumu rindas elements</strong></span><span class="sxs-lookup"><span data-stu-id="d7aa2-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="d7aa2-123">Izveidojiet apstiprināšanas darbplūsmas rindas elementiem izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="d7aa2-124"><strong>Izdevumu rindas elementa automātiska publicēšana</strong></span><span class="sxs-lookup"><span data-stu-id="d7aa2-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="d7aa2-125">Izveidojiet automātiskas publicēšanas darbplūsmas rindas elementiem izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="d7aa2-126"><strong>Ceļojuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="d7aa2-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="d7aa2-127">Izveidojiet apstiprināšanas darbplūsmas komandējumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="d7aa2-128"><strong>Avansa maksājuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="d7aa2-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="d7aa2-129">Izveidojiet apstiprināšanas darbplūsmas avansa maksājumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="d7aa2-130"><strong>PVN atmaksa</strong></span><span class="sxs-lookup"><span data-stu-id="d7aa2-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="d7aa2-131">Izveidojiet apstiprināšanas darbplūsmas pievienotās vērtības nodokļa (PVN) atmaksai.</span><span class="sxs-lookup"><span data-stu-id="d7aa2-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

