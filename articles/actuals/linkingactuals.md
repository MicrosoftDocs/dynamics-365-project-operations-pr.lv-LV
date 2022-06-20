---
title: Darbību izcelsme – saistiet faktiskos datus ar to avotu
description: Šajā rakstā paskaidrots, kā darbību izcelsmes jēdziens tiek izmantots, lai sasaistītu faktiskos datus ar sākotnējiem avota ierakstiem, piemēram, laika ierakstu, izdevumu ierakstu vai materiālu lietojuma žurnāliem.
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
# <a name="transaction-origins---link-actuals-to-their-source"></a>Darbību izcelsme – saistiet faktiskos datus ar to avotu

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Transakciju izcelsmes ieraksti tiek izveidoti, lai sasaistītu faktiskos datus ar to avotu, tādiem laika ierakstiem, izdevumu ierakstiem, materiālu lietojuma žurnāliem un projekta rēķiniem.

Tālāk sniegtajā piemērā ir redzama tipiska laika ierakstu apstrāde Project Operations projekta dzīves ciklā.

> ![Visu laika apstrāde projekta operācijās.](media/basic-guide-17.png)
 
1. Laika ieraksta iesniegšanas rezultātā tiek izveidotas divas žurnāla rindas: viena izmaksām un otra nelīdzenai pārdošanai.
2. Iespējamā laika ieraksta apstiprināšana izraisa divu faktisko datu izveidi: vienu izmaksām un otru par nemainīgu pārdošanu.
3. Kad lietotājs izveido projekta rēķinu, rēķina rindas transakcija tiek izveidota, izmantojot datus no rēķinā neiekļautās pārdošanas faktiskajiem datiem.
4. Apstiprinot rēķinu, tiek izveidoti divu veidu jauni faktiskie dati: rēķinā neiekļautās pārdošanas anulēšana un rēķinā iekļautās pārdošanas faktiskie dati.

Katrs notikums šajā apstrādes darbplūsmā izraisa ierakstu izveidi entītijā Transakcijas izcelsme, lai palīdzētu izveidot šo ierakstu, kas izveidoti laika ievadnē, žurnāla rindā, faktiskajā un rēķina rindas detaļās, lai izveidotu šo ierakstu, žurnāla rindas, faktisko un rēķina rindas detalizēto informāciju.

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


Nākamajā attēlā parādītas saites, kas dažādos notikumos izveidotas starp faktiskajiem un to avotiem, izmantojot laika ierakstu piemēru projekta operācijās.

> ![Kā faktiskie dati ir saistīti ar avota ierakstiem projektu operācijās.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
