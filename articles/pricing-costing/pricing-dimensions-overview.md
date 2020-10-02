---
title: Cenu noteikšanas dimensiju pārskats
description: Šajā tēmā ir sniegta informācija par cenu noteikšanas dimensijām programmā Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898225"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="2590a-103">Cenu noteikšanas dimensiju pārskats</span><span class="sxs-lookup"><span data-stu-id="2590a-103">Pricing dimensions overview</span></span>

<span data-ttu-id="2590a-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="2590a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2590a-105">Dimensijas, kas tiek izmantotas cilvēkresursos, lai iestatītu cenu un izmaksu noteikšanu, ir iedalāmas divās tālāk norādītajās kategorijās.</span><span class="sxs-lookup"><span data-stu-id="2590a-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="2590a-106">Personas</span><span class="sxs-lookup"><span data-stu-id="2590a-106">People</span></span>
- <span data-ttu-id="2590a-107">Plānotais darbs</span><span class="sxs-lookup"><span data-stu-id="2590a-107">Planned work</span></span>

<span data-ttu-id="2590a-108">Šī iemesla dēļ ir pieejamas divu tālāk norādīto tipu cenu noteikšanas dimensiju vērtības:</span><span class="sxs-lookup"><span data-stu-id="2590a-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="2590a-109">**Opciju kopas**: Dimensijas, kas ir fiksēti uzskaitījumi kādai vērtību kopai.</span><span class="sxs-lookup"><span data-stu-id="2590a-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="2590a-110">**Uz entītiju balstītas vērtības**: Dimensijas, kas var būt dažādu vērtību kopa.</span><span class="sxs-lookup"><span data-stu-id="2590a-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="2590a-111">Cenu noteikšanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="2590a-111">Pricing dimensions</span></span>

<span data-ttu-id="2590a-112">Dynamics 365 Project Operations tiek piegādāta ar cenrāžu dimensiju noklusējuma kopu.</span><span class="sxs-lookup"><span data-stu-id="2590a-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="2590a-113">Šīs cenrāžu dimensijas varat skatīt, dodoties uz **Project Operations** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="2590a-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="2590a-114">Parametra ierakstā, cilnē **Uz summu balstītas cenu noteikšanas dimensijas** pārliecinieties, ka lomai **msdyn_resourcecategory** un resursu organizācijas struktūrvienībai **msdyn_organizationalunit** lauki **Attiecināms uz pārdošanu** un **Attiecināms uz izmaksām** ir iestatīti uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="2590a-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="2590a-115">Ja šie lauki ir iespējoti, jūs varat iestatīt maksu un izmaksas katrai lomas un organizācijas vienības kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="2590a-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="2590a-116">Ja resursu cenu vai izmaksu noteikšana ir jāveic, izmantojot papildu atribūtus, varat izveidot pielāgotus laukus, entītijas un dimensijas.</span><span class="sxs-lookup"><span data-stu-id="2590a-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="2590a-117">Cilvēkresursu laika cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="2590a-117">Pricing human resource time</span></span>
<span data-ttu-id="2590a-118">Tas, kā organizācija nosaka cenu cilvēkresursu laikam, bieži vien ir nozīmīgs stratēģisks apsvērums, kas tieši ietekmē organizācijas ienesīgumu.</span><span class="sxs-lookup"><span data-stu-id="2590a-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="2590a-119">Sadarbojieties ar finanšu darba grupām un prakses līderiem, kad organizācija ir gatava noteikt veidu, kā tā vēlas iestatīt norēķinu un izmaksu likmes cilvēkresursu laikam.</span><span class="sxs-lookup"><span data-stu-id="2590a-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="2590a-120">Vēl viens apsvērums attiecībā uz cenu noteikšanu tostarp ir — vai atkārtoti izmantot laukus vai entītijas, kuras pašlaik nav cenu noteikšanas dimensijas, bet kuras ir attiecināmas kā cenu noteikšanas dimensijas jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="2590a-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="2590a-121">Tādi lauki kā **Transakcijas kategorija** (**msdyn_transactioncategory**) un **Rezervējams resurss** (**bookableresource**) ir kandidātdimensiju piemēri.</span><span class="sxs-lookup"><span data-stu-id="2590a-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="2590a-122">Ir jāņem vērā arī tas, vai cenu noteikšanas dimensijai ir jābūt tabulai vai opciju kopai.</span><span class="sxs-lookup"><span data-stu-id="2590a-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="2590a-123">Ja prognozējat, ka dimensiju vērtībām būs izmaiņas, kas pārsniedz 10 vai 12, un ja šīm vērtībām jums ir nepieciešami papildu atribūti, jūs varētu izveidot entītiju, nevis opciju kopu.</span><span class="sxs-lookup"><span data-stu-id="2590a-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="2590a-124">Lai uzturētu opciju kopu, piemēram, pievienotu vai noņemtu vērtības, ir nepieciešams administrators vai izstrādātājs, savukārt jaunu rindu pievienošanu tabulai var veikt vairums lietotāju.</span><span class="sxs-lookup"><span data-stu-id="2590a-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="2590a-125">Nākamajā piemērā ir parādītas norēķinu likmes, kas ir iestatītas, pamatojoties uz lomu un resursu organizācijas struktūrvienību, kurai šis resurss pieder.</span><span class="sxs-lookup"><span data-stu-id="2590a-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="2590a-126">Izmaksu likmes parasti ir balstītas uz darbinieka algas grupu un organizācijas struktūrvienību, kurai šis darbinieks pieder.</span><span class="sxs-lookup"><span data-stu-id="2590a-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="2590a-127">Šajā piemērā norēķinu likmju un izmaksu likmju tabulas izskatīsies šādi.</span><span class="sxs-lookup"><span data-stu-id="2590a-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="2590a-128">**Piemēra norēķinu likmes**</span><span class="sxs-lookup"><span data-stu-id="2590a-128">**Sample bill rates**</span></span>

| <span data-ttu-id="2590a-129">Loma</span><span class="sxs-lookup"><span data-stu-id="2590a-129">Role</span></span>        | <span data-ttu-id="2590a-130">Org. struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="2590a-130">Org Unit</span></span>    |<span data-ttu-id="2590a-131">Vienība</span><span class="sxs-lookup"><span data-stu-id="2590a-131">Unit</span></span>      |<span data-ttu-id="2590a-132">Cena</span><span class="sxs-lookup"><span data-stu-id="2590a-132">Price</span></span>      |<span data-ttu-id="2590a-133">Valūta</span><span class="sxs-lookup"><span data-stu-id="2590a-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="2590a-134">Izstrādātājiem</span><span class="sxs-lookup"><span data-stu-id="2590a-134">Developer</span></span>   | <span data-ttu-id="2590a-135">Contoso ASV</span><span class="sxs-lookup"><span data-stu-id="2590a-135">Contoso US</span></span>  |<span data-ttu-id="2590a-136">Hour</span><span class="sxs-lookup"><span data-stu-id="2590a-136">Hour</span></span> | <span data-ttu-id="2590a-137">200</span><span class="sxs-lookup"><span data-stu-id="2590a-137">200</span></span>|<span data-ttu-id="2590a-138">USD</span><span class="sxs-lookup"><span data-stu-id="2590a-138">USD</span></span>     |
| <span data-ttu-id="2590a-139">Izstrādātājiem</span><span class="sxs-lookup"><span data-stu-id="2590a-139">Developer</span></span>   | <span data-ttu-id="2590a-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="2590a-140">Contoso India</span></span> |<span data-ttu-id="2590a-141">Hour</span><span class="sxs-lookup"><span data-stu-id="2590a-141">Hour</span></span>|   <span data-ttu-id="2590a-142">112</span><span class="sxs-lookup"><span data-stu-id="2590a-142">112</span></span>|<span data-ttu-id="2590a-143">USD</span><span class="sxs-lookup"><span data-stu-id="2590a-143">USD</span></span>     |


<span data-ttu-id="2590a-144">**Piemēra izmaksu likmes**</span><span class="sxs-lookup"><span data-stu-id="2590a-144">**Sample cost rates**</span></span>

| <span data-ttu-id="2590a-145">Algu grupa</span><span class="sxs-lookup"><span data-stu-id="2590a-145">Salary Band</span></span>     | <span data-ttu-id="2590a-146">Org. struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="2590a-146">Org Unit</span></span>    |<span data-ttu-id="2590a-147">Vienība</span><span class="sxs-lookup"><span data-stu-id="2590a-147">Unit</span></span>      |<span data-ttu-id="2590a-148">Cena</span><span class="sxs-lookup"><span data-stu-id="2590a-148">Price</span></span>      |<span data-ttu-id="2590a-149">Valūta</span><span class="sxs-lookup"><span data-stu-id="2590a-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="2590a-150">Mana company_Band1</span><span class="sxs-lookup"><span data-stu-id="2590a-150">My company_Band1</span></span> | <span data-ttu-id="2590a-151">Contoso ASV</span><span class="sxs-lookup"><span data-stu-id="2590a-151">Contoso US</span></span>  |<span data-ttu-id="2590a-152">Hour</span><span class="sxs-lookup"><span data-stu-id="2590a-152">Hour</span></span> | <span data-ttu-id="2590a-153">145</span><span class="sxs-lookup"><span data-stu-id="2590a-153">145</span></span>|<span data-ttu-id="2590a-154">USD</span><span class="sxs-lookup"><span data-stu-id="2590a-154">USD</span></span>     |
| <span data-ttu-id="2590a-155">Mana company_Band2</span><span class="sxs-lookup"><span data-stu-id="2590a-155">My company_Band2</span></span> | <span data-ttu-id="2590a-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="2590a-156">Contoso India</span></span> |<span data-ttu-id="2590a-157">Hour</span><span class="sxs-lookup"><span data-stu-id="2590a-157">Hour</span></span>|   <span data-ttu-id="2590a-158">67</span><span class="sxs-lookup"><span data-stu-id="2590a-158">67</span></span>|<span data-ttu-id="2590a-159">USD</span><span class="sxs-lookup"><span data-stu-id="2590a-159">USD</span></span>     |
