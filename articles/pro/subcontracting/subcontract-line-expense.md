---
title: Apakšlīguma rindas izdevumu kategorijām
description: Šajā tēmā paskaidrots, kā reģistrēt apakšlīguma izdevumu rindas un izmantot laukus, lai reģistrētu laika iegādi no piegādātājiem.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323830"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Apakšlīguma rindas izdevumu kategorijām

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Apakšlīgumam programmā Dynamics 365 Project Operations var būt izdevumu kategoriju rinda. Izdevumu kategoriju apakšlīguma rindas ļauj projekta vadītājam iegādāties pakalpojumu vai produktu kategorijas no pārdevējiem, par ko maksu var pieskaitīt projektam.

Lai programmā Project Operations izveidotu apakšlīguma izdevumu kategoriju rindu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī atlasiet **Apakšlīgumi** un atveriet apakšlīgumu, ar kuru vēlaties strādāt.
2. Lai izveidotu jaunu rindu, cilnē **Apakšlīguma rindas** atlasiet **Jauns**.
3. Lapas **Ātrā izveide** laukā **Transakciju klase** atlasiet **Izdevumi** un ievadiet vai atlasiet jebkādu citu nepieciešamo lauka informāciju.

Tālāk redzamajā tabulā ir sniegta informācija par laukiem detalizētās informācijas lapā **Apakšlīgumu rinda** un lapā **Ātrā izveide**.

| **Lauks** |  **Apraksts** |
| ----------| ---------------- |
| Nosaukums/vārds, uzvārds | Apakšlīguma rindas nosaukums. |
| Apraksts | Apakšlīguma rindā iegādāto pakalpojumu vai produktu kategoriju īss apraksts. |
| Rindas tips | Šim laukam ir noklusējuma vērtība **Uz daudzumu balstīts**.  |
| Rēķinu izrakstīšanas metode | Apakšlīguma rindas norēķinu metode. Pamatojoties uz rindas norēķinu metodi, norēķinu metodei ar fiksēto cenu ir pieejams uz atskaites punktu balstīts rēķinu grafiks.  |
| Transakcijas klase | Šim laukam ir noklusējuma vērtība **Laiks**. Lai izveidotu apakšlīguma rindas produktu iegādei, iestatiet lauku **Transakcijas klase** kā **Izdevumi**. Šī lauka vērtība norāda, ka apakšlīguma rinda tiek izmantota, lai ierakstītu projektos izmantojamu produktu vai pakalpojumu kategorijas iegādi. |
| Darbības kategorija | Atlasiet transakcijas kategoriju. |
| Pieprasītais sākuma datums | Datums, kurā pirkumu kategorijām ir jābūt pieejamām no pārdevēja. Pieprasīto sākuma datumu izmanto arī, lai izvēlētos projekta cenrādi no apakšlīgumam pievienotajiem projekta cenrāžiem. Apakšlīguma rindas kategorijas izmaksas pēc noklusējuma tiek izgūtas no cenrāža. |
| Pieprasītais beigu datums | Datums, kad vairs nav nepieciešamas pirkumu kategorijas. Šis datums ierosina brīdinājumu, kad projekta vadītājs šo apakšlīguma rindu saista ar noteiktiem izdevumu aprēķiniem projektos, kuru iestatītais datums ir pēc šī datuma. |
| Pasūtītais daudzums | No pārdevēja iegādātās kategorijas daudzums. Kad projekta vadītājs pārsniedz iegādāto daudzumu, tiek parādīts brīdinājums.  |
| Vienību grupa | Šī lauka vērtība tiek iestatīta pēc noklusējuma, balstoties uz atlasītajai kategorijai iestatīto noklusējuma vienību grupu. |
| Vienība | Šī lauka vērtība tiek iestatīta pēc noklusējuma, balstoties uz atlasītajai kategorijai iestatīto noklusējuma vienību. Kategorijas un vienības kombinācija tiek izmantota, lai iestatītu pēc noklusējuma vienības cenu apakšlīguma rindā. |
| Vienības cena | Vienības cenas lauka vērtība tiek izgūta pēc noklusējuma no kategorijas un vienības kombinācijas no kategorijas cenām, kas saistītas ar pieprasītajam apakšlīguma rindas sākuma datumam piemērojamo projekta cenrādi.  |
| Starpsumma | Šis tikai lasāmais lauks tiek automātiski aprēķināts kā daudzuma vienības cena, ja ir ievadītas gan daudzuma, gan vienības cenas vērtības. Ja viens vai abi lauki ir tukši, šajā laukā vērtību var ievadīt manuāli.  |
| PVN | Ievadiet pārdošanas nodokļa summu.  |
| Kopsumma | Apakšlīguma rindu kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts kā starpsumma + pārdošanas nodoklis.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
