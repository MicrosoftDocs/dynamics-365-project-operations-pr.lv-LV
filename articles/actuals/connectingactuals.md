---
title: Transakciju savienojumi — saite uz dažādu transakciju tipu datiem
description: Šajā rakstā ir izskaidrots, kā tiek izmantots transakcijas savienojums, lai saistītu dažādu tipu faktiskos datus, tādējādi palīdzot sekot līdzi ienesīgumam, rēķinu izrakstīšanas rezervei un rēķinos iekļautās un neiekļautās peļņas aprēķiniem.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926095"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Transakciju savienojumi — saite uz dažādu transakciju tipu datiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Transakciju savienojumu ieraksti tiek izveidoti, lai saistītu dažādu tipu faktiskos datus, kamēr laiks, izmaksas vai materiālu lietojums dzīves cikla laikā pārvietojas no piedāvājuma vai pirmspārdošanas posma uz līguma posmu, apstiprināšanu un/vai atsaukšanu, rēķinu izrakstīšanu un potenciāli kredītu vai rēķinu korekcijām.

Tālāk sniegtajā piemērā ir redzama tipiska laika ierakstu apstrāde Project Operations projekta dzīves ciklā.

> ![Laika ierakstu apstrāde programmā Project Operations.](media/basic-guide-17.png)

Laika ierakstu apstrāde Project Operations projekta dzīves ciklā notiek, veicot tālāk aprakstītās darbības. 

1. Iesniedzot laika ierakstu, tiek izveidotas divas žurnāla rindas: viena ir paredzēta izmaksām, bet otra ir paredzēta rēķinā neiekļautajai pārdošanai. 
2. Veicot laika ieraksta galīgo apstiprināšanu, tiek izveidoti divu veidu faktiskie dati: vieni ir paredzēti izmaksām, bet otri ir paredzēti rēķinā neiekļautajai pārdošanai. Šie 2 faktisko datu vienumi tiek saistīti, izmantojot transakciju savienojumus.
3. Kad lietotājs izveido projekta rēķinu, rēķina rindas transakcija tiek izveidota, izmantojot datus no rēķinā neiekļautās pārdošanas faktiskajiem datiem.
4. Apstiprinot rēķinu, tiek izveidoti divi jauni faktisko datu vienumi: rēķinā neiekļautās pārdošanas anulēšana un rēķinā iekļautās pārdošanas faktisko datu vienums. Rēķinā neiekļautu pārdošanu apgriešana un sākotnējā rēķinā neiekļautā faktiskā pārdošana tiek saistīta, izmantojot apgriezto transakciju savienojumus. Rēķinos iekļautās pārdošanas un sākotnējās rēķinos neiekļautās faktiskās pārdošana tiek saistītas, arī lai parādītu saites starp vienumiem, kas iepriekš bija rezerve vai notiekoša projekta (NP) ieņēmumi, un vienumiem, kas tagad ir rēķinā iekļautie ieņēmumi.   

Katrs apstrādes darbplūsmas notikums izraisa ierakstu izveidi tabulā **Transakcijas savienojums**. Tas palīdz izveidot izsekojamu ierakstu attiecību vēsturi, kas tiek veidoti dažādos laika ierakstos, laika žurnāla rindā, faktiskajos datos un rēķina rindas informācijā.

Tālāk sniegtajā tabulā ir parādīti iepriekšējās darbplūsmas ieraksti entītijā **Transakcijas savienojums**.

|Notikums                   |1. transakcija                 |1. transakcijas loma |1. transakcijas tips       |2. transakcija          |2. transakcijas loma |2. transakcijas tips |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Laika ieraksta iesniegšana   |Žurnāla rindas (pārdošanas) GUID     |Rēķinā neiekļautā pārdošana |msdyn_journalline            |Žurnāla rindas (izmaksu) GUID     |Izmaksas            |msdyn_journalline  |
|Laika apstiprinājums           |Rēķinā neiekļautās (pārdošanas) GUID  |Rēķinā neiekļautā pārdošana |msdyn_actual                 |Faktisko izmaksu (izmaksu) GUID       |Izmaksas            |msdyn_actual       |
|Rēķina izveide        |Rēķina rindas detaļu GUID      |Rēķinā iekļautā pārdošana   |msdyn_invoicelinetransaction |Rēķinā neiekļautās pārdošanas faktisko datu GUID   |Rēķinā neiekļautā pārdošana  |msdyn_actual       |
|Rēķina apstiprinājums    |Faktisko datu anulēšanas GUID         |Anulēšana      |msdyn_actual                 |Sākotnējās rēķinā neiekļautās pārdošanas GUID |Sākotnējā        |msdyn_actual       |
|                        |Rēķinā iekļautās pārdošanas GUID             |Rēķinā iekļautā pārdošana   |msdyn_actual                 |Rēķinā neiekļautās pārdošanas faktisko datu GUID   |Rēķinā neiekļautā pārdošana  |msdyn_actual       |
|Melnraksta rēķina labojums |Rēķina rindas transakcijas GUID|Aizstāšana      |msdyn_invoicelinetransaction |Rēķinā iekļautās pārdošanas GUID            |Sākotnējā        |msdyn_actual       |
|Rēķina labojuma apstiprināšana|Rēķinā iekļautās pārdošanas anulēšanas GUID  |Anulēšana      |msdyn_actual                 |Rēķinā iekļautās pārdošanas GUID            |Sākotnējā        |msdyn_actual       |
|                        |Jaunas rēķinā neiekļautā pārdošanas GUID |Aizstāšana            |msdyn_actual                 |Rēķinā iekļautās pārdošanas GUID            |Sākotnējā        |msdyn_actual       |


Attēlā tālāk parādītas saites, kas tiek izveidotas starp dažādu tipu faktiskajiem datiem vairākos gadījumos, izmantojot laika ierakstu piemēru programmā Project Operations.

> ![Kā programmā Project Operations tiek saistīti dažādu tipu faktiskie dati.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
