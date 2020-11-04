---
title: Resursu noslodzes sinhronizēšana
description: Šajā tēmā ir sniegta informācija par to, kā sinhronizēt resursa noslodzi kalendāros un projektos.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080422"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="3b223-103">Resursu noslodzes sinhronizēšana</span><span class="sxs-lookup"><span data-stu-id="3b223-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b223-104">Resursa sinhronizēšanas procesi palīdz nodrošināt, ka kalendāra un bāzes kalendāra informācija nonāk projekta resursa plānošanā.</span><span class="sxs-lookup"><span data-stu-id="3b223-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="3b223-105">Ja kalendārs ir mainīts, procesi veic nepieciešamos projekta resursu plānošanas atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="3b223-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="3b223-106">Šie procesi arī palīdz uzlabot veiktspēju, jo kalendāra resursa informācija tiek iepriekš sinhronizēta.</span><span class="sxs-lookup"><span data-stu-id="3b223-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="3b223-107">Tāpēc resursa plānošanas informācijas atjauninājumi tiek veikti ātrāk.</span><span class="sxs-lookup"><span data-stu-id="3b223-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="3b223-108">Mēs jums iesakām plānot procesus kā paketi, nevis pa vienam.</span><span class="sxs-lookup"><span data-stu-id="3b223-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="3b223-109">Pretējā gadījumā pastāv risks, ka kāds aizmirsīs iekļaujošos datumus, kuros informācija pēdējo reizi tika sinhronizēta.</span><span class="sxs-lookup"><span data-stu-id="3b223-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="3b223-110">Ja iekļaujošie datumi netiek lietoti, datumu sinhronizācijas laikā var rasties atstarpes.</span><span class="sxs-lookup"><span data-stu-id="3b223-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendāra sinhronizācija](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="3b223-112">Sinhronizējiet resursa noslodzes apkopojumus</span><span class="sxs-lookup"><span data-stu-id="3b223-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="3b223-113">Sinhronizācijas process ir paredzēts, lai sinhronizētu visu resursa kalendāra informāciju.</span><span class="sxs-lookup"><span data-stu-id="3b223-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="3b223-114">Šī informācija ietver bāzes kalendāra informāciju par jebkādām izmaiņām, kas veiktas projekta resursa kalendāra noslodzes tabulā.</span><span class="sxs-lookup"><span data-stu-id="3b223-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="3b223-115">Ja projektam tiek pievienoti jauni resursi, sinhronizācija palīdz nodrošināt, ka ir pieejama atjaunināta informācija par kalendāru.</span><span class="sxs-lookup"><span data-stu-id="3b223-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="3b223-116">Šo sinhronizāciju var veikt jebkurā laikā.</span><span class="sxs-lookup"><span data-stu-id="3b223-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="3b223-117">Mēs iesakām lietot paketi.</span><span class="sxs-lookup"><span data-stu-id="3b223-117">We recommend that you use a batch.</span></span> <span data-ttu-id="3b223-118">Opcijas ir pieejamas noslodzes rezervāciju sinhronizācijas laikā.</span><span class="sxs-lookup"><span data-stu-id="3b223-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="3b223-119">Atlasiet **Projekta pārvaldība un uzskaite** &gt; **Periodiski** &gt; **Noslodzes sinhronizācija** &gt; **Sinhronizēt resursu noslodzes apkopojumus**.</span><span class="sxs-lookup"><span data-stu-id="3b223-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="3b223-120">Iestatiet opcijas no šīs tabulas.</span><span class="sxs-lookup"><span data-stu-id="3b223-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="3b223-121">Opcija</span><span class="sxs-lookup"><span data-stu-id="3b223-121">Option</span></span>      | <span data-ttu-id="3b223-122">Apraksts</span><span class="sxs-lookup"><span data-stu-id="3b223-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="3b223-123">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="3b223-123">Period code</span></span> | <span data-ttu-id="3b223-124">Ja vēlaties, atlasiet virsgrāmatas datuma intervāla kodu, lai iestatītu sākuma un beigu datumus resursu noslodzes apkopojumu sinhronizācijas procesam.</span><span class="sxs-lookup"><span data-stu-id="3b223-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="3b223-125">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="3b223-125">Start date</span></span>  | <span data-ttu-id="3b223-126">Ievadiet resursa noslodzes apkopojuma sinhronizācijas procesa sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="3b223-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="3b223-127">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="3b223-127">End date</span></span>    | <span data-ttu-id="3b223-128">Ievadiet resursa noslodzes apkopojuma sinhronizācijas procesa beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="3b223-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="3b223-129">[![Sinhronizācijas process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="3b223-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
