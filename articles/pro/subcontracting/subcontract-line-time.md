---
title: Apakšlīguma laika rindas
description: Šajā tēmā ir paskaidrots, kā reģistrēt apakšlīguma laika rindas un reģistrēt laika iegādi no pārdevējiem.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323875"
---
# <a name="subcontract-lines-for-time"></a>Apakšlīguma laika rindas

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Apakšlīgumam programmā Dynamics 365 Project Operations var būt apakšlīguma laika rinda. Apakšlīguma laika rindas ļauj projekta vadītājam iegādāties pārdevēja resursu laiku, lai nodrošinātu darbiniekus projekta uzdevumiem un resursu prasībām.

Lai programmā Project Operations izveidotu apakšlīguma laika rindu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī atlasiet **Apakšlīgumi** un atveriet apakšlīgumu.
2. Lai izveidotu jaunu apakšlīguma rindu, cilnē **Apakšlīguma rindas** atlasiet **Jauns**.
3. Lapas **Ātrā izveide** laukā **Transakciju klase** atlasiet **Laiks**.
4. Ievadiet pārējo lauka informāciju un pēc tam atlasiet **Saglabāt**.

  Tālāk redzamajā tabulā ir sniegta informācija par laukiem lapā **Apakšlīgumu rinda** un lapā **Ātrā izveide**.

| **Lauks** | **Apraksts** |
| --- | --- |
| Nosaukums/vārds, uzvārds | Apakšlīguma rindas nosaukums. |
| Apraksts | Apakšlīguma rindā iegādāto pakalpojumu īss apraksts. | 
| Rindas tips | Šis lauks noklusējuma vērtība.  |
| Rēķinu izrakstīšanas metode | Atlasiet norēķinu metodi. Pamatojoties uz atsauces apakšlīguma rindas norēķinu metodi, norēķinu metodei ar fiksēto cenu ir pieejams uz atskaites punktu balstīts rēķinu grafiks. |
| Transakcijas klase | Šis lauks ir noklusējuma vērtība, kas norāda, vai apakšlīguma rinda tiek izmantota, lai reģistrētu apakšuzņēmēja laika pirkumu. |
| Loma | To apakšuzņēmēju resursu loma, kuru laiks tiek iegādāts. Apakšuzņēmēja resursiem piešķirtā loma nosaka iegādes izmaksas. |
| Pieprasītais sākuma datums | Datums, kad apakšuzņēmēja resursiem ir jāsāk darbs. Pieprasīto sākuma datumu izmanto arī, lai izvēlētos projekta cenrādi no apakšlīgumam pievienotajiem projekta cenrāžiem. Lomas izmaksas apakšlīguma rindā pēc tam pēc noklusējuma tiek izgūtas no cenrāža. |
| Pieprasītais beigu datums | Datums, kad apakšuzņēmēja resursu piešķire beidzas. Šis datums tiek lietots, lai rādītu brīdinājumus, kad projekta vadītājs izmanto šo noslodzi resursu prasībām, kas ir pēc šī datuma. |
| Pasūtītais daudzums | No piegādātāja iegādāto lomu stundu skaits. Šī vērtība tiek lietota, lai parādītu brīdinājumus, kad projekta vadītājs pārāk daudz izmanto šo noslodzi resursu prasībām. |
| Vienību grupa | Šī lauka noklusējuma vērtība ir laika vienību grupa, un to nevar mainīt.  |
| Vienība | Šī lauka noklusējuma vērtība ir stundu pamatvienība no laika vienību grupas. Šo vērtību var mainīt, lai iegādātos jebkuru laika vienību grupas vienību, piemēram, dienu vai nedēļu. Lomas un vienības kombinācija tiek izmantota, lai aprēķinātu apakšlīguma rindas vienības cenu. |
| Vienības cena | Vienības cenas noklusējuma vērtība ir lomas un vienības kombinācija no projekta cenrāža, kas ir piemērojams pieprasītajam apakšlīguma rindas sākuma datumam. Ja piemērojamā projekta cenrāža cena ir iestatīta citā vienībā, nevis apakšlīguma rindas vienībā, sistēma izmanto vienības konversiju, lai aprēķinātu vienas vienības cenu. |
| Starpsumma | Šis ir tikai lasāmais lauks, kas tiek automātiski aprēķināts kā **Daudzums x vienības cena**, ja ir ievadītas gan daudzuma, gan vienības cenas vērtības. Ja daudzuma, vienības cenas vai abi lauki ir tukši, laukā var ievadīt vērtību. |
| PVN |  Ievadiet pārdošanas nodokļa summu. |
| Kopsumma | Apakšlīguma rindu kopsumma pēc nodokļu iekļaušanas. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
