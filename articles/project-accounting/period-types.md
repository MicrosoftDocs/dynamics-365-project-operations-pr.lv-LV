---
title: Periodu tipi
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt periodu tipus ieņēmumu novērtējumiem.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531491"
---
# <a name="period-types"></a><span data-ttu-id="cc471-103">Periodu tipi</span><span class="sxs-lookup"><span data-stu-id="cc471-103">Period types</span></span>

<span data-ttu-id="cc471-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="cc471-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cc471-105">Perioda tips nosaka, cik bieži projekta ieņēmumi tiek novērtēti.</span><span class="sxs-lookup"><span data-stu-id="cc471-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="cc471-106">Šajā tēmā ir sniegta informācija par to, kā iestatīt periodu tipus ieņēmumu novērtējumiem.</span><span class="sxs-lookup"><span data-stu-id="cc471-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="cc471-107">Periodu tipu izveide un darbs ar tiem</span><span class="sxs-lookup"><span data-stu-id="cc471-107">Create and work with period types</span></span>
<span data-ttu-id="cc471-108">Lai izveidotu periodu tipus un strādātu ar tiem, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="cc471-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="cc471-109">Dynamics 365 Finance vidē pārejiet uz **Projektu pārvaldība un uzskaite** > **Iestatīšana** > **Novērtējumi** > **Periodu tipi**.</span><span class="sxs-lookup"><span data-stu-id="cc471-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="cc471-110">Lai izveidotu jaunu perioda tipu, atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="cc471-110">Select **New** to create new period type.</span></span> <span data-ttu-id="cc471-111">Ievadiet nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="cc471-111">Enter a name and description.</span></span>
3. <span data-ttu-id="cc471-112">Laukā **Biežums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cc471-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="cc471-113">Atlasot **Nedēļa**, **Divas nedēļas**, **Divreiz mēnesī**, **Mēnesis**, **Diena**, **Ceturksnis** vai **Gads**, periodu ģenerēšanai tiks izmantots kalendārs.</span><span class="sxs-lookup"><span data-stu-id="cc471-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="cc471-114">Atlasot **Virsgrāmatas periods**, periodu ģenerēšanai tiks izmantoti virsgrāmatā konfigurētie periodi.</span><span class="sxs-lookup"><span data-stu-id="cc471-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="cc471-115">Atlasot **Neierobežots**, varat norādīt pielāgotus periodus.</span><span class="sxs-lookup"><span data-stu-id="cc471-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="cc471-116">Atlasiet perioda tipa ierakstu un pēc tam atlasiet **Ģenerēt periodus**, lai izveidotu periodus, izmantojot šo perioda tipu.</span><span class="sxs-lookup"><span data-stu-id="cc471-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="cc471-117">Pamatojoties uz atlasīto perioda biežumu, var būt pieejama iespēja norādīt sākuma datumu vai ģenerējamo periodu skaitu.</span><span class="sxs-lookup"><span data-stu-id="cc471-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="cc471-118">Atlasiet **Periodi**, lai pārskatītu ģenerētos periodus.</span><span class="sxs-lookup"><span data-stu-id="cc471-118">Select **Periods** to review generated periods.</span></span>

