---
title: Navigācija risinājumā Project Operations
description: Šajā tēmā ir sniegta informācija par to, kā piekļūt risinājumam Project Operations no Lifecycle Services.
author: sigitac
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d948c1cfe2d95e61f2405a9a23e7045af678ae40
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642057"
---
# <a name="navigate-project-operations"></a><span data-ttu-id="8dc23-103">Navigācija risinājumā Project Operations</span><span class="sxs-lookup"><span data-stu-id="8dc23-103">Navigate Project Operations</span></span>

<span data-ttu-id="8dc23-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="8dc23-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8dc23-105">Dynamics 365 Project Operations resursu/bez krājumu scenāriji sastāv no diviem komponentiem.</span><span class="sxs-lookup"><span data-stu-id="8dc23-105">Dynamics 365 Project Operations for resource/non-stocked scenarios consists of two components:</span></span> 

 - <span data-ttu-id="8dc23-106">**Project Operations pakalpojuma Common Data Service (CDS) vidē**: šis komponents aptver iespējas un procesus, sākot no iespējas līdz pro forma rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="8dc23-106">**Project Operations on Common Data Service (CDS) environment**: This component covers capabilities and processes from opportunity to proforma invoicing.</span></span> 
 - <span data-ttu-id="8dc23-107">**Projektu pārvaldība un uzskaite Dynamics 365 Finance vidē**: šis komponents aptver izdevumu pārvaldības iespējas, projektu uzskaiti un ieņēmumu atzīšanu.</span><span class="sxs-lookup"><span data-stu-id="8dc23-107">**Project management and accounting on Dynamics 365 Finance environment**: This component covers expense management capabilities, project accounting, and revenue recognition.</span></span> 

<span data-ttu-id="8dc23-108">Kad esat nodrošinājis Project Operations, kā aprakstīts šajā tēmā, risinājuma Lifecycle Services (LCS) lapa **Vides informācija** nodrošina ērtu piekļuvi abiem Project Operations komponentiem.</span><span class="sxs-lookup"><span data-stu-id="8dc23-108">After you provision Project Operations as described in this topic, the Lifecycle Services (LCS) **Environment details** page provides easy access to both components of Project Operations.</span></span>  

<span data-ttu-id="8dc23-109">Izmantojiet vides nosaukumu sadaļā **Common Data Service Vides nosaukums**, lai pārietu uz Project Operations vidē CDS.</span><span class="sxs-lookup"><span data-stu-id="8dc23-109">Use the environment name in the section, **Common Data Service Environment Name** to navigate to Project Operations on a CDS environment.</span></span> 

  ![Common Data Service vides nosaukums](./media/environment-name.PNG)

<span data-ttu-id="8dc23-111">Atlasiet **Pieteikties** > **Pieteikties vidē**, lai pārietu uz moduli **Projektu pārvaldība un grāmatvedība**, kas atrodas Finansēs.</span><span class="sxs-lookup"><span data-stu-id="8dc23-111">Select **Login** > **Log on to environment** to navigate to the **Project management and accounting** module in Finance.</span></span>  

   ![Pieteikšanās sadaļā Finanses](./media/environment-login.PNG)

> [!NOTE]
> <span data-ttu-id="8dc23-113">Project Operations var piekļūt Common Data Service un tieši modulī **Projektu pārvaldība un uzskaite**, izmantojot atbilstošos vietrāžus URL.</span><span class="sxs-lookup"><span data-stu-id="8dc23-113">You can access Project Operations in the Common Data Service and the **Project management and accounting** module directly by using their respective URLs.</span></span> 