---
title: Cenrāžu iestatīšana
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt izmaksu un pārdošanas cenrāžus.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 227e9a6f0ce6fd3fa1c2b0bd9afa014a3ec4f9758ead0dfb408156535692575c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009495"
---
# <a name="set-up-price-lists"></a>Cenrāžu iestatīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Cenrāži Dynamics 365 Project Operations preču katalogā ir iekļauti. Likmes attēlo izmaksu, pārdošanas un rēķina likmes. Atkarībā no tā, vai cenrādis attēlo izmaksu likmes vai pārdošanas un rēķina likmes, cenrāža konteksts ir **Pārdošana** vai **Izmaksas**.

Tālāk norādītie paplašinājumi ir specifiski Project Operations un tiek lietoti cenrāžiem no Dynamics 365 Sales.

- **Konteksts**: šajā laukā ir atbalstītas vērtības **Izmaksas** un **Pārdošana**. Vērtība **Pirkšana** netiek atbalstīta. Iestatiet kontekstu **Izmaksas**, lai izveidotu izmaksu cenrādi, vai iestatiet kontekstu **Pārdošana** pārdošanas cenrādim. Izmaksu cenrāži nosaka izmaksu tipa cenu budžeta un faktisko datu ierakstos. Pārdošanas cenrāži nosaka cenu novērtētajiem un faktiskajiem ierakstiem, kas attiecas uz pārdošanas veidiem bez rēķina un ar rēķinu.
- **Laika vienība**: šī ir noklusējuma laika vienība, kurai šī cenrāža tabulā ir iestatīta attiecīgā **Lomas cena**.
- **Cenrāža entītija**: šis slēptais lauks ir saskaņā ar Project Operations, lai atšķirtu cenrāžus, kas atbilst piedāvājumam vai līgumam, no tiem, kas ir standarta un globāli piemērojami.

## <a name="price-list-header"></a>Cenrāža galvene

Tālāk sniegtajā tabulā ir iekļauti lauki cenrāža cilnē **Vispārīgi**, kas ir unikāla risinājumā Project Operations, vai ir būtiskas izmaiņas cenrāžu uzvedībā, kas iekļauti pārdošanas darījumos.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| Nosaukums/vārds, uzvārds | Cilne **Vispārīgi** un veidnes **Ātrā izveide** | Cenrāža identifikators. | Cenrādis tiek parādīts ar šo vērtību visās saraksta lapās un nolaižamajās opcijās.|
| Konteksts | Cilne **Vispārīgi** un veidnes **Ātrā izveide** | Šo lauku var iestatīt uz **Izmaksas** vai **Pārdošana**. | Cenrādis, kas iestatīts uz **Izmaksas**, tiek izmantots, lai uzmeklētu izmaksu aprēķinu un izmaksu reālo cenu. Cenrādis, kas iestatīts uz **Pārdošana**, tiek izmantots, lai uzmeklētu pārdošanas aprēķinu un pārdošanas reālo cenu. Projekta cenrāžiem klientiem, projektu piedāvājumiem un projektu līgumiem var pievienot tikai tos cenrāžus, kuru konteksts ir iestatīts uz **Pārdošana**. |
| Sākuma datums | Cilne **Vispārīgi** un veidnes **Ātrā izveide** | Tā perioda sākuma datums, kurā ir spēkā cenrādis. | Lauks **Beigu datums** tiek izmantots, lai noteiktu, kurš cenrādis ir piemērojams noteiktai aplēsei vai faktiskajai rindai. |
| Beigu datums | Cilne **Vispārīgi** un veidnes **Ātrā izveide** | Tā perioda beigu datums, kurā ir spēkā cenrādis. | Lauks **Sākuma datums** tiek izmantots, lai noteiktu, kurš cenrādis ir piemērojams noteiktai aplēsei vai faktiskajai rindai. |
| Valūta | Cilne **Vispārīgi** un veidnes **Ātrā izveide** | Šis lauks tiek izmantots, lai noklusētu valūtu katrai lomai, kategorijai vai cenrāža krājumu rindai, kas saistīta ar šo cenrādi. | **Pārdošana** cenrāži, lomu, kategoriju vai cenrāža elementu rindas nevar izveidot nevienā valūtā, kas nav šī valūta. **Izmaksas** cenrāžos var izveidot lomu cenas rindu jebkurā valūtā. Šeit definētā valūta tiek izmantota kā noklusējuma vērtība. Lietotāja iestatījumi, kas ir saistītās lomu cenas, var ignorēt šo vērtību, lai iespējotu darba izmaksu likmes iestatījumus jebkurā valūtā. Kategoriju izmaksu likmes un cenrāža elementu izmaksas var iestatīt tikai šeit definētajā valūtā. |
| Laika vienība | Cilne **Vispārīgi** un veidnes **Ātrā izveide** | Šis lauks tiek izmantots, lai noklusētu laika vienību katrā ar šo cenrādi saistītā lomas rindā. | Šī lauka vērtība tiek izmantota tikai saistītās lomas cenas iestatījumā. Cenrāžos **Izmaksas** un **Pārdošana** lomas cenas rindu var izveidot jebkurā laika vienībā. Šeit definētā laika vienība tiek izmantota kā noklusējuma vērtība. Ar lietotāja iestatīšanu saistītās lomu cenas var ignorēt šo vērtību, lai iespējotu darba izmaksu un rēķina likmes iestatījumus jebkurā laika vienībā. |
| Apraksts | Cilne **Vispārīgi** un veidnes **Ātrā izveide** | Šis teksta lauks ļauj nodrošināt cenrādi ar vairākrindu aprakstu. | Šis lauks tiek parādīts cenrāža skatos **Saistīts** dažādās entītijās, kurām ir saistīti cenrāži. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]