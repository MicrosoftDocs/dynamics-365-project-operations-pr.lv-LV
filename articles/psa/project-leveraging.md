---
title: Pārdošanas tāmes un projekti
description: Šajā tēmā ir sniegta informācija par to, kā pārdošanas procesā izdevīgi izmantot plānošanu un tāmes.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: eafe60362003198a223026526f56261de414bb4a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080462"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="f5c02-103">Pārdošanas tāmes un projekti</span><span class="sxs-lookup"><span data-stu-id="f5c02-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f5c02-104">Pārdošanas procesa laikā varat izveidot pārdošanas tāmes, sasaistot projektu un pārdošanas piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="f5c02-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="f5c02-105">Šādi pārdošanas procesa laikā var rasties deterministisks novērtējums, lai izmantotu projekta plānošanas un tāmes noteikšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="f5c02-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="f5c02-106">Ja pārdošanas darījums ir sekmīgs, pārdošanas tāmes vajadzībām izmantoto grafiku var izmantot kā pamatu turpmākai projekta plāna pilnveidošanai.</span><span class="sxs-lookup"><span data-stu-id="f5c02-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="f5c02-107">Projekta saistīšana ar piedāvājuma rindu</span><span class="sxs-lookup"><span data-stu-id="f5c02-107">Linking a project to a quote line</span></span>

<span data-ttu-id="f5c02-108">Kad izveidojat uz projektu balstītu piedāvājuma rindu, varat izveidot jaunu projektu vai saistīt jau esošu projektu lapā **Piedāvājuma rinda**.</span><span class="sxs-lookup"><span data-stu-id="f5c02-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Piedāvājuma rindas veidlapa](media/project-8.png)
 
<span data-ttu-id="f5c02-110">Kad no piedāvājuma rindas informācijas veidojat jaunu projektu, varat izdevīgi izmantot projektu veidnes.</span><span class="sxs-lookup"><span data-stu-id="f5c02-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="f5c02-111">Projektu veidnes ir modeļa projekti, kas pārstāv standarta projektu plānus un finanšu tāmes, kādas organizācijai ir tipiskas.</span><span class="sxs-lookup"><span data-stu-id="f5c02-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="f5c02-112">Tās var pārstāvēt arī projektu plānu kopijas un tāmes no iepriekšējiem projektiem.</span><span class="sxs-lookup"><span data-stu-id="f5c02-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Piedāvājuma rindas detaļas](media/project-9.png)
  
<span data-ttu-id="f5c02-114">Kad projektu veidojat no piedāvājuma, šis projekts automātiski tiek saistīts ar piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="f5c02-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="f5c02-115">Tāmju komponenti projektā</span><span class="sxs-lookup"><span data-stu-id="f5c02-115">Components of estimates in a project</span></span>

<span data-ttu-id="f5c02-116">Grafiks ļauj jums sadalīt darbu uzdevumos, uzturēt uzdevumu hierarhiju, noteikt, kādi resursi ir nepieciešami uzdevuma izpildīšanai, un piešķirt piepūles tāmi, kas ir nepieciešama uzdevuma izpildīšanai.</span><span class="sxs-lookup"><span data-stu-id="f5c02-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="f5c02-117">Darba piepūli un grafika tāmes varat definēt, izmantojot laukus lapas **Projekts** cilnē **Grafiks**.</span><span class="sxs-lookup"><span data-stu-id="f5c02-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="f5c02-118">Tā kā cenrādis ir saistīts ar projektu, finanšu tāmes tiek aprēķinātas, izmantojot cenrādī definētās izmaksas un pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="f5c02-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="f5c02-119">Tāmju importēšana no projekta uz piedāvājumu</span><span class="sxs-lookup"><span data-stu-id="f5c02-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="f5c02-120">Pēc projekta tāmju definēšanas varat tās importēt uz piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="f5c02-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="f5c02-121">Lapas **Piedāvājuma rindas informācija** lentē atlasiet vienumu **Importēt no tāmēm** , lai izveidotu projekta tāmju kopsavilkumu pēc transakcijas tipa, lomas vai uzdevuma līmeņa.</span><span class="sxs-lookup"><span data-stu-id="f5c02-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
