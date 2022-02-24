---
title: Spēlētāju statistikas saistīšana ar sākotnējiem ierakstiem
description: Šajā tēmā izskaidrots, kā faktiskos datus saistīt ar sākotnējiem ierakstiem, piemēram, laika ierakstu, izdevumu ierakstu vai materiālu lietojuma žurnāliem.
author: rumant
manager: tfehr
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 545775c4eae6c3dc689f264e7f662471c17b2340
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852598"
---
# <a name="link-actuals-to-original-records"></a>Spēlētāju statistikas saistīšana ar sākotnējiem ierakstiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Programmā Dynamics 365 Project Operations *biznesa transakcija* ir abstrakts koncepts, ko nepārstāv neviena entītija. Taču daži kopējie lauki un procesi entītijās ir izstrādāti biznesa transakciju koncepcijas izmantošanai. Šo konceptu izmanto tālāk norādītās entītijas.

- Piedāvājuma rindas detaļas
- Līguma rindas detaļas
- Novērtējuma rindas
- Žurnāla rindas
- Faktiski

No šīm entītijām **Piedāvājuma rindas informācija**, **Līguma rindas informācija** un **Aprēķinu rindas** tiek kartētas uz projekta dzīves cikla aprēķinu fāzi. Entītijas **Žurnāla rindas** un **Faktiskās entītijas** tiek kartētas uz projekta dzīves cikla izpildes fāzi.

Project Operations ierakstus šajās piecās entītijās uzskata par biznesa transakcijām. Vienīgā atšķirība ir tāda, ka ieraksti entītijās, kas ir kartētas uz aprēķinu fāzi, tiek uzskatīti par finanšu prognozēm, bet ieraksti entītijās, kas ir kartētas uz izpildes fāzi, tiek uzskatīti par finanšu faktiem, kas jau ir notikuši.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepcijas, kas ir unikālas biznesa transakcijām
Biznesa transakciju koncepcijai ir unikālas tālāk norādītās koncepcijas.

- Transakcijas tips
- Transakciju klase
- Transakcijas izcelsme
- Transakcijas savienojums

### <a name="transaction-type"></a>Transakcijas tips

Transakcijas tips norāda projekta finansiālās ietekmes laiku un kontekstu projektā. To norāda opciju kopa, kam programmā Project Operations ir tālāk norādītās atbalstītās vērtības.

  - izdevumi
  - Projekta līgums
  - Rēķinā neiekļautā pārdošana
  - Rēķinā iekļautā pārdošana
  - Starporganizāciju pārdošana
  - Resursu struktūrvienības izmaksas

### <a name="transaction-class"></a>Transakciju klase

Transakciju klase norāda dažādus izmaksu tipus, kas rodas projektos. To norāda opciju kopa, kam programmā Project Operations ir tālāk norādītās atbalstītās vērtības.

  - Laiks
  - Izdevumi
  - Materiāls
  - Maksa
  - Atskaites punkts
  - Nodoklis

Entītiju **Atskaites punkts** parasti izmanto biznesa loģika fiksētas cenas norēķiniem programmā Project Operations.

### <a name="transaction-origin"></a>Transakcijas izcelsme

**Transakcijas izcelsme** ir entītija, kurā tiek glabāta katras biznesa transakcijas izcelsme. Tā kā projekts tiek īstenots pa maziem uzņēmumiem, katra biznesa transakcija palielinās cita biznesa transakciju, kas savukārt radīs vēl vienu darījumu un tā tālāk. Transakcijas izcelsmes entītija ir izstrādāta, lai glabātu datus par katras transakcijas izcelsmes vietu un palīdzētu veidot pārskatus un veikt izsekošanu. 

### <a name="transaction-connection"></a>Transakcijas savienojums

**Transakcijas savienojums** ir entītija, kas glabā attiecības starp divām līdzīgām biznesa transakcijām, piemēram, izmaksām un saistītajiem pārdošanas faktiskajiem datiem vai transakciju anulēšanu, ko izraisa tādas norēķinu darbības kā rēķina apstiprinājums vai rēķina labojumi.

Kopā entītijas **Transakcijas izcelsme** un **Transakcijas savienojums** palīdz jums izsekot relācijas starp biznesa transakcijām un darbībām, ko izraisījusi noteiktas biznesa transakcijas izveide.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Piemērs: kā entītija Transakcijas izcelsme darbojas ar entītiju Transakcijas savienojums

Tālāk sniegtajā piemērā ir redzama tipiska laika ierakstu apstrāde Project Operations projekta dzīves ciklā.

> ![Laika ierakstu apstrāde Project Service dzīves ciklā](media/basic-guide-17.png)
 
1. Iesniedzot laika ierakstu, tiek izveidotas divas žurnāla rindas: viena ir paredzēta izmaksām, bet otra ir paredzēta rēķinā neiekļautajai pārdošanai.
2. Veicot laika ieraksta galīgo apstiprināšanu, tiek izveidoti divu veidu faktiskie dati: vieni ir paredzēti izmaksām, bet otri ir paredzēti rēķinā neiekļautajai pārdošanai.
3. Kad tiek izveidots jauns rēķins, tiek izveidota rēķina rindas transakcija, izmantojot datus no rēķinā neiekļautās pārdošanas faktiskajiem datiem. 
4. Apstiprinot rēķinu, tiek izveidoti divu veidu jauni faktiskie dati: rēķinā neiekļautās pārdošanas anulēšana un rēķinā iekļautās pārdošanas faktiskie dati.

Katrā no šiem notikumiem tiek izveidots ieraksts entītijā **Transakcijas izcelsme** un **Transakcijas savienojums**. Šie jaunie ieraksti palīdz izveidot ierakstu attiecību vēsturi, kas tiek veidoti dažādos laika ierakstos, laika joslu rindā, faktiskajās rindās un rēķina rindas informācijā.

Tālāk sniegtajā tabulā ir parādīti iepriekšējās darbplūsmas ieraksti entītijā **Transakcijas izcelsme**.

| Pasākums                        | Izcelsme                   | Izcelsmes tips                       | Transakcija                       | Transakcijas tips         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Laika ieraksta iesniegšana        | Laika ieraksta GUID   | Laika ieraksts                        | Žurnāla rindas ieraksta GUID (izmaksas)   | Žurnāla rinda             |
| Laika ieraksta GUID       | Laika ieraksts               | Žurnāla rindas ieraksta GUID (pārdošana)  | Žurnāla rinda                      |                          |
| Laika apstiprinājums                | Žurnāla rindas ieraksta GUID | Žurnāla rinda                      | Rēķinā neiekļautās pārdošanas ieraksta GUID        | Faktiski                   |
| Laika ieraksta GUID       | Laika ieraksts               | Rēķinā neiekļautās pārdošanas ieraksta GUID        | Faktiski                            |                          |
| Žurnāla rindas ieraksta GUID     | Žurnāla rinda             | Izmaksu faktisko datu ieraksta GUID           | Faktiski                            |                          |
| Laika ieraksta GUID       | Laika ieraksts               | Izmaksu faktisko datu ieraksta GUID           | Faktiski                            |                          |
| Rēķina izveide             | Laika ieraksta GUID   | Laika ieraksts                        | Rēķina rindas transakcijas GUID     | Rēķina rindas transakcija |
| Žurnāla rindas ieraksta GUID     | Žurnāla rinda             | Rēķina rindas transakcijas GUID     | Rēķina rindas transakcija          |                          |
| Rēķina apstiprinājums         | Rēķina rindas GUID        | Rēķina rinda                      | Rēķinā iekļautās pārdošanas ieraksta GUID          | Faktiski                   |
| Rēķina GUID                 | Rēķins                  | Rēķinā iekļautās pārdošanas ieraksta GUID          | Faktiski                            |                          |
| Rēķina rindas detaļu GUID     | Rēķina rindas informācija      | Rēķinā iekļautās pārdošanas ieraksta GUID          | Faktiski                            |                          |
| Laika ieraksta GUID       | Laika ieraksts               | Rēķinā iekļautās pārdošanas ieraksta GUID          | Faktiski                            |                          |
| Žurnāla rindas ieraksta GUID     | Žurnāla rinda             | Rēķinā iekļautās pārdošanas ieraksta GUID          | Faktiski                            |                          |
| Laika ieraksta GUID       | Laika ieraksts               | Rēķinā neiekļautās pārdošanas anulēšanas GUID      | Faktiski                            |                          |
| Žurnāla rindas ieraksta GUID     | Žurnāla rinda             | Rēķinā neiekļautās pārdošanas anulēšanas GUID      | Faktiski                            |                          |
| Melnraksta rēķina labojums     | Vecās rēķina rindas detaļu GUID             | Rēķina rindas transakcija          | Labotās rēķina rindas detaļu GUID               | Rēķina rindas transakcija |
| Vecās rēķina rindas GUID                  | Rēķina rinda             | Labotās rēķina rindas detaļu GUID               | Rēķina rindas transakcija          |                          |
| Vecā rēķina GUID             | Rēķins                  | Labotās rēķina rindas detaļu GUID               | Rēķina rindas transakcija          |                          |
| Laika ieraksta GUID       | Laika ieraksts               | Labotās rēķina rindas detaļu GUID               | Rēķina rindas transakcija          |                          |
| Žurnāla rindas ieraksta GUID     | Žurnāla rinda             | Labotās rēķina rindas detaļu GUID               | Rēķina rindas transakcija          |                          |
| Apstiprinātā rēķina labojums | Vecās rēķina rindas detaļu GUID             | Rēķina rindas transakcija          | Anulētās, rēķinā iekļautās pārdošanas faktisko datu GUID | Faktiski                   |
| Vecās rēķina rindas GUID                  | Rēķina rinda             | Anulētās, rēķinā iekļautās pārdošanas faktisko datu GUID | Faktiski                            |                          |
| Vecā rēķina GUID             | Rēķins                  | Anulētās, rēķinā iekļautās pārdošanas faktisko datu GUID | Faktiski                            |                          |
| Laika ieraksta GUID       | Laika ieraksts               | Anulētās, rēķinā iekļautās pārdošanas faktisko datu GUID | Faktiski                            |                          |
| Žurnāla rindas ieraksta GUID     | Žurnāla rinda             | Anulētās, rēķinā iekļautās pārdošanas faktisko datu GUID | Faktiski                            |                          |
| Vecās rēķina rindas detaļu GUID                 | Rēķina rindas transakcija | Jaunās, rēķinā neiekļautās pārdošanas faktisko datu GUID    | Faktiski                            |                          |
| Vecās rēķina rindas GUID                  | Rēķina rinda             | Jaunās, rēķinā neiekļautās pārdošanas faktisko datu GUID    | Faktiski                            |                          |
| Vecā rēķina GUID             | Rēķins                  | Jaunās, rēķinā neiekļautās pārdošanas faktisko datu GUID    | Faktiski                            |                          |
| Laika ieraksta GUID       | Laika ieraksts               | Jaunās, rēķinā neiekļautās pārdošanas faktisko datu GUID    | Faktiski                            |                          |
| Žurnāla rindas ieraksta GUID     | Žurnāla rinda             | Jaunās, rēķinā neiekļautās pārdošanas faktisko datu GUID    | Faktiski                            |                          |
| Labotās rēķina rindas detaļu GUID          | Rēķina rindas transakcija | Jaunās, rēķinā neiekļautās pārdošanas faktisko datu GUID    | Faktiski                            |                          |
| Labotās rēķina rindas GUID           | Rēķina rinda             | Jaunās, rēķinā neiekļautās pārdošanas faktisko datu GUID    | Faktiski                            |                          |
| Labotā rēķina GUID      | Rēķins                  | Jaunās, rēķinā neiekļautās pārdošanas faktisko datu GUID    | Faktiski                            |                          |

Tālāk sniegtajā tabulā ir parādīti iepriekšējās darbplūsmas ieraksti entītijā **Transakcijas savienojums**.

| Pasākums                          | Transakcija 1                 | 1. transakcijas loma | 1. transakcijas tips           | 2. transakcija                | 2. transakcijas loma | 2. transakcijas tips |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Laika ieraksta iesniegšana          | Žurnāla rindas (pārdošanas) GUID     | Rēķinā neiekļautā pārdošana     | msdyn_journalline            | Žurnāla rindas (izmaksu) GUID     | Izmaksas               | msdyn_journalline  |
| Laika apstiprinājums                  | Rēķinā neiekļautās (pārdošanas) GUID  | Rēķinā neiekļautā pārdošana     | msdyn_actual                 | Faktisko izmaksu (izmaksu) GUID       | Izmaksas               | msdyn_actual       |
| Rēķina izveide               | Rēķina rindas detaļu GUID      | Rēķinā iekļautā pārdošana       | msdyn_invoicelinetransaction | Rēķinā neiekļautās pārdošanas faktisko datu GUID   | Rēķinā neiekļautā pārdošana     | msdyn_actual       |
| Rēķina apstiprinājums           | Faktisko datu anulēšanas GUID         | Anulēšana          | msdyn_actual                 | Sākotnējās rēķinā neiekļautās pārdošanas GUID | Sākotnējā           | msdyn_actual       |
| Rēķinā iekļautās pārdošanas GUID              | Rēķinā iekļautā pārdošana                  | msdyn_actual       | Rēķinā neiekļautās pārdošanas faktisko datu GUID   | Rēķinā neiekļautā pārdošana               | msdyn_actual       |                    |
| Melnraksta rēķina labojums       | Rēķina rindas transakcijas GUID | Aizstāšana          | msdyn_invoicelinetransaction | Rēķinā iekļautās pārdošanas GUID            | Sākotnējā           | msdyn_actual       |
| Rēķina labojuma apstiprināšana     | Rēķinā iekļautās pārdošanas anulēšanas GUID    | Anulēšana          | msdyn_actual                 | Rēķinā iekļautās pārdošanas GUID            | Sākotnējā           | msdyn_actual       |
| Jaunās, rēķinā neiekļautās pārdošanas faktisko datu GUID | Aizstāšana                     | msdyn_actual       | Rēķinā iekļautās pārdošanas GUID            | Sākotnējā                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
