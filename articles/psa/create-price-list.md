---
title: Izveidojiet cenrādi
description: Cenrāža izveide programmā Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 18f6e7a7a96f374acc85ee1027c5252cbf7ab5f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149462"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="07a60-103">Cenrāža izveide (Project Service)</span><span class="sxs-lookup"><span data-stu-id="07a60-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="07a60-104">Cenrāži nodrošina veidni, kuru uzņēmumu pārvaldnieki var izmantot, lai izveidotu piedāvājumus un projektus un noteiktu projekta izmaksas.</span><span class="sxs-lookup"><span data-stu-id="07a60-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="07a60-105">Tie nodrošina lomu un izdevumu rindas elementu sarakstu un jūsu pieprasīto cenu.</span><span class="sxs-lookup"><span data-stu-id="07a60-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="07a60-106">Varat izveidot vairākus cenrāžus, lai uzturētu atsevišķas cenu struktūras dažādiem reģioniem, kuros pārdodat produktus, vai dažādiem pārdošanas kanāliem.</span><span class="sxs-lookup"><span data-stu-id="07a60-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="07a60-107">Ieteicams izveidot vismaz vienu cenrādi katrai valūtai, kuru paredzēts izmantot rēķinu izrakstīšanai klientiem.</span><span class="sxs-lookup"><span data-stu-id="07a60-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="07a60-108">Lai izveidotu tāmi veicamajam darbam, pārliecinieties, ka katram projektam ir dublēšanas izmaksu un pārdošanas cenu saraksts.</span><span class="sxs-lookup"><span data-stu-id="07a60-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="07a60-109">Izveidojiet noklusējuma izmaksu un pārdošanas cenrādi, kas attiecas uz visiem projektiem, kuri izveidoti jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="07a60-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="07a60-110">Cenrāži balstās uz lomām un izdevumu kategorijām, tāpēc, pirms veidojat cenrādi, pārliecinieties, ka jau esat konfigurējis lomas un izdevumu kategorijas, ko vēlaties izmantot, veidojot cenrādi.</span><span class="sxs-lookup"><span data-stu-id="07a60-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="07a60-111">Dodieties uz **Project Service > Cenrāži**.</span><span class="sxs-lookup"><span data-stu-id="07a60-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="07a60-112">Noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="07a60-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="07a60-113">Sadaļā **Konteksts** atlasiet, vai šis cenrādis ir vienumam **Izmaksas**, **Iegāde** vai **Pārdošana**.</span><span class="sxs-lookup"><span data-stu-id="07a60-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="07a60-114">Laukā **Nosaukums** ievadiet cenrāža nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="07a60-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="07a60-115">Laukā **Valūta** atlasiet valūtu, kuru izmantosiet rēķinu izrakstīšanai vai izmaksu grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="07a60-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="07a60-116">Laukā **Laika vienībā** norādiet laika periodu, uz kuru attiecas cena, piemēram, diena vai stunda.</span><span class="sxs-lookup"><span data-stu-id="07a60-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="07a60-117">Atbilstoši aizpildiet laukus **Sākuma datums**, **Beigu datums** un **Aapraksts**.</span><span class="sxs-lookup"><span data-stu-id="07a60-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="07a60-118">Noklikšķiniet uz **Saglabāt**, lai izveidotu ierakstu un pēc tam varētu veikt tā rediģēšanu.</span><span class="sxs-lookup"><span data-stu-id="07a60-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="07a60-119">Lai cenrādim pievienotu lomas cenu, noklikšķiniet uz **+** sadaļā **Lomu cenas**.</span><span class="sxs-lookup"><span data-stu-id="07a60-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="07a60-120">Rūtī **Lomas cena** aizpildiet datus un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="07a60-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="07a60-121">Ja nepieciešams, turpiniet pievienot lomu cenas.</span><span class="sxs-lookup"><span data-stu-id="07a60-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="07a60-122">Kad esat pabeidzis, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="07a60-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="07a60-123">Lai cenrādim pievienotu izdevumu kategoriju, noklikšķiniet uz **+** sadaļā **Kategoriju cenas**.</span><span class="sxs-lookup"><span data-stu-id="07a60-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="07a60-124">Rūtī **Transakcijas kategorijas cena** aizpildiet datus un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="07a60-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="07a60-125">Ja nepieciešams, turpiniet pievienot kategoriju cenas.</span><span class="sxs-lookup"><span data-stu-id="07a60-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="07a60-126">Kad esat pabeidzis, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="07a60-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="07a60-127">Lai cenrādim pievienotu cenrāža elementus, noklikšķiniet uz **+** sadaļā **Cenrāža elementi**.</span><span class="sxs-lookup"><span data-stu-id="07a60-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="07a60-128">Rūtī **Cenrāža elements** aizpildiet datus un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="07a60-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="07a60-129">Ja nepieciešams, turpiniet pievienot cenrāža elementus.</span><span class="sxs-lookup"><span data-stu-id="07a60-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="07a60-130">Kad esat pabeidzis, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="07a60-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="07a60-131">Lai cenrādim pievienotu teritoriju relācijas, noklikšķiniet uz **+** sadaļā **Teritoriju relācijas**.</span><span class="sxs-lookup"><span data-stu-id="07a60-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="07a60-132">Logā **Jauns savienojums** aizpildiet datus un pēc tam noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="07a60-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="07a60-133">Ja nepieciešams, turpiniet pievienot teritoriju relācijas.</span><span class="sxs-lookup"><span data-stu-id="07a60-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="07a60-134">Kad esat pabeidzis, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="07a60-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="07a60-135">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="07a60-135">See Also</span></span>  
 [<span data-ttu-id="07a60-136">Project Service Automation konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="07a60-136">Configure Project Service Automation</span></span>](../psa/configure.md)
