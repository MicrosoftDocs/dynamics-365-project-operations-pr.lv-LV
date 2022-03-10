---
title: Pārvaldīt vairākus klientus projekta līguma rindās
description: Šajā tēmā ir sniegta informācija par darbu ar līguma rindām un līgumiem, kuros ir vairāki klienti.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25ce50251380d1ca136a81268c74a0675928011dc2eefaee21df83cdd62845a9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992125"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Pārvaldīt vairākus klientus projekta līguma rindās

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta līguma rindās var būt iekļauts to klientu saraksts, kas ir atbildīgi par apmaksu. Šis klientu saraksts projekta līguma rindā var būt tāds pats kā līguma klientu saraksts, bet tas nav obligāti jāaizpilda. Kad projekta piedāvājums ir uzvarējis un ir izveidots projekta līgums, piedāvājuma rindas klientu saraksts tiek iekopēts atbilstošajā līguma rindā. Piedāvājuma debitori tiek kopēti līgumā.

Kad projekta līgumam ir izrakstīts rēķins, projekta līguma rindas klientu saraksts tiek ņemts par prioritāti salīdzinājumā ar līguma klientu sarakstu. Projekta līguma klientu saraksts tiek izmantots tikai jauno līguma rindu noklusējumam.

Visi līguma klienti projekta līguma cilnē **Debitori** pēc noklusējuma ir arī līguma rindu klienti visās jaunajās līguma rindās, kas izveidotas šim projekta līgumam. Jebkādas esošas līguma rindas nemantos jaunos līgumu klientu ierakstus, kas tiek izveidoti vēlāk.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Līguma rindas klienta ieraksta izveide, atjaunināšana vai dzēšana

Līguma rindas klientu var izveidot, atjaunināt vai dzēst cilnē **Līguma rindas klienti**, kas atrodas lapā **Projekta līguma rinda**. Ja projekta līguma rindai tiek pievienots jauns klients, tas tiek pievienots arī vispārējam līgumam kā līguma klients ar noklusējuma rēķina sadalījuma procentuālo vērtību nulle procentu apmērā. Kopējā līgumā norādītie rēķina sadalījuma procenti tiek kopēti uz jaunām līguma rindām un iespējamo projekta līgumu. Tomēr, izrakstot rēķinu no līguma, tiek izmantots rēķinu dalījuma procents līguma rindas līmenī, nevis rēķinu sadalījuma procents vispārējā līguma līmenī. 

Tālāk ir norādīti lauki Līguma rindas klienta ierakstā projekta Līguma rindā, kas jāpatur prātā, kad ar tiem strādājat:

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| Konts | Rediģējams režģis cilnē **Līguma rindas klienti** un veidlapās Galvenais un Ātrā izveide līguma rindas klientam. | Visi aktīvie uzņēmumi. Pēc ieraksta izveides šis lauks tiek slēgts. Lai atjauninātu lauku, dzēsiet attiecīgo ierakstu un izveidojiet jaunu. Ja esat ierakstījis faktiskos datus, ierakstu nevar izdzēst. Tomēr šim uzņēmumam var atzīmēt rēķina sadalījuma procentuālo vērtību kā nulli. Ja ieraksts ir atzīmēts kā nulle, tiek ietekmētas visas turpmākās izmaksas un ieņēmumi, kas tiek piešķirti vai sadalīti šim klientam. | Kad uzņēmuma galvenajā sarakstā izvēlaties kādu uzņēmumu, lai tos pievienotu un saglabātu, līguma rinda klients tiek pievienots arī kā līguma klients. Kad tiek ģenerēti rēķini, tiek izmantoti līguma rindas klienti. |
| Norēķinu sadalījuma procenti | Rediģējams režģis cilnē **Līguma rindas klienti** un veidlapās Galvenais un Ātrā izveide līguma rindas klientam. | Šajā laukā ir norādīts katra rēķinā neiekļautā pārdošanas darījuma procentuālais daudzums, kas tiek piešķirts šim līguma rindas klientam. | Līguma rindas debitori un rēķina sadalījuma procenti tiek lietoti, kad tiek izveidoti faktiskie dati pēc apstiprināšanas un rēķina izveidošanas. |
| Nepārsniedzamais ierobežojums | Rediģējams režģis cilnē **Līguma rindas klienti** un veidlapās Galvenais un Ātrā izveide līguma rindas klientam. | Norāda, vai pastāv vienošanās ierobežojums vai maksājuma robežvērtība attiecībā uz kopējo summu, par kādu šim klientam līguma rindai tiks izrakstīts rēķins. | Nepārsniedzamais ierobežojums līguma rindas klientam tiek lietots tad, kad tiek izveidoti faktiskie dati un tiek ģenerēti rēķini. |
| Atbildīgais uzņēmums | Rediģējams režģis cilnē **Piedāvājuma rindas klienti** un veidlapās Galvenais un Ātrā izveide piedāvājuma rindas klientam. | Šī klienta iestatītā juridiskā entītija. Šis lauks ir tikai lasāms un ir iestatīts kā uzņēmums, kam pieder piedāvājums. Klientu saraksts, ko pievienot laukā **Konts**, jau tiek filtrēts no īpašnieka uzņēmuma saraksta. | Īpašnieka uzņēmuma jēdziens ir vienāds ar juridiskas personas jēdzienu. Visas izmaksas un ieņēmumi, kas uzkrājušies no šī projekta, tiek aprēķināti īpašnieka uzņēmuma Virsgrāmatā. |
| Tiek noapaļots | Rediģējams režģis cilnē **Līguma rindas klienti** un veidlapās Galvenais un Ātrā izveide līguma rindas klientam. | Šis lauks norāda, vai šis klients ir noklusējuma noapaļošanas klients šai projekta līguma līnijai. | Ja ģenerējat faktiskos datus atbilstoši rēķina sadalījuma procentiem, var rasties dažas noapaļošanas atšķirības. Šim klientam šajā gadījumā tiek piešķirtas noapaļošanas atšķirības. |

## <a name="edit-billing-split-percentages"></a>Norēķina sadalījuma procentu rediģēšana

Rēķina sadalījuma procentus var rediģēt režģī. Ja rēķina sadalījuma procenti kopā neveido 100 procentus, radīsies kļūda. Pēc rēķina sadalījuma procentu rediģēšanas atsvaidziniet lapu, lai noņemtu kļūdu.

Varat arī mēģināt līguma rindas klienta apakšrežģī atlasīt vienumu **Vienmērīgs sadalījums**. Šī darbība vienmērīgi piešķir norēķinu sadalījumu visiem līguma rindas klientiem. Ja pastāv noapaļošanas koeficients, tas tiks pievienots noapaļošanas klientam. Viens līguma rindas klients vienmēr tiek marķēts kā **Noapaļošanas** klients, un tam karodziņš **Noapaļošana** ir iestatīts uz **Jā**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]