---
title: Jaunumi 2021. janvārī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2021. gada janvāra laidienā Project Operations resursu/bez krājumu scenārijiem.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24a6f3b49b9c67b7c2d97461ab0f23a9a704dbc7
ms.sourcegitcommit: ef7d498bf80b0bcc1245dc42f30c410c31f891bb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/13/2021
ms.locfileid: "4958931"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="c9de1-103">Jaunumi 2021. janvārī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem</span><span class="sxs-lookup"><span data-stu-id="c9de1-103">What's new January 2021 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="c9de1-104">_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_</span><span class="sxs-lookup"><span data-stu-id="c9de1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="c9de1-105">Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:</span><span class="sxs-lookup"><span data-stu-id="c9de1-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

  - <span data-ttu-id="c9de1-106">Project Operations Dataverse vides versijā 4.6.0.154</span><span class="sxs-lookup"><span data-stu-id="c9de1-106">Project Operations on Dataverse environment version 4.6.0.154</span></span>
  - <span data-ttu-id="c9de1-107">Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.16</span><span class="sxs-lookup"><span data-stu-id="c9de1-107">Project management and accounting in Dynamics 365 Finance environment version 10.0.16</span></span>

## <a name="quality-updates"></a><span data-ttu-id="c9de1-108">Kvalitātes atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="c9de1-108">Quality updates</span></span>

### <a name="project-operations-on-dataverse"></a><span data-ttu-id="c9de1-109">Project Operations pakalpojumā Dataverse</span><span class="sxs-lookup"><span data-stu-id="c9de1-109">Project Operations on Dataverse</span></span>

| <span data-ttu-id="c9de1-110">**Līdzekļu apgabals**</span><span class="sxs-lookup"><span data-stu-id="c9de1-110">**Feature Area**</span></span> | <span data-ttu-id="c9de1-111">**Atsauces numurs**</span><span class="sxs-lookup"><span data-stu-id="c9de1-111">**Reference number**</span></span> | <span data-ttu-id="c9de1-112">**Kvalitātes atjauninājums**</span><span class="sxs-lookup"><span data-stu-id="c9de1-112">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c9de1-113">**Izvietošana un konfigurācija**</span><span class="sxs-lookup"><span data-stu-id="c9de1-113">**Deployment and configuration**</span></span> | <span data-ttu-id="c9de1-114">2106818</span><span class="sxs-lookup"><span data-stu-id="c9de1-114">2106818</span></span> | <span data-ttu-id="c9de1-115">Tīmekļa resursa pārdēvēšana, kas radīja problēmas ar lapas pielāgošanu tika novērsta.</span><span class="sxs-lookup"><span data-stu-id="c9de1-115">Fixed the webresource rename that was causing issues related to customizing a page.</span></span> |
| <span data-ttu-id="c9de1-116">**Cenu noteikšana un norēķini**</span><span class="sxs-lookup"><span data-stu-id="c9de1-116">**Billing and Pricing**</span></span> | <span data-ttu-id="c9de1-117">2091908</span><span class="sxs-lookup"><span data-stu-id="c9de1-117">2091908</span></span> | <span data-ttu-id="c9de1-118">Novērsta **Cenu noteikšanas bloķēšanas** un **Pašreizējās cenu noteikšanas izmantošanas** opciju lietošana lapā **Rēķins**, ja Project Operations instalē kopā ar Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="c9de1-118">Fixed the visibility of the **Lock pricing** and **Use Current Pricing** options on the **Invoice** page when Project Operations is installed together with Dynamics 365 Field Service.</span></span> |
| <span data-ttu-id="c9de1-119">**Cenu noteikšana un norēķini**</span><span class="sxs-lookup"><span data-stu-id="c9de1-119">**Billing and Pricing**</span></span> | <span data-ttu-id="c9de1-120">2103058</span><span class="sxs-lookup"><span data-stu-id="c9de1-120">2103058</span></span> | <span data-ttu-id="c9de1-121">Atsvaidzinātas **Projekta kopsummas**, lai apstrādātu uzdevuma faktisko izmaksu tukšās vērtības.</span><span class="sxs-lookup"><span data-stu-id="c9de1-121">Refreshed **Project Totals** to handle null values for the actual cost on a task.</span></span> |
| <span data-ttu-id="c9de1-122">**Cenu noteikšana un norēķini**</span><span class="sxs-lookup"><span data-stu-id="c9de1-122">**Billing and Pricing**</span></span> | <span data-ttu-id="c9de1-123">2116100</span><span class="sxs-lookup"><span data-stu-id="c9de1-123">2116100</span></span> | <span data-ttu-id="c9de1-124">Uzlaboti kļūdu ziņojumi, kas izmantoti ar funkcionalitāti **Labot ierakstu faktiskajiem datiem**.</span><span class="sxs-lookup"><span data-stu-id="c9de1-124">Improved error messages used with the functionality, **Correct Entries on Actuals**.</span></span> |
| <span data-ttu-id="c9de1-125">**Cenu noteikšana un norēķini**</span><span class="sxs-lookup"><span data-stu-id="c9de1-125">**Billing and Pricing**</span></span> | <span data-ttu-id="c9de1-126">2116129</span><span class="sxs-lookup"><span data-stu-id="c9de1-126">2116129</span></span> | <span data-ttu-id="c9de1-127">Uzlabota izdevumu aprēķinu redzamība lapas **Projekti** cilnē **Aprēķini**.</span><span class="sxs-lookup"><span data-stu-id="c9de1-127">Improved expense estimates visibility on the **Estimates** tab on the **Projects** page.</span></span> |
| <span data-ttu-id="c9de1-128">**Cenu noteikšana un norēķini**</span><span class="sxs-lookup"><span data-stu-id="c9de1-128">**Billing and Pricing**</span></span> | <span data-ttu-id="c9de1-129">2119112</span><span class="sxs-lookup"><span data-stu-id="c9de1-129">2119112</span></span> | <span data-ttu-id="c9de1-130">Salabota faktiskās pārdošanas un faktisko izmaksu apkopošana, ja tiek izmantoti atšķirīgi valūtas kursi.</span><span class="sxs-lookup"><span data-stu-id="c9de1-130">Fixed aggregation of actual sales and actual cost when different exchange rates are used.</span></span> |
| <span data-ttu-id="c9de1-131">**Cenu noteikšana un norēķini**</span><span class="sxs-lookup"><span data-stu-id="c9de1-131">**Billing and Pricing**</span></span> | <span data-ttu-id="c9de1-132">2134705</span><span class="sxs-lookup"><span data-stu-id="c9de1-132">2134705</span></span> | <span data-ttu-id="c9de1-133">Novērsta kļūda "Nevar lasīt rekvizītu **getResourceString** no nedefinētajiem", kad tiek atvērta lapa **Rēķins** un ir uzinstalēts Field Service.</span><span class="sxs-lookup"><span data-stu-id="c9de1-133">Fixed the error, "Cannot read property **getResourceString** of undefined" when the **Invoice** page is opened and Field Service is installed.</span></span> |
| <span data-ttu-id="c9de1-134">**Iespēju pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="c9de1-134">**Opportunity Management**</span></span> | <span data-ttu-id="c9de1-135">2022195</span><span class="sxs-lookup"><span data-stu-id="c9de1-135">2022195</span></span> | <span data-ttu-id="c9de1-136">Uzdevuma norēķinu režģis lapā **Projekts** ietver ikonu, kas norāda, ka ar šo uzdevumu ir saistīts līgums vai piedāvājums.</span><span class="sxs-lookup"><span data-stu-id="c9de1-136">The task-based billing grid on the **Project** page includes an icon indicating that there is a contract or quote line linked to that task.</span></span> |
| <span data-ttu-id="c9de1-137">**Iespēju pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="c9de1-137">**Opportunity Management**</span></span> | <span data-ttu-id="c9de1-138">2029135</span><span class="sxs-lookup"><span data-stu-id="c9de1-138">2029135</span></span> | <span data-ttu-id="c9de1-139">Novērsta biznesa procesa kļūda, kas rodas, ja lietotājs mēģina atvērt rēķina rindu apstiprinātā rēķinā, kurā ir iekļauta avansa summa.</span><span class="sxs-lookup"><span data-stu-id="c9de1-139">Fixed the business process error that occurs when a user tries to open an invoice line on a confirmed invoice that has an advance amount invoiced.</span></span> |
| <span data-ttu-id="c9de1-140">**Iespēju pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="c9de1-140">**Opportunity Management**</span></span> | <span data-ttu-id="c9de1-141">2040713</span><span class="sxs-lookup"><span data-stu-id="c9de1-141">2040713</span></span> | <span data-ttu-id="c9de1-142">Novērsta skripta kļūda, kas rodas, izveidojot rēķinu no līguma un ir instalēts Field Service.</span><span class="sxs-lookup"><span data-stu-id="c9de1-142">Fixed the script error that occurs when creating an invoice from a contract and Field Service is installed.</span></span> |
| <span data-ttu-id="c9de1-143">**Projektu plānošana un izsekošana**</span><span class="sxs-lookup"><span data-stu-id="c9de1-143">**Project Planning and Tracking**</span></span> | <span data-ttu-id="c9de1-144">2090202</span><span class="sxs-lookup"><span data-stu-id="c9de1-144">2090202</span></span> | <span data-ttu-id="c9de1-145">Tās biznesa kārtulas, kuras vairs neizmanto, tiek atzīmētas kā **Novecojušas**.</span><span class="sxs-lookup"><span data-stu-id="c9de1-145">Marked business rules that are no longer used as **Deprecated**.</span></span> |
| <span data-ttu-id="c9de1-146">**Laiks un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-146">**Time and Expense**</span></span> | <span data-ttu-id="c9de1-147">2091249</span><span class="sxs-lookup"><span data-stu-id="c9de1-147">2091249</span></span> | <span data-ttu-id="c9de1-148">Pastiprināta kontrole, lai lietotāji nevar mainīt uzdevumu iesniegtā vai apstiprinātā laika ierakstā.</span><span class="sxs-lookup"><span data-stu-id="c9de1-148">Tightened controls so that users can't change the task on a submitted or approved time entry.</span></span> |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a><span data-ttu-id="c9de1-149">Pārskats par projektu pārvaldību un uzskaiti pakalpojumā Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="c9de1-149">Project management and accounting in Dynamics 365 Finance</span></span>

| <span data-ttu-id="c9de1-150">**Līdzekļu apgabals**</span><span class="sxs-lookup"><span data-stu-id="c9de1-150">**Feature Area**</span></span> | <span data-ttu-id="c9de1-151">**Atsauces numurs**</span><span class="sxs-lookup"><span data-stu-id="c9de1-151">**Reference number**</span></span> | <span data-ttu-id="c9de1-152">**Kvalitātes atjauninājums**</span><span class="sxs-lookup"><span data-stu-id="c9de1-152">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c9de1-153">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-153">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-154">478667</span><span class="sxs-lookup"><span data-stu-id="c9de1-154">478667</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | <span data-ttu-id="c9de1-155">Nepareiza līguma summa lapā **Starpkonts** fiksētas cenas projektam ar vairākiem finansējuma avotiem.</span><span class="sxs-lookup"><span data-stu-id="c9de1-155">Incorrect contract amount on the **On-account** page for a fixed-price project with multiple funding sources.</span></span> |
| <span data-ttu-id="c9de1-156">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-156">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-157">480260</span><span class="sxs-lookup"><span data-stu-id="c9de1-157">480260</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | <span data-ttu-id="c9de1-158">Vietturis **Invoiceproposal.PSAnfRefProjId** nerāda projekta ID darbplūsmai, **Pārskatīt projekta rēķina priekšlikumus**.</span><span class="sxs-lookup"><span data-stu-id="c9de1-158">The **Invoiceproposal.PSAnfRefProjId** placeholder isn't displaying the Project ID for the workflow, **Review project invoice proposals**.</span></span> |
| <span data-ttu-id="c9de1-159">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-159">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-160">481227</span><span class="sxs-lookup"><span data-stu-id="c9de1-160">481227</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | <span data-ttu-id="c9de1-161">Tiek izmantots nepareizs skaidras naudas atlaides datums, izliekot projekta rēķina priekšlikumus.</span><span class="sxs-lookup"><span data-stu-id="c9de1-161">The wrong cash discount date is used when posting project invoice proposals.</span></span> |
| <span data-ttu-id="c9de1-162">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-162">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-163">482558</span><span class="sxs-lookup"><span data-stu-id="c9de1-163">482558</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | <span data-ttu-id="c9de1-164">Piešķiru noņemšana un lasīšana programmā Project Operations dublējas ar Finance projekta prognožu ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="c9de1-164">Removing and reading resource assignments in Project Operations doubles the project forecast entries in Finance.</span></span> |
| <span data-ttu-id="c9de1-165">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-165">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-166">484468</span><span class="sxs-lookup"><span data-stu-id="c9de1-166">484468</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | <span data-ttu-id="c9de1-167">Programmā Project Operations jūs nevarat izveidot projekta aprēķinus pakalpojumā Dataverse, ja projektam nav līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="c9de1-167">In Project Operations, you can't create project estimates in Dataverse without having a contract line on the project.</span></span> |
| <span data-ttu-id="c9de1-168">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-168">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-169">485871</span><span class="sxs-lookup"><span data-stu-id="c9de1-169">485871</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | <span data-ttu-id="c9de1-170">Projekta izdevumu transakcijas finanšu dimensija nav sinhronizēta ar saistīto dokumentu un izdevumu atskaites uzskaites sadali, kad izmaksas tiek izliktas bilancē.</span><span class="sxs-lookup"><span data-stu-id="c9de1-170">The financial dimension on a project expense transaction isn't synchronized with the related voucher and the accounting distribution of the expense report when costs are posted to Balance.</span></span> |
| <span data-ttu-id="c9de1-171">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-171">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-172">488382</span><span class="sxs-lookup"><span data-stu-id="c9de1-172">488382</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | <span data-ttu-id="c9de1-173">**Rēķina statusa** filtrs fiksētas cenas projektu grāmatotajām projekta transakcijām nedarbojas.</span><span class="sxs-lookup"><span data-stu-id="c9de1-173">The **Invoice status** filter for posted project transactions for fixed-price projects doesn't work.</span></span> |
| <span data-ttu-id="c9de1-174">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-174">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-175">491941</span><span class="sxs-lookup"><span data-stu-id="c9de1-175">491941</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | <span data-ttu-id="c9de1-176">Apgriezto aprēķinu korekcijas nedarbojas sadaļā **Periodisks**.</span><span class="sxs-lookup"><span data-stu-id="c9de1-176">Reverse estimate elimination isn't working in the **Periodic** section.</span></span> |
| <span data-ttu-id="c9de1-177">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-177">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-178">509989</span><span class="sxs-lookup"><span data-stu-id="c9de1-178">509989</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | <span data-ttu-id="c9de1-179">Rēķina priekšlikuma rindas Project Operations nevar dzēst, ja integrēts ar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c9de1-179">Invoice proposal lines can be deleted in Project Operations when integrated with Dataverse.</span></span> |
| <span data-ttu-id="c9de1-180">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-180">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-181">510041</span><span class="sxs-lookup"><span data-stu-id="c9de1-181">510041</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | <span data-ttu-id="c9de1-182">Novērsta vairāku līguma rindu funkciju iespējošana bez Dataverse integrācijas.</span><span class="sxs-lookup"><span data-stu-id="c9de1-182">Prevent enabling multiple contract lines feature without Dataverse integration.</span></span> |
| <span data-ttu-id="c9de1-183">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-183">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-184">510527</span><span class="sxs-lookup"><span data-stu-id="c9de1-184">510527</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | <span data-ttu-id="c9de1-185">Ja starpkontu rēķini ir vienādi ar peļņu un zudumu, rēķinā iekļautā peļņa aprēķinu lapā tiek uzskaitīta kā nulle.</span><span class="sxs-lookup"><span data-stu-id="c9de1-185">When on-account invoicing is equal to profit and loss, the invoiced revenue is listed as zero on the Estimates page.</span></span> |
| <span data-ttu-id="c9de1-186">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-186">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-187">514167</span><span class="sxs-lookup"><span data-stu-id="c9de1-187">514167</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | <span data-ttu-id="c9de1-188">Rēķina korekcijas nedarbojas integrētās vidēs.</span><span class="sxs-lookup"><span data-stu-id="c9de1-188">Invoice corrections aren't working in integrated environments.</span></span> |
| <span data-ttu-id="c9de1-189">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-189">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-190">514364</span><span class="sxs-lookup"><span data-stu-id="c9de1-190">514364</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | <span data-ttu-id="c9de1-191">Izliekot NP — pārdošanas vērtību grāmatošanas funkcija, izrakstot starpuzņēmumu projektā rēķinu, atlasa nepareizu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="c9de1-191">When posting WIP - sales value in intercompany project invoicing, the wrong account is selected.</span></span> |
| <span data-ttu-id="c9de1-192">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-192">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-193">514385</span><span class="sxs-lookup"><span data-stu-id="c9de1-193">514385</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | <span data-ttu-id="c9de1-194">Programmā Project Operations atkarības no aprēķinu uzdevumiem programmā Dataverse nevar atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="c9de1-194">In Project Operations, dependencies on estimate tasks in Dataverse can't be updated.</span></span> |
| <span data-ttu-id="c9de1-195">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-195">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-196">515258</span><span class="sxs-lookup"><span data-stu-id="c9de1-196">515258</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | <span data-ttu-id="c9de1-197">Atkārtoti dzēšot Project Operations integrācijas žurnālus programmā Finance, tiek zaudēti dati.</span><span class="sxs-lookup"><span data-stu-id="c9de1-197">Repeatedly deleting Project Operations integration journals in Finance leads to data loss.</span></span> |
| <span data-ttu-id="c9de1-198">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-198">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-199">519716</span><span class="sxs-lookup"><span data-stu-id="c9de1-199">519716</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | <span data-ttu-id="c9de1-200">Izliekot projekta rēķina priekšlikumu, rodas šāda kļūda: "Transakcija nesaskan ar atskaites valūtu, ja tiek pievienots noņemtais avansa rēķins."</span><span class="sxs-lookup"><span data-stu-id="c9de1-200">The following error occurs when posting a project invoice proposal, "Transaction does not balance on reporting currency when advance invoice deducted is added".</span></span> |
| <span data-ttu-id="c9de1-201">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-201">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-202">521807</span><span class="sxs-lookup"><span data-stu-id="c9de1-202">521807</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | <span data-ttu-id="c9de1-203">Ieturējumos tiek iekļauts nepareizs projekta ID pēc tam, kad noklusējuma projekta līgums ir atjaunināts Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c9de1-203">The wrong project ID is included on deductions after the default project contract is updated in Project Operations.</span></span> |
| <span data-ttu-id="c9de1-204">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-204">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-205">522799</span><span class="sxs-lookup"><span data-stu-id="c9de1-205">522799</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | <span data-ttu-id="c9de1-206">Aprēķinu un peļņas atpazīšanu nevar pabeigt, ja ir iespējots Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c9de1-206">Estimate and revenue recognition can't be completed when Project Operations is enabled.</span></span> |
| <span data-ttu-id="c9de1-207">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-207">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-208">527319</span><span class="sxs-lookup"><span data-stu-id="c9de1-208">527319</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | <span data-ttu-id="c9de1-209">Programmā Project Operations, noņemot projektu no līguma, netiek atiestatīts līguma noklusējuma projekts.</span><span class="sxs-lookup"><span data-stu-id="c9de1-209">In Project Operations, removing a project from a contract doesn't reset the default project on the contract.</span></span> |
| <span data-ttu-id="c9de1-210">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="c9de1-210">**Project management and accounting**</span></span> | [<span data-ttu-id="c9de1-211">528212</span><span class="sxs-lookup"><span data-stu-id="c9de1-211">528212</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | <span data-ttu-id="c9de1-212">Programmā Project Operations starpuzņēmumu rēķinā sarakstā **Pievienot rindu** tiek rādītas nepareizās izdevumu rindas.</span><span class="sxs-lookup"><span data-stu-id="c9de1-212">In Project Operations, on an intercompany invoice, the wrong expense lines show up in the **Add line** list.</span></span> |
| <span data-ttu-id="c9de1-213">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-213">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-214">515334</span><span class="sxs-lookup"><span data-stu-id="c9de1-214">515334</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | <span data-ttu-id="c9de1-215">Izmaksu rindas nevar izlikt, jo līguma rindā trūkst stundu iestatījuma.</span><span class="sxs-lookup"><span data-stu-id="c9de1-215">Expense lines can't be posted because hour setup is missing on the contract line.</span></span> |
| <span data-ttu-id="c9de1-216">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-216">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-217">437673</span><span class="sxs-lookup"><span data-stu-id="c9de1-217">437673</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | <span data-ttu-id="c9de1-218">Ja projekta/kategorijas validācija ir obligāta, ar projektu saistītās izdevumu kategorijas nav redzamas izdevumu atskaitē.</span><span class="sxs-lookup"><span data-stu-id="c9de1-218">When project/category validation is mandatory, expense categories associated with the project are not visible in the expense report.</span></span> |
| <span data-ttu-id="c9de1-219">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-219">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-220">441256</span><span class="sxs-lookup"><span data-stu-id="c9de1-220">441256</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | <span data-ttu-id="c9de1-221">Skaidrās naudas avansa bilance netiek atjaunināta, ja izdevumu atskaiti izliek pēc rindas.</span><span class="sxs-lookup"><span data-stu-id="c9de1-221">The cash advance balance isn't updated when an expense report is posted by line.</span></span> |
| <span data-ttu-id="c9de1-222">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-222">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-223">465396</span><span class="sxs-lookup"><span data-stu-id="c9de1-223">465396</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | <span data-ttu-id="c9de1-224">Darbs **Atjaunināt maksājuma informāciju** neizdodas pēc saistīto darbību apgriešanas, kurās rēķinu sedza ar divām vai vairākām maksājumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="c9de1-224">The **Update payment information** job fails after reversing settlements where an invoice was settled with two or more payment transactions.</span></span> |
| <span data-ttu-id="c9de1-225">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-225">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-226">472892</span><span class="sxs-lookup"><span data-stu-id="c9de1-226">472892</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | <span data-ttu-id="c9de1-227">Ir problēma ar pēdējās dienas maltītes samazinājuma aprēķinu katrai dienasnaudas izmaksu kategorijai.</span><span class="sxs-lookup"><span data-stu-id="c9de1-227">There is an issue with the calculation of the last day meal reduction for the per diem expense category.</span></span> |
| <span data-ttu-id="c9de1-228">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-228">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-229">477714</span><span class="sxs-lookup"><span data-stu-id="c9de1-229">477714</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | <span data-ttu-id="c9de1-230">Atskaite **Izmaksu veids katram darbiniekam** nerāda uzskaitītos izdevumus, ja lietotāja pirmais savienojums bija es-MX valodā.</span><span class="sxs-lookup"><span data-stu-id="c9de1-230">The **Expense type per employee** report doesn't show itemized expenses if a user's first connection was in the es-MX language.</span></span> |
| <span data-ttu-id="c9de1-231">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-231">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-232">487516</span><span class="sxs-lookup"><span data-stu-id="c9de1-232">487516</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | <span data-ttu-id="c9de1-233">Pārdevēja maksājums par izdevumu atskaites rēķinu izmanto nepareizu kopsavilkuma kontu seguma izlikšanai.</span><span class="sxs-lookup"><span data-stu-id="c9de1-233">The vendor payment for an expense report invoice is using the wrong summary account for settlement posting.</span></span> |
| <span data-ttu-id="c9de1-234">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-234">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-235">487531</span><span class="sxs-lookup"><span data-stu-id="c9de1-235">487531</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | <span data-ttu-id="c9de1-236">Ja izdevumu atskaiti iegrāmatoto ar iespējotu opciju **Atļauj transakciju grupēšanu, pamatojoties uz nobīdes maksājumu kontu** un **Labojams uzskaites datums grāmatošanas laikā**, redzamie uzskaites datumi nav grupēti tabulā **Uzskaites sadale**, kas ietekmē pārdošanas nodokļu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="c9de1-236">When an expense report is posted with **Allow grouping of transactions based on offset payment account** and **Correcting Accounting Date at posting** enabled, the accounting dates aren't grouped in the **Accounting distribution** table which impacts the sales tax records.</span></span> |
| <span data-ttu-id="c9de1-237">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-237">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-238">488292</span><span class="sxs-lookup"><span data-stu-id="c9de1-238">488292</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | <span data-ttu-id="c9de1-239">Izdevumu apakškategorijas kartēšana tiek noņemta, ja tiek notīrīta un atkal atlasīta izvēles rūtiņa Izmantot izdevumus.</span><span class="sxs-lookup"><span data-stu-id="c9de1-239">Expense subcategory mapping is removed when the Use in expense check box is cleared and then selected again.</span></span> |
| <span data-ttu-id="c9de1-240">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-240">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-241">506175</span><span class="sxs-lookup"><span data-stu-id="c9de1-241">506175</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | <span data-ttu-id="c9de1-242">Nevar izveidot starpuzņēmumu atskaiti, ja projekta ID tiek pievienots virsraksta līmenī.</span><span class="sxs-lookup"><span data-stu-id="c9de1-242">An intercompany expense report can't be created if the Project ID is added at the header level.</span></span> |
| <span data-ttu-id="c9de1-243">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-243">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-244">509491</span><span class="sxs-lookup"><span data-stu-id="c9de1-244">509491</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | <span data-ttu-id="c9de1-245">Rodas problēma ar izdevumu maksājumiem, ja izdevumu summa pārsniedz skaidrās naudas avansa summu.</span><span class="sxs-lookup"><span data-stu-id="c9de1-245">There is an issue with expense payments when the expense amount is more than the cash advance amount.</span></span> |
| <span data-ttu-id="c9de1-246">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-246">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-247">509556</span><span class="sxs-lookup"><span data-stu-id="c9de1-247">509556</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | <span data-ttu-id="c9de1-248">Lauks **Projekta ID** informācija starpuzņēmumu izdevumu atskaitē nav norādīts, ja lietotāja loma ir piešķirta noteiktai organizācijai.</span><span class="sxs-lookup"><span data-stu-id="c9de1-248">The **Project ID** field on an intercompany expense report is empty if the user role is assigned to a specific organization.</span></span> |
| <span data-ttu-id="c9de1-249">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-249">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-250">518186</span><span class="sxs-lookup"><span data-stu-id="c9de1-250">518186</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | <span data-ttu-id="c9de1-251">Izdevumu kategorija ir bloķēta, ja pievieno jaunu izdevumu rindu.</span><span class="sxs-lookup"><span data-stu-id="c9de1-251">The expense category is locked when adding a new expense line.</span></span> |
| <span data-ttu-id="c9de1-252">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-252">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-253">520914</span><span class="sxs-lookup"><span data-stu-id="c9de1-253">520914</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | <span data-ttu-id="c9de1-254">Uzskaitītās izdevumu atskaites rindas, kuras jau ir atdalītas, rada nepilnīgi izlikto debitora/Virsgrāmatas dokumentu.</span><span class="sxs-lookup"><span data-stu-id="c9de1-254">Itemizing expense report lines that are already split results in an incomplete posted Accounts payable\General ledger voucher.</span></span> <span data-ttu-id="c9de1-255">Tā kā **TRVEXPTRANS.SOURCEDOCUMENTLINE** dublējas, tiek pārtraukts arī Uzskaites avota pārlūks.</span><span class="sxs-lookup"><span data-stu-id="c9de1-255">Because of the duplication of **TRVEXPTRANS.SOURCEDOCUMENTLINE**, the Accounting Source Explorer is also broken.</span></span> |
| <span data-ttu-id="c9de1-256">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-256">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-257">521768</span><span class="sxs-lookup"><span data-stu-id="c9de1-257">521768</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | <span data-ttu-id="c9de1-258">Indekss, kas pievienots tabulā **TRVREQUISITIONLINE**, kurai klientam ir dublikāti, atjaunināšanas laikā rada kļūdu.</span><span class="sxs-lookup"><span data-stu-id="c9de1-258">The index added on the **TRVREQUISITIONLINE** table for which the customer has duplicates, results in an error during upgrade.</span></span> |
| <span data-ttu-id="c9de1-259">**Komandējumi un izdevumi**</span><span class="sxs-lookup"><span data-stu-id="c9de1-259">**Travel and Expense**</span></span> | [<span data-ttu-id="c9de1-260">525106</span><span class="sxs-lookup"><span data-stu-id="c9de1-260">525106</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | <span data-ttu-id="c9de1-261">Programmā Project Operations laiku ar starpuzņēmuma uzdevumiem pakalpojumā Dataverse nevar izveidot vai apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="c9de1-261">In Project Operations, time with intercompany tasks in Dataverse can't be created or approved.</span></span> |

## <a name="regulatory-updates"></a><span data-ttu-id="c9de1-262">Reglamentējoši atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="c9de1-262">Regulatory updates</span></span>

<span data-ttu-id="c9de1-263">Informāciju par reglamentējošajiem atjauninājumiem programmās Finance and Operations skatiet sadaļā [Reglamentējošie atjauninājumi](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span><span class="sxs-lookup"><span data-stu-id="c9de1-263">For information about regulatory updates for Finance and Operations apps, see [Regulatory updates](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span></span> <span data-ttu-id="c9de1-264">Varat arī pieteikties LCS un skatīt plānotos reglamentējošos atjauninājumus, izmantojot problēmu meklēšanas rīku.</span><span class="sxs-lookup"><span data-stu-id="c9de1-264">You can also sign in to LCS and view the planned regulatory updates using the Issue search tool.</span></span> <span data-ttu-id="c9de1-265">Problēmu meklēšana ļauj meklēt pēc valsts, līdzekļa tipa un laidiena.</span><span class="sxs-lookup"><span data-stu-id="c9de1-265">Issue search lets you search by country, type of feature, and release.</span></span>