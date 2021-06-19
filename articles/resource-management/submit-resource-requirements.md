---
title: Submit a resource request
description: Ģenerētu resursa prasību varat iesniegt kā resursa pieprasījumu. Pēc tam šis pieprasījums tiek nosūtīts izpildei resursu pārvaldniekam.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014035"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="90aa4-104">Submit a resource request</span><span class="sxs-lookup"><span data-stu-id="90aa4-104">Submit a resource request</span></span>

<span data-ttu-id="90aa4-105">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="90aa4-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="90aa4-106">Ģenerētu resursa prasību varat iesniegt kā resursa pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="90aa4-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="90aa4-107">Pēc tam šis pieprasījums tiek nosūtīts izpildei resursu pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="90aa4-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="90aa4-108">Programmas Dynamics 365 Project Operations lapā **Projekti** noklikšķiniet uz cilnes **Grupa**, lai skatītu rezervējamo resursu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="90aa4-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="90aa4-109">Atlasiet vispārējo resursu, kam sarakstā ir resursa prasība, un pēc tam noklikšķiniet uz **Iesniegt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="90aa4-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="90aa4-110">Vispārēja grupas dalībnieka pieprasījuma statuss mainīsies uz **Iesniegts**.</span><span class="sxs-lookup"><span data-stu-id="90aa4-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="90aa4-111">Pēc tam, kad pieprasījums ir izpildīts, vispārējais resurss tiek aizstāts ar nosauktu resursu, ja resursu pārvaldnieks izpilda pieprasījumu, rezervējot nosauktu resursu.</span><span class="sxs-lookup"><span data-stu-id="90aa4-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="90aa4-112">Pretējā gadījumā, ja resursu pārvaldnieks piedāvā kādu nosauktu resursu, vispārējais resurss paliek darba grupā un pieprasījuma statuss mainās uz **Jāpārskata**.</span><span class="sxs-lookup"><span data-stu-id="90aa4-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]