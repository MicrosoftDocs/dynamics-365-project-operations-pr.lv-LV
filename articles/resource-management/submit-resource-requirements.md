---
title: Submit a resource request
description: Ģenerētu resursa prasību varat iesniegt kā resursa pieprasījumu. Pēc tam šis pieprasījums tiek nosūtīts izpildei resursu pārvaldniekam.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279147"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="a3a4c-104">Submit a resource request</span><span class="sxs-lookup"><span data-stu-id="a3a4c-104">Submit a resource request</span></span>

<span data-ttu-id="a3a4c-105">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="a3a4c-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a3a4c-106">Ģenerētu resursa prasību varat iesniegt kā resursa pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="a3a4c-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="a3a4c-107">Pēc tam šis pieprasījums tiek nosūtīts izpildei resursu pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="a3a4c-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="a3a4c-108">Programmas Dynamics 365 Project Operations lapā **Projekti** noklikšķiniet uz cilnes **Grupa**, lai skatītu rezervējamo resursu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a3a4c-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="a3a4c-109">Atlasiet vispārējo resursu, kam sarakstā ir resursa prasība, un pēc tam noklikšķiniet uz **Iesniegt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="a3a4c-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="a3a4c-110">Vispārēja grupas dalībnieka pieprasījuma statuss mainīsies uz **Iesniegts**.</span><span class="sxs-lookup"><span data-stu-id="a3a4c-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="a3a4c-111">Pēc tam, kad pieprasījums ir izpildīts, vispārējais resurss tiek aizstāts ar nosauktu resursu, ja resursu pārvaldnieks izpilda pieprasījumu, rezervējot nosauktu resursu.</span><span class="sxs-lookup"><span data-stu-id="a3a4c-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="a3a4c-112">Pretējā gadījumā, ja resursu pārvaldnieks piedāvā kādu nosauktu resursu, vispārējais resurss paliek darba grupā un pieprasījuma statuss mainās uz **Jāpārskata**.</span><span class="sxs-lookup"><span data-stu-id="a3a4c-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]