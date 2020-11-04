---
title: Resursu kalendāru definēšana
description: Šajā tēmā ir sniegta informācija par to, kā definēt darba stundu kalendāru resursiem risinājumā Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080292"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="0d737-103">Resursu kalendāru definēšana</span><span class="sxs-lookup"><span data-stu-id="0d737-103">Define resource calendars</span></span>

<span data-ttu-id="0d737-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="0d737-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0d737-105">Katram rezervējamam resursam, kas strādā projektā, ir nepieciešams darba stundu kalendārs, kurā definēta tā pieejamība.</span><span class="sxs-lookup"><span data-stu-id="0d737-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="0d737-106">Resursa darba stundas var definēt divējādi.</span><span class="sxs-lookup"><span data-stu-id="0d737-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="0d737-107">Atsevišķu kalendāra kārtulu definēšana resursam</span><span class="sxs-lookup"><span data-stu-id="0d737-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="0d737-108">Esošas kalendāra veidnes lietošana resursam</span><span class="sxs-lookup"><span data-stu-id="0d737-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="0d737-109">Resursa darba stundu definēšana</span><span class="sxs-lookup"><span data-stu-id="0d737-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="0d737-110">Izvēlnē **Resursi** atlasiet vienumu **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="0d737-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="0d737-111">Režģa skatā atlasiet atbilstošo **Rezervējamo resursu**.</span><span class="sxs-lookup"><span data-stu-id="0d737-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="0d737-112">Lapā **Resursa informācija** atlasiet cilni **Darba stundas**. Pēc noklusējuma rezervējamo resursu kalendāra iestatījums ir darba stundu veidnē izmantotais noklusējuma darba stundu skaits, kas ir definēts organizācijai.</span><span class="sxs-lookup"><span data-stu-id="0d737-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="0d737-113">Lai atjauninātu darba stundu skaitu, ar peles labo pogu noklikšķiniet uz definējamās kalendāra kārtulas sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="0d737-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="0d737-114">Izmantojiet kalendāra kārtulas izvēlni, lai definētu kalendāra kārtulu konkrētai dienai, atlikušām dienām sērijā vai visam kalendāram.</span><span class="sxs-lookup"><span data-stu-id="0d737-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="0d737-115">Pēc tam, kad opcija ir atlasīta, varat definēt tālāk norādītos parametrus.</span><span class="sxs-lookup"><span data-stu-id="0d737-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="0d737-116">Nedēļas diena, kurā tiks piemērotas darba stundas.</span><span class="sxs-lookup"><span data-stu-id="0d737-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="0d737-117">Darba laiki katrā dienā.</span><span class="sxs-lookup"><span data-stu-id="0d737-117">The working times within each day.</span></span>
    - <span data-ttu-id="0d737-118">Kalendāra kārtulas laika josla.</span><span class="sxs-lookup"><span data-stu-id="0d737-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="0d737-119">Ja piemērojams, kārtulai var norādīt laiku, kas nav darba laiks.</span><span class="sxs-lookup"><span data-stu-id="0d737-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="0d737-120">Kalendāra veidnes piemērošana resursam</span><span class="sxs-lookup"><span data-stu-id="0d737-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="0d737-121">Izvēlnē **Resursi** atlasiet vienumu **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="0d737-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="0d737-122">Režģa skatā atlasiet līdz 25 **Rezervējamiem resursiem** , ko vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="0d737-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="0d737-123">Atlasiet vienumu **Iestatīt kalendāru** , un dialoglogā tiks parādīts pieejamo darba stundu veidņu saraksts.</span><span class="sxs-lookup"><span data-stu-id="0d737-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="0d737-124">Atlasiet veidni, ko vēlaties izmantot, un pēc tam atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="0d737-124">Select the template you want to use, and then select **Apply**.</span></span>
