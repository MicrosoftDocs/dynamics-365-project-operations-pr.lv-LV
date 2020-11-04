---
title: Federālo apbalvojumu izmeklēšanas izdevumu plāns
description: Šajā tēmā ir sniegta informācija par Federālās balvas izmeklēšanas izdevumu plāna.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080428"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="32a1b-103">Federālo apbalvojumu izmeklēšanas izdevumu plāns</span><span class="sxs-lookup"><span data-stu-id="32a1b-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32a1b-104">Saskaņā ar Office pārvaldes un budžeta apkārtrakstu A-133 uz aģentūrām, kas saņem federālos līdzekļus, attiecas audita prasības, kuras arī sauc par atsevišķajiem auditiem.</span><span class="sxs-lookup"><span data-stu-id="32a1b-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="32a1b-105">Audita process tiek izmantots, lai regulāri ziņotu par federālo dotāciju ieņēmumiem un izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="32a1b-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="32a1b-106">Atsevišķā audita atskaites daļā ir iekļauts federālo apbalvojumu izdevumu plāns (SEFA).</span><span class="sxs-lookup"><span data-stu-id="32a1b-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="32a1b-107">Federālās balvas izmeklēšanas izdevumu plāns ietver Federālās iekšzemes palīdzības katalogu (CFDA) nosaukumu un numuru, dotācijas numuru, dotācijas gadu, federālās aģentūras nosaukumu, kas nodrošina līdzekļus, un caurlaides uzņēmuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="32a1b-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="32a1b-108">Izdevumi attiecas uz noteiktu periodu.</span><span class="sxs-lookup"><span data-stu-id="32a1b-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="32a1b-109">Parasti šis periods ir tāds pats kā finanšu pārskata periods, kas ir finanšu gads.</span><span class="sxs-lookup"><span data-stu-id="32a1b-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="32a1b-110">Izdevumos ir iekļautas dotācijas, kurām atlasītajā datumu diapazonā ir projekcijas datumi.</span><span class="sxs-lookup"><span data-stu-id="32a1b-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="32a1b-111">Izdevumu ailē **Dotētāja aģentūra** ir norādīts dotācijas klients vai caurlaides dotācijai — dotācijas aģentūra.</span><span class="sxs-lookup"><span data-stu-id="32a1b-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="32a1b-112">Attiecībā uz tiešo piešķīrumu ailē **Caurlaides aģentūra** tiek parādīts dotācijas klients.</span><span class="sxs-lookup"><span data-stu-id="32a1b-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="32a1b-113">Ja dotācija nav caurlaides dotācija, aile **Caurlaides aģentūra** ir tukša.</span><span class="sxs-lookup"><span data-stu-id="32a1b-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="32a1b-114">CFDA klasteru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="32a1b-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="32a1b-115">Ir jāiestata CFDA klasteri, kurus var saistīt ar CFDA numuriem Federālās apbalvošanas izrakstu plānā.</span><span class="sxs-lookup"><span data-stu-id="32a1b-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="32a1b-116">Dodieties uz **Projekta pārvaldība un uzskaite \> Iestatījumi \> Dotācijas \> Federālās iekšzemes palīdzības klasteru katalogs**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="32a1b-117">Lai izveidotu CFDA klasteri, atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="32a1b-118">Ievadiet klastera nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="32a1b-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="32a1b-119">Lai saglabātu izmaiņas, atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="32a1b-120">CFDA numuru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="32a1b-120">Set up CFDA numbers</span></span>

<span data-ttu-id="32a1b-121">Ir jāiestata CFDA numuri, kurus var pievienot dotācijām un iekļaut Federālo apbalvojumu izmeklēšanas izdevumu plānā.</span><span class="sxs-lookup"><span data-stu-id="32a1b-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="32a1b-122">Dodieties uz **Projekta pārvaldība un uzskaite \> Iestatījumi \> Dotācijas \> Federālās iekšzemes palīdzības numuru katalogs**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="32a1b-123">Lai izveidotu CFDA numuru, atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="32a1b-124">Ailē **Numurs** ievadiet CFDA numuru.</span><span class="sxs-lookup"><span data-stu-id="32a1b-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="32a1b-125">Nospiediet **tabulēšanas** taustiņu.</span><span class="sxs-lookup"><span data-stu-id="32a1b-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="32a1b-126">Ailē **Apraksts** ievadiet CFDA nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="32a1b-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="32a1b-127">Nospiediet **tabulēšanas** taustiņu.</span><span class="sxs-lookup"><span data-stu-id="32a1b-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="32a1b-128">Neobligāti: laukā **Programmas klasteris** pievienojiet atbilstošo CFDA klasteri.</span><span class="sxs-lookup"><span data-stu-id="32a1b-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="32a1b-129">Lai saglabātu izmaiņas, atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="32a1b-130">Dotāciju izveide, lai ziņotu par Federālo apbalvojumu izmeklēšanas izdevumu plānu</span><span class="sxs-lookup"><span data-stu-id="32a1b-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="32a1b-131">Dodieties uz **Projekta pārvaldība un uzskaite \> Dotācijas \> Dotācijas** un atlasiet esošu dotāciju.</span><span class="sxs-lookup"><span data-stu-id="32a1b-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="32a1b-132">Kopsavilkuma cilnē **Iestatīšana** , kas atrodas laukā **Federālās iekšzemes palīdzības numuru katalogs** , piešķiriet CFDA numuru.</span><span class="sxs-lookup"><span data-stu-id="32a1b-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="32a1b-133">CFDA numurs dotācijā nosaka CFDA klasteri atskaišu izveidei.</span><span class="sxs-lookup"><span data-stu-id="32a1b-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="32a1b-134">Kopsavilkuma cilnē **Kontaktpersonu informācija** ievadiet dotētāja informāciju, veicot šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="32a1b-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="32a1b-135">Laukā **Dotācijas klients** ievadiet klientu, kas ir atbildīgs par dotāciju.</span><span class="sxs-lookup"><span data-stu-id="32a1b-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="32a1b-136">Esošas dotācijas gadījumā šī informācija var jau būt ievadīta.</span><span class="sxs-lookup"><span data-stu-id="32a1b-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="32a1b-137">Norādiet, vai dotāciju klients ir finansētājs.</span><span class="sxs-lookup"><span data-stu-id="32a1b-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="32a1b-138">Ja dotāciju klients ir finansētājs, atstājiet izvēles rūtiņu **Caurlaide** tukšu.</span><span class="sxs-lookup"><span data-stu-id="32a1b-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="32a1b-139">Ja cits klients ir finansētājs un dotāciju klients ir atbildīgs par izmaksām un naudas izsekošanu, atzīmējiet izvēles rūtiņu **Caurlaide**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="32a1b-140">Ja iepriekšējā darbībā atzīmējāt izvēles rūtiņu **Caurlaide** , laukā **Dotētāja aģentūra** ievadiet klientu, kas nodrošināja šo dotāciju.</span><span class="sxs-lookup"><span data-stu-id="32a1b-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="32a1b-141">Dotētāja aģentūra un dotācijas klients nevar būt viens un tas pats klients.</span><span class="sxs-lookup"><span data-stu-id="32a1b-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="32a1b-142">Šeit ir caurlaides dotācijas piemērs:</span><span class="sxs-lookup"><span data-stu-id="32a1b-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="32a1b-143">Federālā valdība finansēja infrastruktūras projektu valstij.</span><span class="sxs-lookup"><span data-stu-id="32a1b-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="32a1b-144">Federālā valdība deva naudu valstij tērēt.</span><span class="sxs-lookup"><span data-stu-id="32a1b-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="32a1b-145">Šajā gadījumā federālā valdība ir dotētāja aģentūra, un valsts ir dotācijas klients.</span><span class="sxs-lookup"><span data-stu-id="32a1b-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="32a1b-146">Pirmoreiz ieslēdzot līdzekli, sākotnējie CFDA numuri tiks ievadīti, izmantojot piešķīrumos esošos numurus.</span><span class="sxs-lookup"><span data-stu-id="32a1b-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="32a1b-147">Neiekļaut dotācijas no SEFA atskaišu izveides, pamatojoties uz dotāciju tipu</span><span class="sxs-lookup"><span data-stu-id="32a1b-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="32a1b-148">Dodieties uz **Projekta pārvaldība un uzskaite \> Iestatījumi \> Dotācijas \> Dotācijas tipi**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="32a1b-149">Kopsavilkuma cilnē **Noklusējuma informācija** atzīmējiet izvēles rūtiņu **Neiekļaut federālo apbalvojumu izdevumu plānā**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="32a1b-150">Lai saglabātu izmaiņas, atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="32a1b-151">Federālo apbalvojumu izmeklēšanas izdevumu plāna palaišana</span><span class="sxs-lookup"><span data-stu-id="32a1b-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="32a1b-152">Dodieties uz **Projekta pārvaldība un uzskaite \> Pieprasījumi un atskaites \> Dotācijas pieprasījums \> Federālo apbalvojumu izdevumu plāns**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="32a1b-153">Sadaļā **Parametri** veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="32a1b-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="32a1b-154">Laukā **Datumu intervāls** atlasiet datumu intervāla kodu.</span><span class="sxs-lookup"><span data-stu-id="32a1b-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="32a1b-155">Vai arī laukos **Sākuma datums** un **Beigu datums** definējiet datuma intervālu.</span><span class="sxs-lookup"><span data-stu-id="32a1b-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="32a1b-156">Neobligāti: lai izmeklēšanā kā ieņēmumus iekļautu tikai darījumus ar rēķinu, iestatiet opciju **Iekļaut tikai rēķinu ieņēmumus** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="32a1b-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="32a1b-157">Kolonnas</span><span class="sxs-lookup"><span data-stu-id="32a1b-157">Columns</span></span>

<span data-ttu-id="32a1b-158">Federālo apbalvojumu izmeklēšanas izmaksu plānā ietver šādas kolonnas:</span><span class="sxs-lookup"><span data-stu-id="32a1b-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="32a1b-159">Federālā iekšzemes atbalsta klastera kataloga nosaukums</span><span class="sxs-lookup"><span data-stu-id="32a1b-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="32a1b-160">Dotētāja aģentūra</span><span class="sxs-lookup"><span data-stu-id="32a1b-160">Grantor agency</span></span>
- <span data-ttu-id="32a1b-161">Caurlaides aģentūra</span><span class="sxs-lookup"><span data-stu-id="32a1b-161">Pass-through agency</span></span>
- <span data-ttu-id="32a1b-162">Dotācijas nosaukums</span><span class="sxs-lookup"><span data-stu-id="32a1b-162">Grant name</span></span>
- <span data-ttu-id="32a1b-163">Dotācijas ID</span><span class="sxs-lookup"><span data-stu-id="32a1b-163">Grant ID</span></span>
- <span data-ttu-id="32a1b-164">Dotācijas programmas ID</span><span class="sxs-lookup"><span data-stu-id="32a1b-164">Grant application ID</span></span>
- <span data-ttu-id="32a1b-165">Federālā iekšzemes atbalsta katalogs</span><span class="sxs-lookup"><span data-stu-id="32a1b-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="32a1b-166">Apliecinājumi</span><span class="sxs-lookup"><span data-stu-id="32a1b-166">Receipts</span></span>
- <span data-ttu-id="32a1b-167">Izdevumi</span><span class="sxs-lookup"><span data-stu-id="32a1b-167">Expenditures</span></span>
