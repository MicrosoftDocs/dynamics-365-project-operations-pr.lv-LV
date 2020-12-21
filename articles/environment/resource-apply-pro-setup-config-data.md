---
title: Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service
description: Šajā tēmā ir sniegta informācija par konfigurācijas datu iestatīšanu un lietošanu programmā Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642237"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="37779-103">Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service</span><span class="sxs-lookup"><span data-stu-id="37779-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="37779-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="37779-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="37779-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="37779-105">Prerequisites</span></span>

<span data-ttu-id="37779-106">Pirms datu konfigurēšanas pakalpojumā Common Data Service (CDS) ir jāizpilda šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="37779-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="37779-107">Nodrošināt CDS vidi un Dynamics 365 Finance vidi risinājumam Project Operations.</span><span class="sxs-lookup"><span data-stu-id="37779-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="37779-108">Informācija par juridiskajām entītijām no Dynamics 365 Finance tiek kopīgota ar CDS vidi.</span><span class="sxs-lookup"><span data-stu-id="37779-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="37779-109">Tas nozīmē, ka entītijai **Uzņēmums** pakalpojumā CDS ir šādi uzņēmumu ieraksti:</span><span class="sxs-lookup"><span data-stu-id="37779-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="37779-110">THPM</span><span class="sxs-lookup"><span data-stu-id="37779-110">THPM</span></span>
  - <span data-ttu-id="37779-111">USPM</span><span class="sxs-lookup"><span data-stu-id="37779-111">USPM</span></span>
  - <span data-ttu-id="37779-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="37779-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="37779-113">Iestatīšanas un konfigurācijas datu instalēšana</span><span class="sxs-lookup"><span data-stu-id="37779-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="37779-114">Lejupielādējiet, atbloķējiet un izgūstiet no ZIP arhīva [iestatīšanas un konfigurācijas datu pakotni](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="37779-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="37779-115">Pārejiet uz mapi, kas izgūta no ZIP arhīva, un palaidiet izpildāmo failu *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="37779-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="37779-116">Common Data Service Konfigurēšanas migrācijas (CMT) vedņa 1. lapā atlasiet vienumu **Importēt datus** un pēc tam vienumu **Turpināt**.</span><span class="sxs-lookup"><span data-stu-id="37779-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurāciju migrēšana](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="37779-118">CMT Wizard 2. lapā atlasiet **Microsoft 365** kā **Izvietošanas tips** vērtību.</span><span class="sxs-lookup"><span data-stu-id="37779-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="37779-119">Atlasiet izvēles rūtiņas **Parādīt pieejamo organizāciju sarakstu** un **Rādīt opciju Papildus**.</span><span class="sxs-lookup"><span data-stu-id="37779-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="37779-120">Atlasiet sava nomnieka reģionu, ievadiet akreditācijas datus un atlasiet **Pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="37779-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfigurācijas pierakstīšanās](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="37779-122">3. lappusē nomnieka organizāciju sarakstā atlasiet organizāciju, kurā vēlaties importēt demonstrācijas datus, un atlasiet **Pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="37779-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="37779-123">4. lappusē no izpakotās mapes atlasiet .zip failu *SampleSetupAndConfigData*.</span><span class="sxs-lookup"><span data-stu-id="37779-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![.zip faila atlase](./media/3ZipFile.png)

![Atlasīt failu](./media/4SelectAFile.png)

9. <span data-ttu-id="37779-126">Pēc tam, kad ir atlasīts zip fails, atlasiet vienumu **Importēt datus**.</span><span class="sxs-lookup"><span data-stu-id="37779-126">After the zip file is selected, select **Import Data**.</span></span>

![Importēt datus](./media/5ImportData.png)

10. <span data-ttu-id="37779-128">Atkarībā no tīkla ātruma importēšanas darbība notiek apmēram divas līdz desmit minūtes.</span><span class="sxs-lookup"><span data-stu-id="37779-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="37779-129">Pēc importēšanas pabeigšanas izejiet no CMT vedņa.</span><span class="sxs-lookup"><span data-stu-id="37779-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="37779-130">Pārbaudiet savas organizācijas datus šajās 19 entītijās:</span><span class="sxs-lookup"><span data-stu-id="37779-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="37779-131">Valūta</span><span class="sxs-lookup"><span data-stu-id="37779-131">Currency</span></span>
  - <span data-ttu-id="37779-132">Organizācijas vienība</span><span class="sxs-lookup"><span data-stu-id="37779-132">Organizational Unit</span></span>
  - <span data-ttu-id="37779-133">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="37779-133">Contact</span></span>
  - <span data-ttu-id="37779-134">Nodokļu grupa</span><span class="sxs-lookup"><span data-stu-id="37779-134">Tax Group</span></span>
  - <span data-ttu-id="37779-135">Klientu grupa</span><span class="sxs-lookup"><span data-stu-id="37779-135">Customer Group</span></span>
  - <span data-ttu-id="37779-136">Vienība</span><span class="sxs-lookup"><span data-stu-id="37779-136">Unit</span></span>
  - <span data-ttu-id="37779-137">Vienību grupa</span><span class="sxs-lookup"><span data-stu-id="37779-137">Unit Group</span></span>
  - <span data-ttu-id="37779-138">Cenrādis</span><span class="sxs-lookup"><span data-stu-id="37779-138">Price List</span></span>
  - <span data-ttu-id="37779-139">Projekta parametru cenrādis</span><span class="sxs-lookup"><span data-stu-id="37779-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="37779-140">Rēķina izrakstīšanas biežums</span><span class="sxs-lookup"><span data-stu-id="37779-140">Invoice Frequency</span></span>
  - <span data-ttu-id="37779-141">Rezervējamo resursu kategorija</span><span class="sxs-lookup"><span data-stu-id="37779-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="37779-142">Darījuma kategorija</span><span class="sxs-lookup"><span data-stu-id="37779-142">Transaction Category</span></span>
  - <span data-ttu-id="37779-143">Izdevumu kategorija</span><span class="sxs-lookup"><span data-stu-id="37779-143">Expense Category</span></span>
  - <span data-ttu-id="37779-144">Lomas cena</span><span class="sxs-lookup"><span data-stu-id="37779-144">Role Price</span></span>
  - <span data-ttu-id="37779-145">Transakcijas kategorijas cena</span><span class="sxs-lookup"><span data-stu-id="37779-145">Transaction Category Price</span></span>
  - <span data-ttu-id="37779-146">Īpašību</span><span class="sxs-lookup"><span data-stu-id="37779-146">Characteristic</span></span>
  - <span data-ttu-id="37779-147">Rezervējamais resurssss</span><span class="sxs-lookup"><span data-stu-id="37779-147">Bookable Resource</span></span>
  - <span data-ttu-id="37779-148">Rezervējamo resursu kategorijas saistība</span><span class="sxs-lookup"><span data-stu-id="37779-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="37779-149">Rezervējamā resursa īpašība</span><span class="sxs-lookup"><span data-stu-id="37779-149">Bookable Resource Characteristic</span></span>

![Pabeigt importēšanu](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="37779-151">Project Operations konfigurāciju atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="37779-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="37779-152">Pārejiet uz CE vidi.</span><span class="sxs-lookup"><span data-stu-id="37779-152">Navigate to the CE environment.</span></span> <span data-ttu-id="37779-153">To var atrast, atverot [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/environments), atlasot vidi un pēc tam atlasot **Atvērt vidi**.</span><span class="sxs-lookup"><span data-stu-id="37779-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Atvērt vidi](./media/7OpenEnvironment.png)

2. <span data-ttu-id="37779-155">Atveriet sadaļas **Projekti** > **Resursi** un pēc tam atlasiet **Jauns**, lai savam lietotājam izveidotu rezervējamu resursu.</span><span class="sxs-lookup"><span data-stu-id="37779-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervējamie resursi](./media/8BookableResources.png)

3. <span data-ttu-id="37779-157">Cilnē **Vispārīgi** atlasiet savu lietotāju ar administratora atļaujām.</span><span class="sxs-lookup"><span data-stu-id="37779-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="37779-158">Pārbaudiet, vai laika josla atbilst tai, kurā atrodaties.</span><span class="sxs-lookup"><span data-stu-id="37779-158">Verify that the time zone matches the one you are in.</span></span> 

![Jauns rezervējamais resurss](./media/9NewBookableResource.png)

4. <span data-ttu-id="37779-160">Cilnes **Plānošana** laukā **Uzņēmums** izvēlieties **USPM** uzņēmumu un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="37779-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Cilne Plānošana](./media/10SchedulingTab.png)

5. <span data-ttu-id="37779-162">Atlasiet cilni **Darba stundas**.</span><span class="sxs-lookup"><span data-stu-id="37779-162">Select the **Work hours** tab.</span></span>  

![Darba stundas](./media/11WorkHours.png)

6. <span data-ttu-id="37779-164">Veiciet dubultklikšķi uz jebkuras kalendārā ievadītās vērtības un atlasiet **Rediģēt** > **Visi sērijas notikumi**.</span><span class="sxs-lookup"><span data-stu-id="37779-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Darba kalendārs](./media/12WorkCalendar.png)

7. <span data-ttu-id="37779-166">Mainiet darba stundas uz astoņu (8) stundu darba dienu, atzīmējiet nedēļas nogales kā nestrādājamās dienas un pārliecinieties, vai laika josla atbilst jūsu laika joslai.</span><span class="sxs-lookup"><span data-stu-id="37779-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="37779-167">Atlasiet **Saglabāt un aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="37779-167">Select **Save and close**.</span></span>

![Atjaunināt kalendāru](./media/13UpdateCalendar.png)

9. <span data-ttu-id="37779-169">Dodieties uz **Iestatījumi** > **Kalendāra veidnes** un atlasiet **Jauna**.</span><span class="sxs-lookup"><span data-stu-id="37779-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendāra veidnes](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="37779-171">Ievadiet nosaukumu, atlasiet izveidoto veidnes resursu un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="37779-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Saglabāt kalendāra veidni](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="37779-173">Dodieties uz **Parametri** un veiciet dubultklikšķi uz ieraksta.</span><span class="sxs-lookup"><span data-stu-id="37779-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projekta parametri](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="37779-175">Atjauniniet šos laukus:</span><span class="sxs-lookup"><span data-stu-id="37779-175">Update the following fields:</span></span>

 - <span data-ttu-id="37779-176">**Noklusējuma uzņēmums**: USPM</span><span class="sxs-lookup"><span data-stu-id="37779-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="37779-177">**Noklusējuma organizācijas vienība**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="37779-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="37779-178">**Rēķina izrakstīšanas biežums**: septītā un pēdējā diena</span><span class="sxs-lookup"><span data-stu-id="37779-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="37779-179">**Darba stundu veidne**: mainiet uz izveidoto veidni</span><span class="sxs-lookup"><span data-stu-id="37779-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="37779-180">Atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="37779-180">Select **Save**.</span></span> 

![Atjaunināti projekta parametri](./media/17UpdatedProjectParameters.png)
