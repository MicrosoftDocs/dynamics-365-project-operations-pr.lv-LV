---
title: Pielāgotu lauku un entītiju izveide
description: Šajā tēmā ir paskaidrots, kā izveidot opciju kopas un entītijas jūsu risinājumā Power Apps platformā.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290547"
---
# <a name="create-custom-fields-and-entities"></a>Pielāgotu lauku un entītiju izveide 

[!include [banner](../includes/psa-now-project-operations.md)]

Veiciet tālāk norādītās darbības jebkurā laikā, kad vēlaties izveidot pielāgotu opciju kopu vai entītiju platformā Power Apps.  
Šajā tēmā aprakstītās procedūras ir jāizpilda, izmantojot Project Service Automation (PSA) tīmekļa saskarni.

> [!IMPORTANT]
> Iesakām veikt visas pielāgotās cenu noteikšanas dimensijas izmaiņas katrā atsevišķā risinājumā. Šī svarīgā paraugprakse nodrošina elastību nākotnē, lai atjauninātu vai noņemtu nepieciešamās izmaiņas; tā palīdzēs ar jūsu darba atkārtotu izmantošanu un vienkāršos šo izmaiņu saglabāšanu citā gadījumā. Pēc visu nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldīts risinājums** un importējiet to citās instancēs, lai izmantotu cenas noteikšanas iestatījumus.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Pielāgotu lauku un opciju kopu izveide izmaksu dimensijas risinājumā

Cenas noteikšanas dimensija var būt opciju kopa vai entītija. Abi ir jāizveido cenas noteikšanas risinājumā. Šīs procedūras darbībās ir paskaidrots, kā izveidot entītiju pamatotas dimensijas un opciju kopas dimensijas.

### <a name="entity-based-dimensions"></a>Entītiju pamatotas dimensijas

1. Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**.
2. Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet vienumu **Entītijas**.
3. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu entītiju ar nosaukumu **Standarta nosaukums**. Ievadiet pārējo pieprasīto informāciju un pēc tam pieskarieties vienumam **Saglabāt**.

> ![Standarta nosaukuma entītijas definīcija](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Opciju kopas dimensijas 
Var izveidot divas opciju kopas dimensijas. Izmantojiet sadaļu **Resursa darba vieta**, lai izsekotu cenai opcijās **Mājas** un **Darbā**, kā arī lietotu **Resursa darba stundas** ar vērtībām **Regulārs** un **Virsstundas**, lai pievienotu atzīmi, kad darbs ir pabeigts.


1. Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**. 
2. Sadaļas Risinājumu pārlūks kreisajā navigācijas rūtī atlasiet vienumu **Opciju kopas**. 
3. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu opciju kopu, ievadiet atlikušo nepieciešamo informāciju un pēc tam t uz **Saglabāt**.

> ![Opciju kopa atkarībā no cenas, ko sauc par Resursu darba vietu ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Opciju kopa atkarībā no cenas, ko sauc par Resursu darba stundām ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Datu izveide entītijai atbilstošām dimensijām

Entītijas dimensijām datus var izveidot manuāli vai izmantojot Microsoft Excel importēšanas vai pakalpojuma izsaukumus. Izmantojiet šajā procedūrā norādītās darbības, lai izveidotu divu standarta nosaukumus: **Standarta inženieris** un **Vecākais sistēmu inženieris**, izmantojot entītijas dimensiju, kas pamatota sadaļā **Standarta nosaukums**. Ja dati, ko vēlaties izveidot, ir neliela izmēra, kā redzams šajā piemērā, varat izmantot standarta veidlapu.

1. Noklikšķiniet uz **Detalizētā atrašana**. Atlasiet entītiju **Standarta nosaukums** un pēc tam noklikšķiniet uz **Rezultāti**. Tiks rādītas visas **Standarta nosaukums** entītijas rindas.
2. Noklikšķiniet uz **Jauns**. Laukā **Nosaukums** ievadiet “Sistēmas inženieris ” un pēc tam noklikšķiniet uz **Saglabāt**.
3. Aizveriet veidlapu. 
4. Atkārtojiet 1.–3. darbību, lai izveidotu vēl vienu standarta nosaukumu “Vecākais sistēmas inženieris”.

> ![Standarta nosaukuma entītijas datu paraugs ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]