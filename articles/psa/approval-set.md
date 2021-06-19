---
title: Apstiprināšanas kopas
description: Šajā tēmā ir sniegta informācija par apstiprināšanas kopu, pieprasījumiem un šo darbību apakškopām.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116880"
---
# <a name="approval-sets"></a><span data-ttu-id="effd8-103">Apstiprināšanas kopas</span><span class="sxs-lookup"><span data-stu-id="effd8-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="effd8-104">Apstiprināšanas kopas sagrupē apstiprinājuma pieprasījumus mazākās darbību apakškopās.</span><span class="sxs-lookup"><span data-stu-id="effd8-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="effd8-105">Šī grupēšana ļauj apstrādāt apstiprinājumus pasūtījumā pēc projekta, kā arī ļauj atkārtotus mēģinājumus un secības noteikšanu.</span><span class="sxs-lookup"><span data-stu-id="effd8-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="effd8-106">Grupēšana uzlabo apstiprināšanas apstrādes uzticamību un izsekojamību lielam apstiprinājumu apjomam.</span><span class="sxs-lookup"><span data-stu-id="effd8-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="effd8-107">Apstiprināšanas kopas parāda saistīto ierakstu kopējo apstrādes stāvokli.</span><span class="sxs-lookup"><span data-stu-id="effd8-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="effd8-108">Kad apstiprinājuma ieraksts tiek apstrādāts, izmantojot apstiprināšanas kopu, ieraksts tiek pārvietots no **Iesniegts** uz **Apstiprināts** un tiek atsaistīts no apstiprināšanas kopas.</span><span class="sxs-lookup"><span data-stu-id="effd8-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="effd8-109">Ja, iesniedzot apstiprināšanai, ieraksts ir nesekmīgs, tam tiek saglabāts statuss **Iesniegts**, un apstiprināšanas kopa tiek atzīmēta kā nesekmīga.</span><span class="sxs-lookup"><span data-stu-id="effd8-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="effd8-110">Apstiprināšanas kopa reģistrē kļūmes kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="effd8-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="effd8-111">Apstiprinājumu un apstiprināšanas kopu apstrāde</span><span class="sxs-lookup"><span data-stu-id="effd8-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="effd8-112">Apstiprinājumi, kas ir ievietoti rindā apstrādei, ir redzami skatā **Apstiprinājumu apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="effd8-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="effd8-113">Sistēma mēģina apstrādāt visus ierakstus vairākas reizes asinhroni, tostarp mēģina vēlreiz veikt apstiprināšanu, ja iepriekšējie mēģinājumi nav izdevušies.</span><span class="sxs-lookup"><span data-stu-id="effd8-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="effd8-114">Laukā **Apstiprināšanas kopas darbmūžs** tiek reģistrēts atlikušais kopas apstrādes mēģinājumu skaits, pirms tā tiek atzīmēta kā nesekmīga.</span><span class="sxs-lookup"><span data-stu-id="effd8-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="effd8-115">Nesekmīgi apstiprinājumi un apstiprināšanas kopas</span><span class="sxs-lookup"><span data-stu-id="effd8-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="effd8-116">Skatā **Nesekmīgie apstiprinājumi** ir uzskaitīti visi apstiprinājums, kam nepieciešama lietotāja iejaukšanās.</span><span class="sxs-lookup"><span data-stu-id="effd8-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="effd8-117">Atveriet saistītos apstiprināšanas kopu žurnālus, lai noteiktu kļūmes iemeslu.</span><span class="sxs-lookup"><span data-stu-id="effd8-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="effd8-118">Atlasot **Mēģināt vēlreiz**, tiek palielināts apstiprināšanas kopas darbmūža rādītājs, apstiprināšanas kopai tiek atjaunots statuss **Apstrādā**, un notiek mēģinājums apstrādāt atlikušos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="effd8-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="effd8-119">Apstiprināšanas kopu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="effd8-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="effd8-120">Apstiprināšanas kopu līdzekļa iespējošana</span><span class="sxs-lookup"><span data-stu-id="effd8-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="effd8-121">Pirms apstiprināšanas kopu līdzekļa iespējošanas pārliecinieties, vai pašlaik netiek apstrādāts neviens apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="effd8-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="effd8-122">Dodieties uz lapu **Projekta parametri** un atlasiet **Līdzekļu vadība** > **Iespējot mūsdienīgos apstiprinājumus**.</span><span class="sxs-lookup"><span data-stu-id="effd8-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="effd8-123">Apstiprināšanas kopu līdzekļa izslēgšana</span><span class="sxs-lookup"><span data-stu-id="effd8-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="effd8-124">Pirms apstiprināšanas kopu līdzekļa izslēgšanas pārliecinieties, vai pašlaik netiek apstrādāts neviens apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="effd8-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="effd8-125">Dodieties uz lapu **Projekta parametri** un atlasiet **Līdzekļu vadība** > **Atspējot mūsdienīgos apstiprinājumus**.</span><span class="sxs-lookup"><span data-stu-id="effd8-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="effd8-126">Asinhronā sliekšņa konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="effd8-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="effd8-127">Veidojot apstiprināšanas kopas, apstrāde tiek pārcelta fonā, kad atlasītais apstiprināšanai izvēlēto ierakstu skaits pārsniedz norādīto robežvērtību.</span><span class="sxs-lookup"><span data-stu-id="effd8-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="effd8-128">Izmantojiet lauku **Asinhronais slieksnis**, lai konfigurētu, kad apstiprinājumu apstrāde jāveic sinhroni vai asinhroni.</span><span class="sxs-lookup"><span data-stu-id="effd8-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="effd8-129">Derīgas vērtības ir:</span><span class="sxs-lookup"><span data-stu-id="effd8-129">Valid values are:</span></span>

  - <span data-ttu-id="effd8-130">nulle: visi pieprasījumi ir jāapstrādā asinhroni;</span><span class="sxs-lookup"><span data-stu-id="effd8-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="effd8-131">skaitļi, kas ir lielāki par nulli: apstiprinājumus apstrādā asinhroni tikai tad, ja iesniegto apstiprinājumu skaits pārsniedz šo vērtību.</span><span class="sxs-lookup"><span data-stu-id="effd8-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
