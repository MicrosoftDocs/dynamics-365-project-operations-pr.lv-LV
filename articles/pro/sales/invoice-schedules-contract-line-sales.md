---
title: Rēķinu grafiku izveide projekta līguma rindā — Lite
description: Šajā tēmā ir sniegta informācija par rēķinu grafiku un atskaites punktu izveidi.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 728a35b2b69fb63a2b20f218c250365c5068370f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180336"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Rēķinu grafiku izveide projekta līguma rindā — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Jūs varat pievienot rēķinu grafiku projekta līguma rindā. Rēķinu izrakstīšana ir atļauta tikai pēc tam, kad līgums ir iegūts un var tikt veidots Projekta līgums. Rēķinu grafiki ļauj automātiski izveidot rēķinu melnrakstus projekta līguma rindai. Ja vēlaties, lai rēķini vienmēr tiktu izveidoti manuāli, varat izlaist rēķina grafiku izveidi projekta līguma rindā vai līguma rindā.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Laika un materiāla rēķinu grafika izveide projekta līguma rindai

Ja projekta līguma rindai ir laika un materiālu norēķinu metode, varat izveidot rēķina grafiku uz datumu pamata. Lai automātiski ģenerētu rēķina grafiku uz datumu pamata, veiciet tālāk norādītās darbības.

1. Lai iestatītu rēķina izrakstīšanas biežumu, dodieties uz **Iestatījumi** > **Rēķinu izrakstīšanas biežums**.
2. Atveriet projekta līgumu un cilnē **Kopsavilkums** iestatiet pieprasīto piegādes datumu.
3. Atveriet laika un materiālu līguma rindu, kurai vēlaties izveidot uz datumu balstītu rēķinu grafiku. 
4. Cilnē **Rēķina grafiks** atlasiet norēķinu sākuma datumu un rēķinu izrakstīšanas biežumu. 
5. Apakšrežģī atlasiet vienumu **Izveidot rēķinu izrakstīšanas grafiku**.

    Sistēma ģenerē rēķina grafiku ar šādu lauku informāciju:

    - **Rēķina izpildes datums** tiek iestatīts uz datumu, pamatojoties uz rēķinu izrakstīšanas biežumu.
    - **Darījuma pēdējais datums** ir iestatīts uz dienu pirms **Rēķina izpildes datuma**.
    - **Izpildes statuss** tiek automātiski iestatīts uz **Nav palaists**. Kad automātiskās rēķina izveides uzdevums tiek pildīts attiecībā uz noteiktu **Rēķina izpildes datumu**, šis lauks tiek atjaunināts, rādot **Izpilde veiksmīga** vai **Izpilde neizdevās**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Fiksētas cenas rēķinu grafika izveide projekta līguma rindai

Ja projekta līguma rindai ir fiksētas cenas rēķina izrakstīšanas metode, varat izveidot uz atskaites punktu balstītu rēķina grafiku. Izpildiet tālāk aprakstītās darbības, lai automātiski ģenerētu rēķinu izrakstīšanas grafiku saskaņā ar atskaites punktiem, kas atbilst noteiktam atskaites punktam, kas vienādi sadala kalendāru.

1. Lai iestatītu rēķina izrakstīšanas biežumu, dodieties uz **Iestatījumi** > **Rēķinu izrakstīšanas biežums**.
2. Atveriet projekta līgumu un cilnē **Kopsavilkums** iestatiet pieprasīto piegādes datumu.
3. Atveriet fiksētās cenas līguma rindu, kurai ir nepieciešams izveidot atskaites punktu grafiku. 
4. Cilnē **Rēķina grafiks** (Norēķinu atskaites punkti) atlasiet norēķinu sākuma datumu un rēķinu izrakstīšanas biežumu. 
5. Apakšrežģī atlasiet vienumu **Izveidot periodiskos atskaites punktus**.

    Sistēma ģenerē rēķina grafiku ar tālāk norādīto atskaites punktu informāciju.

    - **Atskaites punkta nosaukums** tiek iestatīts uz datumu, ko nosaka, pamatojoties uz rēķina biežumu.
    - **Atskaites punkta datums** tiek iestatīts uz datumu, ko nosaka, pamatojoties uz rēķina biežumu.
    - **Atskaites punkta summa** tiek aprēķināta, sadalot līguma summu projekta līguma rindā ar atskaites punktu skaitu, kas noteikts pēc biežuma, norēķinu sākuma un pieprasītajiem piegādes datumiem.
    - Ja līguma rindai ir vērtība laukā **Novērtētā nodokļu summa**, šis lauks ir arī proporcionāls katram atskaites punktam vienādi, kad tiek ģenerēts periodisks atskaites punkts.

Norēķinu atskaites punktiem ir jābūt vienādiem ar projekta līguma rindu, kuras pamatā ir līguma vērtība. Ja tie nav vienādi, rodas kļūda. Šo kļūdu var novērst, pārbaudot, vai norēķinu atskaites punktu kopsumma ir rindas līguma vērtība, izveidojot, rediģējot vai dzēšot atskaites punktus. Pēc izmaiņu veikšanas atsvaidziniet lapu.

### <a name="manually-create-milestones"></a>Atskaites punktu manuāla izveide

Fiksētas cenas atskaites punktus var ģenerēt manuāli, kad tie netiek periodiski sadalīti. Lai izveidotu manuālu atskaites punktu, izpildiet tālāk norādītās darbības.

1. Atveriet fiksētās cenas līguma rindu, kurai vēlaties izveidot atskaites punktu. 
2. Cilnes **Rēķinu izrakstīšanas grafiks** apakšrežģī atlasiet **+ Izveidot jaunu līguma rindas atskaites punktu**.
3. Veidlapā **Atskaites punktu izveide** ievadiet nepieciešamo informāciju, pamatojoties uz tālāk redzamo tabulu. 

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| Atskaites punkta nosaukums | Ātrā izveide | Teksta lauks atskaites punkta nosaukumam. | Šis lauks ir iekļauts projekta līguma rindas atskaites laukā un rēķinā. |
| Projekta uzdevums | Ātrā izveide | Ja atskaites punkts ir saistīts ar projekta uzdevumu, izmantojiet šo atsauci, lai pievienotu pielāgotu loģiku un iestatītu atskaites punkta statusu, pamatojoties uz uzdevuma statusu. | Šai atsaucei nav nekādas pakārtotas ietekmes uz uzdevumu. |
| Atskaites punkta datums | Ātrā izveide | Datums, kurā automātiskās rēķina izveides procesam ir jāmeklē šī atskaites punkta statuss, lai to izmantotu rēķina izrakstīšanai. | Šis ir iekļauts projekta līguma rindas atskaites laukā un rēķinā. |
| Rēķina statuss | Ātrā izveide | Kad ir izveidots atskaites punkts, šis statuss vienmēr tiek iestatīts uz **Nav gatavs rēķina izrakstīšanai** vai **Nav sākts**. | Šis ir iekļauts projekta līguma rindas atskaites laukā un rēķinā. |
| Rindas summa | Ātrā izveide | To atskaites punktu summa vai vērtība, par ko tiks izrakstīts rēķins klientam. | Šis lauks ir iekļauts projekta līguma rindas atskaites laukā un rēķinā. |
| Nodoklis | Ātrā izveide | Atskaites punktam lietotā nodokļu summa. | Šis ir iekļauts projekta līguma rindas atskaites laukā un rēķinā. |

4. Atlasiet vienumu **Saglabāt un aizvērt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]