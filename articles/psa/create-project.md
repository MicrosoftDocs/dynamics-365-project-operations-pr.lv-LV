---
title: Projekta izveidošana
description: Projekta izveide programmā Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: de26bb4c3fa0ee8abf6edf5494968d1d0403266a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133107"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="0370d-103">Projekta izveide (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0370d-103">Create a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0370d-104">Izveidojiet projektu, izmantojot [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] iespējas pakalpojumā [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], ja vēlaties izveidot ar projektu saistītu pakalpojumu iespēju, piedāvājumu vai līgumu.</span><span class="sxs-lookup"><span data-stu-id="0370d-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="0370d-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] iespējas palīdz jums pārvaldīt projektu no iespējas līdz tā pabeigšanai.</span><span class="sxs-lookup"><span data-stu-id="0370d-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="0370d-106">Izveidojot projektu, tiek izveidota arī darba sadalījuma struktūras, kas ietekmē piedāvājumus, izmaksu aprēķinus un resursu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="0370d-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="0370d-107">Dodieties uz **Project Service > Projekti**.</span><span class="sxs-lookup"><span data-stu-id="0370d-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="0370d-108">Noklikšķiniet uz **Jauns projekts**.</span><span class="sxs-lookup"><span data-stu-id="0370d-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="0370d-109">Zonā **Kopsavilkums** ievadiet projekta nosaukumu un pēc tam iespējami vairāk detalizētu datu.</span><span class="sxs-lookup"><span data-stu-id="0370d-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="0370d-110">Ar sarkanu zvaigznīti (\*) atzīmētie vienumi ir obligāti.</span><span class="sxs-lookup"><span data-stu-id="0370d-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="0370d-111">Noklikšķiniet uz **Saglabāt**, lai izveidotu projektu un varētu turpināt tā rediģēšanu.</span><span class="sxs-lookup"><span data-stu-id="0370d-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="0370d-112">Pēc tam izveidojiet projekta darba sadalījuma struktūru, lai definētu projektam nepieciešamos uzdevumus, laika grafiku un resursu lomas.</span><span class="sxs-lookup"><span data-stu-id="0370d-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="0370d-113">Veicot plānošanu, platforma Project Service Automation ņem vērā lietotās **Darba stundu** veidnes laika joslu.</span><span class="sxs-lookup"><span data-stu-id="0370d-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="0370d-114">Taču, skatot ieplānotos uzdevumus, uzdevuma sākuma un beigu datumi tiks parādīti lietotāja laika joslā.</span><span class="sxs-lookup"><span data-stu-id="0370d-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="0370d-115">Tas attiecas uz citiem laika sadalījuma skatiem veidlapā **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="0370d-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="0370d-116">Ja lietotāja laika josla neatbilst projektā izmantotajai darba stundu veidnes laika joslai, tiek parādīts brīdinājums, kurā paskaidrota šī atšķirība.</span><span class="sxs-lookup"><span data-stu-id="0370d-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="0370d-117">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="0370d-117">See Also</span></span>  
 [<span data-ttu-id="0370d-118">Projekta vadītāja rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="0370d-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
