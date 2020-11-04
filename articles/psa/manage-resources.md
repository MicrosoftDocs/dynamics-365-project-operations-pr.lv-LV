---
title: Resursu pārvaldīšana
description: Šajā tēmā ir sniegta informācija par to, kā varat pārvaldīt resursus.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080645"
---
# <a name="manage-resources"></a><span data-ttu-id="b6e6b-103">Resursu pārvaldīšana</span><span class="sxs-lookup"><span data-stu-id="b6e6b-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b6e6b-104">Dynamics 365 Project Service Automation ietver resursu pārvaldnieka informācijas paneli, kas nodrošina vizuālu pārskatu par resursu pieprasījumu un lietojumu visā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="b6e6b-105">Diagrammas šajā informācijas panelī var izmantot, lai vizualizētu tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="b6e6b-106">**Resursu pieprasījums**  — diagrammā **Aktīvais resursu pieprasījums** ir parādīti iesniegtie resursi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="b6e6b-107">Šie resursi ir apkopoti vai nu pēc lomas, vai pēc projekta.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="b6e6b-108">**Neiesniegts resursu pieprasījums**  — diagrammā **Nepiešķirts resursu pieprasījums** ir parādītas visas resursu vajadzības, kas nav iesniegtas.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="b6e6b-109">Tas palīdz resursu pārvaldniekiem apskatīt pieprasījumu, kas nav apstiprināts un ko varētu iesniegt, izmantojot resursa pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="b6e6b-110">**Apmaksājamā izmantošana iepriekšējai nedēļai**  —– diagrammā **Izmantošana pēc lomas** ir parādīts organizācijas faktiskās apmaksājamajās izmantošanas procentuālais daudzums pēc lomas salīdzinājumā ar tās mērķa izmantošanu pēc lomas.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6e6b-111">Lai diagrammu **Izmantošana pēc lomas** padarītu pieejamu, izveidojiet darbu, kurā tiek izpildīta darbplūsma UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="b6e6b-112">Šis periodiskais darbs tiek palaists ik pēc septiņām dienām, lai aprēķinātu apmaksājamo izmantošanu iepriekšējām septiņām dienām.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="b6e6b-113">Rezultāti tiek apkopoti pēc lomas.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="b6e6b-114">Projekta darba grupas dalībnieku pārvaldīšana</span><span class="sxs-lookup"><span data-stu-id="b6e6b-114">Manage project team members</span></span>

<span data-ttu-id="b6e6b-115">Projektu vadītāji var izmantot šo resursu pārvaldnieka informācijas paneli, lai projektos pārvaldītu resursus.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="b6e6b-116">Viņi var, piemēram, pievienot darba grupas dalībnieku tieši projektam un rezervēt darba grupas dalībnieku, lai izpildītu resursu vajadzības, kuras tvēra kāds vispārējais resurss.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="b6e6b-117">Darba grupas dalībnieka pievienošana tieši projektam</span><span class="sxs-lookup"><span data-stu-id="b6e6b-117">Add a team member directly to a project</span></span>

<span data-ttu-id="b6e6b-118">Lai kādu darba grupas dalībnieku pievienotu tieši projektam, lapā **Projekti** , cilnē **Darba grupa** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="b6e6b-119">Tiek parādīts dialoglodziņš **Ātrā izveide:Projekta darba grupas dalībnieks**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="b6e6b-120">Šajā dialoglodziņā varat veikt tālāk norādītos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="b6e6b-121">**Rezervēt nosauktu resursu**  — laukā **Rezervējamais resurss** atlasiet resursa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="b6e6b-122">Pēc tam atlasiet lomu, iestatiet periodu un atlasiet piešķiršanas metodi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="b6e6b-123">Jūsu atlasītais nosauktais resurss tiek pievienots projektam, izmantojot atlasīto sadalījuma metodi un resursu kalendāru.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="b6e6b-124">**Pievienot vispārēju resursu**  — lauku **Rezervējamais resurss** atstājiet tukšu un pēc tam atlasiet lomu, iestatiet periodu un atlasiet vēlamo piešķiršanas metodi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="b6e6b-125">Darba grupai tiek pievienots vispārējs resurss kā vietturis, lai uzturētu pieprasījuma modeli, kas tiek izmantots nosaukto resursu rezervēšanai darba grupā.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="b6e6b-126">Šī vajadzība tiek izpildīta atbilstoši projekta kalendāram.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="b6e6b-127">**Pievienot darba grupai nosauktu resursu, nepatērējot resursa noslodzi**  — laukā **Rezervējamais resurss** atlasiet kādu resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="b6e6b-128">Pēc tam atlasiet periodu un kā sadalījuma metodi atlasiet **Nav**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="b6e6b-129">Resurss tiek pievienots darba grupai, bet ar rezervēšanu šī resursa noslodze netiek patērēta.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="b6e6b-130">Darba grupas dalībnieka rezervēšana, lai izpildītu resursu vajadzības attiecībā uz vispārēju resursu</span><span class="sxs-lookup"><span data-stu-id="b6e6b-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="b6e6b-131">Programmā PSA vispārēju resursu varat rezervēt kādai projekta darba grupai un varat norādīt lomu, nepieciešamo noslodzi un veidu, kā šī noslodze ir jāizplata.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="b6e6b-132">Resursa vajadzībā varat norādīt atribūtus, kas ir saistīti ar šo vispārējo resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="b6e6b-133">Šie atribūti tostarp ir nepieciešamās prasmes, vēlamā organizācijas struktūrvienība un vēlamie resursi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="b6e6b-134">Lai vispārējā resursā kādam izstrādātājam norādītu nepieciešamās prasmes, izpildiet tālāk aprakstīto procedūru.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="b6e6b-135">Lapā **Projekti** , cilnē **Darba grupa** atlasiet vienumu **Jauns** , lai rezervētu kādu vispārējo resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Darba grupai rezervēts vispārējais resurss](media/Resource-Management-image9.png)

2. <span data-ttu-id="b6e6b-137">Skatā **Visi darba grupas dalībnieki** , kolonnā **Resursu vajadzība** atlasiet saiti, lai vispārīgajam resursam pievienotu nepieciešamās prasmes.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Vajadzības saite](media/Resource-Management-image10.png)

3. <span data-ttu-id="b6e6b-139">Tiek parādīta lapa **Resursu vajadzība** , un tās režģī **Prasmes** atlasiet daudzpunkti ( **...** ) un pēc tam atlasiet **Pievienot jaunu vajadzības īpašību** , lai savam izstrādātājam pievienotu nepieciešamās prasmes.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis ( **...** ) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Komanda Pievienot jaunu vajadzības īpašību](media/Resource-Management-image11.png)

4. <span data-ttu-id="b6e6b-141">Tiek parādīts dialoglodziņš **Ātrā izveide: Vajadzības īpašība** , un tā laukā **Īpašība** atlasiet nepieciešamo prasmi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="b6e6b-142">Pēc tam laukā **Novērtējuma vērtība** atlasiet kvalifikācijas līmeni šai prasmei.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="b6e6b-143">Visbeidzot laukā **Resursu vajadzība** iestatiet šo vajadzību, lai tā kā avotu izmantotu resursus no organizācijas struktūrvienībām vai pat nosauktiem resursiem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="b6e6b-144">Kad esat pabeidzis, noklikšķiniet uz **saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-144">When you've finished, select **Save**.</span></span>

    ![Dialoglodziņš Ātrā izveide: Vajadzības īpašība](media/Resource-Management-image12.png)

5. <span data-ttu-id="b6e6b-146">Lapā **Resursu vajadzība** atlasiet **Rezervēt** , lai izpildītu resursu vajadzību.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Poga Rezervēt lapā Resursu vajadzība](media/Resource-Management-image13.png)

    <span data-ttu-id="b6e6b-148">Varat arī atlasīt vispārējo resursu režģī **Visi darba grupas dalībnieki** un pēc tam atlasīt vienumu **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Poga Rezervēt virs režģa Visi darba grupas dalībnieki](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="b6e6b-150">Šajā piemērā ir 40 pieprasītās stundas, bet nav faktiski rezervētu stundu, jo vispārējiem resursiem nav rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="b6e6b-151">Turklāt nav piešķirtu stundu, jo vispārējais resurss tika pievienots tieši darba grupai.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="b6e6b-152">Tas netika pievienots, izmantojot uzdevumu piešķiršanu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="b6e6b-153">Lapā **Plānošanas palīgs** pieejamos resursus varat filtrēt pēc vajadzībām, kas ir norādītas resursu vajadzībā.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="b6e6b-154">Resursi tiek kārtoti atbilstoši plānošanas panelī norādītajiem kārtošanas parametriem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Lapa Plānošanas palīgs](media/Resource-Management-image15.png)

    <span data-ttu-id="b6e6b-156">Tālāk ir norādīti daži no bieži izmantotajiem filtriem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="b6e6b-157">**Īpašības kopā ar novērtējumu**  — papildus kvalifikācijas novērtējumiem filtrēt arī pēc prasmēm, sertifikācijām un citām resursu īpašībām.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="b6e6b-158">**Lomas**  — filtrēt pēc noklusējuma lomām, kas ir piešķirtas rezervējamiem resursiem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="b6e6b-159">**Organizācijas struktūrvienības**  — filtrēt rezervējamos resursus pēc organizācijas struktūrvienībām, kurām tie ir piešķirti.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="b6e6b-160">Ja neesat apmierināts ar sākotnējās vajadzības meklēšanas rezultātiem, varat mainīt šos filtrēšanas kritērijus.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="b6e6b-161">Izvērsiet rūti **Filtra skats** kreisajā pusē un pēc tam atlasiet **Meklēt** , lai atrastu papildu resursus.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Rūts Filtra skats](media/Resource-Management-image16.png)

7. <span data-ttu-id="b6e6b-163">Lai mainītu rezultātu kārtošanas veidu, atlasiet vienumu **Kārtot**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Komanda Kārtot](media/Resource-Management-image17.png)

8. <span data-ttu-id="b6e6b-165">Atlasiet resursus atbilstoši pieprasījumam, kas ir norādīts vajadzībā, kā redzams režģa augšpusē.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="b6e6b-166">Šūnu atlasi režģī varat notīrīt un atstāt šo resursa noslodzi atvērtu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="b6e6b-167">Kā rezervētu vienlaikus var atlasīt tikai vienu resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="b6e6b-168">Atlasiet **Rezervēt** , lai rezervētu atlasīto resursu, un atstājiet plānošanas paneli atvērtu, lai varētu atlasīt papildu resursus.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="b6e6b-169">Var arī atlasīt **Rezervēt un iziet** , lai rezervētu atlasīto resursu un aizvērtu plānošanas paneli.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Rezervējamais resurss](media/Resource-Management-image19.png)

    <span data-ttu-id="b6e6b-171">Jūs saņemat paziņojumu par rezervētajām stundām.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="b6e6b-172">Pieprasījuma indikatori rāda, cik ļoti rezervācijas vajadzība ir izpildīta un cik vēl ir atlicis.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="b6e6b-173">Varat arī redzēt, cik daudz no atlasītā resursa noslodzes ir patērēts.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="b6e6b-174">Atlasiet **Izvērst** , lai skatītu plašāku informāciju par resursu rezervēšanu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="b6e6b-175">Atgriezieties skatā **Visi darba grupas dalībnieki**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="b6e6b-176">Pievērsiet uzmanību, ka režģī šis vispārējais resurss ir aizstāts ar nosaukto resursu, un 40 stundas šim resursam ir norādītas kā rezervētas.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Atjauninātais skats Visi darba grupas dalībnieki](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="b6e6b-178">Netiek rādīta neviena piešķirtā stunda, jo tās tika rezervētas tieši darba grupai.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="b6e6b-179">Tās netika rezervētas, izmantojot uzdevumu piešķiršanu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="b6e6b-180">Vispārēju resursu piešķiršana uzdevumiem un resursu vajadzību ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="b6e6b-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="b6e6b-181">Programmā PSA varat izveidot uzdevumus un pēc tam šiem uzdevumiem piešķirt vispārējos resursus.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="b6e6b-182">Šādi resursu pieprasījumu var parādīt kā vietturus, kamēr veidojat grafika un finanšu skaitļu tāmi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="b6e6b-183">Pēc tam varat ģenerēt resursu vajadzības attiecībā uz vispārīgajiem resursiem un izpildīt tās.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="b6e6b-184">Lapā **Projekti** , cilnē **Grafiks** atlasiet vienumu **Pievienot** , lai izveidotu uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Izveidots jauns uzdevums](media/Resource-Management-image21.png)

2. <span data-ttu-id="b6e6b-186">Laukā **Resursi** atlasiet simbolu **Resursu atlasītājs**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="b6e6b-187">Tiek parādīts resursu atlasītājs, un tajā tiek rādīti šim projektam esošie darba grupas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Resursu atlasītājs](media/Resource-Management-image22.png)

3. <span data-ttu-id="b6e6b-189">Ievadiet jaunā vispārējā resursa nosaukumu un pēc tam atlasiet vienumu **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Ievadīts jaunā vispārējā resursa nosaukums](media/Resource-Management-image23.png)

4. <span data-ttu-id="b6e6b-191">Tiek parādīts dialoglodziņš **Ātrā izveide: Projekta darba grupas dalībnieks** , un tā laukā **Loma** atlasiet lomu šim vispārējam resursam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="b6e6b-192">Laukā **Resursu vienība** atlasiet organizācijas struktūrvienību šim vispārējam resursam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="b6e6b-193">Pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-193">Then select **Save**.</span></span>

    ![Dialoglodziņš Ātrā izveide: Projekta darba grupas dalībnieks](media/Resource-Management-image24.png)

    <span data-ttu-id="b6e6b-195">Tagad vispārējais darba grupas dalībnieks ir piešķirts šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-195">The generic team member is now assigned to the task.</span></span>

    ![Vispārējais darba grupas dalībnieks ir piešķirts uzdevumam](media/Resource-Management-image25.png)

    <span data-ttu-id="b6e6b-197">Cilnē **Darba grupa** ir redzams jaunais vispārējais darba grupas dalībnieks.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="b6e6b-198">Ievērojiet, ka tam ir tikai piešķirtas stundas.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="b6e6b-199">Šīs stundas ir summa no visiem tiem uzdevumiem, kas ir piešķirti vispārējam darba grupas dalībniekam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="b6e6b-200">Vispārējam darba grupas dalībniekam vēl nav nepieciešamo stundu vai resursu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Vispārējais darba grupas dalībnieks cilnē Darba grupa](media/Resource-Management-image26.png)

5. <span data-ttu-id="b6e6b-202">Tagad šo vispārējo darba grupas dalībnieku varat piešķirt citiem uzdevumiem, izmantojot resursu atlasītāju.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Vispārējais darba grupas dalībnieks resursu atlasītājā](media/Resource-Management-image27.png)

    <span data-ttu-id="b6e6b-204">Kad esat beidzis vispārējā resursa piešķiršanu uzdevumiem, varat ģenerēt resursu vajadzību šim vispārējam resursam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="b6e6b-205">Cilnē **Darba grupa** atlasiet vispārējo resursu un pēc tam atlasiet **Ģenerēt vajadzību**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Komanda Ģenerēt vajadzību](media/Resource-Management-image28.png)

    <span data-ttu-id="b6e6b-207">Kad vajadzība ir ģenerēta, vispārējam darba grupas dalībniekam būs nepieciešamās stundas un saite šai resursu vajadzībai.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Resursu vajadzības saite](media/Resource-Management-image29.png)

    <span data-ttu-id="b6e6b-209">Kad ir rezervēts kāds nosaukts resurss, vispārējais resurss no darba grupas tiek noņemts un aizstāts ar nosaukto resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Vispārējais resurss ir aizstāts ar nosaukto resursu](media/Resource-Management-image30.png)

    <span data-ttu-id="b6e6b-211">Cilnē **Grafiks** vispārējo resursu piešķires tiek noņemtas un aizstātas ar nosaukto resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Cilnē Grafiks vispārējā resursa piešķires ir aizstātas ar nosaukto resursu](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="b6e6b-213">Tas notiek tikai tad, ja vispārējā resursa vajadzībai nosauktais resurss ir rezervēts pilnībā.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="b6e6b-214">Ja nosaukts resurss vispārējā resursa vajadzību aizstāj tikai daļēji vai ja vispārējā resursa vajadzību aizstāj vairāki nosauktie resursi, vispārējais resurss paliek piešķirts uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="b6e6b-215">Nākamajā ilustrācijā ir parādīts, ka 80 stundu uzdevums ir plānots piecu dienu ilgumā (16 stundas dienā piecu dienu ilgumā) un piešķirts vispārējam resursam ar nosaukumu **Funkcionāls**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Astoņdesmit stundu, piecu dienu uzdevums, kas ir piešķirts vispārējam resursam Funkcionāls](media/Resource-Management-image32.png)

    <span data-ttu-id="b6e6b-217">Kad ģenerējat šo vajadzību, tā ir 80 stundām piecu dienu ilgumā.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Vajadzība ir ģenerēta 80 stundām piecu dienu ilgumā](media/Resource-Management-image33.png)

    <span data-ttu-id="b6e6b-219">Tā kā pieejamie resursi darbojas tikai astoņas stundas dienā, šīs vajadzības izpildīšanai ir nepieciešami divi resursi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Otrais resurss](media/Resource-Management-image35.png)

    <span data-ttu-id="b6e6b-221">Tagad cilnē **Darba grupa** varat redzēt, ka vispārējam resursam nav nepieciešamo stundu, bet piešķirtās stundas joprojām tiek rādītas kopā ar abiem nosauktajiem resursiem, kas veido šo izpildi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Divi nosauktie resursi cilnē Darba grupa](media/Resource-Management-image36.png)

    <span data-ttu-id="b6e6b-223">Cilnē **Grafiks** vispārējais resurss paliek piešķirts šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Vispārējie resursi cilnē Grafiks](media/Resource-Management-image37.png)

<span data-ttu-id="b6e6b-225">PSA nepiešķir abus resursus šim uzdevumam, jo šāda uzvedība radītu mazāk prognozējamu grafiku.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="b6e6b-226">Šajā vienkāršajā piemērā stundas var viegli sadalīt vienādi starp diviem resursiem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="b6e6b-227">Taču sarežģītākos scenārijos, kas ietver vairākus uzdevumus un vairākus resursus, programmai PSA būtu jāizdara pieņēmumi par veidu, kā piešķirt rezervācijas, kas ir saņemtas par vairākiem resursiem vairākos uzdevumos.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="b6e6b-228">Tādēļ šajos scenārijos projektu vadītājs ir atbildīgs par vairāku rezervāciju parsēšanu un to piešķiršanu pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="b6e6b-229">Lai sadalītu rezervācijas, projektu vadītājs no vispārējiem resursiem piešķir uzdevumus nosauktajiem resursiem un pēc tam izmanto skatu **Saskaņošana** , lai pārliecinātos, ka sadalīšana ar šādām rezervācijām darbojas.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="b6e6b-230">Resursu vajadzības rediģēšana</span><span class="sxs-lookup"><span data-stu-id="b6e6b-230">Edit a resource requirement</span></span>

<span data-ttu-id="b6e6b-231">Kad resursu vajadzība ir izveidota, projektu vadītājs vai resursu pārvaldnieks varētu vēlēties rediģēt detalizēto informāciju, lai precizētu meklēšanas kritērijus, kad tiek izmantots plānošanas panelis.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="b6e6b-232">Lai rediģētu resursu vajadzību, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="b6e6b-233">Lapā **Projekti** , cilnē **Darba grupa** atlasiet saiti uz jebkuru no vispārējo resursu vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="b6e6b-234">Tiek parādīta lapa **Resursu vajadzība** , un tajā varat atjaunināt vairākus atribūtus.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="b6e6b-235">Lūk, daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="b6e6b-235">Here are some examples:</span></span>

    - <span data-ttu-id="b6e6b-236">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="b6e6b-236">Name</span></span>
    - <span data-ttu-id="b6e6b-237">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="b6e6b-237">From Date</span></span>
    - <span data-ttu-id="b6e6b-238">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="b6e6b-238">To Date</span></span>
    - <span data-ttu-id="b6e6b-239">Ilgums</span><span class="sxs-lookup"><span data-stu-id="b6e6b-239">Duration</span></span>
    - <span data-ttu-id="b6e6b-240">Resursa tips</span><span class="sxs-lookup"><span data-stu-id="b6e6b-240">Resource Type</span></span>

<span data-ttu-id="b6e6b-241">Lapā **Resursu vajadzība** projektu vadītājs vai resursu pārvaldnieks var arī definēt tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="b6e6b-242">Prasmes</span><span class="sxs-lookup"><span data-stu-id="b6e6b-242">Skills</span></span>
- <span data-ttu-id="b6e6b-243">Lomas</span><span class="sxs-lookup"><span data-stu-id="b6e6b-243">Roles</span></span>
- <span data-ttu-id="b6e6b-244">Resursu preferences</span><span class="sxs-lookup"><span data-stu-id="b6e6b-244">Resource preferences</span></span>
- <span data-ttu-id="b6e6b-245">Vēlamā organizācijas struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="b6e6b-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="b6e6b-246">Resursu rezervāciju atjaunināšana pēc to rezervēšanas projektam</span><span class="sxs-lookup"><span data-stu-id="b6e6b-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="b6e6b-247">Kad vispārēju vai nosauktu resursu esat pievienojis projekta darba grupai, varat mainīt šī resursa rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="b6e6b-248">Lapā **Projekti** , cilnē **Darba grupa** atlasiet kādu darba grupas dalībnieku un pēc tam atlasiet vienumu **Uzturēt rezervācijas**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Plānošanas panelis ir atvērts atlasītajam darba grupas dalībniekam](media/Resource-Management-image40.png)

    <span data-ttu-id="b6e6b-250">Tiek parādīts plānošanas panelis, un tajā ir redzamas projekta darba grupas dalībnieku rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="b6e6b-251">Izvērsiet darba grupas dalībnieka ierakstu, lai skatītu informāciju par stundām, kuras ir rezervētas šim projektam un citiem projektiem, kas patērē šī darba grupas dalībnieka noslodzi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="b6e6b-252">Atlasiet un velciet rezervāciju, lai to paplašinātu vai saīsinātu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="b6e6b-253">Tiek parādīts dialoglodziņš **Izveidot resursu rezervāciju** , un tajā varat pielāgot šo rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Dialoglodziņš Izveidot resursu rezervāciju](media/Resource-Management-image41.png)

3. <span data-ttu-id="b6e6b-255">Ar peles labo pogu noklikšķiniet uz rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-255">Right-click the booking.</span></span> <span data-ttu-id="b6e6b-256">Pēc tam varat izmantot īsinājumizvēlni, lai veiktu tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="b6e6b-257">Mainīt rezervācijas statusu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-257">Change the booking status.</span></span>
    - <span data-ttu-id="b6e6b-258">Rediģēt rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-258">Edit the booking.</span></span>
    - <span data-ttu-id="b6e6b-259">Aizstāt resursu projekta grupā.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="b6e6b-260">Rezervācijas statusa mainīšana</span><span class="sxs-lookup"><span data-stu-id="b6e6b-260">Change the booking status</span></span>

<span data-ttu-id="b6e6b-261">Varat mainīt jebkuru noklusējuma vai pielāgoto rezervācijas statusu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-261">You can change any default or custom booking status.</span></span>

![Komanda Mainīt statusu](media/Resource-Management-image42.png)

<span data-ttu-id="b6e6b-263">Programmā PSA ir tālāk norādītie statusi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="b6e6b-264">**Atcelts** — šis statuss atceļ resursa rezervāciju un atbrīvo resursa noslodzi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="b6e6b-265">**Stingrā rezervēšana** — šis statuss patērē resursa noslodzi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="b6e6b-266">Ja vienumu **Uzturēt rezervācijas** atverat no režģa **Visi darba grupas dalībnieki** lapā **Projekti** , rezervācijai parasti ir šis statuss.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="b6e6b-267">**Vieglā rezervēšana** — šis statuss resursu pievieno darba grupai, bet nepatērē resursa noslodzi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="b6e6b-268">Tas norāda, ka resurss ir rezervēts iespējamam darbam, bet tam joprojām ir noslodze, ja gadījumā tas ir nepieciešams citiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="b6e6b-269">Vispārīgās resursu pieejamības ziņā vieglajai rezervēšanai ir citāds statuss nekā stingrajai rezervēšanai.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="b6e6b-270">**Piedāvāts** — šis statuss apzīmē resursu pārvaldnieka vai projektu vadītāja piedāvājumu kādam resursam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="b6e6b-271">Piedāvājumi nepatērē resursa noslodzi, un resurss netiek pievienots projekta grupai.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="b6e6b-272">Lai resursam veiktu stingro rezervēšanu darba grupai, projektu vadītājam ir jāpieņem piedāvājums.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="b6e6b-273">Resursu pieprasījumu iesniegšana</span><span class="sxs-lookup"><span data-stu-id="b6e6b-273">Submit resource requests</span></span>

<span data-ttu-id="b6e6b-274">Resursu pieprasījumi tiek izmantoti, lai ievērotu pieprasījumu (resursu vajadzību), kas ir jāizpilda kādam resursu pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="b6e6b-275">Vispārējam resursam, kas jau ir darba grupā, resursu pieprasījumu varat iesniegt tieši.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="b6e6b-276">Resursu pieprasījumu var izpildīt divos tālāk aprakstītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="b6e6b-277">Resursu pārvaldnieks pieprasījumu izpilda tieši.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="b6e6b-278">Šādā gadījumā vispārējais resurss tiek aizstāts ar stingro rezervēšanu, kurai ir nosaukts resurss.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="b6e6b-279">Resursu pārvaldnieks piedāvā kādu resursu projektu vadītājam, un projektu vadītājs apstiprina vai noraida šo piedāvāto resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="b6e6b-280">Resursu pieprasījumu tiešā izpildīšana</span><span class="sxs-lookup"><span data-stu-id="b6e6b-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="b6e6b-281">Kad resursu vajadzība ir ģenerēta, projektu vadītājs var iesniegt resursu pieprasījumu vispārējam resursam, atlasot šo resursu un pēc tam atlasot vienumu **Iesniegt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Poga Iesniegt pieprasījumu](media/Resource-Management-image45.png)

<span data-ttu-id="b6e6b-283">Resursu pārvaldniekam, kurš izpilda pieprasījumu, var sniegt komentārus par šo resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="b6e6b-284">Kad pieprasījums ir iesniegts, lauks **Statuss** attiecīgajam darba grupas dalībniekam mainās uz **Iesniegts**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Neobligātu komentāru ievadīšana](media/Resource-Management-image46.png)

<span data-ttu-id="b6e6b-286">Kad resursu pārvaldnieks izpilda pieprasījumu, režģī **Visi darba grupas dalībnieki** vispārējais darba grupas dalībnieks tiek aizstāts ar nosaukto resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Vispārējais darba grupas dalībnieks tiek aizstāts ar nosaukto resursu režģī Visi darba grupas dalībnieki](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="b6e6b-288">Resursu piedāvājumu lietošana resursu pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="b6e6b-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="b6e6b-289">Tā vietā, lai resursu tieši rezervētu resursu pieprasījumā, resursu pārvaldnieks resursu var piedāvāt projektu vadītājam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="b6e6b-290">Resursu pārvaldnieks var izmantot šo opciju, ja precīza atbilstība vajadzībām nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="b6e6b-291">Kad resursu pārvaldnieks piedāvā kādu resursu, projektu vadītājs redz, ka lauks **Statuss** attiecīgajam vispārējam darba grupas dalībniekam tiek mainīts uz **Jāpārskata**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Vispārējā darba grupas dalībnieka statuss ir mainīts uz Jāpārskata](media/Resource-Management-image48.png)

<span data-ttu-id="b6e6b-293">Lai piedāvāto resursu skatītu kopā ar piedāvājuma rezervācijas efekta vizualizāciju, veiciet dubultklikšķi uz darba grupas dalībnieka, kura statuss ir **Jāpārskata**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="b6e6b-294">Pēc tam atlasiet cilni **Piedāvātie resursi**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-294">Then select the **Proposed Resources** tab.</span></span>

![Cilne Piedāvātie resursi](media/Resource-Management-image49.png)

<span data-ttu-id="b6e6b-296">Atlasiet **Pieņemt visus piedāvājumus** , lai pieņemtu visus piedāvātos resursus, vai atlasiet **Noraidīt visus piedāvājumus** , lai tos noraidītu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="b6e6b-297">Ja pieņemat piedāvātos resursus, tie ir stingri rezervēti projektā kā darba grupas dalībnieki un aizstāj vispārējos resursus.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="b6e6b-298">Ir jāpieņem vai jānoraida visi piedāvātie resursi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="b6e6b-299">Tos nevar pieņemt vai noraidīt daļēji.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="b6e6b-300">Resursa aizstāšana projekta grupā</span><span class="sxs-lookup"><span data-stu-id="b6e6b-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="b6e6b-301">Reizēm projektu vadītājam projektā ir jāaizstāj kāds no rezervētajiem darba grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="b6e6b-302">Lapā **Projekti** , cilnē **Darba grupa** atlasiet kādu resursu, kam ir nepieciešams aizstājējs, un pēc tam atlasiet vienumu **Uzturēt rezervācijas**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="b6e6b-303">Izvērsiet resursu, lai apskatītu projektus, kuriem tas ir piešķirts.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Resurss ir izvērsts, lai parādītu piešķirtos projektus](media/Resource-Management-image50.png)

3. <span data-ttu-id="b6e6b-305">Ar peles labo pogu noklikšķiniet uz projekta un pēc tam atlasiet vienumu **Aizstāt resursu**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="b6e6b-306">Ja zināt, ar kuru resursu aizstāt pašreizējo resursu, atlasiet vai ierakstiet nosaukumu un pēc tam atlasiet vienumu **Pārpiešķirt**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Aizstājošā resursa norādīšana](media/Resource-Management-image51.png)

    <span data-ttu-id="b6e6b-308">Vai arī izpildiet tālāk norādītās darbības, lai meklētu kādu resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="b6e6b-309">Atlasiet **Atrast aizstājēju**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-309">Select **Find Substitution**.</span></span>

        ![Aizstājošā resursa meklēšana](media/Resource-Management-image52.png)

        <span data-ttu-id="b6e6b-311">Plānošanas palīgs parāda sarakstu ar pieejamajiem aizstājējiem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="b6e6b-312">Plānošanas palīgā pieejamos resursus varat papildus filtrēt, lai atrastu piemērotu aizstājēju.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Pieejamo aizstājēju saraksts](media/Resource-Management-image53.png)

    2. <span data-ttu-id="b6e6b-314">Lai aizstātu resursu, atlasiet nepieciešamo resursu un pēc tam atlasiet **Aizstāt**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Aizstājošais resurss ir atlasīts](media/Resource-Management-image54.png)

    <span data-ttu-id="b6e6b-316">Rezervācijas un piešķires tiek aizstātas ar jauno resursu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Rezervācijas un piešķires ir aizstātas ar jauno resursu](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="b6e6b-318">Darba grupas dalībnieku rezervāciju un piešķiru saskaņošana</span><span class="sxs-lookup"><span data-stu-id="b6e6b-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="b6e6b-319">Darba grupas dalībniekiem rezervācijas un piešķires ir brīvi savienotas.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="b6e6b-320">Citiem vārdiem sakot — resursiem var būt piešķires, bet var nebūt rezervāciju, vai arī tiem var būt rezervācijas, bet var nebūt piešķiru.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="b6e6b-321">Ideālā gadījumā rezervācijām un piešķirēm vajadzētu būt saskaņotām, lai resursiem būtu atvēlēta noslodze uzdevumu piešķiru izpildīšanai.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="b6e6b-322">Taču rezervācijas var būt balstītas uz pieejamību, un projekta gaitā uzdevumu laiki var mainīties.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="b6e6b-323">Tādēļ rezervāciju un piešķiru brīvais savienojums nodrošina elastību.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="b6e6b-324">Programmā PSA ir cilne **Saskaņošana** , kas ļauj projektu vadītājiem saskaņot darba grupas dalībnieku rezervācijas un viņu piešķires projektu darba grupās.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Cilne Saskaņošana](media/Resource-Management-image56.png)

<span data-ttu-id="b6e6b-326">Cilnē **Saskaņošana** rezervācijas un piešķires katram darba grupas dalībniekam ir parādītas līdz atsevišķa uzdevuma piešķires līmenim.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="b6e6b-327">Tur tiek rādītas stundas šūnās, kas apzīmē laika periodus no mēnešiem līdz dienām.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="b6e6b-328">Šajā cilnē ir redzama arī projekta vispārējā neto kopsumma kopā ar kolonnu kopsummu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="b6e6b-329">Katram resursam šī cilne aprēķina atšķirību starp darba grupas dalībnieka rezervācijām un darba grupas dalībnieka uzdevumu piešķiru apkopojumu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="b6e6b-330">Ideālā gadījumā šai atšķirībai vajadzētu būt 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="b6e6b-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="b6e6b-331">Citiem vārdiem sakot — starp rezervācijām un piešķirēm nevajadzētu būt nekādai starpībai.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="b6e6b-332">Atšķirības tiek iekrāsotas un ieēnotas, lai pievērstu uzmanību diviem tālāk aprakstītajiem apstākļiem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="b6e6b-333">**Rezervācijas deficīts** — rezervācijas deficīts rodas, ja resursam ir vairāk piešķiru nekā rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="b6e6b-334">Tā kā šī noslodze vēl nav rezervēta, projektu vadītājs var vēlēties izlabot šo apstākli, paplašinot resursa rezervācijas, lai segtu šo nepietiekamību.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="b6e6b-335">**Rezervāciju pārsniegšana** — rezervāciju pārsniegšana rodas, kad resurss ir rezervēts projektam, bet nav piešķirts uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="b6e6b-336">Šis apstāklis var būt pieņemams gadījumos, kad resurss projektam tika rezervēts vēl pirms tam, kad radās uzdevuma piešķire.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="b6e6b-337">Taču citos gadījumos resursu nav plānots piešķirt uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="b6e6b-338">Šādos gadījumos projektu vadītājam ir jāapsver resursa rezervācijas atcelšana, lai šo noslodzi varētu izmantot citam projektam.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="b6e6b-339">Reizēm, kad laiku skatāt augstākā līmenī nekā dienas līmenis (piemēram, mēneša līmenī), varat pamanīt, ka neto starpība resursam ir nulle (citiem vārdiem sakot, rezervācijas = piešķires).</span><span class="sxs-lookup"><span data-stu-id="b6e6b-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="b6e6b-340">Taču, ja laiku skatāt nedēļas līmenī, varat redzēt, ka pirmajā nedēļā piešķires ir nulle stundu un rezervācijas ir 40 stundas, bet otrajā nedēļā piešķires ir 40 stundas un rezervācijas ir nulle stundu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="b6e6b-341">Kopumā rezervācijas un piešķires ir saskaņotas, bet katrai nedēļai tās atšķiras.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="b6e6b-342">Kad laiku skatāties augstākos līmeņos, šūnām cilnē **Saskaņošana** ir indikators, lai informētu jūs, ka pastāv atšķirības zemākos līmeņos.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="b6e6b-343">Veicot dubultklikšķi uz šūnas, varat tuvināt, lai apskatītu atšķirību.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="b6e6b-344">Pēc tam varat noklikšķināt ar peles labo pogu, lai tālinātu. Atlasot kādu resursu un pēc tam režģa rīkjoslā izmantojot vadīklu **Nākamā atšķirība** , varat pāriet uz nākamo atšķirību starp šī resursa rezervācijām un piešķirēm.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="b6e6b-345">Pēc tam varat izmantot vadīklu **Iepriekšējā atšķirība** , lai dotos atpakaļ.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="b6e6b-346">Varat arī izslēgt atšķirību indikatoru un navigācijas uzvedību sadaļā **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Atšķirību indikators](media/Resource-Management-image57.png)

<span data-ttu-id="b6e6b-348">Ja jums ir uzdevumu piešķires kādam resursam, bet nav nevienas rezervācijas, lapā **Projekti** , cilnē **Saskaņošana** atlasiet rezervāciju deficītu un pēc tam atlasiet vienumu **Paplašināt rezervāciju**.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="b6e6b-349">Tiek parādīts dialoglodziņš **Paplašināt rezervāciju** , un tajā ir redzama rezervācija, kura ir nepieciešama, lai novērstu šo resursu deficītu.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="b6e6b-350">Tur ir redzamas arī resursu esošās rezervācijas visos projektos vai citos plānojamos elementos.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="b6e6b-351">Ja atlasāt **Labi** , lai izveidotu rezervāciju attiecīgajam resursam neatkarīgi no šī resursa pieejamības, varat izraisīt virsrezervāciju.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Dialoglodziņš Paplašināt rezervāciju](media/Resource-Management-image58.png)

<span data-ttu-id="b6e6b-353">Pēc tam projektu vadītājs vai resursu pārvaldnieks var izmantot plānošanas paneli, lai pārvaldītu visas situācijas, kur resursa rezervācija pārsniedz tā noslodzi.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
