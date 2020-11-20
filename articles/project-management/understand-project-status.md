---
title: Projekta statusa izprašana
description: Šajā tēmā ir sniegta informācija par satusu, kas tiek piešķirts projektiem programmā Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127302"
---
# <a name="understand-project-status"></a><span data-ttu-id="d6092-103">Projekta statusa izprašana</span><span class="sxs-lookup"><span data-stu-id="d6092-103">Understand project status</span></span>

<span data-ttu-id="d6092-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="d6092-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d6092-105">Lapas **Projekta entītija** sadaļā **Statuss** ir sniegts kopsavilkums par projekta veselību, pamatojoties uz izmaksām un ieguldījumu.</span><span class="sxs-lookup"><span data-stu-id="d6092-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="d6092-106">Statusa kopsavilkuma lauki</span><span class="sxs-lookup"><span data-stu-id="d6092-106">Status summary fields</span></span>

- <span data-ttu-id="d6092-107">Lauks **Vispārējs projekta statuss** ir rediģējams lauks, kur tiek rādīts projekta vispārējais statuss.</span><span class="sxs-lookup"><span data-stu-id="d6092-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="d6092-108">Šajā laukā tiek izmantots krāsu kodējums, piemēram, zaļa, dzeltena un sarkana krāsa, lai norādītu uz pieaugošu risku.</span><span class="sxs-lookup"><span data-stu-id="d6092-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="d6092-109">Laukā **Komentāri** projektu vadītājs var ievadīt konkrētus komentārus par statusu.</span><span class="sxs-lookup"><span data-stu-id="d6092-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="d6092-110">Lauks **Statusa atjaunināšanas laiks** nav rediģējams.</span><span class="sxs-lookup"><span data-stu-id="d6092-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="d6092-111">Šī lauka vērtība ir laikspiedols, kas norāda, kad pēdējoreiz tika atjaunināts statuss.</span><span class="sxs-lookup"><span data-stu-id="d6092-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="d6092-112">Lauki **Grafika veiktspēja** un **Izmaksu veiktspēja** tiek iestatīti no izsekošanas režģa.</span><span class="sxs-lookup"><span data-stu-id="d6092-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="d6092-113">Ja grafika un izmaksu novirze saknes mezglam skatā **Piepūles izsekošana** ir pozitīva, šie lauki tiek atjaunināti uz **Apsteidz**.</span><span class="sxs-lookup"><span data-stu-id="d6092-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="d6092-114">Ja grafika un izmaksu novirze saknes mezglam ir negatīva, šie lauki tiek iestatīti uz **Atpaliek**.</span><span class="sxs-lookup"><span data-stu-id="d6092-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
