---
title: Fiksētas cenas ieņēmumu novērtējumu projekti
description: Šajā tēmā ir sniegta informācija par fiksētas cenas ieņēmumiem projektos.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531492"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="fb50e-103">Fiksētas cenas ieņēmumu novērtējumu projekti</span><span class="sxs-lookup"><span data-stu-id="fb50e-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="fb50e-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="fb50e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fb50e-105">Izveidojot projekta līguma rindu ar tālāk norādītajiem atribūtiem Dynamics 365 Project Operations risinājumā Microsoft Dataverse, sistēma automātiski izveido fiksētas cenas ieņēmumu novērtējuma projektu.</span><span class="sxs-lookup"><span data-stu-id="fb50e-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="fb50e-106">Informācija šajā projektā ir balstīta uz tālāk uzskaitītajām opcijām.</span><span class="sxs-lookup"><span data-stu-id="fb50e-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="fb50e-107">Fiksētas cenas norēķinu metode.</span><span class="sxs-lookup"><span data-stu-id="fb50e-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="fb50e-108">Saistīts projekts.</span><span class="sxs-lookup"><span data-stu-id="fb50e-108">An associated project.</span></span>
  - <span data-ttu-id="fb50e-109">Vismaz viens atskaites punkts, kas definēts cilnē **Rēķina izrakstīšanas grafiks** lapā **Projekta līguma rinda**.</span><span class="sxs-lookup"><span data-stu-id="fb50e-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="fb50e-110">Fiksētas cenas ieņēmumu novērtējumu projektu pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="fb50e-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="fb50e-111">Lai pārskatītu fiksētas cenas ieņēmumu novērtējumu projektus, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="fb50e-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="fb50e-112">Dynamics 365 Finance vidē pārejiet uz **Projektu pārvaldība un uzskaite** > **Projekti** > **Fiksētas cenas ieņēmumu novērtējumu projekti**.</span><span class="sxs-lookup"><span data-stu-id="fb50e-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="fb50e-113">Atlasiet projektu, kuru vēlaties skatīt, un veiciet dubultklikšķi uz **Novērtējuma projekta ID**, lai atvērtu ierakstu un pārskatītu detalizētu informāciju par projektu.</span><span class="sxs-lookup"><span data-stu-id="fb50e-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="fb50e-114">Izvērsiet cilni **Projekts**. Režģī **Atlasītie projekti** ir redzams viens projekts.</span><span class="sxs-lookup"><span data-stu-id="fb50e-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="fb50e-115">Sistēma to izmanto kā noklusējuma projektu, jo šis projekts, ir saistīts ar projekta līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="fb50e-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="fb50e-116">Lai mainītu šo piesaisti, atlasiet papildu projektus un pievienojiet tos režģī **Atlasītie projekti**.</span><span class="sxs-lookup"><span data-stu-id="fb50e-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="fb50e-117">Ja šajā režģī ir atlasīti vairāki projekti, projekta pabeigšana procentos un ieņēmumu novērtējumi tiek aprēķināti kopā visiem atlasītajiem projektiem.</span><span class="sxs-lookup"><span data-stu-id="fb50e-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="fb50e-118">Projekta izmaksas, ieņēmumu profils, izmaksu veidne un perioda kods var tikt iestatīts manuāli.</span><span class="sxs-lookup"><span data-stu-id="fb50e-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="fb50e-119">Ja šie parametri netiek iestatīti manuāli, pirmā projekta novērtējuma aprēķināšanas laikā tiek iestatītas noklusējuma vērtības, izmantojot projekta izmaksu un ieņēmumu profiliem konfigurētās kārtulas.</span><span class="sxs-lookup"><span data-stu-id="fb50e-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>
