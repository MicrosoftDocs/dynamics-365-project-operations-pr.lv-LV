---
title: Cenrāžu deaktivēšana
description: Šajā tēmā izskaidrots, kā deaktivizēt vai noņemt nelietotus vai vecus cenrāžus.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701952"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="3930f-103">Cenrāžu deaktivēšana</span><span class="sxs-lookup"><span data-stu-id="3930f-103">Deactivate price lists</span></span> 

<span data-ttu-id="3930f-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="3930f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3930f-105">Lai noņemtu vecos vai neizmantotos cenrāžus no Dynamics 365 Project Operations, ir jāveic divas darbības.</span><span class="sxs-lookup"><span data-stu-id="3930f-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="3930f-106">Noņemiet vai dzēsiet cenrādi no noteiktām lapām.</span><span class="sxs-lookup"><span data-stu-id="3930f-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="3930f-107">Deaktivizējiet vai izdzēsiet cenrādi no cenrāža lapas **Cenrāži** aktīvajiem cenrāžiem.</span><span class="sxs-lookup"><span data-stu-id="3930f-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="3930f-108">Lai pilnībā noņemtu cenrādi, ir jāveic abas darbības.</span><span class="sxs-lookup"><span data-stu-id="3930f-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="3930f-109">Nepietiek tikai ar 2. darbību, ar kuru tiek tieši dzēsts vai deaktivizēts cenrādis skatā Aktīvie cenrāži.</span><span class="sxs-lookup"><span data-stu-id="3930f-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="3930f-110">Jums ir arī jāizdzēš šī cenrāža saistība no visām 1. darbībā minētajām vietām.</span><span class="sxs-lookup"><span data-stu-id="3930f-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="3930f-111">Cenrāža dzēšana konkrētās lapās</span><span class="sxs-lookup"><span data-stu-id="3930f-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="3930f-112">Lai programmā Project Operations dzēstu cenrādi, atveriet tākāk minētās lapas.</span><span class="sxs-lookup"><span data-stu-id="3930f-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="3930f-113">Lapa **Projekta parametri** > cilne **Cenrāži**</span><span class="sxs-lookup"><span data-stu-id="3930f-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="3930f-114">Lapa **Organizācijas vienība** > režģis **Cenrāži**</span><span class="sxs-lookup"><span data-stu-id="3930f-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="3930f-115">Lapa **Konts** > režģis **Projekta cenrāži**</span><span class="sxs-lookup"><span data-stu-id="3930f-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="3930f-116">Lapa **Projekta piedāvājumi** > režģis **Projekta cenrāži**: šis attiecas uz visiem aktīvajiem projekta piedāvājumiem.</span><span class="sxs-lookup"><span data-stu-id="3930f-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="3930f-117">Lapa **Projekta līgumi** > režģis **Projekta cenrāži**: šis attiecas uz visiem aktīvajiem projekta līgumiem.</span><span class="sxs-lookup"><span data-stu-id="3930f-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="3930f-118">Katrai lapai ir jāatlasa cenrādis, ko vēlaties dzēst, un pēc tam jāatlasa **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="3930f-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="3930f-119">Cenrāža dzēšana vai deaktivizēšana lapā Cenrāži</span><span class="sxs-lookup"><span data-stu-id="3930f-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="3930f-120">Lai dzēstu cenrādi no aktīvajiem cenrāžiem, atveriet **Pārdošana** > **Klienti** > **Cenrāži**.</span><span class="sxs-lookup"><span data-stu-id="3930f-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="3930f-121">Atlasiet cenrādi, kuru vēlaties dzēst, un pēc tam atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="3930f-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="3930f-122">Ja uz cenrādi ir atsauce uz esošām transakcijām, to nevarēs dzēst.</span><span class="sxs-lookup"><span data-stu-id="3930f-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="3930f-123">Šādā gadījumā cenrādi var deaktivizēt tā, lai tas nebūtu redzams skatos.</span><span class="sxs-lookup"><span data-stu-id="3930f-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="3930f-124">Lai deaktivizētu cenrādi, vēlreiz atlasiet cenrādi un pēc tam atlasiet **Deaktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="3930f-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
