---
title: Projekta pārdošanas procesā veicamo darbu tāmes nodrošināšana
description: Projekta darba tāmju nodrošināšana pārdošanas procesa laikā programmā Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283557"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="48349-103">Projekta darba tāmju nodrošināšana pārdošanas procesa laikā (Project Service)</span><span class="sxs-lookup"><span data-stu-id="48349-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="48349-104">Pārdošanas procesa gaitā var sagatavot pārdošanas tāmi, izmantojot sākotnējā piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="48349-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="48349-105">iespējas pakalpojumā [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] piedāvā zinātniskāku un noteiktāku pārdošanas aplēšu aprēķināšanas metodi, sadalot darbu vienumus un saistot attiecīgos atribūtus, kas atvieglo projekta aplēšu aprēķināšanu darba sadalījuma struktūrā.</span><span class="sxs-lookup"><span data-stu-id="48349-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="48349-106">Kad pārdošanas projekts ir apstiprināts, projekta plānā var izmantot saistīto darba sadalījuma struktūru, ko, ja nepieciešams, var pārveidot, lai projekts tiktu sekmīgi pabeigts.</span><span class="sxs-lookup"><span data-stu-id="48349-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="48349-107">Projekta saistīšana ar piedāvājuma rindu</span><span class="sxs-lookup"><span data-stu-id="48349-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="48349-108">Ja tiek izveidota ar projektu saistīta piedāvājuma rinda, to izmantojot, var izveidot jaunu projektu.</span><span class="sxs-lookup"><span data-stu-id="48349-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="48349-109">Pēc tam var izmantot projekta veidnes, kas ir vai nu jūsu organizācijai raksturīgi iepriekš konfigurēti standarta projekta plāni un finanšu aplēses, vai iepriekšējā projekta plāna un aprēķinu kopija.</span><span class="sxs-lookup"><span data-stu-id="48349-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="48349-110">Izveidojot projektu, izvēlētā projekta veidne nodrošina bāzi, kas tiek izmantota projekta plāna, tāmes un ar lomām saistīto prasību precizēšanai.</span><span class="sxs-lookup"><span data-stu-id="48349-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="48349-111">Ja projekts tiek izveidots, izmantojot piedāvājumu, tas automātiski tiek saistīta ar piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="48349-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="48349-112">Projekta tāmes sastāvdaļas</span><span class="sxs-lookup"><span data-stu-id="48349-112">Project estimate components</span></span>  
 <span data-ttu-id="48349-113">Projekta darba sadalījuma struktūra nodrošina iespējas darba sadalīšanai uzdevumos, uzdevumu hierarhijas saglabāšanai un katra uzdevuma izpildei nepieciešamo resursu budžeta iedalīšanai.</span><span class="sxs-lookup"><span data-stu-id="48349-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="48349-114">Lomas var saistīt arī ar uzdevumu, tādējādi norādot uzdevuma un grafika izpildei nepieciešamā resursa tipa budžetu.</span><span class="sxs-lookup"><span data-stu-id="48349-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="48349-115">Darba sadalījuma struktūras izmantošana palīdz noteikt darba resursu un grafika budžetu.</span><span class="sxs-lookup"><span data-stu-id="48349-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="48349-116">Pēc noklusējuma projektā tiek izmantoti noklusējuma cenrāži, kas ir definēti iepriekš.</span><span class="sxs-lookup"><span data-stu-id="48349-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="48349-117">Cenrāžos noteikto izmaksu un pārdošanas cenas palīdz aprēķināt projekta darbu sadalījuma tāmes.</span><span class="sxs-lookup"><span data-stu-id="48349-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="48349-118">Ja projekts ir saistīts ar piedāvājumu un piedāvājumam pēc noklusējuma ir atšķirīgs cenrādis, piedāvājuma cenrādis tiek izmantots kā tāme.</span><span class="sxs-lookup"><span data-stu-id="48349-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="48349-119">Tāmes importēšana no projekta uz piedāvājumu</span><span class="sxs-lookup"><span data-stu-id="48349-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="48349-120">Kad projektam ir aprēķināta tāme, šo tāmi var importēt piedāvājuma rindā:</span><span class="sxs-lookup"><span data-stu-id="48349-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="48349-121">Sadaļā **Piedāvājuma rindas dati** noklikšķiniet uz **Importēt no tāmes**.</span><span class="sxs-lookup"><span data-stu-id="48349-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="48349-122">Atlasiet, vai importēt pēc transakcijas tipa, lomas vai darba sadalījuma struktūras mezgla līmeņa apkopotu projekta tāmi.</span><span class="sxs-lookup"><span data-stu-id="48349-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="48349-123">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="48349-123">See Also</span></span>  
 [<span data-ttu-id="48349-124">Projekta vadītāja rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="48349-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]