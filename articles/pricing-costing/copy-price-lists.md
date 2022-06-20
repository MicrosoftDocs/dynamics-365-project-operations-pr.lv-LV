---
title: Cenrāžu kopēšana
description: Šajā rakstā ir sniegta informācija par cenrāžu kopēšanu projekta operācijās.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fce3a362fe6326e362c3f77054c10281a9c146c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921173"
---
# <a name="copy-price-lists"></a>Cenrāžu kopēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Programmā Dynamics 365 Project Operations var izveidot cenrāža kopijas. Piemēram, varat izveidot cenrāžus nākamajam gadam, izmantojot pašreizējā gada cenrādi.  Vai arī jūs varat kopēt cenrādi norēķinu likmēm un pārdošanas cenām no izmaksu cenrāžiem. 

Lai kopētu cenrādi, veiciet tālāk norādītās darbības.

1. Atveriet cenrādi, kuru vēlaties nokopēt, un atlasiet **Kopēt**.
2. Ievadiet visu nepieciešamo informāciju, lai kopētu cenrādi. Tālāk sniegtajā tabulā ir norādīti apsvērumi, kas jāņem vērā, ievadot informāciju.

| Lauks | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- |
| Nosaukums/vārds, uzvārds | Avota cenrāža nosaukums ar pievienotu **-copy**. | Cenrādis ietver ar šo vērtību visās saraksta lapās un nolaižamajās opcijās. |
| Konteksts | Ievadiet vēlamo mērķa cenrāža kontekstu. | Cenrādis, kura konteksts ir iestatīts uz **Izmaksas**, tiek izmantots, lai uzmeklētu izmaksu aprēķinu un izmaksu reālo cenu. Cenrādis, kura konteksts ir iestatīts uz **Pārdošana**, tiek izmantots, lai uzmeklētu pārdošanas aprēķinu un pārdošanas reālo cenu. Projekta cenrāžiem klientam, piedāvājumam vai līgumam var pievienot tikai tos cenrāžus, kuru konteksts ir iestatīts uz **Pārdošana**. |
| Sākuma datums | Tā perioda sākuma datums, kurā ir spēkā cenrādis. | Kopā ar lauku **Beigu datums** tiek izmantots, lai noteiktu, kurš cenrādis ir piemērojams noteiktai aplēsei vai faktiskajai rindai. |
| Beigu datums | Tā perioda beigu datums, kurā ir spēkā cenrādis. | Kopā ar lauku **Sākuma datums** tiek izmantots, lai noteiktu, kurš cenrādis ir piemērojams noteiktai aplēsei vai faktiskajai rindai. |
| Valūta | Avota cenrāža valūta. To var mainīt. | Ja tā tiek mainīta, visas iegūtās darba, izmaksu un preču kataloga cenu rindas kopēšanas laikā tiek pārvērstas mērķa cenrāža valūtā. |
| Laika vienība | Avota cenrāža valūta. To var mainīt. | Ja tā tiek mainīta, visas iegūtās darba, vienumu cenu rindas kopēšanas laikā tiek pārvērstas mērķa cenrāža vienībā. Tiek izmantota avota cenrāža un mērķa cenrāža laika elementa konvertēšana no elementa iestatījumiem. |
| Apraksts | Avota cenrāža apraksts ar pievienotu **-copy**. Šis ir teksta lauks, kas ļauj nodrošināt cenrādi ar vairākrindu aprakstu. | Šis lauks tiek parādīts cenrāža skatos **Saistīts** dažādās entītijās, kurām ir saistīti cenrāži. |

3. Saglabājiet cenrādi. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Cenrāža atjaunināšana, piemērojot uzcenojumu visām cenām

1. Cenrāža cilnēs **Loma**, **Kategorija** un **Cenrāža elements** var atlasīt vienumu **Atjaunināt cenas**, lai lietotu uzcenojumu visām cenām apakšrežģī. 
2. Atvērtajā dialoga lapā ievadiet uzcenojumu. Var ievadīt arī negatīvu uzcenojuma procentuālo vērtību, lai samazinātu cenas par noteiktu procentuālo vērtību. 
3. Dialoga lapā atlasiet **Labi** un pēc tam pārbaudiet, vai cenas apakšrežģī atspoguļo jūsu veiktās izmaiņas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]