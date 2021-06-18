---
title: Izdevumu pārvaldības darbplūsmu iestatīšana
description: Varat iestatīt darbplūsmas procesu, kas tiek izmantots, lai pārskatītu komandējumu un izdevumu dokumentus.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab6e18d1ddcffa57cf7cd4cb09eec5a4b89c0fd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001030"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="d6bfc-103">Izdevumu pārvaldības darbplūsmu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d6bfc-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="d6bfc-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="d6bfc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d6bfc-105">Varat iestatīt darbplūsmas procesu, lai pārskatītu komandējumu un izdevumu dokumentus.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="d6bfc-106">Varat definēt darbplūsmas izdevumu atskaitēm, komandējumu pieprasījumiem un avansa pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="d6bfc-107">Darbplūsma reprezentē biznesa procesu un nosaka, kā dokuments plūst pa sistēmu.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="d6bfc-108">Darbplūsma arī norāda, kam ir jāizpilda uzdevums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="d6bfc-109">Darbplūsmas sistēmas lietošanai jūsu organizācijā ir vairākas priekšrocības:</span><span class="sxs-lookup"><span data-stu-id="d6bfc-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="d6bfc-110">**Konsekventi procesi**: Jūs varat definēt konkrētu dokumentu apstiprināšanas procesu, piemēram, iegādes pieprasījumus un izdevumu atskaites.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="d6bfc-111">Darbplūsmas sistēmas lietošana palīdz nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti konsekventi un efektīvi.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="d6bfc-112">**Procesa redzamība**: Varat izsekot konkrētās darbplūsmas instances statusam, vēsturei un veiktspējas metrikai.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="d6bfc-113">Tādējādi varat noteikt, vai darbplūsmā vajadzētu veikt izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="d6bfc-114">**Centralizēts darba saraksts**: Lietotāji var skatīt centralizētu darba sarakstu, lai skatītu darbplūsmu uzdevumus un tiem piešķirtos apstiprinājumus.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="d6bfc-115">Darbplūsmu veidi</span><span class="sxs-lookup"><span data-stu-id="d6bfc-115">Workflow types</span></span>

<span data-ttu-id="d6bfc-116">Šajā tabulā uzskaitīti darbplūsmu veidi, kuras varat izveidot **Izdevumu pārvaldībā**.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="d6bfc-117"><strong>Tips</strong></span><span class="sxs-lookup"><span data-stu-id="d6bfc-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="d6bfc-118"><strong>Izmantojiet šo veidu, lai</strong></span><span class="sxs-lookup"><span data-stu-id="d6bfc-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="d6bfc-119"><strong>Izdevumu atskaišu automātiska apstiprināšana</strong></span><span class="sxs-lookup"><span data-stu-id="d6bfc-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="d6bfc-120">Izveidojiet izdevumu atskaišu apstiprināšanas darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="d6bfc-121"><strong>Izdevumu atskaišu automātiska publicēšana</strong></span><span class="sxs-lookup"><span data-stu-id="d6bfc-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="d6bfc-122">Izveidojiet automātiskas publicēšanas darbplūsmas izdevumu atskaitēm.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="d6bfc-123"><strong>Izdevumu rindas elements</strong></span><span class="sxs-lookup"><span data-stu-id="d6bfc-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="d6bfc-124">Izveidojiet apstiprināšanas darbplūsmas rindas elementiem izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="d6bfc-125"><strong>Izdevumu rindas elementa automātiska publicēšana</strong></span><span class="sxs-lookup"><span data-stu-id="d6bfc-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="d6bfc-126">Izveidojiet automātiskas publicēšanas darbplūsmas rindas elementiem izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="d6bfc-127"><strong>Ceļojuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="d6bfc-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="d6bfc-128">Izveidojiet apstiprināšanas darbplūsmas komandējumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="d6bfc-129"><strong>Avansa maksājuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="d6bfc-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="d6bfc-130">Izveidojiet apstiprināšanas darbplūsmas avansa maksājumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="d6bfc-131"><strong>PVN atmaksa</strong></span><span class="sxs-lookup"><span data-stu-id="d6bfc-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="d6bfc-132">Izveidojiet apstiprināšanas darbplūsmas pievienotās vērtības nodokļa (PVN) atmaksai.</span><span class="sxs-lookup"><span data-stu-id="d6bfc-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]