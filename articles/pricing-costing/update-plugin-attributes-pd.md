---
title: Spraudņu atribūtu atjaunināšana ar jaunām cenu noteikšanas dimensijām
description: Šajā tēmā ir sniegta informācija par to, kā atjaunināt spraudņu atribūtus cenu noteikšanas dimensijām.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274692"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="91dd8-103">Spraudņu atribūtu atjaunināšana ar jaunām cenu noteikšanas dimensijām</span><span class="sxs-lookup"><span data-stu-id="91dd8-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="91dd8-104">Šajā tēmā ir sniegta informācija par to, kā atjaunināt spraudņu atribūtus cenu noteikšanas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="91dd8-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="91dd8-105">Šī tēma attiecas tikai uz piedāvājumu un līgumu līdzekļiem risinājumā Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="91dd8-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="91dd8-106">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="91dd8-106">Prerequisites</span></span>
<span data-ttu-id="91dd8-107">Lai izpildītu šajā tēmā aprakstītās darbības, ir jāizpilda tālāk uzskaitītajās tēmās norādītās procedūras.</span><span class="sxs-lookup"><span data-stu-id="91dd8-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="91dd8-108">Pielāgotu lauku un entītiju izveide</span><span class="sxs-lookup"><span data-stu-id="91dd8-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="91dd8-109">Pielāgotu lauku pievienošana cenu iestatījumiem un transakciju entītijām </span><span class="sxs-lookup"><span data-stu-id="91dd8-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="91dd8-110">[Pielāgotu lauku kā cenu kategoriju iestatīšana](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="91dd8-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="91dd8-111">Ja šīs procedūras neesat pabeidzis, pabeidziet tās un pēc tam atgriezieties pie šīs tēmas.</span><span class="sxs-lookup"><span data-stu-id="91dd8-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="91dd8-112">Spraudņa reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="91dd8-112">Register a plug-in</span></span>
<span data-ttu-id="91dd8-113">Ja projekta piedāvājuma rindai tiek izveidota piedāvājuma rindas detaļa lapā **Piedāvājuma rinda**, sistēma izveido divas novērtējuma rindas.</span><span class="sxs-lookup"><span data-stu-id="91dd8-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="91dd8-114">Viena rinda ir novērtējuma izmaksu puse, un otra rinda ir pārdošanas puse.</span><span class="sxs-lookup"><span data-stu-id="91dd8-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="91dd8-115">Tas pats attiecas uz projekta līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="91dd8-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="91dd8-116">Kad veicat izmaiņas daudzumā vai laukā izmaksu pusē, šīs izmaiņas tiek ieviestas arī pārdošanas pusē.</span><span class="sxs-lookup"><span data-stu-id="91dd8-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="91dd8-117">Tas ir iespējams tāpēc, ka, izmantojot spraudņus PreOperation Quotelinedetail un contractline detaļu entītijās, noteikti atribūti izmaksu pusē tiek savienoti ar transakcijas pārdošanas pusi.</span><span class="sxs-lookup"><span data-stu-id="91dd8-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="91dd8-118">Ja cenu noteikšanas dimensiju vērtībām pārdošanas pusē veiktās izmaiņas ir nepieciešams veikt arī izmaksu pusē, pēc izmaiņu veikšanas cenu noteikšanas dimensijā ir atkārtoti jāreģistrē tālāk minētie spraudņi.</span><span class="sxs-lookup"><span data-stu-id="91dd8-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="91dd8-119">Šie ir spraudņi, kas jāatjaunina un atkārtoti jāreģistrē.</span><span class="sxs-lookup"><span data-stu-id="91dd8-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="91dd8-120">PreOperationContractLineDetailUpdate — **Atjaunina msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="91dd8-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="91dd8-121">PreOperationQuoteLineDetailUpdate — **Atjaunina msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="91dd8-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="91dd8-122">Izpildiet tālāk aprakstītās darbības, lai atjauninātu un atkārtoti reģistrētu spraudņus.</span><span class="sxs-lookup"><span data-stu-id="91dd8-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="91dd8-123">Atveriet **PluginRegistrationTool** un izveidojiet savienojumu ar Project Operations Dataverse vidi.</span><span class="sxs-lookup"><span data-stu-id="91dd8-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="91dd8-124">Atlasiet **Meklēt** un ierakstiet dažus pirmos atjaunināmā spraudņa burtus.</span><span class="sxs-lookup"><span data-stu-id="91dd8-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="91dd8-125">Kad spraudnis ir atrasts, atlasiet to un pēc tam atlasiet **Atlasīt galvenajā veidlapā**.</span><span class="sxs-lookup"><span data-stu-id="91dd8-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="91dd8-126">Atlasiet darbību **Update msdyn_orderlinetransaction**, ar peles labo pogu noklikšķiniet un pēc tam atlasiet vienumu **Atjaunināt**.</span><span class="sxs-lookup"><span data-stu-id="91dd8-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="91dd8-127">Dialoglodziņā **Atjaunināt** atlasiet daudzpunkti (**...**) filtrēšanas atribūtos.</span><span class="sxs-lookup"><span data-stu-id="91dd8-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="91dd8-128">Tiek filtrēšanas atribūtu logs, kurā ir pieejams saraksts ar visiem entītijas atribūtiem un cenu noteikšanas dimensijām.</span><span class="sxs-lookup"><span data-stu-id="91dd8-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="91dd8-129">Atzīmējiet cenu noteikšanas dimensiju atribūtu izvēles rūtiņas.</span><span class="sxs-lookup"><span data-stu-id="91dd8-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="91dd8-130">Atlasiet **Labi**, lai aizvērtu lapu, un pēc tam atlasiet **Atjaunināšanas darbība**.</span><span class="sxs-lookup"><span data-stu-id="91dd8-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="91dd8-131">Otrajā spraudnī **PreOperationQuoteLineDetail** atkārtojiet 2.–7. darbību.</span><span class="sxs-lookup"><span data-stu-id="91dd8-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="91dd8-132">Šim spraudnim ir nepieciešams atjaunināt darbību **Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="91dd8-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="91dd8-133">Aizveriet **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="91dd8-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]