---
title: Atcelt projekta kreditora rēķinu
description: Šajā rakstā izskaidrots, kā atcelt projekta piegādātāja rēķinu programmā Microsoft Dynamics 365 Project Operations, un izskaidrota projekta piegādātāja rēķina atcelšanas finanšu ietekme.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261100"
---
# <a name="cancel-a-project-vendor-invoice"></a>Atcelt projekta kreditora rēķinu

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Pēc piegādātāja rēķina apstiprināšanas to nevar rediģēt vai dzēst. Ja apstiprinātā piegādātāja rēķinā bijusi kļūda, varat izmantot atcelšanas darbību, lai apgrieztu piegādātāja rēķina ietekmi un izveidotu jaunu piegādātāja rēķinu.

Ja piegādātāja rēķinā tiek atlasīts **Atcelt**, notiek šāda darbība:

1. piegādātāja rēķina statuss tiek atjaunināts uz **Atcelts**.
2. Atceltais piegādātāja rēķins un tā saistītie ieraksti kļūst tikai lasāmi, un tos nevar rediģēt vai dzēst.
3. Tiek atgriezti visi izmaksu faktiskie dati, kas tika izveidoti, par pamatu izmantojot piegādātāja rēķina rindas kā daļu no piegādātāja rēķina apstiprinājuma.
4. Ja ar piegādātāja rēķina rindām kā daļu no atbilstības noteikšanas procesa ir saistīti jebkādi izmaksu faktiskie dati, tos apvērš sākotnējā piegādātāja rēķina apstiprināšana. Piegādātāja rēķina atcelšanas laikā šie izmaksu faktiskie dati tiek izveidoti atkārtoti. Izcelsme norāda uz laika, izmaksu vai materiālu lietojuma ierakstiem.
5. Pēc piegādātāja rēķina atcelšanas varat vēlreiz izveidot labošanas žurnālus, apstrādāt laika ierakstu atsaukšanu un atcelt sākotnējos laika, izmaksu vai materiālu faktisko datu apstiprinājumu.

> [!NOTE]
> Atcelt var tikai atceltus projektu piegādātāju rēķinus. Nevar atcelt piegādātāju rēķinus citos gadījumos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
