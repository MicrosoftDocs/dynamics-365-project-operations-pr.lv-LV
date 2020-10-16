---
title: Projekta statusa izprašana
description: Šajā tēmā ir sniegta informācija par satusu, kas tiek piešķirts projektiem programmā Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965685"
---
# <a name="understand-project-status"></a><span data-ttu-id="c6c32-103">Projekta statusa izprašana</span><span class="sxs-lookup"><span data-stu-id="c6c32-103">Understand project status</span></span>

<span data-ttu-id="c6c32-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="c6c32-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c6c32-105">Lapas **Projekta entītija** sadaļā **Statuss** ir sniegts kopsavilkums par projekta veselību, pamatojoties uz izmaksām un ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="c6c32-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="c6c32-106">Statusa kopsavilkuma lauki</span><span class="sxs-lookup"><span data-stu-id="c6c32-106">Status summary fields</span></span>

- <span data-ttu-id="c6c32-107">Lauks **Vispārējais projekta statuss** ir rediģējams lauks, kurā tiek rādīts projekta vispārējais statuss.</span><span class="sxs-lookup"><span data-stu-id="c6c32-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="c6c32-108">Šajā laukā tiek izmantots krāsu kodējums, piemēram, zaļa, dzeltena un sarkana krāsa, lai norādītu uz pieaugošu risku.</span><span class="sxs-lookup"><span data-stu-id="c6c32-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="c6c32-109">Laukā **Komentāri** projekta vadītājs var ievadīt konkrētus komentārus par statusu.</span><span class="sxs-lookup"><span data-stu-id="c6c32-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="c6c32-110">Lauks **Statusa atjaunināšanas laiks** nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="c6c32-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="c6c32-111">Šī lauka vērtība ir laikspiedols, kas norāda, kad pēdējoreiz tika atjaunināts statuss.</span><span class="sxs-lookup"><span data-stu-id="c6c32-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="c6c32-112">Lauki **Grafika veiktspēja** un **Izmaksu veiktspēja** tiek iestatīti no izsekošanas režģa.</span><span class="sxs-lookup"><span data-stu-id="c6c32-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="c6c32-113">Ja grafika un izmaksu novirze saknes mezglam skatā **Ieguldījuma izsekošana** ir pozitīva, šie lauki tiek atjaunināti uz **Apsteidz**.</span><span class="sxs-lookup"><span data-stu-id="c6c32-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="c6c32-114">Ja grafika un izmaksu novirze saknes mezglam ir negatīva, šie lauki tiek iestatīti uz **Atpaliek**.</span><span class="sxs-lookup"><span data-stu-id="c6c32-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
