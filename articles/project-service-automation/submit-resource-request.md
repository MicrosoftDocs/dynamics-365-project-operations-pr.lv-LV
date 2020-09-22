---
title: Resursa pieprasījuma iesniegšana
description: Šajā tēmā ir sniegta informācija par pieprasījuma iesniegšanu par projekta resursu.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753531"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="c46e1-103">Resursa pieprasījuma iesniegšana</span><span class="sxs-lookup"><span data-stu-id="c46e1-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c46e1-104">Ģenerētu resursa prasību varat iesniegt kā resursa pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="c46e1-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="c46e1-105">Pēc tam šis pieprasījums tiek nosūtīts izpildei resursu pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="c46e1-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="c46e1-106">Programmas Project Service Automation (PSA) lapā **Projekti** noklikšķiniet uz cilnes **Grupa**, lai skatītu rezervējamo resursu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="c46e1-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="c46e1-107">Atlasiet vispārējo resursu, kam sarakstā ir resursa prasība, un pēc tam noklikšķiniet uz **Iesniegt pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="c46e1-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Resursa pieprasījuma iesniegšana](media/RM-how-to-18.png)

<span data-ttu-id="c46e1-109">Vispārēja grupas dalībnieka pieprasījuma statuss mainīsies uz **Iesniegts**.</span><span class="sxs-lookup"><span data-stu-id="c46e1-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="c46e1-110">Pēc tam, kad resursu pārvaldnieks ir izpildījis pieprasījumu, vispārējs resurss tiek aizstāts ar nosauktu resursu, ja resursu pārvaldnieks izpilda pieprasījumu ar nosauktā resursa rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="c46e1-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="c46e1-111">Pretējā gadījumā vispārējs resurss paliks komandā, un pieprasījuma statuss mainīsies uz **Jāpārskata**, ja resursu pārvaldnieks ir piedāvājis nosauktu resursu.</span><span class="sxs-lookup"><span data-stu-id="c46e1-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
