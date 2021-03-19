---
title: Project Operations integrācijas konfigurēšana katrā juridiskā entītijā
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt juridisku entītiju integrāciju programmā Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ccdbdce6b7d006adc9be2b5f3573dd8e79dd2b8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276987"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="d06c0-103">Project Operations integrācijas konfigurēšana katrā juridiskā entītijā</span><span class="sxs-lookup"><span data-stu-id="d06c0-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="d06c0-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="d06c0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d06c0-105">Šajā tēmā ir soļi, kas nepieciešami, lai konfigurētu Dynamics 365 Project Operations katru juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="d06c0-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="d06c0-106">Pamatlīdzekļu iespējošana risinājumā Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="d06c0-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="d06c0-107">Lai iespējotu nepieciešamos līdzekļus, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d06c0-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="d06c0-108">Risinājumā Dynamics 365 Finance dodieties uz darbvietu **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="d06c0-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="d06c0-109">Laukā **Līdzekļu saraksts** atrodiet un iespējojiet tālāk norādītos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="d06c0-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="d06c0-110">**Iespējot vairākas projekta līguma rindas**</span><span class="sxs-lookup"><span data-stu-id="d06c0-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="d06c0-111">**Project Operations iespējošana risinājumā Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="d06c0-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="d06c0-112">Ja sarakstā nav norādīti **Pamatlīdzekļi**, pārbaudiet, vai jūsu finanšu versija atbilst minimālās versijas prasībai (programmas versija 10.0.13 ar visiem piemērotajiem vai augstākajiem kvalitātes atjauninājumiem).</span><span class="sxs-lookup"><span data-stu-id="d06c0-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="d06c0-113">Atlasiet **Pārbaudīt, vai nav atjauninājumu**, lai atsvaidzinātu līdzekļu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="d06c0-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="d06c0-114">Project Operations izvietošanas scenārija definēšana juridiskai entītijai</span><span class="sxs-lookup"><span data-stu-id="d06c0-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="d06c0-115">Project Operations var iespējot risinājuma Dynamics 365 Customer Engagement juridiskās entītijas līmenī.</span><span class="sxs-lookup"><span data-stu-id="d06c0-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="d06c0-116">Var būt viena juridiskā entītija, kas izmanto Project Operations risinājumā Dynamics 365 Customer Engagement scenārijiem, kas nav balstīti uz resursiem/krājumiem.</span><span class="sxs-lookup"><span data-stu-id="d06c0-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="d06c0-117">Tajā pašā vidē var būt cita juridiska entītija, kas izmanto Project Operations, kas balstīti uz krājumiem un ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="d06c0-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="d06c0-118">Risinājumā Dynamics 365 Finance dodieties uz **Projektu pārvaldība un uzskaite** > **Iestatīšana** > **Globālie projektu pārvaldības un uzskaites parametri**.</span><span class="sxs-lookup"><span data-stu-id="d06c0-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="d06c0-119">Pieejamo juridisko entītiju sarakstā atlasiet entītijas, kurās ir iespējotas vairākas līguma rindas un Project Operations risinājumā Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="d06c0-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="d06c0-120">Atstājiet juridiskas entītijas, kas izmantos neatlasītus Project Operations scenārijus, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="d06c0-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="d06c0-121">Juridisku entītiju var atlasīt tikai tad, ja tai nav esošu projektu.</span><span class="sxs-lookup"><span data-stu-id="d06c0-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="d06c0-122">Projekta pārvaldības un uzskaites parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d06c0-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="d06c0-123">Katrai juridiskajai entītijai, kas izmanto Project Operations risinājumā Dynamics 365 Customer Engagement, ir nepieciešamas noklusējuma parametru kopas.</span><span class="sxs-lookup"><span data-stu-id="d06c0-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="d06c0-124">Šie parametri ir konfigurēti **Project Operations** cilnes lapā **Projekta pārvaldības un uzskaites parametri**.</span><span class="sxs-lookup"><span data-stu-id="d06c0-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="d06c0-125">Ir šādi parametri:</span><span class="sxs-lookup"><span data-stu-id="d06c0-125">The parameters are:</span></span>

  - <span data-ttu-id="d06c0-126">**Rēķina tipa noklusējuma iestatījumi**: Project Operations izmanto fiksētu norēķinu tipa noklusējuma kopu, kas ir jākartē uz rindas rekvizītu finansēm.</span><span class="sxs-lookup"><span data-stu-id="d06c0-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="d06c0-127">Ierakstu izveide katram norēķinu tipam: **Nav norādīts**, **Rēķinā iekļaujams**, **Rēķinā neiekļaujams**, **Bezmaksas** un **Nav pieejams**.</span><span class="sxs-lookup"><span data-stu-id="d06c0-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="d06c0-128">**Projekta kategorijas noklusējumi**: atlasiet noklusējuma projekta kategorijas, kas jāizmanto katram transakcijas tipam.</span><span class="sxs-lookup"><span data-stu-id="d06c0-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="d06c0-129">Šie noklusējuma iestatījumi tiks lietoti **Project Operations integrācijas žurnālā** un aprēķinos, kur projekta faktiskajai transakcijai nav norādīta transakciju kategorija.</span><span class="sxs-lookup"><span data-stu-id="d06c0-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="d06c0-130">**Prognozes**: atlasiet budžeta modeli, kas tiks izmantots laika un izdevumu novērtējumiem.</span><span class="sxs-lookup"><span data-stu-id="d06c0-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]