---
title: Pārdošanas cenu noteikšana projekta aprēķinos un spēlētāju statistikā
description: Šajā rakstā sniegta informācija par to, kā tiek noteiktas pārdošanas cenas projektu aprēķiniem un datiem.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475194"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Pārdošanas cenu noteikšana projekta aprēķinos un spēlētāju statistikā

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Lai noteiktu pārdošanas cenas aprēķiniem un datiem programmā Microsoft Dynamics 365 Project Operations, sistēma vispirms izmantot ienākošā aprēķina vai faktiskā konteksta datumu un valūtu, lai noteiktu cenrādi. Īpaši datu kontekstā sistēma izmanto lauku **Transakcijas datums**, lai noteiktu, kurš cenrādis ir lietojams. Ienākošā aprēķina vai datu vērtība **Transakcijas datums** tiek salīdzināta ar cenrāža vērtībām **Faktiskais sākums (atkarīgs no laika joslas)** un **Faktiskās beigas (atkarīgs no laika joslas)**. Pēc tam, kad ir noteikts pārdošanas cenrādis, sistēma nosaka pārdošanas vai rēķina likmi.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Pārdošanas likmju noteikšana Laika datu un aprēķinu rindām

Aprēķina konteksts **Laikam** attiecas uz:

- **Laika** piedāvājuma rindas informācija.
- **Laika** līguma rindas informācija.
- Resursu piešķīrumi projektam.

Datu konteksts **Laikam** attiecas uz:

- Ierakstu un labošanas žurnālu rindas **Laikam**.
- Žurnālu rindas, kas tiek izveidotas, kad tiek iesniegts laika ieraksts.
- **Laika** rēķina rindas informācija. 

Pēc tam, kad ir noteikts pārdošanas cenrādis, sistēma izpilda tālāk norādītās darbības, lai ievadītu rēķina likmes noklusējuma vērtību.

1. Sistēma saskaņo lauku **Loma** un **Resursu vienība** kombināciju novērtējuma vai datu kontekstā **Laiks** ar lomas cenu rindām cenrādī. Šī saskaņošana pieņem, ka rēķina likmēm ir izmantotas neiekļautas cenas noteikšanas dimensijas. Ja esat konfigurējis cenu noteikšanu, pamatojoties uz kādu citu lauku, nevis **Loma** un **Resursu vienība**, tad šī ir lauku kombinācija, kas tiks izmantota, lai izgūtu atbilstošo lomas cenu rindu.
1. Ja sistēma atrod lomas cenu rindu, kurai ir rēķina likme lauku rindai **Loma** un **Resursu vienība**, tad šī rēķina likme tiek izmantota kā noklusējuma rēķina likme.
1. Ja sistēma nespēj saskaņot vērtības **Loma** un **Resursu vienība**, tad tā iegūst lomu cenas rindas ar atbilstošu vērtību laukam **Loma**, bet nulles vērtības laukam **Resursu vienība**. Pēc tam, kad sistēma ir atradusi atbilstošu lomas cenas ierakstu, šī ieraksta rēķina likme tiek izmantota kā noklusējuma rēķina likme. Šī atbilstība pieņem ārpus saraksta esošu konfigurāciju **Loma** pret **Resursu vienība** relatīvajai prioritātei kā pārdošanas cenu dimensiju.

> [!NOTE]
> Ja laukiem **Loma** un **Resursu vienība** konfigurējat atšķirīgas prioritātes vai ja ir citas augstākas prioritātes kategorijas, iepriekšējā darbība attiecīgi mainīsies. Sistēma izgūst lomu cenu ierakstus, kuriem ir vērtības, kas atbilst katrai cenas noteikšanas scenārija vērtībai prioritārā secībā. Rindas ar vērtībām Null šīm dimensijām ir pēdējās.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Pārdošanas likmju noteikšana attiecībā uz faktiskajām un novērtējuma rindām par Izdevumiem

Aprēķina konteksts **Izdevumiem** attiecas uz:

- **Izdevumu** piedāvājuma rindas informācija.
- **Izdevumu** līguma rindas informācija.
- Izdevumu projekta aplēšu rindas.

Faktiskais konteksts **Izdevumiem** attiecas uz:

- Ierakstu un labošanas žurnālu rindas **Izdevumiem**.
- Žurnālu rindas, kas tiek izveidotas, kad tiek iesniegts izdevumu ieraksts.
- **Izdevumu** rēķina rindas informācija. 

Kad pārdošanas cenrādis ir noteikts, sistēma pabeidz tālāk norādītās darbības, lai ievadītu vienības pārdošanas noklusējuma cenu.

1. Sistēma saskaņo lauku **Kategorija** un **Vienība** kombināciju **Izdevumu** aplēšu rindā pret kategoriju cenu rindām cenrādī.
1. Ja sistēma atrod kategorijas cenas rindu, kurai ir pārdošanas likme lauku kombinācijai **Kategorija** un **Resursu vienība**, tad šī rēķina likme tiek izmantota kā noklusējuma pārdošanas likme.
1. Ja sistēma atrod atbilstošo kategorijas cenas rindu, varat izmantot cenas noteikšanas metodi, lai ievadītu noklusējuma pārdošanas cenu. Tālāk esošajā tabulā ir redzams izmaksu cenu noklusējuma izturēšanās risinājumā Project Operations.

    | Konteksts | Izcenojuma metode | Noklusējuma cena |
    | --- | --- | --- |
    | Novērtējums | Vienības cena | Pamatojoties uz kategorijas cenas rindu. |
    |        | Pašizmaksa | 0.00 |
    |        | Uzcenojums augstāks par izmaksu | 0.00 |
    | Faktiski | Vienības cena | Pamatojoties uz kategorijas cenas rindu. |
    |        | Pašizmaksa | Pamatojoties uz saistīto izmaksu faktiskajiem datiem. |
    |        | Uzcenojums augstāks par izmaksu | Tiek lietots uzcenojums, kā definējis kategorijas cenu rindā saistītās faktiskās izmaksas likmes vienības izmaksu likmē. |

1. Ja sistēma nevar atrast atbilstību lauku **Kategorija** un **Vienība** vērtībām, pārdošanas likme pēc noklusējuma tiek iestatīta uz **0** (nulle).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Pārdošanas likmju noteikšana faktiskajām un novērtētajām materiāla rindām

Aprēķina konteksts **Materiāliem** attiecas uz:

- **Materiālu** piedāvājuma rindas informācija.
- **Materiālu** līguma rindas informācija.
- Projekta materiālu aprēķinu rindas.

Faktiskais konteksts **Materiāliem** attiecas uz:

- Ierakstu un labošanas žurnālu rindas **Materiāliem**.
- Žurnālu rindas, kas tiek izveidotas, kad tiek iesniegts Materiālu lietojuma žurnāls.
- **Materiālu** rēķina rindas informācija. 

Kad pārdošanas cenrādis ir noteikts, sistēma pabeidz tālāk norādītās darbības, lai ievadītu vienības pārdošanas noklusējuma cenu.

1. Sistēma saskaņo lauku **Produkts** un **Vienība** kombināciju **Materiālu** aprēķinu rindā ar cenrāža vienību rindām cenrādī.
1. Ja sistēma atrod cenrāža elementa rindu, kuras pārdošanas likme lauku **Produkts** un **Vienība** kombinācijai un ja cenu noteikšanas metodei ir **Valūtas summa**, tiek izmantota cenrāža rindā norādītā pārdošanas cena. 
1. Ja lauku **Produkts** un **Vienība** vērtības nesaskan vai ja cenas noteikšanas metode nav **Valūtas summa**, pārdošanas likme pēc noklusējuma tiek iestatīta uz **0** (nulli). Tā notiek tāpēc, ka Project Operations projektā izmantotajiem materiāliem atbalsta tikai cenu noteikšanas metodi **Valūtas summa**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
