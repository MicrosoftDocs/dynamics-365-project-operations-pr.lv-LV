---
title: Piedāvājuma slēgšana
description: Šajā tēmā ir sniegta informācija par piedāvājumu slēgšanu programmā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2c752ba6395ed4bf025092219350dc245f7428f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277257"
---
# <a name="close-a-quote"></a><span data-ttu-id="0eb67-103">Piedāvājuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="0eb67-103">Close a quote</span></span>

<span data-ttu-id="0eb67-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="0eb67-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0eb67-105">Projekta piedāvājumu var slēgt kā iegūtu vai zaudētu.</span><span class="sxs-lookup"><span data-stu-id="0eb67-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="0eb67-106">Tā kā Microsoft Dynamics 365 Project Operations piedāvājumu funkcijas Aktivizēt un Pārskatīt netiek atbalstītas, varat aizvērt piedāvājuma melnrakstu.</span><span class="sxs-lookup"><span data-stu-id="0eb67-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="0eb67-107">Iegūta piedāvājuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="0eb67-107">Close a quote as Won</span></span>

<span data-ttu-id="0eb67-108">Slēdzot projekta piedāvājumu kā iegūtu, piedāvājumam tiks iestatīts statuss **Slēgts** un statusa iemesls **Iegūts**.</span><span class="sxs-lookup"><span data-stu-id="0eb67-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="0eb67-109">Slēdzot piedāvājumu, tas kļūst tikai lasāms, un tiek izveidots projekta līguma melnraksts ar visu piedāvājuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="0eb67-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="0eb67-110">Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms piedāvājuma slēgšanas tiks parādīts apstiprinājuma dialogs, lai apstiprinātu veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="0eb67-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="0eb67-111">No projekta piedāvājuma izveidotais projekta līgums ir pieejams arī Project Operations modulī Projekta pārvaldība un grāmatvedība.</span><span class="sxs-lookup"><span data-stu-id="0eb67-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="0eb67-112">Ja projekta līgums nav kartēts uz projektu jebkurā no tā rindām, šis projekta līgums tiek padarīts pieejams kā neaktīvs projekta līgums un kļūst aktīvs, tiklīdz projekts tiek kartēts uz vismaz vienu no tā līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="0eb67-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="0eb67-113">Ja piedāvājums ir pievienots iespējai, visi pārējie iespējas projekta piedāvājumi tiek automātiski slēgti kā zaudēti.</span><span class="sxs-lookup"><span data-stu-id="0eb67-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="0eb67-114">Finansiālā ietekme, piedāvājumu slēdzot kā iegūtu</span><span class="sxs-lookup"><span data-stu-id="0eb67-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="0eb67-115">Ja projektā ir reģistrēti faktiskie laika dati, kamēr tas joprojām ir pievienots piedāvājuma melnrakstam, tiek reģistrētas tikai laika izmaksas vai izdevumi.</span><span class="sxs-lookup"><span data-stu-id="0eb67-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="0eb67-116">Kad piedāvājums būs slēgts kā iegūts, lietojumprogramma pārstrukturizēs izmaksas, atsaucot vecās faktiskās izmaksas un atkārtoti izveidojot jaunas faktiskās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="0eb67-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="0eb67-117">Lietojumprogramma apstrādās šīs faktiskās izmaksas, pamatojoties uz saistītās projekta līguma rindas norēķinu metodi.</span><span class="sxs-lookup"><span data-stu-id="0eb67-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="0eb67-118">Ja faktiskajās izmaksās ir atsauce uz laika un materiālu līguma rindu, sistēma automātiski izveidos atbilstošos rēķinā neiekļautos pārdošanas faktiskos datus, kad tiks slēgts piedāvājums un tiks izveidots projekta līgums.</span><span class="sxs-lookup"><span data-stu-id="0eb67-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="0eb67-119">Ja faktiskajās izmaksās ir atsauce uz fiksētas cenas līguma rindu, lietojumprogramma pārtrauks faktisko izmaksu atkārtotu apstrādi, pamatojoties uz projekta līguma klientu sadalīšanas norēķinu kārtulām.</span><span class="sxs-lookup"><span data-stu-id="0eb67-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="0eb67-120">Visi atkārtoti apstrādātie faktiskie dati ir pieejami projekta grāmatvedim modulī Projekta pārvaldība un grāmatvedība, lai tos pārskatītu, atjauninātu un grāmatotu virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="0eb67-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="0eb67-121">Zaudēta piedāvājuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="0eb67-121">Close a quote as Lost</span></span>

<span data-ttu-id="0eb67-122">Slēdzot projekta piedāvājumu kā zaudētu, piedāvājums tiks slēgts ar statusu **Slēgts** un statusa iemeslu **Zaudēts**.</span><span class="sxs-lookup"><span data-stu-id="0eb67-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="0eb67-123">Slēdzot piedāvājumu, tas kļūst tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="0eb67-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="0eb67-124">Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms piedāvājuma slēgšanas tiks parādīts apstiprinājuma dialogs, lai apstiprinātu veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="0eb67-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="0eb67-125">Ja projekta piedāvājuma, kas ir slēgts kā zaudēts, jebkurā rindā ir atsauce uz kādu projektu, arī šis projekts tiek atzīmēts arī kā slēgts, kā arī tiek atceltas visas turpmākās resursu rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="0eb67-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="0eb67-126">Programmā Project Operations slēdzot piedāvājumu kā iegūtu vai zaudētu, netiks ietekmēts iespējas statuss — tā paliks atvērta, līdz tiks manuāli slēgta.</span><span class="sxs-lookup"><span data-stu-id="0eb67-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]