---
title: Demonstrācijas iestatīšanas un konfigurācijas datu lietošana — Lite
description: Šajā tēmā ir sniegta informācija par demonstrācijas iestatīšanas un konfigurācijas datu lietošanu programmai Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 694dbc74591de74895095a9da6e590069711fc83
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290143"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="7c0cb-103">Demonstrācijas iestatīšanas un konfigurācijas datu lietošana lietojumprogrammā Project Operations — Lite</span><span class="sxs-lookup"><span data-stu-id="7c0cb-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="7c0cb-104">_\*\*Lite izvietošana — pāriet uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="7c0cb-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="7c0cb-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="7c0cb-105">Prerequisites</span></span>

<span data-ttu-id="7c0cb-106">Pirms konfigurēšanas sākšanas ir nepieciešama Common Data Service (CDS) vide, kas ir nodrošināta risinājumam Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="7c0cb-107">Norādījumi</span><span class="sxs-lookup"><span data-stu-id="7c0cb-107">Instructions</span></span>

1. <span data-ttu-id="7c0cb-108">Lejupielādējiet [Galveno datu pakotni](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="7c0cb-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="7c0cb-109">Pārejiet uz mapi *ProjOpsDemoDataSetupAndMaster - Integrated CMT* un palaidiet izpildāmo failu *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="7c0cb-110">Common Data Service Konfigurēšanas migrācijas (CMT) vedņa 1. lapā atlasiet vienumu **Importēt datus** un pēc tam vienumu **Turpināt**.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Konfigurāciju migrēšana](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="7c0cb-112">CMT Wizard 2. lapā atlasiet **Microsoft 365** kā **Izvietošanas tips** vērtību.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="7c0cb-113">Atlasiet izvēles rūtiņas **Parādīt pieejamo organizāciju sarakstu** un **Rādīt opciju Papildus**.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="7c0cb-114">Atlasiet sava nomnieka reģionu, ievadiet akreditācijas datus un pēc tam atlasiet **Pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Konfigurācijas pierakstīšanās](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="7c0cb-116">3. lappusē Nomnieka Organizāciju sarakstā atlasiet, kurā organizācijā vēlaties importēt demonstrācijas datus, un pēc tam atlasiet **Pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="7c0cb-117">4. lappusē no izpakotās mapes *ProjOpsDemoDataSetupAndMaster - Integrated CMT* atlasiet zip failu *MasterAndSetupData*.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Tilpsaspiestais fails](./media/3ZipFile.png)

   ![Atlasīt failu](./media/4SelectAFile.png)

9. <span data-ttu-id="7c0cb-120">Pēc tam, kad ir atlasīts zip fails, atlasiet vienumu **Importēt datus**.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importēt datus](./media/5ImportData.png)

10. <span data-ttu-id="7c0cb-122">Atkarībā no tīkla ātruma importēšanas darbība notiek apmēram divas līdz desmit minūtes.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="7c0cb-123">Pēc pabeigšanas izejiet no CMT vedņa.</span><span class="sxs-lookup"><span data-stu-id="7c0cb-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="7c0cb-124">Pārbaudiet savas organizācijas datus šajās 20 entītijās:</span><span class="sxs-lookup"><span data-stu-id="7c0cb-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="7c0cb-125">Valūta</span><span class="sxs-lookup"><span data-stu-id="7c0cb-125">Currency</span></span>
    -   <span data-ttu-id="7c0cb-126">Konts</span><span class="sxs-lookup"><span data-stu-id="7c0cb-126">Account</span></span>
    -   <span data-ttu-id="7c0cb-127">Organizācijas vienība</span><span class="sxs-lookup"><span data-stu-id="7c0cb-127">Organizational Unit</span></span>
    -   <span data-ttu-id="7c0cb-128">Kontaktpersona</span><span class="sxs-lookup"><span data-stu-id="7c0cb-128">Contact</span></span>
    -   <span data-ttu-id="7c0cb-129">Vienība</span><span class="sxs-lookup"><span data-stu-id="7c0cb-129">Unit</span></span>
    -   <span data-ttu-id="7c0cb-130">Vienību grupa</span><span class="sxs-lookup"><span data-stu-id="7c0cb-130">Unit Group</span></span>
    -   <span data-ttu-id="7c0cb-131">Cenrādis</span><span class="sxs-lookup"><span data-stu-id="7c0cb-131">Price List</span></span>
    -   <span data-ttu-id="7c0cb-132">Projekta parametru cenrādis</span><span class="sxs-lookup"><span data-stu-id="7c0cb-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="7c0cb-133">Rēķina izrakstīšanas biežums</span><span class="sxs-lookup"><span data-stu-id="7c0cb-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="7c0cb-134">Rezervējamo resursu kategorija</span><span class="sxs-lookup"><span data-stu-id="7c0cb-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="7c0cb-135">Darījuma kategorija</span><span class="sxs-lookup"><span data-stu-id="7c0cb-135">Transaction Category</span></span>
    -   <span data-ttu-id="7c0cb-136">Izdevumu kategorija</span><span class="sxs-lookup"><span data-stu-id="7c0cb-136">Expense Category</span></span>
    -   <span data-ttu-id="7c0cb-137">Lomas cena</span><span class="sxs-lookup"><span data-stu-id="7c0cb-137">Role Price</span></span>
    -   <span data-ttu-id="7c0cb-138">Transakcijas kategorijas cena</span><span class="sxs-lookup"><span data-stu-id="7c0cb-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="7c0cb-139">Īpašību</span><span class="sxs-lookup"><span data-stu-id="7c0cb-139">Characteristic</span></span>
    -   <span data-ttu-id="7c0cb-140">Rezervējamais resurssss</span><span class="sxs-lookup"><span data-stu-id="7c0cb-140">Bookable Resource</span></span>
    -   <span data-ttu-id="7c0cb-141">Rezervējamo resursu kategorijas saistība</span><span class="sxs-lookup"><span data-stu-id="7c0cb-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="7c0cb-142">Rezervējamā resursa īpašība</span><span class="sxs-lookup"><span data-stu-id="7c0cb-142">Bookable Resource Characteristic</span></span>

    ![Pabeigt importēšanu](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]