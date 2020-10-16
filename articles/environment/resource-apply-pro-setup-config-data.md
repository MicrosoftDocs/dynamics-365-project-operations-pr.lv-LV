---
title: Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service programmai Project Operations
description: Šajā tēmā ir sniegta informācija par konfigurācijas datu iestatīšanu un lietošanu programmā Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948970"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="83443-103">Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service programmai Project Operations</span><span class="sxs-lookup"><span data-stu-id="83443-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="83443-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="83443-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="83443-105">Iestatīšanas un konfigurācijas datu instalēšana</span><span class="sxs-lookup"><span data-stu-id="83443-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="83443-106">Lejupielādējiet, atbloķējiet un izgūstiet no ZIP arhīva [iestatīšanas un konfigurācijas datu pakotni](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="83443-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="83443-107">Pārejiet uz mapi, kas izgūta no ZIP arhīva, un palaidiet izpildāmo failu *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="83443-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="83443-108">Common Data Service Konfigurēšanas migrācijas (CMT) vedņa 1. lapā atlasiet vienumu **Importēt datus** un pēc tam vienumu **Turpināt**.</span><span class="sxs-lookup"><span data-stu-id="83443-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurāciju migrēšana](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="83443-110">CMT vedņa 2. lapā atlasiet **Office 365** kā **Izvietošanas tips** vērtību.</span><span class="sxs-lookup"><span data-stu-id="83443-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="83443-111">Atlasiet izvēles rūtiņas **Parādīt pieejamo organizāciju sarakstu** un **Rādīt opciju Papildus**.</span><span class="sxs-lookup"><span data-stu-id="83443-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="83443-112">Atlasiet sava nomnieka reģionu, ievadiet akreditācijas datus un atlasiet **Pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="83443-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfigurācijas pierakstīšanās](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="83443-114">3. lappusē nomnieka organizāciju sarakstā atlasiet organizāciju, kurā vēlaties importēt demonstrācijas datus, un atlasiet **Pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="83443-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="83443-115">4. lappusē no izpakotās mapes atlasiet .zip failu *SampleSetupAndConfigData*.</span><span class="sxs-lookup"><span data-stu-id="83443-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![.zip faila atlase](./media/3ZipFile.png)

![Atlasīt failu](./media/4SelectAFile.png)

9. <span data-ttu-id="83443-118">Pēc tam, kad ir atlasīts zip fails, atlasiet vienumu **Importēt datus**.</span><span class="sxs-lookup"><span data-stu-id="83443-118">After the zip file is selected, select **Import Data**.</span></span>

![Importēt datus](./media/5ImportData.png)

10. <span data-ttu-id="83443-120">Atkarībā no tīkla ātruma importēšanas darbība notiek apmēram divas līdz desmit minūtes.</span><span class="sxs-lookup"><span data-stu-id="83443-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="83443-121">Pēc importēšanas pabeigšanas izejiet no CMT vedņa.</span><span class="sxs-lookup"><span data-stu-id="83443-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="83443-122">Pārbaudiet savas organizācijas datus šajās 19 entītijās:</span><span class="sxs-lookup"><span data-stu-id="83443-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="83443-123">Valūta</span><span class="sxs-lookup"><span data-stu-id="83443-123">Currency</span></span>
  - <span data-ttu-id="83443-124">Organizācijas vienība</span><span class="sxs-lookup"><span data-stu-id="83443-124">Organizational Unit</span></span>
  - <span data-ttu-id="83443-125">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="83443-125">Contact</span></span>
  - <span data-ttu-id="83443-126">Nodokļu grupa</span><span class="sxs-lookup"><span data-stu-id="83443-126">Tax Group</span></span>
  - <span data-ttu-id="83443-127">Klientu grupa</span><span class="sxs-lookup"><span data-stu-id="83443-127">Customer Group</span></span>
  - <span data-ttu-id="83443-128">Vienība</span><span class="sxs-lookup"><span data-stu-id="83443-128">Unit</span></span>
  - <span data-ttu-id="83443-129">Vienību grupa</span><span class="sxs-lookup"><span data-stu-id="83443-129">Unit Group</span></span>
  - <span data-ttu-id="83443-130">Cenrādis</span><span class="sxs-lookup"><span data-stu-id="83443-130">Price List</span></span>
  - <span data-ttu-id="83443-131">Projekta parametru cenrādis</span><span class="sxs-lookup"><span data-stu-id="83443-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="83443-132">Rēķina izrakstīšanas biežums</span><span class="sxs-lookup"><span data-stu-id="83443-132">Invoice Frequency</span></span>
  - <span data-ttu-id="83443-133">Rezervējamo resursu kategorija</span><span class="sxs-lookup"><span data-stu-id="83443-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="83443-134">Darījuma kategorija</span><span class="sxs-lookup"><span data-stu-id="83443-134">Transaction Category</span></span>
  - <span data-ttu-id="83443-135">Izdevumu kategorija</span><span class="sxs-lookup"><span data-stu-id="83443-135">Expense Category</span></span>
  - <span data-ttu-id="83443-136">Lomas cena</span><span class="sxs-lookup"><span data-stu-id="83443-136">Role Price</span></span>
  - <span data-ttu-id="83443-137">Transakcijas kategorijas cena</span><span class="sxs-lookup"><span data-stu-id="83443-137">Transaction Category Price</span></span>
  - <span data-ttu-id="83443-138">Īpašību</span><span class="sxs-lookup"><span data-stu-id="83443-138">Characteristic</span></span>
  - <span data-ttu-id="83443-139">Rezervējamais resurssss</span><span class="sxs-lookup"><span data-stu-id="83443-139">Bookable Resource</span></span>
  - <span data-ttu-id="83443-140">Rezervējamo resursu kategorijas saistība</span><span class="sxs-lookup"><span data-stu-id="83443-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="83443-141">Rezervējamā resursa īpašība</span><span class="sxs-lookup"><span data-stu-id="83443-141">Bookable Resource Characteristic</span></span>

![Pabeigt importēšanu](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="83443-143">Project Operations konfigurāciju atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="83443-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="83443-144">Pārejiet uz CE vidi.</span><span class="sxs-lookup"><span data-stu-id="83443-144">Navigate to the CE environment.</span></span> <span data-ttu-id="83443-145">To var atrast, atverot [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/environments), atlasot vidi un pēc tam atlasot **Atvērt vidi**.</span><span class="sxs-lookup"><span data-stu-id="83443-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Atvērt vidi](./media/7OpenEnvironment.png)

2. <span data-ttu-id="83443-147">Atveriet sadaļas **Projekti** > **Resursi** un pēc tam atlasiet **Jauns**, lai savam lietotājam izveidotu rezervējamu resursu.</span><span class="sxs-lookup"><span data-stu-id="83443-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervējamie resursi](./media/8BookableResources.png)

3. <span data-ttu-id="83443-149">Cilnē **Vispārīgi** atlasiet savu lietotāju ar administratora atļaujām.</span><span class="sxs-lookup"><span data-stu-id="83443-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="83443-150">Pārbaudiet, vai laika josla atbilst tai, kurā atrodaties.</span><span class="sxs-lookup"><span data-stu-id="83443-150">Verify that the time zone matches the one you are in.</span></span> 

![Jauns rezervējamais resurss](./media/9NewBookableResource.png)

4. <span data-ttu-id="83443-152">Cilnes **Plānošana** laukā **Uzņēmums** izvēlieties **USPM** uzņēmumu un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="83443-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Cilne Plānošana](./media/10SchedulingTab.png)

5. <span data-ttu-id="83443-154">Atlasiet cilni **Darba stundas**.</span><span class="sxs-lookup"><span data-stu-id="83443-154">Select the **Work hours** tab.</span></span>  

![Darba stundas](./media/11WorkHours.png)

6. <span data-ttu-id="83443-156">Veiciet dubultklikšķi uz jebkuras kalendārā ievadītās vērtības un atlasiet **Rediģēt** > **Visi sērijas notikumi**.</span><span class="sxs-lookup"><span data-stu-id="83443-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Darba kalendārs](./media/12WorkCalendar.png)

7. <span data-ttu-id="83443-158">Mainiet darba stundas uz astoņu (8) stundu darba dienu, atzīmējiet nedēļas nogales kā nestrādājamās dienas un pārliecinieties, vai laika josla atbilst jūsu laika joslai.</span><span class="sxs-lookup"><span data-stu-id="83443-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="83443-159">Atlasiet **Saglabāt un aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="83443-159">Select **Save and close**.</span></span>

![Atjaunināt kalendāru](./media/13UpdateCalendar.png)

9. <span data-ttu-id="83443-161">Dodieties uz **Iestatījumi** > **Kalendāra veidnes** un atlasiet **Jauna**.</span><span class="sxs-lookup"><span data-stu-id="83443-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendāra veidnes](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="83443-163">Ievadiet nosaukumu, atlasiet izveidoto veidnes resursu un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="83443-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Saglabāt kalendāra veidni](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="83443-165">Dodieties uz **Parametri** un veiciet dubultklikšķi uz ieraksta.</span><span class="sxs-lookup"><span data-stu-id="83443-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projekta parametri](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="83443-167">Atjauniniet šos laukus:</span><span class="sxs-lookup"><span data-stu-id="83443-167">Update the following fields:</span></span>

 - <span data-ttu-id="83443-168">**Noklusējuma uzņēmums**: USPM</span><span class="sxs-lookup"><span data-stu-id="83443-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="83443-169">**Noklusējuma organizācijas vienība**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="83443-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="83443-170">**Rēķina izrakstīšanas biežums**: septītā un pēdējā diena</span><span class="sxs-lookup"><span data-stu-id="83443-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="83443-171">**Darba stundu veidne**: mainiet uz izveidoto veidni</span><span class="sxs-lookup"><span data-stu-id="83443-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="83443-172">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="83443-172">Select **Save**.</span></span> 

![Atjaunināti projekta parametri](./media/17UpdatedProjectParameters.png)
