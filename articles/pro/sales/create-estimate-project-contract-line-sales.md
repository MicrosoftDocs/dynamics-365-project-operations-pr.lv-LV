---
title: Projekta līguma rindas aprēķini — Lite
description: Šajā tēmā ir sniegta informācija par aprēķiniem, pamatojoties uz projekta līguma rindu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 186b982ee440576e10cf5b78922848b8877afd51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273546"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Projekta līguma rindas aprēķini — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Līdzeklī Dynamics 365 Project Operations projekta līguma rindā ir detalizēta informācija, kas palīdz novērtēt attiecīgā darba izmaksas un iespējamos ieņēmumus, lai izpildītu līguma rindu.

Lai aprēķinātu projekta līguma rindu, skatiet cilni **Līguma rindas informācija**, kas atrodas projekta **Līguma rindā**.  Ir divi veidi, kā aprēķināt projekta līguma rindu.

   - Izveidojiet aprēķinu tieši līguma rindā, manuāli pievienojot detalizētu līguma rindas informāciju.
   - Izveidojiet projektu un projekta plānu un pēc tam saistiet projektu un uzdevumus ar projekta līguma rindu. Tas iespējo procesu, ar kuru līguma rindā var importēt projekta plāna aprēķinu, pamatojoties uz līguma rindā iekļautajiem komponentiem.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Aprēķinu izveide tieši projekta līguma rindā

1. Atveriet līguma rindu un atlasiet cilni **Līguma rindas informācija**. Šajā cilnē izveidotās rindas tiek summētas un rādītas kā šīs **Līguma rindas** **Līguma vērtība**. 
2. **Līguma rindas informācijas** apakšrežģī atlasiet **+ Jauna līguma rindas informācija**. Tiek atvērts ātrās izveidošanas slīdnis. **Līguma rindas informācijas** veidlapā ir pieejami tālāk norādītie lauki.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| **Apraksts** | **Ātrā izveide** | Konkrētā aprēķina apraksts. | Šis lauks pēc noklusējuma ir izveidots ar to saistīto līguma rindu informāciju, kas attiecas uz automātiski izveidotajām izmaksām. |
| **Darījuma klase** | **Ātrā izveide** | Šis nolaižamais saraksts ir to darījumu klašu saraksts, kas iekļautas projekta līguma rindas cilnē **Vispārīgi**. | Šis lauks pēc noklusējuma ir izveidots ar to saistīto līguma rindu informāciju, kas attiecas uz automātiski izveidotajām izmaksām. |
| **Loma** | **Ātrā izveide** | Tās personas loma, kas veic šo darbu vai sedz šos izdevumus. | Šis lauks pēc noklusējuma ir izveidots ar to saistīto līguma rindu informāciju, kas attiecas uz automātiski izveidotajām izmaksām. |
| **Kategorija** | **Ātrā izveide** | Darba vai izdevumu kategorija. | Šis lauks pēc noklusējuma ir izveidots ar to saistīto līguma rindu informāciju, kas attiecas uz automātiski izveidotajām izmaksām. |
| **Sākuma datums** | **Ātrā izveide** | Darba sākuma datums. | Šis lauks pēc noklusējuma ir izveidots ar to saistīto līguma rindu informāciju, kas attiecas uz automātiski izveidotajām izmaksām. |
| **Beigu datums** | **Ātrā izveide** | Darba beigu datums. | Šis lauks pēc noklusējuma ir izveidots ar to saistīto līguma rindu informāciju, kas attiecas uz automātiski izveidoto izmaksu. |
| **Resursu vienība** | **Ātrā izveide** | Resursu plānošanas vienība, kas rodas, izmaksājot un sniedzot resursu, lai strādātu ar to. | Šis lauks pēc noklusējuma ir izveidots ar to saistīto līguma rindu informāciju, kas attiecas uz automātiski izveidotajām izmaksām. Šo lauku izmanto arī izmaksu izgūšanai. |
| **Vienības grafiks** | **Ātrā izveide** | Darba vai izdevumu vienību grupa. Vienības pieder vienību grafikam vai vienību grupai. Piemēram, *jūdzes* un *kilometri (km)* pieder vienību grupai, kas norāda attālumu. | Šis lauks pēc noklusējuma ir izveidots ar to saistīto līguma rindu informāciju, kas attiecas uz automātiski izveidotajām izmaksām. |
| **Vienība** | **Ātrā izveide** | Darba vai izdevumu vienība. | Šis lauks pēc noklusējuma ir izveidots ar to saistīto līguma rindu informāciju, kas attiecas uz automātiski izveidotajām izmaksām. |
| **Daudzums** | **Ātrā izveide** | Darba vai izdevumu daudzums. | Šis lauks pēc noklusējuma ir izveidots ar to saistīto līguma rindu informāciju, kas attiecas uz automātiski izveidotajām izmaksām. |
| **Vienības cena** | **Ātrā izveide** | Tās lomas rēķina likme, kas veic darbu, vai izdevumu kategorijas pārdošanas cena. Šis lauks ir noklusējuma **Laiks**, pamatojoties uz lomu un resursu plānošanas vienību kombināciju projekta cenrādī, kas ir spēkā sākuma datumā. Attiecībā uz izdevumiem šī lauka noklusējuma vērtība ir ņemta no cenas, kas ir iestatīta darījuma kategorijai projekta cenrādī, kas ir spēkā sākuma datumam. Ja darījumu kategorijas cenu noteikšanas metode nav **cena par vienību**, noklusējuma vērtības nav un šis lauks tiek atstāts tukšs. | Tās lomas izmaksu likme, kas veic darbu, vai izdevumu kategorijas izmaksas par vienību. Šis lauks pēc noklusējuma ir **Laiks, pamatojoties uz lomu** un resursu vienības kombināciju lomu cenu rindā izmaksu cenrādī, kas pievienots līgumslēdzējai vienībai, kas ir spēkā sākuma datumā. Attiecībā uz izdevumiem šī lauka noklusējuma vērtība ir balstīta uz kategorijas cenu rindu, kas pievienota darījuma kategorijai projekta cenrādī, kas ir spēkā sākuma datumam. Ja darījumu kategorijas cenu noteikšanas metode nav cena par vienību, noklusējuma vērtības nav un šis lauks tiek atstāts tukšs. |
| **Aprēķinātais nodoklis** | **Ātrā izveide** | Paredzamais nodoklis par šo darbu vai izdevumiem, ko lietotājs ievada. | Paredzamais nodoklis par šo darbu vai izdevumiem, ko lietotājs ievada. |
| **Summa** | **Ātrā izveide** | Šī lauka vērtību var pievienot lietotājs, ja lauki **Daudzums** un **Cena** tiek atstāti tukši. Ja lauki **Daudzums** un **Cena** ir aizpildīti, lauks **Summa** ir tikai lasāms un tiek aprēķināts kā **(daudzums \*vienības cena) + nodoklis**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Cenas atjaunināšana līguma rindas informācijā

Ja tiek mainītas cenas projekta cenrādi, kas ir pievienots līgumam vai līgumslēdzējas vienības izmaksu cenrādim, var atsvaidzināt atsevišķas līguma rindas informācijas cenas, lai atspoguļotu izmaiņas. Lapā **Līgums** atlasiet **Pārrēķināt**. Tiek atvērts brīdinājums, lai informētu, ka visām līguma rindām šajā līgumā tiek atiestatītas cenas. Atlasiet **Jā**, lai atsvaidzinātu cenas gan pārdošanas, gan izmaksu līgumu rindu informācijā.

## <a name="access-contract-line-details-for-cost"></a>Piekļuve līgumu rindu informācijai par izmaksām

Cilnē **Līguma rindas informācija** atlasiet režģa rindu, lai parādītu darbības apakšrežģa rīkjoslā. Pirmā darbība apakšrežģa rīkjoslā ir **Atvērt izmaksu informāciju**. Lai skatītu saistītās izmaksu likmes un summu šajā līguma rindu informācijā, atlasiet opciju **Atvērt izmaksu informāciju**. 

> [!NOTE]
> Ja tiek mainītas resursu uzņēmuma, resursu vienības, daudzuma, datumu, lomas vai kategorijas vērtības, kas atrodas **Izmaksu** līguma rindas informācijā, tiek mainītas arī attiecīgās vērtības līguma rindas informācijā **Pārdošanai**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valūta līguma rindas informācijā izmaksām un pārdošanai

Līguma rindu informācija **Pārdošanai** iestata noklusējuma valūtu no projekta cenrāža, kas ir spēkā līguma rindu informācijas sākuma datumam.

Līguma rindu informācija **Izmaksām** iestata noklusējuma valūtu no līgumslēdzēja līguma cenrāža, kas ir spēkā līguma rindu informācijas sākuma datumam **Izmaksām**.

Peļņas aprēķini aprēķina summas par līguma rindu detalizētu informāciju **Izmaksām** un **Pārdošanai** vides bāzes valūtā, lai ziņotu par līguma kopējiem faktiskajiem un prognozējamajiem uzcenojumiem.

> [!NOTE]
> Valūtas noapaļošanas kļūdas un mainīti uzcenojumi var rasties, jo trūkst spēkā stāšanās datuma valūtas kursu. Izmantojiet šos aprēķinus projekta līgumos tikai kā tuvinājumus, nevis kā faktiskos likumā paredzētos vai citus atskaišu veidošanas pasākumus, kam nepieciešama noapaļošanas precizitāte un datums, kurā jāinformē par valūtas maiņas kursiem.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]