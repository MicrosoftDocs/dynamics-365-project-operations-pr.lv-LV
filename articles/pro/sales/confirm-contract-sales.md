---
title: Projekta līguma apstiprināšana
description: Šajā tēmā ir sniegta informācija par līguma apstiprināšanu risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d807d3631f40a93ec7dbd918b64c287fd4875c79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273837"
---
# <a name="confirm-a-project-contract"></a>Projekta līguma apstiprināšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta līgums Dynamics 365 Project Operations var būt aktīvs ar iemeslu **Apstiprināts** vai slēgts ar iemeslu **Zaudēts**. Kad apstiprināsit projekta līgumu, statuss tiks atjaunināts no **Melnraksts** uz **Aktīvs** un statusa iemesls tiks iestatīts kā **Apstiprināts**. Aktīvu vai slēgtu līgumu nevar rediģēt vai atkārtoti atvērt. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Projekta līguma apstiprināšanas finansiālā ietekme

Kad projekta līgums būs apstiprināts, lietojumprogramma atkārtoti aprēķinās izmaksas, atsaucot vecās faktiskās izmaksas un izveidojot jaunas faktiskās izmaksas. Jaunās faktiskās izmaksas tiek apstrādātas, pamatojoties uz saistītās projekta līguma rindas norēķinu metodi. Ja faktisko izmaksu atsauce ir atsauce līguma rinda Laiks un Materiāli, lietojumprogramma automātiski no jauna izveido atbilstošos rēķinā neiekļautās pārdošanas faktiskos datus. Ja faktisko izmaksu atsauce ir fiksētas cenas līguma rinda, lietojumprogramma pārtrauc faktisko izmaksu pārstrādi.

Tiek izvērtēta faktisko rādītāju nepārsniegšanas ierobežojumi, apmaksājamības iestatījumi, kā arī cenas un izmaksas, bet pēc tam tie tiek atjaunināti apstiprināšanas procesa ietvaros.

## <a name="close-a-project-contract-as-lost"></a>Līguma kā zaudēta līguma slēgšana

Slēdzot projekta līgumu kā zaudētu, līguma statuss tiek atjaunināts uz **Slēgts** un statusa iemesls tiek norādīts kā **Zaudēts**. Projekta līgums kļūst tikai lasāms. Pirms izmaiņas ir pabeigtas tiek parādīts apstiprinājuma dialogs, jo nevar atkārtoti atvērt slēgtu projekta līgumu.

Ja projekta līgumā, kas ir slēgts kā zaudēts, ir atsauce uz projektu savās rindās, šis projekts arī tiek atzīmēts kā slēgts. Visas resursu rezervācijas no šīs dienas uz priekšu tiek atceltas. Visi rēķinā neiekļautās pārdošanas faktiskie dati projekta līgumā, kas nav iekļauti rēķinā, tiks atcelti.

> [!NOTE]
> Programmā Dynamics 365 Project Operations, slēdzot projekta līgumu kā zaudētu, netiek ietekmēts šīs saistītās iespējas statuss. Iespēja paliks atvērta, un tā būs jāaizver manuāli.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]