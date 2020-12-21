---
title: Projekta pārdošanas un izmaksu aprēķins, kad rezervējamais resurss projektā aizpilda vairākas lomas
description: Šajā tēmā ir sniegta informācija par to, kā izcenojuma dimensijas var izmantot, lai atbalstītu izcenojuma un izmaksu aprēķināšanu resursam, kas projektā aizpilda vairākas lomas.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080496"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="eafb7-103">Projekta pārdošanas un izmaksu aprēķins, kad rezervējamais resurss projektā aizpilda vairākas lomas</span><span class="sxs-lookup"><span data-stu-id="eafb7-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="eafb7-104">Uz projektiem balstītiem uzņēmumiem bieži vien ir nepieciešams viens resurss, lai izpildītu vairākas lomas projektā.</span><span class="sxs-lookup"><span data-stu-id="eafb7-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="eafb7-105">Katrai no šīm lomām var veikt atšķirīgu izcenojuma un izmaksu aprēķināšanu, kas nozīmē to, ka vienam resursa laikam projektā var būt dažādi finanšu aprēķini atkarībā no rēķina un izmaksu likmes katrai lomai.</span><span class="sxs-lookup"><span data-stu-id="eafb7-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="eafb7-106">Project Service Automation ļauj iestatīt vērtības darba grupas dalībnieka ierakstā par nosaukto resursu, kā arī ļauj veikt dažādus pārlabojumus katrā no darba grupas dalībniekam piešķirtajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="eafb7-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="eafb7-107">Tālāk sniegtajā piemērā ir paskaidrots, kā šīs vērtības vienkārša pārlabošana ļauj piešķirt resursam vairākas lomas projektā ar dažādām izmaksu un rēķina likmēm.</span><span class="sxs-lookup"><span data-stu-id="eafb7-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="eafb7-108">Uzdevumu izveide</span><span class="sxs-lookup"><span data-stu-id="eafb7-108">Create tasks</span></span>
<span data-ttu-id="eafb7-109">Izveidojiet divus projekta uzdevumus, katru pa 40 stundām, A uzdevumu un B uzdevumu. Atlasiet A uzdevumu kā B uzdevuma priekšteci.</span><span class="sxs-lookup"><span data-stu-id="eafb7-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="eafb7-110">Lomas un organizācijas vienības iestatīšana vispārīgam projekta darba grupas dalībniekam</span><span class="sxs-lookup"><span data-stu-id="eafb7-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="eafb7-111">Lapā **Plānošana** atlasiet A uzdevumam rindu **Uzdevums**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="eafb7-112">Laukā **Resursi** nolaižamajā sarakstā atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="eafb7-113">Lapā **Darba grupas dalībnieka ātrā izveide** lapā norādiet tā vispārīgā darba grupas dalībnieka, kas var veikt šo uzdevumu, atribūtus.</span><span class="sxs-lookup"><span data-stu-id="eafb7-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="eafb7-114">Atlasiet atbilstošo lomu un organizācijas vienību un pēc tam atlasiet vienumu **Saglabāt un aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="eafb7-115">Vispārīgs darba grupas dalībnieks tiek izveidots un piešķirts šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="eafb7-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="eafb7-116">Atkārtojiet šīs darbības B uzdevumam un pārliecinieties, vai B uzdevumam izveidotā vispārīgā darba grupas dalībnieka loma un organizācijas vienība ir citāda nekā A uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="eafb7-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="eafb7-117">Lomas un organizācijas vienības iestatīšana projekta uzdevumam</span><span class="sxs-lookup"><span data-stu-id="eafb7-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="eafb7-118">Pēc A uzdevuma izveidošanas atlasiet šo uzdevumu un pēc tam atlasiet vienumu **Rediģēt uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="eafb7-119">Lapā **Uzdevuma dati** atrodiet laukus **Loma** un **Organizācijas vienība** , pievienojiet nepieciešamās vērtības no resursa, kurš veiks šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="eafb7-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="eafb7-120">Ja izpildīsiet šos scenārijus, izmantojot Project Service Automation demonstrācijas datus, lomai atlasiet **Konsultāciju interesents** un **Fabrikam US** kā organizācijas vienību.</span><span class="sxs-lookup"><span data-stu-id="eafb7-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="eafb7-121">Atlasiet B uzdevumu un pēc tam atlasiet **Rediģēt uzdevumu**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="eafb7-122">Lapā **Uzdevuma dati** atrodiet laukus **Loma** un **Organizācijas vienība** , pievienojiet nepieciešamās vērtības no resursa, kurš veiks šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="eafb7-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="eafb7-123">Pārliecinieties, vai vērtības laukos **Loma** un **Organizācijas vienība** B uzdevumam ir citādas nekā A uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="eafb7-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="eafb7-124">Ja izpildīsiet šos scenārijus, izmantojot Project Service Automation demonstrācijas datus, lomai atlasiet **Tīkla tehniķis** un **Fabrikam US** kā organizācijas vienību.</span><span class="sxs-lookup"><span data-stu-id="eafb7-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="eafb7-125">Saglabājiet un aizveriet lapu **Uzdevuma dati**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="eafb7-126">Darba grupas dalībnieka un novērtējuma uzvedība</span><span class="sxs-lookup"><span data-stu-id="eafb7-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="eafb7-127">Lapā **Uzdevuma dati** pie **Darba grupas dalībnieks** atlasiet divus vispārīgus darba grupas dalībniekus un pēc tam atlasiet **Ģenerēt prasības**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="eafb7-128">Tādējādi tiks ģenerētas resursu prasības.</span><span class="sxs-lookup"><span data-stu-id="eafb7-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="eafb7-129">Atlasiet darba grupas dalībnieka rindu, lai izvēletos **Konsultāciju interesentu** , un pēc tam atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="eafb7-130">Tiek atvērts plānošanas panelis, un šai prasībai tiek rezervēts resurss.</span><span class="sxs-lookup"><span data-stu-id="eafb7-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="eafb7-131">Atlasiet darba grupas dalībnieka rindu, lai izvēletos vienumu **Tīkla tehniķis** , un pēc tam atlasiet **Rezervēt**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="eafb7-132">Tiek atvērts plānošanas panelis, un šai prasībai tiek rezervēts tas pats resurss.</span><span class="sxs-lookup"><span data-stu-id="eafb7-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="eafb7-133">Darba grupas dalībnieka režģis</span><span class="sxs-lookup"><span data-stu-id="eafb7-133">Team Member grid</span></span> 
<span data-ttu-id="eafb7-134">Ņemiet vērā, ka **Darba grupas dalībnieka** režģī abi vispārīgā darba grupas dalībnieka ieraksti ir dzēsti un ir aizstāti kā viens resurss.</span><span class="sxs-lookup"><span data-stu-id="eafb7-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="eafb7-135">Šim resursam ir viena vērtību kopa, kurā tiek parādīta **Lomas** un **Organizācijas vienības** noklusējuma vērtību kopa.</span><span class="sxs-lookup"><span data-stu-id="eafb7-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="eafb7-136">Izvēršot šī darba grupas dalībnieka ieraksta rindu, abiem šiem uzdevumiem darba grupas dalībnieka ierakstā redzami atšķirīgi piešķīrumi.</span><span class="sxs-lookup"><span data-stu-id="eafb7-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="eafb7-137">Katrai piešķīruma rindai ir uzdevumam specifiskas **Lomas** un **Organizācijas vienības** vērtības.</span><span class="sxs-lookup"><span data-stu-id="eafb7-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="eafb7-138">Novērtējumu režģis</span><span class="sxs-lookup"><span data-stu-id="eafb7-138">Estimates grid</span></span> 
<span data-ttu-id="eafb7-139">Naviģējot uz **Novērtējumu** režģi, pamanīsiet, ka viena un tā paša resursa diviem uzdevumiem ir atšķirīgs cenas aprēķins.</span><span class="sxs-lookup"><span data-stu-id="eafb7-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="eafb7-140">A uzdevuma resursa piešķīrumam cena tiek noteikta, izmantojot **Lomas** atribūta vērtību no **Konsultāciju interesenta**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="eafb7-141">B uzdevuma tā paša resursa piešķīrumam cena tiek noteikta, izmantojot **Lomas** atribūtu no **Tīkla tehniķa**.</span><span class="sxs-lookup"><span data-stu-id="eafb7-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>




