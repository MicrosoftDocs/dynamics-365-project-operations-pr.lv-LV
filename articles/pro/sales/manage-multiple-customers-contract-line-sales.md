---
title: Pārvaldīt vairākus klientus projekta līguma rindās — Lite
description: Šajā rakstā ir sniegta informācija par vairāku klientu pārvaldīšanu projekta līguma rindās.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f7648c7ef7ec6ffb68932552a0c25b79f1f93733
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922139"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Pārvaldīt vairākus klientus projekta līguma rindās — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta līguma rindās var būt iekļauts to klientu saraksts, kas ir atbildīgi par apmaksu. Šis klientu saraksts projekta līguma rindā var būt tāds pats kā līguma klientu saraksts, bet tas nav obligāti jāaizpilda. Kad projekta piedāvājums ir uzvarējis un ir izveidots projekta līgums, piedāvājuma rindas klientu saraksts tiek iekopēts atbilstošajā līguma rindā. Piedāvājuma debitori tiek kopēti līgumā.

Kad projekta līgumam ir izrakstīts rēķins, projekta līguma rindas klientu saraksts tiek ņemts par prioritāti salīdzinājumā ar līguma klientu sarakstu. Projekta līguma klientu saraksts tiek izmantots tikai jauno līguma rindu noklusējumam.

Visi līguma klienti projekta līguma cilnē **Debitori** pēc noklusējuma ir arī līguma rindu klienti visās jaunajās līguma rindās, kas izveidotas šim projekta līgumam. Jebkādas esošas līguma rindas nemantos jaunos līgumu klientu ierakstus, kas tiek izveidoti vēlāk.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Līguma rindas klienta ieraksta izveide, atjaunināšana vai dzēšana

Līguma rindas klientu var izveidot, atjaunināt vai dzēst cilnē Līguma rindas klienti, kas atrodas lapā Projekta līguma rinda. Ja projekta līguma rindai tiek pievienots jauns klients, tas tiek pievienots arī vispārējam līgumam kā līguma klients ar noklusējuma rēķina sadalījuma procentuālo vērtību nulle procentu apmērā. Kopējā līgumā norādītie rēķina sadalījuma procenti tiek kopēti uz jaunām līguma rindām un iespējamo projekta līgumu. Tomēr, izrakstot rēķinu no līguma, tiek izmantots rēķinu dalījuma procents līguma rindas līmenī, nevis rēķinu sadalījuma procents vispārējā līguma līmenī.

Tālāk ir norādīti lauki projekta līguma rindas klienta ieraksta rindā **Līgums**, kas jāpatur prātā, kad ar tiem strādājat:

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| **Uzņēmums** | Rediģējamais režģis cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma klientam. | Visi aktīvie uzņēmumi. Pēc ieraksta izveides šis lauks tiek slēgts. Lai atjauninātu lauku, dzēsiet attiecīgo ierakstu un izveidojiet jaunu. Ja esat ierakstījis faktiskos datus, ierakstu nevar izdzēst. Tomēr šim uzņēmumam var atzīmēt rēķina sadalījuma procentuālo vērtību kā nulli. Ja ieraksts ir atzīmēts kā nulle, tiek ietekmētas visas turpmākās izmaksas un ieņēmumi, kas tiek piešķirti vai sadalīti šim klientam. | Kad uzņēmuma galvenajā sarakstā izvēlaties kādu uzņēmumu, lai tos pievienotu un saglabātu, līguma rinda klients tiek pievienots arī kā līguma klients. Kad tiek ģenerēti rēķini, tiek izmantoti līguma rindas klienti. |
| **Norēķinu sadalījuma procenti** | Rediģējamais režģis cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma klientam. | Šajā laukā ir norādīts katra rēķinā neiekļautā pārdošanas darījuma procentuālais daudzums, kas tiek piešķirts šim līguma rindas klientam. | Līguma rindas debitori un rēķina sadalījuma procenti tiek lietoti, kad tiek izveidoti faktiskie dati pēc apstiprināšanas un rēķina izveidošanas. |
| **Nepārsniedzamais ierobežojums** | Rediģējamais režģis cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma klientam. | Norāda, vai pastāv vienošanās ierobežojums vai maksājuma robežvērtība attiecībā uz kopējo summu, par kādu šim klientam līguma rindai tiks izrakstīts rēķins. | Nepārsniedzamais ierobežojums līguma rindas klientam tiek lietots tad, kad tiek izveidoti faktiskie dati un tiek ģenerēti rēķini. |
| **Tiek noapaļots** | Rediģējams režģis cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma rindas klientam. | Šis lauks norāda, vai šis klients ir noklusējuma noapaļošanas klients šai projekta līguma līnijai. | Ja ģenerējat faktiskos datus atbilstoši rēķina sadalījuma procentiem, var rasties dažas noapaļošanas atšķirības. Šim klientam šajā gadījumā tiek piešķirtas noapaļošanas atšķirības. |

## <a name="edit-billing-split-percentages"></a>Norēķina sadalījuma procentu rediģēšana

Rēķina sadalījuma procentus var rediģēt režģī. Ja rēķina sadalījuma procenti kopā neveido 100 procentus, radīsies kļūda. Pēc rēķina sadalījuma procentu rediģēšanas atsvaidziniet lapu, lai noņemtu kļūdu.

Varat arī līguma rindas klienta apakšrežģī atlasīt vienumu **Vienmērīgs sadalījums**. Šī darbība vienmērīgi piešķir norēķinu sadalījumu visiem līguma rindas klientiem. Ja pastāv noapaļošanas koeficients, tas tiks pievienots noapaļošanas klientam. Viens līguma rindas klients vienmēr tiek marķēts kā **Noapaļošanas** klients, un tam karodziņš **Noapaļošana** ir iestatīts uz **Jā**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]