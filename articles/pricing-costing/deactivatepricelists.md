---
title: Cenrāžu deaktivēšana
description: Šajā tēmā izskaidrots, kā deaktivizēt vai noņemt nelietotus vai vecus cenrāžus.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001345"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="a1fef-103">Cenrāžu deaktivēšana</span><span class="sxs-lookup"><span data-stu-id="a1fef-103">Deactivate price lists</span></span> 

<span data-ttu-id="a1fef-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="a1fef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a1fef-105">Lai noņemtu vecos vai neizmantotos cenrāžus no Dynamics 365 Project Operations, ir jāveic divas darbības.</span><span class="sxs-lookup"><span data-stu-id="a1fef-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="a1fef-106">Noņemiet vai dzēsiet cenrādi no noteiktām lapām.</span><span class="sxs-lookup"><span data-stu-id="a1fef-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="a1fef-107">Deaktivizējiet vai izdzēsiet cenrādi no cenrāža lapas **Cenrāži** aktīvajiem cenrāžiem.</span><span class="sxs-lookup"><span data-stu-id="a1fef-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="a1fef-108">Lai pilnībā noņemtu cenrādi, ir jāveic abas darbības.</span><span class="sxs-lookup"><span data-stu-id="a1fef-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="a1fef-109">Nepietiek tikai ar 2. darbību, ar kuru tiek tieši dzēsts vai deaktivizēts cenrādis skatā Aktīvie cenrāži.</span><span class="sxs-lookup"><span data-stu-id="a1fef-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="a1fef-110">Jums ir arī jāizdzēš šī cenrāža saistība no visām 1. darbībā minētajām vietām.</span><span class="sxs-lookup"><span data-stu-id="a1fef-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="a1fef-111">Cenrāža dzēšana konkrētās lapās</span><span class="sxs-lookup"><span data-stu-id="a1fef-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="a1fef-112">Lai programmā Project Operations dzēstu cenrādi, atveriet tākāk minētās lapas.</span><span class="sxs-lookup"><span data-stu-id="a1fef-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="a1fef-113">Lapa **Projekta parametri** > cilne **Cenrāži**</span><span class="sxs-lookup"><span data-stu-id="a1fef-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="a1fef-114">Lapa **Organizācijas vienība** > režģis **Cenrāži**</span><span class="sxs-lookup"><span data-stu-id="a1fef-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="a1fef-115">Lapa **Konts** > režģis **Projekta cenrāži**</span><span class="sxs-lookup"><span data-stu-id="a1fef-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="a1fef-116">Lapa **Projekta piedāvājumi** > režģis **Projekta cenrāži**: šis attiecas uz visiem aktīvajiem projekta piedāvājumiem.</span><span class="sxs-lookup"><span data-stu-id="a1fef-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="a1fef-117">Lapa **Projekta līgumi** > režģis **Projekta cenrāži**: šis attiecas uz visiem aktīvajiem projekta līgumiem.</span><span class="sxs-lookup"><span data-stu-id="a1fef-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="a1fef-118">Katrai lapai ir jāatlasa cenrādis, ko vēlaties dzēst, un pēc tam jāatlasa **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="a1fef-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="a1fef-119">Cenrāža dzēšana vai deaktivizēšana lapā Cenrāži</span><span class="sxs-lookup"><span data-stu-id="a1fef-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="a1fef-120">Lai dzēstu cenrādi no aktīvajiem cenrāžiem, atveriet **Pārdošana** > **Klienti** > **Cenrāži**.</span><span class="sxs-lookup"><span data-stu-id="a1fef-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="a1fef-121">Atlasiet cenrādi, kuru vēlaties dzēst, un pēc tam atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="a1fef-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="a1fef-122">Ja uz cenrādi ir atsauce uz esošām transakcijām, to nevarēs dzēst.</span><span class="sxs-lookup"><span data-stu-id="a1fef-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="a1fef-123">Šādā gadījumā cenrādi var deaktivizēt tā, lai tas nebūtu redzams skatos.</span><span class="sxs-lookup"><span data-stu-id="a1fef-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="a1fef-124">Lai deaktivizētu cenrādi, vēlreiz atlasiet cenrādi un pēc tam atlasiet **Deaktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="a1fef-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
