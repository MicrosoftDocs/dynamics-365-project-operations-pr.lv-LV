---
title: Izdevumu kategoriju iestatīšana
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt izdevumu kategorijas un kopīgotās kategorijas izdevumu atskaitēm.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080334"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="7a42b-103">Izdevumu kategoriju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7a42b-103">Set up expense categories</span></span>

<span data-ttu-id="7a42b-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="7a42b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7a42b-105">Kad darbinieki veido izdevumu atskaites, katram reģistrētajam izdevumu ierakstam ir jābūt saistītam ar izdevumu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="7a42b-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="7a42b-106">Izdevumu kategorijas ir atvasinātas no kopīgotām kategorijām, kuras var kopīgot organizācijas juridiskajās personās.</span><span class="sxs-lookup"><span data-stu-id="7a42b-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="7a42b-107">Atkarībā no tā, kā ir definēta jūsu organizācija, šīs izdevumu kategorijas var arī kopīgot citos apgabalos.</span><span class="sxs-lookup"><span data-stu-id="7a42b-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="7a42b-108">Pamatojoties uz jūsu organizācijas definīciju un ieviešanas darba grupas vadlīnijām, ir jānosaka, vai modulī Izdevumu pārvaldība lietotās kategorijas var izmantot tikai modulī Izmaksu pārvaldība vai arī tās var kopīgot citos apgabalos.</span><span class="sxs-lookup"><span data-stu-id="7a42b-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="7a42b-109">Šīs kategorijas var kopīgot projektu pārvaldībā un grāmatvedībā, kā arī izdevumu pārvaldībā vai arī projektu pārvaldībā un grāmatvedībā, kā arī ražošanā.</span><span class="sxs-lookup"><span data-stu-id="7a42b-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="7a42b-110">Taču tās nevar kopīgot izdevumu pārvaldībā un ražošanā.</span><span class="sxs-lookup"><span data-stu-id="7a42b-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="7a42b-111">Lai varētu sākt iestatīšanas procesu, ir jāpieņem šādi lēmumi attiecībā uz katru izdevumu kategoriju:</span><span class="sxs-lookup"><span data-stu-id="7a42b-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="7a42b-112">Kas ir izdevumu kategorija?</span><span class="sxs-lookup"><span data-stu-id="7a42b-112">What is the expense category?</span></span> <span data-ttu-id="7a42b-113">Var būt tādas kategorijas kā lidojumi, viesnīca vai nobraukums.</span><span class="sxs-lookup"><span data-stu-id="7a42b-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="7a42b-114">Vai izdevumu kategoriju var izmantot arī projektu pārvaldībā un grāmatvedībā?</span><span class="sxs-lookup"><span data-stu-id="7a42b-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="7a42b-115">Ja var, jums ir jāpieņem arī šādi lēmumi:</span><span class="sxs-lookup"><span data-stu-id="7a42b-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="7a42b-116">Kuri izmaksu konti tiks izmantoti tālāk norādītajiem izdevumiem?</span><span class="sxs-lookup"><span data-stu-id="7a42b-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="7a42b-117">izdevumi</span><span class="sxs-lookup"><span data-stu-id="7a42b-117">Cost</span></span>
        - <span data-ttu-id="7a42b-118">Algu sadalījums</span><span class="sxs-lookup"><span data-stu-id="7a42b-118">Payroll allocation</span></span>
        - <span data-ttu-id="7a42b-119">WIP-izmaksu vērtība</span><span class="sxs-lookup"><span data-stu-id="7a42b-119">WIP-cost value</span></span>
        - <span data-ttu-id="7a42b-120">Izmaksas-elements</span><span class="sxs-lookup"><span data-stu-id="7a42b-120">Cost-item</span></span>
        - <span data-ttu-id="7a42b-121">WIP-izmaksu vērtība-elements</span><span class="sxs-lookup"><span data-stu-id="7a42b-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="7a42b-122">Uzkrātie zaudējumi</span><span class="sxs-lookup"><span data-stu-id="7a42b-122">Accrued loss</span></span>
        - <span data-ttu-id="7a42b-123">WIP-uzkrātie zaudējumi</span><span class="sxs-lookup"><span data-stu-id="7a42b-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="7a42b-124">Kuri ieņēmumu konti tiks izmantoti tālāk norādītajiem ieņēmumu avotiem?</span><span class="sxs-lookup"><span data-stu-id="7a42b-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="7a42b-125">Ieņēmumi, par ko izrakstīts rēķins</span><span class="sxs-lookup"><span data-stu-id="7a42b-125">Invoiced revenue</span></span>
        - <span data-ttu-id="7a42b-126">Uzkrāto ieņēmumu-pārdošanas vērtība</span><span class="sxs-lookup"><span data-stu-id="7a42b-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="7a42b-127">WIP-pārdošanas vērtība</span><span class="sxs-lookup"><span data-stu-id="7a42b-127">WIP-sales value</span></span>
        - <span data-ttu-id="7a42b-128">Uzkrātie ieņēmumi-ražošana</span><span class="sxs-lookup"><span data-stu-id="7a42b-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="7a42b-129">WIP-ražošana</span><span class="sxs-lookup"><span data-stu-id="7a42b-129">WIP-production</span></span>
        - <span data-ttu-id="7a42b-130">Uzkrātie ieņēmumi-peļņa</span><span class="sxs-lookup"><span data-stu-id="7a42b-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="7a42b-131">WIP-peļņa</span><span class="sxs-lookup"><span data-stu-id="7a42b-131">WIP-profit</span></span>
        - <span data-ttu-id="7a42b-132">Uzkrātie ieņēmumi-abonēšana</span><span class="sxs-lookup"><span data-stu-id="7a42b-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="7a42b-133">WIP-abonēšana</span><span class="sxs-lookup"><span data-stu-id="7a42b-133">WIP-subscription</span></span>

- <span data-ttu-id="7a42b-134">Kāds ir izdevumu tips?</span><span class="sxs-lookup"><span data-stu-id="7a42b-134">What is the expense type?</span></span>
- <span data-ttu-id="7a42b-135">Kāda ir izdevumu kategorijas noklusējuma maksāšanas metode?</span><span class="sxs-lookup"><span data-stu-id="7a42b-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="7a42b-136">Vai izdevumu kategorijas izdevumi ir jāuzskaita?</span><span class="sxs-lookup"><span data-stu-id="7a42b-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="7a42b-137">Kas ir izdevumu kategorijas galvenais noklusējuma konts?</span><span class="sxs-lookup"><span data-stu-id="7a42b-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="7a42b-138">Kas ir izdevumu kategorijas noklusējuma krājumu PVN grupa?</span><span class="sxs-lookup"><span data-stu-id="7a42b-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="7a42b-139">Vai izdevumu kategorijai ir atļautas papildu maksāšanas metodes?</span><span class="sxs-lookup"><span data-stu-id="7a42b-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="7a42b-140">Ja ir atļautas, kādas?</span><span class="sxs-lookup"><span data-stu-id="7a42b-140">If so, what are they?</span></span>
- <span data-ttu-id="7a42b-141">Vai šajā izdevumu kategorijā ir apakškategorijas?</span><span class="sxs-lookup"><span data-stu-id="7a42b-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="7a42b-142">Ja ir apakškategorijas, jums ir jāpieņem arī šādi lēmumi:</span><span class="sxs-lookup"><span data-stu-id="7a42b-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="7a42b-143">Vai jebkura no apakškategorijām ir izslēgta no nodokļu atmaksas?</span><span class="sxs-lookup"><span data-stu-id="7a42b-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="7a42b-144">Kas ir apakškategoriju krājumu PVN grupa?</span><span class="sxs-lookup"><span data-stu-id="7a42b-144">What is the item sales tax group of the subcategories?</span></span>
