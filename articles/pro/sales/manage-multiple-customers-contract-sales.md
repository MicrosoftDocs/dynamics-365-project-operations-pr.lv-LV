---
title: Pārvaldīt vairākus klientus projekta līgumus — lite
description: Šajā rakstā sniegta informācija par vairāku debitoru pārvaldību projektu līgumos.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17cd464bad81a01f5f334524a542104d6f25717b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917214"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Pārvaldīt vairākus klientus projekta līgumus — lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Projekta līgumi risinājumā Dynamics 365 Project Operations atbalsta scenāriju, kurā līgumā ir iesaistīti vairāki klienti, kas finansē darījumu. Lapas **Projekta līgums** cilnē **Kopsavilkums** ir iekļauts lauks **Klients**. Šis lauks norāda darījuma primāro klientu. Citus darījuma klientus var iestatīt lapas **Projekta līgums** cilnē **Klienti**.

Visi līguma klienti, kas uzskaitīti projekta līgumā, pēc noklusējuma ir arī līguma rindu klienti visās jaunajās projekta līguma rindās, kas izveidotas šim projekta līgumam. Esošās projekta līguma rindas nemanto jaunus līguma klientus, kad tiek izveidoti jauni ieraksti.

Produkta līguma rindas automātiski tiek saistītas ar primāro klientu.

Līguma klientus un līguma rindas klientus var pievienot, atjaunināt vai dzēst jebkurā brīdī, pirms līgums ir iegūts.

## <a name="primary-customer"></a>Primārais klients

Klients, kurš ir norādīts projekta līguma cilnē **Kopsavilkums**, jo iespējamais klients ir līguma primārais klients. Mēģinot dzēst primāro klientu no līguma klientu saraksta, tiek parādīts kļūdas ziņojums, ka nevar dzēst primārā klienta ierakstu līgumā.

Primāro klientu nevar atjaunināt, izmantojot līguma klientu sarakstu. Tā vietā mainiet potenciālo klientu līguma cilnē **Kopsavilkums**. Kad šis lauks tiek atjaunināts lapā **Līguma kopsavilkums**, jaunais klients tiek pievienots kā jauns līguma klients ar iestatītu karodziņu **Primārais**. Iepriekšējs primārais klients līgumā joprojām būs redzams kā klients.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Līguma klienta ieraksta izveide, atjaunināšana vai dzēšana

Līguma klientu var izveidot, atjaunināt vai dzēst lapas **Projekta līgums** cilnē **Klienti**. Tālāk norādītās tabulas lauki atrodas projekta līguma esošā līguma klienta ierakstā, un tas ir jāpatur prātā, kad strādājat ar līgumu.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| **Uzņēmums** | Režģi var rediģēt cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma klientam. | Uzskaita visus aktīvos uzņēmumus. Pēc ieraksta izveides šis lauks tiek slēgts. Lai atjauninātu uzņēmumu, dzēsiet attiecīgo ierakstu un izveidojiet to no jauna. Ja ir ierakstītas faktiskās vērtības vai ja līguma klienta ieraksts ir primārais klients, ierakstu nevar izdzēst. | Līguma klienti tiek pārkopēti kā līguma rindas klienti pēc līguma rindas izveides. |
| **Norēķinu sadalījuma procenti** | Režģi var rediģēt cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma klientam. | Norādīts katra rēķinā neiekļautā pārdošanas darījuma procentuālais daudzums, kas ir piešķirts šim līguma klientam. | Pārkopēts uz jaunām līguma rindām un projekta līguma rindu klientiem jaunās projekta līguma rindās. |
| **Rēķina saņēmēja kontaktpersonas vārds** | Režģi var rediģēt cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma klientam. | Šis teksta lauks jāizmanto, lai identificētu šī klienta kontaktpersonu rēķina saņemšanai. Šī lauka noklusējuma vērtība ir no saistītā uzņēmuma ieraksta. | Pārkopēts uz lauku **Rēķina saņēmēja kontaktpersonas vārds** rēķinā, kas tiek ģenerēts šim klientam. |
| **Rēķina saņēmēja nosaukums/vārds** | Režģi var rediģēt cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma klientam. | Šis teksta lauks jāizmanto, lai identificētu šī klienta kontaktpersonu rēķina saņemšanai. Šī lauka noklusējuma vērtība ir no saistītā uzņēmuma ieraksta. | Pārkopēts uz lauku **Rēķina saņēmēja kontaktpersonas vārds** rēķinā, kas tiek ģenerēts šim klientam. |
| **Maksājumu nosacījumi** | Režģi var rediģēt cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma klientam. | Noklusējuma vērtība ir no saistītā uzņēmuma ieraksta. | Pārkopēts uz lauku **Rēķina saņēmēja kontaktpersonas vārds** rēķinā, kas tiek ģenerēts šim klientam. |
| **Tiek noapaļots** | Režģi var rediģēt cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma klientam. | Norāda, vai šis klients ir šī darījuma noklusējuma noapaļošanas klients. Projekta līgumam var būt tikai viens noapaļošanas klients. | Kad izmaksu un rēķinā neiekļautās pārdošanas sadalījums pēc daudzuma rada noapaļošanas starpību, šī atšķirība tiek piemērota faktiskajam, kas tiek pieskaitīts šim klientam. |
| **Nepārsniedzamais ierobežojums** | Režģi var rediģēt cilnē **Līguma klienti** un veidlapās **Galvenais** un **Ātrā izveide** līguma klientam. | Norāda, vai pastāv vienošanās ierobežojums vai maksājuma robežvērtība attiecībā uz kopējo summu, par kādu klientam tiks izrakstīts rēķins par šo piesaisti. | Līguma klienta līmenī iestatītā vērtība **Nepārsniedzamais ierobežojums** tiks vērtēta pēc sadaļas **Rēķinā neiekļautie pārdošanas dati**, kas attiecas uz šo līguma klientu. |

## <a name="edit-billing-split-percentages"></a>Norēķina sadalījuma procentu rediģēšana

Rēķina sadalījuma procentus var rediģēt, izmantojot rindas režģa rediģēšanu. Ja rēķina sadalījuma procenti kopā neveido 100 procentus, jūs saņemsiet kļūdas paziņojumu. Pēc rēķina sadalījuma procentu rediģēšanas atsvaidziniet lapu, lai atmestu kļūdu.

Apakšrežģī **Līguma klienti** varat arī atlasīt opciju **Vienmērīgi sadalīt**, lai sadalītu norēķinus vienmērīgi visiem līguma klientiem. Ja pastāv noapaļošanas koeficients, tas tiks pievienots noapaļošanas klientam. Viens no līguma klientiem vienmēr ir marķēts kā **noapaļošanas** klients, kas nozīmē, ka līguma klienta ierakstam noapaļošanas karodziņš ir iestatīts uz **Jā**. Parasti tas ir līguma primārais klients, bet to var arī mainīt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]