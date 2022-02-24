---
title: Projekta tāmes likvidēšana
description: Šajā tēmā ir sniegta informācija par projekta tāmes likvidēšanu pēc tā pabeigšanas.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270687"
---
# <a name="eliminate-a-project-estimate"></a>Projekta tāmes likvidēšana

[!include [banner](../includes/banner.md)]

Projekta tāmes sniedz finansiālu ieskatu par darbu, kāds ir prognozēts un plānots projektam. Lai strādātu ar projekta tāmi, šis projekts ir jāpievieno novērtējuma projektam. Novērtējuma projekts vienmēr tiek balstīts uz esošu projektu, tomēr vairāki projekti var attiekties uz vienu novērtējuma projektu. Tikai fiksētas cenas un investīciju projektus var pievienot novērtējuma projektiem, un šiem projektiem ir jāpieder tai pašai projektu grupai, kurai pieder novērtējuma projekts.

Lai likvidētu novērtējuma projektu, tam ir jābūt pabeigtam. Tālāk aprakstītajās darbībās ir paskaidrots, kā likvidēt tāmi.

1. Dodieties uz **Projektu pārvaldība un grāmatvedība** > **Visi projekti** un atveriet projektu. 
2. Cilnē **Pārvaldīt** atlasiet **Novērtējums** un lapā **Novērtējums** atlasiet **Likvidēt**.
3. Cilnes **Vispārīgi** lapā **Likvidēt tāmi** iestatiet tālāk norādītās opcijas.

   - **Perioda kods**: atlasiet perioda kodu, lai izvēlētos atbilstošus projektu aprēķinus. 
   - **Aprēķina datums**: atlasiet likvidēšanai atbilstošo aprēķina datumu.
   - **Likvidēt ar NP brīdinājumiem**: iespējojiet šo opciju, lai sniegtu paziņojumu, ja ar nepabeigtu darbu (NP) saistītais aprēķins tiks likvidēts. Ja šī opcija nav iespējota, likvidēšanu nevar turpināt, ja pastāv tāmē neiekļauti darījumi. 
   > [!NOTE]
   > Šī opcija ir pieejama tikai tad, ja novērtējuma projektā liek veikta likvidēšana. Tas nav pieejams, ja izmantojat periodiskus grāmatojumus. Šis iestatījums darbojas ar iestatījumiem, kas atrodas cilnes **Novērtējums** lapā **Projekta parametri** esošajā lauku grupā **Atļaut likvidēšanu, ja pastāv darījumi, kas nav iekļauti tāmē**.
   - **Iestatiet statusu uz Pabeigts**: iespējojiet šo opciju, lai pēc likvidēšanas izpildes iestatītu novērtējuma projekta statusu uz **Pabeigts**.
   - **Drukāt novērtējumu sarakstu**: atlasiet informāciju, kas jāiekļauj, izdrukājot novērtējumu sarakstu.
   - **Parādīt informācijas žurnālu**: iespējojiet šo opciju, lai rādītu informācijas žurnālu.
   - **Grāmatošanas datums**: izvēlieties novērtējuma grāmatošanas datumu.

4.  Atlasiet **Labi**.
5. Pēc tam, kad likvidēšanas process ir pabeigts, likvidētais novērtējuma projekts tiek parādīts ar negatīvu vērtību. 

Ja nevēlējāties likvidēt novērtējumu, varat atlasīt atcelto likvidēto novērtējumu un atlasīt **Atsaukt likvidēšanu**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]