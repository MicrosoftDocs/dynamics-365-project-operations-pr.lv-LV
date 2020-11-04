---
title: Galīgo izmaksu novērtējuma atjaunināšana
description: Šajā tēmā ir sniegta informācija par projekta darba prognozes atjaunināšanu.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080627"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="2ca4f-103">Galīgo izmaksu novērtējuma atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="2ca4f-103">Update estimate at completion</span></span>

<span data-ttu-id="2ca4f-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="2ca4f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2ca4f-105">Projektu vadītāji bieži vien pārskata sākotnējās uzdevumu aplēses.</span><span class="sxs-lookup"><span data-stu-id="2ca4f-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="2ca4f-106">Projekta pārprojektēšana ir projektu vadītāja reaģēšana uz prognozēm, ņemot vērā projekta pašreizējo statusu.</span><span class="sxs-lookup"><span data-stu-id="2ca4f-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="2ca4f-107">Taču mēs neiesakām projektu vadītājiem mainīt bāzlīnijas skaitļus, jo projekta bāzlīnija pārstāv noteikto patiesās informācijas avotu projekta grafikam un izmaksu tāmei, un visas projektā ieinteresētās puses par to ir vienojušās.</span><span class="sxs-lookup"><span data-stu-id="2ca4f-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="2ca4f-108">Projektu vadītājs uzdevumiem var pārprojektēt piepūli divos tālāk norādītajos veidos:</span><span class="sxs-lookup"><span data-stu-id="2ca4f-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="2ca4f-109">Pārlabojiet noklusējuma novērtējumu līdz pabeigšanai (ETC) ar jaunu faktiskā uzdevumam atlikušā darba novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="2ca4f-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="2ca4f-110">Pārlabot noklusējuma progresa procentuālo daudzumu ar jaunu uzdevuma patiesā progresa novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="2ca4f-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="2ca4f-111">Katra no šīm metodēm izraisa uzdevuma ETC, EAC un progresa procentuālā daudzuma pārrēķināšanu, kā arī uzdevumam projektētās piepūles novirzes pārrēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="2ca4f-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="2ca4f-112">Tiek pārrēķināts EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un tiek izveidota jauna piepūles novirzes projektēšana.</span><span class="sxs-lookup"><span data-stu-id="2ca4f-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
