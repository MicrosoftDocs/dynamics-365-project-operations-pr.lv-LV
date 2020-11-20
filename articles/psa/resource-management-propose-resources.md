---
title: Projekta resursu piedāvāšana
description: Šajā tēmā ir sniegta informācija par projekta resursu piedāvāšanu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 1fcb8d1d40286cf5cbb23338f93b072ae5bed70d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120192"
---
# <a name="propose-project-resources"></a><span data-ttu-id="dff91-103">Projekta resursu piedāvāšana</span><span class="sxs-lookup"><span data-stu-id="dff91-103">Propose project resources</span></span>

<span data-ttu-id="dff91-104">Resursu vadītāji var piedāvāt resursu projektu vadītājam, izmantojot resursu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="dff91-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="dff91-105">Pieprasījumu režģī vai pašā pieprasījumā atlasiet opciju **Atrast resursus**.</span><span class="sxs-lookup"><span data-stu-id="dff91-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="dff91-106">Lapā **Plānošanas palīgs** atlasiet resursu un pēc tam rūtī **Izveidot resursu rezervāciju**, laukā **Rezervācijas statuss** atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="dff91-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Piedāvātais resurss atlasīts](media/Resource-Management-image62.png)

<span data-ttu-id="dff91-108">Tiek veikti šādi statusa atjauninājumi:</span><span class="sxs-lookup"><span data-stu-id="dff91-108">The following status updates occur:</span></span>

- <span data-ttu-id="dff91-109">Lapā **Plānošanas palīgs** statusa indikatori tiek atjaunināti, lai norādītu, ka rezervācija ir piedāvāta, nevis stingri rezervēta.</span><span class="sxs-lookup"><span data-stu-id="dff91-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Piedāvātās rezervācijas statusa indikatori lapā Plānošanas palīgs](media/Resource-Management-image63.png)

- <span data-ttu-id="dff91-111">Resursa pieprasījumā statuss tiek mainīts uz **Nepieciešama pārskatīšana**.</span><span class="sxs-lookup"><span data-stu-id="dff91-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Resursu pieprasījumā statuss mainīts uz Nepieciešama pārskatīšana](media/Resource-Management-image64.png)

- <span data-ttu-id="dff91-113">Projekta cilnē **Darba grupa** vērtība vispārējā darba grupas dalībnieka vienumam **Pieprasījuma statuss** ir mainīta uz **Nepieciešama pārskatīšana**.</span><span class="sxs-lookup"><span data-stu-id="dff91-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Vispārējā darba grupas dalībnieka pieprasījuma statusa vērtība mainīta uz Nepieciešama pārskatīšana cilnē Darba grupa](media/Resource-Management-image48.png)

<span data-ttu-id="dff91-115">Projekta vadītājs var pieņemt vai noraidīt piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="dff91-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="dff91-116">Kad resursu vadītāji apstrādā resursu pieprasījumus, viņi var izmantot jebkuru no tālāk minētajām metodēm.</span><span class="sxs-lookup"><span data-stu-id="dff91-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="dff91-117">Piedāvāt vairākus resursus, lai apmierinātu pieprasījumu, ja nepieciešamo stundu izpildei nav pieejams viens resurss.</span><span class="sxs-lookup"><span data-stu-id="dff91-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="dff91-118">Piedāvātās stundas tiek sadalītas starp vairākiem resursiem, kas var apmierināt nepieciešamo stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="dff91-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="dff91-119">Šādā gadījumā stundas nevar pārklāties.</span><span class="sxs-lookup"><span data-stu-id="dff91-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="dff91-120">Piedāvāt mazāk resursu, nekā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="dff91-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="dff91-121">Šādā gadījumā paredzētā resursa noslodze ir mazāka nekā prasītāja norādītais nepieciešamo stundu laiks.</span><span class="sxs-lookup"><span data-stu-id="dff91-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="dff91-122">Tāpēc, kad prasītājs pieņem piedāvātos resursus, tiek izveidota neizpildīta resursa vajadzība, lai norādītu atlikušo pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="dff91-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="dff91-123">Rezervēt vairākus resursus, lai apmierinātu pieprasījumu, ja darba izpildei nav pieejams viens resurss.</span><span class="sxs-lookup"><span data-stu-id="dff91-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="dff91-124">Rezervēt mazāk resursu, nekā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="dff91-124">Book fewer resources than are required.</span></span> <span data-ttu-id="dff91-125">Šādā gadījumā rezervēto stundu skaits ir mazāks par nepieciešamo stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="dff91-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="dff91-126">Sistēma palīdz piedāvāt resursus, nevis rezervācijas, lai pieprasītājs varētu pārbaudīt un sekot līdzi atlikušajām vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="dff91-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="dff91-127">Apmaksājamā izmantošana</span><span class="sxs-lookup"><span data-stu-id="dff91-127">Billable utilization</span></span>

<span data-ttu-id="dff91-128">Resursiem var būt mērķa apmaksājamā izmantošana.</span><span class="sxs-lookup"><span data-stu-id="dff91-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="dff91-129">Šī mērķa izmantošana tiek definēta kā atribūts resursa noklusējuma lomā vai iestatīta atsevišķa rezervācijas resursa ierakstā.</span><span class="sxs-lookup"><span data-stu-id="dff91-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="dff91-130">Izmantošanas aprēķini ir balstīti uz faktiskajām stundām, par kurām resursi ir paziņojuši, izmantojot apstiprinātos laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="dff91-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="dff91-131">Izmantošanas aprēķināšanai lieto šādas formulas:</span><span class="sxs-lookup"><span data-stu-id="dff91-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="dff91-132">Apmaksājamā izmantošana = Rēķinā iekļaujamās stundas ÷ Resursa noslodze</span><span class="sxs-lookup"><span data-stu-id="dff91-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="dff91-133">Neapmaksājamā izmantošana = Faktiskais laiks ar norēķinu tipa ID = Rēķinā neiekļaujams, Papildu vai Nav pieejams ÷ Resursa noslodze</span><span class="sxs-lookup"><span data-stu-id="dff91-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="dff91-134">Iekšējs = Faktiskais laiks bez pārdošanas līguma ÷ Resursa noslodze</span><span class="sxs-lookup"><span data-stu-id="dff91-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="dff91-135">Resursa noslodze = Resursa darba stundas – Ārpus biroja – Brīvdienas</span><span class="sxs-lookup"><span data-stu-id="dff91-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="dff91-136">Skatu **Resursa izmantojums** var atrast rūtī **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="dff91-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Skats Resursa izmantojums](media/Resource-Management-image65.png)

<span data-ttu-id="dff91-138">Katra režģa šūna norāda resursa apmaksājamās izmantošanas procentuālo vērtību periodā, piemēram, dienā, nedēļā vai mēnesī.</span><span class="sxs-lookup"><span data-stu-id="dff91-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="dff91-139">Šūnu iekrāsošanai lieto šādas formulas:</span><span class="sxs-lookup"><span data-stu-id="dff91-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="dff91-140">**Zaļa:** Apmaksājamā izmantošana \>= Resursa mērķa lietojums</span><span class="sxs-lookup"><span data-stu-id="dff91-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="dff91-141">**Dzeltena:** Mērķa lietojums – 20 \<= Apmaksājamā izmantošana \< Mērķa lietojums</span><span class="sxs-lookup"><span data-stu-id="dff91-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="dff91-142">**Sarkana:** Apmaksājamā izmantošana \< Mērķa lietojums – 20</span><span class="sxs-lookup"><span data-stu-id="dff91-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="dff91-143">Tā kā skats **Apmaksājamā izmantošana** ir atkarīgs no plānošanas paneļa, varat izmantot plānošanas paneļa filtrēšanas iespējas, lai filtrētu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="dff91-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="dff91-144">Režģim ir jāiestata mērķa lietojums lomai vai atsevišķam resursam.</span><span class="sxs-lookup"><span data-stu-id="dff91-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="dff91-145">Lai veiktu šo iestatīšanu, atveriet **Resursi** \> **Resursu lomas**.</span><span class="sxs-lookup"><span data-stu-id="dff91-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="dff91-146">Turklāt katram rezervējamajam resursam ir jāpiešķir noklusējuma loma.</span><span class="sxs-lookup"><span data-stu-id="dff91-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="dff91-147">Atveriet sadaļu **Resursi** \> **Resursi.**</span><span class="sxs-lookup"><span data-stu-id="dff91-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="dff91-148">Cilnē **Project Service** pārbaudiet, vai resursa loma ir definēta un vai laukā **Ir noklusējuma** ir iestatīta vērtība **Jā**.</span><span class="sxs-lookup"><span data-stu-id="dff91-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="dff91-149">Varat pievienot papildu lomas, kurām iestatīta opcija **Ir noklusējuma = Nē**.</span><span class="sxs-lookup"><span data-stu-id="dff91-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="dff91-150">Loma, kurai iestatīta opcija **Ir noklusējuma = Jā**, tiek izmantota, lai novērtētu resursa izmantojumu atbilstoši attiecīgās mērķim.</span><span class="sxs-lookup"><span data-stu-id="dff91-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Noklusējuma loma iestatīta](media/Resource-Management-image67.png)

<span data-ttu-id="dff91-152">Cilnē **Project Service** resursam var iestatīt arī atsevišķu mērķa lietojumu.</span><span class="sxs-lookup"><span data-stu-id="dff91-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="dff91-153">Šādā gadījumā lietojuma aprēķinā tiek izmantots mērķa lietojums, lai novērtētu resursa mērķi, nevis resursa noklusējuma lomas mērķi.</span><span class="sxs-lookup"><span data-stu-id="dff91-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="dff91-154">Resursa lietojums tiek rādīts tikai tad, ja šis resurss ir apstiprinājis rēķinā iekļaujamu laiku periodā, kas ir norādīts režģī.</span><span class="sxs-lookup"><span data-stu-id="dff91-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="dff91-155">Resursu pieejamība</span><span class="sxs-lookup"><span data-stu-id="dff91-155">Resource availability</span></span>

<span data-ttu-id="dff91-156">Ir ļoti svarīgi, lai resursu vadītāji varētu apskatīt resursu pieejamību un atjaunināt rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="dff91-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="dff91-157">Dažos gadījumos nav oficiāla pieprasījuma (resursa pieprasījuma), bet resursu vadītājam ir jāreaģē uz neplānotu pieprasījumu, kas rodas, izmantojot tādus kanālus kā e-pasts, tālruņa saruna vai tūlītējais ziņojums.</span><span class="sxs-lookup"><span data-stu-id="dff91-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="dff91-158">Resursu vadītāji izmanto plānošanas paneli, lai atjauninātu resursus un rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="dff91-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="dff91-159">Resursa darba stundas tiek izmantotas par pamatu resursa pieejamības aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="dff91-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="dff91-160">Resursu rezervēšana patērē resursu noslodzi.</span><span class="sxs-lookup"><span data-stu-id="dff91-160">Resource bookings consume the capacity of the resources.</span></span>

![Plānošanas panelis](media/Resource-Management-image68.png)

<span data-ttu-id="dff91-162">Plānošanas panelī tiek izmantotas krāsas un ēnojums, lai norādītu rezervācijas, pieejamību un rezervēšanas pārsniegšanu, kā arī rezervāciju statusu.</span><span class="sxs-lookup"><span data-stu-id="dff91-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="dff91-163">Iestatījums plānošanas paneļa iestatījumos ļauj rādīt apzīmējumus.</span><span class="sxs-lookup"><span data-stu-id="dff91-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="dff91-164">Ja blakus atsevišķiem rezervējamiem resursiem plānošanas panelī tiek parādīta pa labi vērsta bultiņa, resursu var izvērst, lai skatītu detalizētu informāciju par darbu, kuram attiecīgais resurss ir rezervēts.</span><span class="sxs-lookup"><span data-stu-id="dff91-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Rezervējamais resurss izvērsts plānošanas panelī](media/Resource-Management-image69.png)

<span data-ttu-id="dff91-166">Tā kā Dynamics 365 Project Service Automation izmanto programmu Universal Resource Scheduling, ja ir instalēts arī risinājums Dynamics 365 Field Service, varat skatīt detalizētu informāciju par resursu rezervācijām projektiem, darba pasūtījumiem un citām entītijām, uz kurām esat paplašinājis plānošanu.</span><span class="sxs-lookup"><span data-stu-id="dff91-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Detalizēta informācija par resursu rezervēšanu projektiem un darba pasūtījumiem](media/Resource-Management-image70.png)

<span data-ttu-id="dff91-168">Lai skatītu papildinformāciju par atsevišķu resursu, ar peles labo pogu noklikšķiniet uz tā, lai atvērtu resursa karti.</span><span class="sxs-lookup"><span data-stu-id="dff91-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Resursa karte](media/Resource-Management-image71.png)
