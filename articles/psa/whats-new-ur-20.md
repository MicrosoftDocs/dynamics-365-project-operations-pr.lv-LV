---
title: Kas jauns vai mainīts Project Service Automation atjauninājumu izlaidumā 20, V3
description: Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir pieejami Project Service Automation atjauninājumu izlaidumā 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ef24c20f3fa520b25a14773a15363a0f04f98d36
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126762"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="405cd-103">Project Service Automation atjauninājumu izlaidums 20, V3</span><span class="sxs-lookup"><span data-stu-id="405cd-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="405cd-104">Mēs priecājamies paziņot par jaunāko Dynamics 365 pakalpojuma Project Service Automation atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="405cd-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="405cd-105">Šajā laidienā ir ietverti daži svarīgi uzlabojumi attiecībā uz kvalitāti, veiktspēju un lietojamību.</span><span class="sxs-lookup"><span data-stu-id="405cd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="405cd-106">Šis laidiens ir saderīgs ar Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="405cd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="405cd-107">Lai atjauninātu šo laidienu, apmeklējiet administrēšanas centru Dynamics 365 tiešsaistē un dodieties uz risinājumu lapu, lai instalētu atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="405cd-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="405cd-108">Lai iegūtu papildinformācijum, skatiet [Vēlamā risinājuma instalēšana, atjaunināšana vai noņemšana](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="405cd-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="405cd-109">Šajā tēmā ir uzskaitīti līdzekļi un labojumi, kas ir jauni vai mainīti Project Service Automation V3, atjauninājuma izlaidumā 20.</span><span class="sxs-lookup"><span data-stu-id="405cd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="405cd-110">Šīs versijas būvējuma numurs ir V 3.10.31.37, un tā ir vispārīgi pieejama, izmantojot 2020. gada jūnija pašatjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="405cd-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="405cd-111">Atjauninājumu izlaidums 20</span><span class="sxs-lookup"><span data-stu-id="405cd-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="405cd-112">Kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="405cd-112">Bug fixes</span></span>

<span data-ttu-id="405cd-113">**Projekta pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="405cd-113">**Project Management**</span></span>

<span data-ttu-id="405cd-114">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="405cd-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="405cd-115">Projekta darba grupas dalībnieku importēšana ar piešķiršanas metodi, kurai ir nepieciešamas stundas, izraisa neskaidru kļūdas ziņojumu, kad noteiktās stundas ir nulle.</span><span class="sxs-lookup"><span data-stu-id="405cd-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="405cd-116">Lietotāji saņem nepareiza kļūda, ja projekta uzdevuma laukā **Apraksts** ir ievadīti maksimālais rakstzīmju skaits.</span><span class="sxs-lookup"><span data-stu-id="405cd-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="405cd-117">Kad lietotāja valodas iestatījumos ir iestatīta japāņu valoda, **Microsoft Dynamics 365 Project Service Automation pievienojumprogrammu lejupielādes** lapa novirza uz lejupielādes lapu angļu valodā.</span><span class="sxs-lookup"><span data-stu-id="405cd-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="405cd-118">Kad rodas servera kļūda, dažreiz paliek sinhronizācijas etiķete, kas atrodas veidlapas **Projekti** cilnē **Grafiks**.</span><span class="sxs-lookup"><span data-stu-id="405cd-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="405cd-119">Kad uzdevums tiek modificēts, uz serveri tiek nosūtīti lieki uzdevuma atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="405cd-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="405cd-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="405cd-120">**Sales**</span></span>

<span data-ttu-id="405cd-121">Ir novērstas tālāk norādītās problēmas.</span><span class="sxs-lookup"><span data-stu-id="405cd-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="405cd-122">Veidlapā **Līgums** veicot dubultklikšķi uz **Izveidot rēķinu**, tiek izveidoti divi rēķinus vienam faktiskajam ierakstam.</span><span class="sxs-lookup"><span data-stu-id="405cd-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="405cd-123">Lietotāji nevar izveidot izdevumu ierakstus programmā Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="405cd-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="405cd-124">Izmaksu apvērse un rēķinā neiekļauto pārdošanas datu apvērse nav saistītas.</span><span class="sxs-lookup"><span data-stu-id="405cd-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="405cd-125">POga **Atsvaidzināt faktiskos datus** veidlapā **Projekts** neatsvaidzina **Uzdevuma faktisko stundu skaits**.</span><span class="sxs-lookup"><span data-stu-id="405cd-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="405cd-126">Spraudnis **PreValidateProjectTeamMemberCreate** var izveidot dublikātus vispārējiem rezervējamiem resursiem, ja atribūts **msdyn_isgenericresourceprojectscoped** ir iestatīts uz **Aplams**.</span><span class="sxs-lookup"><span data-stu-id="405cd-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="405cd-127">**Pārrēķināt** notīra ar produktiem saistītu piedāvājumu rindas detalizētas informācijas un līgumu rindu detalizētas informācijas rēķinā iekļaujamās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="405cd-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="405cd-128">Noteiktos scenārijos spraudnis **PostEstimateLineUpdate** rāda nulles atsauces kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="405cd-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="405cd-129">Laika fāzes ilgums **Rentabilitātes analīzes diagrammā** neatbilst izmaksu ilgumam piedāvājuma fiksētas cenas piedāvājuma rindas detalizētajā informācijā.</span><span class="sxs-lookup"><span data-stu-id="405cd-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="405cd-130">Vienību un vienību grupu vērtības izmaksu kategorijām veidlapās **Līguma rindu informācija** un **Piedāvājumu rindu informācija** netiek pareizi iestatītas uz noklusējumu.</span><span class="sxs-lookup"><span data-stu-id="405cd-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="405cd-131">Saraksts **Organizācijas vienību izmaksu cenrādis** ļauj pārklāties spēkā esamības datumiem.</span><span class="sxs-lookup"><span data-stu-id="405cd-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="405cd-132">Lietotājiem nav atļauts mainīt **OrgUnit**, ja pasūtījuma tips ir neatkarīgs no darba, jo tas izraisa nulles atsauces izņēmumu kļūdu.</span><span class="sxs-lookup"><span data-stu-id="405cd-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="405cd-133">Mēģinot naviģēt no veidlapas **Piedāvājuma rindu informācija** atpakaļ uz cilni **Piedāvājums**, veidlapa tiek atsvaidzināta un parāda cilni **Kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="405cd-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
