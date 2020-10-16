---
title: Izdevumu tāmes
description: Šajā tēmā ir sniegta informācija par to, kā definēt vai aprēķināt projekta izdevumus.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908362"
---
# <a name="expense-estimates"></a><span data-ttu-id="24995-103">Izdevumu tāmes</span><span class="sxs-lookup"><span data-stu-id="24995-103">Expense estimates</span></span>
<span data-ttu-id="24995-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="24995-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="24995-105">Papildus resursu aprēķinu definēšanai risinājums Dynamics 365 Project Operations ļauj Projekta vadītājiem katram projektam definēt projekta izdevumus.</span><span class="sxs-lookup"><span data-stu-id="24995-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="24995-106">Katru izdevumu elementu var saistīt ar konkrētu projekta uzdevumu vai izdevumu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="24995-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="24995-107">Izdevumu kategorijas parasti tiek definētas organizācijas līmenī.</span><span class="sxs-lookup"><span data-stu-id="24995-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="24995-108">Katras izdevumu kategorijas cenu noteikšana parasti tiek definēta šādā hierarhijā:</span><span class="sxs-lookup"><span data-stu-id="24995-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="24995-109">Organizācija</span><span class="sxs-lookup"><span data-stu-id="24995-109">Organization</span></span>
- <span data-ttu-id="24995-110">Klients</span><span class="sxs-lookup"><span data-stu-id="24995-110">Customer</span></span>
- <span data-ttu-id="24995-111">Piedāvājums/līgums</span><span class="sxs-lookup"><span data-stu-id="24995-111">Quote/contract</span></span>

<span data-ttu-id="24995-112">Lai apskatītu, pievienotu vai dzēstu projekta izdevumus, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="24995-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="24995-113">Dodieties uz sadaļu **Projekti** un atlasiet projektu, ar kuru vēlaties strādāt.</span><span class="sxs-lookup"><span data-stu-id="24995-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="24995-114">Atlasiet cilni **Projekta aprēķini** un skatiet projekta izmaksu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="24995-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="24995-115">Atlasiet **Jauni izdevumi**, lai pievienotu izdevumus.</span><span class="sxs-lookup"><span data-stu-id="24995-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="24995-116">Varat arī atlasīt izmaksas, ko vēlaties dzēst, un pēc tam atlasīt vienumu **Dzēst izdevumus**.</span><span class="sxs-lookup"><span data-stu-id="24995-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="24995-117">Katram izdevumu rindas elementam tiek definēti šādi atribūti:</span><span class="sxs-lookup"><span data-stu-id="24995-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="24995-118">**Kategorija**: kopējas grupas, ko izmanto, lai aprakstītu visus projektā radušos izdevumus.</span><span class="sxs-lookup"><span data-stu-id="24995-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="24995-119">**Sākuma datums**: datums, kurā tiek prognozēta izdevumu rašanās.</span><span class="sxs-lookup"><span data-stu-id="24995-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="24995-120">**Daudzums**: prognozētais izdevumu elementu skaits noteiktā kategorijā.</span><span class="sxs-lookup"><span data-stu-id="24995-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="24995-121">**Vienības izmaksu cena**: vienības cena, ko izmanto izmaksu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="24995-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="24995-122">**Vienības pārdošanas cena**: vienības cena, ko izmanto izmaksu pārdošanas cenu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="24995-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

