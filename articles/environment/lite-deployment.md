---
title: Izvietot projekta operācijas — Lite
description: Šajā tēmā ir sniegta informācija par to, kā instalēt Project Operations Lite izvietošanu — pāreju uz proforma rēķinu izrakstīšanu.
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995540"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="d620e-103">Izvietot projekta operācijas — Lite</span><span class="sxs-lookup"><span data-stu-id="d620e-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="d620e-104">_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_</span><span class="sxs-lookup"><span data-stu-id="d620e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d620e-105">Project Operations atbalsta vairākus izvietošanas modeļus.</span><span class="sxs-lookup"><span data-stu-id="d620e-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="d620e-106">Lai noteiktu labāko izvietošanas modeli, skatiet sadaļu [Izvietošanas tipi](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="d620e-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="d620e-107">Šī izvietošana jeb Lite izvietošana — pāreja uz proforma rēķinu izrakstīšanu, izraisa **Project Operations izvietošanu tikai Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="d620e-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="d620e-108">Project Operations instalēšana jaunā CDS vidē</span><span class="sxs-lookup"><span data-stu-id="d620e-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="d620e-109">Instalēšana esošā CD vidē</span><span class="sxs-lookup"><span data-stu-id="d620e-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="d620e-110">Project Operations instalēšana jaunā CDS vidē</span><span class="sxs-lookup"><span data-stu-id="d620e-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="d620e-111">Kā [Globāls vai Power Platform administrators](/power-platform/admin/global-service-administrators-can-administer-without-license) ar Project Operations licenci izveidojiet jaunu CDS vidi [PowerPlatform administrēšanas centrā](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="d620e-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="d620e-112">Pārliecinieties, ka ir iespējotas opcijas **CDS datu bāze** un **Dynamics 365 programmas**.</span><span class="sxs-lookup"><span data-stu-id="d620e-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="d620e-113">Papildinformāciju skatiet šeit: [Vides izveide un pārvaldība, izmantojot Power Platform administrēšanas centru](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="d620e-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="d620e-114">Dynamics 365 programmu izvietošanas sarakstā atlasiet **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="d620e-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="d620e-115">Project Operations instalēšana esošā CDS vidē</span><span class="sxs-lookup"><span data-stu-id="d620e-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="d620e-116">Kā [Globāls vai Power Platform administrators](/power-platform/admin/global-service-administrators-can-administer-without-license) ar Project Operations licenci atrodiet vidi [PowerPlatform administrēšanas centrā](https://admin.powerplatform.com), kur vēlaties instalēt Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d620e-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="d620e-117">Instalējiet **Microsoft Dynamics 365 Project Operations** no Dynamics 365 programmu izvietošanas saraksta.</span><span class="sxs-lookup"><span data-stu-id="d620e-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="d620e-118">Papildinformāciju skatiet šeit: [Dynamics Dynamics 365 programmu pārvaldība](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="d620e-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]