---
title: Projekta izdevumu kategoriju sinhronizēšana starp Finance and Operations un Project Service Automation
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta izdevumu kategoriju sinhronizēšanai starp Microsoft Dynamics 365 Finance un Dynamics 365 Project Service Automation.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289648"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="bd2a5-103">Projekta izdevumu kategoriju sinhronizēšana starp Finance and Operations un Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bd2a5-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bd2a5-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta izdevumu kategoriju sinhronizēšanai starp Dynamics 365 Finance un Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="bd2a5-105">8.0 versijā varat izmantot projekta uzdevumu integrāciju, izdevumu darbības kategorijas, stundu aprēķinus, izdevumu aprēķinus un funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="bd2a5-106">Faktisko datu integrācija ir pieejama 8.0.1 vai jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="bd2a5-107">Ja izmantojat Enterprise edition 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu aprēķinus, izdevumu aprēķinus un faktiskos datus un konfigurēt funkcionalitātes bloķēšanu.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="bd2a5-108">Ja ir jāatiestata uzskaites sadales, ieteicams instalēt arī KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="bd2a5-109">Datu plūsma Project Service Automation un Finance</span><span class="sxs-lookup"><span data-stu-id="bd2a5-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="bd2a5-110">Project Service Automation un Finance integrācijas risinājumam tiek izmantots datu integrācijas līdzeklis, lai sinhronizētu datus starp Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="bd2a5-111">Integrācijas veidnes, kas ir pieejamas kopā ar datu integrācijas līdzekli, iespējo datu plūsmu par projekta izdevumu transakciju kategorijām starp Finance un Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="bd2a5-112">Ja projekta izmaksu kategorijas ir apstrādātas risinājumā Finance, integrācijas plūsma vispirms ir no Finance uz Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="bd2a5-113">Projekta izmaksu kategoriju integrācijas ID pēc tam tiek atjaunināti, izmantojot sinhronizāciju no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="bd2a5-114">Ja projekta izmaksu kategorijas ir apstrādātas risinājumā Project Service Automation, integrācijas plūsma vispirms ir no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="bd2a5-115">Lai varētu veikt sinhronizāciju no Project Service Automation, projekta kategorijām jau ir jābūt konfigurētām Finance.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="bd2a5-116">Pēc tam sinhronizējiet no Finance atpakaļ uz Project Service Automation un pēc tam vēlreiz no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="bd2a5-117">Šādi tiek nodrošināta garantija, ka kategorijas ir saistītas un netiek izveidoti dublikāti.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="bd2a5-118">Parasti projekta izmaksu kategorijas tiek apstrādātas risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="bd2a5-119">Tomēr, ja tā nav vai ja izdevumu kategorijas jau ir izveidotas Project Service Automation, vispirms ir jāsinhronizē, izmantojot projekta izdevumu transakciju kategoriju (PSA uz Fin un OPS) veidne.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="bd2a5-120">Pēc tam veiciet sinhronizēšanu, izmantojot projekta izdevumu transakciju kategoriju (Fin un Ops uz PSA) veidni.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="bd2a5-121">Pēc tam ir jāsinhronizē no Project Service Automation uz Finance vēl vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="bd2a5-122">Ja vispirms tiek sinhronizēts no Project Service Automation, pirms sinhronizācijas izpildes risinājumā Finance ir jāizpilda šādas prasības:</span><span class="sxs-lookup"><span data-stu-id="bd2a5-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="bd2a5-123">Ir jāpastāv koplietojamai kategorijai, kas atbilst Project Service Automation iestatītajai projekta kategorijai, un tai ir jābūt iespējotai gan **Projekts**, gan **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="bd2a5-124">Attiecībā uz katru Finance juridisko personu, kas ir jāintegrē, ir jāpastāv šādām projekta kategorijām:</span><span class="sxs-lookup"><span data-stu-id="bd2a5-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="bd2a5-125">Pastāv **Projekta kategorija**.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="bd2a5-126">Ir iespējota opcija **Lietot izdevumiem**.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="bd2a5-127">Ir iespējota opcija **Aktīvs žurnālā**.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="bd2a5-128">**Transakcijas tips** ir iestatīts uz **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="bd2a5-129">Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti starp Project Service Automation un Finance.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="bd2a5-130">[![Datu plūsma Project Service Automation integrācijai ar Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="bd2a5-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="bd2a5-131">Projekta izdevumu kategoriju sinhronizēšana no Finance uz Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bd2a5-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="bd2a5-132">Veidne un uzdevums</span><span class="sxs-lookup"><span data-stu-id="bd2a5-132">Template and task</span></span>

<span data-ttu-id="bd2a5-133">Lai piekļūtu veidnei, Microsoft Power Apps administrēšanas centrā atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskas veidnes.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="bd2a5-134">Lai sinhronizētu projekta izmaksu kategorijas no Finance uz Project Service Automation, tiek izmantota šāda veidne un pamata uzdevums:</span><span class="sxs-lookup"><span data-stu-id="bd2a5-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="bd2a5-135">**Veidnes nosaukums datu integrācijā:** Projekta izmaksu transakciju kategorijas (Fin un Ops uz PSA)</span><span class="sxs-lookup"><span data-stu-id="bd2a5-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="bd2a5-136">**Uzdevuma nosaukums projektā:** Kategoriju sinhronizācija uz PSA</span><span class="sxs-lookup"><span data-stu-id="bd2a5-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="bd2a5-137">Entītiju kopa</span><span class="sxs-lookup"><span data-stu-id="bd2a5-137">Entity set</span></span>

| <span data-ttu-id="bd2a5-138">Finanses</span><span class="sxs-lookup"><span data-stu-id="bd2a5-138">Finance</span></span>                           | <span data-ttu-id="bd2a5-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bd2a5-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="bd2a5-140">Kategoriju integrācijas entītija</span><span class="sxs-lookup"><span data-stu-id="bd2a5-140">Integration entity for categories</span></span> | <span data-ttu-id="bd2a5-141">Transakcijas kategorijas</span><span class="sxs-lookup"><span data-stu-id="bd2a5-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="bd2a5-142">Entītijas plūsma</span><span class="sxs-lookup"><span data-stu-id="bd2a5-142">Entity flow</span></span>

<span data-ttu-id="bd2a5-143">Projekta izdevumu kategorijas tiek pārvaldītas pakalpojumā Finance, un tās tiek sinhronizētas uz Project Service Automation kā transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="bd2a5-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="bd2a5-144">Power Query</span></span>

<span data-ttu-id="bd2a5-145">Kad veicat sinhronizēšanu uz Project Service Automation, ir jāizmanto Microsoft Power Query programmai Excel, lai transakciju kategorijā iestatītu norēķinu tipu.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="bd2a5-146">Projekta izdevumu transakciju kategoriju (Fin un Ops uz PSA) veidne nodrošina noklusējuma kolonnu un kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="bd2a5-147">Ja izveidojat savu veidni, ir jāpievieno nosacījuma kolonna, izmantojot Power Query.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="bd2a5-148">Veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-148">Follow these steps.</span></span>

1. <span data-ttu-id="bd2a5-149">Noklikšķiniet uz bultiņas, lai atvērtu projekta izdevumu kategoriju uzdevuma kartējumu projekta izdevumu transakciju kategoriju (Fin un Ops uz PSA) veidnē.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="bd2a5-150">Noklikšķiniet uz **Detalizēto vaicājumu un filtrēšanas** saites, lai atvērtu Power Query.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="bd2a5-151">Atlasiet **Pievienot nosacījuma kolonnu**.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="bd2a5-152">Ievadiet jaunās kolonnas nosaukumu, piemēram, **NorēķinuTips**.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="bd2a5-153">Ievadiet šādu nosacījumu:Ievadiet šādu nosacījumu: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="bd2a5-154">Kolonnā noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="bd2a5-155">Noteikti kartējiet šo jauno kolonnu kartēšanas lapā.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="bd2a5-156">Nākamajā ilustrācijā ir redzams piemērs no veidnes uzdevumu kartējuma datu integrācijā.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="bd2a5-157">Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Finance uz Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="bd2a5-158">[![Projekta izdevumu kategorija Project Service Automation veidnes kartēšanai](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="bd2a5-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="bd2a5-159">Projekta izdevumu kategoriju sinhronizēšana no Project Service Automation uz Finance</span><span class="sxs-lookup"><span data-stu-id="bd2a5-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="bd2a5-160">Veidne un uzdevums</span><span class="sxs-lookup"><span data-stu-id="bd2a5-160">Template and task</span></span>

<span data-ttu-id="bd2a5-161">Lai sinhronizētu projekta izmaksu kategorijas no Project Service Automation uz Finance, tiek izmantota šāda veidne un pamata uzdevums:</span><span class="sxs-lookup"><span data-stu-id="bd2a5-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="bd2a5-162">**Veidnes nosaukums datu integrācijā:** Projekta izmaksu transakciju kategorijas (PSA uz Fin un Ops)</span><span class="sxs-lookup"><span data-stu-id="bd2a5-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="bd2a5-163">**Uzdevuma nosaukums projektā:** Kategoriju sinhronizācija uz Fin Ops</span><span class="sxs-lookup"><span data-stu-id="bd2a5-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="bd2a5-164">Entītiju kopa</span><span class="sxs-lookup"><span data-stu-id="bd2a5-164">Entity set</span></span>

| <span data-ttu-id="bd2a5-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bd2a5-165">Project Service Automation</span></span> | <span data-ttu-id="bd2a5-166">Finanses</span><span class="sxs-lookup"><span data-stu-id="bd2a5-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="bd2a5-167">Transakcijas kategorijas</span><span class="sxs-lookup"><span data-stu-id="bd2a5-167">Transaction categories</span></span>     | <span data-ttu-id="bd2a5-168">Kategoriju integrācijas entītija</span><span class="sxs-lookup"><span data-stu-id="bd2a5-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="bd2a5-169">Entītijas plūsma</span><span class="sxs-lookup"><span data-stu-id="bd2a5-169">Entity flow</span></span>

<span data-ttu-id="bd2a5-170">Projekta izdevumu kategorijas tiek pārvaldītas pakalpojumā Finance, un tās tiek sinhronizētas uz Project Service Automation kā transakciju kategorijas.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="bd2a5-171">Sinhronizācija atpakaļ uz Finance atjaunina projekta kategoriju pakalpojumā Finance ar integrācijas ID no Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="bd2a5-172">Veidņu kartēšana datu integrācijā</span><span class="sxs-lookup"><span data-stu-id="bd2a5-172">Template mapping in Data integration</span></span>

<span data-ttu-id="bd2a5-173">Nākamajā ilustrācijā ir redzams piemērs no veidnes uzdevumu kartējuma datu integrācijā.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="bd2a5-174">Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.</span><span class="sxs-lookup"><span data-stu-id="bd2a5-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="bd2a5-175">[![Project Service Automation Finance veidnes kartēšanai](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="bd2a5-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]