---
title: Projekta līgumu projekta cenu sarakstu pārvaldīšana
description: Šajā tēmā ir sniegta informācija par projekta cenu sarakstu pārvaldību projekta līgumos.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278607"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="8d2fd-103">Projekta līgumu projekta cenu sarakstu pārvaldīšana</span><span class="sxs-lookup"><span data-stu-id="8d2fd-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="8d2fd-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="8d2fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d2fd-105">Projekta līgumi ar Dynamics 365 Project Operations ir paredzēti, lai atbalstītu vairākus aktuālus pārdošanas cenrāžus līgumā.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="8d2fd-106">Project Operations ir jauna saistīta entītija, ko sauc par **projekta cenrāžiem**.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="8d2fd-107">Šai entītijai ir relācija viens pret daudziem ar projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="8d2fd-108">Projekta cenrāžus izmanto, lai noteiktu projekta laika un izdevumu darījumu cenas.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="8d2fd-109">Ja līgumam ir viens vai vairāki projekta cenrāži, šie cenrāži tiek lietoti, lai noteiktu laika un izdevumu aplēses un faktiskās vērtības projektiem, kas saistīti ar šo līgumu, izmantojot līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="8d2fd-110">Ja projekta līgumam nav projekta cenrāža, tiek parādīts brīdinājuma ziņojums par to, ka nav projekta cenrāžu, un jūsu aprēķiniem, faktiskajam projekta darbam un izdevumiem netiks noteiktas cenas.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="8d2fd-111">Pārdošanas vērtībām netiks noteikta cena.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="8d2fd-112">Projekta līgumā paredzētā projekta cenu saraksta saistīšana vai atsaistīšana</span><span class="sxs-lookup"><span data-stu-id="8d2fd-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="8d2fd-113">Izveidojiet vai saistiet noteiktu cenrādi, lai noteiktu uz projektiem balstītu darbu un izdevumus</span><span class="sxs-lookup"><span data-stu-id="8d2fd-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="8d2fd-114">Projekta līgumā atlasiet cilni **Projekta cenrāži**.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="8d2fd-115">Apakšrežģī atlasiet **+ Pievienot jaunu projekta cenrādi**.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="8d2fd-116">Izmantojot **Ātrās izveides** slīdni, atlasiet cenrādi.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="8d2fd-117">Nolaižamajā sarakstā ir parādīti visi cenrāži, kam kontekstā ir iestatīta **Pārdošana**, ja cenrāža valūta atbilst līguma valūtai.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="8d2fd-118">Ievadiet projekta cenrāža sasaisti aprakstu, atlasiet **Saglabāt** un pēc tam aizveriet **Ātrās izveides** slīdni.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="8d2fd-119">Tiek izveidota projekta cenrāža sasaiste.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="8d2fd-120">Atkārtojiet 1.–4. darbību, lai projekta līgumam piesaistītu vairāk nekā vienu projekta cenrādi.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="8d2fd-121">Veidojiet vairākus projekta cenrāžus tikai tad, ja katram no saistītajam projekta cenrāžiem ir atšķirīgi darbības datumi.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="8d2fd-122">Project Operations neatbalsta projekta cenrāža darbības datumu pārklāšanos.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="8d2fd-123">Ja darbībai ar noteiktu datumu ir vairāki projekta cenrāži, šī transakcijas cena pēc noklusējuma tiks ņemta kā nulle.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="8d2fd-124">Projekta cenrāža saistību noņemšana</span><span class="sxs-lookup"><span data-stu-id="8d2fd-124">Remove a project price list association</span></span>

- <span data-ttu-id="8d2fd-125">Atlasiet projekta cenrādi un pēc tam apakšrežģī atlasiet **Dzēst līguma projekta cenrādi**.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="8d2fd-126">Cenrādis tiek noņemts no līguma projektu cenrāžiem.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="8d2fd-127">Pats cenrādis netiks izdzēsts.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="8d2fd-128">Tiks izdzēsts tikai saistījums ar līgumu.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="8d2fd-129">Projekta cenrāža automātiskā noklusējuma iestatīšana līgumā</span><span class="sxs-lookup"><span data-stu-id="8d2fd-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="8d2fd-130">Projekta cenrādi var iestatīt kā projekta līguma noklusējuma sarakstu.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="8d2fd-131">Šis iestatījums var palīdzēt nodrošināt, ka visi jūsu organizācijas līgumi vienmēr tiek sākti ar attiecīgā cenu perioda standarta cenrādi.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="8d2fd-132">Organizācijas noklusējuma projektu cenrāžu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8d2fd-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="8d2fd-133">Atveriet sadaļu **Iestatījumi** > **Vispārīgi** un pēc tam atlasiet vienumu **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="8d2fd-134">Lai atvērtu ierakstu, saraksta lapā **Aktīvie parametri** atlasiet ierakstu un veiciet dubultklikšķi uz tā.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="8d2fd-135">Veicot dubultklikšķi, pārliecinieties, ka neklikšķināt uz lauka vērtības, kas ir hipersaite.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="8d2fd-136">Lapā **Aktīvie parametri** atlasiet cilni **Cenrādis**. Apakšrežģī redzams noklusējuma cenrāžu saraksts.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="8d2fd-137">Šis ir standarta izmaksu un pārdošanas cenrāžu saraksts.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="8d2fd-138">Ja **Pārdošanas** cenrādis šeit ir saistīts ar katru valūtu, kurā pārdodat, tiek nodrošināts, ka pārdošanas cenrādis ir noklusējuma cenrādis katram līgumam, ko izveidojat klientiem, kas veic transakcijas šajā valūtā.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="8d2fd-139">Klientam noteikta projekta cenrāža iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8d2fd-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="8d2fd-140">Varat arī iestatīt klientam noteiktus projekta cenrāžus, kad esat pārrunājis ar klientiem vispārējo cenu noteikšanas līgumu.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="8d2fd-141">Dodieties uz **Pārdošana** > **Klienti**.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="8d2fd-142">Aktīvo uzņēmumu sarakstā atlasiet klientu, kuram ir īpašs cenrādis.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="8d2fd-143">Atlasiet klienta ierakstu, lai to atvērtu, un pēc tam atlasiet cilni **Projekta cenrāži**. Apakšrežģis rāda šim klientam noteikto projekta cenrāžu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="8d2fd-144">Šeit varat izveidot jaunu cenrāža saistību, lai šim klientam būtu noteikts projekta cenrādis.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="8d2fd-145">Cenas pielāgošana projekta līgumam</span><span class="sxs-lookup"><span data-stu-id="8d2fd-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="8d2fd-146">Kad ir izveidoti organizācijas un klientiem noteikti noklusējuma projektu cenrāži, jūsu projekta līgumi tiek automātiski izveidoti ar šīm projekta cenrāžu saistībām.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="8d2fd-147">Tomēr projekta līguma cenrāži, kas attiecas uz projekta līgumu, vienmēr tiek kopēti, norādot tiem pievienoto datumu un līguma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="8d2fd-148">Uzņēmums un projektu vadītāji pēc tam šajās kopijās var sākt labot cenas.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="8d2fd-149">Šīs mainītās cenas ir piemērojamas tikai šim projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="8d2fd-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]