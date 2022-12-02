---
title: Transakciju izcelsme — saistiet datus ar avotu
description: Šajā rakst izskaidrots, kā tiek izmantota transakciju izcelsme, lai saistītu datus ar to oriǵinālavota ierakstiem, piemēram, laika ierakstiem, izdevumu ierakstiem vai materiālu lietojuma žurnāliem.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921311"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Transakciju izcelsme — saistiet datus ar avotu

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Transakciju izcelsmes ieraksti tiek izveidoti, lai saistītu datus ar to avotu, piemēram, laika ierakstiem, izdevumu ierakstiem, materiālu izmantojuma žurnāliem un projekta rēķiniem.

Tālāk sniegtajā piemērā ir redzama tipiska laika ierakstu apstrāde Project Operations projekta dzīves ciklā.

> ![Laika ierakstu apstrāde programmā Project Operations.](media/basic-guide-17.png)
 
1. Iesniedzot laika ierakstu, tiek izveidotas divas žurnāla rindas: viena ir paredzēta izmaksām, bet otra ir paredzēta rēķinā neiekļautajai pārdošanai.
2. Veicot laika ieraksta galīgo apstiprināšanu, tiek izveidoti divu veidu faktiskie dati: vieni ir paredzēti izmaksām, bet otri ir paredzēti rēķinā neiekļautajai pārdošanai.
3. Kad lietotājs izveido projekta rēķinu, rēķina rindas transakcija tiek izveidota, izmantojot datus no rēķinā neiekļautās pārdošanas faktiskajiem datiem.
4. Apstiprinot rēķinu, tiek izveidoti divu veidu jauni faktiskie dati: rēķinā neiekļautās pārdošanas anulēšana un rēķinā iekļautās pārdošanas faktiskie dati.

Katrs no notikumiem šajā apstrādē darbplūsmā izraisa ierakstu izveidi entītijā Transakcijas izcelsme, lai palīdzētu izsekot relācijas starp šiem ierakstiem, kas tiek izveidoti laika ierakstu, žurnāla rindu, faktisko datu un rēķina rindu detaļās.

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


Attēlā tālāk parādītas saites, kas tiek izveidotas starp datiem un to avotiem vairākos gadījumos, izmantojot laika ierakstu piemēru programmā Project Operations.

> ![Kā dati tiek saistīti ar avotu ierakstiem programmā Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
