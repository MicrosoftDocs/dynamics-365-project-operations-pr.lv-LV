---
title: Projekta statusa izsekošana
description: Projekta statusa izsekošana programmā Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080530"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="688a2-103">Projekta statusa izsekošana (Project Service)</span><span class="sxs-lookup"><span data-stu-id="688a2-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="688a2-104">Izmantojiet [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)], lai izsekotu klienta projekta norisei.</span><span class="sxs-lookup"><span data-stu-id="688a2-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="688a2-105">Turpinoties sadarbībai, projekta posmi tiek atjaunināti, atspoguļojot sadarbības pakāpi:</span><span class="sxs-lookup"><span data-stu-id="688a2-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="688a2-106">**Jauns**</span><span class="sxs-lookup"><span data-stu-id="688a2-106">**New**</span></span>    | <span data-ttu-id="688a2-107">Kad veidojat projektu, posms tiek iestatīts uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="688a2-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="688a2-108">Ja projektu izveidojāt no veidnes, šajā posmā projektam var būt grafiks, tāmes un darba grupas dati.</span><span class="sxs-lookup"><span data-stu-id="688a2-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="688a2-109">Pretējā gadījumā tās būs projekta aprises, un pārējie projekta komponenti jums būs jāievada manuāli.</span><span class="sxs-lookup"><span data-stu-id="688a2-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="688a2-110">**Piedāvājums**</span><span class="sxs-lookup"><span data-stu-id="688a2-110">**Quote**</span></span>   |      <span data-ttu-id="688a2-111">Kad projektu saistāt ar piedāvājumu vai to izveidojat no piedāvājuma, projekta posms tiek iestatīts kā **Piedāvājums** un tiek atjaunināti arī prognozētie sākuma un beigu datumi.</span><span class="sxs-lookup"><span data-stu-id="688a2-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote** , and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="688a2-112">Kad projekts atrodas piedāvājuma posmā, detalizēta informācija par piedāvājumu tiek rādīta cilnē **Pārdošana** , lapā **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="688a2-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="688a2-113">**Plāns**</span><span class="sxs-lookup"><span data-stu-id="688a2-113">**Plan**</span></span>   |                                     <span data-ttu-id="688a2-114">Kad iegūstat ar kādu projektu saistītu piedāvājumu un kad sadarbība pāriet līguma posmā, projekta posms atjauninās uz **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="688a2-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="688a2-115">Detalizēta informācija par līgumu tiek rādīta cilnē **Pārdošana** , lapā **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="688a2-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="688a2-116">**Pabeigt**</span><span class="sxs-lookup"><span data-stu-id="688a2-116">**Complete**</span></span> |                    <span data-ttu-id="688a2-117">Kad projekta darbs ir pabeigts, posmu varat pārslēgt uz **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="688a2-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="688a2-118">Kad projekta posms ir iestatīts uz pabeigtu, tiek pieņemts, ka darbs ir 100% pabeigts, bet projekts tiek saglabāts atvērts uz jebkādu gaidīšanas laiku vai ar mērķi reģistrēt izdevumu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="688a2-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="688a2-119">**Aizvērt**</span><span class="sxs-lookup"><span data-stu-id="688a2-119">**Close**</span></span>   |           <span data-ttu-id="688a2-120">Kad visas transakcijas projektam ir reģistrētas un nav paredzēts, ka vēl kaut ko vajadzēs reģistrēt, varat posmu manuāli iestatīt uz **Slēgt**.</span><span class="sxs-lookup"><span data-stu-id="688a2-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="688a2-121">Kad projekts ir iestatīts uz **Slēgt** , šajā projektā vairs nevarat reģistrēt nekādas transakcijas un projekts kļūst tikai lasāms.</span><span class="sxs-lookup"><span data-stu-id="688a2-121">When the project is set to **Close** , you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="688a2-122">Lai izsekotu projekta statusu</span><span class="sxs-lookup"><span data-stu-id="688a2-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="688a2-123">Dodieties uz **Project Service > Projekti**.</span><span class="sxs-lookup"><span data-stu-id="688a2-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="688a2-124">Noklikšķiniet uz projekta, pie kura gribat strādāt.</span><span class="sxs-lookup"><span data-stu-id="688a2-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="688a2-125">Ekrāna augšdaļā esošajā joslā atlasiet lejupvērsto bultiņu pie projekta nosaukuma un pēc tam noklikšķiniet uz **Projekta izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="688a2-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="688a2-126">Nolaižamajā sarakstā virs uzdevumu saraksta atlasiet **Piepūles izsekošana** vai **Izmaksu izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="688a2-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="688a2-127">Veiciet dubultklikšķi uz jebkuru uzdevumu, lai to rediģētu.</span><span class="sxs-lookup"><span data-stu-id="688a2-127">Double-click any task to edit it.</span></span> <span data-ttu-id="688a2-128">Varat arī pārvietot joslas Ganta diagrammā vai mainīt to izmērus, lai mainītu uzdevuma laiku un progresu.</span><span class="sxs-lookup"><span data-stu-id="688a2-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="688a2-129">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="688a2-129">See Also</span></span>  
 [<span data-ttu-id="688a2-130">Projekta vadītāja rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="688a2-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
