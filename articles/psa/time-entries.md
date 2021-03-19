---
title: Laika ierakstu izveide
description: Šajā tēmā ir sniegta informācija par to, kā izveidot laika ierakstus.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.openlocfilehash: 8f86f69090e869bf5e6a7505a4cb1ad1c69b475b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282162"
---
# <a name="create-time-entries"></a><span data-ttu-id="441c3-103">Laika ierakstu izveide</span><span class="sxs-lookup"><span data-stu-id="441c3-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="441c3-104">Dynamics 365 Project Service Automation iepriekšējās versijās laika ieraksti tika ievadīti katru nedēļu.</span><span class="sxs-lookup"><span data-stu-id="441c3-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="441c3-105">Programmas Project Service Automation 3. versijā laika ieraksti tiek ievadīti katru dienu.</span><span class="sxs-lookup"><span data-stu-id="441c3-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="441c3-106">Tomēr pēc dažu laika ierakstu izveidošanas tos var masveidā izveidot vai kopēt.</span><span class="sxs-lookup"><span data-stu-id="441c3-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="441c3-107">Laika ieraksta izveide</span><span class="sxs-lookup"><span data-stu-id="441c3-107">Create a time entry</span></span>

<span data-ttu-id="441c3-108">Lai izveidotu laika ierakstu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="441c3-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="441c3-109">Lapā **Laika ieraksti** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="441c3-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="441c3-110">Dialoglodziņā **Ātrā izveide: laika ieraksts**, ievadiet laika ieraksta ilgumu minūtēs, stundās vai dienās.</span><span class="sxs-lookup"><span data-stu-id="441c3-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="441c3-111">Ilgums ir jāievada šādā formātā: *x* minūtes, *x* stundas vai *x* dienas.</span><span class="sxs-lookup"><span data-stu-id="441c3-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="441c3-112">Stundas un dienas var ievadīt arī kā decimālās vērtības, piemēram, *x,x* stundas vai *x,x* dienas.</span><span class="sxs-lookup"><span data-stu-id="441c3-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="441c3-113">Atlasiet laika ieraksta tipu un projektu, kuram ievadāt laika ierakstu.</span><span class="sxs-lookup"><span data-stu-id="441c3-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="441c3-114">Laukā **Projekta uzdevums** atrodiet šī laika ieraksta uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="441c3-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="441c3-115">Ja izveidojat laika ierakstu uzdevumam, kas nav piešķirts lietotājam, laukā **Projekta uzdevums** atlasiet pogu **Meklēšana**, atlasiet **Mainīt skatu** un pēc tam atlasiet **Visus aktīvus projekta uzdevumus**, lai uzskaitītu visus uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="441c3-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="441c3-116">Ievadiet aprakstu, ja ir nepieciešams apraksts, un pēc tam atlasiet vienumu **Saglabāt un aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="441c3-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="441c3-117">Pēc laika ieraksta izveidošanas un saglabāšanas to var rediģēt laika ierakstu režģī.</span><span class="sxs-lookup"><span data-stu-id="441c3-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="441c3-118">Laika ierakstu režģī tiek atbalstīti divi formāti.</span><span class="sxs-lookup"><span data-stu-id="441c3-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="441c3-119">Laika ierakstus var ievadīt **ss: mm** formātā.</span><span class="sxs-lookup"><span data-stu-id="441c3-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="441c3-120">Šis formāts pēc tam tiek pārvērsts stundās un daļskaitļos.</span><span class="sxs-lookup"><span data-stu-id="441c3-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="441c3-121">Stundas un daļskaitļus var ievadīt tieši.</span><span class="sxs-lookup"><span data-stu-id="441c3-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="441c3-122">Ņemiet vērā, ka stundas daļskaitļi nav minūtes.</span><span class="sxs-lookup"><span data-stu-id="441c3-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="441c3-123">Tāpēc 1,5 stundas apzīmē 1 stundu un 30 minūtes.</span><span class="sxs-lookup"><span data-stu-id="441c3-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="441c3-124">Tas pats noteikums attiecas uz dienas daļskaitļiem.</span><span class="sxs-lookup"><span data-stu-id="441c3-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="441c3-125">Viena diena ir 24 stundas, un 0,5 dienas apzīmē 12 stundas.</span><span class="sxs-lookup"><span data-stu-id="441c3-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="441c3-126">Lielapjoma laika ierakstu izveide</span><span class="sxs-lookup"><span data-stu-id="441c3-126">Bulk create time entries</span></span>

<span data-ttu-id="441c3-127">Pēc dažu laika ierakstu izveides varat tos kopēt, lai izveidotu papildu lielapjoma laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="441c3-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="441c3-128">Lapā **Laika ieraksti** atlasiet **Kopēt nedēļu**.</span><span class="sxs-lookup"><span data-stu-id="441c3-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="441c3-129">Lauka grupā **No perioda**, laukos **Sākuma datums** un **Beigu datums**, definējiet datumu diapazonu, no kura kopēt laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="441c3-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="441c3-130">Lauka grupā **Līdz periodam**, laukā **Sākuma datums** norādiet datumu, kuram izveidot laika ierakstus.</span><span class="sxs-lookup"><span data-stu-id="441c3-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="441c3-131">Atlasiet **Kopēt**, lai izveidotu to laika ierakstu kopiju, kas atbilst tās nedēļas dienai, kura norādīta lauka grupā **Līdz periodam**.</span><span class="sxs-lookup"><span data-stu-id="441c3-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="441c3-132">Piemēram, pagājušās nedēļas pirmdienas laika ieraksts tiek kopēts uz tās nedēļas pirmdienu, kas norādīta lauka grupā **Līdz periodam**.</span><span class="sxs-lookup"><span data-stu-id="441c3-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="441c3-133">Datu importēšana laika ierakstiem</span><span class="sxs-lookup"><span data-stu-id="441c3-133">Import data for time entries</span></span>

<span data-ttu-id="441c3-134">Varat importēt datus no projektu rezervācijām un piešķirēm.</span><span class="sxs-lookup"><span data-stu-id="441c3-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="441c3-135">Importējot datus, var norādīt importējmo rezervāciju datumu diapazonu un pēc tam tieši atlasīt rezervācijas, kas jāizveido kā **Melnraksta** laika ieraksti.</span><span class="sxs-lookup"><span data-stu-id="441c3-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="441c3-136">Grupēšanas, kārtošanas, meklēšanas un filtrēšanas iespējas</span><span class="sxs-lookup"><span data-stu-id="441c3-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="441c3-137">Varat grupēt un filtrēt laika ierakstus pēc dimensijām, kas ir norādītas kolonnās.</span><span class="sxs-lookup"><span data-stu-id="441c3-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="441c3-138">Laukā **Grupēt pēc** atlasiet izmantojamo dimensiju laika ierakstu filtrēšanai.</span><span class="sxs-lookup"><span data-stu-id="441c3-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="441c3-139">Laika ierakstus var kārtot augošā vai dilstošā secībā, izmantojot kārtošanas bultiņu kolonnu virsrakstos.</span><span class="sxs-lookup"><span data-stu-id="441c3-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="441c3-140">Turklāt varat rādīt vai paslēpt ierakstus, atlasot pogu **Filtrēt** kolonnu virsrakstos un pēc tam lodziņā **Meklēšana** ievadīt tekstu, kas jālieto laika ierakstu meklēšanai pēc projekta nosaukuma, projekta uzdevuma, laika ieraksta vai resursa.</span><span class="sxs-lookup"><span data-stu-id="441c3-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]