---
title: Rēķina grafika izveidošana projekta līguma rindā
description: Šajā rakstā sniegta informācija par to, kā izveidot rēķinu grafikus un atskaites punktus līguma rindās.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 490a61b67f54bdad95ecfce905191c381dddc85b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915009"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Rēķina grafika izveidošana projekta līguma rindā 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Jūs varat izveidot rēķinu grafiku projekta līguma rindai. Rēķinu izrakstīšana ir atļauta tikai pēc tam, kad līgums ir iegūts un jūs izveidojat projekta līgumu. Rēķina grafiks ļauj automātiski izveidot rēķinu melnrakstus projekta līguma rindai. Ja tomēr izveidojat rēķinus tikai manuāli, varat izlaist rēķinu grafiku izveidošanu līguma rindām.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Laika un materiālu rēķina grafika izveide līguma rindai

Ja projekta līguma rindai ir laika un materiālu norēķinu metode, varat izveidot rēķina grafiku uz datumu pamata. Lai automātiski ģenerētu rēķina grafiku uz datumu pamata, veiciet tālāk norādītās darbības.

1. Dodieties uz **iestatījumi** > **Rēķinu biežumi** un iestatiet rēķinu biežumu.
2. Atveriet projekta līguma ierakstu un cilnes **Kopsavilkums** laukā **Pieprasītais piegādes datums** atlasiet datumu.
3. Atveriet līguma rindu **Laiks un materiāli**, kurai veidojat rēķina grafiks, pamatojoties uz datumiem. 
4. Cilnē **Rēķinu grafiks** atlasiet norēķinu sākuma datumu un rēķinu biežumu.
5. Apakšrežģī atlasiet vienumu **Izveidot rēķinu izrakstīšanas grafiku**. Rēķinu grafiks tiek ģenerēts ar šādi iestatītiem laukiem **Rēķina izpildes datums**, **Darījuma pēdējais datums** un **Izpildes statuss**.

    - **Rēķina izpildes datums**: šis ir datums, ko nosaka, pamatojoties uz rēķinu biežumu.
    - **Darījuma pēdējais datums**: diena pirms rēķina izpildes datuma.
    - **Izpildes statuss**: automātiski iestatīts uz **Nav palaists**. Kad automātiskās rēķina izveides uzdevums tiek pildīts attiecībā uz noteiktu rēķina izpildes datumu, šis lauks tiek atjaunināts, rādot **Izpilde neveiksmīga** vai **Izpilde neizdevās**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Fiksētas cenas rēķina grafika izveide līguma rindai

Ja līguma rindai ir fiksēta norēķinu metode, jūs varat izveidot uz atskaites punktiem balstītu rēķina grafiku. 

> [!NOTE]
> Atskaites punktus nevar izveidot līguma rindā, ja līguma rindai nav kartēta projekta.

Izpildiet tālāk aprakstītās darbības, lai izveidotu atskaites punktu rēķinu grafiku fiksētai grupai atskaites punktu, kas ir vienmērīgi izplatīti kalendāra periodā.

1. Dodieties uz **iestatījumi** > **Rēķinu biežumi** un iestatiet rēķinu biežumu.
2. Atveriet projekta līguma ierakstu un cilnes **Kopsavilkums** laukā **Pieprasītais piegādes datums** atlasiet datumu.
3. Atveriet līguma rindu **Fiksēta cena**, kurai izveidojat atskaites punktu grafiku. Cilnē **Norēķinu atskaites punkti** atlasiet norēķinu sākuma datumu un rēķinu biežumu. 
4. Apakšrežģī atlasiet vienumu **Izveidot periodiskos atskaites punktus**. Rēķinu grafiks tiek ģenerēts ar šādi iestatītiem laukiem **Atskaites punkta nosaukums**, **Atskaites punkta datums** un **Atskaites punkta summa**.

    - **Atskaites punkta nosaukums**: šo nosaukumu nosaka rēķinu izrakstīšanas biežums.
    - **Atskaites punkta datums**: šis ir datums, ko nosaka, pamatojoties uz rēķinu biežumu.
    - **Atskaites punkta summa**: šī summa tiek aprēķināta, dalot līguma summu līguma rindā ar atskaites punktu skaitu, kas noteikts pēc biežuma, un norēķinu sākuma datuma un pieprasītajiem izpildes datumiem.

    Ja līguma rindai ir vērtība laukā **Aprēķinātā nodokļu summa**, šis lauks ir proporcionāli līdzvērtīgs arī katram atskaites punktam, kad tiek ģenerēti periodiski atskaites punkti.

Norēķinu atskaites punktiem ir jābūt vienāiem ar līguma rindas līgumā ietverto vērtību. Ja tā nav, lapā **Līguma rinda** tiks rādīta kļūda. Kļūdu var labot, pārbaudot, vai norēķinu atskaites punktu kopsumma atbilst līguma rindas vērtībai, izveidojot, rediģējot vai dzēšot atskaites punktus. Pēc izmaiņu veikšanas atsvaidziniet lapu, lai noņemtu kļūdu.

### <a name="manually-create-milestones"></a>Atskaites punktu manuāla izveide

Jūs varat ģenerēt fiksētas cenas atskaites punktus manuāli, ja tie nav periodiski sadalīti. Lai izveidotu jaunu atskaites punktu, veiciet tālāk aprakstītās darbības.

1. Atveriet fiksētās cenas līguma rindu, kurai veidojat atskaites punktu, un apakšrežģa cilnē **Rēķinu grafiks** atlasiet **+ Izveidot jaunu līguma rindas atskaites punktu**. 
2. Lapā **Atskaites punktu izveide** ievadiet nepieciešamo informāciju, pamatojoties uz šo tabulu.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| Atskaites punkta nosaukums | Ātrā izveide | Teksta lauks atskaites punkta nosaukumam. | Tas tiek nodots arī projekta līguma rindas atskaites punktam un rēķinam. |
| Projekta uzdevums | Ātrā izveide | Ja atskaites punkts ir saistīts ar projekta uzdevumu, izmantojiet šo atsauci, lai pievienotu pielāgotu loģiku, lai noteiktu atskaites punkta statusu, pamatojoties uz uzdevuma statusu. | Programmā šī atsauce uz uzdevumu nerada lejupstraumes ietekmi. |
| Atskaites punkta datums | Ātrā izveide | Iestatiet datumu, kurā automātiskās rēķina izveides procesam ir jāpārbauda šī atskaites punkta statuss, lai apsvērtu rēķina izrakstīšanu. | Tas tiek nodots arī projekta līguma rindas atskaites punktam un rēķinam. |
| Rēķina statuss | Ātrā izveide | Kad ir izveidots atskaites punkts, šis statuss vienmēr ir iestatīts uz **Nav gatavs rēķina izrakstīšanai** vai **Nav sākts**. | Tas tiek nodots arī projekta līguma rindas atskaites punktam un rēķinam. |
| Rindas summa | Ātrā izveide | Atskaites punkta summa vai vērtība, par ko tiks izrakstīts rēķins klientam. | Tas tiek nodots arī projekta līguma rindas atskaites punktam un rēķinam. |
| Nodoklis | Ātrā izveide | Atskaites punktam lietotā nodokļu summa. | Tas tiek nodots arī projekta līguma rindas atskaites punktam un rēķinam. |

3. Atlasiet vienumu **Saglabāt un aizvērt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]