---
title: Demonstrācijas iestatīšanas un konfigurācijas datu lietošana — Lite
description: Šajā tēmā ir sniegta informācija par demonstrācijas iestatīšanas un konfigurācijas datu lietošanu programmai Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997160"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="bb892-103">Demonstrācijas iestatīšanas un konfigurācijas datu lietošana lietojumprogrammā Project Operations — Lite</span><span class="sxs-lookup"><span data-stu-id="bb892-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="bb892-104">_\*\*Lite izvietošana — pāriet uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="bb892-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="bb892-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="bb892-105">Prerequisites</span></span>

<span data-ttu-id="bb892-106">Pirms konfigurēšanas sākšanas ir nepieciešama Common Data Service (CDS) vide, kas ir nodrošināta risinājumam Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="bb892-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="bb892-107">Norādījumi</span><span class="sxs-lookup"><span data-stu-id="bb892-107">Instructions</span></span>

1. <span data-ttu-id="bb892-108">Lejupielādējiet [Galveno datu pakotni](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="bb892-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="bb892-109">Pārejiet uz mapi *ProjOpsSampleSetupData - CE only CMT* un palaidiet izpildāmo failu *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="bb892-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="bb892-110">Common Data Service Konfigurēšanas migrācijas (CMT) vedņa 1. lapā atlasiet vienumu **Importēt datus** un pēc tam vienumu **Turpināt**.</span><span class="sxs-lookup"><span data-stu-id="bb892-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Konfigurāciju migrēšana](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="bb892-112">CMT Wizard 2. lapā atlasiet **Microsoft 365** kā **Izvietošanas tips** vērtību.</span><span class="sxs-lookup"><span data-stu-id="bb892-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="bb892-113">Atlasiet izvēles rūtiņas **Parādīt pieejamo organizāciju sarakstu** un **Rādīt opciju Papildus**.</span><span class="sxs-lookup"><span data-stu-id="bb892-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="bb892-114">Atlasiet sava nomnieka reģionu, ievadiet akreditācijas datus un pēc tam atlasiet **Pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="bb892-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Konfigurācijas pierakstīšanās](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="bb892-116">3. lappusē Nomnieka Organizāciju sarakstā atlasiet, kurā organizācijā vēlaties importēt demonstrācijas datus, un pēc tam atlasiet **Pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="bb892-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="bb892-117">4. lapā atlasiet zip failu *SampleSetupAndConfigData* no neizpakotās mapes *ProjOpsSampleSetupData - CE only CMT*.</span><span class="sxs-lookup"><span data-stu-id="bb892-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Tilpsaspiestais fails](./media/3ZipFile.png)

   ![Atlasīt failu](./media/4SelectAFile.png)

9. <span data-ttu-id="bb892-120">Pēc tam, kad ir atlasīts zip fails, atlasiet vienumu **Importēt datus**.</span><span class="sxs-lookup"><span data-stu-id="bb892-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importēt datus](./media/5ImportData.png)

10. <span data-ttu-id="bb892-122">Atkarībā no tīkla ātruma importēšanas darbība notiek apmēram divas līdz desmit minūtes.</span><span class="sxs-lookup"><span data-stu-id="bb892-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="bb892-123">Pēc pabeigšanas izejiet no CMT vedņa.</span><span class="sxs-lookup"><span data-stu-id="bb892-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="bb892-124">Pārbaudiet savas organizācijas datus šajās 18 entītijās:</span><span class="sxs-lookup"><span data-stu-id="bb892-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="bb892-125">Valūta</span><span class="sxs-lookup"><span data-stu-id="bb892-125">Currency</span></span>
    -   <span data-ttu-id="bb892-126">Konts</span><span class="sxs-lookup"><span data-stu-id="bb892-126">Account</span></span>
    -   <span data-ttu-id="bb892-127">Organizācijas vienība</span><span class="sxs-lookup"><span data-stu-id="bb892-127">Organizational Unit</span></span>
    -   <span data-ttu-id="bb892-128">Kontaktpersona</span><span class="sxs-lookup"><span data-stu-id="bb892-128">Contact</span></span>
    -   <span data-ttu-id="bb892-129">Vienība</span><span class="sxs-lookup"><span data-stu-id="bb892-129">Unit</span></span>
    -   <span data-ttu-id="bb892-130">Vienību grupa</span><span class="sxs-lookup"><span data-stu-id="bb892-130">Unit Group</span></span>
    -   <span data-ttu-id="bb892-131">Cenrādis</span><span class="sxs-lookup"><span data-stu-id="bb892-131">Price List</span></span>
    -   <span data-ttu-id="bb892-132">Projekta parametru cenrādis</span><span class="sxs-lookup"><span data-stu-id="bb892-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="bb892-133">Rēķina izrakstīšanas biežums</span><span class="sxs-lookup"><span data-stu-id="bb892-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="bb892-134">Rezervējamo resursu kategorija</span><span class="sxs-lookup"><span data-stu-id="bb892-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="bb892-135">Darījuma kategorija</span><span class="sxs-lookup"><span data-stu-id="bb892-135">Transaction Category</span></span>
    -   <span data-ttu-id="bb892-136">Izdevumu kategorija</span><span class="sxs-lookup"><span data-stu-id="bb892-136">Expense Category</span></span>
    -   <span data-ttu-id="bb892-137">Lomas cena</span><span class="sxs-lookup"><span data-stu-id="bb892-137">Role Price</span></span>
    -   <span data-ttu-id="bb892-138">Transakcijas kategorijas cena</span><span class="sxs-lookup"><span data-stu-id="bb892-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="bb892-139">Īpašību</span><span class="sxs-lookup"><span data-stu-id="bb892-139">Characteristic</span></span>
    -   <span data-ttu-id="bb892-140">Rezervējamais resurssss</span><span class="sxs-lookup"><span data-stu-id="bb892-140">Bookable Resource</span></span>
    -   <span data-ttu-id="bb892-141">Rezervējamo resursu kategorijas saistība</span><span class="sxs-lookup"><span data-stu-id="bb892-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="bb892-142">Rezervējamā resursa īpašība</span><span class="sxs-lookup"><span data-stu-id="bb892-142">Bookable Resource Characteristic</span></span>

    ![Pabeigt importēšanu](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
