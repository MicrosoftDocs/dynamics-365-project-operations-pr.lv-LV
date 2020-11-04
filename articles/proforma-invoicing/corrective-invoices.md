---
title: Labotie rēķini
description: Šajā tēmā ir sniegta informācija par labotiem rēķiniem.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080612"
---
# <a name="corrected-invoices"></a>Labotie rēķini

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Apstiprinātos rēķinus var rediģēt. Rediģējot apstiprinātu rēķinu, tiek izveidots labotā rēķina melnraksts. Tā kā tiek pieņemts, ka vēlaties atsaukt visas transakcijas un daudzumus no sākotnējā rēķina, šis labotais rēķins ietver visas darbības no sākotnējā rēķina un visi tajā ietvertie daudzumi ir nulle (0).

Ja transakcijām nav nepieciešama labošana, tās var noņemt no melnraksta labojošā rēķina. Lai atsauktu vai atgrieztu tikai daļēju daudzumu, var rediģēt rindas informācijas lauku Daudzums. Ja atverat rēķina rindas informāciju, varat redzēt sākotnējo rēķina apjomu. Pašreizējo rēķina daudzumu var rediģēt, lai tas būtu mazāks vai lielāks par sākotnējo rēķina apjomu.

Kad apstiprināsit laboto rēķinu, sākotnējais izmaksātais pārdošanas apjoms tiek apgriezts un tiek izveidots jauns rēķins par pārdošanu. Ja daudzums tika samazināts, starpība izraisīs jaunu nemaksātu pārdošanas darījumu. Piemēram, ja sākotnējais apmaksātais pārdošanas apjoms ir astoņas stundas un labotā rēķina rindu informācijai ir samazināts daudzums uz sešām stundām, sākotnējā izmaksu rinda tiek atgriezta un tiek izveidoti divi jauni reālie dati.

- Rēķins par pārdošanu ir fiksētas sešas stundas.
- Neiekasēts pārdošanas apjoms atlikušajām divām stundām. Šo transakciju var izrakstīt vēlāk vai atzīmēt kā nepiemērojamu atkarībā no vienošanās ar klientu.
