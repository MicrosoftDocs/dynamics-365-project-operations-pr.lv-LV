---
title: Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā tēmā ir sniegta informācija par to, kā abonēt un izvietot Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334836"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="cbfef-103">Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem</span><span class="sxs-lookup"><span data-stu-id="cbfef-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="cbfef-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="cbfef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="cbfef-105">Šajā tēmā izskaidrots, kā pierakstīties izmēģinājumversijas piedāvājumam un izvietot Project Operations vidi resursos /noliktavā neesošos krājumos balstītiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="cbfef-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cbfef-106">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="cbfef-106">Prerequisites</span></span>
- <span data-ttu-id="cbfef-107">Lietotājam, kurš izvieto priekšskatījumu, ir jābūt Azure nomnieka globālā administratora tiesībām.</span><span class="sxs-lookup"><span data-stu-id="cbfef-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="cbfef-108">Pirmā piedāvājuma izmantošanas laikā var izveidot nomnieku.</span><span class="sxs-lookup"><span data-stu-id="cbfef-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="cbfef-109">Finance vides izvietošanai ir nepieciešams derīgs Azure abonements, kam rēķins tiks izrakstīts par katru vidi.</span><span class="sxs-lookup"><span data-stu-id="cbfef-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="cbfef-110">Lai sāktu darbu, varat izmantot esošu organizācijas abonementu vai izmantot [Azure izmēģinājumversiju](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="cbfef-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="cbfef-111">CDS vide tiks nodrošināta bez maksas ierobežotā 30 dienu periodā.</span><span class="sxs-lookup"><span data-stu-id="cbfef-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbfef-112">Šis uzdevums organizācijā ir jāveic tikai vienai personai, t.i., nomnieka administratoram.</span><span class="sxs-lookup"><span data-stu-id="cbfef-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="cbfef-113">Ja neesat šī laidiena abonents, nogaidiet, līdz organizācija būs reģistrējusies un būsit saņēmis savus lietotāja akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="cbfef-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="cbfef-114">Izmēģinājumversijas nomnieka statusā ir vienreizējai lietošanai.</span><span class="sxs-lookup"><span data-stu-id="cbfef-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="cbfef-115">Izmēģinājumversiju var palaist tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="cbfef-115">You can only run a trial one time.</span></span> <span data-ttu-id="cbfef-116">Izmēģinājumversijas nolūkiem ieteicams izveidot jaunu nomnieku.</span><span class="sxs-lookup"><span data-stu-id="cbfef-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="cbfef-117">Dynamics 365 Project Operations (CE) — izmēģinājumversijas priekšskatīšana</span><span class="sxs-lookup"><span data-stu-id="cbfef-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="cbfef-118">Pirms sākšanas pārliecinieties, vai esat pieteicies pārlūkprogrammā ar lietotāja darba kontu nomniekā, kurā vēlaties veikt Project Operations priekšskatīšanu.</span><span class="sxs-lookup"><span data-stu-id="cbfef-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="cbfef-119">Izmantojiet pirmo piedāvājuma kodu **Dynamics 365 Project Operations** šeit [Project Operations izmēģinājumversija](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="cbfef-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="cbfef-120">Apstipriniet pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="cbfef-120">Confirm your order.</span></span>

  <span data-ttu-id="cbfef-121">Jūs redzēsit, ka apstiprinājuma piedāvājums ir veiksmīgi izpirkts.</span><span class="sxs-lookup"><span data-stu-id="cbfef-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="cbfef-122">Dynamics 365 Finance priekšskatījuma izmēģinājumversija</span><span class="sxs-lookup"><span data-stu-id="cbfef-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="cbfef-123">Dodieties uz sadaļu [Dynamics 365 for Finance izmēģinājumversijas priekšskatījums](https://aka.ms/trypoche) un atkārtojiet iepriekšējā sadaļā norādītās darbības piedāvājumam Reģistrēšanās mākonī viesotai videi.</span><span class="sxs-lookup"><span data-stu-id="cbfef-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="cbfef-124">Licenču piešķiršana</span><span class="sxs-lookup"><span data-stu-id="cbfef-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbfef-125">Lai izpildītu tālāk norādītās darbības, jums ir jābūt administratīvai piekļuvei savas organizācijas Microsoft 365 portālam.</span><span class="sxs-lookup"><span data-stu-id="cbfef-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="cbfef-126">Dodieties uz [Microsoft 365 administrēšanas centru](https://portal.office.com/), lai piešķirtu licences saviem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="cbfef-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="cbfef-127">Lapā **Aktīvie lietotāji** atlasiet lietotājus, kuriem vēlaties piešķirt licenci.</span><span class="sxs-lookup"><span data-stu-id="cbfef-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="cbfef-128">Pārbaudiet, vai ir atlasīta **Dynamics 365 Project Operations** licence un atlasiet **Saglabāt izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="cbfef-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="cbfef-129">Finance izmēģinājumversijas piedāvājums nav jāpiešķir lietotājam.</span><span class="sxs-lookup"><span data-stu-id="cbfef-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="cbfef-130">Jauna projekta sākšana LCS</span><span class="sxs-lookup"><span data-stu-id="cbfef-130">Start a new project in LCS</span></span>

<span data-ttu-id="cbfef-131">Izveidojiet jaunu LCS projektu, kā aprakstīts tēmā [Jauna projekta sākšana LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="cbfef-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="cbfef-132">Azure abonementa pievienošana LCS projektam</span><span class="sxs-lookup"><span data-stu-id="cbfef-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="cbfef-133">Lai izpildītu šo uzdevumu, veiciet darbības, kas aprakstītas tēmā [Azure abonementa pievienošana LCS projektam](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="cbfef-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="cbfef-134">Finance demonstrācijas vides izvietošana ar Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem</span><span class="sxs-lookup"><span data-stu-id="cbfef-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="cbfef-135">Lai pabeigtu izvietošanu, izpildiet norādījumus, kas sniegti tēmā [Jaunas vides nodrošināšana](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="cbfef-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="cbfef-136">Izmantojiet priekšskatījumam [demonstrācijas vides](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) izvietošanas tipu.</span><span class="sxs-lookup"><span data-stu-id="cbfef-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="cbfef-137">CDS iestatīšanas un konfigurācijas datu instalēšana</span><span class="sxs-lookup"><span data-stu-id="cbfef-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="cbfef-138">Instalējiet CDS iestatīšanas un konfigurācijas datus, kā aprakstīts tēmā [Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="cbfef-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="cbfef-139">Pabeidziet šo darbību tikai pēc tam, kad Ir Finance demonstrācijas vide ir izvietota un demonstrācijas dati ir gatavi.</span><span class="sxs-lookup"><span data-stu-id="cbfef-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
