---
title: Projekta piedāvājuma rindas aprēķināšana
description: Šajā tēmā sniegta informācija par to, kā izveidot aprēķinu par projekta piedāvājuma rindu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dbd3876e555ee6bc70308ef11a3528a5dd8b6a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273561"
---
# <a name="estimating-a-project-based-quote-line"></a>Projekta piedāvājuma rindas aprēķināšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta piedāvājuma rindā ir informācija, kas palīdz aprēķināt attiecīgā darba izmaksas un iespējamos ieņēmumus, lai izpildītu piedāvājuma rindu.

Lai aprēķinātu projekta piedāvājuma rindu, projekta piedāvājuma rindā atlasiet cilni **Piedāvājuma rindas informācija**. Projekta piedāvājuma rindas piedāvājumu var aprēķināt divējādi.

- Aprēķinu manuāla izveide tieši piedāvājuma rindā, izmantojot piedāvājuma rindas informāciju 
- Izveidojiet projektu un projekta plānu un pēc tam saistiet projektu un projekta uzdevumus ar piedāvājuma rindu. Tiek iespējots process, kurā projekta plānā ietvertie aprēķini tiek importēti piedāvājuma rindā, pamatojoties uz jūsu sniegto informāciju.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Aprēķinu izveide tieši projekta piedāvājuma rindā

Lai izveidotu aprēķinu projekta piedāvājuma rindā, atlasiet cilni **Piedāvājuma rindas informācija** . Rindas elements, ko izveidojat šajā cilnē, apkopo šīs piedāvājuma rindas aprēķināto vērtību. 

Lai izveidotu piedāvājuma rindas informāciju, atlasiet **+ Jauna piedāvājuma rindas informācija** apakšrežģī **Piedāvājuma rindas informācija**. Tiks atvērts ātrās izveides slīdnis. Veidlapā **Piedāvājuma rinda** ir šādi lauki:

| **Lauks** | **Atrašanās vieta** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Apraksts | Ātrā izveide | Konkrētā aprēķina apraksts. | Šis lauks pēc noklusējuma ir saistīts ar automātiski izveidoto piedāvājuma rindas informāciju. |
| Darījuma klase | Ātrā izveide | Šis nolaižamais saraksts nodrošina darījumu klases, kas ir ietvertas projekta piedāvājuma rindas cilnē **Vispārīgi**.  | Šis lauks pēc noklusējuma ir saistīts ar automātiski izveidoto piedāvājuma rindas informāciju. |
| Loma | Ātrā izveide | Persona, kas veiks šo darbu vai apmaksās šos izdevumus. | Šis lauks pēc noklusējuma ir saistīts ar automātiski izveidoto piedāvājuma rindas informāciju. |
| Kategorija | Ātrā izveide | Darba vai izdevumu kategorija. | Šis lauks pēc noklusējuma ir saistīts ar automātiski izveidoto piedāvājuma rindas informāciju. |
| Sākuma datums | Ātrā izveide | Darba sākuma datums. | Šis lauks pēc noklusējuma ir saistīts ar automātiski izveidoto piedāvājuma rindas informāciju. |
| Beigu datums | Ātrā izveide | Darba beigu datums. | Šis lauks pēc noklusējuma ir saistīts ar automātiski izveidoto piedāvājuma rindas informāciju. |
| Resursu vienība | Ātrā izveide | Resursu vienība, kas apmaksās šīs izmaksas un nodrošinās resursu darbam ar to. | Šis lauks pēc noklusējuma ir saistīts ar automātiski izveidoto piedāvājuma rindas informāciju. Šo lauku izmanto arī izmaksu izgūšanai. |
| Vienības grafiks | Ātrā izveide | Darba vai izdevumu vienību grupa. Vienības pieder vienību grafikam vai vienību grupai. Piemēram, jūdzes un km ir vienības, kas pieder vienību grupai, ar ko apraksta attālumu. | Šis lauks pēc noklusējuma ir saistīts ar automātiski izveidoto piedāvājuma rindas informāciju. |
| Vienība | Ātrā izveide | Darba vai izdevumu vienība. | Šis lauks pēc noklusējuma ir saistīts ar automātiski izveidoto piedāvājuma rindas informāciju. |
| Daudzums | Ātrā izveide | Darba vai izdevumu daudzums | Šis lauks pēc noklusējuma ir saistīts ar automātiski izveidoto piedāvājuma rindas informāciju. |
| Vienības cena | Ātrā izveide | Tās lomas rēķina likme, kas veic darbu, vai izdevumu kategorijas pārdošanas cena. Šis lauks ir noklusējuma Laiks, pamatojoties uz lomu un resursu plānošanas vienību kombināciju projekta cenrādi, kas ir spēkā sākuma datumā. Attiecībā uz izdevumiem šis lauks pēc noklusējuma ir cenas iestatījums darījuma kategorijai projekta cenrādī, kas ir spēkā sākuma datumā. Ja darījumu kategorijas cenu noteikšanas metode nav cena par vienību, noklusējuma vērtības nav un šis lauks tiek atstāts tukšs. | Tās lomas izmaksu likme, kas veic darbu, vai izdevumu kategorijas vienības izmaksas. Šis lauks ir noklusējuma Laiks, pamatojoties uz lomu un resursu plānošanas vienību kombināciju Līgumslēdzēja vienības cenā Piedāvājuma cenrādī, kas ir spēkā sākuma datumā. Attiecībā uz izdevumiem šis lauks pēc noklusējuma ir cenas iestatījums darījuma kategorijai Līgumslēdzēja vienības izmaksu cenrādī, kas ir spēkā sākuma datumā. Ja darījumu kategorijas cenu noteikšanas metode nav cena par vienību, noklusējuma vērtības nav un šis lauks tiek atstāts tukšs. |
| Aprēķinātais nodoklis | Ātrā izveide | Varat manuāli ievadīt šī darba vai izdevumu aprēķināto nodokli. | Šim laukam nav lejupstraumes ietekmes. |
| Apjoms/summa | Ātrā izveide | Ja lauki **Daudzums** un **Cena** ir atstāti tukši, šajā laukā varat ievadīt informāciju manuāli. Ja šie lauki nav tukši, šis lauks kļūst tikai lasāms un tiek aprēķināts kā (Daudzums \* Vienības cena) + Nodoklis. | Šim laukam nav lejupstraumes ietekmes. |

## <a name="update-prices-on-quote-line-details"></a>Cenas atjaunināšana piedāvājuma rindas informācijā

Ja esat mainījis cenas projekta cenrādī, kas ir pievienots piedāvājumam, vai līgumslēdzēja vienības izmaksu cenrādī, varat atlasīt vienumu **Pārrēķināt** lapā **Piedāvājums**, lai atsvaidzinātu atsevišķas piedāvājuma rindas informācijas cenas un atspoguļotu veiktās izmaiņas. Kad atlasāt opciju **Pārrēķināt**, jūs ar brīdinājumu tiekat informēts, ka cenas piedāvājuma rindas informācijā par visām šī piedāvājuma rindām tiks atiestatītas. Atlasiet **Jā**, lai atsvaidzinātu cenas gan pārdošanas, gan izmaksu piedāvājuma rindas informācijā.

## <a name="access-quote-line-details-for-cost"></a>Piekļuve piedāvājuma rindas informācijai attiecībā uz izmaksām

Cilnē **Piedāvājuma rindas informācija** atlasiet režģa rindu, lai iespējotu dažas darbības apakšrežģa rīkjoslā. Ja atlasāt piedāvājuma rindas informāciju, pirmā darbība apakšrežģa rīkjoslā ir **Atvērt izmaksu informāciju**. Atlasiet vienumu **Atvērt izmaksu informāciju**, lai skatītu šīs piedāvājuma rindas saistīto izmaksu likmi un summu.

> [!NOTE]
> Mainot piedāvājuma rindas informācijas resursu vienības, daudzuma, datumu, lomas vai kategorijas vērtības attiecībā uz izmaksām, tiek mainītas arī atbilstošās vērtības piedāvājuma rindas informācijā par pārdošanu.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valūta piedāvājuma rindas informācijā attiecībā uz izmaksām un pārdošanu

Valūta piedāvājuma rindas informācijā attiecībā uz pārdošanas noklusējuma vērtībām no projekta cenrāža, kas ir spēkā piedāvājuma rindas informācijas sākuma datumā.

Valūta piedāvājuma rindas informācijā attiecībā uz izmaksu noklusējuma vērtībām no piedāvājuma līgumslēdzēja vienības cenrāža, kas ir spēkā piedāvājuma rindas informācijas par izmaksām sākuma datumā.

Rentabilitātes aprēķinos summas par piedāvājumu rindu informāciju attiecībā uz izmaksām un pārdošanas apjomiem tiek konvertētas attiecīgās vides pamata valūtā, lai sniegtu atskaiti par piedāvājuma prognozēto peļņu.

Tas var izraisīt valūtu noapaļošanas kļūdas un mainīt peļņu, jo nav konkrētajā datumā spēkā esošo valūtas kursu. Izmantojiet šos aprēķinus par Projekta piedāvājumiem tikai kā tuvinājumus, nevis faktiskas obligātas vai cita veida atskaites, kam ir nepieciešama augstāka noapaļošanas precizitāte un konkrētos datumos spēkā esoši valūtas kursi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]