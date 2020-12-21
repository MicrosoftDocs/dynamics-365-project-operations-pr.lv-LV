---
title: Vajadzību viegla rezervēšana
description: Šajā tēmā ir sniegta informācija par to, kā viegli rezervēt vajadzības.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124107"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="f842f-103">Vajadzību viegla rezervēšana</span><span class="sxs-lookup"><span data-stu-id="f842f-103">Soft-book requirements</span></span>

<span data-ttu-id="f842f-104">Resursu vajadzību var viegli rezervēt.</span><span class="sxs-lookup"><span data-stu-id="f842f-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="f842f-105">Stingrā rezervēšana izveido piedāvājumu, kas patērē resursa noslodzi.</span><span class="sxs-lookup"><span data-stu-id="f842f-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="f842f-106">Pēc tam šis piedāvājums tiek nosūtīts atpakaļ prasītājam apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="f842f-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="f842f-107">Vieglā rezervācija veic resursa pagaidu pievienošanu projekta darba grupai, un tai ir cits statuss plānošanas panelī, taču tā nepatērē resursa noslodzi.</span><span class="sxs-lookup"><span data-stu-id="f842f-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="f842f-108">Lai veiktu vieglu resursa rezervēšanu, izmantojot plānošanas paneli, iestatiet laukam **Rezervācijas statuss** vienumu **Viegla**.</span><span class="sxs-lookup"><span data-stu-id="f842f-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Rezervācijas statusam iestatīta opcija Viegla](media/Resource-Management-image77.png)

<span data-ttu-id="f842f-110">Kad cilnē **Darba grupa** ir atvērts skats **Nosaukti darba grupas dalībnieki**, šis resurss tiek parādīts tur.</span><span class="sxs-lookup"><span data-stu-id="f842f-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="f842f-111">Viegli rezervētās stundas ir norādītas kolonnā **Viegli rezervētās stundas**.</span><span class="sxs-lookup"><span data-stu-id="f842f-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Viegli rezervētās stundas skatā Nosaukti darba grupas dalībnieki](media/Resource-Management-image78.png)

<span data-ttu-id="f842f-113">Viegli rezervētos darba grupas dalībniekus var nozīmēt uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="f842f-113">Soft-booked team members can be assigned to tasks.</span></span>

![Viegli rezervētie darba grupas dalībnieki nozīmēti uzdevumam](media/Resource-Management-image79.png)

<span data-ttu-id="f842f-115">Cilnē **Saskaņošana** netiek rādītas viegli rezervēto resursu rezervācijas, jo cilnē **Saskaņošana** tiek ņemtas vērā tikai stingrās rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="f842f-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Viegli rezervēts resurss bez rezervācijām cilnē Saskaņošana](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="f842f-117">Nevar veikt vieglu resursa rezervēšanu no vajadzības, kas ģenerēta no vispārēja darba grupas dalībnieka.</span><span class="sxs-lookup"><span data-stu-id="f842f-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="f842f-118">Plānošanas panelī resursa vieglai rezervācijai tiek izmantotas citas krāsas.</span><span class="sxs-lookup"><span data-stu-id="f842f-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Vieglā rezervēšana plānošanas panelī](media/Resource-Management-image81.png)

<span data-ttu-id="f842f-120">Lai vieglo rezervāciju pārveidotu par stingro rezervāciju, plānošanas panelī ar peles labo pogu noklikšķiniet uz vieglās rezervācijas un pēc tam atlasiet vienumu **Mainīt statusu** \> **Stingrā rezervācija** \> **Stingrā**.</span><span class="sxs-lookup"><span data-stu-id="f842f-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Rezervācijas statusa mainīšana uz iestatījumu Stingrā](media/Resource-Management-image82.png)

<span data-ttu-id="f842f-122">Rezervācija ir mainīta, un tās statuss ir mainīts plānošanas panelī.</span><span class="sxs-lookup"><span data-stu-id="f842f-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="f842f-123">Tā kā rezervācijas statuss tagad ir **Stingrā**, resurss tiek parādīts kā rezervēts un tā noslodze un pieejamība tiek pielāgota.</span><span class="sxs-lookup"><span data-stu-id="f842f-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="f842f-124">Varat izmantot to pašu metodi, lai atceltu stingro rezervāciju vai vieglo rezervāciju, izmantojot plānošanas paneli.</span><span class="sxs-lookup"><span data-stu-id="f842f-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="f842f-125">Lai pārveidotu resursu, kam veikta viegla rezervācija, uz stingro rezervāciju projekta cilnē **Darba grupa**, atlasiet resursu un pēc tam atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="f842f-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Komanda Apstiprināt](media/Resource-Management-image83.png)