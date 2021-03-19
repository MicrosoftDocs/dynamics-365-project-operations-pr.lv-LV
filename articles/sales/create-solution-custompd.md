---
title: Risinājuma izveide pielāgotām cenu noteikšanas dimensijām
description: Šajā tēmā ir sniegta informācija par to, kā izveidot risinājumus pielāgotām cenu noteikšanas dimensijām.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278427"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="ca7cd-103">Risinājuma izveide pielāgotām cenu noteikšanas dimensijām</span><span class="sxs-lookup"><span data-stu-id="ca7cd-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="ca7cd-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="ca7cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="ca7cd-105">Visām pielāgoto cenu noteikšanas dimensiju izmaiņām jābūt atsevišķā risinājumā.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="ca7cd-106">Šī svarīgā paraugprakse nodrošina elastību, lai atjauninātu vai noņemtu nepieciešamās izmaiņas, tā arī palīdz atkārtoti izmantot darbu un vienkāršo izmaiņu saglabāšanu citās instancēs.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="ca7cd-107">Pēc nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldītu risinājumu** un pēc tam importējiet to citās instancēs atkārtotai izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="ca7cd-108">Risinājuma izveide pielāgotām cenu noteikšanas dimensijām</span><span class="sxs-lookup"><span data-stu-id="ca7cd-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="ca7cd-109">Izvēlieties **Iestatījumi** > **Risinājumi** un pēc tam atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="ca7cd-110">Piešķiriet risinājumam nosaukumu *<your organization name> cenu noteikšanas dimensijas*.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="ca7cd-111">Ievadiet pārējo pieprasīto informāciju un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Pielāgotas cenu noteikšanas dimensijas risinājuma izveide](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="ca7cd-113">Pievienojiet visas prasītās entītijas un ar tām saistītos komponentus cenu noteikšanas dimensijas risinājumam</span><span class="sxs-lookup"><span data-stu-id="ca7cd-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="ca7cd-114">Pievienojiet tālāk norādītās Project Service entītijas savam cenu noteikšanas risinājumam, lai veiktu svarīgas shēmas izmaiņas cenu noteikšanas risinājumā.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="ca7cd-115">Pēc procedūras pabeigšanas entītijas atpazīs jaunās cenu noteikšanas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="ca7cd-116">Atlasiet **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **<*Organizācijas nosaukums*> Cenu noteikšanas dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="ca7cd-117">Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Pievienot esošo** > **Entītijas**.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="ca7cd-118">Dialoglodziņā **Risinājumu sastāvdaļas** atlasiet vienu no šīm entītijām:</span><span class="sxs-lookup"><span data-stu-id="ca7cd-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="ca7cd-119">**Faktiski**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-119">**Actual**</span></span>
   - <span data-ttu-id="ca7cd-120">**Rezervējamais resurssss**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="ca7cd-121">**Novērtēšanas rinda**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-121">**Estimate Line**</span></span>
   - <span data-ttu-id="ca7cd-122">**Projekta uzdevums**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-122">**Project Task**</span></span>
   - <span data-ttu-id="ca7cd-123">**Rēķina rindas informācija**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="ca7cd-124">**Žurnāla rinda**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-124">**Journal Line**</span></span>
   - <span data-ttu-id="ca7cd-125">**Projekta līguma rindas informācija**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="ca7cd-126">**Projekta grupas dalībnieks**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-126">**Project Team Member**</span></span>
   - <span data-ttu-id="ca7cd-127">**Piedāvājuma rindas informācija**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="ca7cd-128">**Lomas cenas uzcenojums**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="ca7cd-129">**Lomas cena**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-129">**Role Price**</span></span>
   - <span data-ttu-id="ca7cd-130">**Laika ieraksts**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-130">**Time Entry**</span></span>
 
   ![Esošu entītiju pievienošana pielāgotu cenu noteikšanas dimensiju risinājumam](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="ca7cd-132">Katrai entītijai pārskatiet pievienojamos komponentus un entītiju līdzekļu galīgo sarakstu.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="ca7cd-133">Iekļaujiet visas veidlapas un skatus katrai atlasītajai entītijai.</span><span class="sxs-lookup"><span data-stu-id="ca7cd-133">Include all forms and views for each of the selected entities.</span></span>

  ![Pievienotās entītijas](./media/solution-component-selection.png)


5.  <span data-ttu-id="ca7cd-135">Kad tiek piedāvāts iekļaut jebkādas atlasīto entītiju atkarīgās entītijas, atlasiet **Nē, neiekļaut nepieciešamos komponentus.**</span><span class="sxs-lookup"><span data-stu-id="ca7cd-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Atkarīgo entītiju iekļaušana](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]