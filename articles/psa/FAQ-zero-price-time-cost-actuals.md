---
title: Kāpēc cena pēc noklusējuma ir nulle par faktiskajām laika izmaksām?
description: Novērsiet problēmu, kāpēc cena par faktiskajām laika izmaksām tiek pēc noklusējuma iestatīta uz 0.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 44d4952b77ac0a541cdf8e3e55f202c9209efdf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080463"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="cbad8-103">Kāpēc cena pēc noklusējuma ir nulle par faktiskajām laika izmaksām?</span><span class="sxs-lookup"><span data-stu-id="cbad8-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cbad8-104">Šis bieži uzdoto jautājumu raksts attiecas uz faktiskajām vērtībām, ja transakcijas klasei ir iestatīts vienums Laiks un transakcijas tipam ir atlasīts iestatījums Izmaksas.</span><span class="sxs-lookup"><span data-stu-id="cbad8-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="cbad8-105">Trīs tālāk norādītās pārbaudes darbības palīdzēs novērst problēmu, kāpēc faktisko izmaksu cena pēc noklusējuma tiek iestatīta uz 0.</span><span class="sxs-lookup"><span data-stu-id="cbad8-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="cbad8-106">1. pārbaude: nosakiet projekta izmaksu cenrādi</span><span class="sxs-lookup"><span data-stu-id="cbad8-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="cbad8-107">Atrodiet projektu, izmantojot faktisko izdevumu projekta lauku, un pēc tam pārejiet uz projekta lapu.</span><span class="sxs-lookup"><span data-stu-id="cbad8-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="cbad8-108">Noklikšķiniet uz līgumslēdzēja vienības saiti laukā.</span><span class="sxs-lookup"><span data-stu-id="cbad8-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="cbad8-109">Lapā Līgumslēdzēja vienība pārbaudiet, vai līgumslēdzējai vienībai ir cenrādis režģī Izmaksu cenrāži.</span><span class="sxs-lookup"><span data-stu-id="cbad8-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="cbad8-110">Ja ir vairāk nekā viens cenrādis, esat atradis problēmu.</span><span class="sxs-lookup"><span data-stu-id="cbad8-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="cbad8-111">Project Service atbalsta tikai vienu cenrādi katrai organizācijas vienībai.</span><span class="sxs-lookup"><span data-stu-id="cbad8-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="cbad8-112">Noņemiet visus cenrāžus šai entītijai, līdz organizācijas vienības režģī Cenrāžu saraksti ir pievienots tikai viens cenrādis.</span><span class="sxs-lookup"><span data-stu-id="cbad8-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="cbad8-113">Ja organizācijas vienībai nav pievienots neviens cenrādis, pierakstiet organizācijas vienības valūtu.</span><span class="sxs-lookup"><span data-stu-id="cbad8-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="cbad8-114">Atveriet pakalpojumu Project Service un pēc tam sadaļu Parametri un atveriet cilni Cenrāži. Pārbaudiet, vai pastāv cenrāži, kuru kontekstam ir iestatīta vērtība Izmaksas un kuru valūta atbilst organizācijas vienības valūtai.</span><span class="sxs-lookup"><span data-stu-id="cbad8-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="cbad8-115">Ja nav cenrāžu, kuri atbilst šiem kritērijiem, esat atradis problēmu.</span><span class="sxs-lookup"><span data-stu-id="cbad8-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="cbad8-116">Pārliecinieties, ka ir vismaz viens cenrādis, kura kontekstam ir iestatīta vērtība Izmaksas un kura valūta atbilst organizācijas vienības valūtai.</span><span class="sxs-lookup"><span data-stu-id="cbad8-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="cbad8-117">Ja ir vairāk nekā viens cenrādis, kas atbilst šādiem kritērijiem, turpiniet lasīt šo dokumentu, lai veiktu citas pārbaudes.</span><span class="sxs-lookup"><span data-stu-id="cbad8-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="cbad8-118">2. pārbaude: vai iepriekš minētie cenrāži ir derīgi faktisko laika izmaksu konkrētajam datumam?</span><span class="sxs-lookup"><span data-stu-id="cbad8-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="cbad8-119">Lai programmā Project Service cenrādis tiktu ņemts vērā noklusējuma cenas iestatīšanai, šim cenrādim ir jāatbilst faktisko laika izmaksu datumam.</span><span class="sxs-lookup"><span data-stu-id="cbad8-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="cbad8-120">Pārbaudiet šādus aspektus, lai pārliecinātos, vai iepriekš noteiktie cenrāži ir atbilstoši:</span><span class="sxs-lookup"><span data-stu-id="cbad8-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="cbad8-121">Pārbaudiet, vai pievienotajiem cenrāžiem ir aizpildīts sākuma un beigu datums cilnē Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="cbad8-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="cbad8-122">Ja iepriekš noteikto cenrāžu sākuma un beigu datums nav norādīts, esat atradis problēmu.</span><span class="sxs-lookup"><span data-stu-id="cbad8-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="cbad8-123">Pierakstiet faktisko laika izmaksu sākuma datumu un pārbaudiet, vai kāds no cenrāžiem atbilst šim datumam.</span><span class="sxs-lookup"><span data-stu-id="cbad8-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="cbad8-124">Piemēram, datumam faktiskajās laika izmaksās ir jāietilpst cenrāža sākuma vai beigu datumā.</span><span class="sxs-lookup"><span data-stu-id="cbad8-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="cbad8-125">Ja nav cenrāža, kas atbilst faktisko laika izmaksu datumam, esat atradis problēmu.</span><span class="sxs-lookup"><span data-stu-id="cbad8-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="cbad8-126">Mainiet cenrāža sākuma un beigu datumus, lai nodrošinātu, ka cenrādī ir ietverts faktisko laika izmaksu datums.</span><span class="sxs-lookup"><span data-stu-id="cbad8-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="cbad8-127">Ja faktisko laika izmaksu datumam atbilst vairāk nekā viens cenrādis, esat atradis problēmu.</span><span class="sxs-lookup"><span data-stu-id="cbad8-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="cbad8-128">To varat labot, rediģējot cenrāžu sākuma un beigu datumus, lai būtu tikai viens cenrādis, kas atbilst faktisko laika izmaksu datumam.</span><span class="sxs-lookup"><span data-stu-id="cbad8-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="cbad8-129">Ja ir tikai viens cenrādis, kas attiecas uz šo faktisko laika izmaksu datumu, pārejiet pie nākamās dokumentā aprakstītās pārbaudes.</span><span class="sxs-lookup"><span data-stu-id="cbad8-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="cbad8-130">Kad esat veicis nepieciešamos labojumus, vēlreiz izveidojiet laika ierakstu, apstipriniet to un pārbaudiet, vai faktiskajām laika izmaksām ir derīga cena.</span><span class="sxs-lookup"><span data-stu-id="cbad8-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="cbad8-131">3. pārbaude: vai cenrādī ir cena faktisko laika izmaksu izcenojuma dimensijām?</span><span class="sxs-lookup"><span data-stu-id="cbad8-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="cbad8-132">Ja esat veiksmīgi izpildījis 1. un 2. pārbaudi, jums ir jābūt tikai vienam cenrādim, kas atbilst faktisko laika izmaksu datumam.</span><span class="sxs-lookup"><span data-stu-id="cbad8-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="cbad8-133">Atveriet cenrādi un pārejiet uz cilni Lomu cenas. Pārliecinieties, ka faktisko laika izmaksu cenu dimensijām režģī ir rinda.</span><span class="sxs-lookup"><span data-stu-id="cbad8-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="cbad8-134">Ja faktisko laika izmaksu cenas dimensijām režģī nav rindas, esat atradis problēmu.</span><span class="sxs-lookup"><span data-stu-id="cbad8-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="cbad8-135">Lomu cenu režģī izveidojiet rindu faktisko laika izmaksu cenas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="cbad8-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="cbad8-136">Kad tas ir paveikts, vēlreiz izveidojiet laika ierakstu, apstipriniet to un pārbaudiet, vai faktiskajām laika izmaksām ir derīga cena.</span><span class="sxs-lookup"><span data-stu-id="cbad8-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="cbad8-137">Ja pēc trīs iepriekš minēto pārbaužu veikšanas joprojām neredzat derīgu cenu faktiskajām laika izmaksām, lūdzu, reģistrējiet atbalsta biļeti.</span><span class="sxs-lookup"><span data-stu-id="cbad8-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



