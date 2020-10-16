---
title: Piedāvājumu slēgšana
description: Šajā tēmā ir sniegta informācija par piedāvājuma slēgšanu programmā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896200"
---
# <a name="close-quotes"></a><span data-ttu-id="af574-103">Piedāvājumu slēgšana</span><span class="sxs-lookup"><span data-stu-id="af574-103">Close quotes</span></span> 

<span data-ttu-id="af574-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="af574-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="af574-105">Projekta piedāvājumu var slēgt kā iegūtu vai zaudētu.</span><span class="sxs-lookup"><span data-stu-id="af574-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="af574-106">Programmā Microsoft Dynamics 365 Project Operations netiek atbalstītas piedāvājumu aktivizēšanas un pārskatīšanas operācijas, tāpēc var slēgt piedāvājuma melnrakstu.</span><span class="sxs-lookup"><span data-stu-id="af574-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="af574-107">Iegūta piedāvājuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="af574-107">Close a quote as Won</span></span>

<span data-ttu-id="af574-108">Slēdzot projekta piedāvājumu kā iegūtu, piedāvājums tiks slēgts ar statusu Slēgts un statusa iemeslu Iegūts.</span><span class="sxs-lookup"><span data-stu-id="af574-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="af574-109">Slēdzot piedāvājumu, projekta piedāvājums kļūst tikai lasāms, un tiek izveidots projekta līguma melnraksts, kurā ir ietverta piedāvājuma informācija.</span><span class="sxs-lookup"><span data-stu-id="af574-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="af574-110">Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms izmaiņu veikšanas tiek parādīts apstiprinājuma dialogs, jo slēgtu piedāvājumu vairs nevar atvērt un izmaiņas ir neatgriezeniskas.</span><span class="sxs-lookup"><span data-stu-id="af574-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="af574-111">Ja piedāvājums ir pievienots iespējai, visi pārējie iespējas projekta piedāvājumi tiek automātiski slēgti kā zaudēti.</span><span class="sxs-lookup"><span data-stu-id="af574-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="af574-112">Finansiālā ietekme, piedāvājumu slēdzot kā iegūtu</span><span class="sxs-lookup"><span data-stu-id="af574-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="af574-113">Ja projektā ir reģistrēti faktiskie laika dati, kamēr tas joprojām ir pievienots piedāvājuma melnrakstam, tiek reģistrētas tikai laika izmaksas vai izdevumi.</span><span class="sxs-lookup"><span data-stu-id="af574-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="af574-114">Kad piedāvājums būs slēgts kā iegūts, lietojumprogramma pārstrukturizēs izmaksas, atsaucot vecās faktiskās izmaksas un atkārtoti izveidojot jaunas faktiskās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="af574-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="af574-115">Lietojumprogramma apstrādās šīs faktiskās izmaksas, pamatojoties uz saistītās projekta līguma rindas norēķinu metodi.</span><span class="sxs-lookup"><span data-stu-id="af574-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="af574-116">Ja faktiskajās izmaksās ir atsauce uz laika un materiālu līguma rindu, sistēma automātiski izveidos atbilstošos rēķinā neiekļautos pārdošanas faktiskos datus, kad tiks slēgts piedāvājums un tiks izveidots projekta līgums.</span><span class="sxs-lookup"><span data-stu-id="af574-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="af574-117">Ja faktiskajās izmaksās ir atsauce uz fiksētas cenas līguma rindu, lietojumprogramma pārtrauks faktisko izmaksu atkārtotu apstrādi, pamatojoties uz projekta līguma klientu sadalīšanas norēķinu kārtulām.</span><span class="sxs-lookup"><span data-stu-id="af574-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="af574-118">Zaudēta piedāvājuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="af574-118">Closing a quote as lost:</span></span>

<span data-ttu-id="af574-119">Slēdzot projekta piedāvājumu kā zaudētu, piedāvājums tiks slēgts ar statusu Slēgts un statusa iemeslu Zaudēts.</span><span class="sxs-lookup"><span data-stu-id="af574-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="af574-120">Slēdzot piedāvājumu, projekta piedāvājums kļūst tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="af574-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="af574-121">Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms piedāvājuma slēgšanas tiks parādīts apstiprinājuma dialogs, lai apstiprinātu veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="af574-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="af574-122">Ja projekta piedāvājuma, kas ir slēgts kā zaudēts, jebkurā rindā ir atsauce uz kādu projektu, arī šis projekts tiek atzīmēts arī kā slēgts, kā arī tiek atceltas visas turpmākās resursu rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="af574-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="af574-123">Programmā Project Operations slēdzot piedāvājumu kā iegūtu vai zaudētu, netiks ietekmēts iespējas statuss — tā paliks atvērta, līdz tiks manuāli slēgta.</span><span class="sxs-lookup"><span data-stu-id="af574-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
