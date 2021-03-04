---
title: Resursu lomu konfigurēšana
description: Resursu lomu konfigurēšana programmā Project Service
author: JohnPBurrows
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
ms.openlocfilehash: deaff0977ebb50382a28494fba2a1c34ed5cc9b4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144917"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="cb1d8-103">Resursu lomu konfigurēšana (Project Service)</span><span class="sxs-lookup"><span data-stu-id="cb1d8-103">Configure resource roles (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="cb1d8-104">Lomām ir svarīga nozīme projektu plānošanā, nosakot projekta resursu prasības vai izmaksas.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="cb1d8-105">Katrai lomai, kas nepieciešama projektiem, ir jāizveido resursa loma un jāpiesaista attiecīgajai lomai prasmes un kvalifikācijas.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="cb1d8-106">Piemēram, iespējams, vēlēsieties izveidot lomas izstrādātājam, projektu vadītājam vai spēļu testētājam.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="cb1d8-107">Jūs arī iestatīsiet attiecīgajai lomai nepieciešamo prasmju un kvalifikācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="cb1d8-108">Konfigurējiet resursu lomas, lai nodrošinātu organizācijai efektīvu projektu novērtēšanu.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="cb1d8-109">Arī pārliecinieties, ka ir precīzi iestatīts norēķinu tips.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="cb1d8-110">Vienums, kas iestatīts, izmantojot neapmaksājamu norēķinu veidu, neparādās līguma vai piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="cb1d8-111">Pēc resursu lomas iestatīšanas var iestatīt izmaksas un pārdošanas cenas ar cenrādi.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="cb1d8-112">Veiciet šādas darbības katrai lomai, kuru vēlaties pievienot:</span><span class="sxs-lookup"><span data-stu-id="cb1d8-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="cb1d8-113">Dodieties uz **Project Service > Resursu lomas**.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="cb1d8-114">Noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="cb1d8-115">Apgabalā **Vispārīgi** ievadiet lomas nosaukumu laukā **Nosaukums** un atbilstoši aizpildiet pārējos laukus.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="cb1d8-116">Noklikšķiniet uz **Saglabāt**, lai izveidotu ierakstu un pēc tam varētu veikt tā rediģēšanu.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="cb1d8-117">Lai pievienotu prasmi, apgabalā **Prasmes** noklikšķiniet uz **+**.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="cb1d8-118">Rūtī **Lomas kompetences prasība** noklikšķiniet uz lauka **Prasme**, noklikšķiniet uz pogas **Meklēt** un pēc tam atlasiet prasmi.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="cb1d8-119">Atlasiet kvalifikāciju attiecīgajai prasmei un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="cb1d8-120">Ja nepieciešams, turpiniet pievienot prasmes.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="cb1d8-121">Kad esat pabeidzis, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="cb1d8-122">Lai šī resursu loma būtu pieejama lietošanai projektiem, noklikšķiniet uz **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="cb1d8-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="cb1d8-123">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="cb1d8-123">See Also</span></span>  
 [<span data-ttu-id="cb1d8-124">Resursu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="cb1d8-124">Set up resources</span></span>](../psa/set-up-resources.md)
