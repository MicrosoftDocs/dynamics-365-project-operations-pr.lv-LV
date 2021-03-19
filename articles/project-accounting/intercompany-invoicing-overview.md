---
title: Starpuzņēmumu rēķinu izrakstīšanas pārskats
description: Šajā tēmā ir sniegta informācija un piemēri par starpuzņēmumu rēķinu izrakstīšanu projektiem.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287337"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="ee215-103">Starpuzņēmumu rēķinu izrakstīšanas pārskats</span><span class="sxs-lookup"><span data-stu-id="ee215-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="ee215-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="ee215-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ee215-105">Jūsu organizācijā var būt vairākas nodaļas, meitasuzņēmumi un citas juridiskas personas, kas pārsūta produktus un pakalpojumus cita citai projektu ietvaros.</span><span class="sxs-lookup"><span data-stu-id="ee215-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="ee215-106">Juridiskā persona, kas nodrošina pakalpojumu vai produktu, tiek saukta par *aizdevuma juridisko personu*.</span><span class="sxs-lookup"><span data-stu-id="ee215-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="ee215-107">Juridiskā persona, kas saņem pakalpojumu vai produktu, tiek saukta par *aizņēmuma juridisko personu*.</span><span class="sxs-lookup"><span data-stu-id="ee215-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="ee215-108">Tālāk sniegtajā ilustrācijā ir parādīts tipisks scenārijs, kurā divas juridiskās personas, Contoso Robotics USA (aizņēmuma juridiskā persona) un Contoso Robotics UK (aizdevuma juridiskā persona) koplieto resursus, lai nodrošinātu projektu klientam Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="ee215-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="ee215-109">Šajā scenārijā uzņēmums Contoso Robotics USA ir noslēdzis līgumu, lai izpildītu klientam Adventure Works piegādājamo darbu.</span><span class="sxs-lookup"><span data-stu-id="ee215-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Starpuzņēmumu rēķinu izrakstīšana](./media/IntercompanyScenario.png) 

<span data-ttu-id="ee215-111">Programmā Dynamics 365 Project Operations tiek izmantota tālāk aprakstītā starpuzņēmumu darbību apstrādes plūsma.</span><span class="sxs-lookup"><span data-stu-id="ee215-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="ee215-112">Resursi no aizņēmuma juridiskās personas reģistrē starpuzņēmumu laika vai izdevumu darbības, grāmatojot laiku un izdevumus aizņēmuma juridiskās personas projektos.</span><span class="sxs-lookup"><span data-stu-id="ee215-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="ee215-113">Laika un izdevumu izmaksas aizdevuma uzņēmumā tiek reģistrētas, izmantojot aizņēmuma uzņēmuma vienības izmaksu cenrādi.</span><span class="sxs-lookup"><span data-stu-id="ee215-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="ee215-114">Starpuzņēmumu rēķinā neiekļautās pārdošanas darbības aizdevuma uzņēmumā tiek reģistrētas, izmantojot aizņēmuma uzņēmuma vienības izmaksu cenrādi.</span><span class="sxs-lookup"><span data-stu-id="ee215-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="ee215-115">Rēķinā neiekļautie ieņēmumi tiek reģistrēti aizņēmuma uzņēmumā, izmantojot projekta līguma pārdošanas cenrādi.</span><span class="sxs-lookup"><span data-stu-id="ee215-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="ee215-116">Klientam rēķinu var izrakstīt, kad ir reģistrēti rēķinā neiekļautie ieņēmumi.</span><span class="sxs-lookup"><span data-stu-id="ee215-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="ee215-117">Klientam nav jāgaida, kamēr tiek pabeigta starpuzņēmumu rēķinu apstrāde.</span><span class="sxs-lookup"><span data-stu-id="ee215-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="ee215-118">Starpuzņēmumu klientu rēķini tiek periodiski izveidoti aizdevuma uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="ee215-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="ee215-119">Rēķini tiek izveidoti manuāli vai izmantojot periodisku, automatizētu procesu.</span><span class="sxs-lookup"><span data-stu-id="ee215-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="ee215-120">Var izveidot vienu rēķinu katrai aizņēmuma juridiskajai personai vai arī var izveidot atsevišķus rēķinus projektiem.</span><span class="sxs-lookup"><span data-stu-id="ee215-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="ee215-121">Kad aizdevuma juridiskajā personā tiek grāmatots starpuzņēmumu klienta rēķins, aizņēmuma juridiskajā personā tiek izveidots atbilstošais gaidošais piegādātāja rēķins.</span><span class="sxs-lookup"><span data-stu-id="ee215-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="ee215-122">Izmaksas gaidošajā piegādātāja rēķinā tiks reģistrētas projekta apakšgrāmatā, kad būs iegrāmatots rēķins.</span><span class="sxs-lookup"><span data-stu-id="ee215-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="ee215-123">Tālāk sniegtajā diagrammā ir parādīta starpuzņēmumu rēķinu izrakstīšana saistībā ar uzskaites notikumiem un paredzētajiem grāmatojumiem virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="ee215-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Starpuzņēmumu plūsma](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="ee215-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ee215-125">Additional resources</span></span>

- [<span data-ttu-id="ee215-126">Starpuzņēmumu rēķinu izrakstīšanas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="ee215-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="ee215-127">Starpuzņēmumu darbību reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="ee215-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="ee215-128">Starpuzņēmumu klientu un piegādātāju rēķinu izveide</span><span class="sxs-lookup"><span data-stu-id="ee215-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]