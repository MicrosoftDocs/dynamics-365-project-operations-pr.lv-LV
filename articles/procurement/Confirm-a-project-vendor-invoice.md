---
title: Apstipriniet projekta kreditoru rēķinus
description: Šajā rakstā ir paskaidrots, kā apstiprināt projekta kreditora rēķinu korporācijā Microsoft Dynamics 365 Project Operations, un aprakstīta projekta kreditora rēķina apstiprināšanas finansiālā ietekme.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475477"
---
# <a name="confirm-project-vendor-invoices"></a>Apstipriniet projekta kreditoru rēķinus

_ **Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem

Ja ir iespējots parametrs **Pm manuāla apstiprināšana, izmantojot obligāto** parametru, kreditoru rēķiniem, kas ir izveidoti, Microsoft Dataverse ir **melnraksta** statuss. Šādi izveidoti kreditoru rēķini ir jāpārskata un manuāli jāapstiprina. Ja parametrs **Pm manuālais apstiprinājums ir obligāts**, ir atspējots, kreditoru rēķini, kas tiek izveidoti Dataverse, tiek automātiski apstiprināti. Turpmāka rīcība nav nepieciešama. 

Kad esat verificējis visas rindas kreditora rēķinā, Dynamics 365 Project Operations atlasiet **Apstiprināt**, lai apstiprinātu kreditora rēķinu.

Kreditora rēķinā atlasot **Apstiprināt**, tiek veikta tālāk norādītā darbība.

1. Kreditora rēķina statuss tiek atjaunināts uz **Apstiprināts**.
1. Apstiprinātais kreditora rēķins un ar to saistītie ieraksti kļūst tikai lasāmi, un tos nevar rediģēt vai dzēst.
1. Ja kāda no izmaksām faktiski atsaucas uz kreditora rēķina rindu kā daļu no salīdzināšanas procesa, visas izmaksu faktiskās izmaksas, kas ir saistītas ar atsauces kreditora rēķina rindu, tiek apgrieztas atpakaļ.
1. Jaunas izmaksu faktiskās izmaksas tiek izveidotas, izmantojot informāciju kreditora rēķina rindā.
1. Jūs vairs nevarat izveidot labojumu žurnālus, apstrādāt laika ierakstu atsaukšanu vai atcelt apgrieztā sākotnējā laika, izdevumu vai faktisko materiālu apstiprinājumu.
1. Programmā Dynamics 365 Finance projekta izmaksu **vērtība tiek atjaunināta,** izmantojot projektu integrācijas žurnālu, un sagādes integrācijas konts tiek *anulēts* pēc projekta integrācijas žurnāla grāmatošanas.

> [!NOTE]
> Ja kādai rindai kreditora rēķinā ir cits verifikācijas statuss, nevis **Pabeigts**, kreditora rēķinu nevar apstiprināt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
