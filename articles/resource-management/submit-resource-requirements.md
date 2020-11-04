---
title: Submit a resource request
description: Ģenerētu resursa prasību varat iesniegt kā resursa pieprasījumu. Pēc tam šis pieprasījums tiek nosūtīts izpildei resursu pārvaldniekam.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080338"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="515b7-104">Submit a resource request</span><span class="sxs-lookup"><span data-stu-id="515b7-104">Submit a resource request</span></span>

<span data-ttu-id="515b7-105">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="515b7-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="515b7-106">Ģenerētu resursa prasību varat iesniegt kā resursa pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="515b7-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="515b7-107">Pēc tam šis pieprasījums tiek nosūtīts izpildei resursu pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="515b7-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="515b7-108">Dynamics 365 Project Operations lapā **Projekti** atlasiet cilni **Darba grupa** , lai skatītu rezervējamo resursu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="515b7-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="515b7-109">Atlasiet vispārējo resursu, kam sarakstā ir resursa prasība, un pēc tam noklikšķiniet uz **Iesniegt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="515b7-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="515b7-110">Vispārēja grupas dalībnieka pieprasījuma statuss mainīsies uz **Iesniegts**.</span><span class="sxs-lookup"><span data-stu-id="515b7-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="515b7-111">Pēc tam, kad pieprasījums ir izpildīts, vispārējais resurss tiek aizstāts ar nosauktu resursu, ja resursu pārvaldnieks izpilda pieprasījumu, rezervējot nosauktu resursu.</span><span class="sxs-lookup"><span data-stu-id="515b7-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="515b7-112">Pretējā gadījumā, ja resursu pārvaldnieks piedāvā kādu nosauktu resursu, vispārējais resurss paliek darba grupā un pieprasījuma statuss mainās uz **Jāpārskata**.</span><span class="sxs-lookup"><span data-stu-id="515b7-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
