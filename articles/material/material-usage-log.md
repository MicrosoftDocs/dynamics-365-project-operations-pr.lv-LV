---
title: Materiālu lietojuma ieraksts projektos un projekta uzdevumos
description: Šajā rakstā ir sniegta informācija par to, kā reģistrēt materiālu izmantošanu attiecībā pret projektiem un projekta uzdevumiem.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eeb8303821bc4c246e37333ddbcb77ca798d2e8f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920069"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Materiālu lietojuma ieraksts projektos un projekta uzdevumos

_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_

Tā kā projekta darba grupa darbojas ar projekta uzdevumiem, šī darba grupa izmanto materiālus. Materiālu lietojuma žurnāls nodrošina veidu, kā reģistrēt šo lietojumu, lai to varētu apstiprināt projekta vadītājs un pēc tam izrakstīt rēķinu klientam. 

Lai reģistrētu kataloga vai ierakstāmo materiālu lietojumu un iesniegtu tos apstiprinātājam, veiciet tālāk minētās darbības. 

1. Navigācijas rūtī atlasiet **Materiālu lietojums** un pēc tam — **Jauns**.
2. Lapā **Jaunu materiālu lietojums** ievadiet nepieciešamo materiālu lietojuma informāciju un pēc tam atlasiet **Saglabāt**.

Tālāk sniegtajā tabulā ir sniegta informācija par lapas **Materiālu lietojuma žurnāls** laukiem. 

| **Lauks** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- |
| Apraksts | Specifiska materiālu lietojuma apraksts. | Šim laukam nav lejupstraumes ietekmes. |
| Datums | Datums, kurā materiāli tiks izmantoti. | Šim laukam nav lejupstraumes ietekmes. |
| Project | Aktīvu projektu saraksts. | Atlasot projektu materiālu lietojuma žurnālam, tiek ietekmēts lauks **Uzdevums**, lai rādītu tikai tos uzdevumus, kas atrodas projektā. |
| Uzdevums | Projekta uzdevumu saraksts, tostarp kopsavilkuma un lapas mezgla uzdevumi. | Atlasot uzdevumu materiālu lietojuma žurnālam, tiek ietekmētas uzdevuma faktiskās materiālu izmaksas un faktiskās materiālu pārdošanas vērtības. Ja šis lauks ir tukšs, atbilstošās materiālu izmantošanas izmaksas un pārdošanas vērtības tiek uzskaitītas un apkopotas tikai projekta līmenī. |
| Atlasīt produktu | Norādiet, vai šis materiālu lietojums ir **esošam** (kataloga) produktam vai **ierakstāmam** produktam. | Šis lauks nosaka produkta tipu. |
| Produkts | Produkta ID no produktu kataloga. Kad atlasāt produkta ID, lauks **Atlasīt produktu** automātiski tiek atjaunināts uz **Esošs produkts**. ID tiek izmantots, lai no cenrāža izgūtu izmaksu un pārdošanas cenas. | Šim laukam nav lejupstraumes ietekmes. |
| Ierakstāmā produkta apraksts | Teksta lauks, ko rakstīt produkta nosaukumā. Šis lauks ir pieejams, laukā **Atlasīt produktu** atlasot **Ierakstāms produkts**.| Šim laukam nav lejupstraumes ietekmes. |
| Rezervējamais resurssss| Resurss, kas izmantoja šo materiālu projektā. Šī lauka noklusējuma vērtība ir lietotājam reģistrētais rezervējamais resurss, bet to var mainīt uz ieraksta izmantošanu citu projekta darba grupas dalībnieku vārdā. | Šim laukam nav lejupstraumes ietekmes. |
| Vienību grupa | Šī lauka noklusējuma vērtība tiek ņemta no vienību grupas, kas ir iestatīta kā noklusējuma kataloga produktam. Šo lauku var atjaunināt, lai atlasītu citu vienību grupu. | Šim laukam nav lejupstraumes ietekmes. |
| Vienība | Šī lauka noklusējuma vērtība ir atlasītā produkta noklusējuma vienība. Šo lauku var atjaunināt, lai atlasītu citu vienību grupu. | Mainot vienību, tiek parādīts atšķirīga noklusējuma vienības cena un izmaksas. |
| Daudzums | Projektā vai projekta uzdevumā lietotais produkta daudzums. | Šim laukam nav lejupstraumes ietekmes. |
| Vienības izmaksas | Atlasītā produkta vienības izmaksas un vienību kombinācija, kā tas ir iestatīts piemērojamajam izmaksu cenrādim. | Vienības izmaksas vienmēr tiek parādītas projekta izmaksu valūtā. Ja cenrāža kombinācijas produktam un vienībai nav vienības izmaksu, vienības izmaksas pēc noklusējuma būs 0,00. |
| Kopējās izmaksas | Izmaksu summa, kas tiek aprēķināta kā daudzuma \*vienības izmaksas.| Izmaksu summa vienmēr tiek parādīta projekta izmaksu valūtā. |


## <a name="submit-material-usage-for-review-and-approval"></a>Materiālu lietojuma iesniegšana pārskatīšanai un apstiprināšanai 
Pēc tam, kad tverts viss materiālu lietojums un esat gatavs to apstiprināt, lietošanas informācija ir jāiesniedz pārskatīšanai.

1. Atveriet **Materiālu lietojuma žurnāls** un atlasiet vienu vai vairākus ierakstus. Varat arī atlasīt visus materiālu lietojuma ierakstus, izmantojot galvenes izvēles rūtiņu.
2. Atlasiet **Iesniegt**. Sistēma apstrādā atlasītos ierakstus un pēc tam izveido materiālu lietojuma apstiprinājuma pieprasījumus.

## <a name="recall-a-material-usage-log"></a>Materiālu lietojuma žurnāla atsaukšana

Ja nepieciešams, var tikt atsaukts iesniegts materiālu lietojums. Tas, cik laika nepieciešams, lai atsauktu materiālu izmantošanas ierakstu, ir atkarīgs no apstiprinājuma posma.  Ja apstiprinātājs vēl nav apstiprinājis ierakstu, atsaukšana var notikt nekavējoties. Tomēr, ja ieraksts jau ir apstiprināts, apstiprinātājam tiek lūgts apstiprināt atsaukumu un mainīt darījumus.

1. Atveriet **Materiālu lietojums** un materiālu lietojuma žurnālu sarakstā atlasiet atsaucamo materiālu lietojumu.
2. Atlasiet **Atsaukt**. Ja materiālu lietojuma ieraksts vēl nav apstiprināts, sistēma nekavējoties to atsauc. Ja materiālu ieraksts jau ir apstiprināts, tiek izveidots lūgums sniegt paziņojumu par to apstiprinātājam, ka vēlaties atsaukt materiālu lietojumu. Pēc tam apstiprinātājs apstiprinās, ka var veikt atsaukšanu, un ieraksts tiks atgriezts.

## <a name="delete-a-material-usage-log"></a>Materiālu lietojuma žurnāla dzēšana

Varat izdzēst materiālu lietojuma žurnālus, kas nav iesniegti. Lai izdzēstu materiālu lietojuma žurnālu, kas jau ir iesniegts, vispirms tas ir jāatsauc.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
