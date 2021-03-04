---
title: Kas jauns vai mainīts Project Service Automation 3.x wave 1 2020 versijā
description: Šajā tēmā ir sniegta informācija par to, kas jauns un mainīts Project Service Automation 3. versijā, wave 1 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5110679038ae7ed1e21a3e7dc80a4657e0752b49
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150947"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="2459d-103">Kas jauns vai mainīts Project Service Automation 3 wave 1 2020 versijā</span><span class="sxs-lookup"><span data-stu-id="2459d-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2459d-104">Šajā tēmā ir uzsvērti galvenie jaunināšanas apsvērumi, pārejot uz jaunāko versiju Project Service Automation (PSA), versija 3. x wave 1 2020.</span><span class="sxs-lookup"><span data-stu-id="2459d-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="2459d-105">Laika ieraksts</span><span class="sxs-lookup"><span data-stu-id="2459d-105">Time entry</span></span>
<span data-ttu-id="2459d-106">Laika ievades pieredze ir paplašināta, lai nodrošinātu iespējas paplašināt laiku, ievadot vairāk klientu scenāriju.</span><span class="sxs-lookup"><span data-stu-id="2459d-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="2459d-107">Tas ietver iespēju pievienot ierakstu tipus, kas tagad virza noteiktu uzvedību, pamatojoties uz lauku shēmas **Laika ieraksta iestatījumi** nosaukumu, kas tiek parādīti kā **Laika avots**.</span><span class="sxs-lookup"><span data-stu-id="2459d-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="2459d-108">Šīs funkcionalitātes atbalstam ir pievienots jauns risinājums, ko sauc par laiku, izdevumiem, statusu un apstiprinājumiem (Time, Expense, Statusing, and Approvals — TESA).</span><span class="sxs-lookup"><span data-stu-id="2459d-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="2459d-109">Apsvērumi atjaunināšanai</span><span class="sxs-lookup"><span data-stu-id="2459d-109">Upgrade consideration</span></span>
<span data-ttu-id="2459d-110">Lai atbalstītu šo funkcionalitāti, funkcijas, kas ietilpst PSA, ir atjauninātas, lai iekļautu jaunas atļaujas.</span><span class="sxs-lookup"><span data-stu-id="2459d-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="2459d-111">Šīs atļaujas piešķir lasīšanas piekļuvi jaunajai entītijai **Laika ieraksta iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="2459d-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="2459d-112">Lietotājiem, kuriem nepieciešama iespēja reģistrēt laiku, jāpiešķir lietotāja lomas **Laika ieraksta lietotājs** papildus esošajām lomām.</span><span class="sxs-lookup"><span data-stu-id="2459d-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="2459d-113">Šajā lomā iekļauta jaunā funkcionalitāte, un programma nodrošina, ka laika ieraksts turpina darboties.</span><span class="sxs-lookup"><span data-stu-id="2459d-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="2459d-114">Turklāt, ja jums ir pielāgoti programmu moduļi, kuros ietvertas visas laika ierakstu entītijas veidlapas, no moduļa būs jānoņem **TESA laika ieraksta ātrās izveides forma**.</span><span class="sxs-lookup"><span data-stu-id="2459d-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="2459d-115">Pašlaik paplašinātā laika ieraksta izmaiņas</span><span class="sxs-lookup"><span data-stu-id="2459d-115">Currently extended time entry changes</span></span>
<span data-ttu-id="2459d-116">Lai mazinātu ietekmi uz laika ievadīšanas pašreizējiem lietotājiem, šī lomu maiņa ir vienīgā būtiskā prasība, kas nepieciešama, lai turpinātu izmantot laika ievadni.</span><span class="sxs-lookup"><span data-stu-id="2459d-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="2459d-117">Ja esat izveidojis pielāgotus skatus vai atdalītas laika ievadīšanas iespējas, lauki **Laika ievadnes iestatījums** ir jāiestata uz pareizo PSA vērtību.</span><span class="sxs-lookup"><span data-stu-id="2459d-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
