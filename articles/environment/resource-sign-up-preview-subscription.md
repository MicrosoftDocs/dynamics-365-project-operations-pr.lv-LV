---
title: Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā tēmā ir sniegta informācija par to, kā abonēt un izvietot Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948972"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="3b586-103">Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem</span><span class="sxs-lookup"><span data-stu-id="3b586-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="3b586-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="3b586-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3b586-105">Šajā tēmā ir izskaidrots, kā abonēt priekšskatījuma/partnera piedāvājumu un izvietot Project Operations vidi scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.</span><span class="sxs-lookup"><span data-stu-id="3b586-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3b586-106">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="3b586-106">Prerequisites</span></span>

- <span data-ttu-id="3b586-107">Jūs saņemsit e-pasta ziņojumu, kurā jūs uzaicinās piedalīties priekšskatījumā.</span><span class="sxs-lookup"><span data-stu-id="3b586-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="3b586-108">Varat pieprasīt priekšskatījumu [Project Operations vietnē](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="3b586-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="3b586-109">Lietotājam, kurš izvieto priekšskatījumu, ir jābūt Azure nomnieka globālā administratora tiesībām.</span><span class="sxs-lookup"><span data-stu-id="3b586-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="3b586-110">Finance vides izvietošanai ir nepieciešams derīgs Azure abonements, kam rēķins tiks izrakstīts par katru vidi.</span><span class="sxs-lookup"><span data-stu-id="3b586-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="3b586-111">Lai sāktu darbu, varat izmantot esošu organizācijas abonementu vai izmantot [Azure izmēģinājumversiju](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="3b586-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="3b586-112">CDS vide tiks nodrošināta bez maksas ierobežotā 30 dienu periodā.</span><span class="sxs-lookup"><span data-stu-id="3b586-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="3b586-113">Abonēt</span><span class="sxs-lookup"><span data-stu-id="3b586-113">Subscribe</span></span>

<span data-ttu-id="3b586-114">Kad jūsu [priekšskatījuma pieprasījums](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) tiks apstiprināts, e-pastā saņemsit divus piedāvājumus no Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3b586-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="3b586-115">Šie piedāvājumi jums ļauj izvietot Project Operations priekšskatījumu:</span><span class="sxs-lookup"><span data-stu-id="3b586-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="3b586-116">Dynamics 365 Project Operations — priekšskatījuma izmēģinājumversija</span><span class="sxs-lookup"><span data-stu-id="3b586-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="3b586-117">Dynamics 365 for Finance and Operations priekšskatījuma izmēģinājumversija.</span><span class="sxs-lookup"><span data-stu-id="3b586-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b586-118">Šis uzdevums organizācijā ir jāveic tikai vienai personai, t.i., nomnieka administratoram.</span><span class="sxs-lookup"><span data-stu-id="3b586-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="3b586-119">Ja neesat šī laidiena abonents, nogaidiet, līdz organizācija būs reģistrējusies un būsit saņēmis savus lietotāja akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="3b586-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="3b586-120">Dynamics 365 Project Operations — priekšskatījuma izmēģinājumversija</span><span class="sxs-lookup"><span data-stu-id="3b586-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="3b586-121">Izmantojiet pirmo piedāvājumu, **Dynamics 365 Project Operations izmēģinājumversiju**, ar iepazīšanās e-pasta ziņojumā sniegto vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="3b586-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Pirmais piedāvājums](./media/1FirstOffer.png)

2. <span data-ttu-id="3b586-123">Pārbaudiet, vai esat pieteicies kā lietotājs, kurš pieder organizācijai, kas abonēs pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="3b586-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="3b586-124">Pēc tam izmantojiet piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="3b586-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="3b586-125">Atlasiet **Jā, pievienot manam kontam**.</span><span class="sxs-lookup"><span data-stu-id="3b586-125">Select **Yes, add it to my account**.</span></span>

![Izmantot piedāvājumu](./media/2RedeemFirstOffer.png)

![Apstiprināt piedāvājumu](./media/3ConfirmFirstOffer.png)

![Piedāvājums izmantots](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="3b586-129">Dynamics 365 Finance priekšskatījuma izmēģinājumversija</span><span class="sxs-lookup"><span data-stu-id="3b586-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="3b586-130">Atkārtojiet tās pašas darbības otrajam iepazīšanās e-pasta ziņojumā ietvertajam piedāvājumam.</span><span class="sxs-lookup"><span data-stu-id="3b586-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="3b586-131">Licenču piešķiršana</span><span class="sxs-lookup"><span data-stu-id="3b586-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b586-132">Lai izpildītu tālāk norādītās darbības, jums ir jābūt administratīvai piekļuvei savas organizācijas Office 365 portālam.</span><span class="sxs-lookup"><span data-stu-id="3b586-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="3b586-133">Dodieties uz [Microsoft 365 administrēšanas centru](https://portal.office.com/), lai piešķirtu lietotājiem licences.</span><span class="sxs-lookup"><span data-stu-id="3b586-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Office administrēšanas portāls](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="3b586-135">Lapā **Aktīvie lietotāji** atlasiet lietotājus, kuriem vēlaties piešķirt licenci.</span><span class="sxs-lookup"><span data-stu-id="3b586-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Licenču piešķiršana](./media/6AssignLicenses.png)

3. <span data-ttu-id="3b586-137">Pārbaudiet, vai ir atlasīta Project Operations licence, un atlasiet **Saglabāt izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="3b586-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="3b586-138">Finance izmēģinājumversijas piedāvājums nav jāpiešķir lietotājam.</span><span class="sxs-lookup"><span data-stu-id="3b586-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="3b586-139">Jauna projekta sākšana LCS</span><span class="sxs-lookup"><span data-stu-id="3b586-139">Start a new project in LCS</span></span>

<span data-ttu-id="3b586-140">Izveidojiet jaunu LCS projektu, kā aprakstīts tēmā [Jauna projekta sākšana LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="3b586-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="3b586-141">Azure abonementa pievienošana LCS projektam</span><span class="sxs-lookup"><span data-stu-id="3b586-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="3b586-142">Lai izpildītu šo uzdevumu, veiciet darbības, kas aprakstītas tēmā [Azure abonementa pievienošana LCS projektam](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="3b586-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="3b586-143">Finance demonstrācijas vides izvietošana ar Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem</span><span class="sxs-lookup"><span data-stu-id="3b586-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="3b586-144">Lai pabeigtu izvietošanu, izpildiet norādījumus, kas sniegti tēmā [Jaunas vides nodrošināšana](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="3b586-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="3b586-145">Izmantojiet priekšskatījumam [demonstrācijas vides](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) izvietošanas tipu.</span><span class="sxs-lookup"><span data-stu-id="3b586-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="3b586-146">CDS iestatīšanas un konfigurācijas datu instalēšana</span><span class="sxs-lookup"><span data-stu-id="3b586-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="3b586-147">Instalējiet CDS iestatīšanas un konfigurācijas datus, kā aprakstīts tēmā [Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="3b586-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

