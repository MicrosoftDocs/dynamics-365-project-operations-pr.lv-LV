---
title: Projekta balstīta līguma rindas aprēķins
description: Šajā rakstā ir sniegta informācija par aprēķiniem projekta piedāvājuma rindā.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 633ad3130a28d75ad10b81e03a883e0a732b1ba8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825206"
---
# <a name="estimate-a-project-based-contract-line"></a>Projekta balstīta līguma rindas aprēķins

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_ 

Līdzeklī Dynamics 365 Project Operations projekta līguma rindā ir detalizēta informācija, kas palīdz novērtēt attiecīgā darba izmaksas un iespējamos ieņēmumus, lai izpildītu līguma rindu.

Lai aprēķinātu projekta līguma rindu, skatiet cilni **Līguma rindas informācija**, kas atrodas projekta **Līguma rindā**.  Ir divi veidi, kā aprēķināt projekta līguma rindu.

   - Izveidojiet aprēķinu tieši līguma rindā, manuāli pievienojot detalizētu līguma rindas informāciju.
   - Izveidojiet projektu un projekta plānu un pēc tam saistiet projektu un uzdevumus ar projekta līguma rindu. Tas iespējo procesu, ar kuru līguma rindā var importēt projekta plāna aprēķinu, pamatojoties uz līguma rindā iekļautajiem komponentiem.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Aprēķina izveide tiesi projekta līguma rindā

Lai aprēķinu izveidotu tieši projekta līguma rindā, veiciet šīs darbības:

1. Atveriet līguma rindu un atlasiet cilni **Līguma rindas informācija**. Šajā cilnē izveidotās rindas tiek summētas un rādītas kā šīs **Līguma rindas** **Līguma vērtība**. 
2. Apakšrežģī **Līguma rindas informācija** atlasiet **Jauna līguma rindas informācija**. Tiek atvērts ātrās izveidošanas slīdnis. Lapā **Līguma rindas informācija** ir pieejami tālāk norādītie lauki.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| **Apraksts** | **Ātrā izveide** | Konkrētā aprēķina apraksts. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski. |
| **Transakcijas klase** | **Ātrā izveide** | Šis ir projekta līguma rindas cilnē **Vispārīgi** ietverts transakciju klašu saraksts. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski. |
| **Atlasīt produktu** | **Ātrā izveide** | Attiecas, ja transakcijas klase ir **Materiāls**. Varat norādīt, vai šī novērtējuma rinda ir **esošam** (kataloga) produktam vai **ierakstāmam** produktam. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski. |
| **Produkts** | **Ātrā izveide** | Produkta ID no produktu kataloga. Šis lauks tiek iespējots tikai tad, ja laukā **Atlasīt produktu** tiek atlasīts **Esošs produkts**. ID tiek izmantots, lai izgūtu pārdošanas cenu no projekta cenrāža līgumā. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski. |
| **Ierakstāmais produkts** | **Ātrā izveide** | Teksta lauks, ko rakstīt produkta nosaukumā. Šis lauks tiek iespējots tikai tad, ja laukā **Atlasīt produktu** tiek atlasīts **Ierakstāms produkts**.| Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski. |
| **Loma** | **Ātrā izveide** | Tās personas loma, kas veic šo darbu vai sedz šos izdevumus. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski.|
| **Kategorija** | **Ātrā izveide** | Darba vai izdevumu kategorija. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski.|
| **Sākuma datums** | **Ātrā izveide** | Darba sākuma datums. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski. |
| **Beigu datums** | **Ātrā izveide** | Darba beigu datums. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski. |
| **Resursu uzņēmums** | **Ātrā izveide** | Resursu uzņēmums vai juridiska persona, kas uzkrāj šīs izmaksas un nodrošina resursu, ar kuru strādāt. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski un lietota izmaksu izgūšanai. |
| **Resursu vienība** | **Ātrā izveide** | Atkārtota vienība, kas rodas no izmaksām un nodrošina resursu, ar kuru strādāt. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski un lietota izmaksu izgūšanai. |
| **Vienības grafiks** | **Ātrā izveide** | Darba, produkta vai izdevumu vienību grupa. Vienības pieder vienību grafikam vai vienību grupai. Piemēram, *jūdzes* un *kilometri (km)* pieder vienību grupai, kas norāda attālumu. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski. |
| **Vienība** | **Ātrā izveide** | Darba, produkta vai izdevumu vienība. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski. |
| **Daudzums** | **Ātrā izveide** | Darba, produkta vai izdevumu apjoms. | Šī vērtība pēc noklusējuma tiek mainīta uz saistīto izmaksu līguma rindu, kas tiek izveidota automātiski. |
| **Vienības cena** | **Ātrā izveide** | Tās lomas rēķina likme, kas veic darbu, produkta vienības cena vai produkta vai izdevumu kategorijas pārdošanas cena. Šis lauks pēc noklusējuma tiek iestatīts kā **Laiks**, pamatojoties uz cenu dimensiju vērtībām projekta cenu saraksta lomu cenu rindā, kas ir spēkā sākuma datumā. Attiecībā uz **izdevumiem** šī lauka noklusējuma vērtība ir ņemta no cenas, kas ir iestatīta darījuma kategorijai projekta cenrādī, kas ir spēkā sākuma datumam. Ja darījumu kategorijas cenu noteikšanas metode nav **cena par vienību**, noklusējuma vērtības nav un šis lauks tiek atstāts tukšs. Produktiem šī lauka noklusējuma vērtības pamatā ir rinda **Cenrāža elements** projekta cenrādī, kas ir spēkā sākuma datumā.| Darba veiceja lomas izmaksu likme vai izmaksas par vienību izdevumu kategorijā, vai produkta vienības izmaksas. Šis lauks pēc noklusējuma tiek iestatīts kā **Laiks**, pamatojoties uz cenu dimensiju vērtībām lomas cenrāža rindā, kas ir pievienota līguma vienībai, kas ir spēkā sākuma datumā.  **Izdevumiem** šī lauka noklusējuma vērtības pamatā ir rinda kategorijas cenas rinda cenrādī, kas ir pievienots līguma vienībai, kas ir spēkā sākuma datumā. Ja darījumu kategorijas cenu noteikšanas metode nav cena par vienību, noklusējuma vērtības nav un šis lauks tiek atstāts tukšs. Produktiem šī lauka noklusējuma vērtības pamatā ir rinda **Cenrāža elements** projekta cenrādī, kas ir pievienots līguma vienībai, kas ir spēkā sākuma datumā.|
| **Aprēķinātais nodoklis** | **Ātrā izveide** | Paredzamais nodoklis par šo darbu vai izdevumiem, ko lietotājs ievada. | &nbsp; |
| **Apjoms** | **Ātrā izveide** | Varat pievienot vērtību šajā laukā, ja lauki **Daudzums** un **Cena** ir tukši. Ja lauki **Daudzums** un **Cena** ir aizpildīti, lauks **Summa** ir tikai lasāms un tiek aprēķināts kā **(daudzums \*vienības cena) + nodoklis**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Cenas atjaunināšana līguma rindas informācijā

Ja tiek mainītas cenas projekta cenrādi, kas ir pievienots līgumam vai līgumslēdzējas vienības izmaksu cenrādim, var atsvaidzināt atsevišķas līguma rindas informācijas cenas, lai atspoguļotu izmaiņas. Lapā **Līgums** atlasiet **Pārrēķināt**. Tiek parādīts brīdinājums, ka visu šī līguma rindu cenas tiek atiestatītas. Atlasiet **Jā**, lai atsvaidzinātu cenas gan pārdošanas, gan izmaksu līgumu rindu informācijā.

## <a name="access-contract-line-details-for-cost"></a>Piekļuve līgumu rindu informācijai par izmaksām

Cilnē **Līguma rindas informācija** atlasiet režģa rindu, lai parādītu darbības apakšrežģa rīkjoslā. Pirmā darbība apakšrežģa rīkjoslā ir **Atvērt izmaksu informāciju**. Lai skatītu saistītās izmaksu likmes un summu šajā līguma rindu informācijā, atlasiet opciju **Atvērt izmaksu informāciju**. 

> [!NOTE]
> Ja tiek mainītas resursu uzņēmuma, resursu vienības, daudzuma, datumu, lomas vai kategorijas vērtības, kas atrodas **Izmaksu** līguma rindas informācijā, tiek mainītas arī attiecīgās vērtības līguma rindas informācijā **Pārdošanai**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valūta līguma rindas informācijā izmaksām un pārdošanai

Līguma rindu informācija **Pārdošanai** iestata noklusējuma valūtu no projekta cenrāža, kas ir spēkā līguma rindu informācijas sākuma datumam.

Līguma rindu informācija **Izmaksām** iestata noklusējuma valūtu no līgumslēdzēja līguma cenrāža, kas ir spēkā līguma rindu informācijas sākuma datumam **Izmaksām**.

Peļņas aprēķini aprēķina summas par līguma rindu detalizētu informāciju **Izmaksām** un **Pārdošanai** vides bāzes valūtā, lai ziņotu par līguma kopējiem faktiskajiem un prognozējamajiem uzcenojumiem.

> [!NOTE]
> Valūtas noapaļošanas kļūdas un mainīti uzcenojumi var rasties, jo trūkst spēkā stāšanās datuma valūtas kursu. Izmantojiet šos aprēķinus tikai projekta līgumos, jo tie ir aptuveni un nav paredzēti faktiskiem statūtu vai citu veidu pārskatiem, kuriem nepieciešama augstāka noapaļošanas precizitāte un datuma precizitāte valūtas maiņas kursiem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
