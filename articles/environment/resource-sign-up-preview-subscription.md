---
title: Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā tēmā ir sniegta informācija par to, kā abonēt un izvietot Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4c2cd4c5d4dfbb95398932d432864cf0d4d5d54d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276852"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="5de83-103">Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem</span><span class="sxs-lookup"><span data-stu-id="5de83-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="5de83-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="5de83-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5de83-105">Šajā tēmā ir izskaidrots, kā abonēt priekšskatījuma/partnera piedāvājumu un izvietot Project Operations vidi scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.</span><span class="sxs-lookup"><span data-stu-id="5de83-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5de83-106">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="5de83-106">Prerequisites</span></span>

- <span data-ttu-id="5de83-107">Jūs saņemsit e-pasta ziņojumu, kurā jūs uzaicinās piedalīties priekšskatījumā.</span><span class="sxs-lookup"><span data-stu-id="5de83-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="5de83-108">Varat pieprasīt priekšskatījumu [Project Operations vietnē](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="5de83-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="5de83-109">Lietotājam, kurš izvieto priekšskatījumu, ir jābūt Azure nomnieka globālā administratora tiesībām.</span><span class="sxs-lookup"><span data-stu-id="5de83-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="5de83-110">Finance vides izvietošanai ir nepieciešams derīgs Azure abonements, kam rēķins tiks izrakstīts par katru vidi.</span><span class="sxs-lookup"><span data-stu-id="5de83-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="5de83-111">Lai sāktu darbu, varat izmantot esošu organizācijas abonementu vai izmantot [Azure izmēģinājumversiju](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="5de83-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="5de83-112">CDS vide tiks nodrošināta bez maksas ierobežotā 30 dienu periodā.</span><span class="sxs-lookup"><span data-stu-id="5de83-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="5de83-113">Abonēt</span><span class="sxs-lookup"><span data-stu-id="5de83-113">Subscribe</span></span>

<span data-ttu-id="5de83-114">Kad jūsu [priekšskatījuma pieprasījums](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) tiks apstiprināts, e-pastā saņemsit trīs piedāvājumus no Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5de83-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="5de83-115">Šie piedāvājumi jums ļauj izvietot Project Operations priekšskatījumu:</span><span class="sxs-lookup"><span data-stu-id="5de83-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="5de83-116">Dynamics 365 Project Operations (CRM) — priekšskatījuma izmēģinājumversija</span><span class="sxs-lookup"><span data-stu-id="5de83-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="5de83-117">Office 365 Project Operations — priekšskatījuma izmēģinājumversija</span><span class="sxs-lookup"><span data-stu-id="5de83-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="5de83-118">Dynamics 365 Finance — priekšskatījuma izmēģinājumversija</span><span class="sxs-lookup"><span data-stu-id="5de83-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5de83-119">Šis uzdevums organizācijā ir jāveic tikai vienai personai, t.i., nomnieka administratoram.</span><span class="sxs-lookup"><span data-stu-id="5de83-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="5de83-120">Ja neesat šī laidiena abonents, nogaidiet, līdz organizācija būs reģistrējusies un būsit saņēmis savus lietotāja akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="5de83-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="5de83-121">Dynamics 365 Project Operations (CRM) — priekšskatījuma izmēģinājumversija</span><span class="sxs-lookup"><span data-stu-id="5de83-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="5de83-122">Pirms sākšanas pārliecinieties, vai esat pieteicies pārlūkprogrammā ar lietotāja darba kontu nomniekā, kurā vēlaties veikt Project Operations priekšskatīšanu.</span><span class="sxs-lookup"><span data-stu-id="5de83-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="5de83-123">Izmantojiet pirmo piedāvājuma kodu **Dynamics 365 Project Operations (CRM) — priekšskatījuma izmēģinājumversija**, ielīmējot to pārlūkprogrammas URL.</span><span class="sxs-lookup"><span data-stu-id="5de83-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Izmantot piedāvājumu](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="5de83-125">Apstipriniet pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5de83-125">Confirm your order.</span></span>

![Pasūtījuma apstiprināšana](./media/17ConfirmOrderNew.png)

<span data-ttu-id="5de83-127">Jūs redzēsit, ka apstiprinājuma piedāvājums ir veiksmīgi izpirkts.</span><span class="sxs-lookup"><span data-stu-id="5de83-127">You will see confirmation offer was successfully redeemed.</span></span>

![Apstiprinājums](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="5de83-129">Office 365 Project Operations — priekšskatījuma izmēģinājumversija</span><span class="sxs-lookup"><span data-stu-id="5de83-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="5de83-130">Veiciet tās pašas darbības kā ar pirmo piedāvājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="5de83-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="5de83-131">Pārliecinieties, vai pievienojat otro piedāvājuma kodu, izmantojot to pašu lietotāja kontu, kas tika izmantots ar pirmo piedāvājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="5de83-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="5de83-132">Dynamics 365 Finance priekšskatījuma izmēģinājumversija</span><span class="sxs-lookup"><span data-stu-id="5de83-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="5de83-133">Atkārtojiet tās pašas darbības pēdējam iepazīšanās e-pasta ziņojumā ietvertajam piedāvājumam.</span><span class="sxs-lookup"><span data-stu-id="5de83-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="5de83-134">Licenču piešķiršana</span><span class="sxs-lookup"><span data-stu-id="5de83-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5de83-135">Lai izpildītu tālāk norādītās darbības, jums ir jābūt administratīvai piekļuvei savas organizācijas Microsoft 365 portālam.</span><span class="sxs-lookup"><span data-stu-id="5de83-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="5de83-136">Dodieties uz [Microsoft 365 administrēšanas centru](https://portal.office.com/), lai piešķirtu licences saviem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="5de83-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Administrēšanas centra sākumlapa](./media/14AdminPortal.png)

2. <span data-ttu-id="5de83-138">Lapā **Aktīvie lietotāji** atlasiet lietotājus, kuriem vēlaties piešķirt licenci.</span><span class="sxs-lookup"><span data-stu-id="5de83-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Licenču piešķiršana](./media/15AssignLicenses.png)

3. <span data-ttu-id="5de83-140">Pārbaudiet, vai ir atlasīta **Dynamics 365 Project Operations (CRM) priekšskatījums** un **Office 365 Project Operations — priekšskatījums** licence, un atlasiet **Saglabāt izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="5de83-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="5de83-141">Finance izmēģinājumversijas piedāvājums nav jāpiešķir lietotājam.</span><span class="sxs-lookup"><span data-stu-id="5de83-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="5de83-142">Jauna projekta sākšana LCS</span><span class="sxs-lookup"><span data-stu-id="5de83-142">Start a new project in LCS</span></span>

<span data-ttu-id="5de83-143">Izveidojiet jaunu LCS projektu, kā aprakstīts tēmā [Jauna projekta sākšana LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="5de83-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="5de83-144">Azure abonementa pievienošana LCS projektam</span><span class="sxs-lookup"><span data-stu-id="5de83-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="5de83-145">Lai izpildītu šo uzdevumu, veiciet darbības, kas aprakstītas tēmā [Azure abonementa pievienošana LCS projektam](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="5de83-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="5de83-146">Finance demonstrācijas vides izvietošana ar Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem</span><span class="sxs-lookup"><span data-stu-id="5de83-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="5de83-147">Lai pabeigtu izvietošanu, izpildiet norādījumus, kas sniegti tēmā [Jaunas vides nodrošināšana](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="5de83-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="5de83-148">Izmantojiet priekšskatījumam [demonstrācijas vides](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) izvietošanas tipu.</span><span class="sxs-lookup"><span data-stu-id="5de83-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="5de83-149">CDS iestatīšanas un konfigurācijas datu instalēšana</span><span class="sxs-lookup"><span data-stu-id="5de83-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="5de83-150">Instalējiet CDS iestatīšanas un konfigurācijas datus, kā aprakstīts tēmā [Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="5de83-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="5de83-151">Pabeidziet šo darbību tikai pēc tam, kad finanšu demonstrācijas vide ir izvietota un demo dati FO ir gatavi.</span><span class="sxs-lookup"><span data-stu-id="5de83-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]