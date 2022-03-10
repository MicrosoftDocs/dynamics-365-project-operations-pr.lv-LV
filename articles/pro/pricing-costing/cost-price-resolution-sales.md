---
title: Izmaksu atrisināšana projekta aprēķinos un faktiskajās vērtībās
description: Šajā tēmā ir sniegta informācija par to, kā tiek atrisinātas projekta aprēķinu un faktisko datu izmaksas.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997570"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Izmaksu atrisināšana projekta aprēķinos un faktiskajās vērtībās 

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Lai atrisinātu izmaksas un izmaksu cenrādi attiecībā uz aprēķiniem un faktiskajiem rādītājiem, sistēma izmanto informāciju saistītā projekta laukos **Datums**, **Valūta** un **Līgumslēdzēja vienība**. Kad izmaksu cenrādis ir atrisināts, programma atrisina izmaksu likmi.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Izmaksu likmju atrisināšana attiecībā uz faktiskajām un novērtējuma rindām par laiku

Laika novērtējuma rindas norāda uz piedāvājuma un līguma rindu detalizētu informāciju par laika un resursu piešķirēm projektā.

Kad ir atrisināts izmaksu cenrādis, laika novērtējuma rindas lauki **Loma** un **Resursu vienība** tiek saskaņoti ar lomas cenu rindām cenrādī. Šajā saskaņošanā tiek pieņemts, ka darba spēka izmaksām lietojat standarta cenu noteikšanas dimensijas. Ja esat konfigurējis sistēmu saskaņot laukus, nevis laukus **Loma** un **Resursu vienība** (vai papildus tiem), tad cita kombinācija tiks izmantota, lai izgūtu atbilstošo lomas cenu rindu. Ja lietojumprogramma atrod lomas cenu rindu, kurai ir izmaksu likme lauku rindai **Loma** un **Resursu vienība**, tā ir noklusējuma izmaksu likme. Ja lietojumprogramma nespēj saskaņot lauku **Loma** un **Resursu vienība** vērtības, tad tā iegūst lomu cenu rindas ar atbilstošu lomu, bet anulē vērtības vienumam **Resursu vienība**. Kad ir atrasts atbilstošs lomu cenu ieraksts, šim ierakstam tiek atjaunotas izmaksu likmju noklusējuma vērtības. 

> [!NOTE]
> Ja laukiem **Loma** un **Resursu vienība** konfigurējat atšķirīgas prioritātes vai ja ir citas augstākas prioritātes kategorijas, šī darbība attiecīgi mainīsies. Sistēma iegūst lomu cenu ierakstus ar vērtībām, kas atbilst katrai cenu dimensijas vērtībai prioritātes secībā ar rindām, kurām ir Null vērtības tām dimensijām, kas tuvojas pēdējam.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Izmaksu likmju atrisināšana attiecībā uz faktiskajām un novērtējuma rindām par izdevumiem

Novērtēšanas rindas izdevumiem attiecas uz piedāvājuma un līguma rindas informāciju izdevumiem, kā arī izdevuma novērtēšanas rindām projektā.

Pēc tam, kad ir atrisināts cenrāža saraksts, sistēma izmanto lauku **Kategorija** un **Vienība** kombināciju izmaksu novērtējuma rindā, lai saskaņotu ar **Kategoriju cenas** rindām atrisinātajā cenrādī. Ja sistēma atrod kategorijas cenas rindu, kurai ir izmaksu likme lauku kombinācijai **Kategorija** un **Vienība**, tad izmaksu likme ir tiek noklusēta. Ja sistēma nevar saskaņot vērtības **Kategorija** un **Vienība** vai ja tā nevar atrast atbilstošu kategorijas cenas rindu, bet cenu noteikšanas metode nav **Cena par vienību**, izmaksu likme pēc noklusējuma ir nulle (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Izmaksu likmju atrisināšana faktiskajām un aprēķinātajām materiālu rindām

Materiālu aprēķinu rindas attiecas uz piedāvājuma un līguma rindu informāciju par materiāliem un materiālu aprēķina rindām projektā.

Kad ir atrisināts izmaksu cenrādis, sistēma izmanto lauku **Produkts** un **Vienība** kombināciju materiālu aprēķina rindai, lai nodrošinātu tās atbilstību atrisinātā cenrāža rindām **Cenrāža elementi**. Ja sistēma atrod produkta cenas rindu, kuras izmaksu likmei ir lauku **Produkts** un **Vienība** kombinācija, izmaksu likmei ir noklusējuma vērtība. Ja sistēma neatrod atbilstību lauku **Produkts** un **Vienība** vērtībām vai atrod atbilstību cenrāža elementa rindai, bet cenu noteikšanas metodes pamatā ir standarta izmaksas vai pašreizējās izmaksas un neviena no tām nav definēta produktam, vienības izmaksām noklusējuma vērtība ir nulle.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
