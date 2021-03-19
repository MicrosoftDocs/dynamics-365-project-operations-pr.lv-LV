---
title: Labotie rēķini
description: Šajā tēmā ir sniegta informācija par labotiem rēķiniem.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287832"
---
# <a name="corrected-invoices"></a>Labotie rēķini

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Apstiprinātos rēķinus var rediģēt. Rediģējot apstiprinātu rēķinu, tiek izveidots labotā rēķina melnraksts. Tā kā tiek pieņemts, ka vēlaties atsaukt visas transakcijas un daudzumus no sākotnējā rēķina, šis labotais rēķins ietver visas darbības no sākotnējā rēķina un visi tajā ietvertie daudzumi ir nulle (0).

Ja transakcijām nav nepieciešama labošana, tās var noņemt no melnraksta labojošā rēķina. Lai atsauktu vai atgrieztu tikai daļēju daudzumu, var rediģēt rindas informācijas lauku Daudzums. Ja atverat rēķina rindas informāciju, varat redzēt sākotnējo rēķina apjomu. Pašreizējo rēķina daudzumu var rediģēt, lai tas būtu mazāks vai lielāks par sākotnējo rēķina apjomu.

Kad apstiprināsit laboto rēķinu, sākotnējais izmaksātais pārdošanas apjoms tiek apgriezts un tiek izveidots jauns rēķins par pārdošanu. Ja daudzums tika samazināts, starpība izraisīs jaunu nemaksātu pārdošanas darījumu. Piemēram, ja sākotnējais apmaksātais pārdošanas apjoms ir astoņas stundas un labotā rēķina rindu informācijai ir samazināts daudzums uz sešām stundām, sākotnējā izmaksu rinda tiek atgriezta un tiek izveidoti divi jauni reālie dati.

- Rēķins par pārdošanu ir fiksētas sešas stundas.
- Neiekasēts pārdošanas apjoms atlikušajām divām stundām. Šo transakciju var izrakstīt vēlāk vai atzīmēt kā nepiemērojamu atkarībā no vienošanās ar klientu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]