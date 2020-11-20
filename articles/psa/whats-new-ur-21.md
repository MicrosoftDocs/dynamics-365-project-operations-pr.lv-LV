---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 21, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126717"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="ad99f-103">Project Service Automation atjauninājumu izlaidums 21, V3</span><span class="sxs-lookup"><span data-stu-id="ad99f-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="ad99f-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="ad99f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ad99f-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="ad99f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ad99f-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="ad99f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ad99f-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="ad99f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ad99f-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ad99f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ad99f-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 21.</span><span class="sxs-lookup"><span data-stu-id="ad99f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="ad99f-110">Šīs versijas būvējuma numurs ir V 3.10.32.50, un tā ir vispārīgi pieejama, izmantojot 2020. gada jūnija pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="ad99f-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="ad99f-111">Atjauninājumu izlaidums 21</span><span class="sxs-lookup"><span data-stu-id="ad99f-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ad99f-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="ad99f-112">Bug fixes</span></span>

<span data-ttu-id="ad99f-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="ad99f-113">**Time and Expense**</span></span>

<span data-ttu-id="ad99f-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="ad99f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ad99f-115">Kad tiek viesota **Laika ievadņu režģa vadīkla** informācijas paneļos, režģis neizmanto visu informācijas paneļa režģa konteinera platumu.</span><span class="sxs-lookup"><span data-stu-id="ad99f-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="ad99f-116">Noteiktām laika zonām **Laika ieraksta** režģa vadīklā netiek rādīti ieraksti.</span><span class="sxs-lookup"><span data-stu-id="ad99f-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="ad99f-117">Laika ieraksti, kas ir pēc 21:00, tiek rādīti nepareizā dienā.</span><span class="sxs-lookup"><span data-stu-id="ad99f-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="ad99f-118">Lietotāji nevar iesniegt izdevumus, ja izdevumu kategorijai **Vajadzīga izdevumu kvīts** nav vērtības.</span><span class="sxs-lookup"><span data-stu-id="ad99f-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="ad99f-119">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="ad99f-119">**Resource Management**</span></span>

<span data-ttu-id="ad99f-120">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="ad99f-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="ad99f-121">Neaktīvas rezervācijas tiek rādītas skatā **Saskaņošanas**.</span><span class="sxs-lookup"><span data-stu-id="ad99f-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="ad99f-122">Vispārējai resursu izpildei trūkst validācijas, lai nodrošinātu, ka pastāv derīgs rezervācijas statuss.</span><span class="sxs-lookup"><span data-stu-id="ad99f-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="ad99f-123">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="ad99f-123">**Project Management**</span></span>

<span data-ttu-id="ad99f-124">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="ad99f-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="ad99f-125">**Projekta** veidlapu režģi (**Resursu piešķiršana**, **Uzdevums**, skats **Saskaņošana**, **Izdevumu aprēķini**) paliek rediģējami pat tad, ja projekts nav aktīvs.</span><span class="sxs-lookup"><span data-stu-id="ad99f-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="ad99f-126">Dublētos klientus nevar sapludināt ar klientiem, kas ir saistīti ar apstiprinātajiem projekta līgumiem.</span><span class="sxs-lookup"><span data-stu-id="ad99f-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="ad99f-127">Ja tiek pievienots resurss, kam nav derīga kalendāra, sistēma neatgriež lietotājam draudzīgu kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="ad99f-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="ad99f-128">Poga **Pievienot uzdevumu** poga uzdevuma režģī ir iespējota, ja projekts ir saistīts ar **Microsoft Project pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="ad99f-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="ad99f-129">Intensitāte nekontrolējami pieaug, kad uzdevums ar kategoriju tiek piešķirts resursam, kura lomai ir definēta izmaksu cena.</span><span class="sxs-lookup"><span data-stu-id="ad99f-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="ad99f-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ad99f-130">**Sales**</span></span>

<span data-ttu-id="ad99f-131">Mēs esam veikuši šādus uzlabojumus:</span><span class="sxs-lookup"><span data-stu-id="ad99f-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="ad99f-132">**Rēķinu biežums** un **Apmaksas sākums** ir pārvietoti uz cilni **Rēķinu grafiks**.</span><span class="sxs-lookup"><span data-stu-id="ad99f-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="ad99f-133">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="ad99f-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="ad99f-134">**Kopējā pārdošanas cena** ir nulle (0) attiecībā uz **Kategorija**, pat ja **Lomai** ir kopējā pārdošanas cena, kas nav nulle.</span><span class="sxs-lookup"><span data-stu-id="ad99f-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="ad99f-135">Klienti nevar mainīt lauka **Rēķina statuss** vērtību uz **Gatavs rēķinu izrakstīšanai**, ja cits pielāgots process atjaunina papildu lauku.</span><span class="sxs-lookup"><span data-stu-id="ad99f-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="ad99f-136">Poga **Atsvaidzināt rēķina rindas** atkārtoti tiek atlasīta, var izveidot vairākas dublētas rindas.</span><span class="sxs-lookup"><span data-stu-id="ad99f-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="ad99f-137">Poga **Atjaunināt cenas** nedarbojas apakšrežģī **Lomas cena** veidlapā **Ātrais skats**.</span><span class="sxs-lookup"><span data-stu-id="ad99f-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="ad99f-138">**Pārdošanas cenu saraksta risinājuma** loģika nepareizi uztver laika zonas, kas izraisa nepareizu cenrāžu atlasi.</span><span class="sxs-lookup"><span data-stu-id="ad99f-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="ad99f-139">Projekta **Faktiskās kopējās izmaksas** var tikt dalītas ar frakcionētu summu pēc viena ieraksta apstiprināšanas.</span><span class="sxs-lookup"><span data-stu-id="ad99f-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="ad99f-140">**Cenu atrisināšanas** loģika nenodrošina lietotājam draudzīgu kļūdas ziņojumu, ja **Izgūtā RolePrice** nav vērtību laukos **“Primārā vienība”** un **“Cena primārajās vienībās”**.</span><span class="sxs-lookup"><span data-stu-id="ad99f-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
