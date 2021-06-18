---
title: Kā pielāgot projekta posmu biznesa procesa plūsmu?
description: Pārskats par to, kā pielāgot projekta posmu biznesa procesa plūsmu.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 2e6c60fe67aea908013077bde40c2faeabc2f39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993155"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="8cc93-103">Kā pielāgot projekta posmu biznesa procesa plūsmu?</span><span class="sxs-lookup"><span data-stu-id="8cc93-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="8cc93-104">Ir zināms ierobežojums iepriekšējās Project Service versijās — posmu nosaukumiem projekta posmu biznesa procesa plūsmā ir precīzi jāatbilst paredzētajiem nosaukumiem angļu valodā (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="8cc93-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="8cc93-105">Pretējā gadījumā biznesa loģika, kuras pamatā ir posmu nosaukumi angļu valodā, nedarbojas, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="8cc93-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="8cc93-106">Tāpēc projekta formā jūs neredzat pazīstamas darbības kā **Pārslēgt procesu** vai **Rediģēt procesu**, kā arī nav ieteicams pielāgot biznesa procesa plūsmu.</span><span class="sxs-lookup"><span data-stu-id="8cc93-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="8cc93-107">Šis ierobežojums ir novērsts versijā 2.4.5.48 un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="8cc93-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="8cc93-108">Šajā raksta tiek sniegti ieteicamie risinājumi, ja jums ir nepieciešams pielāgot noklusējuma biznesa procesa plūsmu agrākām versijām.</span><span class="sxs-lookup"><span data-stu-id="8cc93-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="8cc93-109">Biznesa loģikai ir nepieciešama precīza atbilstība ar posmu nosaukumiem angļu valodā</span><span class="sxs-lookup"><span data-stu-id="8cc93-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="8cc93-110">Projekta posmu biznesa procesa plūsma ietver biznesa loģiku, kas programmā vada šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="8cc93-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="8cc93-111">Ja projekts ir saistīts ar piedāvājumu, kods iestata biznesa procesa plūsmu posmā **Quote** (Piedāvajums).</span><span class="sxs-lookup"><span data-stu-id="8cc93-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="8cc93-112">Ja projekts ir saistīts ar līgumu, kods iestata biznesa procesa plūsmu posmā **Plan** (Plāns).</span><span class="sxs-lookup"><span data-stu-id="8cc93-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="8cc93-113">Kad biznesa procesa plūsma tiek iestatīta posmā **Close** (Aizvērt), projekta ieraksts ir deaktivizēts.</span><span class="sxs-lookup"><span data-stu-id="8cc93-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="8cc93-114">Kad projekts tiek deaktivizēts, projekta veidlapa un darba sadalījuma struktūra (WBS) tiek iestatītas kā tikai lasāmas, tiek izlaistas nosaukto resursu rezervācijas un deaktivizēti visi saistītie cenrāži.</span><span class="sxs-lookup"><span data-stu-id="8cc93-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="8cc93-115">Šī biznesa loģika ir balstīta uz projekta posmu nosaukumiem angļu valodā.</span><span class="sxs-lookup"><span data-stu-id="8cc93-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="8cc93-116">Šī atkarība no posma nosaukumiem angļu valodā ir galvenais iemesls, kāpēc nav ieteicams pielāgot projekta posmu biznesa procesa plūsmu, kā arī kāpēc projekta entītijā neredzat bieži izmantotās biznesa procesa plūsmas darbības, piemēram, **Pārslēgt procesu** vai **Rediģēt procesu**.</span><span class="sxs-lookup"><span data-stu-id="8cc93-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="8cc93-117">Kas notiek, ja posmu nosaukumi neatbilst nosaukumiem angļu valodā?</span><span class="sxs-lookup"><span data-stu-id="8cc93-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="8cc93-118">Ja Project Service versijā 1.x platformā 8.2 posmu nosaukumi biznesa procesa plūsmā precīzi neatbilst posmu nosaukumiem angļu valodā, biznesa loģika, kas iestata pareizo posmu piedāvājumiem vai līgumiem vai aizver projektu, tiek izlaista.</span><span class="sxs-lookup"><span data-stu-id="8cc93-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="8cc93-119">Netiek parādīti kļūdu ziņojumi.</span><span class="sxs-lookup"><span data-stu-id="8cc93-119">No error messages are displayed.</span></span> <span data-ttu-id="8cc93-120">Tāpēc šķiet, ka varat pielāgot projekta posmus biznesa procesa plūsmā.</span><span class="sxs-lookup"><span data-stu-id="8cc93-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="8cc93-121">Tomēr nedarbosies automātiskie procesi piedāvājumiem, līgumiem un projektu aizvēršanai.</span><span class="sxs-lookup"><span data-stu-id="8cc93-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="8cc93-122">Project Service versijā 2.4.4.30 vai vecākā versijā platformā 9.0 bija nozīmīgas arhitektūras izmaiņas biznesa procesa plūsmās, kuru dēļ bija jāpārraksta biznesa procesa plūsmas biznesa loģika.</span><span class="sxs-lookup"><span data-stu-id="8cc93-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="8cc93-123">Ja procesa posmu nosaukumi neatbilst paredzētajiem nosaukumiem angļu valodā, šī iemesla dēļ netiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="8cc93-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="8cc93-124">Ja vēlaties pielāgot projekta posmus projekta entītijai biznesa procesa plūsmā, varat tikai pievienot jaunus posmus projekta entītijas noklusējuma biznesa procesa plūsmā, saglabājot posmus **Piedāvājums**, **Plāns** un **Aizvēršana** tādus, kādi tie ir.</span><span class="sxs-lookup"><span data-stu-id="8cc93-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="8cc93-125">Šis ierobežojums nodrošina, ka netiek rādītas kļūdas no biznesa loģikas, kas biznesa procesa plūsmā sagaida posmu nosaukumus angļu valodā.</span><span class="sxs-lookup"><span data-stu-id="8cc93-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="8cc93-126">Versijā 2.4.5.48 un jaunākās versijās biznesa loģika, kas ir aprakstīta šajā rakstā, ir noņemta no projekta entītijas noklusējuma biznesa procesa plūsmas.</span><span class="sxs-lookup"><span data-stu-id="8cc93-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="8cc93-127">Jauninot uz šo versiju vai jaunāku versiju, varēsiet pielāgot vai aizstāt noklusējuma biznesa procesa plūsmu ar savu.</span><span class="sxs-lookup"><span data-stu-id="8cc93-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="8cc93-128">Risinājumi iepriekšējām versijām</span><span class="sxs-lookup"><span data-stu-id="8cc93-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="8cc93-129">Ja nevarat veikt jaunināšanu, varat pielāgot projekta posmu biznesa procesa plūsmu projekta entītijai vienā no diviem tālāk minētajiem veidiem.</span><span class="sxs-lookup"><span data-stu-id="8cc93-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="8cc93-130">Pievienojiet papildu posmus noklusējuma konfigurācijā, saglabājot **Piedāvājums**, **Plāns** un **Aizvēršana** posmu nosaukumus angļu valodā.</span><span class="sxs-lookup"><span data-stu-id="8cc93-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Posmu pievienošanas noklusējuma konfigurācijai ekrānuzņēmums](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="8cc93-132">Izveidojiet savu biznesa procesa plūsmu un iestatiet to kā galveno biznesa procesa plūsmu projekta entītijai, kas ļauj izmantot jebkādus posma vārdus.</span><span class="sxs-lookup"><span data-stu-id="8cc93-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="8cc93-133">Tomēr, ja vēlaties izmantot tādus pašus standarta projekta posmus **Piedāvājums**, **Plāns** un **Aizvēršana**, ir jāveic daži pielāgojumi, kuru pamatā ir pielāgotie posmu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="8cc93-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="8cc93-134">Sarežģītāka loģika ir projekta aizvēršana, ko joprojām varat aktivizēt, deaktivizējot projekta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8cc93-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF pielāgošana](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="8cc93-136">Papildu apsvērumi Project Service versijai 2.4.4.30 vai vecākai versijai platformā 9.0</span><span class="sxs-lookup"><span data-stu-id="8cc93-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="8cc93-137">Programmā Project Service 2.4.4.30 vai vecākā versijā platformā 9.0 ar pielāgotu biznesa procesa plūsmu projekta entītijas lauku **Posma nosaukums** izmantojot diagrammā **Projekts pēc posma**, projektu saraksta skati netiek atjaunināti, tas notiek tāpēc, ka tas ir saistīts ar noklusējuma projektu posmu biznesa procesa plūsmu.</span><span class="sxs-lookup"><span data-stu-id="8cc93-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="8cc93-138">Šo problēmu varat novērst, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8cc93-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="8cc93-139">Pievienojiet pielāgotu lauku, lai tvertu pašreizējo biznesa procesa plūsmas posmu, kas tiek atjaunināts, kad lietotājs no viena pielāgotas biznesa procesa plūsmas posma pāriet uz citu.</span><span class="sxs-lookup"><span data-stu-id="8cc93-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="8cc93-140">Mainiet diagrammu **Projekts pēc posma** tā, lai tā darbotos ar jūsu pielāgoto lauku, nevis noklusējuma konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="8cc93-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="8cc93-141">Darbības, lai projekta entītijai izveidotu savu biznesa procesa plūsmu</span><span class="sxs-lookup"><span data-stu-id="8cc93-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="8cc93-142">Lai projekta entītijai izveidotu savu biznesa procesa plūsmu, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="8cc93-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="8cc93-143">Pārejiet uz **Iestatījumi** > **Procesu centrs**.</span><span class="sxs-lookup"><span data-stu-id="8cc93-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="8cc93-144">Nekopējiet projekta posmu biznesa procesa plūsmu, jo tādējādi tiek kopēta arī Project Service biznesa loģika.</span><span class="sxs-lookup"><span data-stu-id="8cc93-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Procesa izveide](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="8cc93-146">Izmantojiet procesu noformētāju, lai izveidotu vēlamos posmu nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="8cc93-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="8cc93-147">Ja vēlaties tādu pašu funkcionalitāti kā **Piedāvājums**, **Plāns** un **Aizvēršana** noklusējuma posmiem, jums būs tā jāizveido, pamatojoties uz pielāgotās biznesa procesa plūsmas posmu nosaukumiem.</span><span class="sxs-lookup"><span data-stu-id="8cc93-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Ekrānuzņēmums ar procesu noformētāju, kas izmantots BPF pielāgošanai](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="8cc93-149">Procesu noformētājā noklikšķiniet uz **Pasūtījumu procesa plūsma**, lai pielāgotu biznesa procesa plūsmu iestatītu kā galveno biznesa procesa plūsmu projekta entītijai, pārvietojot to virs projekta posmu biznesa procesa plūsmas saraksta sākumā.</span><span class="sxs-lookup"><span data-stu-id="8cc93-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="8cc93-150">Pasūtījumu procesa plūsmas izveides ekrānuzņēmums</span><span class="sxs-lookup"><span data-stu-id="8cc93-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="8cc93-151">Tālāk minētās darbības attiecas uz Project Service 2.4.4.30 vai vecākām versijām platformā 9.0</span><span class="sxs-lookup"><span data-stu-id="8cc93-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="8cc93-152">Pievienojiet jaunu pielāgotu lauku projekta entītijai, lai iestatītu pielāgotus posmus pielāgotajā biznesa procesa plūsmā.</span><span class="sxs-lookup"><span data-stu-id="8cc93-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="8cc93-153">Lai atjauninātu šo lauku, kad tiks atjaunināts pielāgotas biznesa procesa plūsmas posms, būs jāpievieno biznesa loģika (posms/darbplūsma).</span><span class="sxs-lookup"><span data-stu-id="8cc93-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Projekta entītijas pielāgošanas ekrānuzņēmums](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="8cc93-155">Mainiet diagrammu **Projekts pēc posma**, lai posmiem lietotu jūsu jauno pielāgoto lauku.</span><span class="sxs-lookup"><span data-stu-id="8cc93-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Diagrammas Projekts pēc posma izmantošanas ekrānuzņēmums](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="8cc93-157">Mainiet jebkurus projekta entītijas laukus, lai posmiem ietvertu jauno pielāgoto lauku.</span><span class="sxs-lookup"><span data-stu-id="8cc93-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Projekta entītijas skatu maiņas ekrānuzņēmums](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]