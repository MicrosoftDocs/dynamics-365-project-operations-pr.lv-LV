---
title: Pārvaldīt pro formas rēķinu — Lite
description: Šajā tēmā ir sniegta informācija par darbu ar pro formas rēķiniem.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ca6c2cc8855cfed592057ca129b436450104af99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274053"
---
# <a name="manage-a-proforma-invoice---lite"></a>Pārvaldīt pro formas rēķinu — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Risinājumā Dynamics 365 Project Operations pro forma rēķini tiek veidoti kā Dynamics 365 Sales rēķinu paplašinājums. Tomēr rēķinu izrakstīšanas procesā ir daudz atšķirību starp risinājumiem Sales un Project Operations, runājot par rēķinu izrakstīšanu. Piemēram, risinājumā Project Operations nav iespējams izveidot jaunu rēķinu no lapas **Rēķinu saraksts**, bet to var izdarīt risinājumā Sales. Šīs atšķirības un paplašinājumi ir ieviesti, lai atbalstītu rēķinu izrakstīšanas procesus projektiem, kas atšķiras no parasta pārdošanas pasūtījuma rēķina.

> [!IMPORTANT]
> Šo atšķirību dēļ neaizstājiet savā starpā rēķinus risinājumos Sales un Project Operations.

## <a name="invoice-header"></a>Rēķina galvene

Šī informācija ir pieejama pro forma rēķina galvenē programmā Project Operations.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| **Rēķina ID** | Cilne **Kopsavilkums** | ID, kas tiek ģenerēts automātiski, izveidojot pro formas rēķinu. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Šis lauks tiek izmantots kā atsauce katram pro formas rēķinam. |
| **Nosaukums** | Cilne **Kopsavilkums** | Pēc noklusējuma iestatīts uz projekta līguma nosaukumu. Šo lauku var rediģēt lietotājs. | &nbsp;  |
| **Valūta** | Cilne **Kopsavilkums** | Pēc noklusējuma iestatīts uz projekta līguma valūtu. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |&nbsp; |
| **Cenrādis** | Cilne **Kopsavilkums** | Pēc noklusējuma iestatīts uz projekta cenrādi. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Iespēja** | Cilne **Kopsavilkums** | Atsauce uz saistīto iespēju. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp;  |
| **Līgums** | Cilne **Kopsavilkums** | Atsauce uz saistīto projekta līgumu. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Klients** | Cilne **Kopsavilkums** | Atsauce uz saistīto projekta līgumu. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |&nbsp;  |
| **Apraksts** | Cilne **Kopsavilkums** | Teksta lauks, kas apraksta rēķinu. Šo lauku var rediģēt lietotājs. | &nbsp; |
| **Rēķina saņēmējs** un ar to saistītie lauki | **Kopsavilkuma cilne** | Noklusējuma vērtība ir iestatīta no projekta līguma klienta. Šo lauku var rediģēt lietotājs.  | &nbsp; |
| **Statuss** | Cilne **Kopsavilkums** | Iestata šādas opcijas: **Aktīvs**, **Slēgts**, **Apmaksāts** un **Atcelts**, un to var rediģēt lietotājs. | Project Operations neatbalstītie statusi ir **Slēgts** un **Atcelts**. </br> Kad rēķins ir izveidots, statuss tiek iestatīts uz **Aktīvs**. </br>Tikai pēc rēķina apstiprināšanas statusam ir jābūt iestatītam uz **Apmaksāts**. |
| **Projekta rēķina statuss** | Cilne **Kopsavilkums** | Iestata šādas opcijas: **Melnraksts**, **Pārskatīšanā** un **Apstiprināts**, un to var rediģēt lietotājs. | Gan statusā **Melnraksts**, gan **Pārskatīšanā** rēķinu var rediģēt. Rēķinu nevar rediģēt pēc tā apstiprināšanas. |
| **Detalizēta summa** | Cilne **Kopsavilkums** | Visās rēķina rindās esošo apjomu summa pēc avansiem un atskaitījumiem. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Šo lauku izmanto, lai aprēķinātu galīgo summu. |
| **Atlaide (%)** | Cilne **Kopsavilkums** | Šo lauku var rediģēt, lai ievadītu atlaidi procentos. Project Operations funkcionalitāte šo lauku neatbalsta. | Tas ir neatbalstīts lauks. |
| **Atlaides summa** | Cilne **Kopsavilkums** | Šo lauku var rediģēt, lai ievadītu atlaides apjomu. Project Operations funkcionalitāte šo lauku neatbalsta. | Tas ir neatbalstīts lauks. |
| **Summa bez piegādes** | **Kopsavilkuma cilne** | Kopējā rēķina summa pēc atlaižu lietošanas. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Šo lauku izmanto, lai aprēķinātu galīgo summu. |
| **Piegādes summa** | Cilne **Kopsavilkums** | Šo lauku var rediģēt, lai ievadītu vedmaksas apjomu. Project Operations funkcionalitāte šo lauku neatbalsta. | Tas ir neatbalstīts lauks. |
| **Nodokļu kopsumma** | Cilne **Kopsavilkums** | Kopējais nodoklis no visām rēķina rindām rēķinā. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Nav. |
| **Summa** | Cilne **Kopsavilkums** | Apjoma summa, kas ir pēc atlaidēm un nodokļiem. | Summa ir daudzums, kas klientam ir jāmaksā. |
## <a name="project-based-invoice-lines"></a>Projekta rēķina rindas

Project Operations vienmēr ir viena rēķina rinda katrai projekta līguma rindai. Rēķina rinda tiek izveidota pat tad, ja nav faktisku datu. Šī informācija ir pieejama pro forma rēķina rindā.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| **Rēķina ID** | Cilne **Vispārīgi** | Atsauce uz rēķina ID. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Rēķina ID saiti var izmantot, lai pārietu atpakaļ uz rēķina galveni. |
| **Nosaukums** | Cilne **Vispārīgi** | Rēķina rindas nosaukums, kas pēc noklusējuma ir iestatīts kā līguma rindas nosaukums. Šo lauku var rediģēt lietotājs. | &nbsp; |
| **Project** | Cilne **Vispārīgi** | Projekts saistītajā projekta līguma rindā. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Projekta saiti var izmantot, lai naviģētu uz projektu. |
| **Rēķinu izrakstīšanas metode** | Cilne **Vispārīgi** | Norēķinu metode saistītajā projekta līguma rindā. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Līguma rindas summa** | Cilne **Vispārīgi** | Līguma summa saistītajā projekta līguma rindā. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Iekļauts rēķinā līdz šim datumam** | Cilne **Vispārīgi** | Rēķina apjomu summa visās šī rēķina rindas detaļās. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Summa** | Cilne **Vispārīgi** | Šī rēķina apjomu summa visās rēķinā iekļaujamajās rindas detaļās. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Šo lauku izmanto, lai aprēķinātu galīgo summu rēķina galvenē. |
| **Nodoklis** | Cilne **Vispārīgi** | Rēķina rindas nodokļu summa visās šī rēķina rindas detaļās. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Šo lauku izmanto, lai aprēķinātu galīgo nodokļu summu rēķina galvenē. |
| **Kopējā summa** | Cilne **Vispārīgi** | Rēķina rindas kopējā summa (**Nodoklis + apjoms**) visās šī rēķinā iekļaujamās rindas detaļās. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Šo lauku izmanto, lai aprēķinātu galīgo summu rēķina galvenē. |


## <a name="invoice-line-details"></a>Rēķina rindas informācija

Projekta rēķinā katra rēķina rinda ietver rēķina rindas informāciju. Šī rindas informācija ir saistīta ar rēķinos neiekļautajiem faktiskajiem pārdošanas datiem un atskaites punktiem, kas attiecas uz rēķina rindā ietverto līguma rindu. Visi šie darījumi ir atzīmēti kā **Gatavs rēķina izrakstīšanai**.

Attiecībā uz **Laika un materiālu rēķina** rindu rēķina rindas informācija lapā **Rēķina rinda** ir sagrupēta sadaļās **Rēķinā iekļaujams**, **Rēķinā neiekļaujams** un **Bezmaksas**. **Rēķinā iekļaujamas rēķina rindas** informācija tiek pievienota rēķina rindas kopsummai. **Bezmaksas** un **Rēķinā neiekļaujamie faktiskie apjomi** netiek pievienoti rēķina rindas kopsummai.

Rindai **Fiksētas cenas rēķins** rēķina rindas informācija tiek izveidota no atskaites punktiem, kas ir atzīmēti kā **Gatavi rēķina izrakstīšanai** saistītajā līguma rindā. Pēc tam kad rēķina rindas informācija ir izveidota no atskaites punkta, atskaites punkta norēķinu statuss tiek atjaunināts uz **Klienta rēķins izveidots**.

### <a name="edit-invoice-line-details"></a>Rēķina rindas informācijas rediģēšana

Tālāk norādītie lauki ir pieejami rēķina rindas informācijā, kas ir balstīta uz faktisko rēķinā neiekļauto pārdošanas apjomu.

| Lauks | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- |
| **Rēķina rinda** | Atsauce uz **Rēķina rindas ID**. Tikai lasāms lauks, bloķēts rediģēšanai. | Šo saiti var izmantot, lai pārietu atpakaļ uz rēķina galveni. |
| **Apraksts** | Rēķina rindas informācijas apraksts. Pēc noklusējuma iestatīts no lauka **Iekšējie komentāri** sadaļā **Laika ieraksts** un no lauka **Apraksts** sadaļā **Izdevumu ieraksts**. Lauku var rediģēt lietotājs.| &nbsp; |
| **Ārējais apraksts** | Rēķina rindas informācijas apraksts. Pēc noklusējuma iestatīts no lauka **Ārējie komentāri** sadaļā **Laika ieraksts** un no lauka **Apraksts** sadaļā **Izdevumu ieraksts**. Lauku var rediģēt lietotājs. | Šo aprakstu var izmantot, lai noteiktu, kam jābūt ietvertam drukātajā rēķinā, kas tiks nosūtīts klientam. Risinājumā Project Operations pro forma rēķinam nav visu nepieciešamo funkcionalitāšu, lai konfigurētu rēķina drukāšanas iestatījumus. |
| **Sākuma datums** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Šo lauku var rediģēt jaunā rēķina rindas informācijā, kas nebalstās uz avota faktiskajām vērtībām. |
| **Project** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Pēc noklusējuma iestatīts kā projekts attiecīgajā līguma rindā. |
| **Uzdevums** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Lauku var rediģēt jaunā rēķina rindas informācijā, kas nebalstās uz avota faktiskajām vērtībām. Nolaižamajā sarakstā ir parādīti visi uzdevumi, kas saistīti ar saistīto projekta līguma rindu.  |
| **Transakciju kategorija** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Lauku var rediģēt jaunā rēķina rindas informācijā, kas nebalstās uz avota faktiskajām vērtībām. |
| **Loma** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Lauku var rediģēt jaunā rēķina rindas informācijā, kas nebalstās uz avota faktiskajām vērtībām. |
| **Rezervējamais resurssss** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Lauku var rediģēt jaunā rēķina rindas informācijā, kas nebalstās uz avota faktiskajām vērtībām. |
| **Resursu vienība** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Lauku var rediģēt jaunā rēķina rindas informācijā, kas nebalstās uz avota faktiskajām vērtībām. |
| **Daudzums** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Lauku var rediģēt jaunā rēķina rindas informācijā, kas nebalstās uz avota faktiskajām vērtībām. |
| **Vienības grafiks** | Rēķina rindas informācijai par laiku tas vienmēr tiek iestatīts kā laiks, un to nevar rediģēt. Attiecībā uz izdevumiem tas pēc noklusējuma tiek iestatīts no faktiskajiem avota izdevumiem. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Pēc noklusējuma iestatīts kā **Laiks** jaunā rēķina rindas informācijā, kas nebalstās uz faktiskajām vērtībām. |
| **Vienība** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Lauku var rediģēt jaunā rēķina rindas informācijā, kas nebalstās uz avota faktiskajām vērtībām. |
| **Cenrādis** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Lauku var rediģēt jaunā rēķina rindas informācijā, kas nebalstās uz avota faktiskajām vērtībām. Ja vērtība nav ievadīta, tā pēc noklusējuma tiek iestatīta pēc **Saglabāšanas**. |
| **Valūta** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Noklusējuma vērtība ir rēķina galvene, kad tiek radīta jauna rēķina informācija bez faktisko datu dublēšanas.  Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Summa** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Aprēķināts kā **Daudzums \* Cena**, ja veidojat jaunu rēķina informāciju bez faktisko datu dublēšanas. Tas tiek aprēķināts pēc **Saglabāšanas**. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Nodoklis** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Lauku var rediģēt lietotājs | Lauku var rediģēt lietotājs, izveidojot jaunu rēķina rindas informāciju bez faktisko vērtību dublēšanas. |
| **Kopējā summa** | Aprēķināts lauks, kas aprēķināts kā **Summa + nodoklis**. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Norēķinu tips** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Lauku var rediģēt lietotājs. | Ja tiek atlasīts **Rēķinā iekļaujams**, tiek pievienota rinda rēķina rindas kopsummai. **Bezmaksas** un **Rēķinā neiekļaujams** to izslēgs no rēķina rindas kopsummas. |
| **Transakcijas tips** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Pēc noklusējuma iestatīts kā **Rēķinā iekļautā pārdošana** un bloķēts, izveidojot jaunu **Rēķina rindas informāciju** bez faktisko datu kopēšanas.  |
| **Darījuma klase** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Iestatīts pēc noklusējuma, pamatojoties uz to, vai lietotājs vēlas izveidot **Laika**, **Izdevumu** vai **Maksas** rēķina rindu, vienlaikus izveidojot jaunu **Rēķina rindas informāciju** bez faktisko datu kopēšanas. Bloķēts rediģēšanai. |

Tālāk norādītie lauki ir pieejami rēķina rindas informācijā, kas ir balstīta uz atskaites punktu.

| Lauks | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- |
| **Rēķina rinda** | Atsauce uz **Rēķina rindas ID**. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | Saiti var izmantot, lai pārietu atpakaļ uz rēķina galveni. |
| **Apraksts** | Rēķina rindas informācijas apraksts. Pēc noklusējuma iestatīts avota atskaites punkta aprakstā. | &nbsp; |
|**Ārējais apraksts** | Rēķina rindas informācijas apraksts, kas pēc noklusējuma ir iestatīts no avota atskaites punkta apraksta. | Šo lauku var izmantot, lai noteiktu, kam jābūt ietvertam drukātajā rēķinā, kas tiks nosūtīts klientam. Risinājumā Project Operations pro forma rēķinam nav visu nepieciešamo funkcionalitāšu, lai konfigurētu rēķina drukāšanas iestatījumus. |
| **Sākuma datums** | Pēc noklusējuma iestatīts no **Atskaites punkta** datuma avota atskaites punktā. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Project** | Pēc noklusējuma iestatīts no avota atskaites punkta. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Uzdevums** | Pēc noklusējuma iestatīts no avota atskaites punkta. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Transakciju kategorija** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Loma** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Rezervējamais resurssss** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Resursu vienība** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Vienības grafiks** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Vienība** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Cenrādis** | Pēc noklusējuma iestatīts no avota atskaites punkta summas. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Valūta** | Pēc noklusējuma iestatīts no avota atskaites punkta. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |&nbsp; |
| **Summa** | Pēc noklusējuma iestatīts no avota atskaites punkta summas. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Nodoklis** | Pēc noklusējuma iestatīts no avota atskaites punkta nodokļa summas. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Kopējā summa** | Pēc noklusējuma iestatīts no avota atskaites punkta kopējās summas. Lauku var rediģēt lietotājs | &nbsp; |
| **Norēķinu tips** | Pēc noklusējuma vienmēr iestatīts kā **Rēķinā iekļaujams**. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Transakcijas tips** | Pēc noklusējuma iestatīts no avota atskaites punkta. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |
| **Darījuma klase** | Pēc noklusējuma iestatīts no avota atskaites punkta. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Jaunas rēķina rindas informācijas izveide

Laika un materiālu rēķina rindās var izveidot jaunu rēķina rindas informāciju. Šī rēķina rindas informācija netiek dublēta ar faktisko. Laika un materiālu rēķina rindas rēķina rindā var atlasīt **Jauns**, lai veidotu jaunu rēķina rindas informāciju tām darījumu klasēm, kas ir iekļautas līguma rindā.

## <a name="refresh-invoice-transactions"></a>Rēķina darījuma atsvaidzināšana

Ja jums ir faktiskie dati, kas ienāca pēc rēķina izveidošanas, varat tos iekļaut rēķinā.

1. Skatā **Norēķinu neizpildīto darbību žurnāls** atzīmējiet datus kā **Gatavs rēķina izrakstīšanai**.   
2. Atveriet pro forma rēķina melnrakstu un lentē **Darbības** noklikšķiniet uz **Atsvaidzināt rēķina rindas transakcijas**.

  Šādi tiek izveidota rēķina rindas informācija par visiem faktiskajiem datiem, kas ir iepriekš datēti un atzīmēti kā **Gatavi rēķina izrakstīšanai**, bet rēķinā netiek iekļauti.

## <a name="product-based-invoice-lines"></a>Produkta rēķina rindas

Project Operations var izveidot rēķina rindas produktiem, kas neattiecas uz projektu vai visiem projektiem, kā arī uz projekta rēķina rindām. Šīs rēķinu rindas tiek izveidotas kā uz produktu balstītas līguma rindas, un pēc tam, kad tās ir atzīmētas kā gatavas rēķina izrakstīšanai, tās tiek pievienotas kā produktu rēķinu rindas.

Pēc tam, kad esat pievienojis uz produktu balstītas rēķinu rindas, tās vairs nevar mainīt. Tomēr tās var izdzēst no pro forma rēķina melnraksta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]