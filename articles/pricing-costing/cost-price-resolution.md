---
title: Izmaksu atrisināšana novērtējumiem un faktiskajiem datiem
description: Šajā tēmā ir sniegta informācija par to, kā tiek atrisinātas novērtējumu un faktiskās izmaksas.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d81b521acbfd97127cf056bd41a3249c01108374
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001390"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Izmaksu atrisināšana novērtējumiem un faktiskajiem datiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Lai atrisinātu izmaksas un izmaksu cenrādi attiecībā uz aprēķiniem un faktiskajiem rādītājiem, sistēma izmanto informāciju saistītā projekta laukos **Datums**, **Valūta** un **Līgumslēdzēja vienība**. Kad izmaksu cenrādis ir atrisināts, programma atrisina izmaksu likmi.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Izmaksu likmju atrisināšana attiecībā uz faktiskajām un novērtējuma rindām par laiku

Laika novērtējuma rindas norāda uz piedāvājuma un līguma rindu detalizētu informāciju par laika un resursu piešķirēm projektā.

Kad izmaksu cenrādis ir atrisināts, sistēma izmanto laukus **Loma**, **Resursu uzņēmums** un **Resursu vienība** novērtējuma rindā laikam, lai atrastu lomu cenu rindu atbilstību atrisinātajā cenrādī. Šī saskaņošana pieņem, ka darba izmaksām izmantojat neiekļautas cenas noteikšanas dimensijas. Ja esat konfigurējis sistēmu saskaņot laukus, nevis laukus **Loma**, **Resursu uzņēmums** un **Resursu vienība** (vai papildus tiem), tad cita kombinācija tiks izmantota, lai izgūtu atbilstošo lomas cenu rindu. Ja lietojumprogramma atrod lomas cenu rindu, kurai ir izmaksu likme lauku rindai **Loma**, **Resursu uzņēmums** un **Resursu vienība**, tā ir noklusējuma izmaksu likme. Ja lietojumprogramma nevar atrast atbilstību lauku **Loma**, **Resursu uzņēmums** un **Resursu vienība** vērtībām, tā izgūs lomas cenu rindas ar atbilstošu lomas vērtību, bet laukiem **Resursu vienība** un **Resursu uzņēmums** būs nulles vērtība. Pēc tam, kad ir atrasts atbilstošas lomas cenas ieraksts ar atbilstošu lomas cenas vērtību, izmaksu likmei ir noklusējuma vērtība no šī ieraksta. 

> [!NOTE]
> Ja laukiem **Loma**, **Resursu uzņēmums** un **Resursu vienība** konfigurējat atšķirīgas prioritātes vai ja ir citas augstākas prioritātes kategorijas, šī darbība attiecīgi mainīsies. Sistēma izgūst lomu cenu ierakstus ar vērtībām, kas atbilst katrai cenu noteikšanas domensijas vērtībai secībā, kurā pēdējās ir rindas, kurām šīm dimensijām ir nulles vērtība.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Izmaksu likmju atrisināšana attiecībā uz faktiskajām un novērtējuma rindām par izdevumiem

Novērtēšanas rindas izdevumiem attiecas uz piedāvājuma un līguma rindas informāciju izdevumiem, kā arī izdevuma novērtēšanas rindām projektā.

Kad izmaksu cenrādis ir atrisināts, sistēma izmanto lauku **Kategorija** un **Vienība** kombināciju izdevumu novērtēšanas rindā, lai atrastu atbilstību ar **Kategorijas cena** rindām atrisinātajā cenrādī. Ja sistēma atrod kategorijas cenas rindu, kurai ir izmaksu likme lauku kombinācijai **Kategorija** un **Vienība**, tad izmaksu likme ir tiek noklusēta. Ja sistēma nevar saskaņot **Kategorija** un **Vienība** vērtības vai tā var atrast atbilstošu kategorijas cenu rindu, bet cenas noteikšanas metode nav **Cena par vienību**, tiek atjaunota izmaksu likmes noklusējuma vērtība — nulle (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Izmaksu likmju atrisināšana faktiskajām un aprēķinātajām materiālu rindām

Materiālu aprēķinu rindas attiecas uz piedāvājuma un līguma rindu informāciju par materiāliem un materiālu aprēķina rindām projektā.

Kad ir atrisināts izmaksu cenrādis, sistēma izmanto lauku **Produkts** un **Vienība** kombināciju materiālu aprēķina rindai, lai nodrošinātu tās atbilstību atrisinātā cenrāža rindām **Cenrāža elementi**. Ja sistēma atrod produkta cenas rindu, kuras izmaksu likmei ir lauku **Produkts** un **Vienība** kombinācija, izmaksu likmei ir noklusējuma vērtība. Ja sistēma nevar atrast atbilstību lauku **Produkts** un **Vienība** vērtībām, vienības izmaksas noklusējuma vērtība ir nulle. Šis noklusējums tiks izmantots arī tad, ja ir atbilstoša cenrāža elementa rinda, bet cenu noteikšanas metode tiek pamatota uz standarta izmaksām vai pašreizējām izmaksām, kas nav definētas produktā.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
