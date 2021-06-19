---
title: Izdevumu pārvaldības darbplūsmu iestatīšana
description: Varat iestatīt darbplūsmas procesu, lai pārskatītu komandējumu un izdevumu dokumentus.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005125"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="ff0be-103">Izdevumu pārvaldības darbplūsmu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ff0be-103">Set up Expense management workflows</span></span>

<span data-ttu-id="ff0be-104">Varat iestatīt darbplūsmas procesu, kas tiek izmantots, lai pārskatītu komandējumu un izdevumu dokumentus.</span><span class="sxs-lookup"><span data-stu-id="ff0be-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="ff0be-105">Dokumenti, kuriem var definēt darbplūsmas, ietver izdevumu atskaites, komandējumu pieprasījumus un avansa pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="ff0be-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="ff0be-106">Darbplūsma atspoguļo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="ff0be-106">A workflow represents a business process.</span></span> <span data-ttu-id="ff0be-107">Tas definē, kā dokuments pārvietojas sistēmā, un norāda, kam ir jāizpilda uzdevums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="ff0be-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ff0be-108">Darbplūsmas sistēmas lietošanai jūsu organizācijā ir vairākas priekšrocības:</span><span class="sxs-lookup"><span data-stu-id="ff0be-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="ff0be-109">**Konsekventi procesi** — jūs varat definēt konkrētu dokumentu apstiprināšanas procesu, piemēram, iegādes pieprasījumus un izdevumu atskaites.</span><span class="sxs-lookup"><span data-stu-id="ff0be-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ff0be-110">Darbplūsmas sistēmas lietošana palīdz nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti konsekventi un efektīvi.</span><span class="sxs-lookup"><span data-stu-id="ff0be-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="ff0be-111">Procesa redzamība — varat izsekot konkrētās darbplūsmas instances statusam, vēsturei un veiktspējas metrikai.</span><span class="sxs-lookup"><span data-stu-id="ff0be-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ff0be-112">Tādējādi varat noteikt, vai darbplūsmā vajadzētu veikt izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="ff0be-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="ff0be-113">Centralizēts darba saraksts — lietotāji var skatīt centralizētu darba sarakstu, lai skatītu darbplūsmu uzdevumus un tiem piešķirtos apstiprinājumus.</span><span class="sxs-lookup"><span data-stu-id="ff0be-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="ff0be-114">**Darbplūsmu veidi, ko var izveidot**</span><span class="sxs-lookup"><span data-stu-id="ff0be-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="ff0be-115">Šajā tabulā uzskaitīti darbplūsmu veidi, kurus varat izveidot sadaļā **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="ff0be-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="ff0be-116"><strong>Tips</strong></span><span class="sxs-lookup"><span data-stu-id="ff0be-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="ff0be-117"><strong>Izmantojiet šo veidu, lai</strong></span><span class="sxs-lookup"><span data-stu-id="ff0be-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="ff0be-118"><strong>Izdevumu atskaite</strong></span><span class="sxs-lookup"><span data-stu-id="ff0be-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="ff0be-119">Izveidojiet izdevumu atskaišu apstiprināšanas darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="ff0be-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="ff0be-120"><strong>Izdevumu atskaišu automātiska publicēšana</strong></span><span class="sxs-lookup"><span data-stu-id="ff0be-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="ff0be-121">Izveidojiet automātiskas publicēšanas darbplūsmas izdevumu atskaitēm.</span><span class="sxs-lookup"><span data-stu-id="ff0be-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="ff0be-122"><strong>Izdevumu rindas elements</strong></span><span class="sxs-lookup"><span data-stu-id="ff0be-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="ff0be-123">Izveidojiet apstiprināšanas darbplūsmas rindas elementiem izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="ff0be-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="ff0be-124"><strong>Izdevumu rindas elementa automātiska publicēšana</strong></span><span class="sxs-lookup"><span data-stu-id="ff0be-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="ff0be-125">Izveidojiet automātiskas publicēšanas darbplūsmas rindas elementiem izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="ff0be-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="ff0be-126"><strong>Ceļojuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="ff0be-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="ff0be-127">Izveidojiet apstiprināšanas darbplūsmas komandējumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="ff0be-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="ff0be-128"><strong>Avansa maksājuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="ff0be-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="ff0be-129">Izveidojiet apstiprināšanas darbplūsmas avansa maksājumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="ff0be-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="ff0be-130"><strong>PVN atmaksa</strong></span><span class="sxs-lookup"><span data-stu-id="ff0be-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="ff0be-131">Izveidojiet apstiprināšanas darbplūsmas pievienotās vērtības nodokļa (PVN) atmaksai.</span><span class="sxs-lookup"><span data-stu-id="ff0be-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]