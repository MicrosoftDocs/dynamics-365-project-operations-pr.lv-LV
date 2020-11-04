---
title: Spraudņu atribūtu atjaunināšana, lai iekļautu jaunas cenu noteikšanas dimensijas
description: Šajā tēmā ir sniegta informācija par to, kā atjaunināt spraudņu atribūtus cenu noteikšanas dimensijām.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: dynamics-365-customerservice
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f215555dd7b29444e00499c0e731624e51057250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080527"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="0116a-103">Spraudņu atribūtu atjaunināšana, lai iekļautu jaunas cenu noteikšanas dimensijas</span><span class="sxs-lookup"><span data-stu-id="0116a-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="0116a-104">Ja neizmantojat Project Service Automation (PSA) piedāvājuma un līguma funkcijas, varat izlaist šo tēmu.</span><span class="sxs-lookup"><span data-stu-id="0116a-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="0116a-105">Šajā tēmā tiek pieņemts, ka esat pabeidzis tēmā norādītās procedūras: [Pielāgotu lauku un entītiju izveide](create-custom-fields-entities.md), [Pielāgotu lauku pievienošana cenas iestatīšanas un transakciju entītijām](field-references.md) un [Pielāgotu lauku iestatīšana kā cenu noteikšanas dimensijas](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="0116a-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="0116a-106">Ja šīs procedūras neesat pabeidzis, atgriezieties un pabeidziet tās, un pēc tam atgriezieties pie šīs tēmas.</span><span class="sxs-lookup"><span data-stu-id="0116a-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="0116a-107">Kad piedāvājuma rindas papildinformācija tiek izveidota **Piedāvājuma rindas** lapā projekta piedāvājuma rindai, sistēma fonā izveido divas aprēķinu rindas — vienu rindu izmaksu aprēķiniem pusei un vienu pārdošanas aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="0116a-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="0116a-108">Tas pats attiecas uz projekta līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="0116a-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="0116a-109">Kad veicat izmaiņas daudzumā vai laukā izmaksu pusē, šīs izmaiņas tiek ieviestas pārdošanas pusē.</span><span class="sxs-lookup"><span data-stu-id="0116a-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="0116a-110">Tas ir iespējams tālāk minēto spraudņu dēļ, kas ir atkārtoti jāreģistrē pēc izmaiņām cenu noteikšanas dimensijās.</span><span class="sxs-lookup"><span data-stu-id="0116a-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="0116a-111">PreOperationContractLineDetailUpdate - Atjauninājumi **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="0116a-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="0116a-112">PreOperationContractLineDetailUpdate - Atjauninājumi **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="0116a-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="0116a-113">Tālāk aprakstītās darbības izskaidro spraudņu reģistrēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="0116a-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="0116a-114">Atveriet **PluginRegistrationTool** un izveidojiet savienojumu ar tiešsaistes instanci.</span><span class="sxs-lookup"><span data-stu-id="0116a-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="0116a-115">Noklikšķiniet uz **Meklēšana** un meklējiet spraudni atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="0116a-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Meklēšanas koka ekrānuzņēmums](media/PRT-1.png)

3. <span data-ttu-id="0116a-117">Kad spraudnis ir atrasts, atlasiet to un pēc tam noklikšķiniet uz **Atlasīt galvenajā veidlapā**.</span><span class="sxs-lookup"><span data-stu-id="0116a-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="0116a-118">Atlasiet atjaunināmā spraudņa darbību, noklikšķiniet ar peles labo pogu un pēc tam atlasiet **Atjaunināt**.</span><span class="sxs-lookup"><span data-stu-id="0116a-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Tiek atjaunināts spraudņa ekrānuzņēmums](media/PRT-2.png)
 
5. <span data-ttu-id="0116a-120">Atjaunināšanas logā noklikšķiniet uz daudzpunktes ( **...** ) filtrēšanas atribūtos.</span><span class="sxs-lookup"><span data-stu-id="0116a-120">In the update window, click the ellipsis ( **...** ) in the filtering attributes.</span></span>

 ![Esošās darbības konfigurācijas informācijas atjauninājuma ekrānuzņēmums](media/PRT-3.png)
 
6. <span data-ttu-id="0116a-122">Atzīmējiet cenu noteikšanas atribūtu izvēles rūtiņas.</span><span class="sxs-lookup"><span data-stu-id="0116a-122">Select the pricing attribute check boxes.</span></span>

 ![Ekrānuzņēmums, kas parāda izvēles rūtiņu atlasi cenu noteikšanas atribūtiem](media/PRT-4.png)

7. <span data-ttu-id="0116a-124">Noklikšķiniet uz **Labi** , lai aizvērtu lapu, un pēc tam atlasiet **Atjaunināšanas darbība**.</span><span class="sxs-lookup"><span data-stu-id="0116a-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Ekrānuzņēmums, kurā redzama poga “Atjaunināšanas darbība”](media/PRT-5.png)
 
8. <span data-ttu-id="0116a-126">Atkārtojiet šo procesu otrajam spraudnim, **PreOperationQuoteLineDetail msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="0116a-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="0116a-127">Aizveriet spraudņa reģistrācijas rīku.</span><span class="sxs-lookup"><span data-stu-id="0116a-127">Close the plug-in registration tool.</span></span>

