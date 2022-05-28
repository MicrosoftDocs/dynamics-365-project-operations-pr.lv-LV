---
title: Atcelt projekta kreditora rēķinu
description: Šajā tēmā paskaidrots, kā atcelt projekta kreditora rēķinu programmā Microsoft Dynamics 365 Project Operations, un projekta kreditora rēķina atcelšanas finansiālā ietekme.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580649"
---
# <a name="cancel-a-project-vendor-invoice"></a>Atcelt projekta kreditora rēķinu

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Pēc kreditora rēķina apstiprināšanas to nevar rediģēt vai dzēst. Ja apstiprinātā kreditora rēķinā radās kļūda, varat izmantot darbību Atcelt, lai atsauktu kreditora rēķina ietekmi un izveidotu jaunu kreditora rēķinu.

Kreditora rēķinā atlasot **Atcelt**, notiek šāda darbība:

1. Kreditora rēķina stāvoklis tiek atjaunināts uz **Atcelts**.
2. Atceltais kreditora rēķins un ar to saistītie ieraksti kļūst tikai lasāmi, un tos nevar rediģēt vai dzēst.
3. Visas izmaksu faktiskās darbības, kas tika izveidotas, pamatojoties uz kreditora rēķina rindām kā daļa no kreditora rēķina apstiprinājuma, tiek atsauktas.
4. Ja izmaksu fakti tika saistīti ar kreditora rēķina rindām kā daļa no atbilstības procesa, sākotnējais kreditora rēķina apstiprinājums tos atsauca. Kreditora rēķina atcelšanas laikā šīs izmaksu faktiskās tiek izveidotas no jauna. Izcelsme norāda uz laika, izdevumu vai materiālu lietojuma ierakstiem.
5. Pēc piegādātāja rēķina atcelšanas var vēlreiz izveidot labojumu žurnālus, apstrādāt laika ieraksta atsaukšanas un atcelt sākotnējā laika, izdevumu vai materiālu faktiskās apstiprināšanas.

> [!NOTE]
> Var atcelt tikai apstiprinātos projekta kreditoru rēķinus. Kreditoru rēķinus citos štatos nevar atcelt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
