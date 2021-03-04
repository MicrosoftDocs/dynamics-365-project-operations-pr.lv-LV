---
title: Piedāvājuma aizvēršana — Lite
description: Šajā tēmā ir sniegta informācija par piedāvājuma slēgšanu programmā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764873"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="d70a1-103">Piedāvājuma aizvēršana — Lite</span><span class="sxs-lookup"><span data-stu-id="d70a1-103">Close a quote - lite</span></span>

<span data-ttu-id="d70a1-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="d70a1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d70a1-105">Projekta piedāvājumu var slēgt kā iegūtu vai zaudētu.</span><span class="sxs-lookup"><span data-stu-id="d70a1-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="d70a1-106">Piedāvājuma melnrakstu var slēgt, jo Microsoft Dynamics 365 Project Operations neatbalsta aktivizēšanas un pārskatīšanas darbības.</span><span class="sxs-lookup"><span data-stu-id="d70a1-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="d70a1-107">Iegūta piedāvājuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="d70a1-107">Close a quote as Won</span></span>

<span data-ttu-id="d70a1-108">Slēdzot projekta piedāvājumu kā iegūtu, statuss tiek iestatīts uz aizvērtu un statusa iemesls ir Iegūts.</span><span class="sxs-lookup"><span data-stu-id="d70a1-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="d70a1-109">Slēdzot piedāvājumu, projekta piedāvājums kļūst tikai lasāms, un tiek izveidots projekta līguma melnraksts, kurā ir ietverta piedāvājuma informācija.</span><span class="sxs-lookup"><span data-stu-id="d70a1-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="d70a1-110">Tā kā slēgtu piedāvājumu nevar atvērt no jauna, jūsu izmaiņas apstiprinās apstiprinājuma dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="d70a1-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="d70a1-111">Ja piedāvājums ir pievienots iespējai, visi pārējie iespējas projekta piedāvājumi tiek automātiski slēgti kā zaudēti.</span><span class="sxs-lookup"><span data-stu-id="d70a1-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="d70a1-112">Finansiālā ietekme, piedāvājumu slēdzot kā iegūtu</span><span class="sxs-lookup"><span data-stu-id="d70a1-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="d70a1-113">Ja projekta laikam ir kādi faktiskie dati, kamēr tas joprojām ir pievienots projekta piedāvājumam, tiek ierakstītas tikai laika vai izdevumu izmaksas.</span><span class="sxs-lookup"><span data-stu-id="d70a1-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="d70a1-114">Kad piedāvājums būs slēgts kā iegūts, lietojumprogramma pārstrukturizēs izmaksas, atsaucot vecās faktiskās izmaksas un atkārtoti izveidojot jaunas faktiskās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="d70a1-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="d70a1-115">Lietojumprogramma apstrādās šīs faktiskās izmaksas, pamatojoties uz saistītās projekta līguma rindas norēķinu metodi.</span><span class="sxs-lookup"><span data-stu-id="d70a1-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="d70a1-116">Ja izmaksu faktiskās vērtības atsaucas uz laika un materiāla līguma rindu, atbilstošie rēķinā neiekļautie pārdošanas faktiskie dati tiek izveidoti laikam, kad piedāvājums ir slēgts un tiek izveidots projekta līgums.</span><span class="sxs-lookup"><span data-stu-id="d70a1-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="d70a1-117">Ja izdevumu faktiskie dati atsaucas uz fiksētas cenas līguma rindu, programma beigs no jauna pārstrādāt izmaksu faktiskās vērtības, kuras balstīt dalīto norēķinu kārtulās projekta līguma klientiem.</span><span class="sxs-lookup"><span data-stu-id="d70a1-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="d70a1-118">Zaudēta piedāvājuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="d70a1-118">Closing a quote as lost:</span></span>

<span data-ttu-id="d70a1-119">Slēdzot projekta piedāvājumu kā zaudētu, statuss tiek iestatīts uz Aizvērtu un statusa iemesls ir Zaudēts.</span><span class="sxs-lookup"><span data-stu-id="d70a1-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="d70a1-120">Slēdzot piedāvājumu, projekta piedāvājums kļūst tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="d70a1-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="d70a1-121">Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms piedāvājuma slēgšanas tiks parādīts apstiprinājuma dialogs, lai apstiprinātu veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="d70a1-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="d70a1-122">Ja projekta piedāvājums, kas ir aizvērts kā Zaudēts attiecas uz projektu jebkurā no tā rindām, šo projektu arī atzīmē kā Slēgtu.</span><span class="sxs-lookup"><span data-stu-id="d70a1-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="d70a1-123">Visas resursu rezervācijas no šīs dienas uz priekšu tiek atceltas.</span><span class="sxs-lookup"><span data-stu-id="d70a1-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="d70a1-124">Programmā Project Operations slēdzot piedāvājumu kā iegūtu vai zaudētu, netiks ietekmēts iespējas statuss — tā paliks atvērta, līdz tiks manuāli slēgta.</span><span class="sxs-lookup"><span data-stu-id="d70a1-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
