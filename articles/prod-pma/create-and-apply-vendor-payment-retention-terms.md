---
title: Piegādātāja maksājuma saglabāšanas nosacījumu izveide un lietošana
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt un uzturēt saglabāšanas nosacījumus piegādātāju maksājumiem.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080581"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="2a134-103">Piegādātāja maksājuma saglabāšanas nosacījumu izveide un lietošana</span><span class="sxs-lookup"><span data-stu-id="2a134-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="2a134-104">Ja jūsu organizācija vēlas saglabāt daļu no piegādātājam veiktajiem maksājumiem, ir noderīgi iestatīt piegādātāja maksājumu saglabāšanas nosacījumus projektam.</span><span class="sxs-lookup"><span data-stu-id="2a134-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="2a134-105">Piemēram, ja vēlaties, lai maksājums piegādātājam tiktu aizturēts, līdz piegādātie produkti atbilst jūsu vēlmēm.</span><span class="sxs-lookup"><span data-stu-id="2a134-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="2a134-106">Piegādātāja maksājuma saglabāšanas nosacījumus var norādīt, vienojoties par piegādātāja līgumu.</span><span class="sxs-lookup"><span data-stu-id="2a134-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="2a134-107">Piegādātāja maksājuma saglabāšanas nosacījumu izveide</span><span class="sxs-lookup"><span data-stu-id="2a134-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="2a134-108">Var ievadīt procentuālo daļu, kas jāsaglabā no piegādātāja maksājuma, kā arī procentuālo daļu no iepriekš saglabātajām summām, kas jāizlaiž.</span><span class="sxs-lookup"><span data-stu-id="2a134-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="2a134-109">Summas tiek automātiski saglabātas piegādātāja rēķinos, līdz līgums sasniedz norādīto pabeigšanas statusu.</span><span class="sxs-lookup"><span data-stu-id="2a134-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="2a134-110">Kad esat iestatījis saglabāšanas nosacījumus, varat tos lietot jebkuram šī piegādātāja projektam.</span><span class="sxs-lookup"><span data-stu-id="2a134-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="2a134-111">Izmantojiet tālāk norādītās darbības, lai iestatītu un uzturētu piegādātāja maksājumu saglabāšanas nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="2a134-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="2a134-112">Atveriet **Projekta pārvaldības un grāmatvedības** > **Saglabāšana** > **Piegādātāja maksājumu saglabāšanas nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="2a134-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="2a134-113">Atlasiet **Jauns** , lai pievienotu jaunu piegādātāja saglabāšanas nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="2a134-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="2a134-114">Lauka **Kārtulas ID** vērtība jaunajam nosacījumam tiek ievadīta automātiski.</span><span class="sxs-lookup"><span data-stu-id="2a134-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="2a134-115">Laukā **Apraksts** ievadiet īsu aprakstu, bet FastTab cilnē **Nosacījumi** atlasiet **Pievienot rindu** , lai ievadītu nosacījuma vērtības tālāk minētajām opcijām.</span><span class="sxs-lookup"><span data-stu-id="2a134-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="2a134-116">**Piegādāto vienību procents** : ievadiet nosacījuma pabeigtības procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="2a134-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="2a134-117">Summas tiek automātiski saglabātas piegādātāja rēķinos, līdz projekta pabeigtības posms ir vienāds ar norādīto procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="2a134-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="2a134-118">Piemēram, ja ievadīsiet 50,00, summas tiek saglabātas, līdz projekta pabeigtība ir 50 procenti.</span><span class="sxs-lookup"><span data-stu-id="2a134-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="2a134-119">**Procentuālā vērtība, kas jāsaglabā** : ievadiet piegādātāja rēķina summas procentuālo vērtību, kas jāsaglabā.</span><span class="sxs-lookup"><span data-stu-id="2a134-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="2a134-120">Piemēram, ja ievadīsiet 10,00, tad 10 procenti no piegādātāja rēķina summas tiek saglabāti, līdz projekts sasniedz pabeigtības procentuālo vērtību, kas iestatīta laukā **Piegādāto vienību procentuālā vērtība**.</span><span class="sxs-lookup"><span data-stu-id="2a134-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="2a134-121">**Atbrīvošanas procentuālā vērtība** : atlasiet **Pievienot rindu** , lai ievadītu jebkuras iepriekš saglabātās summas procentuālo vērtību, kas ir jāatbrīvo atbilstoši atlasītajam projekta izpildes līmenim.</span><span class="sxs-lookup"><span data-stu-id="2a134-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="2a134-122">Ja jums ir vairāk nekā viens atskaites punkts dažādiem projekta pabeigšanas līmeņiem, ievadiet atsevišķu piegādātāja saglabāšanas nosacījuma rindu katrai saglabāšanas kārtulai.</span><span class="sxs-lookup"><span data-stu-id="2a134-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="2a134-123">Katrā rindā var norādīt citu saglabāšanas procentuālo vērtību un atšķirīgu atbrīvošanas procentuālo daļu katram piešķirtajam projekta pabeigšanas līmenim.</span><span class="sxs-lookup"><span data-stu-id="2a134-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="2a134-124">Kad esat izveidojis piegādātāja saglabāšanas nosacījumus, varat tos lietot projektam.</span><span class="sxs-lookup"><span data-stu-id="2a134-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="2a134-125">Piegādātāja saglabāšanas nosacījumu lietošana projektam</span><span class="sxs-lookup"><span data-stu-id="2a134-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="2a134-126">Atveriet **Projektu pārvaldība un grāmatvedība** > **Projekti** > **Visi projekti** un projektu saraksta lapā atveriet projektu.</span><span class="sxs-lookup"><span data-stu-id="2a134-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="2a134-127">Kopsavilkuma cilnē **Piegādātāju līgumi** atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="2a134-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="2a134-128">Laukā **Uzņēmuma kods** atlasiet vienu no tālāk minētajām opcijām.</span><span class="sxs-lookup"><span data-stu-id="2a134-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="2a134-129">**Tabula** : piegādātāja saglabāšanas nosacījumi attiecas uz vienu piegādātāju.</span><span class="sxs-lookup"><span data-stu-id="2a134-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="2a134-130">**Grupa** : piegādātāja saglabāšanas nosacījumi attiecas uz visiem grupā esošajiem piegādātājiem.</span><span class="sxs-lookup"><span data-stu-id="2a134-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="2a134-131">**Visi** : piegādātāju saglabāšanas nosacījumi attiecas uz visiem piegādātājiem.</span><span class="sxs-lookup"><span data-stu-id="2a134-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="2a134-132">Laukā **Piegādātājs/piegādātāju grupa** atlasiet piegādātāju vai piegādātāju grupu, uz kuru attiecas piegādātāju saglabāšanas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="2a134-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="2a134-133">Ja iepriekšējā darbībā atlasāt **Visi** , šis lauks nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="2a134-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="2a134-134">Laukā **Piegādātāju saglabāšanas nosacījumi** atlasiet saglabāšanas nosacījumus, ko izveidojāt iepriekšējā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="2a134-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="2a134-135">Ja projektā piegādātājam ir iestatīti arī maksāt-kad-apmaksāts (PWP) nosacījumi, ievadiet projekta sliekšņa procentuālo vērtību laukā **PWP sliekšņa procentuālā vērtība**.</span><span class="sxs-lookup"><span data-stu-id="2a134-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="2a134-136">Piegādātāja saglabāšanas nosacījumi tiek rādīti arī pirkšanas pasūtījumos, ko izveidojat šim piegādātājam.</span><span class="sxs-lookup"><span data-stu-id="2a134-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
