---
title: Apakšuzņēmēju kā rezervējamu resursu iestatīšana
description: Šajā rakstā izskaidrots, kā iestatīt un uzturēt apakšuzņēmēju resursus, kas tiek veidoti no sistēmas lietotājiem un kontaktpersonām, lai tos varētu saistīt ar apakšuzņēmējiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 727508c41c190c3703e9cd1420066fa0e551f147
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522711"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Apakšuzņēmēju kā rezervējamu resursu iestatīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Veiciet šīs darbības, lai apakšuzņēmējus iestatītu kā rezervējamus resursus programmā Microsoft Dynamics 365 Project Operations.

1. Atveriet sadaļu **Projekts** \> **Resursi** un atlasiet **Jauns**.
2. Lapas **Jauns rezervējams resurss** laukā **Resursa tips** atlasiet kādu no šīm opcijām:

    - **Lietotājs** — atlasiet šo resursa tipu, ja apakšuzņēmējam jāpiekļūst programmai Project Operations, lai ievadītu laiku vai izmaksas. Atlasot **Lietotājs**, apakšuzņēmējam ir nepieciešama derīga licence, lai piekļūtu sistēmai.
    - **Kontaktpersona** vai **Uzņēmums** — atlasiet vienu no šiem resursu tipiem, ja apakšuzņēmējam nav nepieciešama piekļuve programmai Project Operations, bet jābūt pieejamam uzdevumu piešķirēm vai rezervācijām projektos. Neviens no šiem resursu tipiem nenodrošina piekļuvi sistēmai. Atlasiet **Uzņēmums**, lai pārdevēja uzņēmumu norādītu kā rezervējamu resursu. Atlasiet vienumu **Kontaktpersona**, lai pārstāvētu atsevišķus pārdevēja darbiniekus.

3. Atkarībā no atlasītā resursa tipa tiek piedāvāts atlasīt atbilstošo lietotāja, uzņēmuma vai kontaktpersonas ierakstu.
4. Laukā **Darbinieka tips** atlasiet "Līgumdarbinieks", lai apakšuzņēmēju iestatītu kā rezervējamu resursu.

    > [!NOTE]
    > Atstājot lauku **Darbinieka tips** tukšu, rezervējamais resurss tiks uzskatīts par darbinieku.

5. Ja kā darbinieka tipu atlasījāt **Līgumdarbinieks**, atlasiet pārdevēju, ar kuru šis resurss sadarbojas.
6. Atlasiet resursa laika joslu un pēc tam atlasiet **Saglabāt**. Lai rezervējamam resursam piešķirtu darba stundu veidni, saraksta **Rezervējami resursi** lapā atlasiet **Iestatīt kalendāru**.

Lai rezervējamais resurss būtu saistīts ar apakšlīguma rindu, tam jāatbilst tālāk minētajiem nosacījumiem.

- Rezervējamajam resursam ir jābūt līgumdarbiniekam.
- **Kontaktpersonas** resursa tipa rezervējamam resursam jābūt saistītam ar pārdevēja uzņēmumu kā kontaktpersonu. Resursa tipa **Lietotājs** rezervējamam resursam nav jābūt saistītam ar pārdevēja uzņēmumu kā kontaktpersonu.
- Rezervējamā resursa lauka **Pārdevējs** vērtībai ir jāatbilst apakšlīguma lauka **Pārdevējs** vērtībai.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Rezervējamo resursu darbinieku un pārdevēju kartējuma tipa atjaunināšana

Rezervējamā resursa lauks **Darbinieka tips** tips nosaka, vai rezervējamais resurss ir līgumdarbinieks vai algots darbinieks. Lauks **Pārdevējs** nosaka pārdevēja uzņēmumu, ar kuru ir saistīts rezervējamais resurss. Saistot rezervējamu resursu ar pārdevēju kā kontaktpersonu, tiek norādīts, ka kontaktpersona ir pārdevēja uzņēmuma darbinieks.

Ja rezervējamā resursa lauki **Darbinieka tips** un **Pārdevējs** tiek mainīti, šīs izmaiņas ietekmē turpmāku rezervējamā resursa veiktu jaunu ierakstu, piemēram, laika ierakstu, apstiprināšanu. Tomēr šīs izmaiņas nepadara esošos ierakstus par nederīgiem.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
