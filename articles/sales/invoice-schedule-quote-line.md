---
title: Rēķinu grafiki projekta piedāvājuma rindās
description: Šajā tēmā ir sniegta informācija par rēķinu grafiku un atskaites punktu izveidi piedāvājuma rindām.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6b443a353c98fe5c7475d8a95c99abe01cd00987
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601073"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Rēķinu grafiki projekta piedāvājuma rindās

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta piedāvājuma rinda nodrošina iespēju izteikt rēķinu grafiku. Tas nav obligāti piedāvājuma fāzes laikā, jo programma neatbalsta rēķinu izrakstīšanu par projektu, ja tas ir saistīts ar Piedāvājuma rindu. Rēķinu izrakstīšana ir atļauta tikai pēc tam, kad piedāvājums ir iegūts. Ja rēķina grafiks izveidots piedāvājuma fāzē, vienīgā lejupstraumes ietekme ir tas, ka šis rēķinu grafiks tiek kopēts projekta līguma rindā. Ja piedāvājuma fāzē neizveidojat rēķina grafiku, to var izdarīt projekta līguma rindā.

Kopumā rēķinu grafiku nolūks ir ļaut automātiski izveidot rēķinu melnrakstus projekta līguma rindai. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Laika un materiālu rēķina grafika izveide projekta piedāvājuma rindai

Ja projekta piedāvājuma rindas norēķinu metode ir Laiks un materiāli, sistēma ģenerē rēķina grafiku uz datumu pamata. Lai automātiski ģenerētu rēķina grafiku uz datumu pamata, veiciet tālāk norādītās darbības.

1. Dodieties uz **iestatījumi** > **Rēķinu biežumi** un iestatiet rēķina biežumu.
2. Lapā **Piedāvājumi** atveriet Projekta piedāvājumu un cilnē **Kopsavilkums** iestatiet pieprasīto izpildes datumu.
3. Atveriet laika un materiālu piedāvājuma rindu, kurai jāizveido rēķina grafiks, pamatojoties uz datumiem. 
4. Cilnē **Rēķinu grafiks** atlasiet vērtības laukos **Rēķina perioda sākuma datums** un **Rēķini biežums**. 
5. Apakšrežģī atlasiet vienumu **Izveidot rēķinu izrakstīšanas grafiku**.
6. Programma izveido rēķinu izrakstīšanas grafiku, kurā lauki **Rēķina izpildes datums**, **Darījuma pēdējais datums** un **Izpildes statuss** iestatīti tālāk norādītajā veidā.

    - **Rēķina izpildes datums** ir iestatīts uz datumu, ko nosaka, pamatojoties uz rēķinu biežumu.
    - **Darījuma pēdējais datums** ir iestatīts uz dienu pirms **Rēķina izpildes datuma**.
    - **Izpildes statuss** tiek automātiski iestatīts uz **Nav palaists**. Kad automātiskās rēķina izveides uzdevums tiek pildīts attiecībā uz noteiktu rēķina izpildes datumu, šis lauks tiek atjaunināts, rādot **Izpilde neveiksmīga** vai **Izpilde neizdevās**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Fiksētas cenas rēķina grafika izveide projekta piedāvājuma rindai

Ja projekta piedāvājuma rindai ir **Fiksēta** norēķinu metode, sistēma izveido uz atskaites punktiem balstītu rēķina grafiku. Izpildiet tālāk aprakstītās darbības, lai automātiski izveidotu šo grafiku fiksētai atskaites punktu kopai, kas ir vienmērīgi izplatīti kalendāra periodā.

1. Dodieties uz **iestatījumi** > **Rēķinu biežumi** un iestatiet rēķina biežumu.
2. Lapā **Piedāvājumi** atveriet Projekta piedāvājumu un cilnē **Kopsavilkums** iestatiet pieprasīto izpildes datumu.
3. Atveriet fiksētās cenas piedāvājuma rindu, kurai ir nepieciešams izveidot atskaites punktu grafiku. 
4. Cilnē **Rēķinu grafiks** atlasiet vērtības laukos **Rēķina perioda sākuma datums** un **Rēķini biežums**. 
5. Apakšrežģī atlasiet vienumu **Izveidot periodiskos atskaites punktus**.
6. Programma izveido rēķinu grafiku ar atskaites punkta nosaukumu, datumu un summu.

    - Atskaites punkta nosaukums ir iestatīts uz datumu, ko nosaka, pamatojoties uz rēķinu biežumu.
    - Atskaites punkta datums ir iestatīts uz datumu, ko nosaka, pamatojoties uz rēķinu biežumu.
    - Atskaites punkta summa tiek aprēķināta, dalot piedāvājuma summu projekta piedāvājuma rindā ar atskaites punktu skaitu, kas noteikts pēc biežuma, un norēķinu sākuma datuma un pieprasītajiem izpildes datumiem.
    - Ja Piedāvājuma rindai ir arī prognozējamā nodokļu summa, šī vērtība tiek vienmērīgi sadalīta starp visiem atskaites punktiem, izveidojot periodiskos atskaites punktus.

### <a name="manually-create-milestones"></a>Atskaites punktu manuāla izveide

Fiksētas cenas atskaites punktus var izveidot arī manuāli, ja tie nav periodiski sadalīti. Lai manuāli izveidotu atskaites punktu, veiciet tālāk aprakstītās darbības.

Atveriet Fiksētās cenas piedāvājuma rindu, kurai ir nepieciešams izveidot atskaites punktu. Cilnes **Rēķinu grafiks** apakšrežģī atlasiet **+ Izveidot jaunu piedāvājuma rindas atskaites punktu** un ievadiet nepieciešamo informāciju, pamatojoties uz tālāk redzamo tabulu.

| **Lauks** | **Atrašanās vieta** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Atskaites punkta nosaukums | Ātrā izveide | Atskaites punkta nosaukums. | Tas tiek izplatīts arī uz projekta līguma rindas atskaites punktu un rēķinu |
| Projekta uzdevums | Ātrā izveide | Ja atskaites punkts ir saistīts ar projekta uzdevumu, šo atsauci var izmantot, lai pievienotu pielāgotu loģiku, lai noteiktu atskaites punkta statusu, pamatojoties uz uzdevuma statusu. | Programmā šī atsauce uz uzdevumu nerada lejupstraumes ietekmi. |
| Atskaites punkta datums | Ātrā izveide | Iestatiet datumu, kurā automātiskās rēķina izveides procesam ir jāpārbauda šī atskaites punkta statuss, lai apsvērtu rēķina izrakstīšanu. | Tas tiek izplatīts arī uz projekta līguma rindas atskaites punktu un rēķinu. |
| Rēķina statuss | Ātrā izveide | Kad ir izveidots atskaites punkts, šis statuss vienmēr ir iestatīts uz **Nav gatavs rēķina izrakstīšanai**. | Tas tiek izplatīts arī uz projekta līguma rindas atskaites punktu un rēķinu. |
| Rindas summa | Ātrā izveide | Atskaites punkta summa vai vērtība, par ko tiks izrakstīts rēķins klientam. | Tas tiek izplatīts arī uz projekta līguma rindas atskaites punktu un rēķinu. |
| Nodoklis | Ātrā izveide | Nodokļu summa, kas tiks piemērota atskaites punktam. | Tas tiek izplatīts arī uz projekta līguma rindas atskaites punktu un rēķinu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]