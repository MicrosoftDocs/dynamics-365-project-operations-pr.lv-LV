---
title: Vairāku klientu pārvaldība projekta piedāvājumos — Lite
description: Šajā tēmā ir sniegta informācija par darbu ar piedāvājumiem ar vairākiem klientiem, kuri finansēs šo projektu. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bdda1a940e733270399d092e543c3982c47174d0
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181627"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a>Vairāku klientu pārvaldība projekta piedāvājumos — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta piedāvājumi atbalsta scenāriju, kurā priekšlikumā ir iesaistīti vairāki klienti, kas finansēs darījumu. Piedāvājuma cilnē **Kopsavilkums** ir lauks **Potenciālais klients**, kurā identificē darījuma primāro klientu. Citus darījuma klientus var iestatīt projekta piedāvājuma cilnē **Klienti**.

Visi piedāvājuma klienti projekta piedāvājuma cilnē **Klienti** pēc noklusējuma ir piedāvājuma rindas klienti visām **jaunajām** projekta piedāvājuma rindām, kas izveidotas šim piedāvājumam. Esošas projekta piedāvājuma rindas nepārņem jaunus piedāvājuma klientu ierakstus, kas ir izveidoti pēc tām.

Produktu piedāvājuma rindas automātiski tiek saistītas ar primāro klientu, kas ir arī klients laukā **Potenciālais klients** piedāvājuma cilnē **Kopsavilkums**.

Piedāvājuma klientus un piedāvājuma rindas klientus var pievienot, atjaunināt vai dzēst jebkurā brīdī, pirms piedāvājums ir iegūts.

## <a name="concept-of-a-primary-customer"></a>Primārā klienta koncepcija

Klients, kas norādīts projekta piedāvājuma kopsavilkuma cilnē kā potenciālais klients, ir piedāvājuma primārais klients. Mēģinot dzēst primāro klientu no piedāvājuma klientu saraksta, jums tiek parādīts kļūdas ziņojums par to, ka piedāvājumam nevar dzēst primārā klienta ierakstu.

Primāro klientu nedrīkst atjaunināt no piedāvājuma klienta saraksta. Tomēr varat ietekmēt primāro klientu, mainot potenciālo klientu piedāvājuma cilnē **Kopsavilkums**. Kad šis lauks tiek atjaunināts sadaļā **Piedāvājuma kopsavilkumā**, jaunais potenciālais klients tiek pievienots kā jauns piedāvājuma klients ar iestatītu karodziņu **Primārais**. Iepriekšējais potenciālais klients joprojām būs piedāvājuma klients.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Piedāvājuma klienta ieraksta izveide, atjaunināšana vai dzēšana

Piedāvājuma klientu var izveidot, atjaunināt vai dzēst no Cilnes **Piedāvājuma klienti** lapā **Piedāvājums**. Tālāk sniegtajā tabulā uzskaitītie lauki ir iekļauti piedāvājuma klienta ierakstā projekta piedāvājumā.

| **Lauks** | **Atrašanās vieta** | **Apraksts** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Konts | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Uzskaita visus aktīvos uzņēmumus. Pēc ieraksta izveides šis lauks tiek slēgts. Ja vēlaties to atjaunināt, dzēsiet ierakstu un izveidojiet to no jauna. Ja esat ierakstījis faktiskos datus vai ja piedāvājuma klienta ieraksts ir primārais klients, šo ierakstu varēsit dzēst. | Kad tiek izveidota piedāvājuma rinda, piedāvājuma klienti tiek pārkopēti kā piedāvājuma rindas klienti. Tāpat piedāvājuma klienti arī pārkopēti uz projekta līguma klientiem, kad piedāvājums ir iegūts. |
| Norēķinu sadalījuma procenti | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Norāda katra nepārdotā pārdošanas darījuma procentuālo attiecību, kas tiks piešķirta šim piedāvājuma klientam. | Pārkopēts uz jaunām piedāvājuma rindām un projekta līguma klientiem. |
| Rēķina saņēmēja kontaktpersonas vārds | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Šis ir teksta lauks, un tas ir jāizmanto, lai identificētu šī klienta kontaktpersonu rēķina saņemšanai. Tos pēc noklusējuma pārņem no saistītā uzņēmuma ieraksta | Pārkopēts uz projekta līguma klientiem, kad Piedāvājums ir iegūts, un pēc tam uz lauku Rēķina saņēmēja kontaktpersonas vārds rēķinā, kas tiek ģenerēts šim klientam. |
| Rēķina saņēmēja nosaukums/vārds | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Šis teksta lauks jāizmanto, lai identificētu šī klienta kontaktpersonu rēķina saņemšanai. | Pārkopēts uz projekta līguma klientiem, kad piedāvājums ir iegūts, un pēc tam uz lauku **Rēķina saņēmēja kontaktpersonas vārds** rēķinā, kas tiek ģenerēts šim klientam. |
| Maksājumu nosacījumi | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Šī ir opciju kopa ar vērtībām, kas pēc noklusējuma tiek pārņemtas no saistītā uzņēmuma ieraksta. | Pārkopēts uz projekta līguma klientiem, kad piedāvājums ir iegūts, un pēc tam uz lauku **Rēķina saņēmēja kontaktpersonas vārds** rēķinā, kas tiek ģenerēts šim klientam, |
| Tiek noapaļots | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Norāda, vai šis klients ir šī darījuma noklusējuma noapaļošanas klients. | Pārkopēts uz projekta līguma klientiem, kad piedāvājums ir iegūts. |
| Nepārsniedzamais ierobežojums | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Norāda, vai pastāv vienošanās ierobežojums vai maksimālā vērtība attiecībā uz kopējo summu, par ko šim klientam tiks izrakstīts rēķins šīs sadarbības ietvaros | Pārkopēts uz projekta līguma klientiem, kad piedāvājums ir iegūts. |

## <a name="editing-billing-split-percentages"></a>Norēķina sadalījuma procentu rediģēšana

Varat rediģēt norēķinu sadalījuma procentus, izmantojot režģa rediģēšanas pieredzi rindā. Ja norēķinu sadalījuma procentu summa neveido 100%, rodas kļūda. Pēc tam, kad ir atjaunināti norēķinu sadalījuma procenti, atsvaidziniet lapu, lai noņemtu kļūdu.

Varat arī mēģināt piedāvājuma klienta apakšrežģī atlasīt vienumu **Vienmērīgs sadalījums**. Šī darbība sadala norēķinus starp visiem piedāvājuma klientiem. Ja ir noapaļošanas koeficients, tas tiek pievienots noapaļošanas klientam. Viens no piedāvājuma klientiem vienmēr tiek marķēts kā noapaļošanas klients. tas nozīmē, ka piedāvājuma klienta ierakstam ir karodziņš **Noapaļošana** ir iestatīts kā **Jā**. Parasti tas ir piedāvājuma primārais klients, taču to var mainīt.
