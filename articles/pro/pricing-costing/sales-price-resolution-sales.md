---
title: Pārdošanas cenu noteikšana projekta aplēsēm un faktiskajiem datiem
description: Šajā rakstā ir sniegta informācija par to, kā tiek noteiktas projekta aplēšu un faktisko vērtību pārdošanas cenas.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410128"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Pārdošanas cenu noteikšana projekta aplēsēm un faktiskajiem datiem

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Lai noteiktu pārdošanas cenas aplēsēm un faktiskajiem datiem korporācijā Microsoft Dynamics 365 Project Operations, sistēma vispirms izmanto datumu un valūtu ienākošajā aplēsē vai faktiskajā kontekstā, lai noteiktu pārdošanas cenrādi. Konkrēti faktiskajā kontekstā sistēma izmanto lauku Transakcijas **datums**, lai noteiktu, kurš cenrādis ir piemērojams. Pēc pārdošanas cenrāža noteikšanas sistēma nosaka pārdošanas vai rēķina likmi.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Pārdošanas likmju noteikšana faktiskajās un aptuvenajās laika rindās

Laika **aplēses konteksts** attiecas uz:

- Citātu rindas informācija par **laiku**.
- Detalizēta informācija par līguma rindiņu par **laiku**.
- Resursu piešķiršana projektā.

Faktiskais laika **konteksts** attiecas uz:

- Ierakstu un labojumu žurnāla rindas **laikam**.
- Žurnāla rindas, kas tiek izveidotas, kad tiek iesniegts laika ieraksts.
- Detalizēta informācija par rēķina rindiņu par **laiku**. 

Pēc pārdošanas cenrāža noteikšanas sistēma veic tālāk norādītās darbības, lai ievadītu noklusējuma rēķina likmi.

1. Sistēma atbilst **lauku Lomu** un **resursu vienība** kombinācijai **aplēses** vai faktiskā laika kontekstā ar lomu cenu rindām cenrādī. Veicot atbilstošu atbilstību, tiek pieņemts, ka rēķinu likmēm izmantojat standarta cenu kategorijas. Ja cenu noteikšana ir konfigurēta tā, lai **tās pamatā būtu lauki, kas nav lomu** un **resursu vienība** vai ir papildus tiem, šī lauku kombinācija tiek izmantota, lai izgūtu atbilstošu lomu cenu rindu.
1. Ja sistēma atrod lomu cenu rindu, kurai ir rēķina likme **lomas** un **resursu vienības** kombinācijai, šī rēķina likme tiek izmantota kā noklusējuma rēķina likme.
1. Ja sistēma nevar saskaņot lomu un resursu vienības **vērtību, tā izgūst lomu cenu rindas, kurām ir atbilstošas vērtības laukā Loma**, **bet kurām ir vērtības Null laukos** Resursu vienība **.** **·** Pēc tam, kad sistēma ir atradusi atbilstošu lomu cenas ierakstu, šī ieraksta rēķina likme tiks izmantota kā noklusējuma rēķina likme. Šajā saskaņošanā tiek pieņemta standarta konfigurācija lomas **relatīvajai prioritātei** **pret resursu piešķiršanas vienību** kā pārdošanas cenu dimensijai.

> [!NOTE]
> Ja konfigurējat atšķirīgu lauku Lomu **un** resursu vienība **prioritāšu noteikšanu** vai ja jums ir citas dimensijas, kurām ir augstāka prioritāte, iepriekšējā darbība attiecīgi mainīsies. Sistēma izgūst lomu cenu ierakstus, kuru vērtības atbilst katrai cenu noteikšanas dimensijas vērtībai prioritārā secībā. Rindas, kurās šīm dimensijām ir nulles vērtības, ir pēdējās.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Pārdošanas likmju noteikšana faktiskajās un aplēses rindās izdevumam Izdevumi

Izdevumu **aplēses konteksts** attiecas uz:

- Detalizēta informācija par izdevumu **piedāvājuma rindiņu**.
- Detalizēta informācija par līguma rindiņu **izdevumiem**.
- Projekta izdevumu tāmes rindas.

Faktiskais izdevumu **konteksts** attiecas uz:

- Ierakstu un korekcijas žurnāla rindas izdevumam **Izdevumi**.
- Žurnāla rindas, kas tiek izveidotas, kad tiek iesniegts izdevumu ieraksts.
- Detalizēta informācija par rēķina rindiņu izdevumam **Izdevumi**. 

Pēc pārdošanas cenrāža noteikšanas sistēma veic tālāk norādītās darbības, lai ievadītu noklusējuma vienības pārdošanas cenu.

1. Sistēma atbilst lauku Kategorija un Vienība kombinācijai **izdevumu aplēses** **rindā ar kategoriju cenu rindām cenrādī.** **·**
1. Ja sistēma atrod kategorijas cenu rindu, kurā ir pārdošanas likme kombinācijai **Kategorija** un **Vienība**, šis pārdošanas līmenis tiek izmantots kā noklusējuma pārdošanas līmenis.
1. Ja sistēma atrod atbilstošu kategorijas cenu rindu, iespējams, tiks izmantota cenu noteikšanas metode, lai ievadītu noklusējuma pārdošanas cenu. Nākamajā tabulā ir parādīta izdevumu cenu noklusējuma darbība programmā Project Operations.

    | Konteksts | Izcenojuma metode | Noklusējuma cena |
    | --- | --- | --- |
    | Novērtējums | Vienības cena | Pamatojoties uz kategorijas cenu līniju. |
    |        | Pašizmaksa | 0.00 |
    |        | Uzcenojums augstāks par izmaksu | 0.00 |
    | Faktiski | Vienības cena | Pamatojoties uz kategorijas cenu līniju. |
    |        | Pašizmaksa | Pamatojoties uz faktiskajām saistītajām izmaksām. |
    |        | Uzcenojums augstāks par izmaksu | Uzcenojums tiek piemērots, kā noteikts kategorijas cenu rindā, saistīto faktisko izmaksu vienības izmaksu likmei. |

1. Ja sistēma neatbilst kategorijas **un** **vienības** vērtībām, pārdošanas likme pēc noklusējuma ir iestatīta uz **0** (nulle).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Pārdošanas likmju noteikšana materiāla faktiskajās un tāmes rindās

Materiāla **aplēses konteksts** attiecas uz:

- Citātu rindas informācija **materiālam**.
- Detalizēta informācija par līguma līniju **materiālam**.
- Projekta materiālu tāmes rindas.

Materiāla **faktiskais konteksts** attiecas uz:

- Ieraksta un korekcijas žurnāla rindas **materiālam**.
- Žurnāla rindas, kas tiek izveidotas, kad tiek iesniegts materiāla lietojuma žurnāls.
- Detalizēta informācija par rēķina rindiņu **materiālam**. 

Pēc pārdošanas cenrāža noteikšanas sistēma veic tālāk norādītās darbības, lai ievadītu noklusējuma vienības pārdošanas cenu.

1. Sistēma atbilst laukam Prece un Vienība, kas atrodas materiāla **aplēses rindā, kombinācijai** **ar cenrāža pozīciju rindām cenrādī.** **·**
1. Ja sistēma atrod cenrāža krājuma rindu, kurā ir pārdošanas kurss preču un vienības kombinācijai **, un ja cenu noteikšanas metode ir** Valūtas summa **, tiek izmantota pārdošanas cena, kas ir norādīta cenrāža rindā.** **·** 
1. **Ja lauka Preces** un **Vienības** vērtības neatbilst vai ja cenu noteikšanas metode ir kaut kas cits, nevis **summa Valūta**, pārdošanas likme pēc noklusējuma ir iestatīta uz **0** (nulle). Šī problēma rodas, jo Project Operations atbalsta tikai **valūtas summas** cenu noteikšanas metodi materiāliem, kas tiek izmantoti projektā.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
