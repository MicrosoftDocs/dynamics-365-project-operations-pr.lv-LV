---
title: Darbs ar personīgajiem izdevumiem izdevumu atskaitē
description: Šajā tēmā sniegta informācija par to, kā strādāt ar personīgajiem izdevumiem, kas darbiniekiem radušies, ceļojot darba vajadzībām.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025693"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="9997f-103">Darbs ar personīgajiem izdevumiem izdevumu atskaitē</span><span class="sxs-lookup"><span data-stu-id="9997f-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="9997f-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="9997f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9997f-105">Komandējuma laikā darbinieks var ieturēt personīgos izdevumus no savas uzņēmuma kredītkartes.</span><span class="sxs-lookup"><span data-stu-id="9997f-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="9997f-106">Ja personīgo izdevumu apstrādei nav noteikts process, izdevumu atskaites apstiprināšanas process var tikt traucēts, kad darbinieks iesniedz uzskaitīto izdevumu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="9997f-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="9997f-107">Lai strādātu ar darbinieka personīgajiem izdevumiem, varat pielietot divas metodes:</span><span class="sxs-lookup"><span data-stu-id="9997f-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="9997f-108">**Apmaksā darbinieks**: Jūsu organizācija neapmaksā personiskos izdevumus, kas parādās uzņēmuma kredītkartes rēķinā.</span><span class="sxs-lookup"><span data-stu-id="9997f-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="9997f-109">Tā vietā darbinieks par izdevumiem maksā tieši kredītkartes pārdevējam.</span><span class="sxs-lookup"><span data-stu-id="9997f-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="9997f-110">**Apmaksā uzņēmums**: Jūsu organizācija apmaksā pilno rēķinu par uzņēmuma kredītkarti un pēc tam ietur debetu no darbinieka konta par personīgajiem izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="9997f-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="9997f-111">Lapā **Izdevumu pārvaldības parametri** varat atlasīt metodi, ko organizācija izmanto.</span><span class="sxs-lookup"><span data-stu-id="9997f-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="9997f-112">Dalīto izdevumu funkcijas iespējošana, kad personiskās summas laukā ir definēta vērtība</span><span class="sxs-lookup"><span data-stu-id="9997f-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="9997f-113">Līdzeklis **Dalīto izdevumu funkcijas iespējošana, kad personiskās summas laukā ir definēta vērtība** attiecas tikai uz tām izdevumu atskaitēm, kas ir apstiprinātas, izmantojot rindas līmeņa darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="9997f-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="9997f-114">Atskaites tiek apstiprinātas, atverot sadaļu **Procesu izdevumu atskaites** > **Man piešķirtās izdevumu atskaites** > **Atvērt izdevumu atskaiti**.</span><span class="sxs-lookup"><span data-stu-id="9997f-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="9997f-115">Lai iespējotu šo līdzekli, dodieties uz **Darbvietas** > **Līdzekļu pārvaldība**, atlasiet **Dalīto izdevumu funkcijas iespējošana, kad personiskās summas laukā ir definēta vērtība** un pēc tam atlasiet **Iespējot tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="9997f-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="9997f-116">Ja līdzeklis ir iespējots, izdevumu rindas, kas izmanto šo funkcionalitāti, atskaites iesniegšanas laikā ģenerē divas rindas.</span><span class="sxs-lookup"><span data-stu-id="9997f-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="9997f-117">Abas rindas tiek ģenerētas, lai apstiprinātājs katru rindu varētu apstiprināt atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="9997f-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
