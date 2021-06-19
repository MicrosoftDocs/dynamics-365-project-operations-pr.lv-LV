---
title: Projekta līgumu projekta cenu sarakstu pārvaldīšana
description: Šajā tēmā ir sniegta informācija par projekta cenu sarakstu pārvaldību projekta līgumos.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010390"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="2f6c8-103">Projekta līgumu projekta cenu sarakstu pārvaldīšana</span><span class="sxs-lookup"><span data-stu-id="2f6c8-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="2f6c8-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="2f6c8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2f6c8-105">Projekta līgumi ar Dynamics 365 Project Operations ir paredzēti, lai atbalstītu vairākus aktuālus pārdošanas cenrāžus līgumā.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="2f6c8-106">Project Operations ir jauna saistīta entītija, ko sauc par **projekta cenrāžiem**.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="2f6c8-107">Šai entītijai ir relācija viens pret daudziem ar projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="2f6c8-108">Projekta cenrāži tiek izmantoti, lai projekta ietvaros izveidotu cenas, materiālu un izmaksu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="2f6c8-109">Ja līgumam ir viens vai vairāki projekta cenrāži, šie cenrāži tiek izmantoti, lai noteiktu cenas laiku, materiālus, izmaksu aprēķinus un faktiskos rezultātus projektos, kas ar līgumu saistīti, izmantojot līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-109">When a contract has one or more project price lists, these price lists are used to price for time, material, expense estimates, and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="2f6c8-110">Ja projekta līgumā nav projekta cenrāžu, tiks parādīts brīdinājuma ziņojums, ka projekta cenrāži nav pieejami un jūsu aprēķini, projekta faktiskais darbs, materiāli un reģistrēto izmaksu cena netiks veikta.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, material, and expenses logged will not be priced.</span></span> <span data-ttu-id="2f6c8-111">Pārdošanas vērtībām netiks noteikta cena.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="2f6c8-112">Projekta līgumā paredzētā projekta cenu saraksta saistīšana vai atsaistīšana</span><span class="sxs-lookup"><span data-stu-id="2f6c8-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a><span data-ttu-id="2f6c8-113">Izveidojiet vai saistiet noteiktu cenrādi, lai novērtētu projekta darbu, materiālus un izmaksas</span><span class="sxs-lookup"><span data-stu-id="2f6c8-113">Create or associate a specific price list for estimating project-based work, material, and expenses</span></span>

1. <span data-ttu-id="2f6c8-114">Projekta līgumā atlasiet cilni **Projekta cenrāži**.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="2f6c8-115">Apakšrežģī atlasiet **+ Pievienot jaunu projekta cenrādi**.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="2f6c8-116">Izmantojot **Ātrās izveides** slīdni, atlasiet cenrādi.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="2f6c8-117">Nolaižamajā sarakstā ir parādīti visi cenrāži, kam kontekstā ir iestatīta **Pārdošana**, ja cenrāža valūta atbilst līguma valūtai.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="2f6c8-118">Ievadiet projekta cenrāža sasaisti aprakstu, atlasiet **Saglabāt** un pēc tam aizveriet **Ātrās izveides** slīdni.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="2f6c8-119">Tiek izveidota projekta cenrāža sasaiste.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="2f6c8-120">Atkārtojiet 1.–4. darbību, lai projekta līgumam piesaistītu vairāk nekā vienu projekta cenrādi.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="2f6c8-121">Veidojiet vairākus projekta cenrāžus tikai tad, ja katram no saistītajam projekta cenrāžiem ir atšķirīgi darbības datumi.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="2f6c8-122">Project Operations neatbalsta projekta cenrāža darbības datumu pārklāšanos.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="2f6c8-123">Ja darbībai ar noteiktu datumu ir vairāki projekta cenrāži, šī transakcijas cena pēc noklusējuma tiks ņemta kā nulle.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="2f6c8-124">Projekta cenrāža saistību noņemšana</span><span class="sxs-lookup"><span data-stu-id="2f6c8-124">Remove a project price list association</span></span>

- <span data-ttu-id="2f6c8-125">Atlasiet projekta cenrādi un pēc tam apakšrežģī atlasiet **Dzēst līguma projekta cenrādi**.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="2f6c8-126">Cenrādis tiek noņemts no līguma projektu cenrāžiem.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="2f6c8-127">Pats cenrādis netiks izdzēsts.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="2f6c8-128">Tiks izdzēsts tikai saistījums ar līgumu.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="2f6c8-129">Projekta cenrāža automātiskā noklusējuma iestatīšana līgumā</span><span class="sxs-lookup"><span data-stu-id="2f6c8-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="2f6c8-130">Projekta cenrādi var iestatīt kā noklusējuma projekta cenrādi.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-130">A project price list can be set up as the default project price list.</span></span> <span data-ttu-id="2f6c8-131">Šī iestatīšana nodrošina, ka visi līgumi jūsu organizācijā vienmēr sākas ar standarta projekta cenrādi attiecīgajā cenrāža periodā.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-131">This setup ensures that all contracts in your organization always start with a standard project price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="2f6c8-132">Organizācijas noklusējuma projektu cenrāžu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="2f6c8-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="2f6c8-133">Atveriet sadaļu **Iestatījumi** > **Vispārīgi** un pēc tam atlasiet vienumu **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="2f6c8-134">Lai atvērtu ierakstu, saraksta lapā **Aktīvie parametri** atlasiet ierakstu un veiciet dubultklikšķi uz tā.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="2f6c8-135">Veicot dubultklikšķi, pārliecinieties, ka neklikšķināt uz lauka vērtības, kas ir hipersaite.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="2f6c8-136">Lapā **Aktīvie parametri** atlasiet cilni **Cenrādis**. Apakšrežģī redzams noklusējuma cenrāžu saraksts.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="2f6c8-137">Šis ir standarta izmaksu un pārdošanas cenrāžu saraksts.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="2f6c8-138">Ja **Pārdošanas** cenrādis šeit ir saistīts ar katru valūtu, kurā pārdodat, tiek nodrošināts, ka pārdošanas cenrādis ir noklusējuma cenrādis katram līgumam, ko izveidojat klientiem, kas veic transakcijas šajā valūtā.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="2f6c8-139">Klientam noteikta projekta cenrāža iestatīšana</span><span class="sxs-lookup"><span data-stu-id="2f6c8-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="2f6c8-140">Varat arī iestatīt klientam noteiktus projekta cenrāžus, kad esat pārrunājis ar klientiem vispārējo cenu noteikšanas līgumu.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="2f6c8-141">Dodieties uz **Pārdošana** > **Klienti**.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="2f6c8-142">Aktīvo uzņēmumu sarakstā atlasiet klientu, kuram ir īpašs cenrādis.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="2f6c8-143">Atlasiet klienta ierakstu, lai to atvērtu, un pēc tam atlasiet cilni **Projekta cenrāži**. Apakšrežģis rāda šim klientam noteikto projekta cenrāžu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="2f6c8-144">Šeit varat izveidot jaunu cenrāža saistību, lai šim klientam būtu noteikts projekta cenrādis.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="2f6c8-145">Cenas pielāgošana projekta līgumam</span><span class="sxs-lookup"><span data-stu-id="2f6c8-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="2f6c8-146">Kad ir izveidoti organizācijas un klientiem noteikti noklusējuma projektu cenrāži, jūsu projekta līgumi tiek automātiski izveidoti ar šīm projekta cenrāžu saistībām.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="2f6c8-147">Tomēr projekta līguma cenrāži, kas attiecas uz projekta līgumu, vienmēr tiek kopēti, norādot tiem pievienoto datumu un līguma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="2f6c8-148">Uzņēmums un projektu vadītāji pēc tam šajās kopijās var sākt labot cenas.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="2f6c8-149">Šīs mainītās cenas ir piemērojamas tikai šim projekta līgumam.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
