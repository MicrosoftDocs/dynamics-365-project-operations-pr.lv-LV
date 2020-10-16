---
title: Vairāku klientu pārvaldība projekta piedāvājumu rindās
description: Šajā tēmā aprakstīts, kā pārvaldīt vairākus klientus projekta piedāvājuma rindās.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6a509fcf8d1fa11b4ce1ba1493d9c3cc64b4f22f
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965839"
---
# <a name="managing-multiple-customers-on-project-based-quote-lines"></a>Vairāku klientu pārvaldība projekta piedāvājumu rindās

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta piedāvājuma rindas atbalsta scenārijus, kuros katrā piedāvājuma rindā ir to klientu saraksts, kas par to maksā. Šis klientu saraksts projekta piedāvājuma rindā var būt tāds pats kā piedāvājuma klientu saraksts. Varat arī mainīt klientu sarakstu, lai tas būtu atšķirīgs. Kad projekta piedāvājums ir iegūts, projekta piedāvājuma rindas klientu saraksts tiek kopēts uz atbilstošo projekta līguma rindu, lai izveidotu izrietošo projekta līgumu. Projekta piedāvājuma klienti tiek pārkopēti projekta līgumā.

Izrakstot rēķinu saskaņā ar izrietošo projekta līgumu, klientu sarakstam projekta līguma rindā ir prioritāte pār projekta līguma sarakstu. Projekta līgumā esošais klientu saraksts pēc noklusējuma tiek izmantots kā noklusējuma vērtības jaunajās projekta līguma rindās.

Visi piedāvājuma klienti projekta piedāvājuma cilnē **Klienti** pēc noklusējuma ir piedāvājuma rindas klienti visām jaunajām projekta piedāvājuma rindām, kas izveidotas projekta piedāvājumam. Esošas projekta piedāvājuma rindas nepārņem jaunus piedāvājuma klientu ierakstus, kas ir izveidoti pēc tām.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Piedāvājuma rindas klienta ieraksta izveide, atjaunināšana vai dzēšana

Piedāvājuma rindas klientu var izveidot, atjaunināt vai dzēst cilnē **Piedāvājuma rindas klienti** lapā **Projekta piedāvājuma rinda**. Kad projekta piedāvājuma rindā pievienojat jaunu klientu, šis klients tiek pievienots arī vispārējam piedāvājumam kā piedāvājuma klients ar noklusējuma norēķinu sadalījumu procentu no kopējā piedāvājuma 0% apmērā. Rēķina sadalījuma procenti no kopējā piedāvājuma tiek kopēti jaunās piedāvājuma rindās un izrietošajā projekta līgumā. Tomēr, izrakstot rēķinu saskaņā ar līgumu, tiek izmantoti norēķinu sadalījuma procenti piedāvājuma rindu līmenī, nevis kopējā līguma līmenī. 

Tālāk sniegtajā tabulā parādīti lauki piedāvājuma rindas klienta ierakstā projekta piedāvājuma rindā.

| Lauks | Atrašanās vieta | Apraksts un norādes | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| **Uzņēmums** | Rediģējams režģis cilnē **Piedāvājuma klienti**, galvenā veidlapa un ātrās izveides veidlapas attiecībā uz piedāvājuma rindas klientu. | Uzskaita visus aktīvos uzņēmumus. Pēc ieraksta izveides šis lauks tiek slēgts. Ja ir jāatjaunina lauks, dzēsiet un atkārtoti izveidojiet šo ierakstu. Ja esat ierakstījis faktiskās vērtības, ierakstu nevar izdzēst. | Kad izvēlaties uzņēmumu no pievienojamo uzņēmumu galvenā saraksta, piedāvājuma rindas klients tiek pievienots arī kā piedāvājuma klients, kad to saglabājat. Kad piedāvājums ir iegūts, piedāvājuma rindas klienti tiek pārkopēti uz projekta līguma rindas klientiem. |
| **Norēķinu sadalījuma procenti** | Rediģējams režģis cilnē **Piedāvājuma klienti**, galvenā veidlapa un ātrās izveides veidlapas attiecībā uz piedāvājuma rindas klientu. | Norāda katra nepārdotā pārdošanas darījuma procentuālo attiecību, kas tiks piešķirta šim piedāvājuma rindas klientam. | Kopēts uz projekta līguma rindas klientiem. |
| **Nepārsniedzamais ierobežojums** | Rediģējams režģis cilnē **Piedāvājuma klienti**, galvenā veidlapa un ātrās izveides veidlapas attiecībā uz piedāvājuma rindas klientu. | Norāda, vai pastāv vienošanās ierobežojums vai maksimālā vērtība attiecībā uz kopējo summu, par ko šim klientam tiks izrakstīts rēķins saistībā ar šo piedāvājuma rindu. | Pārkopēts uz projekta līguma rindas klientiem, kad piedāvājums ir iegūts. |
| **Tiek noapaļots** | Rediģējams režģis cilnē **Piedāvājuma klienti**, galvenā veidlapa un ātrās izveides veidlapas attiecībā uz piedāvājuma rindas klientu. | Norāda, vai šis klients ir šīs projekta piedāvājuma rindas noklusējuma noapaļošanas klients. | Pārkopēts uz projekta līguma klientiem, kad piedāvājums ir iegūts. |

## <a name="edit-billing-split-percentages"></a>Norēķina sadalījuma procentu rediģēšana

Norēķinu sadalījuma procentus varat rediģēt rindā. Ja norēķinu sadalījuma procentu summa neveido 100%, rodas kļūda. Pēc tam, kad ir rediģēti norēķinu sadalījuma procenti, atsvaidziniet piedāvājuma rindu lapu, lai noņemtu kļūdu.

Izmantojiet vienmērīga sadalījuma darbību piedāvājuma rindu klientu apakšrežģī, lai piešķirtu norēķinu sadalīšanu starp visiem piedāvājuma rindas klientiem. Ja ir noapaļošanas koeficients, tas tiek pievienots noapaļošanas klientam. Viens no piedāvājuma rindas klientiem vienmēr ir marķēts kā noapaļošanas klients, kas nozīmē, ka piedāvājuma rindas klienta ierakstam karodziņš ir iestatīts kā **Jā**. 
