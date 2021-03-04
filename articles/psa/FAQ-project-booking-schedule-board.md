---
title: Projekta rezervāciju izveide plānošanas panelī
description: Šajā tēmā ir sniegta informācija par to, kā plānošanas panelī izveidot projekta rezervāciju.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146537"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="871b2-103">Projekta rezervāciju izveide plānošanas panelī</span><span class="sxs-lookup"><span data-stu-id="871b2-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="871b2-104">Jūs varat rezervēt resursu projektam tieši projekta cilnē **Darba grupa** vai izveidojot resursu prasību no vispārēja darba grupas dalībnieka piešķires un pēc tam izpildot izveidoto prasību ar projekta darba grupas dalībnieku.</span><span class="sxs-lookup"><span data-stu-id="871b2-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="871b2-105">Varat arī rezervēt resursu projektam tieši plānošanas panelī.</span><span class="sxs-lookup"><span data-stu-id="871b2-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="871b2-106">To var izdarīt trīs tālāk minētajos veidos.</span><span class="sxs-lookup"><span data-stu-id="871b2-106">There are three ways to do this:</span></span>

- <span data-ttu-id="871b2-107">**Rezervēt no izveidotās resursa prasības:** pēc vispārēja resursa izveides var izveidot resursu pieprasījumu un piešķirt uzdevumus projektā.</span><span class="sxs-lookup"><span data-stu-id="871b2-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="871b2-108">**Rezervēt no primārajām prasībām:** primārās prasības tiek rādītas plānošanas paneļa cilnē **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="871b2-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="871b2-109">**Rezervēt no jaunas resursu prasības:** varat izveidot no fragmentiem resursu prasību un saistīt to ar projektu.</span><span class="sxs-lookup"><span data-stu-id="871b2-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="871b2-110">Plānošanas panelī resursa prasība tiek rādīta cilnē **Atvērtās prasības**.</span><span class="sxs-lookup"><span data-stu-id="871b2-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="871b2-111">Rezervēšana no izveidotas resursa prasības</span><span class="sxs-lookup"><span data-stu-id="871b2-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="871b2-112">Varat izveidot vispārēju resursu un piešķirt to vienam projekta uzdevumam vai vairākiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="871b2-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="871b2-113">Pēc tam varat izveidot resursa prasību no vispārējā darba grupas dalībnieka.</span><span class="sxs-lookup"><span data-stu-id="871b2-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="871b2-114">Plānošanas panelī šis resurss tiks rādīts cilnē **Atvērtās prasības**. Ja jums ir daudz atvērtu prasību, iespējams, būs jāizmanto režģa kolonnu filtri.</span><span class="sxs-lookup"><span data-stu-id="871b2-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="871b2-115">![Pieprasījuma cilnes atvēršana plānošanas panelim](media/FAQ-Project-Booking-Schedule-Board-1.png "Rezervāciju un uzdevumu tabulas ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="871b2-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="871b2-116">Atlasiet prasību.</span><span class="sxs-lookup"><span data-stu-id="871b2-116">Select the requirement.</span></span> <span data-ttu-id="871b2-117">Atlasītās rindas augšdaļā tiek parādīta cilne **Atrast pieejamību**.</span><span class="sxs-lookup"><span data-stu-id="871b2-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="871b2-118">Atlasot šo cilni, tiek aktivizēts plānošanas paneļa režīms Plānošanas palīgs un tiek filtrēti pieejamie resursi, kas atbilst resursa prasībai.</span><span class="sxs-lookup"><span data-stu-id="871b2-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="871b2-119">Pēc tam varat rezervēt resursu.</span><span class="sxs-lookup"><span data-stu-id="871b2-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="871b2-120">Varat arī vilkt un nomest atlasīto rindu no plānošanas paneļa apakšdaļas uz kāda resursa šūnu augstāk atrodamajā režģī.</span><span class="sxs-lookup"><span data-stu-id="871b2-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="871b2-121">Kad to nometat, labajā pusē tiek atvērts panelis **Resursa rezervācijas izveide**.</span><span class="sxs-lookup"><span data-stu-id="871b2-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="871b2-122">Atlasot **Rezervēt**, resurss tiek rezervēts projekta darba grupā.</span><span class="sxs-lookup"><span data-stu-id="871b2-122">Selecting **Book** books the resource onto the project team.</span></span>

![Resursa rezervāciju paneļa izveide](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="871b2-124">Rezervēšana no galvenās prasības</span><span class="sxs-lookup"><span data-stu-id="871b2-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="871b2-125">Izveidojot projektu programmā Project Service, tiek automātiski izveidota resursa prasība Galvenā prasība.</span><span class="sxs-lookup"><span data-stu-id="871b2-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="871b2-126">Tā ir tukša prasība, kas tiek izmantota, lai ātri rezervētu resursu plānošanas panelī, neizveidojot prasību vai neizveidojot prasību no fragmentiem.</span><span class="sxs-lookup"><span data-stu-id="871b2-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="871b2-127">Tā kā prasība ir tukša, ir nepieciešams norādīt datumus, kā arī piešķiršanas metodi un stundas, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="871b2-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="871b2-128">Lai rezervētu resursu ar galveno prasību, plānošanas panelī atlasiet cilni **Projekts**. Ja jums ir daudz projektu, iespējams, kolonnā **Projekts** būs jāizmanto filtrs.</span><span class="sxs-lookup"><span data-stu-id="871b2-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="871b2-129">![Kolonnu filtri plānošanas panelī](media/FAQ-Project-Booking-Schedule-Board-2.png "Rezervāciju un uzdevumu tabulas ekrānuzņēmums")</span><span class="sxs-lookup"><span data-stu-id="871b2-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="871b2-130">Atlasiet prasību, kuras nosaukumā ir tikai projekta nosaukums un kuras ilgums ir nulle (0).</span><span class="sxs-lookup"><span data-stu-id="871b2-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="871b2-131">Atlasiet cilni **Atrast pieejamību**, kas tiek parādīta rindā.</span><span class="sxs-lookup"><span data-stu-id="871b2-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="871b2-132">Šādi plānošanas panelī tiek aktivizēts režīms Plānošanas palīgs un tiek rādīti pieejamie resursi, kurus var rezervēt šim projektam.</span><span class="sxs-lookup"><span data-stu-id="871b2-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="871b2-133">Tā kā lauks **Primārā prasība** ir tukšs prasība ar nulles (0) ilgumu, atlasot un rezervējot resursu, panelī **Resursa rezervācijas izveide** ir jāiestata ilgums.</span><span class="sxs-lookup"><span data-stu-id="871b2-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="871b2-134">Varat arī atlasīt vienumu **Projekta primārā prasība** plānošanas paneļa apakšdaļā un vilkt un nomest to uz resursa, lai to rezervētu.</span><span class="sxs-lookup"><span data-stu-id="871b2-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="871b2-135">Tā kā **Primārā prasība** ir tukša prasība ar nulles (0) ilgumu, atlasot un rezervējot resursu, panelī **Resursa rezervācijas izveide** ir jāiestata ilgums.</span><span class="sxs-lookup"><span data-stu-id="871b2-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="871b2-136">Rezervējot resursu, izmantojot plānošanas paneļa lauku **Primārā prasība**, varat to pievienot projekta darba grupai bez piešķīrumiem.</span><span class="sxs-lookup"><span data-stu-id="871b2-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="871b2-137">Rezervēšana no jaunas resursa prasības</span><span class="sxs-lookup"><span data-stu-id="871b2-137">Book from a new resource requirement</span></span>
<span data-ttu-id="871b2-138">Izpildiet tālāk aprakstītās darbības, lai rezervētu no jauna resursa prasības.</span><span class="sxs-lookup"><span data-stu-id="871b2-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="871b2-139">Dodieties uz sadaļu **Resursu prasības** un atlasiet **Jauns**, lai izveidotu jaunu resursa prasību.</span><span class="sxs-lookup"><span data-stu-id="871b2-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="871b2-140">Cilnē **Projekts** atlasiet projektu, lai prasību saistītu ar šo projektu.</span><span class="sxs-lookup"><span data-stu-id="871b2-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="871b2-141">Šī jaunizveidotā prasība plānošanas panelī tiek parādīta kā **Atvērta prasība**, ko varat izpildīt.</span><span class="sxs-lookup"><span data-stu-id="871b2-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="871b2-142">Rezervējiet resursu, lai to pievienots projekta darba grupai.</span><span class="sxs-lookup"><span data-stu-id="871b2-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="871b2-143">Tagad, kad resurss ir rezervēts, ir manuāli jāpiešķir uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="871b2-143">Now that the resource is booked, you must assign tasks manually.</span></span>

