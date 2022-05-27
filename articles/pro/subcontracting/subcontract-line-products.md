---
title: Apakšlīguma produktu rindas
description: Šajā tēmā paskaidrots, kā reģistrēt apakšlīguma produktu rindas un izmantot dažādos laukus, lai reģistrētu produktu pirkumus no piegādātājiem.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71e4a48c3d29d7ea5b015f6c6797da60001fccff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579082"
---
# <a name="subcontract-lines-for-products"></a>Apakšlīguma produktu rindas

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Apakšuzņēmējam programmā Dynamics 365 Project Operations var būt apakšlīguma produktu rinda. Šīs rindas projekta vadītājam ļauj iegādāties produktus no piegādātājiem, ko pēc tam var izmantot projekta uzdevumiem.

Izpildiet tālāk norādītās darbības, lai programmā Project Operations izveidotu apakšlīguma produktu rindu.

1. Navigācijas lapā atlasiet **Apakšlīgumi** un pēc tam atveriet apakšlīgumu, ar kuru vēlaties strādāt. 
2. Cilnē **Apakšlīguma rindas** atlasiet **+ Jauns**, lai izveidotu jaunu apakšlīguma rindu.
3. Lapas **Ātrā izveide** laukā **Transakciju klase** atlasiet **Materiāli** un ievadiet vai atlasiet nepieciešamo lauka informāciju. 
4. Atlasiet vienumu **Saglabāt**.

Tālāk redzamajā tabulā ir sniegta informācija par lapas **Apakšlīguma rindas informācija** laukiem un lapu **Ātrā izveide**, jo tie ir saistīti ar produktu iegādi.

| Lauks | Apraksts | Funkcionālā ietekme|
| ----- | ----------- | ----------- |
| Nosaukums/vārds, uzvārds | Apakšuzņēmēja līguma rindas nosaukums palīdzēs veikt identificēšanu. |Tas tiks parādīts, kā pirmā kolonna visos uzmeklēšanas rezultātos, pamatojoties apakšuzņēmēja līguma rindām.
| Apraksts | Apakšlīguma rindā pasūtīto produktu īss apraksts. | Nevienu |
| Rindas tips | Šim laukam ir noklusējuma vērtība **Uz daudzumu balstīts**. |Nevienu |
| Rēķinu izrakstīšanas metode | Šī ir opciju kopa, kas ir divi galvenie Project Operations atbalstītie līgumu slēgšanas modeļi: **Fiksēta cena** un **Laiks un materiāli**. | Uz rēķinu izrakstīšanas metodi balstīts uz atskaites punktu balstīts rēķinu grafiks ir pieejams apakšuzņēmēja līguma rindām, ja ir atlasīta fiksētas cenas norēķinu metode. |
| Transakcijas klase |Šim laukam ir noklusējuma vērtība **Laiks**. Lai izveidotu apakšuzņēmēja līguma rindas produktu iegādē, nomainiet lauku **Transakcijas klase** uz **Materiālu**.  | Tas norāda, ka apakšuzņēmēja līguma rinda tiek izmantota, lai reģistrētu projektos izmantojamu produktu iegādi. |
| Atlasīt produktu | Atlasiet, vai iegādātais produkts tiek saglabāts preču katalogā vai ir ierakstāms produkts. |Nevienu |
| Produkts | Katalogā atlasiet aktīvu produktu. Šis lauks ir pieejams tikai tad, ja opcijas **Atlasīt produktu** iestatījums ir **Esošs**. |**Produkta** un **Vienības** kombinācija tiks izmantota kā noklusējuma vērtība vai tiks aprēķināta apakšuzņēmēja līguma rindas vienības cena.
| Ierakstāmais produkts | Ievadiet ierakstāmās preces nosaukumu. Šis lauks ir pieejams tikai tad, ja opcijas **Atlasīt produktu** iestatījums ir **Ierakstāms**.  |Iegādes cena netiek automātiski aizpildīta ierakstāmiem produktiem.|
| Pieprasītais piegādes datums | Ievadiet pieprasīto produktu piegādes datumu.| Šo datumu izmanto arī, lai izvēlētos projekta cenrādi no apakšlīgumam pievienotajiem projekta cenrāžiem. Produkta izmaksas apakšlīguma rindā pēc tam pēc noklusējuma tiek izgūtas no cenrāža. |
| Līgumā paredzētais piegādes datums | Ievadiet datumu, kad produkti saskaņā ar līgumu tiks piegādāti.  |Nevienu|
| Pasūtītais daudzums | Ievadiet no pārdevēja iegādātā produkta daudzumu.| Šis tiks izmantots, lai parādītu brīdinājumus, kad projekta vadītājs izmanto pārāk daudz šī daudzuma.|
| Vienību grupa | Šī vērtība pēc noklusējuma attiecas tikai uz kataloga produktiem. |Kad ir atlasīts gan **Produkts**, gan **Pieprasītais piegādes datums**, sistēma izvēlas piemērojamo cenrādi, pamatojoties uz piegādes datumu. Saistītajos cenrāža elementos tiek veikti atbilstošo produktu meklējumi. Vienību un vienību grupu vērtības pēc noklusējuma ir no cenrāža elementa ieraksta iestatījuma. |
| Vienība | Šī vērtība pēc noklusējuma ir vienība, kas ir iestatīta cenrāža elementa ierakstā. Ja nepieciešams, šo vienību var mainīt uz citu.| Produkta un vienības kombinācija tiek izmantota, lai pēc noklusējuma iestatītu vienības cenu apakšlīguma rindā esošajiem kataloga produktiem. |
| Vienības cena | Vienības cena pēc noklusējuma tiek iegūta, izmantojot produkta un vienības kombināciju no cenrāža elementiem, kas saistīti ar projekta cenrādi, kas ir piemērojams pieprasītajam apakšlīguma rindas piegādes datumam.  |Nevienu |
| Starpsumma | Šis tikai lasāmais lauks tiek aprēķināts kā daudzums x vienības cena, ja abos laukos ir ievadītas vērtības. Ja lauks **Daudzums** vai **Vienības cena**, vai abi lauki ir tukši, vērtību var ievadīt manuāli.  |Nevienu |
| PVN | Ievadiet pārdošanas nodokļa vērtību. |Nevienu |
| Kopsumma | Šajā aprēķinātajā laukā ir redzama apakšlīguma rindas kopsumma pēc nodokļu iekļaušanas. Šī lauka vērtība tiek aprēķināta, kā starpsumma + nodoklis. |Nevienu |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
