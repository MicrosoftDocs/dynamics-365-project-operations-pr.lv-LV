---
title: Pielāgotu lauku un entītiju kā cenu noteikšanas kategoriju izveide
description: Šajā tēmā sniegta informācija par to, kā izveidot pielāgotas opciju kopas vai entitījas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080482"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Pielāgotu lauku un entītiju kā cenu noteikšanas kategoriju izveide

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Veiciet tālāk norādītās darbības jebkurā laikā, kad vēlaties izveidot pielāgotu opciju kopu vai entītiju.

> [!IMPORTANT]
> Iesakām veikt visas pielāgotās cenu noteikšanas dimensijas izmaiņas katrā atsevišķā risinājumā. Šī svarīgā paraugprakse nodrošina elastību nākotnē, lai atjauninātu vai noņemtu nepieciešamās izmaiņas; tā palīdzēs ar jūsu darba atkārtotu izmantošanu un vienkāršos šo izmaiņu saglabāšanu citā gadījumā. Pēc visu nepieciešamo izmaiņu veikšanas eksportējiet šo risinājumu kā **Pārvaldīts risinājums** un importējiet to citās instancēs, lai izmantotu cenas noteikšanas iestatījumus.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Pielāgota risinājuma izveide cenu noteikšanas dimensijām
1. Dodieties uz **Iestatījumi** > **Risinājumi** un pēc tam atlasiet **Jauns** , lai izveidotu jaunu risinājumu. 
2. Nosauciet risinājumu **\<your organization name>cenu noteikšanas dimensijas** , ievadiet atlikušo nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Pielāgotu lauku un opciju kopu izveide izmaksu dimensijas risinājumā

Cenas noteikšanas dimensija var būt opciju kopa vai entītija. Abi ir jāizveido cenas noteikšanas risinājumā. Šīs procedūras darbībās ir paskaidrots, kā izveidot entītiju pamatotas dimensijas un opciju kopas dimensijas.

### <a name="entity-based-dimensions"></a>Entītiju pamatotas dimensijas

1. Dodieties uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**.
2. Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet vienumu **Entītijas**.
3. Atlasiet **Jauns** , lai izveidotu jaunu entītiju ar nosaukumu **Standarta nosaukums**. 
4. Ievadiet pārējo pieprasīto informāciju un pēc tam atlasiet **Saglabāt**.


### <a name="option-set-based-dimensions"></a>Opciju kopas dimensijas 
Var izveidot divas opciju kopas dimensijas. Izmantojiet sadaļu **Resursa darba vieta** , lai izsekotu cenai opcijās **Mājas** un **Darbā** , kā arī lietotu **Resursa darba stundas** ar vērtībām **Regulārs** un **Virsstundas** , lai pievienotu atzīmi, kad darbs ir pabeigts.


1. Dodieties uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**. 
2. Sadaļas Risinājumu pārlūks kreisajā navigācijas rūtī atlasiet vienumu **Opciju kopas**. 
3. Atlasiet **Jauns** , lai izveidotu jaunu opciju kopu, ievadiet atlikušo nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.

## <a name="create-data-for-entity-based-dimensions"></a>Datu izveide entītijai atbilstošām dimensijām

Entītijas dimensijām datus var izveidot manuāli vai izmantojot Microsoft Excel importēšanas vai pakalpojuma izsaukumus. Izmantojiet šajā procedūrā norādītās darbības, lai izveidotu divu standarta nosaukumus: **Standarta inženieris** un **Vecākais sistēmu inženieris** , izmantojot entītijas dimensiju, kas pamatota sadaļā **Standarta nosaukums**. Ja dati, ko vēlaties izveidot, ir neliela izmēra, kā redzams šajā piemērā, varat izmantot standarta veidlapu.

1. Atlasiet **Detalizēta atrašana** , atlasiet entitīju **Standarta nosaukums** un pēc tam atlasiet **Rezultāti**. Tiks rādītas visas **Standarta nosaukums** entītijas rindas.
2. Atlasiet **Jauns** un laukā **Nosaukums** ievadiet "Sistēmu inženieris", un pēc tam atlasiet **Saglabāt**.
3. Aizvērt veidlapu. 
4. Atkārtojiet 1.–3. darbību, lai izveidotu vēl vienu standarta nosaukumu “Vecākais sistēmas inženieris”.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Pievienojiet visas prasītās entītijas un ar tām saistītos komponentus cenas noteikšanas risinājumam.
Cenas risinājumam ir jāpievieno tālāk norādītās entītijas. Izmantojiet šajā procedūrā norādītās darbības, lai veiktu dažas svarīgas shēmas izmaiņas cenas noteikšanas risinājumā un lai entītijas apzinātos jaunās cenu noteikšanas dimensijas.

1. Atlasiet **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**. 
2. Risinājumu pārlūka kreisajā navigācijas rūtī atlasiet **Pievienot esošo** > **Entītijas**.
3. Dialoglodziņā **Risinājumu sastāvdaļas** atlasiet vienu no šīm entītijām:

  - Faktiski
  - Rezervējams resurss
  - Novērtējuma rinda
  - Rēķina rindas informācija
  - Žurnāla rinda
  - Projekta līguma rindas informācija
  - Projekta grupas dalībnieks
  - Piedāvājuma rindas informācija
  - Lomas cenas uzcenojums
  - Lomas cena 
  - Laika ieraksts 


> [!NOTE]
> Pārliecinieties, vai visām atlasītajām entītijām ir atlasītas visas formas un skati.

4. Kad tiek piedāvāts iekļaut iepriekš atlasīto entītiju atkarīgās entītijas, atlasiet **Nē**.

