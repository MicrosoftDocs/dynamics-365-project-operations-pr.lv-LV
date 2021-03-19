---
title: Izmaksu atrisināšana novērtējumiem un faktiskajiem datiem
description: Šajā tēmā ir sniegta informācija par to, kā tiek atrisinātas novērtējumu un faktiskās izmaksas.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c2fe2a15d38ab5a1f2a93c6db4ed6b7eb9bbd33d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275682"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Izmaksu atrisināšana novērtējumiem un faktiskajiem datiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Lai atrisinātu izmaksas un izmaksu cenrādi attiecībā uz aprēķiniem un faktiskajiem rādītājiem, sistēma izmanto informāciju saistītā projekta laukos **Datums**, **Valūta** un **Līgumslēdzēja vienība**. Kad izmaksu cenrādis ir atrisināts, programma atrisina izmaksu likmi.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Izmaksu likmju atrisināšana attiecībā uz faktiskajām un novērtējuma rindām par laiku

Laika novērtējuma rindas norāda uz piedāvājuma un līguma rindu detalizētu informāciju par laika un resursu piešķirēm projektā.

Kad izmaksu cenrādis ir atrisināts, sistēma izmanto laukus **Loma**, **Resursu uzņēmums** un **Resursu vienība** novērtējuma rindā laikam, lai atrastu lomu cenu rindu atbilstību atrisinātajā cenrādī. Šī saskaņošana pieņem, ka darba izmaksām izmantojat neiekļautas cenas noteikšanas dimensijas. Ja esat konfigurējis sistēmu saskaņot laukus, nevis laukus **Loma**, **Resursu uzņēmums** un **Resursu vienība** (vai papildus tiem), tad cita kombinācija tiks izmantota, lai izgūtu atbilstošo lomas cenu rindu. Ja lietojumprogramma atrod lomas cenu rindu, kurai ir izmaksu likme lauku rindai **Loma**, **Resursu uzņēmums** un **Resursu vienība**, tā ir noklusējuma izmaksu likme. Ja lietojumprogramma nespēj saskaņot lauku **Loma**, **Resursu uzņēmums** un **Resursu vienība** vērtības, tad tā iegūst lomu cenu rindas ar atbilstošu lomu, bet anulē vērtības vienumam **Resursu vienība**. Kad ir atrasts atbilstošs lomu cenu ieraksts, šim ierakstam tiek atjaunotas izmaksu likmju noklusējuma vērtības. 

> [!NOTE]
> Ja laukiem **Loma**, **Resursu uzņēmums** un **Resursu vienība** konfigurējat atšķirīgas prioritātes vai ja ir citas augstākas prioritātes kategorijas, šī darbība attiecīgi mainīsies. Sistēma iegūst lomu cenu ierakstus ar vērtībām, kas atbilst katrai cenu dimensijas vērtībai prioritātes secībā ar rindām, kurām ir Null vērtības tām dimensijām, kas tuvojas pēdējam.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Izmaksu likmju atrisināšana attiecībā uz faktiskajām un novērtējuma rindām par izdevumiem

Novērtēšanas rindas izdevumiem attiecas uz piedāvājuma un līguma rindas informāciju izdevumiem, kā arī izdevuma novērtēšanas rindām projektā.

Kad izmaksu cenrādis ir atrisināts, sistēma izmanto lauku **Kategorija** un **Vienība** kombināciju izdevumu novērtēšanas rindā, lai atrastu atbilstību ar **Kategorijas cena** rindām atrisinātajā cenrādī. Ja sistēma atrod kategorijas cenas rindu, kurai ir izmaksu likme lauku kombinācijai **Kategorija** un **Vienība**, tad izmaksu likme ir tiek noklusēta. Ja sistēma nevar saskaņot **Kategorija** un **Vienība** vērtības vai tā var atrast atbilstošu kategorijas cenu rindu, bet cenas noteikšanas metode nav **Cena par vienību**, tiek atjaunota izmaksu likmes noklusējuma vērtība — nulle (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]