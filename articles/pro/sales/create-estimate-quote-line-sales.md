---
title: Projekta piedāvājuma rindas aprēķināšana
description: Šajā tēmā sniegta informācija par to, kā izveidot aprēķinu par projekta piedāvājuma rindu.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a29cf20fe95ee5bfb189defded4f06aadb75a841
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598359"
---
# <a name="estimating-a-project-based-quote-line"></a>Projekta piedāvājuma rindas aprēķināšana

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta piedāvājuma rindā ir informācija, kas palīdz aprēķināt attiecīgā darba izmaksas un iespējamos ieņēmumus, lai izpildītu piedāvājuma rindu.

Lai aprēķinātu projekta piedāvājuma rindu, projekta piedāvājuma rindā atlasiet cilni **Piedāvājuma rindas informācija**. Projekta piedāvājuma rindas piedāvājumu var aprēķināt divējādi.

- Novērtējuma manuāla izveide tieši piedāvājuma rindā, izmantojot piedāvājuma rindas informāciju. 
- Izveidojiet projektu un projekta plānu un pēc tam saistiet projektu un projekta uzdevumus ar piedāvājuma rindu. Tiek iespējots process, kurā projekta plānā ietvertie aprēķini tiek importēti piedāvājuma rindā, pamatojoties uz jūsu sniegto informāciju.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Aprēķinu izveide tieši projekta piedāvājuma rindā

Lai izveidotu aprēķinu projekta piedāvājuma rindā, atlasiet cilni **Piedāvājuma rindas informācija** . Rindas elements, ko izveidojat šajā cilnē, apkopo šīs piedāvājuma rindas aprēķināto vērtību. 

Lai izveidotu piedāvājuma rindas informāciju, atlasiet **Jauna piedāvājuma rindas informācija** apakšrežģī **Piedāvājuma rindas informācija**. Tiks atvērts ātrās izveides slīdnis. Tabulā ir sniegta detalizēta informācija par laukiem lapā **Piedāvājuma rindas informācija** un to, kā vērtības ietekmē funkcionalitāti.

| **Lauks** | **Atrašanās vieta** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Apraksts | Ātrā izveide | Konkrētā aprēķina apraksts. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Darījuma klase | Ātrā izveide | Šajā nolaižamajā sarakstā ir ietvertas projekta piedāvājuma rindas cilnē **Vispārīgi** iekļautās transakciju klases.  | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Atlasīt produktu | Ātrā izveide | Attiecas, ja transakcijas klase ir **Materiāls**. Varat norādīt, vai šī novērtējuma rinda ir **esošam** (kataloga) produktam vai **ierakstāmam** produktam. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Produkts | Ātrā izveide | Produkta ID no produktu kataloga. Šis lauks tiek iespējots tikai tad, ja laukā **Atlasīt produktu** tiek atlasīts **Esošs produkts**. ID tiek izmantots, lai izgūtu pārdošanas cenu no projekta cenrāža piedāvājumā. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Ierakstāmais produkts | Ātrā izveide | Tekstlodziņš, ko rakstīt produkta nosaukumā. Šis lauks tiek iespējots tikai tad, ja laukā **Atlasīt produktu** tiek atlasīts **Ierakstāms produkts**.| Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Loma | Ātrā izveide | Tās personas loma, kas veiks šo darbu vai radīs šīs izmaksas. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Kategorija | Ātrā izveide | Darba vai izdevumu kategorija. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Sākuma datums | Ātrā izveide | Darba sākuma datums. | Šis lauks pēc noklusējuma tiek aizpildīts ar izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Beigu datums | Ātrā izveide | Darba beigu datums. | Šis lauks pēc noklusējuma tiek aizpildīts ar izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Resursu vienība | Ātrā izveide | Atkārtota vienība, kas radīs šīs izmaksas un nodrošinās resursu, ar kuru strādāt. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski un lietota izmaksu izgūšanai. |
| Vienības grafiks | Ātrā izveide | Darba, produkta vai izdevumu vienību grupa. Vienības pieder vienību grafikam vai vienību grupai. Piemēram, jūdzes un kilometri pieder vienību grupai, kas norāda attālumu. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Vienība | Ātrā izveide | Darba, produkta vai izdevumu vienība. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Daudzums | Ātrā izveide | Darba, produkta vai izdevumu apjoms. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Vienības cena | Ātrā izveide |Tās lomas rēķina likme, kas veic darbu, produkta vienības cena vai produkta vai izdevumu kategorijas pārdošanas cena. Šis lauks pēc noklusējuma tiek iestatīts kā **Laiks**, pamatojoties uz cenu dimensiju vērtībām projekta cenu saraksta lomu cenu rindā, kas ir spēkā sākuma datumā. Attiecībā uz **izdevumiem** noklusējuma vērtība ir ņemta no cenas, kas ir iestatīta darījuma kategorijai projekta cenrādī, kas ir spēkā sākuma datumam. Ja transakciju kategorijas cenu noteikšanas metode nav cena par vienību, netiek izmantota noklusējuma vērtība un šis lauks tiek atstāts tukšs. Produktiem noklusējuma vērtības pamatā ir rinda **Cenrāža elements** projekta cenrādī, kas ir spēkā sākuma datumā.| Darba veiceja lomas izmaksu likme vai izmaksas par vienību izdevumu kategorijā, vai produkta vienības izmaksas. Šis lauks pēc noklusējuma tiek iestatīts kā **Laiks**, pamatojoties uz cenu dimensiju vērtībām projekta cenu saraksta lomu cenu rindā, kas ir spēkā sākuma datumā. Attiecībā uz **izdevumiem** noklusējuma vērtība ir ņemta no cenas, kas ir iestatīta darījuma kategorijai projekta cenrādī, kas ir spēkā sākuma datumam. Ja transakciju kategorijas cenu noteikšanas metode nav cena par vienību, netiek izmantota noklusējuma vērtība un šis lauks tiek atstāts tukšs. Produktiem noklusējuma vērtības pamatā ir rinda **Cenrāža elements** projekta cenrādī, kas ir spēkā sākuma datumā.|
| Aprēķinātais nodoklis | Ātrā izveide | Varat manuāli ievadīt šī darba vai izdevumu aprēķināto nodokli. | Šim laukam nav lejupstraumes ietekmes. |
| Apjoms | Ātrā izveide | Ja lauki **Daudzums** un **Cena** ir atstāti tukši, šajā laukā varat ievadīt informāciju manuāli. Ja šie lauki nav tukši, šis lauks kļūst tikai lasāms un tiek aprēķināts kā (Daudzums \* Vienības cena) + Nodoklis. | Šim laukam nav lejupstraumes ietekmes. |


## <a name="update-prices-on-quote-line-details"></a>Cenas atjaunināšana piedāvājuma rindas informācijā

Ja piedāvājumam pievienotajā projekta cenrādis vai līguma slēgšanas vienības izmaksu cenrādis ir mainījis cenas, lapā **Piedāvājums** varat atlasīt **Pārrēķināt**, lai atsvaidzinātu atsevišķas piedāvājuma rindas detalizēto informāciju, lai atspoguļotu šīs izmaiņas. Atlasot  **Pārrēķināt**, tiek parādīts brīdinājums, ka tiks atiestatītas piedāvājumu rindu detalizētas cenas visām šī piedāvājuma rindām. Atlasiet **Jā**, lai atsvaidzinātu cenas gan pārdošanas, gan izmaksu piedāvājuma rindas informācijā.

## <a name="access-quote-line-details-for-cost"></a>Piekļuve piedāvājuma rindas informācijai attiecībā uz izmaksām

Cilnē **Piedāvājuma rindas informācija** atlasiet režģa rindu, lai iespējotu dažas darbības apakšrežģa rīkjoslā. Ja atlasāt piedāvājuma rindas informāciju, pirmā darbība apakšrežģa rīkjoslā ir **Atvērt izmaksu informāciju**. Atlasiet vienumu **Atvērt izmaksu informāciju**, lai skatītu šīs piedāvājuma rindas saistīto izmaksu likmi un summu.

> [!NOTE]
> Mainot piedāvājuma rindas informācijas resursu vienības, daudzuma, datumu, lomas vai kategorijas vērtības attiecībā uz izmaksām, tiek mainītas arī atbilstošās vērtības piedāvājuma rindas informācijā par pārdošanu.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valūta piedāvājuma rindas informācijā attiecībā uz izmaksām un pārdošanu

Valūta piedāvājuma rindas informācijā attiecībā uz pārdošanas noklusējuma vērtībām no projekta cenrāža, kas ir spēkā piedāvājuma rindas informācijas sākuma datumā.

Valūta piedāvājuma rindas informācijā attiecībā uz izmaksu noklusējuma vērtībām no piedāvājuma līgumslēdzēja vienības cenrāža, kas ir spēkā piedāvājuma rindas informācijas par izmaksām sākuma datumā.

Rentabilitātes aprēķinos summas par piedāvājumu rindu informāciju attiecībā uz izmaksām un pārdošanas apjomiem tiek konvertētas attiecīgās vides pamata valūtā, lai sniegtu atskaiti par piedāvājuma prognozēto peļņu.

> [PIEZĪME
> > Valūtas noapaļošanas kļūdas un mainīti uzcenojumi var rasties, jo trūkst spēkā stāšanās datuma valūtas kursu. Izmantojiet šos aprēķinus tikai projekta līgumos, jo tie ir aptuveni un nav paredzēti faktiskiem statūtu vai citu veidu pārskatiem, kuriem nepieciešama augstāka noapaļošanas precizitāte un datuma precizitāte valūtas maiņas kursiem.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
