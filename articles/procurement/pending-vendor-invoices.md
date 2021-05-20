---
title: Krājumos neesošu materiālu iegāde, izmantojot neapstiprinātu piegādātāju rēķinu
description: Šajā tēmā ir izskaidrots, kā ierakstīt neapstiprinātus piegādātāju rēķinus.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880664"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="c2661-103">Krājumos neesošu materiālu iegāde, izmantojot neapstiprinātu piegādātāju rēķinu</span><span class="sxs-lookup"><span data-stu-id="c2661-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="c2661-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="c2661-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c2661-105">Kad uzņēmums projekta vajadzībām veic krājumos neesošu materiālu iepirkumu, izmaksas var nekavējoties reģistrēt saistībā ar šo projektu.</span><span class="sxs-lookup"><span data-stu-id="c2661-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="c2661-106">Piemēram, Contoso Robotics US īsteno aprīkojuma atjaunošanas projektu, un tam ir nepieciešamas programmatūras licences.</span><span class="sxs-lookup"><span data-stu-id="c2661-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="c2661-107">Šīs licences tiek iegādātas no trešās puses piegādātāja.</span><span class="sxs-lookup"><span data-stu-id="c2661-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="c2661-108">Izmantojot Dynamics 365 Finance, kreditoru ierēdnis ieraksta neapstiprinātu piegādātāja rēķina dokumentu un pieskaita licences izmaksas tieši aprīkojuma atjaunošanas projektam.</span><span class="sxs-lookup"><span data-stu-id="c2661-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="c2661-109">Pirms šajā tēmā aprakstītās funkcionalitātes izmantošanas pārskatiet un lietojiet nepieciešamās konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c2661-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="c2661-110">Papildinformāciju skatiet sadaļā [Krājumos neesošu materiālu un neapstiprinātu piegādātāju rēķinu iespējošana](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="c2661-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="c2661-111">Ar projektu saistīta neapstiprināta piegādātāja rēķina grāmatošana</span><span class="sxs-lookup"><span data-stu-id="c2661-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="c2661-112">Neapstiprinātos piegādātāju rēķinus var ierakstīt lapā **Neapstiprinātie piegādātāju rēķini** (**Kreditori** > **Rēķini** > **Neapstiprinātie piegādātāju rēķini**).</span><span class="sxs-lookup"><span data-stu-id="c2661-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="c2661-113">Lai grāmatotu ar projektu saistītu neapstiprinātu piegādātāja rēķinu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c2661-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="c2661-114">Dodieties uz **Kreditori** > **Rēķini** un atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c2661-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="c2661-115">Laukā **Rēķina konts** atlasiet piegādātāju un laukā **Numurs** ievadiet piegādātāja rēķina identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="c2661-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="c2661-116">Pievienojiet piegādātāja rēķinam rindu un laukā **Vienuma numurs** atlasiet no piegādātāja iegādāto krājumos neesošo preci.</span><span class="sxs-lookup"><span data-stu-id="c2661-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="c2661-117">Piegādātāja rēķina rindas, kas ir balstītas uz sagādes kategoriju, nevar ierakstīt attiecībā uz projektu.</span><span class="sxs-lookup"><span data-stu-id="c2661-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="c2661-118">Pievienojiet iegādāto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="c2661-118">Add the quantity purchased.</span></span> <span data-ttu-id="c2661-119">Sistēma aizpilda cenu par vienību, pamatojoties uz krājumos neesošo preču cenas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c2661-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="c2661-120">Pārbaudiet kopējo summu un citu rindā nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="c2661-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="c2661-121">Rindas detalizētās informācijas cilnē **Projekts** atlasiet tā projekta ID, kurā šis vienums tiks ierakstīts.</span><span class="sxs-lookup"><span data-stu-id="c2661-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="c2661-122">Ja vēlaties, atlasiet darbības numuru un atjauniniet projekta kategoriju un rindas rekvizītu.</span><span class="sxs-lookup"><span data-stu-id="c2661-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="c2661-123">Grāmatojiet neapstiprināto piegādātāja rēķinu.</span><span class="sxs-lookup"><span data-stu-id="c2661-123">Post pending vendor invoice.</span></span> <span data-ttu-id="c2661-124">Kad rēķins ir grāmatots, sistēma ieraksta:</span><span class="sxs-lookup"><span data-stu-id="c2661-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="c2661-125">piegādātāja bilances summu;</span><span class="sxs-lookup"><span data-stu-id="c2661-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="c2661-126">PVN summu.</span><span class="sxs-lookup"><span data-stu-id="c2661-126">The sales tax amount.</span></span>
    - <span data-ttu-id="c2661-127">Projekta izmaksas tiek ierakstītas sagādes integrācijas kontā.</span><span class="sxs-lookup"><span data-stu-id="c2661-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="c2661-128">Projekta faktiskā transakcija programmā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c2661-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="c2661-129">Šī transakcija tiek apstrādāta tālāk, izmantojot [Project Operations integrācijas žurnālu](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="c2661-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="c2661-130">Grāmatojot šo žurnālu, summa tiek pārvietota no sagādes integrācijas konta uz projekta izmaksu kontu.</span><span class="sxs-lookup"><span data-stu-id="c2661-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
