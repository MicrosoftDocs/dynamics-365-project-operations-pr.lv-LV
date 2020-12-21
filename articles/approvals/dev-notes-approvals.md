---
title: Izstrādātāja piezīmes par apstiprinājumiem
description: Šajā tēmā ir sniegta papildu izstrādātāja informācija par darbu ar apstiprinājumiem.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483957"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="4eace-103">Izstrādātāja piezīmes par apstiprinājumiem</span><span class="sxs-lookup"><span data-stu-id="4eace-103">Developer notes for Approvals</span></span>

<span data-ttu-id="4eace-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="4eace-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4eace-105">Dynamics 365 Project Operations ir iekļauta validācijas loģika, kas nodrošina pareizu ieraksta pāreju, lietojot apstiprinājuma posmus.</span><span class="sxs-lookup"><span data-stu-id="4eace-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="4eace-106">Pareizas ieraksta pārejas nodrošina:</span><span class="sxs-lookup"><span data-stu-id="4eace-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="4eace-107">Visas atbalsta rindas tiek izveidotas saistītajās tabulās, piemēram, žurnālos un faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="4eace-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="4eace-108">Apstiprinātājs projektā tiek atzīmēts kā **Projekta apstiprinātājs** pirms turpināšanas.</span><span class="sxs-lookup"><span data-stu-id="4eace-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>