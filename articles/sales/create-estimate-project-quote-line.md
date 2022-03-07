---
title: Projekta piedāvājuma rindas aprēķins
description: Šajā tēmā ir sniegta informācija par aprēķina izveidi projekta piedāvājuma rindā.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: adb5a7f113b15abd2fe7364fa9b592d2c02db389
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000715"
---
# <a name="estimate-a-project-quote-line"></a>Projekta piedāvājuma rindas aprēķins

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Projekta piedāvājuma rindā ir informācija, kas palīdz aprēķināt attiecīgā darba izmaksas un iespējamos ieņēmumus, lai izpildītu piedāvājuma rindu.

Lai novērtētu projekta piedāvājuma rindu, piedāvājuma rindā atlasiet cilni **Piedāvājuma rindas informācija**. Ir divi veidi, kā izveidot novērtējumu projekta piedāvājuma rindai.

   - Novērtējuma manuāla izveide tieši piedāvājuma rindā, izmantojot piedāvājuma rindas informāciju. 
   - Izveidojiet projektu un projekta plānu un pēc tam saistiet projektu un projekta uzdevumus ar piedāvājuma rindu. Tiek iespējots process, kurā projekta plānā ietvertie aprēķini tiek importēti piedāvājuma rindā, pamatojoties uz jūsu sniegto informāciju.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Aprēķinu izveide tieši projekta piedāvājuma rindā

Lai novērtējumu izveidotu tieši projekta piedāvajuma rindā, veiciet šīs darbības:

1. Lai izveidotu aprēķinu projekta piedāvājuma rindā, atlasiet cilni **Piedāvājuma rindas informācija** . Rindas elements, ko izveidojat šajā cilnē, apkopo šīs piedāvājuma rindas aprēķināto vērtību. 
2. Lai izveidotu piedāvājuma rindas informāciju, atlasiet **Jauna piedāvājuma rindas informācija** apakšrežģī **Piedāvājuma rindas informācija**. Tiks atvērts ātrās izveides slīdnis. Lapā **Piedāvājuma rinda** ir tālāk minētie lauki.

| **Lauks** | **Atrašanās vieta** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Apraksts | Ātrā izveide | Konkrētā aprēķina apraksts. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Darījuma klase | Ātrā izveide | Šis nolaižamais saraksts nodrošina darījumu klases, kas ir ietvertas projekta piedāvājuma rindas cilnē **Vispārīgi**.  | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Atlasīt produktu | Ātrā izveide | Attiecas, ja transakcijas klase ir **Materiāls**. Varat norādīt, vai šī novērtējuma rinda ir **esošam** (kataloga) produktam vai **ierakstāmam** produktam. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Produkts | Ātrā izveide | Produkta ID no produktu kataloga. Šis lauks tiek iespējots tikai tad, ja laukā **Atlasīt produktu** tiek atlasīts **Esošs produkts**. ID tiek izmantots, lai izgūtu pārdošanas cenu no projekta cenrāža piedāvājumā. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Ierakstāmais produkts | Ātrā izveide | Tekstlodziņš, ko rakstīt produkta nosaukumā. Šis lauks tiek iespējots tikai tad, ja laukā **Atlasīt produktu** tiek atlasīts **Ierakstāms produkts**.| Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Loma | Ātrā izveide | Tās personas loma, kas veiks šo darbu vai radīs šīs izmaksas. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Kategorija | Ātrā izveide | Darba vai izdevumu kategorija. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Sākuma datums | Ātrā izveide | Darba sākuma datums. | Šis lauks pēc noklusējuma tiek aizpildīts ar izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Beigu datums | Ātrā izveide | Darba beigu datums. | Šis lauks pēc noklusējuma tiek aizpildīts ar izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Resursu uzņēmums | Ātrā izveide | Resursu uzņēmums vai juridiska persona, kas uzkrāj šīs izmaksas un nodrošina resursu, ar kuru strādāt. | Vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski un lietota izmaksu izgūšanai. |
| Resursu vienība | Ātrā izveide | Atkārtota vienība, kas rodas no izmaksām un nodrošina resursu, ar kuru strādāt. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski un lietota izmaksu izgūšanai. |
| Vienības grafiks | Ātrā izveide | Darba, produkta vai izdevumu vienību grupa. Vienības pieder vienību grafikam vai vienību grupai. Piemēram, jūdzes un kilometri pieder vienību grupai, kas norāda attālumu. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Vienība | Ātrā izveide | Darba, produkta vai izdevumu vienība. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Daudzums | Ātrā izveide | Darba, produkta vai izdevumu apjoms. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu piedāvajuma rindu, kas tiek izveidota automātiski. |
| Vienības cena | Ātrā izveide |Tās lomas rēķina likme, kas veic darbu, produkta vienības cena vai produkta vai izdevumu kategorijas pārdošanas cena. Šis lauks pēc noklusējuma tiek iestatīts kā **Laiks**, pamatojoties uz cenu dimensiju vērtībām projekta cenu saraksta lomu cenu rindā, kas ir spēkā sākuma datumā. Attiecībā uz **izdevumiem** noklusējuma vērtība ir ņemta no cenas, kas ir iestatīta darījuma kategorijai projekta cenrādī, kas ir spēkā sākuma datumam. Ja darījumu kategorijas cenu noteikšanas metode nav cena par vienību, noklusējuma vērtības nav un šis lauks tiek atstāts tukšs. Produktiem šī lauka noklusējuma vērtības pamatā ir rinda **Cenrāža elements** projekta cenrādī, kas ir spēkā sākuma datumā.| Darba veiceja lomas izmaksu likme vai izmaksas par vienību izdevumu kategorijā, vai produkta vienības izmaksas. Šis lauks pēc noklusējuma tiek iestatīts kā **Laiks**, pamatojoties uz cenu dimensiju vērtībām lomas cenrāža rindā, kas ir pievienota līguma vienībai, kas ir spēkā sākuma datumā. Izdevumiem šī lauka noklusējuma vērtības pamatā ir rinda kategorijas cenas rinda cenrādī, kas ir pievienots līguma vienībai, kas ir spēkā sākuma datumā. Ja transakciju kategorijas cenu noteikšanas metode nav cena par vienību, netiek izmantota noklusējuma vērtība un šis lauks tiek atstāts tukšs. Produktiem šī lauka noklusējuma vērtības pamatā ir rinda **Cenrāža elements** projekta cenrādī, kas ir pievienots līguma vienībai, kas ir spēkā sākuma datumā.|
| Aprēķinātais nodoklis | Ātrā izveide | Varat manuāli ievadīt šī darba vai izdevumu aprēķināto nodokli. | Šim laukam nav lejupstraumes ietekmes. |
| Apjoms | Ātrā izveide | Ja lauki **Daudzums** un **Cena** ir atstāti tukši, šajā laukā varat ievadīt informāciju manuāli. Ja šie lauki nav tukši, šis lauks kļūst tikai lasāms un tiek aprēķināts kā (Daudzums \* Vienības cena) + Nodoklis. | Šim laukam nav lejupstraumes ietekmes. |

## <a name="update-prices-on-quote-line-details"></a>Cenas atjaunināšana piedāvājuma rindas informācijā

Ja esat mainījis cenas projekta cenrādī, kas ir pievienots piedāvājumam, vai līgumslēdzēja vienības izmaksu cenrādī, varat atlasīt vienumu **Pārrēķināt** lapā **Piedāvājums**, lai atsvaidzinātu atsevišķas piedāvājuma rindas informācijas cenas un atspoguļotu veiktās izmaiņas. Atlasot  **Pārrēķināt**, tiek parādīts brīdinājums, ka tiks atiestatītas piedāvājumu rindu detalizētas cenas visām šī piedāvājuma rindām. Atlasiet **Jā**, lai atsvaidzinātu cenas gan pārdošanas, gan izmaksu piedāvājuma rindas informācijā.

## <a name="access-quote-line-details-for-cost"></a>Piekļuve piedāvājuma rindas informācijai attiecībā uz izmaksām

Lai piekļūtu piedāvājuma rindas detalizētai informācijai par izmaksām, veiciet šīs darbības:

1. Cilnē **Piedāvājuma rindas informācija** atlasiet rindu režģī, lai iespējotu darbības apakšrežģa rīkjoslā. 
2. Atlasiet vienumu **Atvērt izmaksu informāciju**, lai skatītu šīs piedāvājuma rindas saistīto izmaksu likmi un summu.

> [!NOTE]
> Mainot piedāvājuma rindas informācijas resursu vienības, daudzuma, datumu, lomas vai kategorijas vērtības attiecībā uz izmaksām, tiek mainītas arī atbilstošās vērtības piedāvājuma rindas informācijā par pārdošanu.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valūta piedāvājuma rindas informācijā attiecībā uz izmaksām un pārdošanu

Piedāvājuma rindas informācija par pārdošanas noklusējuma valūtu no projekta cenrāža, kas ir spēkā piedāvājuma rindas detalizētas informācijas sākuma datumā.

Valūtai piedāvājuma rindas informācijā par izmaksām pēc noklusējuma ir vērtība no līguma vienības cenrāža piedāvājumam, kas ir spēkā cenas piedāvājuma rindas informācijas sākuma datumā.

> [!NOTE]
> Rentabilitātes aprēķinos summas par piedāvājumu rindu informāciju attiecībā uz izmaksām un pārdošanas apjomiem tiek konvertētas attiecīgās vides pamata valūtā, lai sniegtu atskaiti par piedāvājuma prognozēto peļņu. Valūtas noapaļošanas kļūdas un mainīti uzcenojumi var rasties, jo trūkst spēkā stāšanās datuma valūtas kursu. Izmantojiet šos aprēķinus tikai projekta piedāvājumos, jo tie ir aptuveni un nav paredzēti faktiskiem statūtu vai citu veidu pārskatiem, kuriem nepieciešama augstāka noapaļošanas precizitāte un datuma precizitāte valūtas maiņas kursiem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
