---
title: Projekta līguma apstiprināšana
description: Šajā tēmā ir sniegta informācija par līguma apstiprināšanu risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128292"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="721fb-103">Projekta līguma apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="721fb-103">Confirm a project contract</span></span>

<span data-ttu-id="721fb-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="721fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="721fb-105">Projekta līgums risinājumā Dynamics 365 Project Operations var būt aktīvs, ja tā iemesls ir **Apstiprināts** vai tas ir slēgts ar iemeslu **Zaudēts**.</span><span class="sxs-lookup"><span data-stu-id="721fb-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="721fb-106">Kad apstiprināsit projekta līgumu, statuss tiks atjaunināts no **Melnraksts** uz **Aktīvs** un statusa iemesls tiks iestatīts kā **Apstiprināts**.</span><span class="sxs-lookup"><span data-stu-id="721fb-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="721fb-107">Aktīvu vai slēgtu līgumu nevar rediģēt vai atkārtoti atvērt.</span><span class="sxs-lookup"><span data-stu-id="721fb-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="721fb-108">Projekta līguma apstiprināšanas finansiālā ietekme</span><span class="sxs-lookup"><span data-stu-id="721fb-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="721fb-109">Kad projekta līgums būs apstiprināts, lietojumprogramma atkārtoti aprēķinās izmaksas, atsaucot vecās faktiskās izmaksas un izveidojot jaunas faktiskās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="721fb-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="721fb-110">Jaunās faktiskās izmaksas tiek apstrādātas, pamatojoties uz saistītās projekta līguma rindas norēķinu metodi.</span><span class="sxs-lookup"><span data-stu-id="721fb-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="721fb-111">Ja faktisko izmaksu atsauce ir atsauce līguma rinda Laiks un Materiāli, lietojumprogramma automātiski no jauna izveido atbilstošos rēķinā neiekļautās pārdošanas faktiskos datus.</span><span class="sxs-lookup"><span data-stu-id="721fb-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="721fb-112">Ja faktisko izmaksu atsauce ir fiksētas cenas līguma rinda, lietojumprogramma pārtrauc faktisko izmaksu pārstrādi.</span><span class="sxs-lookup"><span data-stu-id="721fb-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="721fb-113">Tiek izvērtēta faktisko rādītāju nepārsniegšanas ierobežojumi, apmaksājamības iestatījumi, kā arī cenas un izmaksas, bet pēc tam tie tiek atjaunināti apstiprināšanas procesa ietvaros.</span><span class="sxs-lookup"><span data-stu-id="721fb-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="721fb-114">Līguma kā zaudēta līguma slēgšana</span><span class="sxs-lookup"><span data-stu-id="721fb-114">Close a project contract as lost</span></span>

<span data-ttu-id="721fb-115">Slēdzot projekta līgumu kā zaudētu, līguma statuss tiek atjaunināts uz **Slēgts** un statusa iemesls tiek norādīts kā **Zaudēts**.</span><span class="sxs-lookup"><span data-stu-id="721fb-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="721fb-116">Projekta līgums kļūst tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="721fb-116">The project contract becomes read-only.</span></span> <span data-ttu-id="721fb-117">Pirms izmaiņas ir pabeigtas tiek parādīts apstiprinājuma dialogs, jo nevar atkārtoti atvērt slēgtu projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="721fb-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="721fb-118">Ja projekta līgumā, kas ir slēgts kā zaudēts, ir atsauce uz projektu savās rindās, šis projekts arī tiek atzīmēts kā slēgts.</span><span class="sxs-lookup"><span data-stu-id="721fb-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="721fb-119">Visas resursu rezervācijas no šīs dienas uz priekšu tiek atceltas.</span><span class="sxs-lookup"><span data-stu-id="721fb-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="721fb-120">Visi rēķinā neiekļautās pārdošanas faktiskie dati projekta līgumā, kas nav iekļauti rēķinā, tiks atcelti.</span><span class="sxs-lookup"><span data-stu-id="721fb-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="721fb-121">Risinājumā Dynamics 365 Project Operations projekta līguma kā zaudēta līguma slēgšana neietekmēs saistītās iespējas statusu.</span><span class="sxs-lookup"><span data-stu-id="721fb-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="721fb-122">Iespēja paliks atvērta, un tā būs jāaizver manuāli.</span><span class="sxs-lookup"><span data-stu-id="721fb-122">The opportunity will remain open and must be manually closed.</span></span>
