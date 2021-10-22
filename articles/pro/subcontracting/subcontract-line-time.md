---
title: Apakšlīguma laika rindas
description: Šajā tēmā ir paskaidrots, kā reģistrēt apakšlīguma laika rindas un reģistrēt laika iegādi no pārdevējiem.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547253"
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

| **Lauks** | **Apraksts** | **Funkcionālā ietekme** |
| --- | --- | --- |
| Nosaukums/vārds, uzvārds | Apakšuzņēmēja līguma rindas nosaukums palīdzēs veikt identificēšanu. | Tas tiks parādīts, kā pirmā kolonna visos uzmeklēšanas rezultātos, pamatojoties apakšuzņēmēja līguma rindām. |
| Apraksts | Apakšlīguma rindā iegādāto pakalpojumu īss apraksts. |Nevienu |
| Rindas tips |   Šim laukam ir noklusējuma vērtība **Uz daudzumu balstīts**.| Nevienu |
| Rēķinu izrakstīšanas metode | Šī ir opciju kopa, kas ir divi galvenie Project Operations atbalstītie līgumu slēgšanas modeļi: **Fiksēta cena** un **Laiks un materiāli**. | Uz rēķinu izrakstīšanas metodi balstīts uz atskaites punktu balstīts rēķinu grafiks ir pieejams apakšuzņēmēja līguma rindām, ja ir atlasīta fiksētas cenas norēķinu metode. |
| Transakcijas klase | Noklusējuma vērtība ir **"Laiks"**. | Tas norāda, ka apakšuzņēmēja līguma rinda tiek izmantota, lai ierakstītu apakšuzņēmēja līguma laika iegādi. |
| Loma | Atlasiet to apakšuzņēmēja līguma resursu lomu, kuru laiks tiks iegādāts. | Loma, ko veic apakšuzņēmēja līguma resursi, nosaka iegādes izmaksas. |
| Pieprasītais sākuma datums | Ievadiet datumu, kad darba uzsākšanai ir nepieciešami apakšuzņēmēja līguma resursi. | Šis tiek izmantots projekta cenrāža izvēlei no projekta cenrāžiem, kas ir pievienoti apakšuzņēmēja līgumam. Apakšuzņēmēja līgumu rindas lomu kategoriju izmaksas tiek ņemtas no šī cenrāža. |
| Pieprasītais beigu datums | Ievadiet datumu, kad beidzas apakšuzņēmēja resursu piešķiršana. | Tas tiks izmantots, lai parādītu brīdinājumus, kad projekta vadītājs izmanto noslodzi resursu prasībām, kas rodas pēc šī datuma. |
| Pasūtītais daudzums | Ievadiet no pārdevēja iegādāto lomu stundu skaitu. | Tas tiks izmantots, lai parādītu brīdinājumus, kad projekta vadītājs pārāk daudz izmanto noslodzi resursu prasībām. |
| Vienību grupa | Noklusējuma vērtība ir **Laika vienību grupa**, ko nevar mainīt. | Nevienu|
| Vienība | Šī lauka noklusējuma vērtība ir **Laika vienību grupas** stundu pamatvienība. Šo vērtību var mainīt, lai iegādātos jebkuru **Laika vienību grupas** vienību, piemēram, dienu vai nedēļu. | **Lomas** un **Vienības** kombinācija tiks izmantota, kā noklusējuma vērtība vai tiks aprēķināta apakšuzņēmēja līguma rindas vienības cena. |
| Vienības cena | Noklusējuma vienības cena izmanto kombināciju no **Lomas** un **Vienības**, kas ir saistītas ar projekta cenrādi un kas ir piemērojamas **Pieprasītajam sākuma** datumam apakšuzņēmēja līguma rindā. | Ja piemērojamā projekta cenrāža cena ir iestatīta citā vienībā, nevis apakšlīguma rindas vienībā, sistēma izmanto vienības konversiju, lai aprēķinātu vienas vienības cenu. |
| Starpsumma |    Šis ir tikai lasāms lauks, kas tiek aprēķināts kā daudzums x vienības cena, ja ir ievadītas gan daudzuma, gan vienības cenas vērtības. Ja daudzuma, vienības cenas vai abi lauki ir tukši, laukā var ievadīt vērtību. | Nevienu|
| PVN |   Ievadiet pārdošanas nodokļa summu. |Nevienu |
| Kopsumma | Apakšlīguma rindu kopsumma, ieskaitot nodokļus. Šis lauks tiek aprēķināts, kā starpsumma + pārdošanas nodoklis.|Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
