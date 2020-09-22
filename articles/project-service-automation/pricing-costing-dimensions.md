---
title: Cenu un izmaksu noteikšanas dimensiju sākumlapa
description: Šajā tēmā ir sniegts pārskats par cenu noteikšanas dimensijām.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753467"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="4bd96-103">Cenu un izmaksu noteikšanas dimensiju sākumlapa</span><span class="sxs-lookup"><span data-stu-id="4bd96-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="4bd96-104">Dimensijas, kas tiek izmantotas cilvēkresursos, lai iestatītu cenu un izmaksu noteikšanu, ir iedalāmas divās tālāk norādītajās kategorijās.</span><span class="sxs-lookup"><span data-stu-id="4bd96-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="4bd96-105">Personas</span><span class="sxs-lookup"><span data-stu-id="4bd96-105">People</span></span>
- <span data-ttu-id="4bd96-106">Plānotais darbs</span><span class="sxs-lookup"><span data-stu-id="4bd96-106">Planned work</span></span>

<span data-ttu-id="4bd96-107">Šī iemesla dēļ programmā Project Service Automation (PSA) ir pieejamas divu tālāk norādīto tipu cenu noteikšanas dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="4bd96-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="4bd96-108">**Opciju kopas** — dimensijas, kas ir fiksēti uzskaitījumi kādai vērtību kopai.</span><span class="sxs-lookup"><span data-stu-id="4bd96-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="4bd96-109">**Uz entītiju balstītas vērtības** — dimensijas, kas var būt dažādu vērtību kopa.</span><span class="sxs-lookup"><span data-stu-id="4bd96-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="4bd96-110">Cenu noteikšanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="4bd96-110">Pricing dimensions</span></span>

<span data-ttu-id="4bd96-111">Programma PSA tiek piegādāta ar cenu noteikšanas dimensiju noklusējuma kopu.</span><span class="sxs-lookup"><span data-stu-id="4bd96-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="4bd96-112">Šo sarakstu varat apskatīt, dodoties uz **Project Service** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="4bd96-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="4bd96-113">Parametra ierakstā, cilnē **Uz summu balstītas cenu noteikšanas dimensijas** pārliecinieties, ka lomai **msdyn_resourcecategory** un resursu organizācijas struktūrvienībai **msdyn_organizationalunit** lauki **Attiecināms uz pārdošanu** un **Attiecināms uz izmaksām** ir iestatīti uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4bd96-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="4bd96-114">Tas ļaus jums iestatīt cenas un izmaksas katrai lomas un organizācijas struktūrvienības kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="4bd96-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Project Service parametru ekrānuzņēmums ar izceltu lauku “Attiecināms uz pārdošanu”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="4bd96-116">Ja pirms PSA versijas 3 kā cenu noteikšanas dimensijas lietojāt lomas un organizācijas struktūrvienības standarta laukus, nekādas izmaiņas nebūs manāmas.</span><span class="sxs-lookup"><span data-stu-id="4bd96-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="4bd96-117">Varat turpināt lietot programmu Project Service kā parasti.</span><span class="sxs-lookup"><span data-stu-id="4bd96-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="4bd96-118">Ja resursu cenu vai izmaksu noteikšana ir jāveic, izmantojot papildu atribūtus, varat izveidot pielāgotus laukus, entītijas un dimensijas.</span><span class="sxs-lookup"><span data-stu-id="4bd96-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="4bd96-119">Lai iegūtu plašāku informāciju, skatiet tālāk norādītās tēmas, taču ņemiet vērā, ka šīs procedūras ir jāizpilda tālāk norādītajā secībā.</span><span class="sxs-lookup"><span data-stu-id="4bd96-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="4bd96-120">Pielāgotu lauku un entītiju izveidošana</span><span class="sxs-lookup"><span data-stu-id="4bd96-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="4bd96-121">Pielāgotu lauku pievienošana cenu iestatījumiem un transakciju entītijām</span><span class="sxs-lookup"><span data-stu-id="4bd96-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="4bd96-122">Pielāgotu lauku kā cenu noteikšanas dimensiju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4bd96-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="4bd96-123">Spraudņa atribūtu atjaunināšana, lai iekļautu jaunas cenu noteikšanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="4bd96-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="4bd96-124">Cilvēkresursu laika cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="4bd96-124">Pricing human resource time</span></span>
<span data-ttu-id="4bd96-125">Tas, kā organizācija nosaka cenu cilvēkresursu laikam, bieži vien ir nozīmīgs stratēģisks apsvērums, kas tieši ietekmē organizācijas ienesīgumu.</span><span class="sxs-lookup"><span data-stu-id="4bd96-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="4bd96-126">Sadarbojieties ar finanšu darba grupām un prakses līderiem, kad organizācija ir gatava noteikt veidu, kā tā vēlas iestatīt norēķinu un izmaksu likmes cilvēkresursu laikam.</span><span class="sxs-lookup"><span data-stu-id="4bd96-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="4bd96-127">Vēl viens apsvērums attiecībā uz cenu noteikšanu tostarp ir — vai atkārtoti izmantot laukus vai entītijas, kuras pašlaik nav cenu noteikšanas dimensijas, bet kuras ir attiecināmas kā cenu noteikšanas dimensijas jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="4bd96-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="4bd96-128">Tādi lauki kā **Transakcijas kategorija** (**msdyn_transactioncategory**) un **Rezervējams resurss** (**bookableresource**) ir kandidātdimensiju piemēri.</span><span class="sxs-lookup"><span data-stu-id="4bd96-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="4bd96-129">Tāpat ir jāņem vērā arī tas, vai cenu noteikšanas dimensijai ir jābūt tabulai vai opciju kopai.</span><span class="sxs-lookup"><span data-stu-id="4bd96-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="4bd96-130">Ja prognozējat, ka dimensiju vērtībām būs izmaiņas, kas pārsniedz 10 vai 12, un ja šīm vērtībām jums ir nepieciešami papildu atribūti, jūs varētu izveidot entītiju, nevis opciju kopu.</span><span class="sxs-lookup"><span data-stu-id="4bd96-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="4bd96-131">Lai uzturētu opciju kopu, piemēram, pievienotu vai noņemtu vērtības, ir nepieciešams administrators vai izstrādātājs, savukārt jaunu rindu pievienošanu tabulai var veikt vairums lietotāju.</span><span class="sxs-lookup"><span data-stu-id="4bd96-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="4bd96-132">Nākamajā piemērā ir parādītas norēķinu likmes, kas ir iestatītas, pamatojoties uz lomu un resursu organizācijas struktūrvienību, kurai šis resurss pieder.</span><span class="sxs-lookup"><span data-stu-id="4bd96-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="4bd96-133">Izmaksu likmes parasti ir balstītas uz darbinieka algas grupu un organizācijas struktūrvienību, kurai šis darbinieks pieder.</span><span class="sxs-lookup"><span data-stu-id="4bd96-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="4bd96-134">Šajā piemērā norēķinu likmju un izmaksu likmju tabulas izskatīsies šādi.</span><span class="sxs-lookup"><span data-stu-id="4bd96-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="4bd96-135">**Piemēra norēķinu likmes**</span><span class="sxs-lookup"><span data-stu-id="4bd96-135">**Sample bill rates**</span></span>

| <span data-ttu-id="4bd96-136">Loma</span><span class="sxs-lookup"><span data-stu-id="4bd96-136">Role</span></span>        | <span data-ttu-id="4bd96-137">Org. struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="4bd96-137">Org Unit</span></span>    |<span data-ttu-id="4bd96-138">Vienība</span><span class="sxs-lookup"><span data-stu-id="4bd96-138">Unit</span></span>      |<span data-ttu-id="4bd96-139">Cena</span><span class="sxs-lookup"><span data-stu-id="4bd96-139">Price</span></span>      |<span data-ttu-id="4bd96-140">Valūta</span><span class="sxs-lookup"><span data-stu-id="4bd96-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="4bd96-141">Izstrādātājiem</span><span class="sxs-lookup"><span data-stu-id="4bd96-141">Developer</span></span>   | <span data-ttu-id="4bd96-142">Contoso ASV</span><span class="sxs-lookup"><span data-stu-id="4bd96-142">Contoso US</span></span>  |<span data-ttu-id="4bd96-143">Hour</span><span class="sxs-lookup"><span data-stu-id="4bd96-143">Hour</span></span> | <span data-ttu-id="4bd96-144">200</span><span class="sxs-lookup"><span data-stu-id="4bd96-144">200</span></span>|<span data-ttu-id="4bd96-145">USD</span><span class="sxs-lookup"><span data-stu-id="4bd96-145">USD</span></span>     |
| <span data-ttu-id="4bd96-146">Izstrādātājiem</span><span class="sxs-lookup"><span data-stu-id="4bd96-146">Developer</span></span>   | <span data-ttu-id="4bd96-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="4bd96-147">Contoso India</span></span> |<span data-ttu-id="4bd96-148">Hour</span><span class="sxs-lookup"><span data-stu-id="4bd96-148">Hour</span></span>|   <span data-ttu-id="4bd96-149">112</span><span class="sxs-lookup"><span data-stu-id="4bd96-149">112</span></span>|<span data-ttu-id="4bd96-150">USD</span><span class="sxs-lookup"><span data-stu-id="4bd96-150">USD</span></span>     |


<span data-ttu-id="4bd96-151">**Piemēra izmaksu likmes**</span><span class="sxs-lookup"><span data-stu-id="4bd96-151">**Sample cost rates**</span></span>

| <span data-ttu-id="4bd96-152">Algu grupa</span><span class="sxs-lookup"><span data-stu-id="4bd96-152">Salary Band</span></span>     | <span data-ttu-id="4bd96-153">Org. struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="4bd96-153">Org Unit</span></span>    |<span data-ttu-id="4bd96-154">Vienība</span><span class="sxs-lookup"><span data-stu-id="4bd96-154">Unit</span></span>      |<span data-ttu-id="4bd96-155">Cena</span><span class="sxs-lookup"><span data-stu-id="4bd96-155">Price</span></span>      |<span data-ttu-id="4bd96-156">Valūta</span><span class="sxs-lookup"><span data-stu-id="4bd96-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="4bd96-157">Mana company_Band1</span><span class="sxs-lookup"><span data-stu-id="4bd96-157">My company_Band1</span></span> | <span data-ttu-id="4bd96-158">Contoso ASV</span><span class="sxs-lookup"><span data-stu-id="4bd96-158">Contoso US</span></span>  |<span data-ttu-id="4bd96-159">Hour</span><span class="sxs-lookup"><span data-stu-id="4bd96-159">Hour</span></span> | <span data-ttu-id="4bd96-160">145</span><span class="sxs-lookup"><span data-stu-id="4bd96-160">145</span></span>|<span data-ttu-id="4bd96-161">USD</span><span class="sxs-lookup"><span data-stu-id="4bd96-161">USD</span></span>     |
| <span data-ttu-id="4bd96-162">Mana company_Band2</span><span class="sxs-lookup"><span data-stu-id="4bd96-162">My company_Band2</span></span> | <span data-ttu-id="4bd96-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="4bd96-163">Contoso India</span></span> |<span data-ttu-id="4bd96-164">Hour</span><span class="sxs-lookup"><span data-stu-id="4bd96-164">Hour</span></span>|   <span data-ttu-id="4bd96-165">67</span><span class="sxs-lookup"><span data-stu-id="4bd96-165">67</span></span>|<span data-ttu-id="4bd96-166">USD</span><span class="sxs-lookup"><span data-stu-id="4bd96-166">USD</span></span>     |
