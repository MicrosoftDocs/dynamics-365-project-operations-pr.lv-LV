---
title: Jaunu pielāgotu entītiju veidlapu pievienošana (Project Service Automation 2.x)
description: Šajā tēmā ir sniegta informācija par to, kā programmā Dynamics 365 Project Service Automation 2.x pievienot pielāgotas entītiju veidlapas iespējām, piedāvājumiem, pasūtījumiem vai rēķiniem.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e59e343887ef59ee28bee13346a0c9bf3ad7df27346e2a4f3f02a1e5c08c060f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995230"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Jaunu pielāgotu entītiju veidlapu pievienošana (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Lauks Tips 

Dynamics 365 Project Service Automation izmanto entītiju Iespēja, Piedāvājums, Pasūtījums un Rēķins lauku **Tips** (**msdyn\_ordertype**), lai atšķirtu šo entītiju **darba** versijas no **vienuma** un **servisa** versijām. Šo entītiju darba versijas apstrādā PSA. Liela daļa biznesa loģikas risinājuma klienta pusē un servera pusē ir atkarīga no lauka **Tips**. Tāpēc ir svarīgi, lai lauks tiktu inicializēts ar pareizu vērtību entītiju izveides brīdī. Nepareiza vērtība var izraisīt nepareizu uzvedību, un daļa biznesa loģikas var nedarboties pareizi.

## <a name="automatic-form-switching"></a>Automātiska veidlapu pārslēgšana

Lai izvairītos no iespējamiem datu bojājumiem un neparedzētas uzvedības, kas rodas, nepareizi inicializējot un rediģējot pārdošanas entītiju ierakstus, PSA tagad ietver loģiku automātiskai veidlapu pārslēgšanai neiekļautās veidlapās. Šī loģika novirza lietotājus uz pareizo veidlapu darbam ar darba versiju vai jebkuru citu entītijas Iespēja, Piedāvājums, Pasūtījums vai Rēķins tipu. Kad lietotājs atver entītijas Iespēja, Piedāvājums, Pasūtījums vai Rēķins darba versiju, veidlapa tiek pārslēgta uz vienumu **Projekta informācija**.

Automātiskās veidlapu pārslēgšanas loģikas pamatā ir kartēšana starp vērtību **formId** un lauku **msdyn\_ordertype**. Šai kartēšanai ir pievienotas visas neiekļautās veidlapas. Taču pielāgotās veidlapas ir jāpievieno manuāli, lai norādītu, kura entītijas versija ir paredzēta apstrādei. Tā pamatā ir lauks **msdyn\_ordertype**. Ja kartēšanā trūkst veidlapas pārslēgšanas, loģika pārslēgsies uz veidlapas neiekļauto veidlapu, pamatojoties uz vērtību, kas ir saglabāta entītijas laukā **msdyn\_ordertype**.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Pielāgotu veidlapu pievienošana un veidlapas pārslēgšanas loģikas ieslēgšana

Tālāk esošajā piemērā ir parādīts, kā pievienot pielāgotu veidlapu **Mana projekta informācija** tā, lai tā darbotos iespējām, kas balstītas uz darbu. Tas pats process tiek izmantots pielāgotu veidlapu pievienošanai tā, lai tās darbotos ar piedāvājumiem, pasūtījumiem un rēķiniem.

Veiciet šīs darbības, lai izveidotu pielāgotu veidlapas **Projekta informācija** versiju.

1. Entītijā Iespēja atveriet veidlapu **Projekta informācija** un saglabājiet kopiju ar nosaukumu **Mana projekta informācija**.
2. Atveriet jauno veidlapu un pēc tam rekvizītos pārliecinieties, vai ir pieejami veidlapas inicializācijas skripti no veidlapas **Projekta informācija**. 

    > [!IMPORTANT]
    > Nenoņemiet skriptus. Pretējā gadījumā daļa datu var tikt inicializēti nepareizi.

3. Pārbaudiet, vai veidlapā ir lauks **Tips** (**msdyn\_ordertype**). 

    > [!IMPORTANT]
    > Nenoņemiet šo lauku. Pretējā gadījumā inicializācijas skripti neizdosies.

4. Atrodiet jaunās veidlapas vērtību **formId**. To var izdarīt divos dažādos veidos.

    - Eksportējiet veidlapu **Mana projekta informācija** kā nepārvaldīta risinājuma daļu un pēc tam uzmeklējiet vērtību **formId** eksportētā risinājuma failā customization.xml.
    - Atveriet veidlapu **Mana projekta informācija** veidlapu redaktorā un pēc tam meklējiet vispārēji unikālo identifikatoru (GUID) blakus parametram **fromId** vietrādī URL, kā parādīts tālāk redzamajā attēlā.

    ![Jaunās veidlapas vērtība formId vietrādī URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Izveidojiet **msdyn\_ordertype** kartējumu vērtībai **formId**, rediģējot msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js tīmekļa resursu. Noņemiet no resursa kodu un aizstājiet ar tālāk norādīto kodu.

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

6. Saglabājiet un publicējiet pielāgojumus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]