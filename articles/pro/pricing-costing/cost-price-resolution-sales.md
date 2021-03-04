---
title: Izmaksu cenu atrisināšana aprēķiniem un faktiskajiem datiem — Lite
description: Šajā tēmā ir sniegta informācija par to, kā tiek atrisinātas novērtējumu un faktiskās izmaksas.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764602"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Izmaksu cenu atrisināšana aprēķiniem un faktiskajiem datiem — Lite

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
