---
title: Projekta cenrāžu sarakstu ignorēšana
description: Šajā tēmā ir sniegta informācija par pielāgotu pārdošanas cenrāžu izveidi.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672240"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="547d8-103">Projekta cenrāžu sarakstu ignorēšana</span><span class="sxs-lookup"><span data-stu-id="547d8-103">Override project sales price lists</span></span>

<span data-ttu-id="547d8-104">_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_</span><span class="sxs-lookup"><span data-stu-id="547d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="547d8-105">Klientam noteikts projekta cenrādis</span><span class="sxs-lookup"><span data-stu-id="547d8-105">Customer-specific project price lists</span></span>

<span data-ttu-id="547d8-106">Klientam noteiktas cenas var tikt iestatītas kā projekta cenrāži uzņēmuma ierakstā risinājumā Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="547d8-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="547d8-107">Lai iestatītu klientam noteiktu projekta cenrādi, zonā **Pārdošana** pārejiet uz uzņēmuma ierakstu.</span><span class="sxs-lookup"><span data-stu-id="547d8-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="547d8-108">Atveriet saraksta lapu **Konts**.</span><span class="sxs-lookup"><span data-stu-id="547d8-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="547d8-109">Atrodiet un veiciet dubultklikšķi uz klienta ieraksta, lai atvērtu informācijas lapu **Konts**.</span><span class="sxs-lookup"><span data-stu-id="547d8-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="547d8-110">Cilnē **Projekta cenrāži** atlasiet **+ Jauns projekta cenrādis**.</span><span class="sxs-lookup"><span data-stu-id="547d8-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="547d8-111">Lapas **Jauns projekta cenrādis** nolaižamajā sarakstā atlasiet cenrādi.</span><span class="sxs-lookup"><span data-stu-id="547d8-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="547d8-112">Ir iekļauti tikai tie cenrāži, kuru konteksts ir iestatīts kā **Pārdošana** un kuru valūta atbilst uzņēmuma valūtai.</span><span class="sxs-lookup"><span data-stu-id="547d8-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="547d8-113">Ierakstiet saistības nosaukumu un pēc tam atlasiet vienumu **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="547d8-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="547d8-114">Tiek izveidots klientam noteikts projekta cenrādis.</span><span class="sxs-lookup"><span data-stu-id="547d8-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="547d8-115">Šis cenrādis tiks izmantots, lai ievietotu noklusējuma projekta cenas projekta piedāvājumos vai līgumos, kas izveidoti šim klientam, ja piedāvājuma vai projekta līguma izveidošanas datums atbilst cenrāža darbības laikam.</span><span class="sxs-lookup"><span data-stu-id="547d8-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="547d8-116">Pielāgotas cenas projekta piedāvājumos</span><span class="sxs-lookup"><span data-stu-id="547d8-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="547d8-117">Projekta piedāvājumos var būt projekta izcenojums, kas sākas ar noklusējuma standarta cenrādi, kas pēc noklusējuma tiek ņemts no klienta vai no projekta parametriem.</span><span class="sxs-lookup"><span data-stu-id="547d8-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="547d8-118">Kad konkrētam piedāvājumam ir nepieciešama pielāgota cenu noteikšana ar projektu saistītam darbam, to var iegūt no projekta cenrāža saistītās entītijas.</span><span class="sxs-lookup"><span data-stu-id="547d8-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="547d8-119">Izpildiet tālāk aprakstītās darbības, lai iestatītu piedāvājumam specifiskas projekta cenas.</span><span class="sxs-lookup"><span data-stu-id="547d8-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="547d8-120">Atveriet projekta piedāvājumu un atlasiet cilni **Projekta cenrāži**.</span><span class="sxs-lookup"><span data-stu-id="547d8-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="547d8-121">Apakšrežģī atlasiet **Izveidot pielāgotu izcenojumu**.</span><span class="sxs-lookup"><span data-stu-id="547d8-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="547d8-122">Visi piedāvājumam pievienotie projekta cenrāži tiek pārkopēti uz jauniem cenrāžiem.</span><span class="sxs-lookup"><span data-stu-id="547d8-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="547d8-123">Jauno cenrāžu nosaukumi atspoguļo piedāvājuma nosaukumu ar datuma laikspiedolu, kad ir izveidoti šie cenrāži.</span><span class="sxs-lookup"><span data-stu-id="547d8-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="547d8-124">Varat izmantot katru no šiem cenrāžiem un veikt darba (lomas cena) un izmaksu (kategorijas cena) cenu atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="547d8-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="547d8-125">Šīs cenas ir piemērojamas tikai šim projekta piedāvājumam.</span><span class="sxs-lookup"><span data-stu-id="547d8-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="547d8-126">Projekta līguma cenrāži</span><span class="sxs-lookup"><span data-stu-id="547d8-126">Price lists on a project contract</span></span>

<span data-ttu-id="547d8-127">Projekta līgumā projekta cenas vienmēr pēc noklusējuma tiek iestatītas kā pielāgots cenrādis, kura nosaukumam pievienots līguma nosaukums un izveides datuma laikspiedols.</span><span class="sxs-lookup"><span data-stu-id="547d8-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="547d8-128">Tas attiecas gan uz līgumiem, kas izveidoti uzvarētiem piedāvājumiem, gan arī uz pilnīgi jauniem izveidotiem līgumiem.</span><span class="sxs-lookup"><span data-stu-id="547d8-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="547d8-129">Ja nepieciešams, varat noņemt šo saistību ar pielāgoto cenrādi un tā vietā projekta līgumam piesaistīt standarta cenrādi.</span><span class="sxs-lookup"><span data-stu-id="547d8-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="547d8-130">Kad standarta cenrādis tiek saistīts ar piedāvājuma vai līguma projekta cenrāžiem, jebkuras izmaiņas cenrāža cenās ietekmēs visus piedāvājumus un līgumus, kas izmanto cenrādi.</span><span class="sxs-lookup"><span data-stu-id="547d8-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
