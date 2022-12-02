---
title: Izmaksu likmju noteikšana projekta aprēķinos un faktiskajos datos
description: Šajā rakstā sniegta informācija par to, kā tiek noteiktas izmaksu likmes projektos balstītiem aprēķiniem un datiem.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475241"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Izmaksu likmju noteikšana projekta aprēķinos un faktiskajos datos

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Lai noteiktu izmaksu likmes aprēķiniem un datiem programmā Microsoft Dynamics 365 Project Operations, sistēma vispirms izmantot ienākošā aprēķina vai faktiskā konteksta datumu un valūtu, lai noteiktu izmaksu cenrādi. Īpaši datu kontekstā sistēma izmanto lauku **Transakcijas datums**, lai noteiktu, kurš cenrādis ir lietojams. Ienākošā aprēķina vai datu vērtība **Transakcijas datums** tiek salīdzināta ar cenrāža vērtībām **Faktiskais sākums (atkarīgs no laika joslas)** un **Faktiskās beigas (atkarīgs no laika joslas)**. Kad izmaksu cenrādis ir noteikts, sistēma nosaka izmaksu likmi. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Izmaksu likmju noteikšana attiecībā uz novērtējuma un faktisko datu kontekstiem par laiku

Aprēķina konteksts **Laikam** attiecas uz:

- **Laika** piedāvājuma rindas informācija.
- **Laika** līguma rindas informācija.
- Resursu piešķīrumi projektam.

Datu konteksts **Laikam** attiecas uz:

- Ierakstu un labošanas žurnālu rindas **Laikam**.
- Žurnālu rindas, kas tiek izveidotas, kad tiek iesniegts laika ieraksts.

Pēc tam, kad ir noteikts izmaksu cenrādis, sistēma izpilda tālāk norādītās darbības, lai ievadītu izmaksu likmes noklusējuma vērtību.

1. Sistēma saskaņo lauku **Loma** un **Resursu vienība** kombināciju novērtējuma vai datu kontekstā **Laiks** ar lomas cenu rindām cenrādī. Šajā saskaņošanā tiek pieņemts, ka darba spēka izmaksām lietojat standarta cenu noteikšanas dimensijas. Ja esat konfigurējis sistēmu saskaņot citus laukus, nevis laukus **Loma** un **Resursu vienība** (vai papildus tiem), tad cita kombinācija tiks izmantota, lai izgūtu atbilstošo lomas cenu rindu.
1. Ja sistēma atrod lomas cenu rindu, kurai ir izmaksu likme lauku rindai **Loma** un **Resursu vienība**, šī izmaksu likme tiek izmantota kā noklusējuma izmaksu likme.
1. Ja sistēma nespēj saskaņot vērtības **Loma** un **Resursu vienība**, tad tā iegūst lomu cenas rindas ar atbilstošu vērtību laukam **Loma**, bet nulles vērtības laukam **Resursu vienība**. Pēc tam, kad sistēma ir atradusi atbilstošu lomas cenas ierakstu, šī ieraksta izmaksu likme tiek izmantota kā noklusējuma izmaksu likme.

> [!NOTE]
> Ja laukiem **Loma** un **Resursu vienība** konfigurējat atšķirīgas prioritātes vai ja ir citas augstākas prioritātes kategorijas, iepriekšējā darbība attiecīgi mainīsies. Sistēma izgūst lomu cenu ierakstus, kuriem ir vērtības, kas atbilst katrai cenas noteikšanas scenārija vērtībai prioritārā secībā. Rindas ar vērtībām Null šīm dimensijām ir pēdējās.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Izmaksu likmju noteikšana attiecībā uz faktiskajām un novērtējuma rindām par izdevumiem

Aprēķina konteksts **Izdevumiem** attiecas uz:

- **Izdevumu** piedāvājuma rindas informācija.
- **Izdevumu** līguma rindas informācija.
- Izdevumu aplēses projektā.

Faktiskais konteksts **Izdevumiem** attiecas uz:

- Ierakstu un labošanas žurnālu rindas **Izdevumiem**.
- Žurnālu rindas, kas tiek izveidotas, kad tiek iesniegts izdevumu ieraksts.

Pēc tam, kad ir noteikts izmaksu cenrādis, sistēma izpilda tālāk norādītās darbības, lai ievadītu izmaksu likmes noklusējuma vērtību.

1. Sistēma saskaņo vienuma **Izdevumi** novērtējuma vai faktisko datu konteksta lauku **Kategorija** un **Vienība** kombināciju ar kategoriju cenu rindām cenrādī.
1. Ja sistēma atrod kategorijas cenas rindu, kurai ir izmaksu likme lauku kombinācijai **Kategorija** un **Vienība**, tad šī izmaksu likme tiek izmantota kā noklusējuma izmaksu likme.
1. Ja sistēma nevar atrast atbilstību lauku **Kategorija** un **Vienība** vērtībām, cena pēc noklusējuma tiek iestatīta uz **0** (nulle).
1. Ja novērtējuma kontekstā sistēma nevar atrast atbilstošu kategorijas cenas rindu, bet cenu noteikšanas metode ir cita, nevis **Cena par vienību**, izmaksu likme pēc noklusējuma tiek iestatīta uz **0** (nulle).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Izmaksu likmju noteikšana faktiskajām un aprēķinātajām materiālu rindām

Aprēķina konteksts **Materiāliem** attiecas uz:

- **Materiālu** piedāvājuma rindas informācija.
- **Materiālu** līguma rindas informācija.
- Projekta materiālu aprēķini.

Faktiskais konteksts **Materiāliem** attiecas uz:

- Ierakstu un labošanas žurnālu rindas **Materiāliem**.
- Žurnālu rindas, kas tiek izveidotas, kad tiek iesniegts Materiālu lietojuma žurnāls.

Pēc tam, kad ir noteikts izmaksu cenrādis, sistēma izpilda tālāk norādītās darbības, lai ievadītu izmaksu likmes noklusējuma vērtību.

1. Sistēma izmanto vienuma **Materiāls** novērtējuma vai faktisko datu konteksta lauku **Produkts** un **Vienība** kombināciju attiecībā pret cenrāža elementu rindām cenrādī.
1. Ja sistēma atrod cenrāža elementa rindu, kurai ir izmaksu likme lauku kombinācijai **Produkts** un **Vienība**, tad šī izmaksu likme tiek izmantota kā noklusējuma izmaksu likme.
1. Ja sistēma nevar atrast atbilstību lauku **Produkts** un **Vienība** vērtībām, vienības izmaksas pēc noklusējuma tiek iestatītas uz **0** (nulle).
1. Ja novērtējuma vai faktisko datu kontekstā sistēma nevar atrast atbilstošu cenrāža elementa rindu, bet cenu noteikšanas metode ir cita, nevis **Valūtas summa**, vienības izmaksas pēc noklusējuma tiek iestatītas uz **0** (nulle). Tā notiek tāpēc, ka Project Operations projektā izmantotajiem materiāliem atbalsta tikai cenu noteikšanas metodi **Valūtas summa**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
