---
title: Izdevumu politiku iestatīšana
description: Varat iestatīt izdevumu politikas, kuras jūsu darbiniekiem ir jāievēro, ievadot un iesniedzot izdevumu atskaites un komandējumu pieprasījumus risinājumā Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650103"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="d2e94-103">Izdevumu politiku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d2e94-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2e94-104">Varat definēt politikas, kuras jūsu darbiniekiem ir jāievēro, ievadot un iesniedzot izdevumu atskaites un komandējumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="d2e94-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="d2e94-105">Izdevumu politiku ieviešana var palīdzēt efektīvi pārvaldīt izdevumus.</span><span class="sxs-lookup"><span data-stu-id="d2e94-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="d2e94-106">Piemēram, varat iestatīt politiku viesnīcas izdevumiem Ņujorkā, kuri nosaka, ka izdevumi par nakti nedrīkst pārsniegt 250 USD.</span><span class="sxs-lookup"><span data-stu-id="d2e94-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="d2e94-107">Ja darbinieks iesniedz izdevumu atskaiti vai komandējuma pieprasījumu, kur numura likme pārsniedz šo summu, sistēma to paziņos</span><span class="sxs-lookup"><span data-stu-id="d2e94-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="d2e94-108">darbiniekam, ka ir pārsniegta izdevumu politikas summa.</span><span class="sxs-lookup"><span data-stu-id="d2e94-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="d2e94-109">Varat konfigurēt ziņojumu, kuru darbinieks saņems, kad</span><span class="sxs-lookup"><span data-stu-id="d2e94-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="d2e94-110">definēsit politiku.</span><span class="sxs-lookup"><span data-stu-id="d2e94-110">define the policy.</span></span>      
        
<span data-ttu-id="d2e94-111">Varat definēt triju veidu politikas:</span><span class="sxs-lookup"><span data-stu-id="d2e94-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="d2e94-112">Brīdinājums — ļauj darbiniekam iesniegt izdevumu atskaiti vai komandējuma pieprasījumu, taču izdevumi tiks atzīmēti visiem apstiprinātājiem un</span><span class="sxs-lookup"><span data-stu-id="d2e94-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="d2e94-113">vēlākai ziņošanai.</span><span class="sxs-lookup"><span data-stu-id="d2e94-113">for later reporting.</span></span>        

- <span data-ttu-id="d2e94-114">Kļūda — darbiniekam ir jāpārskata izdevumi, lai tie atbilstu politikai, pirms viņš iesniedz izdevumu atskaiti vai komandējuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="d2e94-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="d2e94-115">Pamatojums — darbiniekam vai vadītājam ir jāievada pamatojums politikas apmēra pārsniegšanai, pirms tiek iesniegta izdevumu atskaite vai komandējuma pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="d2e94-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="d2e94-116">Politikas padomi</span><span class="sxs-lookup"><span data-stu-id="d2e94-116">Policy tips</span></span>
<span data-ttu-id="d2e94-117">Tālāk sniegti daži ierosinājumi, kas var jums palīdzēt, veidojot jaunas izdevumu pārvaldības politikas.</span><span class="sxs-lookup"><span data-stu-id="d2e94-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="d2e94-118">Politikām ir spēkā stāšanās datums, un tās nestāsies spēkā, ja politika tiks izveidota ar datumu pēc izdevumu rašanās datuma.</span><span class="sxs-lookup"><span data-stu-id="d2e94-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="d2e94-119">Piemēram, ja šodien izveidojat jaunu politiku, lai īstenotu 50 ASV dolāru vērtus maksimālo maltīšu izdevumus, tad jebkādas no vakardienas esošām izmaksām netiks pārbaudītas attiecībā pret šo politiku.</span><span class="sxs-lookup"><span data-stu-id="d2e94-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="d2e94-120">Veidojot politiku izdevumu kategorijai, kuru nevar uzskaitīt, apsveriet pievienot izdevumu rindas veida nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="d2e94-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="d2e94-121">Dažas politikas, piemēram, ieejas plūsmas pieprasīšana, var nebūt noderīgas detalizētām rindām, un tās ir jālieto tikai galvenes rindai vai neiekļautai rindai.</span><span class="sxs-lookup"><span data-stu-id="d2e94-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="d2e94-122">Izdevumu pārvaldības politikas pēc noklusējuma tiek novērtētas attiecībā pret avota entitīju.</span><span class="sxs-lookup"><span data-stu-id="d2e94-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="d2e94-123">Starpuzņēmumu scenārijos varat iestatīt, ka politika tiek novērtēta attiecībā pret mērķa entitīju (aizņēmuma entitīju).</span><span class="sxs-lookup"><span data-stu-id="d2e94-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="d2e94-124">Lai palaistu politiku pret mērķa entītīju, ieslēdziet līdzekli “Novērtēt Izdevumu politiku attiecībā pret aizņēmuma juridisko entītiju” darbvietā **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="d2e94-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="d2e94-125">Kad novērtēt politikas</span><span class="sxs-lookup"><span data-stu-id="d2e94-125">When to evaluate policies</span></span>

<span data-ttu-id="d2e94-126">Izdevumu pārvaldības parametros ir iespēja novērtēt izdevumu pārvaldības politikas, kad tiek saglabāta rinda vai tiek iesniegts izdevumu pārskats.</span><span class="sxs-lookup"><span data-stu-id="d2e94-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="d2e94-127">Ja izvēlaties novērtēt, kad tiek saglabāta rinda, tiek nodrošināts, ka lietotājiem ir iepriekš redzama informācija par to, kas jādara, lai pabeigtu izdevumu pārskatu visu uzreiz.</span><span class="sxs-lookup"><span data-stu-id="d2e94-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="d2e94-128">Pretējā gadījumā var aizkavēt politikas novērtēšanu un ietaupīt laiku, ja validācija notiek beigās, iesniegšanas darbplūsmā laikā.</span><span class="sxs-lookup"><span data-stu-id="d2e94-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
