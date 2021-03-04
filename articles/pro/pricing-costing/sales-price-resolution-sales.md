---
title: Aprēķinu un faktisko pārdošanas cenu atrisināšana — Lite
description: Šajā tēmā ir sniegta informācija par pārdošanas cenu atrisināšanu novērtējumos un faktiskajos datos.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 92cebbe851c3cface86d0580e7e060134295e8c2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176755"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Aprēķinu un faktisko pārdošanas cenu atrisināšana — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Ja pārdošanas cenas novērtējumiem un faktiskajiem datiem ir atrisinātas risinājumā Dynamics 365 Project Operations, sistēma vispirms izmanto saistītā projekta piedāvājuma vai līguma datumu un valūtu, lai atrisinātu pārdošanas cenas sarakstu. Pēc tam, kad pārdošanas cenrādis ir atrisināts, sistēma atrisina pārdošanas vai rēķina likmi.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Pārdošanas likmju atrisināšana attiecībā uz faktiskajām un novērtējuma rindām par laiku

Risinājumā Project Operations laika novērtējuma rindas tiek izmantotas, lai norādītu piedāvājuma rindas un līguma rindas informāciju par laiku un projekta resursu piešķires.

Pēc tam, kad ir atrisināts pārdošanas cenrādis, sistēma izpilda tālāk norādītās darbības, lai noklusējuma rēķina likme būtu noklusējuma.

1. Sistēma izmanto aprēķinātās rindas laukus **Lomas** un **Resursu vienība**, lai pieskaņotos lomu cenu rindām atrisinātajā cenrādī. Šī saskaņošana pieņem, ka rēķina likmēm ir izmantotas neiekļautas cenas noteikšanas dimensijas. Ja esat konfigurējis cenu noteikšanu, pamatojoties uz kādu citu lauku, nevis **Loma** un **Resursu vienība**, tad šī ir kombinācija, kas tiks izmantota, lai izgūtu atbilstošo lomas cenu rindu.
2. Ja sistēma atrod lomas cenu rindu, kurai ir rēķina likme lauku rindai **Loma** un **Resursu vienība**, tad šī rēķina likme ir noklusējumā.
3. Ja sistēma nespēj saskaņot lauku **Loma** un **Resursu vienība** vērtības, tad tā iegūst lomu cenas rindas ar atbilstošu lomu, bet nulles vērtības vienumam **Resursu vienība**. Pēc tam, kad sistēma atradīs atbilstošu lomas cenas ierakstu, tā noklusēs šī ieraksta rēķina likmi. Šī atbilstība pieņem ārpus saraksta esošu konfigurāciju **Loma** pret **Resursu vienība** relatīvajai prioritātei kā pārdošanas cenu dimensiju.

> [!NOTE]
> Ja laukiem **Loma** un **Resursu vienība** ir konfigurētas atšķirīgas prioritātes vai ja ir citas augstākas prioritātes kategorijas, šī darbība attiecīgi mainīsies. Sistēma iegūst lomu cenu ierakstus ar atbilstošajām vērtībām katrai cenu dimensijas vērtībai prioritātes secībā ar rindām, kurām ir Null vērtības tām dimensijām, kas tuvojas pēdējam.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Pārdošanas likmju atrisināšana attiecībā uz faktiskajām un novērtējuma rindām par izdevumiem

Risinājumā Project Operations novērtējumu rindas izdevumiem tiek izmantotas, lai norādītu piedāvājuma rindu un līguma rindas detalizētu informāciju par projekta izdevumiem un izdevumu novērtējuma rindām.

Kad pārdošanas cenrādis ir atrisināts, sistēma pabeidz tālāk norādītās darbības, lai noklusētu vienības pārdošanas cenu.

1. Sistēma izmanto novērtējuma rindas lauku **Kategorija** un **Vienība** kombināciju, lai izdevumi sakristu ar kategoriju cenu rindām cenrādī, kas tika atrisināts.
2. Ja sistēma atrod kategorijas cenas rindu, kurai ir pārdošanas likme lauku kombinācijai **Kategorija** un **Resursu vienība**, tad šī rēķina likme ir tiek noklusēta.
3. Ja sistēma atrod atbilstošo kategorijas cenas rindu, varat izmantot cenas noteikšanas metodi, lai noklusējuma pārdošanas cena būtu noklusējuma. Tālāk esošajā tabulā ir redzams izmaksu cenu noklusējuma izturēšanās risinājumā Project Operations.

    | Konteksts | Izcenojuma metode | Noklusētā cena |
    | --- | --- | --- |
    | Novērtējums | Vienības cena | Pamatojoties uz kategorijas cenas rindu |
    | &nbsp; | Pašizmaksa | 0.00 |
    | &nbsp; | Uzcenojums augstāks par izmaksu | 0.00 |
    | Faktiski | Vienības cena | Pamatojoties uz kategorijas cenas rindu |
    | &nbsp; | Pašizmaksa | Pamatojoties uz saistīto izmaksu faktiskajiem datiem |
    | &nbsp; | Uzcenojums augstāks par izmaksu | Lietot uzcenojumu, kā definējis kategorijas cenu rindā saistītās faktiskās izmaksas likmes vienības izmaksu likmē |

4. Ja sistēma nespēj saskaņot **Kategorija** un **Vienība** lauku vērtības, pārdošanas likme pēc noklusējuma ir nulle (0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]