---
title: Projekta budžetu prognožu modeļu izveide
description: Šajā tēmā aprakstīts, kā izveidot prognožu modeli atlikušajiem budžetiem.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271047"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="00fee-103">Projekta budžetu prognožu modeļu izveide</span><span class="sxs-lookup"><span data-stu-id="00fee-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00fee-104">Šajā tēmā aprakstīts, kā izveidot prognožu modeli atlikušajiem budžetiem.</span><span class="sxs-lookup"><span data-stu-id="00fee-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="00fee-105">Projekts, kam tiek kontrolēts budžets, izmanto divu veidu budžetus: sākotnējo un atlikušo.</span><span class="sxs-lookup"><span data-stu-id="00fee-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="00fee-106">Kad izveidojat projekta budžetu, ir jānorāda sākotnējā un atlikušā budžeta prognožu modeļi, kas izveidoti lapā **Prognožu modeļi**.</span><span class="sxs-lookup"><span data-stu-id="00fee-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="00fee-107">Projekta budžeti, kuru pamatā ir noteikti modeļi, tiek izveidoti, kad izpildāt projekta budžetu.</span><span class="sxs-lookup"><span data-stu-id="00fee-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="00fee-108">Prognožu modelim, kas tiek izmantots budžeta kontrolei, nevar būt apakšmodelis, vai tas nevar tikt izmantots kā apakšmodelis.</span><span class="sxs-lookup"><span data-stu-id="00fee-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="00fee-109">Atlasiet **Projektu vadība un grāmatvedība** > **Iestatījumi** > **Prognozes**  > **Prognožu modeļi**.</span><span class="sxs-lookup"><span data-stu-id="00fee-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="00fee-110">Atlasiet **Jauns**, lai izveidotu jaunu prognožu modeli, un pēc tam ievadiet modeļa ID numuru un jaunā modeļa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="00fee-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="00fee-111">Opciju **Apturēts** iestatiet uz **Jā**, lai neļautu veikt izmaiņas prognožu modeļa prognožu rindās.</span><span class="sxs-lookup"><span data-stu-id="00fee-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="00fee-112">Ja prognožu rindām, ar kurām ir saistīts modelis, ir jāģenerē naudas plūsmas prognozes virsgrāmatā, vienumu **Iekļaut naudas plūsmas prognozēs** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="00fee-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="00fee-113">Lai projekta datumu izmantotu kā rēķina datumu, vienumu **Prognozēt rēķina datumu** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="00fee-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="00fee-114">Laukā **Budžeta tips** atlasiet vienu no šiem modeļu tipiem.</span><span class="sxs-lookup"><span data-stu-id="00fee-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="00fee-115">**Sākotnējais budžets**: izmantojiet sākotnējās budžeta summas, kas ir iestatītas, izveidojot un aprēķinot sākotnējo budžetu.</span><span class="sxs-lookup"><span data-stu-id="00fee-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="00fee-116">**Atlikušais budžets**: atlikušās budžeta summas izmantojiet projekta dzīves laikā.</span><span class="sxs-lookup"><span data-stu-id="00fee-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="00fee-117">Bilances šajā prognožu modelī samazina faktiskie darījumi un palielina vai samazina budžeta pārskatījumi.</span><span class="sxs-lookup"><span data-stu-id="00fee-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="00fee-118">**Pārnesumi** : izmantojiet pārnesumu budžeta summas projektam.</span><span class="sxs-lookup"><span data-stu-id="00fee-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="00fee-119">Pārnešana ir neobligāts process, ko var palaist, lai pārnestu neizmantotās budžeta summas no viena finanšu gada uz citu.</span><span class="sxs-lookup"><span data-stu-id="00fee-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="00fee-120">Pēc nepieciešamības iestatiet tālāk minētās opcijas.</span><span class="sxs-lookup"><span data-stu-id="00fee-120">Set the following options as required:</span></span>

   - <span data-ttu-id="00fee-121">Lai projekta datumu izmantotu kā rēķina datumu, iespējojiet vienumu **Prognozēt rēķina datumu**.</span><span class="sxs-lookup"><span data-stu-id="00fee-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="00fee-122">Iespējojiet **Prognozēt ar NP**, lai prognozētu, pamatojoties uz notiekošo darbu (NP), un pēc tam atlasiet NP tipu.</span><span class="sxs-lookup"><span data-stu-id="00fee-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="00fee-123">Noklusējuma **budžeta tipu** var atstāt kā **Nav** vai var ievadīt jaunu tipu.</span><span class="sxs-lookup"><span data-stu-id="00fee-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="00fee-124">Pēc ieraksta maiņas budžeta tipu nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="00fee-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="00fee-125">Ja mainīsit noklusējuma budžeta tipu, visas citas opcijas būs nepieejamas atjauninājumiem un šo budžeta modeli nevarēs atkārtoti izmantot.</span><span class="sxs-lookup"><span data-stu-id="00fee-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]