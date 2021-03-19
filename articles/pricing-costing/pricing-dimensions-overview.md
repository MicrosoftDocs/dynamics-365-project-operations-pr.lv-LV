---
title: Cenu noteikšanas dimensiju pārskats
description: Šajā tēmā ir sniegta informācija par cenu noteikšanas dimensijām risinājumā Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ff675823d84c6e2b83be1e313f881bd672e53981
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275412"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="14416-103">Cenu noteikšanas dimensiju pārskats</span><span class="sxs-lookup"><span data-stu-id="14416-103">Pricing dimensions overview</span></span>

<span data-ttu-id="14416-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="14416-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="14416-105">Dimensijas, kas tiek izmantotas cilvēkresursos, lai iestatītu cenu un izmaksu noteikšanu, ir iedalāmas divās tālāk norādītajās kategorijās.</span><span class="sxs-lookup"><span data-stu-id="14416-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="14416-106">Personas</span><span class="sxs-lookup"><span data-stu-id="14416-106">People</span></span>
- <span data-ttu-id="14416-107">Plānotais darbs</span><span class="sxs-lookup"><span data-stu-id="14416-107">Planned work</span></span>

<span data-ttu-id="14416-108">Šī iemesla dēļ ir pieejamas divu tālāk norādīto tipu cenu noteikšanas dimensiju vērtības:</span><span class="sxs-lookup"><span data-stu-id="14416-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="14416-109">**Opciju kopas**: Dimensijas, kas ir fiksēti uzskaitījumi kādai vērtību kopai.</span><span class="sxs-lookup"><span data-stu-id="14416-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="14416-110">**Uz entītiju balstītas vērtības**: Dimensijas, kas var būt dažādu vērtību kopa.</span><span class="sxs-lookup"><span data-stu-id="14416-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="14416-111">Cenu noteikšanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="14416-111">Pricing dimensions</span></span>

<span data-ttu-id="14416-112">Dynamics 365 Project Operations tiek piegādāta ar cenu noteikšanas dimensiju noklusējuma kopu.</span><span class="sxs-lookup"><span data-stu-id="14416-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="14416-113">Šīs cenrāžu dimensijas varat skatīt, dodoties uz **Project Operations** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="14416-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="14416-114">Parametra ierakstā, cilnē **Uz summu balstītas cenu noteikšanas dimensijas** pārliecinieties, ka lomai **msdyn_resourcecategory** un resursu organizācijas struktūrvienībai **msdyn_organizationalunit** lauki **Attiecināms uz pārdošanu** un **Attiecināms uz izmaksām** ir iestatīti uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="14416-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="14416-115">Ja šie lauki ir iespējoti, jūs varat iestatīt maksu un izmaksas katrai lomas un organizācijas vienības kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="14416-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![Project Service parametru ekrānuzņēmums ar izceltu lauku “Attiecināms uz pārdošanu”](media/PS-OOB-parameters.png)

<span data-ttu-id="14416-117">Ja resursu cenu vai izmaksu noteikšana ir jāveic, izmantojot papildu atribūtus, varat izveidot pielāgotus laukus, entītijas un dimensijas.</span><span class="sxs-lookup"><span data-stu-id="14416-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="14416-118">Papildinformāciju skatiet nākamajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="14416-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="14416-119">Procedūras ir jāaizpilda tādā secībā, kādā tās ir norādītas.</span><span class="sxs-lookup"><span data-stu-id="14416-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="14416-120">Risinājuma izveide pielāgotām cenu noteikšanas dimensijām</span><span class="sxs-lookup"><span data-stu-id="14416-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="14416-121">Pielāgotu lauku un entītiju izveide</span><span class="sxs-lookup"><span data-stu-id="14416-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="14416-122">Pielāgotu lauku pievienošana cenu iestatījumiem un transakciju entītijām </span><span class="sxs-lookup"><span data-stu-id="14416-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="14416-123">Pielāgotu lauku kā cenu kategoriju iestatīšana </span><span class="sxs-lookup"><span data-stu-id="14416-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="14416-124">Spraudņa atribūtu atjaunināšana, lai iekļautu jaunas cenu noteikšanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="14416-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="14416-125">Cilvēkresursu laika cenu noteikšana</span><span class="sxs-lookup"><span data-stu-id="14416-125">Pricing human resource time</span></span>
<span data-ttu-id="14416-126">Tas, kā organizācija nosaka cenu cilvēkresursu laikam, bieži vien ir nozīmīgs stratēģisks apsvērums, kas tieši ietekmē organizācijas ienesīgumu.</span><span class="sxs-lookup"><span data-stu-id="14416-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="14416-127">Sadarbojieties ar finanšu darba grupām un prakses līderiem, kad organizācija ir gatava noteikt veidu, kā tā vēlas iestatīt norēķinu un izmaksu likmes cilvēkresursu laikam.</span><span class="sxs-lookup"><span data-stu-id="14416-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="14416-128">Vēl viens apsvērums attiecībā uz cenu noteikšanu tostarp ir — vai atkārtoti izmantot laukus vai entītijas, kuras pašlaik nav cenu noteikšanas dimensijas, bet kuras ir attiecināmas kā cenu noteikšanas dimensijas jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="14416-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="14416-129">Tādi lauki kā **Transakcijas kategorija** (**msdyn_transactioncategory**) un **Rezervējams resurss** (**bookableresource**) ir kandidātdimensiju piemēri.</span><span class="sxs-lookup"><span data-stu-id="14416-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="14416-130">Ir jāņem vērā arī tas, vai cenu noteikšanas dimensijai ir jābūt tabulai vai opciju kopai.</span><span class="sxs-lookup"><span data-stu-id="14416-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="14416-131">Ja prognozējat, ka dimensiju vērtībām būs izmaiņas, kas pārsniedz 10 vai 12, un ja šīm vērtībām jums ir nepieciešami papildu atribūti, jūs varētu izveidot entītiju, nevis opciju kopu.</span><span class="sxs-lookup"><span data-stu-id="14416-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="14416-132">Lai uzturētu opciju kopu, piemēram, pievienotu vai noņemtu vērtības, ir nepieciešams administrators vai izstrādātājs, savukārt jaunu rindu pievienošanu tabulai var veikt vairums lietotāju.</span><span class="sxs-lookup"><span data-stu-id="14416-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="14416-133">Nākamajā piemērā ir parādītas norēķinu likmes, kas ir iestatītas, pamatojoties uz lomu un resursu organizācijas struktūrvienību, kurai šis resurss pieder.</span><span class="sxs-lookup"><span data-stu-id="14416-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="14416-134">Izmaksu likmes parasti ir balstītas uz darbinieka algas grupu un organizācijas struktūrvienību, kurai šis darbinieks pieder.</span><span class="sxs-lookup"><span data-stu-id="14416-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="14416-135">Šajā piemērā norēķinu likmju un izmaksu likmju tabulas izskatīsies šādi.</span><span class="sxs-lookup"><span data-stu-id="14416-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="14416-136">**Piemēra norēķinu likmes**</span><span class="sxs-lookup"><span data-stu-id="14416-136">**Sample bill rates**</span></span>

| <span data-ttu-id="14416-137">Loma</span><span class="sxs-lookup"><span data-stu-id="14416-137">Role</span></span>        | <span data-ttu-id="14416-138">Org. struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="14416-138">Org Unit</span></span>    |<span data-ttu-id="14416-139">Vienība</span><span class="sxs-lookup"><span data-stu-id="14416-139">Unit</span></span>      |<span data-ttu-id="14416-140">Cena</span><span class="sxs-lookup"><span data-stu-id="14416-140">Price</span></span>      |<span data-ttu-id="14416-141">Valūta</span><span class="sxs-lookup"><span data-stu-id="14416-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="14416-142">Izstrādātājiem</span><span class="sxs-lookup"><span data-stu-id="14416-142">Developer</span></span>   | <span data-ttu-id="14416-143">Contoso ASV</span><span class="sxs-lookup"><span data-stu-id="14416-143">Contoso US</span></span>  |<span data-ttu-id="14416-144">Hour</span><span class="sxs-lookup"><span data-stu-id="14416-144">Hour</span></span> | <span data-ttu-id="14416-145">200</span><span class="sxs-lookup"><span data-stu-id="14416-145">200</span></span>|<span data-ttu-id="14416-146">USD</span><span class="sxs-lookup"><span data-stu-id="14416-146">USD</span></span>     |
| <span data-ttu-id="14416-147">Izstrādātājiem</span><span class="sxs-lookup"><span data-stu-id="14416-147">Developer</span></span>   | <span data-ttu-id="14416-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="14416-148">Contoso India</span></span> |<span data-ttu-id="14416-149">Hour</span><span class="sxs-lookup"><span data-stu-id="14416-149">Hour</span></span>|   <span data-ttu-id="14416-150">112</span><span class="sxs-lookup"><span data-stu-id="14416-150">112</span></span>|<span data-ttu-id="14416-151">USD</span><span class="sxs-lookup"><span data-stu-id="14416-151">USD</span></span>     |


<span data-ttu-id="14416-152">**Piemēra izmaksu likmes**</span><span class="sxs-lookup"><span data-stu-id="14416-152">**Sample cost rates**</span></span>

| <span data-ttu-id="14416-153">Algu grupa</span><span class="sxs-lookup"><span data-stu-id="14416-153">Salary Band</span></span>     | <span data-ttu-id="14416-154">Org. struktūrvienība</span><span class="sxs-lookup"><span data-stu-id="14416-154">Org Unit</span></span>    |<span data-ttu-id="14416-155">Vienība</span><span class="sxs-lookup"><span data-stu-id="14416-155">Unit</span></span>      |<span data-ttu-id="14416-156">Cena</span><span class="sxs-lookup"><span data-stu-id="14416-156">Price</span></span>      |<span data-ttu-id="14416-157">Valūta</span><span class="sxs-lookup"><span data-stu-id="14416-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="14416-158">Mana company_Band1</span><span class="sxs-lookup"><span data-stu-id="14416-158">My company_Band1</span></span> | <span data-ttu-id="14416-159">Contoso ASV</span><span class="sxs-lookup"><span data-stu-id="14416-159">Contoso US</span></span>  |<span data-ttu-id="14416-160">Hour</span><span class="sxs-lookup"><span data-stu-id="14416-160">Hour</span></span> | <span data-ttu-id="14416-161">145</span><span class="sxs-lookup"><span data-stu-id="14416-161">145</span></span>|<span data-ttu-id="14416-162">USD</span><span class="sxs-lookup"><span data-stu-id="14416-162">USD</span></span>     |
| <span data-ttu-id="14416-163">Mana company_Band2</span><span class="sxs-lookup"><span data-stu-id="14416-163">My company_Band2</span></span> | <span data-ttu-id="14416-164">Contoso India</span><span class="sxs-lookup"><span data-stu-id="14416-164">Contoso India</span></span> |<span data-ttu-id="14416-165">Hour</span><span class="sxs-lookup"><span data-stu-id="14416-165">Hour</span></span>|   <span data-ttu-id="14416-166">67</span><span class="sxs-lookup"><span data-stu-id="14416-166">67</span></span>|<span data-ttu-id="14416-167">USD</span><span class="sxs-lookup"><span data-stu-id="14416-167">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]