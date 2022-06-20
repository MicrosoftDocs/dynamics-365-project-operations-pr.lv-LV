---
title: Projekta rēķina apstiprināšana
description: Šajā rakstā paskaidrots, kā apstiprināt projekta kreditora rēķinu Microsoft Dynamics 365 Project Operations un projekta kreditora rēķina apstiprināšanas finansiālā ietekme.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932443"
---
# <a name="confirm-a-project-vendor-invoice"></a>Projekta rēķina apstiprināšana

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Pēc tam, kad esat pārbaudījis visas Microsoft Dynamics 365 Project Operations piegādātāja rēķina rindas, piegādātāja rēķina apstiprināšanai varat izmantot darbību Apstiprināt.

Atlasot **Apstiprināt** kreditora rēķinā, notiek šāda darbība:

1. Kreditora rēķina stāvoklis ir atjaunināts uz **Apstiprināts**.
2. Apstiprinātais kreditora rēķins un ar to saistītie ieraksti kļūst tikai lasāmi, un tos nevar rediģēt vai dzēst.
3. Ja kāds izmaksu faktiskais atsaucas uz kreditora rēķina rindu kā daļu no atbilstības procesa, visas izmaksu faktiskās izmaksas, kas ir saistītas ar atsauces kreditora rēķina rindu, tiek anulētas.
4. Jaunas izmaksu faktiskās versijas tiek izveidotas, izmantojot informāciju kreditora rēķina rindā.
5. Pēc piegādātāja rēķina apstiprināšanas vairs nevar izveidot labojumu žurnālus, apstrādāt laika ieraksta atsaukšanas vai atcelt anulēt anulētā sākotnējā laika, izdevumu vai materiālu faktisko apstiprinājumu.

> [!NOTE]
> Ja kādai kreditora rēķina rindai ir cits pārbaudes statuss, nevis **Pabeigts**, kreditora rēķinu nevar apstiprināt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
