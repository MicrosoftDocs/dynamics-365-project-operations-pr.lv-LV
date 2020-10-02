---
title: Izdevumu pārvaldības darbplūsmu iestatīšana
description: Varat iestatīt darbplūsmas procesu, kas tiek izmantots, lai pārskatītu komandējumu un izdevumu dokumentus.
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
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896560"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="280a9-103">Izdevumu pārvaldības darbplūsmu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="280a9-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="280a9-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="280a9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="280a9-105">Varat iestatīt darbplūsmas procesu, lai pārskatītu komandējumu un izdevumu dokumentus.</span><span class="sxs-lookup"><span data-stu-id="280a9-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="280a9-106">Varat definēt darbplūsmas izdevumu atskaitēm, komandējumu pieprasījumiem un avansa pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="280a9-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="280a9-107">Darbplūsma reprezentē biznesa procesu un nosaka, kā dokuments plūst pa sistēmu.</span><span class="sxs-lookup"><span data-stu-id="280a9-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="280a9-108">Darbplūsma arī norāda, kam ir jāizpilda uzdevums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="280a9-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="280a9-109">Darbplūsmas sistēmas lietošanai jūsu organizācijā ir vairākas priekšrocības:</span><span class="sxs-lookup"><span data-stu-id="280a9-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="280a9-110">**Konsekventi procesi**: Jūs varat definēt konkrētu dokumentu apstiprināšanas procesu, piemēram, iegādes pieprasījumus un izdevumu atskaites.</span><span class="sxs-lookup"><span data-stu-id="280a9-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="280a9-111">Darbplūsmas sistēmas lietošana palīdz nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti konsekventi un efektīvi.</span><span class="sxs-lookup"><span data-stu-id="280a9-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="280a9-112">**Procesa redzamība**: Varat izsekot konkrētās darbplūsmas instances statusam, vēsturei un veiktspējas metrikai.</span><span class="sxs-lookup"><span data-stu-id="280a9-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="280a9-113">Tādējādi varat noteikt, vai darbplūsmā vajadzētu veikt izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="280a9-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="280a9-114">**Centralizēts darba saraksts**: Lietotāji var skatīt centralizētu darba sarakstu, lai skatītu darbplūsmu uzdevumus un tiem piešķirtos apstiprinājumus.</span><span class="sxs-lookup"><span data-stu-id="280a9-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="280a9-115">Darbplūsmu veidi</span><span class="sxs-lookup"><span data-stu-id="280a9-115">Workflow types</span></span>

<span data-ttu-id="280a9-116">Šajā tabulā uzskaitīti darbplūsmu veidi, kuras varat izveidot **Izdevumu pārvaldībā**.</span><span class="sxs-lookup"><span data-stu-id="280a9-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="280a9-117"><strong>Tips</strong></span><span class="sxs-lookup"><span data-stu-id="280a9-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="280a9-118"><strong>Izmantojiet šo veidu, lai</strong></span><span class="sxs-lookup"><span data-stu-id="280a9-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="280a9-119"><strong>Izdevumu atskaišu automātiska apstiprināšana</strong></span><span class="sxs-lookup"><span data-stu-id="280a9-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="280a9-120">Izveidojiet izdevumu atskaišu apstiprināšanas darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="280a9-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="280a9-121"><strong>Izdevumu atskaišu automātiska publicēšana</strong></span><span class="sxs-lookup"><span data-stu-id="280a9-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="280a9-122">Izveidojiet automātiskas publicēšanas darbplūsmas izdevumu atskaitēm.</span><span class="sxs-lookup"><span data-stu-id="280a9-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="280a9-123"><strong>Izdevumu rindas elements</strong></span><span class="sxs-lookup"><span data-stu-id="280a9-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="280a9-124">Izveidojiet apstiprināšanas darbplūsmas rindas elementiem izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="280a9-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="280a9-125"><strong>Izdevumu rindas elementa automātiska publicēšana</strong></span><span class="sxs-lookup"><span data-stu-id="280a9-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="280a9-126">Izveidojiet automātiskas publicēšanas darbplūsmas rindas elementiem izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="280a9-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="280a9-127"><strong>Ceļojuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="280a9-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="280a9-128">Izveidojiet apstiprināšanas darbplūsmas komandējumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="280a9-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="280a9-129"><strong>Avansa maksājuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="280a9-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="280a9-130">Izveidojiet apstiprināšanas darbplūsmas avansa maksājumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="280a9-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="280a9-131"><strong>PVN atmaksa</strong></span><span class="sxs-lookup"><span data-stu-id="280a9-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="280a9-132">Izveidojiet apstiprināšanas darbplūsmas pievienotās vērtības nodokļa (PVN) atmaksai.</span><span class="sxs-lookup"><span data-stu-id="280a9-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
