---
title: Ceļojuma pieprasījumi
description: Šajā tēmā ir sniegta informācija par ceļojuma pieprasījumiem.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: e05f54349eaa09dd22331ff07950542dd326e711
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001750"
---
# <a name="travel-requisitions"></a><span data-ttu-id="36fc7-103">Ceļojuma pieprasījumi</span><span class="sxs-lookup"><span data-stu-id="36fc7-103">Travel requisitions</span></span>

<span data-ttu-id="36fc7-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="36fc7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="36fc7-105">Ceļojuma pieprasījumā ir uzskaitīti izdevumi, kas radīsies ceļojuma vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="36fc7-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="36fc7-106">Ceļojuma pieprasījumu iesniedz pārskatīšanai, un to var izmantot, lai atļautu izdevumus.</span><span class="sxs-lookup"><span data-stu-id="36fc7-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="36fc7-107">Jums var prasīt iesniegt ceļojuma pieprasījumu, pirms rodas jebkādi izdevumi, kas jāapmaksā organizācijai.</span><span class="sxs-lookup"><span data-stu-id="36fc7-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="36fc7-108">Šī prasība ir spēkā neatkarīgi no tā, vai izdevumi rodas, izmantojot uzņēmuma kredītkarti, tērējat avansā saņemtu skaidru naudu vai arī jūsu izdevumus vēlāk atlīdzinās organizācija.</span><span class="sxs-lookup"><span data-stu-id="36fc7-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="36fc7-109">Ceļojuma pieprasījumus un politikas var izmantot, lai palīdzētu pārvaldīt organizācijas izdevumus.</span><span class="sxs-lookup"><span data-stu-id="36fc7-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="36fc7-110">Piemēram, ja jūsu organizācija strādā ar fiksētas cenas projektu, kurā nepieciešama ceļošana, projekta darba grupas dalībnieku ceļojuma izdevumiem ir jāatbilst projekta budžetam.</span><span class="sxs-lookup"><span data-stu-id="36fc7-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="36fc7-111">Pieprasot ceļojuma izdevumus apstiprināt pirms to rašanās, organizācija var palīdzēt nodrošināt, ka projekts nepārsniegs budžetu.</span><span class="sxs-lookup"><span data-stu-id="36fc7-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="36fc7-112">Konfigurācija</span><span class="sxs-lookup"><span data-stu-id="36fc7-112">Configuration</span></span> 

<span data-ttu-id="36fc7-113">Ceļojuma pieprasījumus var konfigurēt kā “obligātus”, izdevumu pārvaldības parametros iespējojot parametru “Atļauja pirms ceļošanas ir obligāta”.</span><span class="sxs-lookup"><span data-stu-id="36fc7-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="36fc7-114">Ceļojuma pieprasījuma izveide un iesniegšana</span><span class="sxs-lookup"><span data-stu-id="36fc7-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="36fc7-115">Dodieties uz **Mani izdevumi: ceļojuma pieprasījums** un atlasiet **Jauns ceļojuma pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="36fc7-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="36fc7-116">Ievadiet pieprasījuma nolūku un galamērķi.</span><span class="sxs-lookup"><span data-stu-id="36fc7-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="36fc7-117">Laukā **Ceļojuma apraksts** ievadiet papildinformāciju.</span><span class="sxs-lookup"><span data-stu-id="36fc7-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="36fc7-118">Katram no paredzamajiem izdevumiem, piemēram, lidojumiem, maltītēm vai automašīnu nomai, izveidojiet izdevumu rindas elementu.</span><span class="sxs-lookup"><span data-stu-id="36fc7-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="36fc7-119">Katram izdevumam norādiet plānoto datumu, plānoto summu un valūtu.</span><span class="sxs-lookup"><span data-stu-id="36fc7-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="36fc7-120">Kad esat beidzis pievienot paredzamos izdevumus, atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="36fc7-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="36fc7-121">Kad esat gatavs iesniegt ceļojuma pieprasījumu, atlasiet **Darbplūsma** > **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="36fc7-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="36fc7-122">Savus apstiprinātos ceļojuma pieprasījumus varat skatīt sadaļā **Mani izdevumi: ceļojuma pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="36fc7-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="36fc7-123">Pieejamo ceļojuma pieprasījumu skatīšana</span><span class="sxs-lookup"><span data-stu-id="36fc7-123">View available travel requisitions</span></span>

<span data-ttu-id="36fc7-124">Visus savus ceļojuma pieprasījumus varat skatīt sadaļā **Mani izdevumi: ceļojuma pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="36fc7-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="36fc7-125">Ceļojuma pieprasījumu apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="36fc7-125">Approve travel requisitions</span></span>

<span data-ttu-id="36fc7-126">Atlasiet ceļojuma pieprasījumu, kuru vēlaties apstiprināt, un pēc tam atlasiet **Darbplūsma** > **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="36fc7-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="36fc7-127">Izdevumu atskaites iesniegšana, izmantojot apstiprināto ceļojuma pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="36fc7-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="36fc7-128">Izveidojiet jaunu izdevumu atskaiti un izdevumu atskaites galvenē, kā arī apstiprināto ceļa pieprasījumu sarakstā atlasiet **Kartēt uz ceļojuma pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="36fc7-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="36fc7-129">Lauks **Ceļojuma pieprasījuma summa** tiek automātiski atjaunināts izdevumu atskaites galvenē.</span><span class="sxs-lookup"><span data-stu-id="36fc7-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="36fc7-130">Pievienojiet visus izdevumus, kas radušies ceļojuma laikā.</span><span class="sxs-lookup"><span data-stu-id="36fc7-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="36fc7-131">Ja ir aktivizēts lauks **Iepriekš atļauts**, tiek atjaunināta konkrētās izdevumu kategorijas saskaņotā summa un atļautā summa.</span><span class="sxs-lookup"><span data-stu-id="36fc7-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="36fc7-132">Kartējot izdevumu atskaiti uz apstiprinātu ceļojuma pieprasījumu, transakcijas summa nevar būt lielāka par atļauto summu.</span><span class="sxs-lookup"><span data-stu-id="36fc7-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]