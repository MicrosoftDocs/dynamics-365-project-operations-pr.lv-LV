---
title: Pārdošanas procesi
description: Šajā tēmā ir sniegta informācija par pamata pārdošanas procesiem.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 38e02018e46943f53680babd12c7bede0a5d19de
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129327"
---
# <a name="sales-processes"></a><span data-ttu-id="343b3-103">Pārdošanas procesi</span><span class="sxs-lookup"><span data-stu-id="343b3-103">Sales processes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="343b3-104">Pārdošanas procesi, kas tiek izmantoti uz projektu balstītā organizācijā, atšķiras no pārdošanas procesiem, kas tiek izmantoti uz preci balstītā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="343b3-104">The sales processes that are used in a project-based organization differ from the sales processes that are used in a product-based organization.</span></span> <span data-ttu-id="343b3-105">Šī atšķirība rodas tāpēc, ka uz projektu balstītu organizāciju pārdošanas cikli ir garāki un tiem ir nepieciešamas pielāgotas novērtēšanas metodes, lai analizētu un izveidotu piedāvājumus katram darījumam.</span><span class="sxs-lookup"><span data-stu-id="343b3-105">This difference occurs because the sales cycles for project-based organizations are longer and require customized estimation techniques to analyze and create quotes for each deal.</span></span> <span data-ttu-id="343b3-106">Dynamics 365 Project Service Automation izmanto daļu no tās pašas funkcionalitātes, kas tiek izmantota Dynamics 365 Sales pārdošanas procesā.</span><span class="sxs-lookup"><span data-stu-id="343b3-106">Dynamics 365 Project Service Automation uses some of the same functionality that is used in the sales process for Dynamics 365 Sales.</span></span> <span data-ttu-id="343b3-107">Lūk, daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="343b3-107">Here are some examples:</span></span>

- <span data-ttu-id="343b3-108">Entītija Interesents tiek izmantota, lai izsekotu pārdošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="343b3-108">A Lead entity is used to track the sales process.</span></span>
- <span data-ttu-id="343b3-109">Kvalificētie interesenti tiek izsekoti kā iespējas.</span><span class="sxs-lookup"><span data-stu-id="343b3-109">Qualifying leads are tracked as opportunities.</span></span> <span data-ttu-id="343b3-110">Pārdošanas process var sākties arī ar iespēju.</span><span class="sxs-lookup"><span data-stu-id="343b3-110">The sales process can also start with opportunity.</span></span>
- <span data-ttu-id="343b3-111">Var piekļūt visiem ar iespēju saistītajiem artefaktiem.</span><span class="sxs-lookup"><span data-stu-id="343b3-111">All related artifacts for an opportunity are accessed.</span></span> <span data-ttu-id="343b3-112">Šie artefakti ietver pārdošanas darba grupu, ieinteresētās puses, varbūtību, vērtējumu, pārdošanas posmus un biznesa procesus.</span><span class="sxs-lookup"><span data-stu-id="343b3-112">These artifacts include the sales team, stakeholders, probability, rating, sales stages, and business processes.</span></span>
- <span data-ttu-id="343b3-113">Iespējai tiek izveidoti vairāki piedāvājumi.</span><span class="sxs-lookup"><span data-stu-id="343b3-113">Multiple quotes are created for an opportunity.</span></span>
- <span data-ttu-id="343b3-114">Piedāvājums tiek atzīmēts ar **Slēgts kā iegūts**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="343b3-114">A quote is marked **Closed as Won** to create a sales order.</span></span> <span data-ttu-id="343b3-115">Programmā PSA pārdošanas pasūtījums ir pielāgots, un to dēvē par projekta līgumu.</span><span class="sxs-lookup"><span data-stu-id="343b3-115">In PSA, the sales order is customized and is called a project contract.</span></span>

<span data-ttu-id="343b3-116">Tālāk esošajā attēlā ir parādīts tipisks pārdošanas process uz projektu balstītā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="343b3-116">The following illustration shows a typical sales process in a project-based organization.</span></span>

> ![Pārdošanas process uz projektu balstītā organizācijā](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a><span data-ttu-id="343b3-118">Pārdošanas novērtēšana</span><span class="sxs-lookup"><span data-stu-id="343b3-118">Estimating a sale</span></span>
<span data-ttu-id="343b3-119">Pārdošanas vērtību var novērtēt, pamatojoties uz iepriekš piegādātajiem projektiem un projektu sarežģītības.</span><span class="sxs-lookup"><span data-stu-id="343b3-119">The value of a sale can be estimated based on projects that have previously been delivered and the complexity of projects.</span></span> <span data-ttu-id="343b3-120">Projektiem, kas ietver iepriekšējo projektu pagarinājumus, vai projektiem, kuros kreditora zināšanu līmenis ir augsts un tiek izmantotas labi pazīstamas darba veidnes, varat izmantot vienkāršāku novērtēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="343b3-120">For projects that involve extensions to previous projects, or projects where the vendor's expertise is high and well-known work templates are used, you can use a simpler estimation process.</span></span> <span data-ttu-id="343b3-121">Sarežģītākiem projektiem parasti ir ilgāks pirkšanas process.</span><span class="sxs-lookup"><span data-stu-id="343b3-121">More complex projects usually have a longer purchase process.</span></span> <span data-ttu-id="343b3-122">Tāpēc pārdošanas novērtēšanas procesā ir vairāk posmu.</span><span class="sxs-lookup"><span data-stu-id="343b3-122">Therefore, there are more stages in the sales estimation process.</span></span> <span data-ttu-id="343b3-123">Procesa sākumā pārdošanas darba grupa izmanto uzņēmumu vadītāju un jomas speciālistu (SME) ieguldījumu, lai sāktu veidot augsta līmeņa novērtējumu attiecībā uz katru atsevišķo piedāvājumā iekļauto darba komponentu.</span><span class="sxs-lookup"><span data-stu-id="343b3-123">Early in the process, the sales team uses the input of account managers and subject matter experts (SMEs) to start to create a high-level estimate for each distinct component of work that is quoted.</span></span> <span data-ttu-id="343b3-124">Šie darba komponenti ir norādīti piedāvājuma rindās.</span><span class="sxs-lookup"><span data-stu-id="343b3-124">These components of work are represented by quote lines.</span></span> 

<span data-ttu-id="343b3-125">Varat izveidot augsta līmeņa piedāvājuma novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="343b3-125">You can create a high-level estimate of the quote.</span></span> <span data-ttu-id="343b3-126">Visbeidzot, šis augsta līmeņa novērtējums tiks aizstāts ar detalizētāku novērtējumu, kura pamatā ir projekta plāns, ko izveidojat, izmantojot standartizētas projekta veidnes.</span><span class="sxs-lookup"><span data-stu-id="343b3-126">Eventually, this high-level estimate will be replaced by a more detailed estimate that is based on a project plan that you create by using the standardized project templates.</span></span> <span data-ttu-id="343b3-127">Šīs veidnes palīdz izveidot grafiku un noteikt piedāvājuma un tā komponentu (piedāvājuma rindu) naudas vērtības.</span><span class="sxs-lookup"><span data-stu-id="343b3-127">These templates help you build a schedule and determine monetary values on the quote and its components (quote lines).</span></span> 

<span data-ttu-id="343b3-128">Varat izveidot projektam vairākus piedāvājumus un grupēt tos, izmantojot vienu iespējas entītijas tipu.</span><span class="sxs-lookup"><span data-stu-id="343b3-128">You can create multiple quotes for a project and group them under a single opportunity entity type.</span></span> <span data-ttu-id="343b3-129">Visbeidzot, viens no šiem piedāvājumiem tiek atzīmēts ar **Slēgts kā iegūts**, un tiek izveidots projekta līgums vai darba paziņojums (SOW).</span><span class="sxs-lookup"><span data-stu-id="343b3-129">Eventually, one of those quotes is marked **Closed as Won**, and a project contract or statement of work (SOW) is created.</span></span> <span data-ttu-id="343b3-130">Projekta līgumā ir ietverta katra komponenta (līguma rindas) līguma vērtība, ko klients akceptējis piegādei.</span><span class="sxs-lookup"><span data-stu-id="343b3-130">A project contract holds the contracted value for each component (contract line) that is accepted by the customer for delivery.</span></span> <span data-ttu-id="343b3-131">SOW parasti izveido kā Microsoft Word dokumentu.</span><span class="sxs-lookup"><span data-stu-id="343b3-131">An SOW is usually created as a Microsoft Word document.</span></span> <span data-ttu-id="343b3-132">Visi rēķini, kas klientam nosūtīti projekta piegādes laikā, ietver atsauci uz projekta līgumu vai SOW.</span><span class="sxs-lookup"><span data-stu-id="343b3-132">All invoices that are sent to the customer over the course of the project's delivery reference the project contract or SOW.</span></span>

<span data-ttu-id="343b3-133">Varat arī izveidot alternatīvus piedāvājumus ar vienu iespējas entītijas tipu vai iestatīt sistēmu tā, lai projekta līgums tiktu izveidots pēc piedāvājuma iegūšanas.</span><span class="sxs-lookup"><span data-stu-id="343b3-133">You can also create alternate quotes under one opportunity entity type or set up the system so that a project contract is created when a quote is won.</span></span> <span data-ttu-id="343b3-134">Šajā gadījumā varat pievienot Word dokumentu, kas norāda SOW projekta līguma ierakstam.</span><span class="sxs-lookup"><span data-stu-id="343b3-134">In this case, you can attach a Word document that represents the SOW to the project contract record.</span></span>

![Piedāvājuma slēgšana, lai izveidotu projekta līgumu](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a><span data-ttu-id="343b3-136">Pārdošanas procesa konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="343b3-136">Configuring the sales process</span></span>
<span data-ttu-id="343b3-137">Varat izmantot biznesa procesa plūsmas (BPF) programmā Microsoft Dynamics 365, lai konfigurētu pārdošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="343b3-137">You can use business process flows (BPFs) in Microsoft Dynamics 365 to configure your sales process.</span></span> <span data-ttu-id="343b3-138">BPF piešķiriet pārdošanas personālam vadītu vizuālo interfeisu, ko tas var izmantot, lai virzītu darījumus cauri posmiem, kas ir tipiski jūsu uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="343b3-138">BPFs give your sales staff a guided visual interface that they can use to move deals forward through the stages that are typical for your company.</span></span>

<span data-ttu-id="343b3-139">Jūsu uzņēmumā var būt, piemēram, tālāk norādītie seši pārdošanas procesa posmi.</span><span class="sxs-lookup"><span data-stu-id="343b3-139">For example, your company might have the following six stages in the sales process:</span></span>

1. <span data-ttu-id="343b3-140">Kvalificēšana</span><span class="sxs-lookup"><span data-stu-id="343b3-140">Qualify</span></span>
2. <span data-ttu-id="343b3-141">Novērtējums</span><span class="sxs-lookup"><span data-stu-id="343b3-141">Estimate</span></span>
3. <span data-ttu-id="343b3-142">Iekšējā pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="343b3-142">Internal review</span></span>
4. <span data-ttu-id="343b3-143">Līgums</span><span class="sxs-lookup"><span data-stu-id="343b3-143">Contract</span></span>
5. <span data-ttu-id="343b3-144">Piegādāt</span><span class="sxs-lookup"><span data-stu-id="343b3-144">Deliver</span></span>
6. <span data-ttu-id="343b3-145">Aizvērt</span><span class="sxs-lookup"><span data-stu-id="343b3-145">Close</span></span>

<span data-ttu-id="343b3-146">Šos sešus posmus apzīmē skujiņas (\>), ko atlasāt, lai izvērstu katru jūsu izveidoto iespējas entītijas tipu.</span><span class="sxs-lookup"><span data-stu-id="343b3-146">These six stages are represented by chevrons (\>) that you select to expand in each opportunity entity type that you create.</span></span>

![Biznesa procesu konfigurācija programmā Dynamics 365](media/basic-guide-3.png)
 
<span data-ttu-id="343b3-148">Jūsu organizācija var izmantot dažādas entītijas, lai apzīmētu to pašu darījumu dažādās tā attīstības fāzēs.</span><span class="sxs-lookup"><span data-stu-id="343b3-148">Your organization might use different entities to represent the same deal as it evolves.</span></span> <span data-ttu-id="343b3-149">Pārdošanas procesa sākumā darījumu apzīmē entītija Iespēja.</span><span class="sxs-lookup"><span data-stu-id="343b3-149">Early in the sales process, a deal is represented by the Opportunity entity.</span></span> <span data-ttu-id="343b3-150">Laika gaitā, kad parādās papildinformācija, varat izmantot augsta līmeņa novērtējumus, lai izveidotu vienu vai vairākus piedāvājumus.</span><span class="sxs-lookup"><span data-stu-id="343b3-150">As time passes and more details emerge, you might use high-level estimates to create one or more quotes.</span></span> <span data-ttu-id="343b3-151">Ja kādu no šiem piedāvājumiem pārskata iekšējās un klienta ieinteresētās puses, darījumu apzīmē entītija Piedāvājums.</span><span class="sxs-lookup"><span data-stu-id="343b3-151">If one of these quotes is reviewed by internal and customer stakeholders, the Quote entity represents the deal.</span></span> <span data-ttu-id="343b3-152">Pēc tam, kad klients ir akceptējis piedāvājumu, darījumu apzīmē projekta līgums vai SOW.</span><span class="sxs-lookup"><span data-stu-id="343b3-152">After the customer accepts the quote, a project contract or SOW represents the deal.</span></span> <span data-ttu-id="343b3-153">Lai atbalstītu šo uzvedību, BPF ir strukturēts tā, lai katrs procesa posms tiktu saistīts ar citu datu bāzes tabulu.</span><span class="sxs-lookup"><span data-stu-id="343b3-153">To support this behavior, BPFs are structured so that each stage in the process is linked to a different database table.</span></span>

<span data-ttu-id="343b3-154">Posmu **Kvalificēšana** pārdošanas procesā var atbalstīt ar entītiju Iespēja.</span><span class="sxs-lookup"><span data-stu-id="343b3-154">The **Qualify** stage in the sales process can be backed by an Opportunity entity.</span></span> <span data-ttu-id="343b3-155">Posmus **Novērtējums** un **Iekšējā pārskatīšana** var atbalstīt ar entītiju Piedāvājums.</span><span class="sxs-lookup"><span data-stu-id="343b3-155">The **Estimate** and **Internal Review** stages can be backed by a Quote entity.</span></span> <span data-ttu-id="343b3-156">Posmus **Līgums**, **Piegāde** un **Slēgšana** var atbalstīt ar entītiju Projekta līgums.</span><span class="sxs-lookup"><span data-stu-id="343b3-156">The **Contract**, **Delivery**, and **Close** stages can be backed by a Project Contract entity.</span></span>

<span data-ttu-id="343b3-157">Virzot darījumus cauri posmiem, saņemsit aicinājumu izveidot atbilstošo entītijas ierakstu, kas palīdzēs izpildīt procesu un vadīs to.</span><span class="sxs-lookup"><span data-stu-id="343b3-157">As you move deals through the stages, you're prompted to create the appropriate entity record to help and guide you through the process.</span></span> <span data-ttu-id="343b3-158">Posmi var būt nosacījuma.</span><span class="sxs-lookup"><span data-stu-id="343b3-158">The stages can be conditional.</span></span> <span data-ttu-id="343b3-159">Piemēram, ja piedāvājumam iekšēja pārskatīšana ir nepieciešama tikai tad, ja piedāvājumā ir izmantots pielāgots cenrādis, varat šo nosacījumu konfigurēt atbilstošajā biznesa procesa posmā.</span><span class="sxs-lookup"><span data-stu-id="343b3-159">For example, if you require an internal review of a quote only if the quote uses a custom price list, you can configure that condition in the appropriate stage of the business process.</span></span> <span data-ttu-id="343b3-160">Šādi posms **Iekšējā pārskatīšana** tiek rādīts tikai piedāvājumiem, kas izmanto pielāgotu cenrādi.</span><span class="sxs-lookup"><span data-stu-id="343b3-160">The **Internal Review** stage is then shown only for quotes that use a custom price list.</span></span> <span data-ttu-id="343b3-161">Attiecībā uz visiem citiem darījumiem un piedāvājumiem pēc posma **Novērtējums** seko posms **Līgums**.</span><span class="sxs-lookup"><span data-stu-id="343b3-161">For all other deals and quotes, the **Estimate** stage is followed by the **Contract** stage.</span></span>

> [!NOTE]
> <span data-ttu-id="343b3-162">Programmā PSA ir entītijām Iespēja, Piedāvājums, Pasūtījums un Rēķins paredzētas lapas.</span><span class="sxs-lookup"><span data-stu-id="343b3-162">PSA has specific pages for the Opportunity, Quote, Order, and Invoice entities.</span></span> <span data-ttu-id="343b3-163">Jums ir jāizveido projekta pakalpojumu iespējas, piedāvājumi, pasūtījumi un rēķini, izmantojot šo entītiju projekta informācijas lapas.</span><span class="sxs-lookup"><span data-stu-id="343b3-163">You must create project service opportunities, quotes, orders, and invoices using the project information pages for these entities.</span></span> <span data-ttu-id="343b3-164">Ja ieraksta izveidei izmantosit citu lapu, nevarēsit atvērt šo ierakstu lapā **Projekta informācija**.</span><span class="sxs-lookup"><span data-stu-id="343b3-164">If you use another page to create a record, you won't be able to open the record from the **Project Information** page.</span></span> <span data-ttu-id="343b3-165">Ja vēlaties ierakstu atvērt lapā **Projekta informācija**, jums ir jādzēš ieraksts un tas atkārtoti jāizveido, izmantojot lapu **Projekta informācija**.</span><span class="sxs-lookup"><span data-stu-id="343b3-165">If you want to open a record from the **Project Information** page, you must delete the record and recreate it using the **Project Information** page.</span></span> <span data-ttu-id="343b3-166">Lapā **Projekta informācija** katra šo entītiju tipu biznesa loģika nodrošina, ka ieraksta lauks **Tips** ir iestatīts pareizi un visas obligātās koncepcijas ir pareizi inicializētas.</span><span class="sxs-lookup"><span data-stu-id="343b3-166">On the **Project Information** page, business logic for each of these entity types ensures that the **Type** field of the record is set correctly, and all of the mandatory concepts are properly initialized.</span></span>

> ![Jauna pasūtījuma projekta informācija](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a><span data-ttu-id="343b3-168">Atšķirības starp Project Service Automation un Sales</span><span class="sxs-lookup"><span data-stu-id="343b3-168">Differences between Project Service Automation and Sales</span></span>
<span data-ttu-id="343b3-169">Lai gan pārdošanas process programmā PSA izmanto programmā Sales pieejamās pārdošanas procesa pamata iespējas, tam ir dažas būtiskas atšķirības, jo uz projektu balstītās organizācijās pastāv dažādas biznesa prakses.</span><span class="sxs-lookup"><span data-stu-id="343b3-169">Although the sales process in PSA uses the basic capabilities of the sales process in Sales, it does have some key differences because of variations in the business practices of project-based organizations.</span></span> <span data-ttu-id="343b3-170">Lūk, daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="343b3-170">Here are some examples:</span></span>

- <span data-ttu-id="343b3-171">**Projekta piedāvājumi** — programmā Project Service Automation piedāvājums tiek slēgts, kad no piedāvājuma tiek izveidots projekta līgums.</span><span class="sxs-lookup"><span data-stu-id="343b3-171">**Project quotes** – In Project Service Automation, a quote is closed after a project contract is created from a quote.</span></span> <span data-ttu-id="343b3-172">Programmā Sales piedāvājumu var saglabāt atvērtu pēc tam, kad tas ir iegūts.</span><span class="sxs-lookup"><span data-stu-id="343b3-172">In Sales, you can keep a quote open after you've won it.</span></span> <span data-ttu-id="343b3-173">Šīs atšķirības iemesls ir tāds, ka piedāvājuma un projekta līguma atbilstība ir piemērotāka uz projektu balstītām organizācijām.</span><span class="sxs-lookup"><span data-stu-id="343b3-173">The reason for this difference is that a match between a quote and a project contract is better for project-based organizations.</span></span> 
- <span data-ttu-id="343b3-174">**Aktivizēšana un pārskatījumi** — programmā PSA aktivizēšana un pārskatījumi netiek atbalstīti projekta piedāvājumiem.</span><span class="sxs-lookup"><span data-stu-id="343b3-174">**Activation and revisions** – In PSA, activation and revisions aren't supported for project quotes.</span></span> <span data-ttu-id="343b3-175">Programmā Sales piedāvājumu var bloķēt, lai neļautu veikt papildu rediģēšanu.</span><span class="sxs-lookup"><span data-stu-id="343b3-175">In Sales, a quote can be locked to prevent additional edits.</span></span>
- <span data-ttu-id="343b3-176">**Zaudēta vai iegūta piedāvājuma slēgšana** — kad programmā PSA projekta piedāvājums tiek slēgts kā iegūts vai zaudēts, iespēja paliek atvērta.</span><span class="sxs-lookup"><span data-stu-id="343b3-176">**Closing a quote as lost or won** – In PSA, when a project quote is closed as won or lost, the opportunity remains open.</span></span> <span data-ttu-id="343b3-177">Visi pārējie iespējas piedāvājumi tiek slēgti kā zaudēti.</span><span class="sxs-lookup"><span data-stu-id="343b3-177">All other quotes on the opportunity are closed as lost.</span></span> <span data-ttu-id="343b3-178">Kad programmā Sales piedāvājums tiek slēgts kā iegūts vai zaudēts, lietotājam tiek parādīts aicinājums veikt darbību iespējā.</span><span class="sxs-lookup"><span data-stu-id="343b3-178">In Sales, when a quote is closed as won or lost, the user is prompted to take an action on the opportunity.</span></span> <span data-ttu-id="343b3-179">Atkarībā no lietotāja ievades pamatā esošā iespēja var tikt slēgta vai saglabāta atvērta.</span><span class="sxs-lookup"><span data-stu-id="343b3-179">Depending on the user input, the underlying opportunity might be closed or left open.</span></span>

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a><span data-ttu-id="343b3-180">Pārskatījumu izsekošana attiecībā uz piedāvājumiem un projekta plāniem pārdošanas ciklā</span><span class="sxs-lookup"><span data-stu-id="343b3-180">Tracking revisions to quotes and project plans in the sales cycle</span></span>
<span data-ttu-id="343b3-181">Programmā PSA nevar izsekot pārskatījumus, kas veikti piedāvājumā.</span><span class="sxs-lookup"><span data-stu-id="343b3-181">In PSA, you can't track revisions that are made to a quote.</span></span> <span data-ttu-id="343b3-182">Tā vietā ir jāatzīmē, ka esošais piedāvājums ir **Slēgts kā zaudēts**, un pēc tam jāizveido jauns piedāvājums.</span><span class="sxs-lookup"><span data-stu-id="343b3-182">Instead, you must mark the existing quote **Closed as Lost** and then create a new quote.</span></span> <span data-ttu-id="343b3-183">Izmantojot PSA, varat kopēt piedāvājumu vai klonēt uz projektu balstītu piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="343b3-183">You can copy a quote or clone a project-based quote by using PSA.</span></span>

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a><span data-ttu-id="343b3-184">Piedāvājumu un projekta līgumu komentāru un apstiprinājumu izsekošana</span><span class="sxs-lookup"><span data-stu-id="343b3-184">Tracking comments and approvals of quotes and project contracts</span></span>
<span data-ttu-id="343b3-185">Varat pārvaldīt piedāvājumu un projekta līgumu pārskatīšanu un apstiprināšanu, izmantojot Record Wall un ziņas.</span><span class="sxs-lookup"><span data-stu-id="343b3-185">You can manage the review and approval of quotes and project contracts by using the record wall and posts.</span></span> <span data-ttu-id="343b3-186">Jūsu organizācija var izveidot pielāgotas darbplūsmas un spraudņus, lai piešķirtu, pārvirzītu, eskalētu un pārvaldītu paziņojumus par darba vienumu pārskatīšanu un apstiprināšanu.</span><span class="sxs-lookup"><span data-stu-id="343b3-186">Your organization can create custom workflows and plug-ins to assign, redirect, escalate, and manage notifications of review and approval work items.</span></span>