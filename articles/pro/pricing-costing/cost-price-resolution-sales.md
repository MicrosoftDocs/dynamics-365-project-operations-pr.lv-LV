---
title: Izmaksu likmju noteikšana projekta aplēsēm un faktiskajiem faktiskajiem faktoriem
description: Šajā rakstā ir sniegta informācija par to, kā tiek noteiktas projekta tāmes un faktiskās izmaksas.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410159"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Izmaksu likmju noteikšana projekta aplēsēm un faktiskajiem faktiskajiem faktoriem

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Lai noteiktu izmaksu cenrādi un izmaksu likmes tāmes un faktiskajos kontekstos, sistēma izmanto informāciju saistītā projekta laukos **Datums**, **Valūta** un **Līgumslēdzēja vienība**.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Izmaksu likmju noteikšana aplēses un laika faktiskos kontekstos

Laika **aplēses konteksts** attiecas uz:

- Citātu rindas informācija par **laiku**.
- Detalizēta informācija par līguma rindiņu par **laiku**.
- Resursu piešķiršana projektā.

Faktiskais laika **konteksts** attiecas uz:

- Ierakstu un labojumu žurnāla rindas **laikam**.
- Žurnāla rindas, kas tiek izveidotas, kad tiek iesniegts laika ieraksts.

Kad izmaksu cenrādis ir noteikts, sistēma veic tālāk norādītās darbības, lai ievadītu noklusējuma izmaksu likmi.

1. Sistēma atbilst **lauku Lomu** un **resursu vienība** kombinācijai **aplēses** vai faktiskā laika kontekstā ar lomu cenu rindām cenrādī. Šajā saskaņošanā tiek pieņemts, ka jūs izmantojat standarta cenu noteikšanas kategorijas darbaspēka izmaksām. Ja esat konfigurējis sistēmu, lai tā atbilstu laukiem, kas nav lomu **un** resursu vienība **vai ir papildus tiem**, tiek izmantota cita kombinācija, lai izgūtu atbilstošu lomu cenu rindu.
1. Ja sistēma atrod lomu cenu rindu, kurai ir izmaksu likme kombinācijai **Lomu** un **resursu vienība**, šī izmaksu likme tiek izmantota kā noklusējuma izmaksu likme.
1. Ja sistēma neatbilst lomu un resursu vienības **vērtībām, tā izgūst lomu cenu rindas, kurām ir atbilstošas vērtības laukā Loma**, **bet kurām ir nulles vērtības laukam** Resursu vienība **.** **·** Pēc tam, kad sistēmai ir atbilstošs lomu cenu ieraksts, izmaksu likme no šī ieraksta tiks izmantota kā noklusējuma izmaksu likme.

> [!NOTE]
> Ja konfigurējat atšķirīgu lauku Lomu **un** resursu vienība **prioritāšu noteikšanu** vai ja jums ir citas dimensijas, kurām ir augstāka prioritāte, iepriekšējā darbība attiecīgi mainīsies. Sistēma izgūst lomu cenu ierakstus, kuru vērtības atbilst katrai cenu noteikšanas dimensijas vērtībai prioritārā secībā. Rindas, kurās šīm dimensijām ir nulles vērtības, ir pēdējās.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Izmaksu likmju noteikšana faktiskajās un aplēstajās izdevumu rindās

Izdevumu **aplēses konteksts** attiecas uz:

- Detalizēta informācija par izdevumu **piedāvājuma rindiņu**.
- Detalizēta informācija par līguma rindiņu **izdevumiem**.
- Projekta izdevumu tāmes.

Faktiskais izdevumu **konteksts** attiecas uz:

- Ierakstu un korekcijas žurnāla rindas izdevumam **Izdevumi**.
- Žurnāla rindas, kas tiek izveidotas, kad tiek iesniegts izdevumu ieraksts.

Kad izmaksu cenrādis ir noteikts, sistēma veic tālāk norādītās darbības, lai ievadītu noklusējuma izmaksu likmi.

1. Sistēma atbilst kategorijas **un** **vienības** lauku kombinācijai aplēses **vai faktiskā izdevumu** kontekstā ar kategorijas cenu rindām cenrādī.
1. Ja sistēma atrod kategorijas cenu rindu, kurai ir izmaksu likme kategorijas **un** vienības **kombinācijai**, šī izmaksu likme tiek izmantota kā noklusējuma izmaksu likme.
1. Ja sistēma neatbilst kategorijas **un** **vienības** vērtībām, cena pēc noklusējuma tiek iestatīta uz **0** (nulle).
1. Aplēses kontekstā, ja sistēma var atrast atbilstošu kategorijas cenu rindu, bet cenu noteikšanas metode ir kaut kas cits, nevis **cena par vienību**, izmaksu likme pēc noklusējuma tiek iestatīta uz **0** (nulle).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Izmaksu likmju noteikšana materiāla faktiskajās un aplēstajās rindās

Materiāla **aplēses konteksts** attiecas uz:

- Citātu rindas informācija **materiālam**.
- Detalizēta informācija par līguma līniju **materiālam**.
- Projekta materiālu tāmes.

Materiāla **faktiskais konteksts** attiecas uz:

- Ieraksta un korekcijas žurnāla rindas **materiālam**.
- Žurnāla rindas, kas tiek izveidotas, kad tiek iesniegts materiāla lietojuma žurnāls.

Kad izmaksu cenrādis ir noteikts, sistēma veic tālāk norādītās darbības, lai ievadītu noklusējuma izmaksu likmi.

1. Sistēma izmanto lauku Produkts un Vienība kombināciju **aplēses** vai faktiskā materiāla kontekstā attiecībā pret **cenrāža pozīciju rindām cenrādī**.**·**
1. Ja sistēma atrod cenrāža krājuma rindu, kurai ir izmaksu likme preču **un** vienības **kombinācijai**, šī izmaksu likme tiek izmantota kā noklusējuma izmaksu likme.
1. Ja sistēma neatbilst **produkta** un **vienības** vērtībām, vienības izmaksas pēc noklusējuma tiek iestatītas uz **0** (nulle).
1. Aplēses vai faktiskā kontekstā, ja sistēma var atrast atbilstošu cenrāža rindu, bet cenu noteikšanas metode ir kaut kas cits, nevis **Valūtas summa**, vienības izmaksas pēc noklusējuma tiek iestatītas uz 0.**·** Šī problēma rodas, jo Project Operations atbalsta tikai **valūtas summas** cenu noteikšanas metodi materiāliem, kas tiek izmantoti projektā.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
