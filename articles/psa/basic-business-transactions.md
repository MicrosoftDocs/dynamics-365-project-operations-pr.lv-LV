---
title: Biznesa transakcijas
description: Šajā tēmā ir sniegta informācija par biznesa transakcijām.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 33c27acc6747c94d76892f41031adc46150da0e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011560"
---
# <a name="business-transactions"></a>Biznesa transakcijas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Programmā Dynamics 365 Project Service Automation *biznesa transakcija* ir abstrakta koncepcija, ko nepārstāv neviena entītija. Taču daži kopējie lauki un procesi entītijās ir izstrādāti biznesa transakciju koncepcijas izmantošanai. Šo abstrakciju izmanto tālāk norādītās entītijas.

- Piedāvājuma rindas detaļas
- Līguma rindas detaļas
- Novērtējuma rindas
- Žurnāla rindas
- Faktiski

No šīm entītijām Piedāvājuma rindas detaļas, Līguma rindas detaļas un Novērtējuma rindas tiek kartētas uz projekta dzīves cikla novērtēšanas fāzi. Entītijas Žurnāla rindas un Faktiskie dati tiek kartētas uz projekta dzīves cikla izpildes fāzi.

PSA ierakstus šajās piecās entītijās uzskata par biznesa transakcijām. Vienīgā atšķirība ir tāda, ka ieraksti entītijās, kas ir kartētas uz novērtēšanas fāzi, tiek uzskatīti par finanšu prognozēm, bet ieraksti entītijās, kas ir kartētas uz izpildes fāzi, tiek uzskatīti par finanšu faktiem, kas jau ir notikuši.

Papildinformāciju skatiet sadaļās [Novērtējumi](estimates.md) un [Faktiskie dati](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepcijas, kas ir unikālas biznesa transakcijām
Biznesa transakciju koncepcijai ir unikālas tālāk norādītās koncepcijas.

- Transakcijas tips
- Transakciju klase
- Transakcijas izcelsme
- Transakcijas savienojums

### <a name="transaction-type"></a>Transakcijas tips

Transakcijas tips norāda projekta finansiālās ietekmes laiku un kontekstu projektā. To norāda opciju kopa, kam programmā PSA ir tālāk norādītās atbalstītās vērtības.
- Izmaksas
- Projekta līgums
- Rēķinā neiekļautā pārdošana
- Rēķinā iekļautā pārdošana
- Starporganizāciju pārdošana
- Resursu struktūrvienības izmaksas

### <a name="transaction-class"></a>Transakciju klase

Transakciju klase norāda dažādus izmaksu tipus, kas rodas projektos. To norāda opciju kopa, kam programmā PSA ir tālāk norādītās atbalstītās vērtības.

- Time
- Izdevumi
- Materiāls
- Maksa
- Atskaites punkts
- Nodoklis

Vienuma **Atskaites punkts** vērtību parasti izmanto biznesa loģika fiksētas cenas norēķiniem programmā PSA.

### <a name="transaction-origin"></a>Transakcijas izcelsme

Transakcijas izcelsme ir entītija, kurā tiek glabāta katras biznesa transakcijas izcelsme. Tā kā projekta izpilde tika sākta, katra biznesa transakcija izveidos vēl vienu biznesa transakciju, kas savukārt izveidos vēl vienu un tā tālāk. Transakcijas izcelsmes entītija tika izstrādāta, lai glabātu datus par katras transakcijas izcelsmi, kas palīdz atskaišu izveidē un izsekojamībā. 

### <a name="transaction-connection"></a>Transakcijas savienojums

Transakcijas savienojums ir entītija, kas glabā attiecības starp divām līdzīgām biznesa transakcijām, piemēram, izmaksām un saistītajiem pārdošanas faktiskajiem datiem vai transakciju anulēšanu, ko izraisa tādas norēķinu darbības kā rēķina apstiprinājums vai rēķina labojumi.

Kopā entītijas Transakcijas izcelsme un Transakcijas savienojums palīdz jums izsekot relācijas starp biznesa transakcijām un darbībām, ko izraisījusi noteiktas biznesa transakcijas izveide.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Piemērs: kā entītija Transakcijas izcelsme darbojas ar entītiju Transakcijas savienojums

Tālāk sniegtajā piemērā ir redzama tipiska laika ierakstu apstrāde PSA projekta dzīves ciklā.

> ![Laika ierakstu apstrāde Project Service dzīves ciklā](media/basic-guide-17.png)
 
1. Iesniedzot laika ierakstu, tiek izveidotas divas žurnāla rindas: viena ir paredzēta izmaksām, bet otra ir paredzēta rēķinā neiekļautajai pārdošanai.
2. Veicot laika ieraksta galīgo apstiprināšanu, tiek izveidoti divu veidu faktiskie dati: vieni ir paredzēti izmaksām, bet otri ir paredzēti rēķinā neiekļautajai pārdošanai.
3. Kad lietotājs izveido projekta rēķinu, rēķina rindas transakcija tiek izveidota, izmantojot datus no rēķinā neiekļautās pārdošanas faktiskajiem datiem. 
4. Apstiprinot rēķinu, tiek izveidoti divu veidu jauni faktiskie dati: rēķinā neiekļautās pārdošanas anulēšana un rēķinā iekļautās pārdošanas faktiskie dati.

Katrs no šiem notikumiem izraisa ierakstu izveidi entītijās Transakcijas izcelsme un Transakcijas savienojums, lai palīdzētu izsekot relācijas starp šiem ierakstiem, kas tiek izveidoti laika ierakstu, žurnāla rindu, faktisko datu un rēķina rindu detaļās.

Tālāk sniegtajā tabulā ir parādīti iepriekšējās darbplūsmas ieraksti entītijā Transakcijas izcelsme.

| Notikums                        | Izcelsme                   | Izcelsmes tips                       | Transakcija                       | Transakcijas tips         |
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

Tālāk sniegtajā tabulā ir parādīti iepriekšējās darbplūsmas ieraksti entītijā Transakcijas savienojums.

| Notikums                          | 1. transakcija                 | 1. transakcijas loma | 1. transakcijas tips           | 2. transakcija                | 2. transakcijas loma | 2. transakcijas tips |
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