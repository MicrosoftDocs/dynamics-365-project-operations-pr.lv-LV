---
title: Projekta rēķina apstiprināšana
description: Šajā rakstā izskaidrots, kā apstiprināt projekta piegādātāja rēķinu programmā Microsoft Dynamics 365 Project Operations, un aprakstīta projekta piegādātāja rēķina apstiprināšanas finanšu ietekme.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261521"
---
# <a name="confirm-a-project-vendor-invoice"></a>Projekta rēķina apstiprināšana

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Kad esat pārbaudījis visas rindas piegādātāja rēķinā programmā Microsoft Dynamics 365 Project Operations, varat izmantot apstiprināšanas darbību, lai apstiprinātu piegādātāja rēķinu.

Ja piegādātāja rēķinā tiek atlasīts **Apstiprināt**, notiek šāda darbība:

1. piegādātāja rēķina statuss tiek atjaunināts uz **Apstiprināts**.
2. Apstiprinātais piegādātāja rēķins un tā saistītie ieraksti kļūst tikai lasāmi, un tos nevar rediģēt vai dzēst.
3. Ja kādas faktiskās izmaksas atsaucas uz piegādātāja rēķina rindu kā daļu no atbilstības noteikšanas procesa, tiek apgrieztas visas faktiskās izmaksas, kas ir saistītas ar atsaucē norādīto piegādātāja rēķina rindu.
4. Tiek izveidotas jaunas faktiskās izmaksas, izmantojot informāciju no piegādātāja rēķina rindas.
5. Pēc piegādātāja rēķina apstiprināšanas vairs nevar izveidot labošanas žurnālus, apstrādāt laika ierakstu atsaukšanu vai atcelt sākotnējos apgrieztos laika, izdevumu vai materiālu faktiskos datus.

> [!NOTE]
> Ja kādai no piegādātāja rēķina rindām ir pārbaudes statuss, kas nav **Pabeigts**, nevar apstiprināt piegādātāja rēķinu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
