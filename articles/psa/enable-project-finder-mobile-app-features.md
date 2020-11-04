---
title: Programmas Project Finder Mobile funkciju iespējošana
description: Programmas Project Finder Mobile funkciju iespējošana programmā Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080451"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="1c609-103">Programmas Project Finder Mobile funkciju iespējošana (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1c609-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1c609-104">Jūsu resursi var izmantot programmu Project Finder Mobile savā telefonā ar [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], lai atrastu jaunus darba projektus un atjauninātu savas prasmes.</span><span class="sxs-lookup"><span data-stu-id="1c609-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="1c609-105">Programma ir pieejama [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] un [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] tālruņiem.</span><span class="sxs-lookup"><span data-stu-id="1c609-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="1c609-106">Jums jāiestata pāris opciju parametru iestatījumā jūsu organizācijas vienībai, lai ļautu lietotājiem skatīt projekta resursu prasības un atjauninātu to prasmes.</span><span class="sxs-lookup"><span data-stu-id="1c609-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1c609-107">Project Finder Mobile programma darbojas tikai ar [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (ne ar lokālām instalācijām).</span><span class="sxs-lookup"><span data-stu-id="1c609-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="1c609-108">Pārejiet uz sadaļu **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="1c609-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="1c609-109">Klikšķiniet uz parametru iestatījumu, ko vēlaties izmantot Project Finder Mobile programmas funkciju atļaušanai.</span><span class="sxs-lookup"><span data-stu-id="1c609-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="1c609-110">Apgabalā **Vispārīgi** iestatiet **Resursu prasības redzamas resursiem** kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="1c609-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="1c609-111">Iestatiet **Atļaut resursam prasmju atjaunināšanu** kā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="1c609-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="1c609-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="1c609-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="1c609-113">Šis ir globāls iestatījums.</span><span class="sxs-lookup"><span data-stu-id="1c609-113">This is a global setting.</span></span> <span data-ttu-id="1c609-114">Projektu vadītāji var iestatīt, vai atsevišķs projektu būs redzamas tā projekta lapā **Projekta darba grupa**.</span><span class="sxs-lookup"><span data-stu-id="1c609-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="1c609-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="1c609-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="1c609-116">E-pasta paziņojumi</span><span class="sxs-lookup"><span data-stu-id="1c609-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="1c609-117">sūta e-pasta vēstules attiecībā uz resursu pieprasījumiem šādiem adresātiem šādos laikos.</span><span class="sxs-lookup"><span data-stu-id="1c609-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="1c609-118">Adresāts</span><span class="sxs-lookup"><span data-stu-id="1c609-118">Recipient</span></span>|<span data-ttu-id="1c609-119">Pasākums</span><span class="sxs-lookup"><span data-stu-id="1c609-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="1c609-120">Projekta vadītājs</span><span class="sxs-lookup"><span data-stu-id="1c609-120">Project manager</span></span>|<span data-ttu-id="1c609-121">-   Kad resurss reģistrējas projektam, izmantojot programmu Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="1c609-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="1c609-122">Resurss</span><span class="sxs-lookup"><span data-stu-id="1c609-122">Resource</span></span>|<span data-ttu-id="1c609-123">-   Kad cits resurss jau ir izpildījis projekta darbu, kam ir reģistrējies resurss.</span><span class="sxs-lookup"><span data-stu-id="1c609-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="1c609-124">-   Kad tiek apstiprināts vai noraidīts resursa prasmju apstiprinājuma pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="1c609-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="1c609-125">-   Kad tiek apstiprināts vai noraidīts resursa reģistrēšanās projektam pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="1c609-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="1c609-126">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="1c609-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="1c609-127">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="1c609-127">See Also</span></span>  
 [<span data-ttu-id="1c609-128">Resursu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1c609-128">Set up resources</span></span>](../psa/set-up-resources.md)
