---
title: Projekta līguma apstiprināšana
description: Šajā rakstā ir sniegta informācija par līguma apstiprināšanu risinājumā Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930005"
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