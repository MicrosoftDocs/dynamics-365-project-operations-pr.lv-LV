---
title: Cenu un izmaksu noteikšanas dimensiju sākumlapa
description: Šajā tēmā ir sniegts pārskats par cenu noteikšanas dimensijām.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368890"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="505a0-103">Cenu un izmaksu noteikšanas dimensiju sākumlapa</span><span class="sxs-lookup"><span data-stu-id="505a0-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="505a0-104">Dimensijas, ko izmanto, lai iestatītu darbaspēka izcenojumu un izmaksu aprēķināšanu uz projektiem bāzētās organizācijās, ietekmē tālāk uzskaitītie atribūti.</span><span class="sxs-lookup"><span data-stu-id="505a0-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="505a0-105">Personas dara darbu, kas ir līdzīgs to pieredzei, lomai vai ģeogrāfijai</span><span class="sxs-lookup"><span data-stu-id="505a0-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="505a0-106">Darbs jāveic līdzīgi tā sarežģītībai vai diennakts laikam</span><span class="sxs-lookup"><span data-stu-id="505a0-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="505a0-107">Ņemot vērā šo darba atribūtu un darba veikšanai nepieciešamo darbinieku raksturīgās īpašības, platformā Project Service Automation ir pieejamas divu veidu izcenojuma dimensijas vērtības:</span><span class="sxs-lookup"><span data-stu-id="505a0-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="505a0-108">**Opciju kopas**: atribūti, kas ir fiksēti uzskaitījumi kādai vērtību kopai;</span><span class="sxs-lookup"><span data-stu-id="505a0-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="505a0-109">**Entītiju bāzes vērtības**: atribūti, kam var būt dažādi vērtību kopumi, kas ir ierobežoti, bet ar laiku var mainīties.</span><span class="sxs-lookup"><span data-stu-id="505a0-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="505a0-110">Cenu noteikšanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="505a0-110">Pricing dimensions</span></span>

<span data-ttu-id="505a0-111">Programma PSA tiek piegādāta ar cenu noteikšanas dimensiju noklusējuma kopu.</span><span class="sxs-lookup"><span data-stu-id="505a0-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="505a0-112">Šo sarakstu varat apskatīt, dodoties uz **Project Service** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="505a0-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="505a0-113">Parametra ierakstā, cilnē **Uz summu balstītas cenu noteikšanas dimensijas** pārliecinieties, ka lomai **msdyn_resourcecategory** un resursu organizācijas struktūrvienībai **msdyn_organizationalunit** lauki **Attiecināms uz pārdošanu** un **Attiecināms uz izmaksām** ir iestatīti uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="505a0-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="505a0-114">Tas ļaus jums iestatīt cenas un izmaksas katrai lomas un organizācijas struktūrvienības kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="505a0-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Project Service parametru ekrānuzņēmums ar izceltu lauku “Attiecināms uz pārdošanu”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="505a0-116">Ja pirms PSA versijas 3 kā cenu noteikšanas dimensijas lietojāt lomas un organizācijas struktūrvienības standarta laukus, nekādas izmaiņas nebūs manāmas.</span><span class="sxs-lookup"><span data-stu-id="505a0-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="505a0-117">Varat turpināt lietot programmu Project Service kā parasti.</span><span class="sxs-lookup"><span data-stu-id="505a0-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="505a0-118">Ja resursu cenu vai izmaksu noteikšana ir jāveic, izmantojot papildu atribūtus, varat izveidot pielāgotus laukus, entītijas un dimensijas.</span><span class="sxs-lookup"><span data-stu-id="505a0-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="505a0-119">Lai iegūtu plašāku informāciju, skatiet tālāk norādītās tēmas, taču ņemiet vērā, ka šīs procedūras ir jāizpilda tālāk norādītajā secībā.</span><span class="sxs-lookup"><span data-stu-id="505a0-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="505a0-120">Pielāgotu lauku un entītiju izveidošana</span><span class="sxs-lookup"><span data-stu-id="505a0-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="505a0-121">Pielāgotu lauku pievienošana cenu iestatījumiem un transakciju entītijām</span><span class="sxs-lookup"><span data-stu-id="505a0-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="505a0-122">Pielāgotu lauku kā cenu kategoriju iestatīšana </span><span class="sxs-lookup"><span data-stu-id="505a0-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="505a0-123">Spraudņa atribūtu atjaunināšana, lai iekļautu jaunas cenu noteikšanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="505a0-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="505a0-124">Cilvēkresursu laika cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="505a0-124">Pricing human resource time</span></span>
<span data-ttu-id="505a0-125">Tas, kā organizācija nosaka cenu cilvēkresursu laikam, bieži vien ir nozīmīgs stratēģisks apsvērums, kas tieši ietekmē organizācijas ienesīgumu.</span><span class="sxs-lookup"><span data-stu-id="505a0-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="505a0-126">Sadarbojieties ar finanšu darba grupām un prakses līderiem, kad organizācija ir gatava noteikt veidu, kā tā vēlas iestatīt norēķinu un izmaksu likmes cilvēkresursu laikam.</span><span class="sxs-lookup"><span data-stu-id="505a0-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="505a0-127">Vēl viens apsvērums attiecībā uz cenu noteikšanu tostarp ir — vai atkārtoti izmantot laukus vai entītijas, kuras pašlaik nav cenu noteikšanas dimensijas, bet kuras ir attiecināmas kā cenu noteikšanas dimensijas jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="505a0-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="505a0-128">Tādi lauki kā **Transakcijas kategorija** (**msdyn_transactioncategory**) un **Rezervējams resurss** (**bookableresource**) ir kandidātdimensiju piemēri.</span><span class="sxs-lookup"><span data-stu-id="505a0-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="505a0-129">Ir jāņem vērā arī tas, vai cenu noteikšanas dimensijai ir jābūt tabulai vai opciju kopai.</span><span class="sxs-lookup"><span data-stu-id="505a0-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="505a0-130">Ja prognozējat, ka dimensiju vērtībām būs izmaiņas, kas pārsniedz 10 vai 12, un ja šīm vērtībām jums ir nepieciešami papildu atribūti, izveidojiet entītiju, nevis opciju kopu.</span><span class="sxs-lookup"><span data-stu-id="505a0-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="505a0-131">Lai uzturētu opciju kopu, piemēram, pievienotu vai noņemtu vērtības, ir nepieciešams administrators vai izstrādātājs, savukārt jaunu rindu pievienošanu tabulai var veikt vairums biznesa lietotāju.</span><span class="sxs-lookup"><span data-stu-id="505a0-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="505a0-132">Nākamajā piemērā ir parādītas norēķinu likmes, kas ir iestatītas, pamatojoties uz lomu un resursu organizācijas struktūrvienību, kurai šis resurss pieder.</span><span class="sxs-lookup"><span data-stu-id="505a0-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="505a0-133">Izmaksu likmes parasti ir balstītas uz darbinieka algas grupu un organizācijas struktūrvienību, kurai šis darbinieks pieder.</span><span class="sxs-lookup"><span data-stu-id="505a0-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="505a0-134">Šajā piemērā norēķinu likmju un izmaksu likmju tabulas izskatīsies šādi.</span><span class="sxs-lookup"><span data-stu-id="505a0-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="505a0-135">**Piemēra norēķinu likmes**</span><span class="sxs-lookup"><span data-stu-id="505a0-135">**Sample bill rates**</span></span>

| <span data-ttu-id="505a0-136">Loma</span><span class="sxs-lookup"><span data-stu-id="505a0-136">Role</span></span>        | <span data-ttu-id="505a0-137">Org. struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="505a0-137">Org Unit</span></span>    |<span data-ttu-id="505a0-138">Vienība</span><span class="sxs-lookup"><span data-stu-id="505a0-138">Unit</span></span>      |<span data-ttu-id="505a0-139">Cenrādis</span><span class="sxs-lookup"><span data-stu-id="505a0-139">Price</span></span>      |<span data-ttu-id="505a0-140">Valūta</span><span class="sxs-lookup"><span data-stu-id="505a0-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="505a0-141">Izstrādātājiem</span><span class="sxs-lookup"><span data-stu-id="505a0-141">Developer</span></span>   | <span data-ttu-id="505a0-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="505a0-142">Contoso US</span></span>  |<span data-ttu-id="505a0-143">stunda</span><span class="sxs-lookup"><span data-stu-id="505a0-143">Hour</span></span> | <span data-ttu-id="505a0-144">200</span><span class="sxs-lookup"><span data-stu-id="505a0-144">200</span></span>|<span data-ttu-id="505a0-145">USD</span><span class="sxs-lookup"><span data-stu-id="505a0-145">USD</span></span>     |
| <span data-ttu-id="505a0-146">Izstrādātājiem</span><span class="sxs-lookup"><span data-stu-id="505a0-146">Developer</span></span>   | <span data-ttu-id="505a0-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="505a0-147">Contoso India</span></span> |<span data-ttu-id="505a0-148">stunda</span><span class="sxs-lookup"><span data-stu-id="505a0-148">Hour</span></span>|   <span data-ttu-id="505a0-149">112</span><span class="sxs-lookup"><span data-stu-id="505a0-149">112</span></span>|<span data-ttu-id="505a0-150">USD</span><span class="sxs-lookup"><span data-stu-id="505a0-150">USD</span></span>     |


<span data-ttu-id="505a0-151">**Piemēra izmaksu likmes**</span><span class="sxs-lookup"><span data-stu-id="505a0-151">**Sample cost rates**</span></span>

| <span data-ttu-id="505a0-152">Algu grupa</span><span class="sxs-lookup"><span data-stu-id="505a0-152">Salary Band</span></span>     | <span data-ttu-id="505a0-153">Org. struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="505a0-153">Org Unit</span></span>    |<span data-ttu-id="505a0-154">Vienība</span><span class="sxs-lookup"><span data-stu-id="505a0-154">Unit</span></span>      |<span data-ttu-id="505a0-155">Cenrādis</span><span class="sxs-lookup"><span data-stu-id="505a0-155">Price</span></span>      |<span data-ttu-id="505a0-156">Valūta</span><span class="sxs-lookup"><span data-stu-id="505a0-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="505a0-157">Mana company_Band1</span><span class="sxs-lookup"><span data-stu-id="505a0-157">My company_Band1</span></span> | <span data-ttu-id="505a0-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="505a0-158">Contoso US</span></span>  |<span data-ttu-id="505a0-159">stunda</span><span class="sxs-lookup"><span data-stu-id="505a0-159">Hour</span></span> | <span data-ttu-id="505a0-160">145</span><span class="sxs-lookup"><span data-stu-id="505a0-160">145</span></span>|<span data-ttu-id="505a0-161">USD</span><span class="sxs-lookup"><span data-stu-id="505a0-161">USD</span></span>     |
| <span data-ttu-id="505a0-162">Mana company_Band2</span><span class="sxs-lookup"><span data-stu-id="505a0-162">My company_Band2</span></span> | <span data-ttu-id="505a0-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="505a0-163">Contoso India</span></span> |<span data-ttu-id="505a0-164">stunda</span><span class="sxs-lookup"><span data-stu-id="505a0-164">Hour</span></span>|   <span data-ttu-id="505a0-165">67</span><span class="sxs-lookup"><span data-stu-id="505a0-165">67</span></span>|<span data-ttu-id="505a0-166">USD</span><span class="sxs-lookup"><span data-stu-id="505a0-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]