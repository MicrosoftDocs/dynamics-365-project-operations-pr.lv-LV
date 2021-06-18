---
title: Resursu rezervācijas un kā tās saistītas ar uzdevumu piešķiri
description: Šī tēma sniedz informāciju par to, kā pārvaldīt nosauktos resursus, resursu rezervēšanu un uzdevumu piešķiršanu un kā tie saistīti viens ar otru.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 72c741d8a0644589004ba20afbcd0baff7cfcb06
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993200"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Resursu rezervācijas un kā tās saistītas ar uzdevumu piešķiri

[!include [banner](../includes/psa-now-project-operations.md)]

Ir divi veidi, kā nosauktos resursus var rezervēt projekta darba grupai un piešķirt projekta uzdevumus:

- Resurss var tieši rezervēts projektam un pēc tam vēlāk piešķirts projekta uzdevumiem.
- Uzdevumus var piešķirt vispārējam resursam, kas pēc tam tiek izmantots, lai atrastu un aizstātu vispārējo ar nosauktu resursu. 

Abos gadījumos ar resursa rezervēšanas darbību tiek rezervēta resursa noslodze.

Projekta vadītājam, kurš plāno šo projektu, pieder projekta plāns un grafiks. Izmantojot vispārējo resursu piešķiršanai un pēc tam izveidojot no tā resursu pieprasījumu, projekta vadītājs var rezervēt resursus projektam ar projekta plānā norādītajām kontūrām. Viņi var rezervēt resursu projektam un pēc tam piešķirt tos uzdevumiem, taču nav iespējams izlīdzināt rezervāciju kontūras ar uzdevumu kontūrām. Rezervācijas neietekmē projekta grafiku.

Ieteicams izmantot sarežģītu projektu ar vairākiem uzdevumiem, kuri pārklājas un kuros vienlaikus ir jādarbojas vairākiem viena veida resursiem. Ja resursam ir piešķirta kontūra, kas atšķiras no piešķīres apkopošanas, ir sarežģīti mainīt uzdevumus, lai tie rezervāciju kontūras piemērotu to atsevišķajiem uzdevumiem un sākotnējām kontūrām.

Tālāk atrodamajā piemērā kopējā piepūle, kas nepieciešama četru uzdevumu kopā esošam resursam, ir 62 stundas divu nedēļu periodā, un tiek izmantota noteikta kontūra. Ja resurss Bob ir rezervēts 62 stundas to pašu divu nedēļu laikā, bet ar citu kontūru, prasības un rezervācijas atbilst.

| **Uzdevuma kontūras**    | **Kopējais stundu skaits** | Pr 04.06. | Ot 05.06. | Tr 06.06. | Ce 07.06. | Pk 08.06. | Se 09.06. | Sv 10.06. | Pr 11.06. | Ot 12.06. | Tr 13.06. | Ce 14.06. | Pk 15.06. |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| 1. uzdevums               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| 2. uzdevums               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| 3. uzdevums               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| 4. uzdevums               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Kopsummas**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Jāņa pieejamība
| **Resursa rezervācija** | **Kopējais stundu skaits** | Pr 04.06. | Ot 05.06. | Tr 06.06. | Ce 07.06. | Pk 08.06. | Se 09.06. | Sv 10.06. | Pr 11.06. | Ot 12.06. | Tr 13.06. | Ce 14.06. | Pk 15.06. |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Jānis                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Tomēr nav sistemātiska veids, kā piešķirt rezervēto stundu kontūru uzdevumiem uz dienu. Ja projekta vadītājs ir gatavs mainīt projekta grafiku atbilstoši resursa pieejamībai, būs jānoņem piešķīre un jāpārskata visu uzdevumi, lai tie atbilstu rezervācijas kontūrām

Ja organizācija ir piešķīrusi projekta plānošanas uzdevumu gan projektu vadītājam un resursu pārvaldniekam, projekta vadītājs nosaka grafiku, kas ietver nepieciešamo darba konturēšanu. Resursu pārvaldniekam nevajadzētu ietekmēt grafiku bez projekta vadītāja ziņas, mainot darba kontūras, kad tiek veikta reālu resursu rezervācija. Ja resursu pārvaldnieks izpilda uzdevumu, kas atšķiras no projekta vadītāja pieprasīta, viņiem ir jāvienojas, kādas izmaiņas ir nepieciešamas projekta grafikā.

Tā kā rezervācijas un piešķīrumi nav cieši saistīti, ir iespējams rezervēt kontūras, kas atšķiras no uzdevuma kontūrām, vai mainīt piešķīrumus, lai rastos apstākļi, kur rezervācijas un piešķīrumi nav atbilstoši.

**Saskaņošanas skats** ļauj projekta vadītājam skatīt rezervācijas un piešķīrumus katram projekta darba grupas dalībniekam. Skats izmanto krāsas un ēnojumu, lai parādītu, kur ir neatbilstība starp darba grupas dalībnieku rezervācijām un piešķīrumiem. Pamatojoties uz šo informāciju, projektu vadītājs var veikt korekcijas, lai paplašinātu resursu rezervācijas gadījumos, kad ir piešķīrumi un nav rezervāciju, vai atcelt rezervācijas, ja resursi ir rezervēti, bet nav neviena piešķīruma.

> [!NOTE]
> Pārvietojot uzdevumu, kura kontūras esat izveidojis pats, kontūras netiek saglabātas. Kontūras atkārtoti tiek veidotas atbilstoši projekta kalendāram, lai ņemtu vērā darba laika un brīvdienu izmaiņas. Tas notiek uz konstrukcijas pamata, jo sistēma nezina sākotnējās kontūras nodomu un nevar noteikt, vai ir jēga šo kontūru saglabāt jaunā laika posmā. Tā kā rezervācijas un piešķīrumi ir atvienoti, rezervācijas saglabā sākotnējās rezervāciju kontūras. Šādā gadījumā būs jāatceļ un atkārtoti jārezervē jaunā piešķīruma kontūra.



[!INCLUDE[footer-include](../includes/footer-banner.md)]