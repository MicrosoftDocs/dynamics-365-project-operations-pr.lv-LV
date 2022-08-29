---
title: Apakšlīguma rindas izdevumu kategorijām
description: Šajā rakstā ir paskaidrots, kā ierakstīt apakšuzņēmuma līgumu rindas par izdevumiem un izmantot laukus, lai reģistrētu laika iegādi no kreditoriem.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7166642abc2187a53f7019639df6f0d7124f4765
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261850"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Apakšlīguma rindas izdevumu kategorijām

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Apakšlīgumam programmā Dynamics 365 Project Operations var būt izdevumu kategoriju rinda. Izdevumu kategoriju apakšlīguma rindas ļauj projekta vadītājam iegādāties pakalpojumu vai produktu kategorijas no pārdevējiem, par ko maksu var pieskaitīt projektam.

Lai programmā Project Operations izveidotu apakšlīguma izdevumu kategoriju rindu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī atlasiet **Apakšlīgumi** un atveriet apakšlīgumu, ar kuru vēlaties strādāt.
2. Lai izveidotu jaunu rindu, cilnē **Apakšlīguma rindas** atlasiet **Jauns**.
3. Lapas **Ātrā izveide** laukā **Transakciju klase** atlasiet **Izdevumi** un ievadiet vai atlasiet jebkādu citu nepieciešamo lauka informāciju.

Tālāk redzamajā tabulā ir sniegta informācija par laukiem detalizētās informācijas lapā **Apakšlīgumu rinda** un lapā **Ātrā izveide**.

| **Lauks** | **Apraksts** | **Funkcionālā ietekme** |
| --- | --- | --- |
| Nosaukums/vārds, uzvārds | Apakšuzņēmēja līguma rindas nosaukums palīdzēs veikt identificēšanu. | Tas tiks parādīts, kā pirmā kolonna visos uzmeklēšanas rezultātos, pamatojoties apakšuzņēmēja līguma rindām. |
| Apraksts | Īss izmaksu kategoriju apraksts, kas tiek iegādāts saskaņā ar apakšuzņēmēja līguma rindu. | Nevienu |
|Rindas tips | Šim laukam ir noklusējuma vērtība **Uz daudzumu balstīts**. |Nevienu |
| Rēķinu izrakstīšanas metode | Šī ir opciju kopa, kas ir divi galvenie Project Operations atbalstītie līgumu slēgšanas modeļi: **Fiksēta cena** un **Laiks un materiāli**. | Uz atskaites punktu balstīts rēķinu grafiks ir padarīts pieejams apakšuzņēmēja līguma rindām, ja ir atlasīta fiksētas cenas norēķinu metode. |
| Transakcijas klase | Šim laukam ir noklusējuma vērtība **Laiks**. Lai izveidotu apakšuzņēmēja līguma rindas produktu iegādei, iestatiet lauku **Transakcijas klase** kā **Izdevumi**.  | Tas norāda, ka apakšuzņēmēja līguma rinda tiek izmantota, lai reģistrētu projektos izmantojamu izdevumu kategoriju iegādi. |
| Darbības kategorija | Parāda sistēmā aktīvo transakciju kategoriju sarakstu. |Nevienu |
| Pieprasītais sākuma datums | Ievadiet datumu, kad pārdošanas kategorijām ir jābūt pieejamām no pārdevēja. | Pieprasītais sākums tiek izmantots projekta cenrāža izvēlei no projekta cenrāžiem, kas ir pievienoti apakšuzņēmēja līgumam. Apakšuzņēmēja līgumu rindas kategorijas izmaksas tiek ņemtas no šī cenrāža. |
| Pieprasītais beigu datums | Ievadiet datumu, no kura vairs nebūs nepieciešamas pirkumu kategorijas. | Šis tiks izmantots, lai parādītu brīdinājumus, kad projekta vadītājs saista šo apakšuzņēmēja līguma rindu ar noteiktiem projekta izmaksu aprēķiniem, kas nepieciešami pēc šī datuma. |
| Pasūtītais daudzums | No pārdevēja iepērkamās kategorijas daudzums. | Šis tiks izmantots, lai parādītu brīdinājumus, kad projekta vadītājs izmanto pārāk daudz šī daudzuma.|
| Vienību grupa | Noklusējuma vērtība tiek pamatota uz noklusējuma vienību grupu, kas ir iestatīta atlasītajai kategorijai. |Nevienu |
| Vienība | Noklusējuma vērtība tiek pamatota uz noklusējuma vienību grupu atlasītajai kategorijai.  | **Produkta** un **Vienības** kombinācija tiks izmantota, kā noklusējuma vērtība vai tiks aprēķināta apakšuzņēmēja līguma rindas vienības cena.  |
| Vienības cena | Noklusējuma vērtība izmanto kategoriju un vienību kombināciju no **Kategorijas** un **Vienības** cenām, kas ir saistītas ar projekta cenrādi un kas ir piemērojama pieprasītajam apakšuzņēmēja līguma rindas sākumam. |Nevienu |
| Starpsumma | Šis ir tikai lasāms lauks, kas tiek aprēķināts kā daudzums X vienības cena, ja ir ievadītas gan daudzuma, gan vienības cenas vērtības. Ja viens vai abi lauki ir tukši, tad tajos var ievadīt vērtību. |Nevienu |
| PVN | Ievadiet pārdošanas nodokļa summu. |Nevienu |
| Kopsumma | Apakšlīguma rindu kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts, kā starpsumma + pārdošanas nodoklis. |Nevienu |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
