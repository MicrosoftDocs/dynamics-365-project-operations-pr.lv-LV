---
title: Darba stundu veidnes izveidošana
description: Darba stundu veidnes izveide programmā Project Service
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
ms.openlocfilehash: a0fce327587940e557e0214c8c0897116ac91901
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133062"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="d0c67-103">Darba stundu veidnes izveide (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d0c67-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d0c67-104">Lai varētu izveidot projekta grafikus, ir nepieciešams iestatīt projekta kalendāru, kas nosaka darba stundu skaitu, ko dienā izkārtot grafikā, ka arī visus uzņēmuma slēgšanas gadījumus.</span><span class="sxs-lookup"><span data-stu-id="d0c67-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="d0c67-105">Tas ir jāizdara ar darba stundu veidni, kurā ir iekļauta informācija par darba stundu skaitu dienā, brīvdienām un citiem uzņēmuma slēgšanas gadījumiem.</span><span class="sxs-lookup"><span data-stu-id="d0c67-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="d0c67-106">Kad veidojat projektu, darba veidni jūs saistāt ar projekta kalendāru, lai šim projektam lietotu šo grafiku.</span><span class="sxs-lookup"><span data-stu-id="d0c67-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="d0c67-107">Darba stundu veidni varat izveidot divējādi:</span><span class="sxs-lookup"><span data-stu-id="d0c67-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="d0c67-108">Izveidot darba stundu veidni, kuras pamatā ir resursu kalendārs.</span><span class="sxs-lookup"><span data-stu-id="d0c67-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="d0c67-109">Izveidot jaunu darba stundu veidni.</span><span class="sxs-lookup"><span data-stu-id="d0c67-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="d0c67-110">Lai izveidotu darba stundu veidni, kuras pamatā ir resursu kalendārs</span><span class="sxs-lookup"><span data-stu-id="d0c67-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="d0c67-111">Dodieties uz **Project Service > Resursi**.</span><span class="sxs-lookup"><span data-stu-id="d0c67-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="d0c67-112">Atlasiet resursu, uz kuru jūs vēlētos balstīt savas darba stundas.</span><span class="sxs-lookup"><span data-stu-id="d0c67-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="d0c67-113">Noklikšķiniet uz **Saglabāt kalendāru kā**, ievadiet darba stundu veidnes nosaukumu un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d0c67-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="d0c67-114">Kad opciju mainīšana ir pabeigta, noklikšķiniet uz **Saglabāt un aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="d0c67-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="d0c67-115">Ekrāna apakšējā labajā stūrī noklikšķiniet uz pogas **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d0c67-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="d0c67-116">Lai izveidotu jaunu darba stundu veidni</span><span class="sxs-lookup"><span data-stu-id="d0c67-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="d0c67-117">Dodieties uz **Project Service > Darba stundu veidnes**.</span><span class="sxs-lookup"><span data-stu-id="d0c67-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="d0c67-118">Noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d0c67-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="d0c67-119">Ievadiet darba stundu veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="d0c67-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="d0c67-120">Atlasiet resursu, kuru izmantot darba stundu pamatam, un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d0c67-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d0c67-121">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d0c67-121">See Also</span></span>  
 [<span data-ttu-id="d0c67-122">Resursu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d0c67-122">Set up resources</span></span>](../psa/set-up-resources.md)