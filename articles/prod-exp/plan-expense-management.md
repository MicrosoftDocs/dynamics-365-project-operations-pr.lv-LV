---
title: Izdevumu pārvaldības konfigurēšana
description: Šajā rakstā ir aprakstīti apsvērumi un lēmumi, kas ir jāpieņem plānošanas procesa laikā pirms izdevumu pārvaldības konfigurēšanas Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080592"
---
# <a name="configure-expense-management"></a><span data-ttu-id="6f1fa-103">Izdevumu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="6f1fa-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f1fa-104">Šajā tēmā ir aprakstīti apsvērumi un lēmumi, kas ir jāpieņem plānošanas procesa laikā pirms izdevumu pārvaldības konfigurēšanas.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="6f1fa-105">Izdevumu pārvaldībā var glabāt informāciju par maksājuma metodēm, ceļa pieprasījumiem, izdevumu atskaitēm, politikām un citu informāciju.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="6f1fa-106">Tā kā daudzi no jūsu pieņemtajiem lēmumiem attiecībā uz izdevumu pārvaldības konfigurācijas plānošanu ir balstīti uz jūsu organizācijas hierarhiju un finanšu struktūru, ir jāatsaucas uz šo apgabalu plānošanas dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="6f1fa-107">Starpuzņēmumu izdevumi</span><span class="sxs-lookup"><span data-stu-id="6f1fa-107">Intercompany expenses</span></span>

<span data-ttu-id="6f1fa-108">Iespējojot starpuzņēmumu izdevumus, juridiskās personas un darbinieki tiek pilnvaroti apmaksāt izdevumus citas juridiskas personas vārdā, kā arī iekasēt samaksu no juridiskās entītijas, kas nodarbināta jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="6f1fa-109">Piemēram, darbinieks juridiskajā entītijā A izpilda projektu juridiskajai personai B, un projektam rodas ar ceļojumiem saistīti izdevumi.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="6f1fa-110">Ja ir iespējotas starpuzņēmumu izmaksas, darbinieks pēc tam var iesniegt izdevumu atskaiti, kurā tiks grāmatoti izdevumi juridiskajai personai B, un juridiskajai personai A ir jāapmaksā izdevumi. Ja organizācijā nav vairāku juridisku entītiju, starpuzņēmumu izdevumi nav jāiespējo.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="6f1fa-111">**Lēmums:**  vai vēlaties iespējot starpuzņēmumu izdevumus?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="6f1fa-112">Finanšu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="6f1fa-112">Financial management</span></span>

<span data-ttu-id="6f1fa-113">Izdevumu pārvaldība ir cieši integrēta organizācijas finanšu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="6f1fa-114">Daudz jūsu izdevumu pārvaldības konfigurēšanas pamatā būs lēmumi, ko esat pieņēmis saistībā ar jūsu organizācijas finansēm.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="6f1fa-115">Tālāk esošajās sadaļās ir aprakstīti dažādi apgabali, kuros ir nepieciešama plānošana un lēmumi, pamatojoties uz jūsu organizācijas finanšu lēmumiem un vadlīnijām no jūsu vadības darba grupas.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="6f1fa-116">Dienasnauda</span><span class="sxs-lookup"><span data-stu-id="6f1fa-116">Per diems</span></span>

<span data-ttu-id="6f1fa-117">Jums ir jādefinē darbinieku dienasnauda, ko nodrošina jūsu organizācija.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="6f1fa-118">Tā kā dienasnauda parasti tiek izmantota, lai segtu izdevumus, piemēram, ēdināšanu, naktsmītnes un citus papildu izdevumus, varat izveidot kārtulas jūsu organizācijas piedāvātajām dienasnaudas summām.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="6f1fa-119">Dienasnaudas likmes var būt atkarīgas no gada laika, ceļojuma galamērķa vai abiem.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="6f1fa-120">Kad definējat dienasnaudas kārtulu, varat norādīt, ka noteikta procentuālā dienasnaudas likme tiek ieturēta, ja darbinieks saņem bezmaksas maltītes vai pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="6f1fa-121">Varat definēt arī dienasnaudas likmju līmeņus, lai iestatītu minimālo un maksimālo stundu skaitu, kam var piemērot darba ņēmēja komandējuma dienasnaudas likmi.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="6f1fa-122">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="6f1fa-122">**Decisions:**</span></span>

- <span data-ttu-id="6f1fa-123">Dienasnaudas noklusējuma kārtulas pirmajai un pēdējai dienai:</span><span class="sxs-lookup"><span data-stu-id="6f1fa-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="6f1fa-124">Kāds ir minimālais stundu skaits, ko darbinieks var pieprasīt par dienu un joprojām saņemt dienasnaudu?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="6f1fa-125">Vai ir samazināta summa, kas tiek piedāvāta par ēdienu pirmajai un pēdējai dienai?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="6f1fa-126">Ja ir samazinājums, kāda ir samazinājuma procentuālā daļa?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="6f1fa-127">Vai ir samazināta summa, kas tiek piedāvāta par viesnīcu pirmajai un pēdējai dienai?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="6f1fa-128">Ja ir samazinājums, kāda ir samazinājuma procentuālā daļa?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="6f1fa-129">Vai ir samazināta summa, kas tiek piedāvāta par citiem izdevumiem pirmajā un pēdējā dienā?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="6f1fa-130">Ja ir samazinājums, kāda ir samazinājuma procentuālā daļa?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="6f1fa-131">Dienasnaudas noklusējuma kārtulas:</span><span class="sxs-lookup"><span data-stu-id="6f1fa-131">Default per diem rules:</span></span>

    - <span data-ttu-id="6f1fa-132">Vai dienasnauda tiek procentuāli samazināta par katru maltīti, ja, piemēram, maltīte ir bez maksas?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="6f1fa-133">Ja ir samazinājums, kāda ir samazinājuma procentuālā daļa par katru maltīti?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="6f1fa-134">Vai maltītes samazinājums ir aprēķināts dienā, ceļojumā vai pēc ēdienreižu skaita dienā?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="6f1fa-135">Vai dienasnaudas summas ir jānoapaļo parastā veidā vai jānoapaļo uz augšu?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="6f1fa-136">Vai dienasnauda tiek aprēķināta 24 stundu periodā vai kalendārajā dienā?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="6f1fa-137">Dienasnaudas kārtulas, kuru pamatā ir atrašanās vieta:</span><span class="sxs-lookup"><span data-stu-id="6f1fa-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="6f1fa-138">Vai dienas naudas likmes mainās atkarībā no atrašanās vietas?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="6f1fa-139">Kādas atrašanās vietas ir iekļautas?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-139">What locations are included?</span></span>
    - <span data-ttu-id="6f1fa-140">Ja dienasnaudas likmes ir atkarīgas no atrašanās vietas, kāda procentuālā summa katrai atrašanās vietai tiek nodrošināta tālāk minētajiem izdevumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="6f1fa-141">Maltītes</span><span class="sxs-lookup"><span data-stu-id="6f1fa-141">Meals</span></span>
        - <span data-ttu-id="6f1fa-142">Viesnīca</span><span class="sxs-lookup"><span data-stu-id="6f1fa-142">Hotel</span></span>
        - <span data-ttu-id="6f1fa-143">Citi izdevumi</span><span class="sxs-lookup"><span data-stu-id="6f1fa-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="6f1fa-144">Izdevumu pārvaldības žurnāli un konti</span><span class="sxs-lookup"><span data-stu-id="6f1fa-144">Expense management journals and accounts</span></span>

<span data-ttu-id="6f1fa-145">Izmaksu pārvaldībai ir nepieciešams lietot vairākus žurnālus un kontus.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="6f1fa-146">Jums ir jāizlemj, piemēram, vai tas naudas avansiem un kredītkaršu strīdiem tiek izmantots viens konts.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="6f1fa-147">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="6f1fa-147">**Decisions:**</span></span>

- <span data-ttu-id="6f1fa-148">Kurā virsgrāmatas žurnālā tiek grāmatotas apstiprinātās izdevumu atskaites?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="6f1fa-149">Kurš konts tiek izmantots naudas avansiem?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="6f1fa-150">Vai naudas avansi ir jāgrāmato nekavējoties?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="6f1fa-151">Maksāšanas metodes</span><span class="sxs-lookup"><span data-stu-id="6f1fa-151">Payment methods</span></span>

<span data-ttu-id="6f1fa-152">Ja ļaujat darbiniekiem jūsu uzņēmuma vārdā apmaksāt izdevumus, jums ir jādefinē maksājuma metodes, kuras darbiniekiem ir atļauts lietot.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="6f1fa-153">Piemēram, varat atļaut darbiniekiem izmantot skaidru naudu vai uzņēmuma kredītkarti.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="6f1fa-154">Varat arī atļaut darbiniekiem izmantot personiskās kredītkartes un pēc tam atlīdzināt izdevumus darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="6f1fa-155">Ir jāpieņem šādi lēmumi attiecībā uz katru atļauto maksāšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="6f1fa-156">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="6f1fa-156">**Decisions:**</span></span>

- <span data-ttu-id="6f1fa-157">Kādas maksāšanas metodes ir atļautas?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="6f1fa-158">Kam pieder maksājuma metodes izdevumi?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="6f1fa-159">Vai ir nobīdes konta tips?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-159">Is there an offset account type?</span></span> <span data-ttu-id="6f1fa-160">Ja ir nobīdes konta tips, kas tas ir?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="6f1fa-161">Ja ir nobīdes konta tips, kāds ir konts?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="6f1fa-162">Ja maksāšanas metode ir kredītkarte, vai maksāšanas metode ir jāizmanto tikai ar importētajiem darījumiem?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="6f1fa-163">Izdevumu kategorijas un koplietotās kategorijas</span><span class="sxs-lookup"><span data-stu-id="6f1fa-163">Expense categories and shared categories</span></span>

<span data-ttu-id="6f1fa-164">Kad darbinieki veido izdevumu atskaiti, katram reģistrētajam izdevumu ierakstam ir jābūt saistītam ar izdevumu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="6f1fa-165">Izdevumu kategorijas ir atvasinātas no kopīgotām kategorijām, kuras var kopīgot organizācijas juridiskajās personās.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="6f1fa-166">Šīs kategorijas var arī kopīgot projektu vadībā un grāmatvedībā atkarībā no organizācijas definēšanas veida.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="6f1fa-167">Pamatojoties uz jūsu organizācijas definīciju un ieviešanas darba grupas vadlīnijām, ir jānosaka, vai modulī Izdevumu pārvaldība lietotās kategorijas tiks izmantotas tikai modulī Izmaksu pārvaldība vai arī tās būtu nepieciešams kopīgot moduļos Projektu vadība un grāmatvedība un Izdevumu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="6f1fa-168">Ņemiet vērā, ka šīs kategorijas var koplietot projektā un izdevumos vai projektā un ražošanā, bet ne izdevumos un ražošanā.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="6f1fa-169">Attiecībā uz katru izdevumu kategoriju ir jāpieņem tālāk minētie lēmumi.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="6f1fa-170">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="6f1fa-170">**Decisions:**</span></span>

- <span data-ttu-id="6f1fa-171">Kas ir izdevumu kategorija?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-171">What is the expense category?</span></span> <span data-ttu-id="6f1fa-172">Var būt tādas kategorijas kā lidojumi, viesnīca vai nobraukums.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="6f1fa-173">Vai izdevumu kategoriju var izmantot arī projektu pārvaldībā un grāmatvedībā?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="6f1fa-174">Kāds ir izdevumu tips?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-174">What is the expense type?</span></span>
- <span data-ttu-id="6f1fa-175">Kāda ir izdevumu kategorijas noklusējuma maksāšanas metode?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="6f1fa-176">Vai izdevumu kategorijas izdevumi ir jāuzskaita?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="6f1fa-177">Kas ir izdevumu kategorijas galvenais noklusējuma konts?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="6f1fa-178">Kas ir izdevumu kategorijas noklusējuma krājumu PVN grupa?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="6f1fa-179">Vai izdevumu kategorijai ir atļautas papildu maksāšanas metodes?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="6f1fa-180">Ja ir atļautas papildu maksāšanas metodes, kādas tās ir?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="6f1fa-181">Vai šajā izdevumu kategorijā ir apakškategorijas?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="6f1fa-182">Ja ir apakškategorijas, jums ir jāpieņem arī šādi lēmumi:</span><span class="sxs-lookup"><span data-stu-id="6f1fa-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="6f1fa-183">Vai jebkura no apakškategorijām ir izslēgta no nodokļu atmaksas?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="6f1fa-184">Kas ir apakškategoriju krājumu PVN grupa?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="6f1fa-185">Ja izdevumu kategorija tiek izmantota arī projektu vadībā un grāmatvedībā, atbildiet uz atlikušajiem jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="6f1fa-186">Pretējā gadījumā pārejiet uz nākamo sadaļu.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="6f1fa-187">Kuri izmaksu konti tiks izmantoti tālāk norādītajiem izdevumiem?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="6f1fa-188">izdevumi</span><span class="sxs-lookup"><span data-stu-id="6f1fa-188">Cost</span></span>
    - <span data-ttu-id="6f1fa-189">Algu sadalījums</span><span class="sxs-lookup"><span data-stu-id="6f1fa-189">Payroll allocation</span></span>
    - <span data-ttu-id="6f1fa-190">WIP-izmaksu vērtība</span><span class="sxs-lookup"><span data-stu-id="6f1fa-190">WIP-cost value</span></span>
    - <span data-ttu-id="6f1fa-191">Izmaksas-elements</span><span class="sxs-lookup"><span data-stu-id="6f1fa-191">Cost-item</span></span>
    - <span data-ttu-id="6f1fa-192">WIP-izmaksu vērtība-elements</span><span class="sxs-lookup"><span data-stu-id="6f1fa-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="6f1fa-193">Uzkrātie zaudējumi</span><span class="sxs-lookup"><span data-stu-id="6f1fa-193">Accrued loss</span></span>
    - <span data-ttu-id="6f1fa-194">WIP-uzkrātie zaudējumi</span><span class="sxs-lookup"><span data-stu-id="6f1fa-194">WIP-accrued loss</span></span>

- <span data-ttu-id="6f1fa-195">Kuri ieņēmumu konti tiks izmantoti tālāk norādītajiem vienumiem?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="6f1fa-196">Ieņēmumi, par ko izrakstīts rēķins</span><span class="sxs-lookup"><span data-stu-id="6f1fa-196">Invoiced revenue</span></span>
    - <span data-ttu-id="6f1fa-197">Uzkrāto ieņēmumu-pārdošanas vērtība</span><span class="sxs-lookup"><span data-stu-id="6f1fa-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="6f1fa-198">WIP-pārdošanas vērtība</span><span class="sxs-lookup"><span data-stu-id="6f1fa-198">WIP-sales value</span></span>
    - <span data-ttu-id="6f1fa-199">Uzkrātie ieņēmumi-ražošana</span><span class="sxs-lookup"><span data-stu-id="6f1fa-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="6f1fa-200">WIP-ražošana</span><span class="sxs-lookup"><span data-stu-id="6f1fa-200">WIP-production</span></span>
    - <span data-ttu-id="6f1fa-201">Uzkrātie ieņēmumi-peļņa</span><span class="sxs-lookup"><span data-stu-id="6f1fa-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="6f1fa-202">WIP-peļņa</span><span class="sxs-lookup"><span data-stu-id="6f1fa-202">WIP-profit</span></span>
    - <span data-ttu-id="6f1fa-203">Uzkrātie ieņēmumi-abonēšana</span><span class="sxs-lookup"><span data-stu-id="6f1fa-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="6f1fa-204">WIP-abonēšana</span><span class="sxs-lookup"><span data-stu-id="6f1fa-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="6f1fa-205">Nodokļi</span><span class="sxs-lookup"><span data-stu-id="6f1fa-205">Taxes</span></span>

<span data-ttu-id="6f1fa-206">Ar izdevumiem saistītos nodokļus ir jānosaka, kas ir iekļauts vai iespējots izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="6f1fa-207">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="6f1fa-207">**Decisions:**</span></span>

- <span data-ttu-id="6f1fa-208">Vai pārdošanas nodoklis ir iekļauts izdevumu summās?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="6f1fa-209">Vai nodokļu atgūšana ir iespējota izdevumiem?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f1fa-210">Ja plānojat virsgrāmatu un esat nolēmis lietot ASV pārdošanas nodokli un izmantot nodokļu kārtulas, nevarat iespējot nodokļu atmaksāšanu izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="6f1fa-211">(Lai lietotu ASV pārdošanas nodokli un izmantotu nodokļu kārtulas, opciju **Lietot pārdošanas nodokļu kārtulu** iestatiet uz **Jā**.)</span><span class="sxs-lookup"><span data-stu-id="6f1fa-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="6f1fa-212">Politikas</span><span class="sxs-lookup"><span data-stu-id="6f1fa-212">Policies</span></span>

<span data-ttu-id="6f1fa-213">Izveidojot izdevumu atskaišu politikas, varat palīdzēt organizācijai ietaupīt laiku un naudu, kad darbinieki apmaksā izdevumus organizācijas vārdā.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="6f1fa-214">Politikas palīdz nodrošināt, ka darbinieki ievēro budžetu, sniedz visu nepieciešamo informāciju un tērē naudu tikai tad, kad nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="6f1fa-215">Ir jāpieņem tālāk norādītie lēmumi attiecībā uz katru izdevumu atskaites politiku un katru izveidoto izmaksu atskaišu apstiprināšanas politiku.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="6f1fa-216">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="6f1fa-216">**Decisions:**</span></span>

- <span data-ttu-id="6f1fa-217">Kāds ir politikas nosaukums?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-217">What is the name of the policy?</span></span>
- <span data-ttu-id="6f1fa-218">Kam ir paredzēta izdevumu politika?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-218">What is the expense policy for?</span></span>
- <span data-ttu-id="6f1fa-219">Ja iepriekš esat nolēmis iespējot starpuzņēmumu izdevumus, uz kādiem uzņēmumiem jūsu organizācijā attieksies šī politika?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="6f1fa-220">Kad politika stājas spēkā?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-220">When does the policy become effective?</span></span>
- <span data-ttu-id="6f1fa-221">Kad beidzas politikas termiņš?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-221">When does the policy expire?</span></span>
- <span data-ttu-id="6f1fa-222">Kāda ir politikas kārtula?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-222">What is the policy rule?</span></span>
- <span data-ttu-id="6f1fa-223">Kāds ir politikas kārtulas rezultāts?</span><span class="sxs-lookup"><span data-stu-id="6f1fa-223">What is the outcome of the policy rule?</span></span>
