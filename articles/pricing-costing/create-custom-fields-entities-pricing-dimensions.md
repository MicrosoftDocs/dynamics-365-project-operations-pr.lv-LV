---
title: Pielāgotu lauku un entītiju kā cenu noteikšanas kategoriju izveide
description: Šajā tēmā sniegta informācija par to, kā izveidot pielāgotas opciju kopas vai entitījas.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275637"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Pielāgotu lauku un entītiju kā cenu noteikšanas kategoriju izveide

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Veiciet tālāk norādītās darbības, kad vēlaties izveidot pielāgotu opciju kopu vai entītiju, lai to izmantotu kā cenu noteikšanas dimensiju. Papildinformāciju skatiet sadaļā [Cenu noteikšanas dimensiju pārskats](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Iesakām veikt visas pielāgotās cenu noteikšanas dimensijas izmaiņas katrā atsevišķā risinājumā. Šī svarīgā paraugprakse nodrošina elastību nākotnē, lai atjauninātu vai noņemtu nepieciešamās izmaiņas. Tā arī palīdzēs atkārtoti izmantot darbu un vienkāršos šo izmaiņu saglabāšanu citā instancē. Pēc visu nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldītu risinājumu** un importējiet to citās instancēs, lai atkārtoti izmantotu cenu noteikšanas iestatījumus.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Pielāgotu lauku un opciju kopu izveide izmaksu dimensijas risinājumā

Cenas noteikšanas dimensija var būt opciju kopa vai entītija. Abi ir jāizveido cenas noteikšanas risinājumā. Šīs procedūras darbībās ir paskaidrots, kā izveidot entītiju pamatotas dimensijas un opciju kopas dimensijas.

### <a name="entity-based-dimensions"></a>Entītiju pamatotas dimensijas
Lai izveidotu entītiju dimensijas, veiciet tālāk norādītās darbības.

1. Dodieties uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**.
2. Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Entītijas**.
3. Atlasiet **Jauns**, lai izveidotu jaunu entītiju ar nosaukumu **Standarta nosaukums**. 
4. Ievadiet pārējo pieprasīto informāciju un pēc tam atlasiet **Saglabāt**.

> ![Standarta nosaukuma entītijas definīcija](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Opciju kopas dimensijas 
Var izveidot divas opciju kopas dimensijas. 

- Izmantojiet opciju **Resursa darba atrašanās vieta**, lai izsekotu atrašanās vietu **Mājas** un **Uz vietas** darba cenu. 
- Izmantojiet **Resursa darba stundas** ar vērtībām **Regulāras** un **Virsstundas**, lai pēc darba pabeigšanas lietotu uzcenojumu.

Tālāk esošajā grafikā ir sniegts dimensijas **Resursa darba atrašanās vieta** skats. 

> ![Opciju kopa atkarībā no cenas, ko sauc par Resursu darba vietu](media/Option-set-PD-called-Resource-Work-Location.png)

Tālāk esošajā grafikā ir sniegts dimensijas **Resursa darba stundas** skats. 

> ![Opciju kopa atkarībā no cenas, ko sauc par Resursu darba stundām](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Dodieties uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**. 
2. Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Opciju kopas**. 
3. Atlasiet **Jauns**, lai izveidotu jaunu opciju kopu, ievadiet atlikušo nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.

## <a name="create-data-for-entity-based-dimensions"></a>Datu izveide entītijai atbilstošām dimensijām

Entītijas dimensijām datus var izveidot manuāli vai izmantojot Microsoft Excel importēšanas vai pakalpojuma izsaukumus. Izmantojiet šajā procedūrā norādītās darbības, lai izveidotu divu standarta nosaukumus: **Standarta inženieris** un **Vecākais sistēmu inženieris**, izmantojot entītijas dimensiju, kas pamatota sadaļā **Standarta nosaukums**. Ja dati, ko vēlaties izveidot, ir neliela izmēra, kā redzams šajā piemērā, varat izmantot standarta veidlapu.

1. Atlasiet **Detalizētā atrašana**.
2. Atlasiet entītiju **Standarta nosaukums** un pēc tam atlasiet **Rezultāti**. Tiks rādītas visas **Standarta nosaukums** entītijas rindas.
3. Atlasiet **Jauns** un laukā **Nosaukums** ievadiet "Sistēmu inženieris", un pēc tam atlasiet **Saglabāt**.
4. Aizveriet lapu. 
5. Atkārtojiet 1.–3. darbību, lai izveidotu vēl vienu standarta nosaukumu “Vecākais sistēmas inženieris”.

> ![Standarta nosaukuma entītijas datu paraugs](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]