---
title: Izstrādātāja piezīmes par apstiprinājumiem
description: Šajā tēmā ir sniegta papildu izstrādātāja informācija par darbu ar apstiprinājumiem.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996800"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="8fac9-103">Izstrādātāja piezīmes par apstiprinājumiem</span><span class="sxs-lookup"><span data-stu-id="8fac9-103">Developer notes for Approvals</span></span>

<span data-ttu-id="8fac9-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="8fac9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8fac9-105">Programmā Dynamics 365 Project Operations ir iekļauta validācijas loģika, kas nodrošina pareizu ieraksta pāreju, lietojot apstiprinājuma posmus.</span><span class="sxs-lookup"><span data-stu-id="8fac9-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="8fac9-106">Pareizas ieraksta pārejas nodrošina:</span><span class="sxs-lookup"><span data-stu-id="8fac9-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="8fac9-107">Visas atbalsta rindas tiek izveidotas saistītajās tabulās, piemēram, žurnālos un faktiskajos datos.</span><span class="sxs-lookup"><span data-stu-id="8fac9-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="8fac9-108">Apstiprinātājs projektā tiek atzīmēts kā **Projekta apstiprinātājs** pirms turpināšanas.</span><span class="sxs-lookup"><span data-stu-id="8fac9-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]