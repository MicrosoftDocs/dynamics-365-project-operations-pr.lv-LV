---
title: Resursu plānošana projektam
description: Resursu plānošana projektam programmā Project Service
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080650"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="b72f9-103">Resursu plānošana projektam (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b72f9-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b72f9-104">Jūs varat pārbaudīt resursu pieejamību, lai iegūtu vispārēju priekšstatu par resursu rezervēšanas līmeni, vai arī varat veikt skata filtrēšanu pēc prasmēm, darba grupas, atrašanās vietas un citām opcijām.</span><span class="sxs-lookup"><span data-stu-id="b72f9-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="b72f9-105">Plānošanas panelis parāda sarakstu ar resursiem un to pieejamību.</span><span class="sxs-lookup"><span data-stu-id="b72f9-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="b72f9-106">Izvēlieties skata režīmu, lai parādītu pieejamību pēc vērtības **Stundas** , **Diena** , **Nedēļa** vai **Mēnesis**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="b72f9-107">Lai izmantotu plānošanas paneli, ir svarīgi to iestatīt.</span><span class="sxs-lookup"><span data-stu-id="b72f9-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="b72f9-108">Lai iegūtu papildinformāciju, skatiet [Plānošanas paneļa konfigurēšana (Field Service vai Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="b72f9-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="b72f9-109">Ja lietojat vecāku versiju, resursu pieejamību skatiet sadaļā [Resursu pieejamības skatīšana](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="b72f9-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="b72f9-110">Lai izmantotu plānošanas paneļa rezervēšana funkcionalitāti, ģeogrāfiskās atrašanās vietas un atrašanās vietas noteikšanas pakalpojumus, nepieciešams ieslēgt kartes.</span><span class="sxs-lookup"><span data-stu-id="b72f9-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="b72f9-111">Galvenajā izvēlnē atlasiet **Resursu plānošana** > **Administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="b72f9-112">Noklikšķiniet uz **Plānošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="b72f9-113">Atveriet ierakstu un ritiniet uz leju līdz sadaļai **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="b72f9-114">Laukā **Izveidot savienojumu ar kartēm** izvēlieties **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="b72f9-115">Piekrītiet noteikumiem un saglabājiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b72f9-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="b72f9-116">Galvenajā izvēlnē atlasiet **Project Service** > **Plānošanas panelis**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="b72f9-117">Šeit ir vairāki veidi, kā manuāli plānot rezervācijas prasības.</span><span class="sxs-lookup"><span data-stu-id="b72f9-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="b72f9-118">Izvēlieties jums piemēroto metodi.</span><span class="sxs-lookup"><span data-stu-id="b72f9-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="b72f9-119">Pieejamo resursu atrašana</span><span class="sxs-lookup"><span data-stu-id="b72f9-119">Find available resources</span></span>

1.  <span data-ttu-id="b72f9-120">Sarakstā **Rezervācijas prasības** ar peles labo pogu noklikšķiniet uz neplānotas rezervācijas un izvēlēties kādu no tālāk norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="b72f9-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="b72f9-121">Izvēlieties **Atrast pieejamību — pašreizējie resursi** , lai atrastu pieejamos resursus no plānošanas paneļa resursu saraksta.</span><span class="sxs-lookup"><span data-stu-id="b72f9-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="b72f9-122">Izvēlieties **Atrast pieejamību — visi resursi** , lai atrastu sistēmā pieejamos resursus.</span><span class="sxs-lookup"><span data-stu-id="b72f9-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="b72f9-123">Kad jūs to izdarāt, filtri parādīs izvēlēto rezervācijas prasību opcijas.</span><span class="sxs-lookup"><span data-stu-id="b72f9-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="b72f9-124">Kad redzat brīvo laika sprīdi, ar peles labo pogu noklikšķiniet uz laika sprīža plānošanas panelī un izvēlieties **Rezervēt šeit**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="b72f9-125">Vai velciet un nometiet rezervācijas prasību pieejamajā laika sprīdī.</span><span class="sxs-lookup"><span data-stu-id="b72f9-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="b72f9-126">Rezervējiet resursu, izmantojot ikdienas skatu, un uzziniet, kurš resurss ir maz rezervēts</span><span class="sxs-lookup"><span data-stu-id="b72f9-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="b72f9-127">Plānošanas panelī atlasiet **Skata režīms** un atlasiet **Dienas**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="b72f9-128">Tiks parādīts režģa skats ar dienā rezervēto stundu skaitu un to, kurās dienās nav rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="b72f9-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="b72f9-129">Noklikšķiniet uz rezervējamā resursa nosaukuma un pēc tam atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="b72f9-130">Dialoglodziņā **Resursa rezervēšana (izveide)** izvēlēties projektu, kuram vēlaties rezervēt resursu, rezervēšanas metodi un sākuma un beigu laiku.</span><span class="sxs-lookup"><span data-stu-id="b72f9-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="b72f9-131">Kad esat beidzis, atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="b72f9-132">Plānošanas paneļa skatīšana</span><span class="sxs-lookup"><span data-stu-id="b72f9-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="b72f9-133">Atlasiet neplānotu rezervācijas prasību apakšdaļā esošajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="b72f9-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="b72f9-134">Velciet rezervācijas prasību uz pieejamu resursu/laika sprīdi plānošanas panelī.</span><span class="sxs-lookup"><span data-stu-id="b72f9-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="b72f9-135">Kad esat beidzis, atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="b72f9-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="b72f9-136">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b72f9-136">Additional resources</span></span>  
 [<span data-ttu-id="b72f9-137">Resursu pārvaldnieka rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="b72f9-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
