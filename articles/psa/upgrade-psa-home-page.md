---
title: Jaunināšanas sākumlapa
description: Šajā tēmā parādīts, kur meklēt svarīgu informāciju par jaunām un izmainītām funkcijām programmā Dynamics 365 Project Service Automation, kā arī par procesu jaunināšanai uz jaunāko versiju.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
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
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121767"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="4ad8d-103">Jaunināšanas sākumlapa</span><span class="sxs-lookup"><span data-stu-id="4ad8d-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="4ad8d-104">Jaunināšana no PSA versijas 2.x vai 1.x uz versiju 3.x</span><span class="sxs-lookup"><span data-stu-id="4ad8d-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="4ad8d-105">Jaunas instances</span><span class="sxs-lookup"><span data-stu-id="4ad8d-105">New instances</span></span>

<span data-ttu-id="4ad8d-106">No 2019. gada 17. maija, atlasot Project Service Automation jaunas instances nodrošināšanas laikā, versija 3.x tiek instalēta pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="4ad8d-107">Esošās instances</span><span class="sxs-lookup"><span data-stu-id="4ad8d-107">Existing instances</span></span>

<span data-ttu-id="4ad8d-108">Iepriekš klienti, kam ir PSA versijas 2.x instance un kam tā jājaunina uz versiju 3.x, kas ir Apvienotā uz klienta interfeisa balstītā (UCI) PSA versija, bija jāsazinās ar Microsoft atbalsta dienestu un jāsniedz papildinformācija par savu instanci, lai atbalsts varētu palīdzēt veikt jaunināšanu uz versiju 3.x.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="4ad8d-109">Sākot ar 2020. gada 1. martu klienti, kam ir PSA versijas 2.x instance un kam tā jājaunina uz versiju 3.x, varēs jaunināt savas instances tieši no administratora portāla, un viņiem nebūs jāsazinās ar Microsoft atbalsta dienestu.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ad8d-110">PSA versija 3.x ietver būtiskas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="4ad8d-111">Tā ir izveidota, izmantojot vienotā interfeisa struktūru, lai palīdzētu nodrošināt uzlabotu lietotāja pieredzi.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="4ad8d-112">Pārveidotajā lietojumprogrammā ir nodrošināts konsekvents, vienots lietotāja interfeiss (UI), kā arī reaģējošie noformējuma principi optimālai skatīšanai jebkāda izmēra ekrānā vai ierīcē.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="4ad8d-113">Lietojumprogrammā ir veiktas arī citas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="4ad8d-114">Daži no izmainītajiem apgabaliem ietver cenu noteikšanu, rezervāciju un resursu piešķiršanu, laiku, izdevumus un apstiprinājumus.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="4ad8d-115">Pirms jaunināšanas procesa sākšanas ieteicams izpildīt tālāk norādītos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="4ad8d-116">Pārbaudiet, vai Dynamics 365 Field Service un Project Service Automation ir instalēti noteiktajā instancē.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="4ad8d-117">Ja ir instalēti abi risinājumi, jums ir jāplāno to jaunināšana, pirms atsākat regulāru instances lietošanu.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="4ad8d-118">Rūpīgi pārskatiet tālāk norādītās tēmas.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-118">Carefully review the following topics.</span></span> <span data-ttu-id="4ad8d-119">Izpratne par izmaiņām versijās palīdzēs jums jaunināšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="4ad8d-120">Šīs tēmas sniedz informāciju par lielākajām izmaiņām programmā PSA kopā ar apsvērumiem un ieteikumiem, lai plānotu jaunināšanu uz versiju 3. x.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="4ad8d-121">Kas jauns vai mainīts Project Service Automation 3. versijā</span><span class="sxs-lookup"><span data-stu-id="4ad8d-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="4ad8d-122">Jaunināšanas apsvērumi – Project Service Automation versijas 2.x vai 1.x uz versiju 3.x</span><span class="sxs-lookup"><span data-stu-id="4ad8d-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="4ad8d-123">Jauniniet savu smilškastes instanci, lai novērtētu veiktās ieviešanas izmaiņas pirms ražošanas instances jaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="4ad8d-124">Pēc tam, kad būsit pārskatījis jau iepriekš minētās tēmas un esat gatavs veikt jaunināšanu uz PSA versiju 3.x vai uz UCI balstītu versiju, iesniedziet pieprasījumu Microsoft atbalstam, lai padarītu jaunināšanu pieejamu no administratora centra.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="4ad8d-125">Pieprasījumā norādiet detalizētu informāciju par savu instanci.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="4ad8d-126">Vecāku versiju PSA (PSA versija 2.x) no jauna izveidotajā instancē</span><span class="sxs-lookup"><span data-stu-id="4ad8d-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="4ad8d-127">No 2019. gada 17. maija visas jaunās instancēs UCI būs iekļauts kā noklusējuma klients.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="4ad8d-128">Attiecībā uz saskaņošanu ar šīm izmaiņām, PSA versija 3.x un Field Service versija 8.x tiks nodrošinātas pēc noklusējuma, jo šīs versijas ir paredzētas darbam ar UCI klientu.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="4ad8d-129">Sākot ar 2020. gada 1. martu Dynamics PSA klienti vairs nevarēs izveidot jaunas vides, izmantojot vecākas PSA versijas, piemēram, PSA versiju 2.x vai vecāku.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="4ad8d-130">Jebkura jaunā vide būs pieejama tikai ar PSA versiju 3.x.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="4ad8d-131">Lai varētu izmantot labākās iespējas, lietojot vecākas Field Service un PSA lietojumprogrammu versijas, pārejiet uz lapu **Sistēmas iestatījumi** un laukam **Izmantot tikai jauno vienoto interfeisu (ieteicams)** atlasiet **Nē**, jo šīs versijas nav paredzētas pareizai ielādēšanai UCI.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="4ad8d-132">Pēc UCI izslēgšanas varat atvērt un palaist šīs Field Service un PSA versijas, izmantojot veco tīmekļa klientu.</span><span class="sxs-lookup"><span data-stu-id="4ad8d-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
