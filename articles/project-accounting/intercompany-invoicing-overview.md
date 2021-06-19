---
title: Starpuzņēmumu rēķinu izrakstīšanas pārskats
description: Šajā tēmā ir sniegta informācija un piemēri par starpuzņēmumu rēķinu izrakstīšanu projektiem.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002650"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="68f31-103">Starpuzņēmumu rēķinu izrakstīšanas pārskats</span><span class="sxs-lookup"><span data-stu-id="68f31-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="68f31-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="68f31-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="68f31-105">Jūsu organizācijā var būt vairākas nodaļas, meitasuzņēmumi un citas juridiskas personas, kas pārsūta produktus un pakalpojumus cita citai projektu ietvaros.</span><span class="sxs-lookup"><span data-stu-id="68f31-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="68f31-106">Juridiskā persona, kas nodrošina pakalpojumu vai produktu, tiek saukta par *aizdevuma juridisko personu*.</span><span class="sxs-lookup"><span data-stu-id="68f31-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="68f31-107">Juridiskā persona, kas saņem pakalpojumu vai produktu, tiek saukta par *aizņēmuma juridisko personu*.</span><span class="sxs-lookup"><span data-stu-id="68f31-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="68f31-108">Nākamajā attēlā parādīts tipisks scenārijs, kad divas juridiskās personas, Contoso Robotics USA (aizņemošā juridiskā persona) un Contoso Robotics UK (aizdodošā juridiskā persona), koplieto resursus klienta Adventure Works projekta izpildei.</span><span class="sxs-lookup"><span data-stu-id="68f31-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="68f31-109">Šajā scenārijā Ir noslēgts līgums ar Contoso Robotics USA, lai izpildītu darbu Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="68f31-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Starpuzņēmumu rēķinu izrakstīšana](./media/IntercompanyScenario.png) 

<span data-ttu-id="68f31-111">Programmā Dynamics 365 Project Operations tiek izmantota tālāk aprakstītā starpuzņēmumu darbību apstrādes plūsma.</span><span class="sxs-lookup"><span data-stu-id="68f31-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="68f31-112">Resursi no aizņēmuma juridiskās personas reģistrē starpuzņēmumu laika vai izdevumu darbības, grāmatojot laiku un izdevumus aizņēmuma juridiskās personas projektos.</span><span class="sxs-lookup"><span data-stu-id="68f31-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="68f31-113">Laika un izdevumu izmaksas aizdevuma uzņēmumā tiek reģistrētas, izmantojot aizņēmuma uzņēmuma vienības izmaksu cenrādi.</span><span class="sxs-lookup"><span data-stu-id="68f31-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="68f31-114">Starpuzņēmumu rēķinā neiekļautās pārdošanas darbības aizdevuma uzņēmumā tiek reģistrētas, izmantojot aizņēmuma uzņēmuma vienības izmaksu cenrādi.</span><span class="sxs-lookup"><span data-stu-id="68f31-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="68f31-115">Rēķinā neiekļautie ieņēmumi tiek reģistrēti aizņēmuma uzņēmumā, izmantojot projekta līguma pārdošanas cenrādi.</span><span class="sxs-lookup"><span data-stu-id="68f31-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="68f31-116">Klientam rēķinu var izrakstīt, kad ir reģistrēti rēķinā neiekļautie ieņēmumi.</span><span class="sxs-lookup"><span data-stu-id="68f31-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="68f31-117">Klientam nav jāgaida, kamēr tiek pabeigta starpuzņēmumu rēķinu apstrāde.</span><span class="sxs-lookup"><span data-stu-id="68f31-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="68f31-118">Starpuzņēmumu klientu rēķini tiek periodiski izveidoti aizdevuma uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="68f31-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="68f31-119">Rēķini tiek izveidoti manuāli vai izmantojot periodisku, automatizētu procesu.</span><span class="sxs-lookup"><span data-stu-id="68f31-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="68f31-120">Var izveidot vienu rēķinu katrai aizņēmuma juridiskajai personai vai arī var izveidot atsevišķus rēķinus projektiem.</span><span class="sxs-lookup"><span data-stu-id="68f31-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="68f31-121">Kad aizdevuma juridiskajā personā tiek grāmatots starpuzņēmumu klienta rēķins, aizņēmuma juridiskajā personā tiek izveidots atbilstošais gaidošais piegādātāja rēķins.</span><span class="sxs-lookup"><span data-stu-id="68f31-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="68f31-122">Izmaksas gaidošajā piegādātāja rēķinā tiks reģistrētas projekta apakšgrāmatā, kad būs iegrāmatots rēķins.</span><span class="sxs-lookup"><span data-stu-id="68f31-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="68f31-123">Tālāk sniegtajā diagrammā ir parādīta starpuzņēmumu rēķinu izrakstīšana saistībā ar uzskaites notikumiem un paredzētajiem grāmatojumiem virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="68f31-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Starpuzņēmumu plūsma](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="68f31-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="68f31-125">Additional resources</span></span>

- [<span data-ttu-id="68f31-126">Starpuzņēmumu rēķinu izrakstīšanas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="68f31-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="68f31-127">Starpuzņēmumu darbību reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="68f31-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="68f31-128">Starpuzņēmumu klientu un piegādātāju rēķinu izveide</span><span class="sxs-lookup"><span data-stu-id="68f31-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]