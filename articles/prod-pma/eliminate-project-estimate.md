---
title: Projekta tāmes likvidēšana
description: Šajā tēmā ir sniegta informācija par projekta tāmes likvidēšanu pēc tā pabeigšanas.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080497"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="d3a4d-103">Projekta tāmes likvidēšana</span><span class="sxs-lookup"><span data-stu-id="d3a4d-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3a4d-104">Projekta tāmes sniedz finansiālu ieskatu par darbu, kāds ir prognozēts un plānots projektam.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="d3a4d-105">Lai strādātu ar projekta tāmi, šis projekts ir jāpievieno novērtējuma projektam.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="d3a4d-106">Novērtējuma projekts vienmēr tiek balstīts uz esošu projektu, tomēr vairāki projekti var attiekties uz vienu novērtējuma projektu.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="d3a4d-107">Tikai fiksētas cenas un investīciju projektus var pievienot novērtējuma projektiem, un šiem projektiem ir jāpieder tai pašai projektu grupai, kurai pieder novērtējuma projekts.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="d3a4d-108">Lai likvidētu novērtējuma projektu, tam ir jābūt pabeigtam.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="d3a4d-109">Tālāk aprakstītajās darbībās ir paskaidrots, kā likvidēt tāmi.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="d3a4d-110">Dodieties uz **Projektu pārvaldība un grāmatvedība** > **Visi projekti** un atveriet projektu.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="d3a4d-111">Cilnē **Pārvaldīt** atlasiet **Novērtējums** un lapā **Novērtējums** atlasiet **Likvidēt**.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="d3a4d-112">Cilnes **Vispārīgi** lapā **Likvidēt tāmi** iestatiet tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="d3a4d-113">**Perioda kods** : atlasiet perioda kodu, lai izvēlētos atbilstošus projektu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="d3a4d-114">**Aprēķina datums** : atlasiet likvidēšanai atbilstošo aprēķina datumu.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="d3a4d-115">**Likvidēt ar NP brīdinājumiem** : iespējojiet šo opciju, lai sniegtu paziņojumu, ja ar nepabeigtu darbu (NP) saistītais aprēķins tiks likvidēts.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="d3a4d-116">Ja šī opcija nav iespējota, likvidēšanu nevar turpināt, ja pastāv tāmē neiekļauti darījumi.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="d3a4d-117">Šī opcija ir pieejama tikai tad, ja novērtējuma projektā liek veikta likvidēšana.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="d3a4d-118">Tas nav pieejams, ja izmantojat periodiskus grāmatojumus.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="d3a4d-119">Šis iestatījums darbojas ar iestatījumiem, kas atrodas cilnes **Novērtējums** lapā **Projekta parametri** esošajā lauku grupā **Atļaut likvidēšanu, ja pastāv darījumi, kas nav iekļauti tāmē**.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="d3a4d-120">**Iestatiet statusu uz Pabeigts** : iespējojiet šo opciju, lai pēc likvidēšanas izpildes iestatītu novērtējuma projekta statusu uz **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="d3a4d-121">**Drukāt novērtējumu sarakstu** : atlasiet informāciju, kas jāiekļauj, izdrukājot novērtējumu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="d3a4d-122">**Parādīt informācijas žurnālu** : iespējojiet šo opciju, lai rādītu informācijas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="d3a4d-123">**Grāmatošanas datums** : izvēlieties novērtējuma grāmatošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="d3a4d-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-124">Select **OK**.</span></span>
5. <span data-ttu-id="d3a4d-125">Pēc tam, kad likvidēšanas process ir pabeigts, likvidētais novērtējuma projekts tiek parādīts ar negatīvu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="d3a4d-126">Ja nevēlējāties likvidēt novērtējumu, varat atlasīt atcelto likvidēto novērtējumu un atlasīt **Atsaukt likvidēšanu**.</span><span class="sxs-lookup"><span data-stu-id="d3a4d-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
