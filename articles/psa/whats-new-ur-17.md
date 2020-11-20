---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 17, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 17, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: bb93208217972639f91b39b7b6705d9897373ef7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126808"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="ff9f8-103">Project Service Automation atjauninājumu izlaidums 17, V3</span><span class="sxs-lookup"><span data-stu-id="ff9f8-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="ff9f8-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ff9f8-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="ff9f8-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ff9f8-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="ff9f8-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ff9f8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ff9f8-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti PSA V3, atjauninājuma izlaidumā 17.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="ff9f8-110">Šīs versijas būvējuma numurs ir V3.10.6.34, un tas parasti ir pieejams, izmantojot 2020. gada marta pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="ff9f8-111">Atjauninājumu izlaidums 17</span><span class="sxs-lookup"><span data-stu-id="ff9f8-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ff9f8-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="ff9f8-112">Bug fixes</span></span>

<span data-ttu-id="ff9f8-113">**Vispārīgi**</span><span class="sxs-lookup"><span data-stu-id="ff9f8-113">**General**</span></span>

- <span data-ttu-id="ff9f8-114">Izlabots: atjauniniet pakalpojumu Project Service Automation, lai ieviestu darba grupas dalībnieku licences (projekta resursu centrmezgls iekļaus darba grupas dalībnieku pakalpojumu plānu metadatiem 3.x)</span><span class="sxs-lookup"><span data-stu-id="ff9f8-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="ff9f8-115">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="ff9f8-115">**Time and Expense**</span></span>

- <span data-ttu-id="ff9f8-116">Izlabots: nav iespējams mainīt izdevumu aplēses no cenas, kas nav nulle, uz nulli (0).</span><span class="sxs-lookup"><span data-stu-id="ff9f8-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="ff9f8-117">Izmaiņas tiek ignorētas.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-117">The change is ignored.</span></span>

<span data-ttu-id="ff9f8-118">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="ff9f8-118">**Project Management**</span></span>

- <span data-ttu-id="ff9f8-119">Izlabots: darba grupas dalībnieka amata nosaukumam ir pievienota nulle vērtības pārbaude.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="ff9f8-120">Izlabots: entītijas **msdyn_resourceassignment** lauks **msdyn_userresourceid** vairs nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="ff9f8-121">Izlabots: jauninot no versijas 2.x uz 3.x, tagad uzdevumu piešķirēs tiek apstrādātas tukšas ieguldījumu kontūras.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="ff9f8-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ff9f8-122">**Sales**</span></span>

- <span data-ttu-id="ff9f8-123">Izlabots: parametrs **Invoice.PreValidateInvoiceUpdate** tagad atbilstoši apstrādā ieraksta īpašnieku atkārtotu piešķiršanu.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="ff9f8-124">Izlabots: ja transakcijas klase ir **Laiks**, parametrs **UnitGroup** nav rediģējams visām entītijām, tostarp **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** un **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="ff9f8-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="ff9f8-125">Taču parametrs **Vienība** nav rediģējams tikai entītijai **JournalLine** un **InvoiceLineDetails.**</span><span class="sxs-lookup"><span data-stu-id="ff9f8-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


