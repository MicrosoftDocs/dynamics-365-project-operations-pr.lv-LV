---
title: Izdevumu pārvaldības darbplūsma
description: Šajā tēmā ir paskaidrots, kā sistēmā Microsoft Dynamics 365 Finance izmantot darbplūsmas sistēmu, lai izmaksu pārvaldībā iestatītu atsauksmju sniegšanas procesu par izmaksu atskaitēm.
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
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080599"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="e16fa-103">Izdevumu pārvaldības darbplūsma</span><span class="sxs-lookup"><span data-stu-id="e16fa-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e16fa-104">Varat izmantot darbplūsmas sistēmu, lai izmaksu pārvaldībā iestatītu atsauksmju sniegšanas procesu par izmaksu atskaitēm.</span><span class="sxs-lookup"><span data-stu-id="e16fa-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="e16fa-105">Varat iestatīt darbplūsmu, kas izmanto tālāk norādītos kritērijus, lai noteiktu, kurš apstiprina izmaksu atskaites.</span><span class="sxs-lookup"><span data-stu-id="e16fa-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="e16fa-106">Darbinieku atskaišu izveides hierarhija un iepriekš noteikti apstiprināšanas ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="e16fa-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="e16fa-107">Vairāku līmeņu apstiprināšana, kas atbalsta pagaidu apstiprinātājus un galīgo apstiprinātāju</span><span class="sxs-lookup"><span data-stu-id="e16fa-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="e16fa-108">Finanšu rādītāji un projekta atbildība</span><span class="sxs-lookup"><span data-stu-id="e16fa-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="e16fa-109">Piešķiršana noteiktiem lietotājiem vai lietotāju grupām</span><span class="sxs-lookup"><span data-stu-id="e16fa-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="e16fa-110">Darbplūsmas apstiprinājumus var izveidot izdevumu atskaitēm, ceļojumu pieprasījumiem, naudas avansiem un pievienotās vērtības nodokļa (PVN) atmaksāšanai.</span><span class="sxs-lookup"><span data-stu-id="e16fa-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="e16fa-111">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="e16fa-111">**Example**</span></span>

<span data-ttu-id="e16fa-112">Tālāk minētais process ir izmaksu atskaites izmaksu pārvaldības darbplūsmas piemērs.</span><span class="sxs-lookup"><span data-stu-id="e16fa-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="e16fa-113">Darbinieks izveido un saglabā izmaksu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="e16fa-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="e16fa-114">Darbinieks iesniedz izdevumu atskaiti apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="e16fa-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="e16fa-115">Apstiprinātājs tiek noteikts, pamatojoties uz kārtulām, kas tika definētas, iestatot darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="e16fa-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="e16fa-116">Apstiprinātājs saņem paziņojumu, ka izdevumu atskaite ir gatava apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="e16fa-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="e16fa-117">Apstiprinātājs pārskata izmaksu atskaiti un pārbauda, vai ir izpildīti tālāk minētie nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="e16fa-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="e16fa-118">Izdevumi nepārkāpj nevienu izdevumu politiku.</span><span class="sxs-lookup"><span data-stu-id="e16fa-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="e16fa-119">Ja izdevumi pārkāpj politiku, apstiprinātājs pārbauda, vai izmaksu atskaitē ir iekļauts derīgs komerciāls pamatojums.</span><span class="sxs-lookup"><span data-stu-id="e16fa-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="e16fa-120">Izmaksu atskaitei ir pievienotas elektroniskas kvītis.</span><span class="sxs-lookup"><span data-stu-id="e16fa-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="e16fa-121">Apstiprinātājs apstiprina izdevumu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="e16fa-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="e16fa-122">Izdevumu atskaite tiek piešķirta kreditoru koordinatoram grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="e16fa-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="e16fa-123">Tiek veikta viena no tālāk minētajām darbībām atkarībā no tā, vai ir konfigurēta automātiskā grāmatošana.</span><span class="sxs-lookup"><span data-stu-id="e16fa-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="e16fa-124">Ja ir konfigurēta automātiskā grāmatošana, izmaksu atskaite tiek apstrādāta maksājumam un izmaksu atskaites statuss tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="e16fa-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="e16fa-125">Ja automātiskā grāmatošana nav konfigurēta, kreditoru koordinators pārbauda, vai ir iesniegtas visi oriģinālās kvītis un vai kvītis atbilst izdevumu atskaitē norādītajiem izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="e16fa-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="e16fa-126">Visiem nodokļu kodiem, kas ievadīti izdevumu atskaitē, arī ir jābūt pārbaudītiem.</span><span class="sxs-lookup"><span data-stu-id="e16fa-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="e16fa-127">Kad šīs prasības ir pārbaudītas, izmaksu atskaite tiek iegrāmatota.</span><span class="sxs-lookup"><span data-stu-id="e16fa-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="e16fa-128">Pēc tam, kad izmaksu atskaite ir iegrāmatota, maksājums ir atļauts izdevumu atskaitei, un darbiniekam tiek piešķirta atmaksa.</span><span class="sxs-lookup"><span data-stu-id="e16fa-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>