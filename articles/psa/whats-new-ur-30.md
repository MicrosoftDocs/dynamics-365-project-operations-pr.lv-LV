---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 30, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852873"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="cc19c-103">Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 30, V3</span><span class="sxs-lookup"><span data-stu-id="cc19c-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cc19c-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="cc19c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cc19c-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="cc19c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cc19c-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="cc19c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cc19c-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="cc19c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cc19c-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cc19c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cc19c-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 30.</span><span class="sxs-lookup"><span data-stu-id="cc19c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="cc19c-110">Šīs versijas būvējuma numurs ir V 3.10.51.61, un tā ir vispārīgi pieejama, izmantojot 2021. gada aprīļa pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="cc19c-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="cc19c-111">Atjauninājumu izlaidums 30</span><span class="sxs-lookup"><span data-stu-id="cc19c-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cc19c-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="cc19c-112">Bug fixes</span></span>

<span data-ttu-id="cc19c-113">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="cc19c-113">**Time and Expense**</span></span>

<span data-ttu-id="cc19c-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="cc19c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc19c-115">Rodas kļūda, kad lapā **Ātrā izveide** izveidojat un saglabājat laika ierakstu, ja ir noņemts lauks **Loma**.</span><span class="sxs-lookup"><span data-stu-id="cc19c-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="cc19c-116">Filtrs Laika ievade lieto nepareizo filtra operatoru.</span><span class="sxs-lookup"><span data-stu-id="cc19c-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="cc19c-117">Kad laika ievades vadīklā atlasāt **Kopēt nedēļu**, kopētās laika uzskaites tabulas netiek automātiski parādītas.</span><span class="sxs-lookup"><span data-stu-id="cc19c-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="cc19c-118">**Resursu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="cc19c-118">**Resource Management**</span></span>

<span data-ttu-id="cc19c-119">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="cc19c-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc19c-120">Paplašinot rezervāciju, rezervācijas statuss, kas piešķirts stingrajai rezervācijai, ir nepareizs.</span><span class="sxs-lookup"><span data-stu-id="cc19c-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="cc19c-121">Paplašinot rezervāciju, tiek ņemts vērā rezervācijas statuss, kas rezervācijas iestatīšanas metadatos definēts kā **Iesniegts**.</span><span class="sxs-lookup"><span data-stu-id="cc19c-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="cc19c-122">Ja nav norādīts derīgs rezervācijas statuss, kļūdas ziņojums nav pareizi lokalizēts.</span><span class="sxs-lookup"><span data-stu-id="cc19c-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="cc19c-123">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="cc19c-123">**Project Management**</span></span>

<span data-ttu-id="cc19c-124">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="cc19c-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc19c-125">Nevar izveidot projektus vienā valūtā un ietvert saistītos uzdevumus citā valūtā.</span><span class="sxs-lookup"><span data-stu-id="cc19c-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="cc19c-126">**Pārdošana**</span><span class="sxs-lookup"><span data-stu-id="cc19c-126">**Sales**</span></span>

<span data-ttu-id="cc19c-127">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="cc19c-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc19c-128">Veicot cenrāža kopēšanu, cenas netiek atjauninātas.</span><span class="sxs-lookup"><span data-stu-id="cc19c-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="cc19c-129">Neizdodas slēgt piedāvajumu kā uzvarētu, ja izmaksu detalizētai informācijai ir izcelsmes vērtība.</span><span class="sxs-lookup"><span data-stu-id="cc19c-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="cc19c-130">Entītijā **Projekta uzdevums** **Izmaksu aprēķins** ir pārdēvēts par **Plānotās izmaksas (pamatvalūtā)**.</span><span class="sxs-lookup"><span data-stu-id="cc19c-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="cc19c-131">Izveidojot vai dzēšot rēķinus, tiek ģenerēts nulles atsauces izņēmums.</span><span class="sxs-lookup"><span data-stu-id="cc19c-131">A null reference exception is generated when invoices are created or deleted.</span></span>
