---
title: Papildu parametru iestatījumu konfigurācija
description: Papildu parametru iestatījumu konfigurēšana programmā Project Service
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
ms.openlocfilehash: 5ce7ffd635b10689c8295d9349966450f11282d1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129372"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="48af3-103">Papildu parametru iestatījumu konfigurēšana (Project Service)</span><span class="sxs-lookup"><span data-stu-id="48af3-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="48af3-104">Kad esat konfigurējis vienumus iepriekšējās tēmās, jums jāiestata papildu projekta parametri, ko izmantot jūsu projektiem.</span><span class="sxs-lookup"><span data-stu-id="48af3-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="48af3-105">Kad pirmoreiz instalējāt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], jūs izveidojāt parametru iestatījumu, visu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] darbībai vajadzīgo ierakstu pirmajai izveidei.</span><span class="sxs-lookup"><span data-stu-id="48af3-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="48af3-106">Tagad ir pienācis laiks doties atpakaļ un konfigurēt papildu laukus šiem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="48af3-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="48af3-107">Jums jābūt konfigurētiem šādiem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="48af3-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="48af3-108">Organizācijas vienība</span><span class="sxs-lookup"><span data-stu-id="48af3-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="48af3-109">Rēķinu izrakstīšanas biežums</span><span class="sxs-lookup"><span data-stu-id="48af3-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="48af3-110">Darba stundu veidne</span><span class="sxs-lookup"><span data-stu-id="48af3-110">Work hours template</span></span>  
  
-   <span data-ttu-id="48af3-111">Cenrādis</span><span class="sxs-lookup"><span data-stu-id="48af3-111">Price list</span></span>  
 
<span data-ttu-id="48af3-112">Šajā solī jūs arī norādīsiet, kādu resursu piešķiršanas tipu vēlaties:</span><span class="sxs-lookup"><span data-stu-id="48af3-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="48af3-113">**Centrāls**.</span><span class="sxs-lookup"><span data-stu-id="48af3-113">**Central**.</span></span> <span data-ttu-id="48af3-114">Resursus projektiem var piešķirt tikai resursu pārvaldītāji.</span><span class="sxs-lookup"><span data-stu-id="48af3-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="48af3-115">**Hibrīds**.</span><span class="sxs-lookup"><span data-stu-id="48af3-115">**Hybrid**.</span></span> <span data-ttu-id="48af3-116">Resursu pārvaldītāji, projekta vadītāji un uzņēmumu vadītāji var piešķirt resursus projektiem.</span><span class="sxs-lookup"><span data-stu-id="48af3-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="48af3-117">Lai iestatītu projekta parametrus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="48af3-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="48af3-118">Pārejiet uz sadaļu **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="48af3-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="48af3-119">Klikšķiniet uz parametru iestatījumu, kuru vēlaties konfigurēt (kuru izveidojāt, kad pirmoreiz instalējāt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), vai noklikšķiniet uz **Jauns**, lai izveidotu jaunu.</span><span class="sxs-lookup"><span data-stu-id="48af3-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="48af3-120">Apgabalā **Vispārīgi**, iestatiet visas opcijas jūsu projekta parametriem.</span><span class="sxs-lookup"><span data-stu-id="48af3-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="48af3-121">Apgabalā **Cenrādis** noklikšķiniet uz **+**, lai pievienotu cenrādi, izvelieties cenrādi nolaižamajā sarakstā **Projekta parametru cenrādis** un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="48af3-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="48af3-122">Ekrāna apakšējā labajā stūrī noklikšķiniet uz pogas **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="48af3-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="48af3-123">Projekta parametra ierakstam ir jābūt uzturētam Project Service, lai tas darbotos pareizi.</span><span class="sxs-lookup"><span data-stu-id="48af3-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="48af3-124">Šo ierakstu nedrīkst dzēst.</span><span class="sxs-lookup"><span data-stu-id="48af3-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="48af3-125">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="48af3-125">See Also</span></span>  
 [<span data-ttu-id="48af3-126">Resursu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="48af3-126">Set up resources</span></span>](../psa/set-up-resources.md)
