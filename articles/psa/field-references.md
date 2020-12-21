---
title: Pielāgoti lauki cenas iestatījumam un transakciju entītijām
description: Šajā tēmā ir sniegta informācija par pielāgotu lauku pievienošanu cenas iestatījumam un transakciju entītijām.
author: Rumant
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
ms.openlocfilehash: 32d0dbc3a69d713dcae8d27e52f2a0c6fc296127
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080550"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a><span data-ttu-id="36809-103">Pielāgoti lauki cenas iestatījumam un transakciju entītijām</span><span class="sxs-lookup"><span data-stu-id="36809-103">Add custom fields to price setup and transactional entities</span></span> 
<span data-ttu-id="36809-104">Šajā tēmā tiek pieņemts, ka tēmas procedūras ir pabeigtas, [Pielāgotu lauku un entītiju izveide](create-custom-fields-entities.md).</span><span class="sxs-lookup"><span data-stu-id="36809-104">This topic assumes that you have completed the procedures in the topic, [Create custom fields and entities](create-custom-fields-entities.md).</span></span> <span data-ttu-id="36809-105">Ja šīs procedūras neesat pabeidzis, atgriezieties un pabeidziet tās, un pēc tam atgriezieties pie šīs tēmas.</span><span class="sxs-lookup"><span data-stu-id="36809-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="36809-106">Šajā tēmā procedūras parādīs, kā pievienot vajadzīgās pielāgotās lauku atsauces entītijām un lietotāja saskarnes (UI) elementus, piemēram, veidlapas un skatus.</span><span class="sxs-lookup"><span data-stu-id="36809-106">In this topic, the procedures will show you how to add the required custom field references to entities and to the user interface (UI) elements such as forms and views.</span></span>

## <a name="add-custom-pricing-dimension-fields"></a><span data-ttu-id="36809-107">Pielāgotu cenas noteikšanas dimensiju lauku pievienošana</span><span class="sxs-lookup"><span data-stu-id="36809-107">Add custom pricing dimension fields</span></span> 
<span data-ttu-id="36809-108">Pēc pielāgotu lauku un entītiju izveidošanas nākamais solis ir panākt, lai cenas iestatījumi un transakciju entītijas brīdinātu par pielāgotām entītijām vai opciju kopām, izveidojot atsauču laukus.</span><span class="sxs-lookup"><span data-stu-id="36809-108">After custom fields and entities have been created, the next step is to make price setup and transactional entities aware of any custom entities or option sets by creating reference fields.</span></span> <span data-ttu-id="36809-109">Atkarībā no tā, vai jūsu cenrāža dimensiju sarakstā ir iekļautas opciju kopas dimensijas vai entītiju dimensijas, vai arī abas, veiciet tikai tās darbības, kas ir **Uz opciju kopu pamatotas pielāgotās cenu noteiktās dimensijas** vai **Uz entītijām pamatotas pielāgotās cenu noteiktās dimensijas** , vai tās abas.</span><span class="sxs-lookup"><span data-stu-id="36809-109">Depending on whether your pricing dimensions list includes option set dimensions or entity dimensions or both, follow only the steps in **Option set-based custom pricing dimensions** or **Entity-based custom pricing dimensions** , or both, respectively.</span></span>

### <a name="option-set-based-custom-pricing-dimensions"></a><span data-ttu-id="36809-110">Uz opciju kopu pamatotas pielāgotās cenu noteiktās dimensijas</span><span class="sxs-lookup"><span data-stu-id="36809-110">Option set-based custom pricing dimensions</span></span>
<span data-ttu-id="36809-111">Ja ir noteikta opcija pielāgotā cenu noteikšanas dimensija, pievienojiet to kā galveno Project Service entītiju lauku.</span><span class="sxs-lookup"><span data-stu-id="36809-111">When a custom pricing dimension is option set-based, add it as a field to key Project Service entities.</span></span> <span data-ttu-id="36809-112">Šajā procedūrā **Resursa darba atrašanās vieta** un **Resursa darba stundas** tiek izmantotas kā opciju kopas cenas noteikšanas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="36809-112">In the following procedure, **Resource Work Location** and **Resource Work Hours** are used as the option set-based pricing dimensions.</span></span> <span data-ttu-id="36809-113">Tās vispirms ir jāpievieno kā cenu noteikšanas entītijām **Lomu cenas** un **Lomu cenas uzcenojums**.</span><span class="sxs-lookup"><span data-stu-id="36809-113">These must first be added as fields to the pricing entities, **Role Price** and **Role Price Markup**.</span></span>

1. <span data-ttu-id="36809-114">Platformā Project Service Automation (PSA) noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="36809-114">In Project Service Automation (PSA), click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="36809-115">Kreisajā navigācijas rūtī izvērsiet sadaļu **Entītijas > Lomas cenas**.</span><span class="sxs-lookup"><span data-stu-id="36809-115">In Solution Explorer, on the left navigation pane, select **Entities > Role Price**.</span></span>
3. <span data-ttu-id="36809-116">Izvērsiet entītiju **Lomas cenas** un atlasiet vienumu **Lauki**.</span><span class="sxs-lookup"><span data-stu-id="36809-116">Expand the entity **Role Price** and select **Fields**.</span></span>
4. <span data-ttu-id="36809-117">Noklikšķiniet uz **Jauns** , lai izveidotu jaunu lauku ar nosaukumu **Resursa darba atrašanās vieta** un atlasiet vienumu **Opciju kopa** kā lauka tipu.</span><span class="sxs-lookup"><span data-stu-id="36809-117">Click **New** to create a new field called **Resource Work Location** and select **Option set** as the field type.</span></span> 
5. <span data-ttu-id="36809-118">Atlasiet **Lietot esošu opciju kopu** , atlasiet **Resursu darba atrašanās vieta** opciju kopu un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="36809-118">Select **Use an existing Option set** , select the **Resource Work Location** option set, and then click **Save**.</span></span>
6. <span data-ttu-id="36809-119">Atkārtojiet 1.–5. darbību, lai šo lauku pievienotu entītijai **Lomu cenas uzcenojumi**.</span><span class="sxs-lookup"><span data-stu-id="36809-119">Repeat steps 1 - 5 to add this field to the **Role Price Markup** entity.</span></span> 
7. <span data-ttu-id="36809-120">Atkārtojiet 1.–5. darbību opciju kopai **Resursu darba stundas**.</span><span class="sxs-lookup"><span data-stu-id="36809-120">Repeat steps 1 - 5 for the **Resource Work Hours** option set.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36809-121">Ja pievienojat lauku vairāk nekā vienai entītijai, izmantojiet vienu un to pašu lauka nosaukumu visās entītijās.</span><span class="sxs-lookup"><span data-stu-id="36809-121">When you add a field to more than one entity, use the same field name across all of the entities.</span></span> 

> ![Resursu darba atrašanās vietas pievienošana lomas cenai](media/RWL-Field.png)

<span data-ttu-id="36809-123">Projekta pārdošanas un novērtējuma fāzēs aprēķini par darba intensitāti, kas nepieciešams, lai pabeigtu **Vietēji** un **Uz vietas** darbu, kā arī **Regulārās stundās** un **Virsstundas** , tiek izmantotas, lai novērtētu piedāvājuma/projekta vērtību.</span><span class="sxs-lookup"><span data-stu-id="36809-123">In the sales and estimation phases for a project, estimates of the work effort that is required to complete **Local** and **Onsite** work, in **Regular hours** and **Overtime hours**  are used to estimate the value of the Quote/Project.</span></span> <span data-ttu-id="36809-124">Lauki **Resursa darba atrašanās vieta** un **Resursa darba stundas** tiek pievienoti novērtēšanas entītijām **Piedāvājumu rindu informācija** , **Līgumu rindu informācija** , **Projekta uzdevums** , **Projekta darba grupas dalībnieks** un **Novērtējuma rinda**.</span><span class="sxs-lookup"><span data-stu-id="36809-124">The fields **Resource Work Location** and **Resource Work Hours** will be added to the estimation entities, **Quote Line Detail** , **Contract Line detail** , **Project Task** , **Project Team Member** , and **Estimate Line**.</span></span>

1. <span data-ttu-id="36809-125">Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="36809-125">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="36809-126">Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Piedāvājuma rindu informācija**.</span><span class="sxs-lookup"><span data-stu-id="36809-126">In Solution Explorer, on the left navigation pane, select **Entities > Quote Line Detail**.</span></span>
3. <span data-ttu-id="36809-127">Izvērsiet entītiju **Piedāvājuma rindas** un atlasiet **Lauki**.</span><span class="sxs-lookup"><span data-stu-id="36809-127">Expand the **Quote Line Detail** entity, and select **Fields**.</span></span>
4. <span data-ttu-id="36809-128">Noklikšķiniet uz **Jauns** , lai izveidotu jaunu lauku ar nosaukumu **Resursa darba atrašanās vieta** un atlasiet **Opciju kopa** kā lauka tipu.</span><span class="sxs-lookup"><span data-stu-id="36809-128">Click **New** to create a new field called **Resource Work Location** and select the field type, **Option set**.</span></span> 
5. <span data-ttu-id="36809-129">Atlasiet **Izmantot esošu opciju kopu** un **Resursa darba atrašanās vieta** un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="36809-129">Select **Use an existing Option set** and **Resource Work Location** , and then click **Save**.</span></span>
6. <span data-ttu-id="36809-130">Atkārtojiet 1.–5. darbību, lai pievienotu šo lauku entītijām **Projekta līguma rindas informācija** , **Projekta uzdevums** , **Projekta darba grupas dalībnieks** un **Novērtējuma rinda**.</span><span class="sxs-lookup"><span data-stu-id="36809-130">Repeat steps 1 - 5 to add this field to the **Project Contract line detail** , **Project Task** , **Project Team Member** , and **Estimate Line** entities.</span></span>
7. <span data-ttu-id="36809-131">Atkārtojiet 1.–6. darbību opciju kopai **Resursa darba stundas**.</span><span class="sxs-lookup"><span data-stu-id="36809-131">Repeat steps 1 - 6 for the **Resource Work Hours** option set.</span></span> 

> ![Resursu darba atrašanās vietas pievienošana rindai Novērtējums](media/RWL-Default-Value.png)


<span data-ttu-id="36809-133">Piegādei un rēķinu izrakstīšanai pabeigtajam darbam ir precīzi jārēķinās, vai tas ir veikts **Vietēji** vai **Uz vietas** , kā arī to, vai tas ir pabeigts projekta faktiskajās **Regulārās stundas** laikā vai **Virsstundas**.</span><span class="sxs-lookup"><span data-stu-id="36809-133">For delivery and invoicing, completed work needs to be accurately priced to select whether it was performed **Local** or **Onsite** , and whether it was completed during **Regular hours** or **Overtime** on the Project Actuals.</span></span> <span data-ttu-id="36809-134">**Resursa darba atrašanās vieta** un **Resursa darba stundas** lauki jāpievieno entītijām **Laika ievade** , **Faktiski** , **Rēķina rindas informācija** un **Žurnāla rinda**.</span><span class="sxs-lookup"><span data-stu-id="36809-134">The **Resource Work Location** and **Resource Work hours** fields should be added to the **Time Entry** , **Actual** , **Invoice Line Detail** , and **Journal Line** entities.</span></span>

1. <span data-ttu-id="36809-135">Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="36809-135">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="36809-136">Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Laika ievade**.</span><span class="sxs-lookup"><span data-stu-id="36809-136">In Solution Explorer, on the left navigation pane, select  **Entities > Time Entry**.</span></span>
3. <span data-ttu-id="36809-137">Izvērsiet **Piedāvājuma rindas informācija** un atlasiet **Lauki**.</span><span class="sxs-lookup"><span data-stu-id="36809-137">Expand the **Quote Line Detail** entity, and then select **Fields**.</span></span>
4. <span data-ttu-id="36809-138">Noklikšķiniet uz **Jauns** , lai izveidotu jaunu lauku ar nosaukumu **Resursa darba atrašanās vieta** un atlasiet vienumu **Opciju kopa** kā lauka tipu.</span><span class="sxs-lookup"><span data-stu-id="36809-138">Click **New** to create a new field called **Resource Work Location** and select **Option set** as the field type.</span></span> 
5. <span data-ttu-id="36809-139">Atlasiet **Lietot esošu opciju kopu** , atlasiet **Resursu darba atrašanās vieta** opciju kopu un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="36809-139">Select **Use an existing Option set** , select the **Resource Work Location** option set, and then click **Save**.</span></span>
6. <span data-ttu-id="36809-140">Atkārtojiet 1.–5. darbību, lai o lauku pievienotu **Faktiski** , **Rēķina rindu informācija** un **Žurnāla rinda** entītijām.</span><span class="sxs-lookup"><span data-stu-id="36809-140">Repeat steps 1 - 5 to add this field to the **Actual** , **Invoice Line Detail** , and **Journal Line** entities.</span></span>
7. <span data-ttu-id="36809-141">Atkārtojiet 1.–6. darbību opciju kopai **Resursa darba stundas**.</span><span class="sxs-lookup"><span data-stu-id="36809-141">Repeat steps 1 - 6 for the **Resource Work Hours** option set.</span></span> 

> ![Resursu darba atrašanās vietas pievienošana laika ievadei](media/RWL-time-entry.png)

<span data-ttu-id="36809-143">Šādi tiek pabeigtas shēmas izmaiņas, kas nepieciešamas opciju kopas pielāgotām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="36809-143">This completes the schema changes required for option set-based custom dimensions.</span></span>

## <a name="entity-based-custom-pricing-dimensions"></a><span data-ttu-id="36809-144">Uz entītijām pamatotas opciju kopas pielāgotas cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="36809-144">Entity-based custom pricing dimensions</span></span>

<span data-ttu-id="36809-145">Ja pielāgotā cenu noteikšanas dimensija ir entītija, jūs pievienosit 1: N attiecības starp dimensiju entītiju un galvenajām Project Service entītijām.</span><span class="sxs-lookup"><span data-stu-id="36809-145">When the custom pricing dimension is an entity, you will add 1:N relationships between the dimension entity and key Project Service entities.</span></span> <span data-ttu-id="36809-146">Izmantojot iepriekš aprakstīto standarta nosaukuma piemēru, ir saprātīgi gaidīt, ka katram darbiniekam ir piešķirts standarta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="36809-146">Using the Standard Title example from above, it is reasonable to expect that each employee is assigned a standard title.</span></span> <span data-ttu-id="36809-147">SAs rezultātā ir nepieciešama 1: N attiecība no Standarta nosaukuma līdz Rezervētajam resursam vai N:1 attiecības, ja tas ir izveidots no Rezervētā resursa uz Standarta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="36809-147">SAs a result, you will need a 1:N relationship from Standard Title to Bookable Resource, or a N:1 relationship if it were created from Bookable Resource to Standard Title.</span></span>

1. <span data-ttu-id="36809-148">Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="36809-148">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="36809-149">Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="36809-149">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
3. <span data-ttu-id="36809-150">Izvērsiet **Standarta nosaukums** entītiju un atlasiet **1: N attiecības**.</span><span class="sxs-lookup"><span data-stu-id="36809-150">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
4. <span data-ttu-id="36809-151">Noklikšķiniet uz **Jauns** , lai veidotu jaunu 1:N attiecību, ko sauc **Standarta nosaukums rezervējamam resursam**.</span><span class="sxs-lookup"><span data-stu-id="36809-151">Click **New** to create a new 1:N relationship called **Standard Title to Bookable Resource**.</span></span> <span data-ttu-id="36809-152">Ievadiet pieprasīto informāciju un pēc tam noklikšķiniet uz vienuma **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="36809-152">Enter the required information, and then click **Save**.</span></span>

> ![Standarta nosaukuma kā atsauces lauka pievienošana rezervējamam resursam](media/ST-BR.png)

<span data-ttu-id="36809-154">Standarta nosaukums būs jāpievieno arī Project Service cenu noteikšanas entītijām **Lomas cena** un **Lomas cenas uzcenojums.**</span><span class="sxs-lookup"><span data-stu-id="36809-154">The Standard Title will also need to be added to Project Service Pricing entities, **Role Price** and **Role Price Markup**.</span></span> <span data-ttu-id="36809-155">Tas tiek pabeigts arī, izmantojot 1:N attiecības starp **Standarta nosaukums** un **Lomas cena** entītijām, kā arī **Standarta nosaukums** un **Lomas cenas uzcenojums**.</span><span class="sxs-lookup"><span data-stu-id="36809-155">This is also completed using 1:N relationships between the **Standard Title** and **Role Price** entities and **Standard Title** and **Role Price Markup** entities.</span></span>

1. <span data-ttu-id="36809-156">Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="36809-156">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
2. <span data-ttu-id="36809-157">Izvērsiet **Standarta nosaukums** entītiju un atlasiet **1: N attiecības**.</span><span class="sxs-lookup"><span data-stu-id="36809-157">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
3. <span data-ttu-id="36809-158">Noklikšķiniet uz **Jauns** , lai izveidotu jaunu 1:N attiecību, ko sauc par **Standarta nosaukums rezervētajam resursam**.</span><span class="sxs-lookup"><span data-stu-id="36809-158">Click **New** to create a new 1:N relationship called **Standard Title to Role Price**.</span></span> <span data-ttu-id="36809-159">Ievadiet pieprasīto informāciju un pēc tam noklikšķiniet uz vienuma **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="36809-159">Enter the required information, and then click **Save**.</span></span>
4. <span data-ttu-id="36809-160">Atkārtojiet 1.–4. darbību, lai izveidotu 1: N attiecību starp **Standarta nosaukums** un **Lomu cenas uzcenojums** entītijām,</span><span class="sxs-lookup"><span data-stu-id="36809-160">Repeat steps 1 - 4 to create 1:N relationships between the **Standard Title** and **Role Price Markup** entities,</span></span>

<span data-ttu-id="36809-161">Projekta pārdošanas un novērtēšanas fāzēs cenas piedāvājumam/projektam ir nepieciešami darba intensitātes aprēķini katram standarta nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="36809-161">In the sales and estimation phases for the project, to price the Quote/Project, estimates of the work effort are required for each standard title.</span></span> <span data-ttu-id="36809-162">Tas nozīmē, ka 1:N attiecības no Standarta nosaukums līdz katrai no šīm novērtēšanas entītijām pakalpojumā Project Service ir nepieciešamas:</span><span class="sxs-lookup"><span data-stu-id="36809-162">This means that 1:N relationships from Standard Title to each of these estimation entities in Project Service are needed:</span></span> 

- <span data-ttu-id="36809-163">**Piedāvājuma rindas informācija**</span><span class="sxs-lookup"><span data-stu-id="36809-163">**Quote line Detail**</span></span>
- <span data-ttu-id="36809-164">**Projekta līguma rindas informācija**</span><span class="sxs-lookup"><span data-stu-id="36809-164">**Project Contract Line Detail**</span></span>
- <span data-ttu-id="36809-165">**Projekta uzdevums**</span><span class="sxs-lookup"><span data-stu-id="36809-165">**Project Task**</span></span>
- <span data-ttu-id="36809-166">**Projekta grupas dalībnieks**</span><span class="sxs-lookup"><span data-stu-id="36809-166">**Project Team Member**</span></span>
- <span data-ttu-id="36809-167">**Novērtēšanas rinda**</span><span class="sxs-lookup"><span data-stu-id="36809-167">**Estimate Line**</span></span>

5. <span data-ttu-id="36809-168">Atkārtojiet 1.–5. darbību, lai izveidotu 1:N attiecības no **Standarta nosaukums** uz **Piedāvājuma rindas informācija** , **Projekta līguma rindas informācija** , **Projekta uzdevums** , **Projekta darba grupas dalībnieks** un **Novērtētā rinda**.</span><span class="sxs-lookup"><span data-stu-id="36809-168">Repeat steps 1 - 5 to create 1:N relationships from **Standard Title** to **Quote line Detail** , **Project Contract Line Detail** , **Project Task** , **Project Team Member** , and **Estimate Line**.</span></span>

> ![Standarta nosaukuma kā atsauces lauka pievienošana novērtētajai rindai](media/ST-Estimate-Line.png)

<span data-ttu-id="36809-170">Piegādes un rēķinu izrakstīšanas fāzēs darbam, kas pabeigts pēc katra standarta nosaukuma, ir precīzi jāatbilst projekta faktiskajām cenām.</span><span class="sxs-lookup"><span data-stu-id="36809-170">In the Delivery and Invoicing phases, the work completed by each standard title must be accurately priced on the Project Actuals.</span></span> <span data-ttu-id="36809-171">Tas nozīmē, ka ir jābūt 1: N attiecībām no **Standarta virsraksts** uz **Laika ievade** , **Faktiskie** , **Rēķina rindas informācija** un **Žurnāla rindas entītijas**.</span><span class="sxs-lookup"><span data-stu-id="36809-171">This means that there needs to be 1:N relationships from **Standard Title** to **Time Entry** , **Actual** , **Invoice Line Detail** , and **Journal Line entities**.</span></span>

6. <span data-ttu-id="36809-172">Atkārtojiet 1.–6. darbību, lai izveidotu 1: N attiecības no **Standarta virsraksts** uz **Laika ievade** , **Faktiskie** , **Rēķina rindas informācija** un **Žurnāla rindas entītijas**.</span><span class="sxs-lookup"><span data-stu-id="36809-172">Repeat steps 1 - 6 to create 1:N relationships from **Standard Title** to **Time Entry** , **Actual** , **Invoice Line Detail** , and **Journal Line entities**.</span></span>

> ![Standarta nosaukuma kā atsauces lauka pievienošana laika ievadei](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a><span data-ttu-id="36809-174">Dimensiju vērtību noklusējuma iestatīšana, izmantojot platformas kartēšanas līdzekļus</span><span class="sxs-lookup"><span data-stu-id="36809-174">Set up Dimension value defaulting using the mappings features of the platform</span></span>
<span data-ttu-id="36809-175">Laika ievadei būtu noderīgi, ja sistēmas būtu noklusējuma standarta ieraksts laika ievadē no rezervējamā resursa, kas reģistrē laika ierakstu.</span><span class="sxs-lookup"><span data-stu-id="36809-175">For Time Entry, it would be helpful to have the system default the standard title on the Time Entry from the Bookable Resource that is recording the time entry.</span></span> <span data-ttu-id="36809-176">Veiciet šīs darbības, lai pievienotu lauka kartējumus 1:N attiecībā no **Rezervējams resurss** uz **Laika ievade**.</span><span class="sxs-lookup"><span data-stu-id="36809-176">Use the following steps to add field mappings on the 1:N relationship from **Bookable Resource** to **Time Entry**.</span></span>

1. <span data-ttu-id="36809-177">Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Standarta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="36809-177">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
2. <span data-ttu-id="36809-178">Izvērsiet **Standarta nosaukums** entītiju un atlasiet **1: N attiecības**.</span><span class="sxs-lookup"><span data-stu-id="36809-178">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
3. <span data-ttu-id="36809-179">Veiciet dubultklikšķi uz **Rezervējams resurss uz Laika ievade**.</span><span class="sxs-lookup"><span data-stu-id="36809-179">Double-click **Bookable Resource to Time Entry**.</span></span> <span data-ttu-id="36809-180">Lapā **Attiecības** noklikšķiniet uz **Izmantot lauku kartējumus.**</span><span class="sxs-lookup"><span data-stu-id="36809-180">On the **Relationship** page, click **Use Field mappings**.</span></span> 
4. <span data-ttu-id="36809-181">Noklikšķiniet uz **Jauns** , lai izveidotu jaunu lauka kartēšanu starp lauku **Standarta nosaukums** entītijā **Rezervējams resurss** atsauces laukā **Standarta nosaukums** lauka entītijā **Laika ievade**.</span><span class="sxs-lookup"><span data-stu-id="36809-181">Click **New** to create a new field mapping between the **Standard Title** field on the **Bookable Resource** entity to the **Standard Title** reference field on **Time Entry** entity.</span></span> 

> ![Iestatīšanas lauka kartēšana, lai standarta nosaukuma noklusējumu no Rezervējams resurss līdz Laika ievade](media/ST-Mapping2.png)


<span data-ttu-id="36809-183">Šādi tiek pabeigtas shēmas izmaiņas, kas nepieciešamas uz entītijām pamatotām pielāgotām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="36809-183">This completes the schema changes required for entity-based custom dimensions.</span></span>

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a><span data-ttu-id="36809-184">Pielāgoto lauku pievienošana veidlapām, skatiem un biznesa noteikumiem</span><span class="sxs-lookup"><span data-stu-id="36809-184">Add custom fields to forms, views, and business rules</span></span>

<span data-ttu-id="36809-185">Kad esat veicis visas nepieciešamās shēmas izmaiņas, nākamā darbība ir padarīt laukus redzamus lietotāja saskarnē, pievienojot laukus veidlapām un skatiem.</span><span class="sxs-lookup"><span data-stu-id="36809-185">After you have made all of the required schema changes, the next step is to make the fields visible in the UI by adding the fields to the forms and views.</span></span>

1. <span data-ttu-id="36809-186">Atveriet veidlapu vai skatu.</span><span class="sxs-lookup"><span data-stu-id="36809-186">Open the form or the view.</span></span> <span data-ttu-id="36809-187">Labajā navigācijas rūtī atlasiet lauku un velciet to uz veidlapu kanvu.</span><span class="sxs-lookup"><span data-stu-id="36809-187">On the right navigation pane, select the field and drag it on to the form canvas.</span></span> 
2. <span data-ttu-id="36809-188">Ja rediģējat skatu, izmantojiet navigācijas rūti, noklikšķiniet uz **Pievienot laukus** un dialoglodziņā **Lauku saraksts** atlasiet vajadzīgos laukus un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="36809-188">If you are editing a view, use the right navigation pane, click **Add fields** , and in the **Field listing** dialog box, select the fields that you need and click **Ok**.</span></span>

<span data-ttu-id="36809-189">Tālāk sniegtajā tabulā ir sniegts visaptverošs formātu un skatu saraksts pa entītijām, kas būs jāatjaunina ar jaunajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="36809-189">The following table provides a comprehensive list of out-of-the-box forms and views, by entity, that will need to be updated with the new fields.</span></span> <span data-ttu-id="36809-190">Ja šajās entītijās pielāgojumos ir papildu skati vai veidlapas, pievienojiet arī jaunus laukus.</span><span class="sxs-lookup"><span data-stu-id="36809-190">If you have any additional views or forms in your customizations on these entities, add the new fields to those as well.</span></span>

| <span data-ttu-id="36809-191">Project Service entītijas</span><span class="sxs-lookup"><span data-stu-id="36809-191">Project Service Entity</span></span>        | <span data-ttu-id="36809-192">Veidlapas, kurām ir vajadzīgs jauns lauks</span><span class="sxs-lookup"><span data-stu-id="36809-192">Forms that need the new field</span></span>   |<span data-ttu-id="36809-193">Skati, kuriem ir vajadzīgs jauns lauks</span><span class="sxs-lookup"><span data-stu-id="36809-193">Views that need the new field</span></span>      |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="36809-194">Lomas cena</span><span class="sxs-lookup"><span data-stu-id="36809-194">Role Price</span></span>|<span data-ttu-id="36809-195">• Informācija</span><span class="sxs-lookup"><span data-stu-id="36809-195">• Information</span></span> |<span data-ttu-id="36809-196">• Aktīvu resursu kategoriju cenas</span><span class="sxs-lookup"><span data-stu-id="36809-196">• Active Resource Category Prices</span></span><br> <span data-ttu-id="36809-197">• Ar resursu kategorijas cenu saistītais skats</span><span class="sxs-lookup"><span data-stu-id="36809-197">• Resource Category Price Associated View</span></span>|
|  <span data-ttu-id="36809-198">Lomas cenas uzcenojums</span><span class="sxs-lookup"><span data-stu-id="36809-198">Role Price Markup</span></span>|<span data-ttu-id="36809-199">• Informācija</span><span class="sxs-lookup"><span data-stu-id="36809-199">• Information</span></span>|<span data-ttu-id="36809-200">• Aktīvais lomas cenas uzcenojums</span><span class="sxs-lookup"><span data-stu-id="36809-200">• Active Role Price Markup</span></span><br><span data-ttu-id="36809-201">• Ar lomas cenas uzcenojumu saistītais skats</span><span class="sxs-lookup"><span data-stu-id="36809-201">• Role Price Markup Associated View</span></span>|
|  <span data-ttu-id="36809-202">Piedāvājuma rindas informācija</span><span class="sxs-lookup"><span data-stu-id="36809-202">Quote line detail</span></span>|<span data-ttu-id="36809-203">• Projekta informācija</span><span class="sxs-lookup"><span data-stu-id="36809-203">• Project Information</span></span><br><span data-ttu-id="36809-204">• Projekta ātrā izveidošana</span><span class="sxs-lookup"><span data-stu-id="36809-204">• Project Quick Create</span></span>|<span data-ttu-id="36809-205">• Aktīva piedāvājuma rindas papildinformācija</span><span class="sxs-lookup"><span data-stu-id="36809-205">• Active Quote Line Detail</span></span><br><span data-ttu-id="36809-206">Apvienota piedāvājuma rindas papildinformācija</span><span class="sxs-lookup"><span data-stu-id="36809-206">• Combined Quote Line Details</span></span><br><span data-ttu-id="36809-207">Piedāvājuma rindas papildinformācijas saistītais skats</span><span class="sxs-lookup"><span data-stu-id="36809-207">• Quote Line Detail associated view</span></span>|
|  <span data-ttu-id="36809-208">Projekta līguma rindas papildinformācija</span><span class="sxs-lookup"><span data-stu-id="36809-208">Project Contract line detail</span></span>|<span data-ttu-id="36809-209">• Projekta informācija</span><span class="sxs-lookup"><span data-stu-id="36809-209">• Project Information</span></span><br><span data-ttu-id="36809-210">• Projekta ātrā izveidošana</span><span class="sxs-lookup"><span data-stu-id="36809-210">• Project Quick Create</span></span>|<span data-ttu-id="36809-211">• Līguma rindas apvienotā informācija</span><span class="sxs-lookup"><span data-stu-id="36809-211">• Combined Contract Line Details</span></span><br><span data-ttu-id="36809-212">Aktīvās līguma rindas papildinformācija</span><span class="sxs-lookup"><span data-stu-id="36809-212">• Active Contract Line Details</span></span><br><span data-ttu-id="36809-213">• Līguma rindu informācijas saistītais skats</span><span class="sxs-lookup"><span data-stu-id="36809-213">• Contract Line Details Associated View</span></span>|
|  <span data-ttu-id="36809-214">Projekta uzdevums</span><span class="sxs-lookup"><span data-stu-id="36809-214">Project Task</span></span>|<span data-ttu-id="36809-215">• Informācija</span><span class="sxs-lookup"><span data-stu-id="36809-215">• Information</span></span><br><span data-ttu-id="36809-216">• Jauna veidlapa</span><span class="sxs-lookup"><span data-stu-id="36809-216">• New Form</span></span>||
|  <span data-ttu-id="36809-217">Projekta grupas dalībnieks</span><span class="sxs-lookup"><span data-stu-id="36809-217">Project Team Member</span></span>|<span data-ttu-id="36809-218">• Informācija</span><span class="sxs-lookup"><span data-stu-id="36809-218">• Information</span></span><br><span data-ttu-id="36809-219">• Jauna veidlapa</span><span class="sxs-lookup"><span data-stu-id="36809-219">• New Form</span></span>|<span data-ttu-id="36809-220">• Aktīvie projekta darba grupas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="36809-220">• Active Project Team Members</span></span><br><span data-ttu-id="36809-221">• Projekta darba grupas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="36809-221">• Project Team Members</span></span><br><span data-ttu-id="36809-222">• Projekta grupas dalībnieku saistītais skats</span><span class="sxs-lookup"><span data-stu-id="36809-222">• Project Team members associated View</span></span>|
|  <span data-ttu-id="36809-223">Laika ieraksts</span><span class="sxs-lookup"><span data-stu-id="36809-223">Time Entry</span></span>|<span data-ttu-id="36809-224">• Informācija</span><span class="sxs-lookup"><span data-stu-id="36809-224">• Information</span></span><br><span data-ttu-id="36809-225">• Laika ieraksta izveide</span><span class="sxs-lookup"><span data-stu-id="36809-225">• Create Time Entry</span></span>|<span data-ttu-id="36809-226">• Mani laika ieraksti pēc datuma</span><span class="sxs-lookup"><span data-stu-id="36809-226">• My Time Entries By Date</span></span><br><span data-ttu-id="36809-227">• Mani laika ieraksti šajā nedēļā</span><span class="sxs-lookup"><span data-stu-id="36809-227">• My time Entries for this week</span></span><br><span data-ttu-id="36809-228">• Laika ieraksti apstiprināšanai</span><span class="sxs-lookup"><span data-stu-id="36809-228">• Time entries for approval</span></span>|
|  <span data-ttu-id="36809-229">Žurnāla rinda</span><span class="sxs-lookup"><span data-stu-id="36809-229">Journal Line</span></span>|<span data-ttu-id="36809-230">• Informācija</span><span class="sxs-lookup"><span data-stu-id="36809-230">• Information</span></span><br><span data-ttu-id="36809-231">• Ātrā izveide</span><span class="sxs-lookup"><span data-stu-id="36809-231">• Quick create</span></span>|<span data-ttu-id="36809-232">• Aktīvās žurnāla rindas</span><span class="sxs-lookup"><span data-stu-id="36809-232">• Active journal lines</span></span><br><span data-ttu-id="36809-233">• Žurnāla rindas saistītais skats</span><span class="sxs-lookup"><span data-stu-id="36809-233">• Journal Line associated view</span></span>|
|  <span data-ttu-id="36809-234">Rēķina rindas informācija</span><span class="sxs-lookup"><span data-stu-id="36809-234">Invoice Line Detail</span></span>|<span data-ttu-id="36809-235">• Informācija</span><span class="sxs-lookup"><span data-stu-id="36809-235">• Information</span></span><br><span data-ttu-id="36809-236">• Ātrā izveide</span><span class="sxs-lookup"><span data-stu-id="36809-236">• Quick create</span></span>|<span data-ttu-id="36809-237">• Aktīva rēķina rindas papildinformācija</span><span class="sxs-lookup"><span data-stu-id="36809-237">• Active Invoice Line Details</span></span><br><span data-ttu-id="36809-238">• Rēķinā iekļaujamas darbības</span><span class="sxs-lookup"><span data-stu-id="36809-238">• Chargeable Invoice Transactions</span></span><br><span data-ttu-id="36809-239">• Papildu rēķina darbības</span><span class="sxs-lookup"><span data-stu-id="36809-239">• Complimentary Invoice Transactions</span></span><br><span data-ttu-id="36809-240">• Rēķina rindas papildinformācijas saistītais skats</span><span class="sxs-lookup"><span data-stu-id="36809-240">• Invoice Line Detail associated view</span></span><br><span data-ttu-id="36809-241">• Rēķinā neiekļaujamas darbības</span><span class="sxs-lookup"><span data-stu-id="36809-241">• Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="36809-242">Faktiski</span><span class="sxs-lookup"><span data-stu-id="36809-242">Actual</span></span>|<span data-ttu-id="36809-243">• Informācija</span><span class="sxs-lookup"><span data-stu-id="36809-243">• Information</span></span><br><span data-ttu-id="36809-244">• Aktīvās faktiskās vērtības</span><span class="sxs-lookup"><span data-stu-id="36809-244">• Active Actuals</span></span>|<span data-ttu-id="36809-245">• Faktiskais saistītais skats</span><span class="sxs-lookup"><span data-stu-id="36809-245">• Actual Associated view</span></span>|

<span data-ttu-id="36809-246">Atkarībā no tā, ko esat definējis, biznesa noteikumiem, iespējams, būs jāpievieno arī pielāgoti lauki.</span><span class="sxs-lookup"><span data-stu-id="36809-246">Custom fields may also need to be added on business rules depending on what you have defined.</span></span> <span data-ttu-id="36809-247">Viens nepieejams piemērs ir biznesa noteikumam **Laika ievades rediģēšana, pamatojoties uz statusu**.</span><span class="sxs-lookup"><span data-stu-id="36809-247">One out-of-the-box example is for the business rule **Editability of Time Entry based on status**.</span></span> <span data-ttu-id="36809-248">Šī kārtula definē, kuri lauki ir jābloķē, ja laika ievade atrodas nerediģējamā statusā, piemēram, **Apstiprināta**.</span><span class="sxs-lookup"><span data-stu-id="36809-248">This rule defines which fields need to be locked when the Time Entry is in a non-editable status such as **Approved**.</span></span> <span data-ttu-id="36809-249">Pievienojiet laukus šai biznesa kārtulai tā, lai lauki tiktu bloķēti rediģēšanai, ja laika ievades statuss nav **Melnraksts** vai **Atgriezts**.</span><span class="sxs-lookup"><span data-stu-id="36809-249">Add fields to this business rule so that the fields are locked for editing when the Time Entry is in a status other than **Draft** or **Returned**.</span></span>