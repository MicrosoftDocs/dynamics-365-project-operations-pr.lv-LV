---
title: Project Operations duālās rakstīšanas integrācija
description: Šajā tēmā ir sniegts pārskats par Project Operations duālās rakstīšanas integrāciju.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368440"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="3382f-103">Project Operations duālās rakstīšanas integrācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="3382f-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="3382f-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="3382f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3382f-105">Project Operations izmanto [duālās rakstīšanas iespējas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), lai sinhronizētu datus starp Microsoft Dataverse un Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="3382f-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="3382f-106">Tālāk redzamajā attēlā ir parādīts, kā dati tiek sinhronizēti kā daļa no šīs integrācijas starp Dataverse un Finance.</span><span class="sxs-lookup"><span data-stu-id="3382f-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Project Operations datu plūsmu pārskats](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="3382f-108">Project Operations risinājumā Dataverse nodrošina modernu lietotāja interfeisu (UI) un ērtu paplašināmību bez kodēšanas/ar minimālu kodēšanu, izmantojot Power Platform iespējas.</span><span class="sxs-lookup"><span data-stu-id="3382f-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="3382f-109">Projektu vadītāji, resursu vadītāji, projektu darba grupas dalībnieki un citi biroja darbinieki veic savas darbības Project Operations risinājumā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3382f-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="3382f-110">Project Operations risinājumā Finance nodrošina projektu grāmatvedību un ieņēmumu atpazīšanas atbalstu.</span><span class="sxs-lookup"><span data-stu-id="3382f-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="3382f-111">Project Operations pieslēdzas Finance finanšu struktūrai, lai aprēķinātu pārdošanas nodokļus, valūtas maiņas kursu, finanšu dimensiju atskaites un veiktu citas darbības.</span><span class="sxs-lookup"><span data-stu-id="3382f-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="3382f-112">Projekta grāmatvežu pieredzes lielākoties ir balstītas risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="3382f-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="3382f-113">Project Operations integrācija sastāv no šādu komponentu integrācijas:</span><span class="sxs-lookup"><span data-stu-id="3382f-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="3382f-114">Project Operations iestatīšanas un konfigurēšanas datu integrācija</span><span class="sxs-lookup"><span data-stu-id="3382f-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="3382f-115">Projekta aprēķini un faktiskie dati</span><span class="sxs-lookup"><span data-stu-id="3382f-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="3382f-116">Projekta rēķini</span><span class="sxs-lookup"><span data-stu-id="3382f-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="3382f-117">Izdevumu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="3382f-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="3382f-118">Piegādātāja rēķins</span><span class="sxs-lookup"><span data-stu-id="3382f-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
