---
title: Piedāvājuma aizvēršana — Lite
description: Šajā tēmā ir sniegta informācija par piedāvājuma slēgšanu programmā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175720"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="85ebb-103">Piedāvājuma aizvēršana — Lite</span><span class="sxs-lookup"><span data-stu-id="85ebb-103">Close a quote - lite</span></span>

<span data-ttu-id="85ebb-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="85ebb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="85ebb-105">Projekta piedāvājumu var slēgt kā iegūtu vai zaudētu.</span><span class="sxs-lookup"><span data-stu-id="85ebb-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="85ebb-106">Programmā Microsoft Dynamics 365 Project Operations netiek atbalstītas piedāvājumu aktivizēšanas un pārskatīšanas operācijas, tāpēc var slēgt piedāvājuma melnrakstu.</span><span class="sxs-lookup"><span data-stu-id="85ebb-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="85ebb-107">Iegūta piedāvājuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="85ebb-107">Close a quote as Won</span></span>

<span data-ttu-id="85ebb-108">Slēdzot projekta piedāvājumu kā iegūtu, piedāvājums tiks slēgts ar statusu Slēgts un statusa iemeslu Iegūts.</span><span class="sxs-lookup"><span data-stu-id="85ebb-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="85ebb-109">Slēdzot piedāvājumu, projekta piedāvājums kļūst tikai lasāms, un tiek izveidots projekta līguma melnraksts, kurā ir ietverta piedāvājuma informācija.</span><span class="sxs-lookup"><span data-stu-id="85ebb-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="85ebb-110">Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms izmaiņu veikšanas tiek parādīts apstiprinājuma dialogs, jo slēgtu piedāvājumu vairs nevar atvērt un izmaiņas ir neatgriezeniskas.</span><span class="sxs-lookup"><span data-stu-id="85ebb-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="85ebb-111">Ja piedāvājums ir pievienots iespējai, visi pārējie iespējas projekta piedāvājumi tiek automātiski slēgti kā zaudēti.</span><span class="sxs-lookup"><span data-stu-id="85ebb-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="85ebb-112">Finansiālā ietekme, piedāvājumu slēdzot kā iegūtu</span><span class="sxs-lookup"><span data-stu-id="85ebb-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="85ebb-113">Ja projektā ir reģistrēti faktiskie laika dati, kamēr tas joprojām ir pievienots piedāvājuma melnrakstam, tiek reģistrētas tikai laika izmaksas vai izdevumi.</span><span class="sxs-lookup"><span data-stu-id="85ebb-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="85ebb-114">Kad piedāvājums būs slēgts kā iegūts, lietojumprogramma pārstrukturizēs izmaksas, atsaucot vecās faktiskās izmaksas un atkārtoti izveidojot jaunas faktiskās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="85ebb-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="85ebb-115">Lietojumprogramma apstrādās šīs faktiskās izmaksas, pamatojoties uz saistītās projekta līguma rindas norēķinu metodi.</span><span class="sxs-lookup"><span data-stu-id="85ebb-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="85ebb-116">Ja faktiskajās izmaksās ir atsauce uz laika un materiālu līguma rindu, sistēma automātiski izveidos atbilstošos rēķinā neiekļautos pārdošanas faktiskos datus, kad tiks slēgts piedāvājums un tiks izveidots projekta līgums.</span><span class="sxs-lookup"><span data-stu-id="85ebb-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="85ebb-117">Ja faktiskajās izmaksās ir atsauce uz fiksētas cenas līguma rindu, lietojumprogramma pārtrauks faktisko izmaksu atkārtotu apstrādi, pamatojoties uz projekta līguma klientu sadalīšanas norēķinu kārtulām.</span><span class="sxs-lookup"><span data-stu-id="85ebb-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="85ebb-118">Zaudēta piedāvājuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="85ebb-118">Closing a quote as lost:</span></span>

<span data-ttu-id="85ebb-119">Slēdzot projekta piedāvājumu kā zaudētu, piedāvājums tiks slēgts ar statusu Slēgts un statusa iemeslu Zaudēts.</span><span class="sxs-lookup"><span data-stu-id="85ebb-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="85ebb-120">Slēdzot piedāvājumu, projekta piedāvājums kļūst tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="85ebb-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="85ebb-121">Tā kā slēgtu piedāvājumu nevar atkārtoti atvērt, pirms piedāvājuma slēgšanas tiks parādīts apstiprinājuma dialogs, lai apstiprinātu veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="85ebb-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="85ebb-122">Ja projekta piedāvājuma, kas ir slēgts kā zaudēts, jebkurā rindā ir atsauce uz kādu projektu, arī šis projekts tiek atzīmēts arī kā slēgts, kā arī tiek atceltas visas turpmākās resursu rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="85ebb-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="85ebb-123">Programmā Project Operations slēdzot piedāvājumu kā iegūtu vai zaudētu, netiks ietekmēts iespējas statuss — tā paliks atvērta, līdz tiks manuāli slēgta.</span><span class="sxs-lookup"><span data-stu-id="85ebb-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
