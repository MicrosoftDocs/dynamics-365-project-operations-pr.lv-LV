---
title: Galīgo izmaksu novērtējuma atjaunināšana
description: Šajā tēmā ir sniegta informācija par projekta darba prognozes atjaunināšanu.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127212"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="6becd-103">Galīgo izmaksu novērtējuma atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="6becd-103">Update estimate at completion</span></span>

<span data-ttu-id="6becd-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="6becd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6becd-105">Projektu vadītāji bieži vien pārskata sākotnējās uzdevumu aplēses.</span><span class="sxs-lookup"><span data-stu-id="6becd-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="6becd-106">Projekta pārprojektēšana ir projektu vadītāja reaģēšana uz prognozēm, ņemot vērā projekta pašreizējo statusu.</span><span class="sxs-lookup"><span data-stu-id="6becd-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="6becd-107">Taču mēs neiesakām projektu vadītājiem mainīt bāzlīnijas skaitļus, jo projekta bāzlīnija pārstāv noteikto patiesās informācijas avotu projekta grafikam un izmaksu tāmei, un visas projektā ieinteresētās puses par to ir vienojušās.</span><span class="sxs-lookup"><span data-stu-id="6becd-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="6becd-108">Projektu vadītājs uzdevumiem var pārprojektēt piepūli divos tālāk norādītajos veidos:</span><span class="sxs-lookup"><span data-stu-id="6becd-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="6becd-109">Pārlabojiet noklusējuma novērtējumu līdz pabeigšanai (ETC) ar jaunu faktiskā uzdevumam atlikušā darba novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="6becd-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="6becd-110">Pārlabot noklusējuma progresa procentuālo daudzumu ar jaunu uzdevuma patiesā progresa novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="6becd-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="6becd-111">Katra no šīm metodēm izraisa uzdevuma ETC, EAC un progresa procentuālā daudzuma pārrēķināšanu, kā arī uzdevumam projektētās piepūles novirzes pārrēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="6becd-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="6becd-112">Tiek pārrēķināts EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un tiek izveidota jauna piepūles novirzes projektēšana.</span><span class="sxs-lookup"><span data-stu-id="6becd-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
