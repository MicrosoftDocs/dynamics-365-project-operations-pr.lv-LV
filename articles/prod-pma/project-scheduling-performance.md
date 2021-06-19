---
title: Projekta resursu plānošanas veiktspēja
description: Šajā tēmā ir sniegta informācija par to, kā uzlabot resursu plānošanas veiktspēju lielam skaitam projektu.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010030"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="65a19-103">Projekta resursu plānošanas veiktspēja</span><span class="sxs-lookup"><span data-stu-id="65a19-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="65a19-104">Veiktspējas problēmas, kas saistītas ar resursu plānošanu, var rasties, ja projektu skaits sasniedz tūkstošus.</span><span class="sxs-lookup"><span data-stu-id="65a19-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="65a19-105">Lai uzlabotu resursu plānošanas veiktspēju, ir pieejams līdzeklis, kas ļauj lietotājiem samazināt laiku, kas nepieciešams, lai palaistu resursu pieejamības veidlapu.</span><span class="sxs-lookup"><span data-stu-id="65a19-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="65a19-106">Precīzāk — tas noņem resursu ietilpības apkopošanas sinhronizācijas procesu un izmanto tabulu **ResProjectResource**, lai paātrinātu resursu pārlūkošanu.</span><span class="sxs-lookup"><span data-stu-id="65a19-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="65a19-107">Ņemiet vērā, ka tabula **ResRollup** vairs netiks izmantota.</span><span class="sxs-lookup"><span data-stu-id="65a19-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65a19-108">Ja ir atkarība no resursu noslodzes apkopojuma sinhronizācijas procesa vai tabulas **ResProjectResource**, neizmantojiet šo līdzekli.</span><span class="sxs-lookup"><span data-stu-id="65a19-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="65a19-109">Resursu plānošanas veiktspējas uzlabojuma iespējošana</span><span class="sxs-lookup"><span data-stu-id="65a19-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="65a19-110">Lai iespējotu resursu plānošanas veiktspējas uzlabošanu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="65a19-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="65a19-111">Dodieties uz **Līdzekļu pārvaldība** > **Visi** un līdzekļu sarakstā atrodiet **Iespējot projekta resursu plānošanas veiktspējas uzlabošanas līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="65a19-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="65a19-112">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="65a19-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="65a19-113">Ja sarakstā nevarat atrast šo līdzekli, atlasiet **Pārbaudīt, vai nav atjauninājumu**, lai atsvaidzinātu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="65a19-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="65a19-114">Atsvaidziniet pārlūkprogrammu un pēc tam apmeklējiet sadaļu **Projekta pārvaldība un uzskaite** > **Periodisks** > **Projekta resursi** > **Sinhronizēt resursu kalendāru noslodzi visiem uzņēmumiem**.</span><span class="sxs-lookup"><span data-stu-id="65a19-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="65a19-115">Lai noņemtu iepriekšējos datus, iestatiet **Esošu noslodzes ierakstu noņemšana** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="65a19-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="65a19-116">Ja vēlaties ģenerēt inkrementālos datus, iestatiet to uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="65a19-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="65a19-117">Laukā **Perioda kods** atlasiet datu ģenerēšanas periodu.</span><span class="sxs-lookup"><span data-stu-id="65a19-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="65a19-118">Ja atlasāt perioda kodu, ir jādefinē sākuma un beigu datumi.</span><span class="sxs-lookup"><span data-stu-id="65a19-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="65a19-119">Ja lauks **Perioda kods** netiek aizpildīts, atlasiet noteiktus sākuma un beigu datumus, lai ģenerētu datus.</span><span class="sxs-lookup"><span data-stu-id="65a19-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="65a19-120">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="65a19-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="65a19-121">Šādi vispārējie dati tiks izplatīti tabulā **ResCalendarCapacity** visos uzņēmumos jūsu apkārtnē, tāpēc pakešuzdevumam ir jābūt izpildītam tikai vienā juridiskā entītijā.</span><span class="sxs-lookup"><span data-stu-id="65a19-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="65a19-122">Šī pakešuzdevuma dati ir nepieciešami, lai aprēķinātu resursa noslodzi caur saistīto kalendāru.</span><span class="sxs-lookup"><span data-stu-id="65a19-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="65a19-123">Atveriet **Projekta pārvaldība un uzskaite** > **Periodisks** > **Projekta resursi** > **Projekta resursu aizpildīšana visos uzņēmumos** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="65a19-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="65a19-124">Šis ir datu jaunināšanas skripts vispārējiem datiem tabulās **ResProjectResource**, **ResCalendarDateTimeRange** un **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="65a19-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="65a19-125">Arī lauka **PSAPRojSchedRole.RootActivity** vērtības tiek atjauninātas.</span><span class="sxs-lookup"><span data-stu-id="65a19-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="65a19-126">Ja tas netiek izpildīts, kad mēģināsit izpildīt resursu plānošanas operācijas, saņemsit brīdinājumu.</span><span class="sxs-lookup"><span data-stu-id="65a19-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="65a19-127">Resursu plānošanas veiktspējas uzlabojuma izslēgšana</span><span class="sxs-lookup"><span data-stu-id="65a19-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="65a19-128">Dodieties uz **Līdzekļu pārvaldība** > **Visi** un meklējiet **Iespējot projekta resursu plānošanas veiktspējas uzlabošanas līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="65a19-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="65a19-129">Atlasiet līdzekli un pēc tam noklikšķiniet uz pogas **Atspējot**.</span><span class="sxs-lookup"><span data-stu-id="65a19-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="65a19-130">Atsvaidziniet pārlūkprogrammu.</span><span class="sxs-lookup"><span data-stu-id="65a19-130">Refresh your browser.</span></span>
4. <span data-ttu-id="65a19-131">Dodieties uz **Projekta pārvaldība un uzskaite** > **Periodisks** > **Noslodzes sinhronizācija** > **Sinhronizēt resursu noslodzes apkopojumus**.</span><span class="sxs-lookup"><span data-stu-id="65a19-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="65a19-132">Lapā **Noslodzes apkopojuma sinhronizācija** iestatiet **Esošo noslodzes ierakstu noņemšana** uz **Jā**, lai noņemtu iepriekšējos datus.</span><span class="sxs-lookup"><span data-stu-id="65a19-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="65a19-133">Ja vēlaties ģenerēt inkrementālos datus, iestatiet to uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="65a19-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="65a19-134">Laukā **Perioda kods** atlasiet datu ģenerēšanas periodu.</span><span class="sxs-lookup"><span data-stu-id="65a19-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="65a19-135">Ja atlasāt perioda kodu, ir jādefinē sākuma un beigu datumi.</span><span class="sxs-lookup"><span data-stu-id="65a19-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="65a19-136">Ja lauks **Perioda kods** netiek aizpildīts, atlasiet noteiktus sākuma un beigu datumus, lai ģenerētu datus.</span><span class="sxs-lookup"><span data-stu-id="65a19-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="65a19-137">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="65a19-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="65a19-138">Šādi vispārējie dati tiks izplatīti tabulā **ResRollup** visos uzņēmumos jūsu apkārtnē, tāpēc pakešuzdevumam ir jābūt izpildītam tikai vienā juridiskā entītijā.</span><span class="sxs-lookup"><span data-stu-id="65a19-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="65a19-139">Šis pakešuzdevums ir nepieciešams visiem **Resursa pieejamība** skatiem.</span><span class="sxs-lookup"><span data-stu-id="65a19-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="65a19-140">Ja šis pakešuzdevums netiek izpildīts, **ResRollup** dati tiek ģenerēti izveides laikā, kas var prasīt laiku.</span><span class="sxs-lookup"><span data-stu-id="65a19-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]