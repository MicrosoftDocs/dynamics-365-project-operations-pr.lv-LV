---
title: Izdevumu politiku definēšana
description: Varat definēt izdevumu politikas, kuras jūsu darbiniekiem ir jāievēro, ievadot un iesniedzot izdevumu atskaites un komandējumu pieprasījumus.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001885"
---
# <a name="define-expense-policies"></a><span data-ttu-id="f3709-103">Izdevumu politiku definēšana</span><span class="sxs-lookup"><span data-stu-id="f3709-103">Define expense policies</span></span>

<span data-ttu-id="f3709-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="f3709-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f3709-105">Varat definēt politikas, kuras jūsu darbiniekiem ir jāievēro, ievadot un iesniedzot izdevumu atskaites un komandējumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="f3709-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="f3709-106">Izdevumu politiku ieviešana var palīdzēt efektīvi pārvaldīt izdevumus.</span><span class="sxs-lookup"><span data-stu-id="f3709-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="f3709-107">Piemēram, varat iestatīt politiku viesnīcas izdevumiem Ņujorkā, kuri nosaka, ka izdevumi par nakti nedrīkst pārsniegt 250 USD.</span><span class="sxs-lookup"><span data-stu-id="f3709-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="f3709-108">Ja darbinieks iesniedz izdevumu atskaiti vai komandējuma pieprasījumu, kurā numura likme pārsniedz šo summu sistēma paziņos</span><span class="sxs-lookup"><span data-stu-id="f3709-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="f3709-109">darbiniekam, ka ir pārsniegta izdevumu politikas summa.</span><span class="sxs-lookup"><span data-stu-id="f3709-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="f3709-110">Varat konfigurēt ziņojumu, kuru darbinieks saņems, kad</span><span class="sxs-lookup"><span data-stu-id="f3709-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="f3709-111">definēsit politiku.</span><span class="sxs-lookup"><span data-stu-id="f3709-111">define the policy.</span></span>      
        
<span data-ttu-id="f3709-112">Varat definēt triju veidu politikas:</span><span class="sxs-lookup"><span data-stu-id="f3709-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="f3709-113">**Brīdinājums**: Ļauj darbiniekam iesniegt izdevumu atskaiti vai komandējuma pieprasījumu, taču izdevumi tiks atzīmēti visiem apstiprinātājiem un</span><span class="sxs-lookup"><span data-stu-id="f3709-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="f3709-114">vēlākai ziņošanai.</span><span class="sxs-lookup"><span data-stu-id="f3709-114">for later reporting.</span></span>        

- <span data-ttu-id="f3709-115">**Kļūda**: Darbiniekam ir jāpārskata izdevumi, lai tie atbilstu politikai, pirms viņš iesniedz izdevumu atskaiti vai komandējuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="f3709-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="f3709-116">**Pamatojums**: Darbiniekam vai vadītājam ir jāievada pamatojums politikas apmēra pārsniegšanai, pirms tiek iesniegta izdevumu atskaite vai komandējuma pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="f3709-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="f3709-117">Politikas padomi</span><span class="sxs-lookup"><span data-stu-id="f3709-117">Policy tips</span></span>
<span data-ttu-id="f3709-118">Tālāk sniegti daži ierosinājumi, kas var jums palīdzēt, veidojot jaunas izdevumu pārvaldības politikas:</span><span class="sxs-lookup"><span data-stu-id="f3709-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="f3709-119">Politikām ir spēkā stāšanās datums, kas nozīmē, ka tās nestāsies spēkā, ja tiks izveidotas datumā, kas ir vēlāks par datumu, kad radās izdevumi.</span><span class="sxs-lookup"><span data-stu-id="f3709-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="f3709-120">Piemēram, jūs izveidojat jaunu politiku šodien, lai noteiktu, ka maksimālie maltīšu izdevumi ir 50$.</span><span class="sxs-lookup"><span data-stu-id="f3709-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="f3709-121">Jebkuri izdevumi, kas ievadīti no vakardienas, netiks pārbaudīti attiecībā pret šo politiku.</span><span class="sxs-lookup"><span data-stu-id="f3709-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="f3709-122">Veidojot politiku izdevumu kategorijai, kuru nevar uzskaitīt, apsveriet pievienot izdevumu rindas veida nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="f3709-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="f3709-123">Dažas politikas, piemēram, nepieciešamība pēc kvīts, var nebūt loģiskas attiecībā uz uzskaitītajām rindām.</span><span class="sxs-lookup"><span data-stu-id="f3709-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="f3709-124">Šādā gadījumā politika tiek piemērota vienīgi virsraksta rindai vai neuzskaitītajai rindai.</span><span class="sxs-lookup"><span data-stu-id="f3709-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="f3709-125">Izdevumu pārvaldības politikas pēc noklusējuma tiek novērtētas attiecībā pret avota entitīju.</span><span class="sxs-lookup"><span data-stu-id="f3709-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="f3709-126">Starpuzņēmumu scenārijos varat iestatīt, ka politika tiek novērtēta attiecībā pret mērķa entitīju (aizņēmuma entitīju).</span><span class="sxs-lookup"><span data-stu-id="f3709-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="f3709-127">Lai palaistu politiku pret mērķa entitīju, ieslēdziet līdzekli **Novērtēt Izdevumu politiku attiecībā pret aizņēmuma juridisko personu** darbvietā **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="f3709-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="f3709-128">Kad novērtēt politikas</span><span class="sxs-lookup"><span data-stu-id="f3709-128">When to evaluate policies</span></span>

<span data-ttu-id="f3709-129">Izdevumu pārvaldības parametros varat atlasīt izvērtēt izdevumu pārvaldības politikas, ja tiek saglabāta rinda vai ja tiek iesniegta izdevumu atskaite.</span><span class="sxs-lookup"><span data-stu-id="f3709-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="f3709-130">Ja izvēlaties izvērtēt, kad rinda tiek saglabāta, lietotajiem būs agrāka redzamība par to, kas viņiem ir jādara, lai vienlaikus aizpildītu visu izdevumu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="f3709-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="f3709-131">Pretējā gadījumā varat aizkavēt politikas novērtējumu un ietaupīt laiku beigās, iesniedzot darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="f3709-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]