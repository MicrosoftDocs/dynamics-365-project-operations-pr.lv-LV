---
title: Resursu lietojamības pārskats
description: Šajā tēmā ir sniegta informācija par resursu lietojumu risinājumā Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401385"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="29238-103">Resursu lietojamības pārskats</span><span class="sxs-lookup"><span data-stu-id="29238-103">Resource utilization overview</span></span>

<span data-ttu-id="29238-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="29238-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="29238-105">Resursiem var būt mērķa apmaksājamā izmantošana.</span><span class="sxs-lookup"><span data-stu-id="29238-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="29238-106">Šī mērķa izmantošana tiek vai nu definēta kā atribūts resursa noklusējuma lomā, vai iestatīta atsevišķa rezervācijas resursa ierakstā.</span><span class="sxs-lookup"><span data-stu-id="29238-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="29238-107">Izmantošanas aprēķini ir balstīti uz faktiskajām stundām, par kurām resursi ir paziņojuši, izmantojot apstiprinātos laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="29238-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="29238-108">Izmantošanas aprēķināšanai lieto šādas formulas:</span><span class="sxs-lookup"><span data-stu-id="29238-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="29238-109">Apmaksājamā izmantošana = Rēķinā iekļaujamās stundas ÷ Resursa noslodze</span><span class="sxs-lookup"><span data-stu-id="29238-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="29238-110">Neapmaksājamā izmantošana = Faktiskais laiks ar norēķinu tipa ID = Rēķinā neiekļaujams, Papildu vai Nav pieejams ÷ Resursa noslodze</span><span class="sxs-lookup"><span data-stu-id="29238-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="29238-111">Iekšējs = Faktiskais laiks bez pārdošanas līguma ÷ Resursa noslodze</span><span class="sxs-lookup"><span data-stu-id="29238-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="29238-112">Resursa noslodze = Resursa darba stundas – Ārpus biroja – Brīvdienas</span><span class="sxs-lookup"><span data-stu-id="29238-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="29238-113">Skatu **Resursa izmantojums** var atrast rūtī **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="29238-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="29238-114">Katra režģa šūna norāda resursa apmaksājamās izmantošanas procentuālo vērtību periodā, piemēram, dienā, nedēļā vai mēnesī.</span><span class="sxs-lookup"><span data-stu-id="29238-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="29238-115">Šūnu iekrāsošanai lieto šādas formulas:</span><span class="sxs-lookup"><span data-stu-id="29238-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="29238-116">**Zaļa**: rēķinā iekļaujamais lietojums >= resursa mērķa lietojums</span><span class="sxs-lookup"><span data-stu-id="29238-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="29238-117">**Dzeltena**: mērķa lietojums – 20 <= rēķinā iekļaujamais lietojums < mērķa lietojums</span><span class="sxs-lookup"><span data-stu-id="29238-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="29238-118">**Sarkana**: rēķinā iekļaujamais lietojums < mērķa lietojums – 20</span><span class="sxs-lookup"><span data-stu-id="29238-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="29238-119">Tā kā skats **Apmaksājamā izmantošana** ir atkarīgs no plānošanas paneļa, varat izmantot plānošanas paneļa filtrēšanas iespējas, lai filtrētu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="29238-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="29238-120">Režģim ir jāiestata mērķa lietojums lomai vai atsevišķam resursam.</span><span class="sxs-lookup"><span data-stu-id="29238-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="29238-121">Lai veiktu šo iestatīšanu, atveriet **Resursi** > **Resursu lomas**.</span><span class="sxs-lookup"><span data-stu-id="29238-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="29238-122">Turklāt katram rezervējamajam resursam ir jāpiešķir noklusējuma loma.</span><span class="sxs-lookup"><span data-stu-id="29238-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="29238-123">Atveriet sadaļu **Resursi** > **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="29238-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="29238-124">Cilnē **Project Service** pārbaudiet, vai resursa loma ir definēta un vai laukā **Ir noklusējuma** ir iestatīta vērtība **Jā**.</span><span class="sxs-lookup"><span data-stu-id="29238-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="29238-125">Varat pievienot papildu lomas, kurām iestatīta opcija **Ir noklusējuma** = **Nē**.</span><span class="sxs-lookup"><span data-stu-id="29238-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="29238-126">Loma, kurai iestatīta opcija **Ir noklusējuma** = **Jā**, tiek izmantota, lai novērtētu resursa izmantojumu atbilstoši attiecīgās mērķim.</span><span class="sxs-lookup"><span data-stu-id="29238-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="29238-127">Cilnē **Project Service** resursam var iestatīt arī atsevišķu mērķa lietojumu.</span><span class="sxs-lookup"><span data-stu-id="29238-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="29238-128">Šādā gadījumā lietojuma aprēķinā tiek izmantots mērķa lietojums, lai novērtētu resursa mērķi, nevis resursa noklusējuma lomas mērķi.</span><span class="sxs-lookup"><span data-stu-id="29238-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="29238-129">Resursa lietojums tiek rādīts tikai tad, ja šis resurss ir apstiprinājis rēķinā iekļaujamu laiku periodā, kas ir norādīts režģī.</span><span class="sxs-lookup"><span data-stu-id="29238-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>