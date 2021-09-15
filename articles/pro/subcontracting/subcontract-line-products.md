---
title: Apakšlīguma produktu rindas
description: Šajā tēmā paskaidrots, kā reģistrēt apakšlīguma produktu rindas un izmantot dažādos laukus, lai reģistrētu produktu pirkumus no piegādātājiem.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323695"
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

| Lauks | Apraksts |
| ----- | ----------- |
| Nosaukums/vārds, uzvārds | Apakšlīguma rindas nosaukums. |
| Apraksts | Apakšlīguma rindā pasūtīto produktu īss apraksts. |
| Rindas tips | Šī lauka vērtība pēc noklusējuma ir **Uz daudzumu balstīts**. |
| Rēķinu izrakstīšanas metode |  Apakšlīguma rindas norēķinu metode. Fiksētas cenas norēķinu metodēm ir pieejams uz atskaites punktu balstīts rēķinu grafiks. |
| Transakcijas klase | Šī lauka vērtība pēc noklusējuma ir **Laiks**. Lai izveidotu apakšlīguma rindas produktu iegādei, laukā **Transakcijas klase** atlasiet **Materiāls**. Šī atlase norāda, ka apakšlīguma rinda tiek izmantota, lai reģistrētu projektos izmantojamu produktu iegādi. |
| Atlasīt produktu | Atlasiet, vai iegādātais produkts tiek saglabāts preču katalogā vai ir ierakstāms produkts. |
| Produkts | Katalogā atlasiet aktīvu produktu. Šis lauks ir pieejams tikai tad, ja opcijas **Atlasīt produktu** iestatījums ir **Esošs**. |
| Ierakstāmais produkts | Ievadiet ierakstāmās preces nosaukumu. Šis lauks ir pieejams tikai tad, ja opcijas **Atlasīt produktu** iestatījums ir **Ierakstāms**.  |
| Pieprasītais piegādes datums | Atlasiet produktiem nepieciešamo piegādes datumu. Šo datumu izmanto arī, lai izvēlētos projekta cenrādi no apakšlīgumam pievienotajiem projekta cenrāžiem. Produkta izmaksas apakšlīguma rindā pēc tam pēc noklusējuma tiek izgūtas no cenrāža. |
| Līgumā paredzētais piegādes datums | Atlasiet datumu, kad preces piegāde tiek apstiprināta ar līgumu.  |
| Pasūtītais daudzums | Ievadiet no pārdevēja iegādātā produkta daudzumu. Ja projekta vadītājs pārsniedz šo daudzumu, tiek parādīts brīdinājums. |
| Vienību grupa | Šī vērtība pēc noklusējuma attiecas tikai uz kataloga produktiem. Kad ir atlasīts gan **Produkts**, gan **Pieprasītais piegādes datums**, sistēma izvēlas piemērojamo cenrādi, pamatojoties uz piegādes datumu. Saistītajos cenrāža elementos tiek veikti atbilstošo produktu meklējumi. Vienību un vienību grupu vērtības pēc noklusējuma ir no cenrāža elementa ieraksta iestatījuma. |
| Vienība | Šī vērtība pēc noklusējuma tiek mainīta uz cenrāža elementa ieraksta vienības iestatījumu. Ja nepieciešams, šo vienību var mainīt uz citu. Produkta un vienības kombinācija tiek izmantota, lai pēc noklusējuma iestatītu vienības cenu apakšlīguma rindā esošajiem kataloga produktiem. |
| Vienības cena | Vienības cena pēc noklusējuma tiek iegūta, izmantojot produkta un vienības kombināciju no cenrāža elementiem, kas saistīti ar projekta cenrādi, kas ir piemērojams pieprasītajam apakšlīguma rindas piegādes datumam.  |
| Starpsumma | Šis tikai lasāmais lauks tiek aprēķināts kā daudzums x vienības cena, ja abos laukos ir ievadītas vērtības. Ja lauks **Daudzums** vai **Vienības cena**, vai abi lauki ir tukši, vērtību var ievadīt manuāli.  |
| PVN | Ievadiet pārdošanas nodokļa vērtību. |
| Kopsumma | Šajā aprēķinātajā laukā ir redzama apakšlīguma rindas kopsumma pēc nodokļu iekļaušanas. Šī lauka vērtība tiek aprēķināta kā starpsumma + nodoklis. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
