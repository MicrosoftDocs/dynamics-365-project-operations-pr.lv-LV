---
title: Projekta statusa izprašana
description: Šajā tēmā ir sniegta informācija par projektiem piešķirto statusu programmā Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ad8c012b93bc65595dca33df1770562916c557e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993425"
---
# <a name="understand-project-status"></a><span data-ttu-id="237a0-103">Projekta statusa izprašana</span><span class="sxs-lookup"><span data-stu-id="237a0-103">Understand project status</span></span>

<span data-ttu-id="237a0-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="237a0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="237a0-105">Lapas **Projekta entītija** sadaļā **Statuss** ir sniegts kopsavilkums par projekta veselību, pamatojoties uz izmaksām un ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="237a0-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="237a0-106">Statusa kopsavilkuma lauki</span><span class="sxs-lookup"><span data-stu-id="237a0-106">Status summary fields</span></span>

- <span data-ttu-id="237a0-107">Lauks **Vispārējs projekta statuss** ir rediģējams lauks, kur tiek rādīts projekta vispārējais statuss.</span><span class="sxs-lookup"><span data-stu-id="237a0-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="237a0-108">Šajā laukā tiek izmantots krāsu kodējums, piemēram, zaļa, dzeltena un sarkana krāsa, lai norādītu uz pieaugošu risku.</span><span class="sxs-lookup"><span data-stu-id="237a0-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="237a0-109">Laukā **Komentāri** projektu vadītājs var ievadīt konkrētus komentārus par statusu.</span><span class="sxs-lookup"><span data-stu-id="237a0-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="237a0-110">Lauks **Statusa atjaunināšanas laiks** nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="237a0-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="237a0-111">Šī lauka vērtība ir laikspiedols, kas norāda, kad pēdējoreiz tika atjaunināts statuss.</span><span class="sxs-lookup"><span data-stu-id="237a0-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="237a0-112">Lauki **Grafika veiktspēja** un **Izmaksu veiktspēja** tiek iestatīti no izsekošanas režģa.</span><span class="sxs-lookup"><span data-stu-id="237a0-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="237a0-113">Ja grafika un izmaksu novirze saknes mezglam skatā **Piepūles izsekošana** ir pozitīva, šie lauki tiek atjaunināti uz **Apsteidz**.</span><span class="sxs-lookup"><span data-stu-id="237a0-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="237a0-114">Ja grafika un izmaksu novirze saknes mezglam ir negatīva, šie lauki tiek iestatīti uz **Atpaliek**.</span><span class="sxs-lookup"><span data-stu-id="237a0-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]