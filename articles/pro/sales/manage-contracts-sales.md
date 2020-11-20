---
title: Projekta līgumu pārvaldīšana
description: Šajā tēmā ir sniegta informācija par projekta līgumu skatīšanu.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177340"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="dea45-103">Projekta līgumu pārvaldīšana</span><span class="sxs-lookup"><span data-stu-id="dea45-103">Manage project contracts</span></span>

<span data-ttu-id="dea45-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="dea45-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dea45-105">Projekta līgumi risinājumā Dynamics 365 Project Operations ietver un pārvalda līgumā atrunātās projekta saistības un norēķinu detaļas.</span><span class="sxs-lookup"><span data-stu-id="dea45-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="dea45-106">Risinājumā Project Operations ietvertā projekta līguma struktūra ir pielāgota projekta darbam, izmantojot tālāk norādītos komponentus.</span><span class="sxs-lookup"><span data-stu-id="dea45-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="dea45-107">Līguma rindas, kas identificē diskrētos darba komponentus, kas projekta rēķinā tiks parādīti kā augsta līmeņa komponenti.</span><span class="sxs-lookup"><span data-stu-id="dea45-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="dea45-108">Līgumu rindu informācija, kas identificē un novērtē darbu katram augsta līmeņa komponentam vai līguma rindai.</span><span class="sxs-lookup"><span data-stu-id="dea45-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="dea45-109">Prognozētajās izmaksās ir iekļauts ar līguma rindu saistītā darba grafiks un finanšu aspekti.</span><span class="sxs-lookup"><span data-stu-id="dea45-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="dea45-110">Līgumu slēgšanas modeļi un maksas komponenti ir iestatīti katrai līguma rindai, kas ietver rēķinu izrakstīšanas izkārtojumu katrai līguma rindai un vispārējam līgumam.</span><span class="sxs-lookup"><span data-stu-id="dea45-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="dea45-111">Visu projekta līgumu skatīšana</span><span class="sxs-lookup"><span data-stu-id="dea45-111">View all project-based contracts</span></span>

<span data-ttu-id="dea45-112">Visu projekta līgumu sarakstu var skatīt lapā **Līgumi**.</span><span class="sxs-lookup"><span data-stu-id="dea45-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="dea45-113">Dodieties uz **Pārdošana** > **Kontaktpersonas**.</span><span class="sxs-lookup"><span data-stu-id="dea45-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="dea45-114">Tiek parādīts visu sistēmā esošo projekta līgumu saraksts.</span><span class="sxs-lookup"><span data-stu-id="dea45-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="dea45-115">Atlasiet **Skatu pārslēdzēju** (nolaižamā bultiņa blakus skata nosaukumam), lai atlasītu citus filtrētos skatus.</span><span class="sxs-lookup"><span data-stu-id="dea45-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="dea45-116">Varat izveidot savus skatus, kuros ir pielāgoti filtrēšanas kritēriji.</span><span class="sxs-lookup"><span data-stu-id="dea45-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="dea45-117">Līgumus var izveidot vai izdzēst no šīs saraksta lapas vai detalizētās lapas.</span><span class="sxs-lookup"><span data-stu-id="dea45-117">Contracts can be created or deleted from this list page or detail pages.</span></span>
