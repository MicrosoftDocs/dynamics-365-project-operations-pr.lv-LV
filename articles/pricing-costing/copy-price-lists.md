---
title: Cenrāžu kopēšana
description: Šajā tēmā ir sniegta informācija par cenrāžu kopēšanu risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080483"
---
# <a name="copy-price-lists"></a>Cenrāžu kopēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Varat izveidot cenrāžu kopijas risinājumā Dynamics 365 Project Operations. Piemēram, varat izveidot cenrāžus nākamajam gadam, izmantojot pašreizējā gada cenrādi.  Vai arī jūs varat kopēt cenrādi norēķinu likmēm un pārdošanas cenām no izmaksu cenrāžiem. 

Lai kopētu cenrādi, veiciet tālāk norādītās darbības.

1. Atveriet cenrādi, kuru vēlaties nokopēt, un atlasiet **Kopēt**.
2. Ievadiet visu nepieciešamo informāciju, lai kopētu cenrādi. Tālāk sniegtajā tabulā ir norādīti apsvērumi, kas jāņem vērā, ievadot informāciju.

| Lauks | Atbilstība, mērķis un norādes | Lejupstraumes ietekme |
| --- | --- | --- |
| Nosaukums/vārds, uzvārds | Avota cenrāža nosaukums ar pievienotu **-copy**. | Cenrādis ietver ar šo vērtību visās saraksta lapās un nolaižamajās opcijās. |
| Konteksts | Ievadiet vēlamo mērķa cenrāža kontekstu. | Cenrādis, kura konteksts ir iestatīts uz **Izmaksas** , tiek izmantots, lai uzmeklētu izmaksu aprēķinu un izmaksu reālo cenu. Cenrādis, kura konteksts ir iestatīts uz **Pārdošana** , tiek izmantots, lai uzmeklētu pārdošanas aprēķinu un pārdošanas reālo cenu. Projekta cenrāžiem klientam, piedāvājumam vai līgumam var pievienot tikai tos cenrāžus, kuru konteksts ir iestatīts uz **Pārdošana**. |
| Sākuma datums | Tā perioda sākuma datums, kurā ir spēkā cenrādis. | Kopā ar lauku **Beigu datums** tiek izmantots, lai noteiktu, kurš cenrādis ir piemērojams noteiktai aplēsei vai faktiskajai rindai. |
| Beigu datums | Tā perioda beigu datums, kurā ir spēkā cenrādis. | Kopā ar lauku **Sākuma datums** tiek izmantots, lai noteiktu, kurš cenrādis ir piemērojams noteiktai aplēsei vai faktiskajai rindai. |
| Valūta | Avota cenrāža valūta. To var mainīt. | Ja tā tiek mainīta, visas iegūtās darba, izmaksu un preču kataloga cenu rindas kopēšanas laikā tiek pārvērstas mērķa cenrāža valūtā. |
| Laika vienība | Avota cenrāža valūta. To var mainīt. | Ja tā tiek mainīta, visas iegūtās darba, vienumu cenu rindas kopēšanas laikā tiek pārvērstas mērķa cenrāža vienībā. Tiek izmantota avota cenrāža un mērķa cenrāža laika elementa konvertēšana no elementa iestatījumiem. |
| Apraksts | Avota cenrāža apraksts ar pievienotu **-copy**. Šis ir teksta lauks, kas ļauj nodrošināt cenrādi ar vairākrindu aprakstu. | Šis lauks tiek parādīts cenrāža skatos **Saistīts** dažādās entītijās, kurām ir saistīti cenrāži. |

3. Saglabājiet cenrādi. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Cenrāža atjaunināšana, piemērojot uzcenojumu visām cenām

1. Cenrāža cilnēs **Loma** , **Kategorija** un **Cenrāža elements** var atlasīt **Atjaunināt cenas** , lai visām apakšrežģa cenām lietotu uzcenojumu. 
2. Atvērtajā dialoga lapā ievadiet uzcenojumu. Var ievadīt arī negatīvu uzcenojuma procentuālo vērtību, lai samazinātu cenas par noteiktu procentuālo vērtību. 
3. Dialoga lapā atlasiet **Labi** un pēc tam pārbaudiet, vai apakšrežģa cenās ir redzamas jūsu veiktās izmaiņas.
