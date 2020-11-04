---
title: Jaunu pielāgotu entītiju veidlapu pievienošana (Project Service Automation 2.x)
description: Šajā tēmā ir sniegta informācija par to, kā programmā Dynamics 365 Project Service Automation 2.x pievienot pielāgotas entītiju veidlapas iespējām, piedāvājumiem, pasūtījumiem vai rēķiniem.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080638"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="25245-103">Jaunu pielāgotu entītiju veidlapu pievienošana (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="25245-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="25245-104">Lauks Tips</span><span class="sxs-lookup"><span data-stu-id="25245-104">Type field</span></span> 

<span data-ttu-id="25245-105">Dynamics 365 Project Service Automation izmanto entītiju Iespēja, Piedāvājums, Pasūtījums un Rēķins lauku **Tips** ( **msdyn\_ordertype** ), lai atšķirtu šo entītiju **darba** versijas no **vienuma** un **servisa** versijām.</span><span class="sxs-lookup"><span data-stu-id="25245-105">Dynamics 365 Project Service Automation relies on the **Type** ( **msdyn\_ordertype** ) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="25245-106">Šo entītiju darba versijas apstrādā PSA.</span><span class="sxs-lookup"><span data-stu-id="25245-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="25245-107">Liela daļa biznesa loģikas risinājuma klienta pusē un servera pusē ir atkarīga no lauka **Tips**.</span><span class="sxs-lookup"><span data-stu-id="25245-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="25245-108">Tāpēc ir svarīgi, lai lauks tiktu inicializēts ar pareizu vērtību entītiju izveides brīdī.</span><span class="sxs-lookup"><span data-stu-id="25245-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="25245-109">Nepareiza vērtība var izraisīt nepareizu uzvedību, un daļa biznesa loģikas var nedarboties pareizi.</span><span class="sxs-lookup"><span data-stu-id="25245-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="25245-110">Automātiska veidlapu pārslēgšana</span><span class="sxs-lookup"><span data-stu-id="25245-110">Automatic form switching</span></span>

<span data-ttu-id="25245-111">Lai izvairītos no iespējamiem datu bojājumiem un neparedzētas uzvedības, kas rodas, nepareizi inicializējot un rediģējot pārdošanas entītiju ierakstus, PSA tagad ietver loģiku automātiskai veidlapu pārslēgšanai neiekļautās veidlapās.</span><span class="sxs-lookup"><span data-stu-id="25245-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="25245-112">Šī loģika novirza lietotājus uz pareizo veidlapu darbam ar darba versiju vai jebkuru citu entītijas Iespēja, Piedāvājums, Pasūtījums vai Rēķins tipu.</span><span class="sxs-lookup"><span data-stu-id="25245-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="25245-113">Kad lietotājs atver entītijas Iespēja, Piedāvājums, Pasūtījums vai Rēķins darba versiju, veidlapa tiek pārslēgta uz vienumu **Projekta informācija**.</span><span class="sxs-lookup"><span data-stu-id="25245-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="25245-114">Automātiskās veidlapu pārslēgšanas loģikas pamatā ir kartēšana starp vērtību **formId** un lauku **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="25245-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="25245-115">Šai kartēšanai ir pievienotas visas neiekļautās veidlapas.</span><span class="sxs-lookup"><span data-stu-id="25245-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="25245-116">Taču pielāgotās veidlapas ir jāpievieno manuāli, lai norādītu, kura entītijas versija ir paredzēta apstrādei.</span><span class="sxs-lookup"><span data-stu-id="25245-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="25245-117">Tā pamatā ir lauks **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="25245-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="25245-118">Ja kartēšanā trūkst veidlapas pārslēgšanas, loģika pārslēgsies uz veidlapas neiekļauto veidlapu, pamatojoties uz vērtību, kas ir saglabāta entītijas laukā **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="25245-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="25245-119">Pielāgotu veidlapu pievienošana un veidlapas pārslēgšanas loģikas ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="25245-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="25245-120">Tālāk esošajā piemērā ir parādīts, kā pievienot pielāgotu veidlapu **Mana projekta informācija** tā, lai tā darbotos iespējām, kas balstītas uz darbu.</span><span class="sxs-lookup"><span data-stu-id="25245-120">The following example shows how to add a custom form, **My Project Information** , so that it works with work-based opportunities.</span></span> <span data-ttu-id="25245-121">Tas pats process tiek izmantots pielāgotu veidlapu pievienošanai tā, lai tās darbotos ar piedāvājumiem, pasūtījumiem un rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="25245-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="25245-122">Veiciet šīs darbības, lai izveidotu pielāgotu veidlapas **Projekta informācija** versiju.</span><span class="sxs-lookup"><span data-stu-id="25245-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="25245-123">Entītijā Iespēja atveriet veidlapu **Projekta informācija** un saglabājiet kopiju ar nosaukumu **Mana projekta informācija**.</span><span class="sxs-lookup"><span data-stu-id="25245-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="25245-124">Atveriet jauno veidlapu un pēc tam rekvizītos pārliecinieties, vai ir pieejami veidlapas inicializācijas skripti no veidlapas **Projekta informācija**.</span><span class="sxs-lookup"><span data-stu-id="25245-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="25245-125">Nenoņemiet skriptus.</span><span class="sxs-lookup"><span data-stu-id="25245-125">Don't remove the scripts.</span></span> <span data-ttu-id="25245-126">Pretējā gadījumā daļa datu var tikt inicializēti nepareizi.</span><span class="sxs-lookup"><span data-stu-id="25245-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="25245-127">Pārbaudiet, vai veidlapā ir lauks **Tips** ( **msdyn\_ordertype** ).</span><span class="sxs-lookup"><span data-stu-id="25245-127">Verify that the **Type** ( **msdyn\_ordertype** ) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="25245-128">Nenoņemiet šo lauku.</span><span class="sxs-lookup"><span data-stu-id="25245-128">Don't remove this field.</span></span> <span data-ttu-id="25245-129">Pretējā gadījumā inicializācijas skripti neizdosies.</span><span class="sxs-lookup"><span data-stu-id="25245-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="25245-130">Atrodiet jaunās veidlapas vērtību **formId**.</span><span class="sxs-lookup"><span data-stu-id="25245-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="25245-131">To var izdarīt divos dažādos veidos.</span><span class="sxs-lookup"><span data-stu-id="25245-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="25245-132">Eksportējiet veidlapu **Mana projekta informācija** kā nepārvaldīta risinājuma daļu un pēc tam uzmeklējiet vērtību **formId** eksportētā risinājuma failā customization.xml.</span><span class="sxs-lookup"><span data-stu-id="25245-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="25245-133">Atveriet veidlapu **Mana projekta informācija** veidlapu redaktorā un pēc tam meklējiet vispārēji unikālo identifikatoru (GUID) blakus parametram **fromId** vietrādī URL, kā parādīts tālāk redzamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="25245-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Jaunās veidlapas vērtība formId vietrādī URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="25245-135">Izveidojiet **msdyn\_ordertype** kartējumu vērtībai **formId** , rediģējot msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js tīmekļa resursu.</span><span class="sxs-lookup"><span data-stu-id="25245-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="25245-136">Noņemiet no resursa kodu un aizstājiet ar tālāk norādīto kodu.</span><span class="sxs-lookup"><span data-stu-id="25245-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="25245-137">Saglabājiet un publicējiet pielāgojumus.</span><span class="sxs-lookup"><span data-stu-id="25245-137">Save and then publish the customizations.</span></span>
