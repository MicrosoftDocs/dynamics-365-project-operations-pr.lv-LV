---
title: Pro forma projektā balstīta rēķina pārvaldība
description: Šajā tēmā ir sniegta informācija par projektu pro forma rēķinu pārvaldību un darbu ar tiem.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cba74c14f6d039dce0650f25ee04cbe35ec8f668b774cdaaa3bbf1aab99cb44d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989335"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Pro forma projektā balstīta rēķina pārvaldība

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Risinājumā Dynamics 365 Project Operations pro forma rēķini tiek veidoti kā Dynamics 365 Sales rēķinu paplašinājums. Tomēr rēķinu izrakstīšanas procesā ir daudz atšķirību starp risinājumiem Sales un Project Operations, runājot par rēķinu izrakstīšanu. Piemēram, risinājumā Project Operations nav iespējams izveidot jaunu rēķinu no lapas **Rēķinu saraksts**, bet to var izdarīt risinājumā Sales. Šīs atšķirības un paplašinājumi ir ieviesti, lai atbalstītu rēķinu izrakstīšanas procesus projektiem, kas atšķiras no parasta pārdošanas pasūtījuma rēķina.

> [!IMPORTANT]
> Šo atšķirību dēļ neaizstājiet savā starpā rēķinus risinājumos Sales un Project Operations.

## <a name="invoice-header"></a>Rēķina galvene

Šī informācija ir pieejama pro forma rēķina galvenē programmā Project Operations.

| Lauks | Atrašanās vieta | Apraksts |
| --- | --- | --- | 
| **Rēķina ID** | Cilne **Kopsavilkums** | ID, kas tiek ģenerēts automātiski, izveidojot pro formas rēķinu. Tikai lasāms lauks, kura rediģēšana ir bloķēta. Šis lauks tiek izmantots kā atsauce katram pro formas rēķinam. |
| **Nosaukums** | Cilne **Kopsavilkums** | Pēc noklusējuma iestatīts uz projekta līguma nosaukumu. Šo lauku var rediģēt. | 
| **Valūta** | Cilne **Kopsavilkums** | Pēc noklusējuma iestatīts uz projekta līguma valūtu. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Cenrādis** | Cilne **Kopsavilkums** | Pēc noklusējuma iestatīts uz projekta cenrādi. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Iespēja** | Cilne **Kopsavilkums** | Atsauce uz saistīto iespēju. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Līgums** | Cilne **Kopsavilkums** | Atsauce uz saistīto projekta līgumu. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Klients** | Cilne **Kopsavilkums** | Atsauce uz saistīto projekta līgumu. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Apraksts** | Cilne **Kopsavilkums** | Teksta lauks, kas apraksta rēķinu. Šo lauku var rediģēt. | 
| **Rēķina saņēmējs** un ar to saistītie lauki | **Kopsavilkuma cilne** | Noklusējuma vērtība ir iestatīta no projekta līguma klienta. Šo lauku var rediģēt.  | 
| **Statuss** | Cilne **Kopsavilkums** | Tiek iestatītas šādas opcijas: **Aktīvs**, **Slēgts**, **Samaksāts** un **Atcelts**, un tās var rediģēt. Project Operations neatbalstītie statusi ir **Slēgts** un **Atcelts**. </br> Kad rēķins ir izveidots, statuss tiek iestatīts uz **Aktīvs**. </br>Tikai pēc rēķina apstiprināšanas statusam ir jābūt iestatītam uz **Apmaksāts**.  | 
| **Projekta rēķina statuss** | Cilne **Kopsavilkums** | Tiek iestatītas šādas opcijas: **Melnraksts**, **Pārskatīšanā** un **Apstiprināts**, un tās var rediģēt. Gan statusā **Melnraksts**, gan **Pārskatīšanā** rēķinu var rediģēt. Rēķinu nevar rediģēt pēc tā apstiprināšanas. | 
| **Detalizēta summa** | Cilne **Kopsavilkums** | Visās rēķina rindās esošo apjomu summa pēc avansiem un atskaitījumiem. Tikai lasāms lauks, kura rediģēšana ir bloķēta.  Šo lauku izmanto, lai aprēķinātu galīgo summu. | 
| **Atlaide (%)** | Cilne **Kopsavilkums** | Šo lauku var rediģēt, lai ievadītu atlaidi procentos. Project Operations funkcionalitāte šo lauku neatbalsta. Tas ir neatbalstīts lauks.|  
| **Atlaides summa** | Cilne **Kopsavilkums** | Šo lauku var rediģēt, lai ievadītu atlaides apjomu. Project Operations funkcionalitāte šo lauku neatbalsta. Tas ir neatbalstīts lauks. |  
| **Summa bez piegādes** | **Kopsavilkuma cilne** | Kopējā rēķina summa pēc atlaižu lietošanas. Tikai lasāms lauks, kura rediģēšana ir bloķēta. Šo lauku izmanto, lai aprēķinātu galīgo summu.  | 
| **Piegādes summa** | Cilne **Kopsavilkums** | Šo lauku var rediģēt, lai ievadītu vedmaksas apjomu. Project Operations funkcionalitāte šo lauku neatbalsta. Tas ir neatbalstīts lauks. |
| **Nodokļu kopsumma** | Cilne **Kopsavilkums** | Kopējais nodoklis no visām rēķina rindām rēķinā. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Kopsumma** | Cilne **Kopsavilkums** | Apjoma summa, kas ir pēc atlaidēm un nodokļiem. Summa ir daudzums, kas klientam ir jāmaksā. | 

## <a name="project-based-invoice-lines"></a>Projekta rēķina rindas

Project Operations vienmēr ir viena rēķina rinda katrai projekta līguma rindai. Rēķina rinda tiek izveidota pat tad, ja nav faktisku datu. Šī informācija ir pieejama pro forma rēķina rindā.

| Lauks | Atrašanās vieta | Apraksts | 
| --- | --- | --- |
| **Rēķina ID** | Cilne **Vispārīgi** | Atsauce uz rēķina ID. Tikai lasāms lauks, kura rediģēšana ir bloķēta. Rēķina ID saiti var izmantot, lai pārietu atpakaļ uz rēķina galveni. | 
| **Nosaukums** | Cilne **Vispārīgi** | Rēķina rindas nosaukums, kas pēc noklusējuma ir iestatīts kā līguma rindas nosaukums. Šo lauku var rediģēt. |
| **Project** | Cilne **Vispārīgi** | Projekts saistītajā projekta līguma rindā. Tikai lasāms lauks, kura rediģēšana ir bloķēta. Projekta saiti var izmantot, lai naviģētu uz projektu. | 
| **Rēķinu izrakstīšanas metode** | Cilne **Vispārīgi** | Norēķinu metode saistītajā projekta līguma rindā. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Līguma rindas summa** | Cilne **Vispārīgi** | Līguma summa saistītajā projekta līguma rindā. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Iekļauts rēķinā līdz šim datumam** | Cilne **Vispārīgi** | Rēķina apjomu summa visās šī rēķina rindas detaļās. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Summa** | Cilne **Vispārīgi** | Šī rēķina apjomu summa visās rēķinā iekļaujamajās rindas detaļās. Tikai lasāms lauks, kura rediģēšana ir bloķēta. Šo lauku izmanto, lai aprēķinātu galīgo summu rēķina galvenē. | 
| **Nodoklis** | Cilne **Vispārīgi** | Rēķina rindas nodokļu summa visās šī rēķina rindas detaļās. Tikai lasāms lauks, kura rediģēšana ir bloķēta. Šo lauku izmanto, lai aprēķinātu galīgo nodokļu summu rēķina galvenē. | 
| **Kopējā summa** | Cilne **Vispārīgi** | Rēķina rindas kopējā summa (**Nodoklis + apjoms**) visās šī rēķinā iekļaujamās rindas detaļās. Tikai lasāms lauks, kura rediģēšana ir bloķēta. Šo lauku izmanto, lai aprēķinātu galīgo summu rēķina galvenē. |

## <a name="invoice-line-details"></a>Rēķina rindas informācija

Projekta rēķinā katra rēķina rinda ietver rēķina rindas informāciju. Šī rindas informācija ir saistīta ar rēķinos neiekļautajiem faktiskajiem pārdošanas datiem un atskaites punktiem, kas attiecas uz rēķina rindā ietverto līguma rindu. Visi šie darījumi ir atzīmēti kā **Gatavs rēķina izrakstīšanai**.

Rindā **Laika un materiālu rēķins** rēķina rindas informācija ir grupēta **Iekasējams**, **Neiekasējams** un **Bezmaksas** lapā **Rēķina rinda**. **Rēķinā iekļaujamas rēķina rindas** informācija tiek pievienota rēķina rindas kopsummai. **Bezmaksas** un **Rēķinā neiekļaujamie faktiskie apjomi** netiek pievienoti rēķina rindas kopsummai.

Rindai **Fiksētas cenas rēķins** rēķina rindas informācija tiek izveidota no atskaites punktiem, kas ir atzīmēti kā **Gatavs rēķina izrakstīšanai** saistītajā līguma rindā. Pēc tam kad rēķina rindas informācija ir izveidota no atskaites punkta, atskaites punkta norēķinu statuss tiek atjaunināts uz **Klienta rēķins izveidots**.

### <a name="edit-invoice-line-details"></a>Rēķina rindas informācijas rediģēšana

Tālāk norādītie lauki ir pieejami rēķina rindas informācijā, kas ir balstīta uz faktisko rēķinā neiekļauto pārdošanas apjomu.

| Lauks | Apraksts |
| --- | --- | 
| **Rēķina rinda** | Atsauce uz **Rēķina rindas ID**. Šis lauks ir tikai lasāms un bloķēts rediģēšanai. Šo saiti var izmantot, lai pārietu atpakaļ uz rēķina galveni. | 
| **Apraksts** | Rēķina rindas informācijas apraksts. Pēc noklusējuma iestatīts no lauka **Iekšējie komentāri** sadaļā **Laika ieraksts** un no lauka **Apraksts** sadaļā **Izdevumu ieraksts**. Šo lauku var rediģēt.| 
| **Ārējais apraksts** | Rēķina rindas informācijas apraksts. Pēc noklusējuma iestatīts no lauka **Ārējie komentāri** sadaļā **Laika ieraksts** un no lauka **Apraksts** sadaļā **Izdevumu ieraksts**. Šo lauku var rediģēt. Šo aprakstu var izmantot, lai noteiktu, kam jābūt ietvertam drukātajā rēķinā, kas tiks nosūtīts klientam. Risinājumā Project Operations pro forma rēķinam nav visu nepieciešamo funkcionalitāšu, lai konfigurētu rēķina drukāšanas iestatījumus. | 
| **Sākuma datums** | Šis ir tikai lasāms lauks, kas ir iestatīts pēc noklusējuma no avota faktiskajām vērtībām. |
| **Project** | Šis ir tikai lasāms lauks, kas pēc noklusējuma tiek iestatīts no avota faktiskajām vērtībām projekta saistītajā līguma rindā. |  
| **Uzdevums** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Transakciju kategorija** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Loma** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |  
| **Rezervējamais resurssss** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Resursu uzņēmums** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Resursu vienība** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Daudzums** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |  
| **Vienības grafiks** | Rēķina rindas informācijai par laiku tas vienmēr tiek iestatīts kā laiks, un to nevar rediģēt. Attiecībā uz izdevumiem tas pēc noklusējuma tiek iestatīts no faktiskajiem avota izdevumiem. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Vienība** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |  
| **Cenrādis** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Valūta** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Apjoms** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Nodoklis** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Šo lauku var rediģēt.| 
| **Kopējā summa** | Aprēķināts lauks, kas aprēķināts kā **Summa + nodoklis**. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Norēķinu tips** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Šo lauku var rediģēt. Ja tiek atlasīts **Rēķinā iekļaujams**, tiek pievienota rinda rēķina rindas kopsummai. **Bezmaksas** un **Rēķinā neiekļaujams** to izslēgs no rēķina rindas kopsummas.| 
| **Atlasīt produktu** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Produkts** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Preces nosaukums** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |  
| **Ierakstāmā produkta apraksts** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Transakcijas tips** | Šis ir tikai lasāms lauks, kas ir iestatīts pēc noklusējuma no avota faktiskajām vērtībām uz **Rēķinā iekļautā pārdošana**. |  
| **Transakcijas klase** | Pēc noklusējuma iestatīts no avota faktiskajām vērtībām. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 

Tālāk norādītie lauki ir pieejami rēķina rindas informācijā, kas ir balstīta uz atskaites punktu.

| Lauks | Apraksts |
| --- | --- | 
| **Rēķina rinda** | Atsauce uz **Rēķina rindas ID**. Tikai lasāms lauks, kura rediģēšana ir bloķēta. Saiti var izmantot, lai pārietu atpakaļ uz rēķina galveni.  | 
| **Apraksts** | Rēķina rindas informācijas apraksts. Pēc noklusējuma iestatīts avota atskaites punkta aprakstā. | 
|**Ārējais apraksts** | Rēķina rindas informācijas apraksts, kas pēc noklusējuma ir iestatīts no avota atskaites punkta apraksta. Šo lauku var izmantot, lai noteiktu, kam jābūt ietvertam drukātajā rēķinā, kas tiks nosūtīts klientam. Risinājumā Project Operations pro forma rēķinam nav visu nepieciešamo funkcionalitāšu, lai konfigurētu rēķina drukāšanas iestatījumus. | 
| **Sākuma datums** | Pēc noklusējuma iestatīts no **Atskaites punkta** datuma avota atskaites punktā. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Project** | Pēc noklusējuma iestatīts no avota atskaites punkta. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Uzdevums** | Pēc noklusējuma iestatīts no avota atskaites punkta. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Transakciju kategorija** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Loma** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Rezervējamais resurssss** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Resursu vienība** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Vienības grafiks** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Vienība** | Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Cenrādis** | Pēc noklusējuma iestatīts no avota atskaites punkta summas. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Valūta** | Pēc noklusējuma iestatīts no avota atskaites punkta. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Summa** | Pēc noklusējuma iestatīts no avota atskaites punkta summas. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Nodoklis** | Pēc noklusējuma iestatīts no avota atskaites punkta nodokļa summas. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Kopējā summa** | Pēc noklusējuma iestatīts no avota atskaites punkta kopējās summas. Šo lauku var rediģēt. | 
| **Norēķinu tips** | Pēc noklusējuma vienmēr iestatīts kā **Rēķinā iekļaujams**. Tikai lasāms lauks, kura rediģēšana ir bloķēta. |
| **Transakcijas tips** | Pēc noklusējuma iestatīts no avota atskaites punkta. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 
| **Darījuma klase** | Pēc noklusējuma iestatīts no avota atskaites punkta. Tikai lasāms lauks, kura rediģēšana ir bloķēta. | 

## <a name="refresh-invoice-transactions"></a>Rēķina darījuma atsvaidzināšana

Ja jums ir faktiskie dati, kas ienāca pēc rēķina izveidošanas, varat tos iekļaut rēķinā.

1. Skatā **Norēķinu neizpildīto darbību žurnāls** atzīmējiet datus kā **Gatavs rēķina izrakstīšanai**.   
2. Atveriet pro forma rēķina melnrakstu lentē **Darbības** un atlasiet **Atsvaidzināt rēķina rindas transakcijas**.

  Rēķina rindas informācija ir izveidota visām faktiskajām vērtībām, kas ir ar pagātnes datumu un atzīmētas kā **Gatavs rēķinam**, bet nav ietvertas rēķinā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
