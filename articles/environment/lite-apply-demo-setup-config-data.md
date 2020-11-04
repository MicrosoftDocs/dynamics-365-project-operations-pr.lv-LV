---
title: Demonstrācijas iestatīšanas un konfigurācijas datu lietošana
description: Šajā tēmā ir sniegta informācija par demonstrācijas iestatīšanas un konfigurācijas datu lietošanu programmai Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080309"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="dfee0-103">Demonstrācijas iestatīšanas un konfigurācijas datu lietošana Project Operations Lite izvietošanā — pāreja uz proforma rēķinu izrakstīšanu</span><span class="sxs-lookup"><span data-stu-id="dfee0-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="dfee0-104">_\*\*Lite izvietošana — pāriet uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="dfee0-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="dfee0-105">Lejupielādējiet [Galveno datu pakotni](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="dfee0-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="dfee0-106">Pārejiet uz mapi *ProjOpsDemoDataSetupAndMaster - Integrated CMT* un palaidiet izpildāmo failu *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="dfee0-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="dfee0-107">Common Data Service Konfigurēšanas migrācijas (CMT) vedņa 1. lapā atlasiet vienumu **Importēt datus** un pēc tam vienumu **Turpināt**.</span><span class="sxs-lookup"><span data-stu-id="dfee0-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurāciju migrēšana](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="dfee0-109">CMT Wizard 2. lapā atlasiet **Microsoft 365** kā **Izvietošanas tips** vērtību.</span><span class="sxs-lookup"><span data-stu-id="dfee0-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="dfee0-110">Atlasiet izvēles rūtiņas **Parādīt pieejamo organizāciju sarakstu** un **Rādīt opciju Papildus**.</span><span class="sxs-lookup"><span data-stu-id="dfee0-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="dfee0-111">Atlasiet sava nomnieka reģionu, ievadiet akreditācijas datus un pēc tam atlasiet **Pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="dfee0-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfigurācijas pierakstīšanās](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="dfee0-113">3. lappusē Nomnieka Organizāciju sarakstā atlasiet, kurā organizācijā vēlaties importēt demonstrācijas datus, un pēc tam atlasiet **Pieteikties**.</span><span class="sxs-lookup"><span data-stu-id="dfee0-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="dfee0-114">4. lappusē no izpakotās mapes *ProjOpsDemoDataSetupAndMaster - Integrated CMT* atlasiet zip failu *MasterAndSetupData*.</span><span class="sxs-lookup"><span data-stu-id="dfee0-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Tilpsaspiestais fails](./media/3ZipFile.png)

![Atlasīt failu](./media/4SelectAFile.png)

9. <span data-ttu-id="dfee0-117">Pēc tam, kad ir atlasīts zip fails, atlasiet vienumu **Importēt datus**.</span><span class="sxs-lookup"><span data-stu-id="dfee0-117">After the zip file is selected, select **Import Data**.</span></span>

![Importēt datus](./media/5ImportData.png)

10. <span data-ttu-id="dfee0-119">Atkarībā no tīkla ātruma importēšanas darbība notiek apmēram divas līdz desmit minūtes.</span><span class="sxs-lookup"><span data-stu-id="dfee0-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="dfee0-120">Pēc pabeigšanas izejiet no CMT vedņa.</span><span class="sxs-lookup"><span data-stu-id="dfee0-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="dfee0-121">Pārbaudiet savas organizācijas datus šajās 20 entītijās:</span><span class="sxs-lookup"><span data-stu-id="dfee0-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="dfee0-122">Valūta</span><span class="sxs-lookup"><span data-stu-id="dfee0-122">Currency</span></span>
- <span data-ttu-id="dfee0-123">Organizācijas vienība</span><span class="sxs-lookup"><span data-stu-id="dfee0-123">Organizational Unit</span></span>
- <span data-ttu-id="dfee0-124">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="dfee0-124">Contact</span></span>
- <span data-ttu-id="dfee0-125">Nodokļu grupa</span><span class="sxs-lookup"><span data-stu-id="dfee0-125">Tax Group</span></span>
- <span data-ttu-id="dfee0-126">Klientu grupa</span><span class="sxs-lookup"><span data-stu-id="dfee0-126">Customer Group</span></span>
- <span data-ttu-id="dfee0-127">Vienība</span><span class="sxs-lookup"><span data-stu-id="dfee0-127">Unit</span></span>
- <span data-ttu-id="dfee0-128">Vienību grupa</span><span class="sxs-lookup"><span data-stu-id="dfee0-128">Unit Group</span></span>
- <span data-ttu-id="dfee0-129">Cenrādis</span><span class="sxs-lookup"><span data-stu-id="dfee0-129">Price List</span></span>
- <span data-ttu-id="dfee0-130">Projekta parametru cenrādis</span><span class="sxs-lookup"><span data-stu-id="dfee0-130">Project Parameter Price List</span></span>
- <span data-ttu-id="dfee0-131">Rēķina izrakstīšanas biežums</span><span class="sxs-lookup"><span data-stu-id="dfee0-131">Invoice Frequency</span></span>
- <span data-ttu-id="dfee0-132">Rēķinu biežuma informācija</span><span class="sxs-lookup"><span data-stu-id="dfee0-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="dfee0-133">Rezervējamo resursu kategorija</span><span class="sxs-lookup"><span data-stu-id="dfee0-133">Bookable Resource Category</span></span>
- <span data-ttu-id="dfee0-134">Darījuma kategorija</span><span class="sxs-lookup"><span data-stu-id="dfee0-134">Transaction Category</span></span>
- <span data-ttu-id="dfee0-135">Izdevumu kategorija</span><span class="sxs-lookup"><span data-stu-id="dfee0-135">Expense Category</span></span>
- <span data-ttu-id="dfee0-136">Lomas cena</span><span class="sxs-lookup"><span data-stu-id="dfee0-136">Role Price</span></span>
- <span data-ttu-id="dfee0-137">Transakcijas kategorijas cena</span><span class="sxs-lookup"><span data-stu-id="dfee0-137">Transaction Category Price</span></span>
- <span data-ttu-id="dfee0-138">Īpašību</span><span class="sxs-lookup"><span data-stu-id="dfee0-138">Characteristic</span></span>
- <span data-ttu-id="dfee0-139">Rezervējamais resurssss</span><span class="sxs-lookup"><span data-stu-id="dfee0-139">Bookable Resource</span></span>
- <span data-ttu-id="dfee0-140">Rezervējamo resursu kategorijas saistība</span><span class="sxs-lookup"><span data-stu-id="dfee0-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="dfee0-141">Rezervējamā resursa īpašība</span><span class="sxs-lookup"><span data-stu-id="dfee0-141">Bookable Resource Characteristic</span></span>

![Pabeigt importēšanu](./media/6CompleteImport.png)
