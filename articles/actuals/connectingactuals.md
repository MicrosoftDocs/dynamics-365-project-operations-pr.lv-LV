---
title: Darbību savienojumi – saistīt dažādu darbību tipu faktiskos datus
description: Šajā tēmā paskaidrots, kā transakcijas savienojums tiek izmantots, lai saistītu dažādu veidu faktiskos datus, kas palīdz izsekot rentabilitātei, rēķinu uzkrāšanai un rēķinu izrakstīšanai salīdzinājumā ar nesalīdzinātiem ieņēmumu aprēķiniem.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580787"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Darbību savienojumi – saistīt dažādu darbību tipu faktiskos datus

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Transakciju savienojuma ieraksti tiek izveidoti, lai saistītu dažādu tipu faktiskos datus kā laika, izdevumu vai materiālu lietojuma kustības tā dzīves ciklā no piedāvājuma vai pirmspārdošanas posma uz līguma stadiju, apstiprinājumiem un/vai atsaukumiem, rēķinu izrakstīšanu un, iespējams, kredīta vai koriģējošiem rēķiniem.

Tālāk sniegtajā piemērā ir redzama tipiska laika ierakstu apstrāde Project Operations projekta dzīves ciklā.

> ![Laika ierakstu apstrāde projekta operācijās.](media/basic-guide-17.png)

Projekta operāciju projekta dzīves cikla laika ierakstu apstrāde notiek šādi: 

1. Laika ieraksta iesniegšanas rezultātā tiek izveidotas divas žurnāla rindas: viena izmaksām un otra nelīdzenai pārdošanai. 
2. Iespējamā laika ieraksta apstiprināšana izraisa divu faktisko datu izveidi: vienu izmaksām un otru par nemainīgu pārdošanu. Šie 2 faktiskie fakti ir saistīti, izmantojot transakciju savienojumus.
3. Kad lietotājs izveido projekta rēķinu, rēķina rindas transakcija tiek izveidota, izmantojot datus no rēķinā neiekļautās pārdošanas faktiskajiem datiem.
4. Kad rēķins ir apstiprināts, tiek izveidoti divi jauni fakti: nemainīga pārdošanas anulēšana un faktiskā rēķinā iekļautā pārdošana. Nemainīgā pārdošanas atsaukšana un sākotnējā nemainīgā pārdošana faktiski ir savienota, izmantojot atpakaļgaitas transakciju savienojumus. Rēķinos iekļautie pārdošanas apjomi un sākotnējie nemainīgie pārdošanas fakti ir saistīti arī, lai parādītu saikni starp kādreiz neizskatītajiem vai nepabeigtā darba (NP) ieņēmumiem ar tagadējiem rēķinos iekļautajiem ieņēmumiem.   

Katrs notikums apstrādes darbplūsmā izraisa ierakstu izveidi tabulā Transakcijas **savienojums**. Tas palīdz izveidot to ierakstu attiecību izsekošanu, kas izveidoti laika ieraksta, žurnāla rindas, faktiskās un rēķina rindas detaļās.

Šajā tabulā ir parādīti iepriekšējās darbplūsmas transakciju **savienojuma** entītijas ieraksti.

|Notikums                   |1. transakcija                 |1. transakcijas loma |1. transakcijas tips       |2. transakcija          |2. transakcijas loma |2. transakcijas tips |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Laika ieraksta iesniegšana   |Žurnāla rindas (pārdošanas) GUID     |Rēķinā neiekļautā pārdošana |msdyn_journalline            |Žurnāla rindas (izmaksu) GUID     |Izmaksas            |msdyn_journalline  |
|Laika apstiprinājums           |Rēķinā neiekļautās (pārdošanas) GUID  |Rēķinā neiekļautā pārdošana |msdyn_actual                 |Faktisko izmaksu (izmaksu) GUID       |Izmaksas            |msdyn_actual       |
|Rēķina izveide        |Rēķina rindas detaļu GUID      |Rēķinā iekļautā pārdošana   |msdyn_invoicelinetransaction |Rēķinā neiekļautās pārdošanas faktisko datu GUID   |Rēķinā neiekļautā pārdošana  |msdyn_actual       |
|Rēķina apstiprinājums    |Faktisko datu anulēšanas GUID         |Anulēšana      |msdyn_actual                 |Sākotnējās rēķinā neiekļautās pārdošanas GUID |Sākotnējā        |msdyn_actual       |
|                        |Rēķinā iekļautās pārdošanas GUID             |Rēķinā iekļautā pārdošana   |msdyn_actual                 |Rēķinā neiekļautās pārdošanas faktisko datu GUID   |Rēķinā neiekļautā pārdošana  |msdyn_actual       |
|Melnraksta rēķina labojums |Rēķina rindas transakcijas GUID|Aizstāšana      |msdyn_invoicelinetransaction |Rēķinā iekļautās pārdošanas GUID            |Sākotnējā        |msdyn_actual       |
|Rēķina labojuma apstiprināšana|Rēķinā iekļautās pārdošanas anulēšanas GUID  |Anulēšana      |msdyn_actual                 |Rēķinā iekļautās pārdošanas GUID            |Sākotnējā        |msdyn_actual       |
|                        |Jauns nemainīgs pārdošanas GUID |Aizstāšana            |msdyn_actual                 |Rēķinā iekļautās pārdošanas GUID            |Sākotnējā        |msdyn_actual       |


Šajā attēlā parādītas saites, kas izveidotas starp dažāda veida faktiskajiem datiem dažādos pasākumos, izmantojot laika ierakstu piemēru projekta operācijās.

> ![Kā projektu operācijās tiek savstarpēji saistīti dažādu tipu faktiskie fakti.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
