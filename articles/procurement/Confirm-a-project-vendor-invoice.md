---
title: Projekta kreditoru rēķinu apstiprināšana
description: Šajā rakstā izskaidrots, kā apstiprināt projekta piegādātāja rēķinu programmā Microsoft Dynamics 365 Project Operations, un aprakstīta projekta piegādātāja rēķina apstiprināšanas finanšu ietekme.
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
# <a name="confirm-project-vendor-invoices"></a>Projekta kreditoru rēķinu apstiprināšana

_ **Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem

Ja ir iespējots parametrs **Nepieciešams manuāls projekta vadītāja apstiprinājums**, piegādātāju rēķiniem, kas izveidoti Microsoft Dataverse, ir statuss **Melnraksts**. Šādi izveidotie piegādātāju rēķini ir jāpārskata un manuāli jāapstiprina. Ja ir atspējots parametrs **Nepieciešams manuāls projekta vadītāja apstiprinājums**, piegādātāju rēķiniem, kas izveidoti Dataverse, tiek automātiski apstiprināti. Nav jāveic papildu darbības. 

Kad esat pārbaudījis visas rindas piegādātāja rēķinā programmā Dynamics 365 Project Operations, atlasiet **Apstiprināt**, lai apstiprinātu piegādātāja rēķinu.

Ja piegādātāja rēķinā tiek atlasīts **Apstiprināt**, notiek šāda darbība:

1. piegādātāja rēķina statuss tiek atjaunināts uz **Apstiprināts**.
1. Apstiprinātais piegādātāja rēķins un tā saistītie ieraksti kļūst tikai lasāmi, un tos nevar rediģēt vai dzēst.
1. Ja kādas faktiskās izmaksas atsaucas uz piegādātāja rēķina rindu kā daļu no atbilstības noteikšanas procesa, tiek apgrieztas visas faktiskās izmaksas, kas ir saistītas ar atsaucē norādīto piegādātāja rēķina rindu.
1. Tiek izveidotas jaunas faktiskās izmaksas, izmantojot informāciju no piegādātāja rēķina rindas.
1. Vairs nevar izveidot labošanas žurnālus, apstrādāt laika ierakstu atsaukšanu vai atcelt sākotnējo apgriezto laika, izdevumu vai materiālu faktisko datu apstiprinājumu.
1. Programmā Dynamics 365 Finance vērtība **Projekta izmaksas** tiek atjaunināta, izmantojot projekta integrācijas žurnālu, un iepirkumu integrācijas konts tiek *apgriezts* pēc projekta integrācijas žurnāla grāmatošanas.

> [!NOTE]
> Ja kādai no piegādātāja rēķina rindām ir pārbaudes statuss, kas nav **Pabeigts**, nevar apstiprināt piegādātāja rēķinu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
