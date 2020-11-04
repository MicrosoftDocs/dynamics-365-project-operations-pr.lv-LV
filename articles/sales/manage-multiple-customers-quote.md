---
title: Vairāku klientu pārvaldība projekta piedāvājumos
description: Šajā tēmā ir sniegta informācija par darbu ar piedāvājumiem, kas ietver vairākus klientus, kuri finansēs šo projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080298"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Vairāku klientu pārvaldība projekta piedāvājumos

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta piedāvājumi atbalsta scenāriju, kurā priekšlikumā ir iesaistīti vairāki klienti, kas finansēs darījumu. Piedāvājuma cilnē **Kopsavilkums** ir lauks **Potenciālais klients** , kurā identificē darījuma primāro klientu. Citus darījuma klientus var iestatīt projekta piedāvājuma cilnē **Klienti**.

Visi piedāvājuma klienti projekta piedāvājuma cilnē **Klienti** pēc noklusējuma ir piedāvājuma rindas klienti visām **jaunajām** projekta piedāvājuma rindām, kas izveidotas šim piedāvājumam. Esošas projekta piedāvājuma rindas nepārņem jaunus piedāvājuma klientu ierakstus, kas ir izveidoti pēc tām.

Piedāvājuma klientus un piedāvājuma rindas klientus var pievienot, atjaunināt vai dzēst jebkurā brīdī, pirms piedāvājums ir iegūts. Piedāvājumam ir jāiestata derīgs klients kā klients Atbildīgajā uzņēmumā vai Juridiskajā personā lapā **Klienti**. Juridiskās personas iestata Dynamics 365 Project Operations modulī **Projekta pārvaldība un uzskaite** , un tie tiek padarīti pieejami kā Uzņēmumi Project Operations moduļos **Projekta pārdošana un izpilde**.

## <a name="concept-of-a-primary-customer"></a>Primārā klienta koncepcija

Klients, kas ir norādīts projekta piedāvājuma cilnē **Kopsavilkums** kā potenciālais klients, ir piedāvājuma primārais klients. Mēģinot dzēst primāro klientu no piedāvājuma klientu saraksta, tiek parādīts kļūdas ziņojums par to, ka piedāvājumam nevar dzēst primārā klienta ierakstu.

Primāro klientu nedrīkst atjaunināt no piedāvājuma klienta saraksta. Tomēr varat ietekmēt primāro klientu, mainot potenciālo klientu piedāvājuma cilnē **Kopsavilkums**. Kad šis lauks tiek atjaunināts sadaļā **Piedāvājuma kopsavilkumā** , jaunais potenciālais klients tiek pievienots kā jauns piedāvājuma klients ar iestatītu karodziņu **Primārais**. Iepriekšējais potenciālais klients joprojām būs piedāvājuma klients.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Piedāvājuma klienta ieraksta izveide, atjaunināšana vai dzēšana

Piedāvājuma klientu var izveidot, atjaunināt vai dzēst no Cilnes **Piedāvājuma klienti** lapā **Piedāvājums**. Tālāk sniegtajā tabulā uzskaitītie lauki ir iekļauti piedāvājuma klienta ierakstā projekta piedāvājumā.

| **Lauks** | **Atrašanās vieta** | **Atbilstība, mērķis un norādes** | **Lejupstraumes ietekme** |
| --- | --- | --- | --- |
| Konts | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Uzskaita visus aktīvos uzņēmumus. Pēc ieraksta izveides šis lauks tiek slēgts. Ja vēlaties to atjaunināt, dzēsiet ierakstu un izveidojiet to no jauna. Ja esat ierakstījis faktiskos datus vai ja piedāvājuma klienta ieraksts ir primārais klients, šo ierakstu varēsit dzēst. | Kad tiek izveidota piedāvājuma rinda, piedāvājuma klienti tiek pārkopēti kā piedāvājuma rindas klienti. Tāpat piedāvājuma klienti arī pārkopēti uz projekta līguma klientiem, kad piedāvājums ir iegūts. |
| Norēķinu sadalījuma procenti | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Norāda katra nepārdotā pārdošanas darījuma procentuālo attiecību, kas tiks piešķirta šim piedāvājuma klientam. | Pārkopēts uz jaunizveidotām piedāvājuma rindām un projekta līguma klientiem. |
| Rēķina saņēmēja kontaktpersonas vārds | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Šis ir teksta lauks, un tas ir jāizmanto, lai identificētu šī klienta kontaktpersonu rēķina saņemšanai. Tos pēc noklusējuma pārņem no saistītā uzņēmuma ieraksta | Pārkopēts uz projekta līguma klientiem, kad Piedāvājums ir iegūts, un pēc tam uz lauku Rēķina saņēmēja kontaktpersonas vārds rēķinā, kas tiek ģenerēts šim klientam. |
| Rēķina saņēmēja nosaukums/vārds | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Šis teksta lauks jāizmanto, lai identificētu šī klienta kontaktpersonu rēķina saņemšanai. | Pārkopēts uz projekta līguma klientiem, kad piedāvājums ir iegūts, un pēc tam uz lauku **Rēķina saņēmēja kontaktpersonas vārds** rēķinā, kas tiek ģenerēts šim klientam. |
| Maksājumu nosacījumi | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Šī ir opciju kopa ar vērtībām, kas pēc noklusējuma tiek pārņemtas no saistītā uzņēmuma ieraksta. | Pārkopēts uz projekta līguma klientiem, kad piedāvājums ir iegūts, un pēc tam uz lauku **Rēķina saņēmēja kontaktpersonas vārds** rēķinā, kas tiek ģenerēts šim klientam. |
| Tiek noapaļots | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Norāda, vai šis klients ir šī darījuma noklusējuma noapaļošanas klients. | Pārkopēts uz projekta līguma klientiem, kad piedāvājums ir iegūts. |
| Atbildīgais uzņēmums | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Šī klienta iestatītajai juridiskajai personai ir iestatīts modulis **Projekta pārvaldība un uzskaite**. Šis lauks ir tikai lasāms un ir iestatīts kā pats par piedāvājumu atbildīgais uzņēmums. Klientu saraksts, ko pievienot laukā **Uzņēmums** , jau tiek filtrēts kā šī atbildīgā uzņēmuma saraksts Project Operations modulī **Projekta pārvaldība un uzskaite**. | Atbildīgais uzņēmums ir pielīdzināms Juridiskās personas jēdzienam Project Operations modulī **Projekta pārvaldība un grāmatvedība**. Visas izmaksas un ieņēmumi, kas uzkrājas no šī projekta, tiek ieskaitīti atbildīgā uzņēmuma Virsgrāmatā, |
| Nepārsniedzamais ierobežojums | Rediģējamais režģis cilnē **Piedāvājuma klienti** un veidlapās **Galvenā** un **Ātrā izveide** attiecībā uz piedāvājuma klientu. | Norāda, vai pastāv vienošanās ierobežojums vai maksimālā vērtība attiecībā uz kopējo summu, par ko šim klientam tiks izrakstīts rēķins šīs sadarbības ietvaros. | Pārkopēts uz projekta līguma klientiem, kad piedāvājums ir iegūts. |

## <a name="editing-billing-split-percentages"></a>Norēķina sadalījuma procentu rediģēšana

Varat rediģēt norēķinu sadalījuma procentus, izmantojot režģa rediģēšanas pieredzi rindā. Ja norēķinu sadalījuma procentu summa neveido 100%, rodas kļūda. Pēc tam, kad ir atjaunināti norēķinu sadalījuma procenti, atsvaidziniet lapu, lai noņemtu kļūdu.

Varat arī mēģināt atlasīt opciju **Vienmērīgs sadalījums** piedāvājuma klientu apakšrežģī. Šī darbība sadala norēķinus starp visiem piedāvājuma klientiem. Ja ir noapaļošanas koeficients, tas tiek pievienots noapaļošanas klientam. Viens no piedāvājuma klientiem vienmēr tiek marķēts kā noapaļošanas klients. tas nozīmē, ka piedāvājuma klienta ierakstam ir karodziņš **Noapaļošana** ir iestatīts kā **Jā**. Parasti tas ir piedāvājuma primārais klients, taču to var mainīt.