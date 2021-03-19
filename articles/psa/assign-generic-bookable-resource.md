---
title: Vispārējo rezervējamo resursu piešķiršana uzdevumam un projekta darba grupai
description: Šajā tēmā ir sniegta informācija par vispārējo resursu rezervēšanu uzdevumiem un projektu darba grupām.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 5b4c47513b96310745fd2cdb296988a57df0e966
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291403"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="79601-103">Vispārējo rezervējamo resursu piešķiršana uzdevumam un resursu vajadzību ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="79601-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="79601-104">Papildus nosaukto vai reālo resursu rezervēšanas un piešķiršanas projektam, projekta uzdevumiem varat piešķirt vispārējos resursus.</span><span class="sxs-lookup"><span data-stu-id="79601-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="79601-105">Šos resursus var izmantot kā vietturus nosauktajiem resursiem, līdz esat gatavs projektam piešķirt darbiniekus, izmantojot norādītos resursus.</span><span class="sxs-lookup"><span data-stu-id="79601-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="79601-106">Programmā Project Service Automation (PSA) atveriet lapu **Projekts** un cilnē **Grafiks** ievadiet vispārējā resursa amata nosaukumu grafika šūnā **Resurss**.</span><span class="sxs-lookup"><span data-stu-id="79601-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="79601-107">Vai arī noklikšķiniet uz ikonas **Resurss**, lai atvērtu resursu atlasītāju, un pēc tam ievadiet tā vispārējā resursa nosaukumu, ko vēlaties izveidot.</span><span class="sxs-lookup"><span data-stu-id="79601-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Vispārējā darba grupas dalībnieka izveide un piešķiršana](media/RM-how-to-9.png)

<span data-ttu-id="79601-109">Šādi tiks atvērts panelis **Ātrā izveide: projekta darba grupas dalībnieks**.</span><span class="sxs-lookup"><span data-stu-id="79601-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="79601-110">Ievadiet vispārējā resursu darba grupas dalībnieka lomu un organizācijas struktūrvienību un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="79601-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Vispārējā darba grupas dalībnieka ātrā izveide](media/RM-how-to-10.png)

3. <span data-ttu-id="79601-112">Pēc jaunā vispārējā resursu darba grupas dalībnieka izveidošanas tas tiek piešķirts uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="79601-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="79601-113">Šo vispārējo resursu varat turpināt piešķirt citiem uzdevumu grafikā esošajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="79601-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Esošu vispārējo darba grupas dalībnieku piešķiršana uzdevumiem](media/RM-how-to-11.png)

4. <span data-ttu-id="79601-115">Pēc tam, kad ir piešķirts vispārējais resurss, varat ģenerēt resursu vajadzību un to izpildīt, tieši rezervējot vai iesniedzot resursa pieprasījumu resursu pārvaldniekā.</span><span class="sxs-lookup"><span data-stu-id="79601-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Vajadzības ģenerēšana vispārējam darba grupas dalībniekam](media/RM-how-to-12.png)

<span data-ttu-id="79601-117">Darba grupas dalībnieku režģī varat ne tikai izmantot resursu atlasītāju, kā minēts iepriekš, bet varat arī tiešā veidā pievienot vispārējos resursus.</span><span class="sxs-lookup"><span data-stu-id="79601-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="79601-118">Resursi tiek pievienoti, izmantojot resursu vajadzību, kuras pamatā ir sākuma/beigu datumi un piešķiršanas metode, kas norādīta panelī **Ātrā izveide: projekta darba grupas dalībnieks.**</span><span class="sxs-lookup"><span data-stu-id="79601-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="79601-119">Pastāv atšķirība, ja vispārējo darba grupas dalībnieku pievienojat tieši un pēc tam vispārējam resursam piešķirat vairāk uzdevumu, nekā tam ir pieejamas izpildei nepieciešamās stundas.</span><span class="sxs-lookup"><span data-stu-id="79601-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="79601-120">Noklikšķiniet uz **Ģenerēt vajadzību**, lai atkārtoti ģenerētu vajadzību un līdzsvarotu nepieciešamās stundas ar piešķirēm.</span><span class="sxs-lookup"><span data-stu-id="79601-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="79601-121">Varat arī noklikšķināt uz saites **Resursu vajadzība** darba grupas režģī, lai atvērtu vajadzības un pievienotu prasmes, vēlamos resursus utt.</span><span class="sxs-lookup"><span data-stu-id="79601-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Resursu prasība](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]