---
title: Vairāku klientu pārvaldība projekta līgumos
description: Šajā rakstā sniegta informācija par to, kā pārvaldīt vairākus debitorus projekta līgumā.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 78ee117c1068e7af4674cc3b21e1055fd05bb43a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928349"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Vairāku klientu pārvaldība projekta līgumos

Šajā rakstā sniegta informācija par to, kā pārvaldīt vairākus debitorus projekta līgumā. Ja darījuma finansēšanai ir nepieciešams līgums, kurā ir iesaistīti vairāki klienti, var izmantot projekta līgumu. Lapas **Projekta līgums** cilnē **Kopsavilkums** ir iekļauta informācija par darījuma primāro klientu. Citus klientus, kas piedalās darījumā, var pievienot cilnē **Klienti**.

Visi līguma klienti projekta līguma cilnē **Klienti** pēc noklusējuma ir arī līguma rindu klienti visās jaunajās projekta līguma rindās, kas izveidotas šim projekta līgumam. Esošās projekta līguma rindas nemanto jaunus līguma klientu ierakstus, kas tiek izveidoti vēlāk.

Varat pievienot, atjaunināt vai dzēst līgumu un līguma rindas klientus jebkurā brīdī, pirms līgums ir iegūts. Klients, kuram ir projekta līgums, ir jāiestata kā klients atbildīgajā uzņēmumā vai juridiskajā personā lapā **Klienti**. Juridiskās personas tiek iestatītas Dynamics 365 Project Operations modulī **Projektu pārvaldība un uzskaite** un ir pieejamas kā uzņēmumi Project Operations moduļos **Projekta pārdošana** un **Piegāde**.

## <a name="primary-customers"></a>Primārie klienti

Potenciālais klients, kurš ir norādīts projekta līguma cilnē **Kopsavilkums**, ir līguma primārais klients. Primāro klientu nevar atjaunināt, izmantojot līguma klienta sarakstu. Mēģinot dzēst primāro klientu no klientu saraksta līgumā, tiek parādīts kļūdas ziņojums, ka nevar dzēst primārā klienta ierakstu līgumā. Tā vietā nomainiet klientu projekta līguma cilnes **Kopsavilkums** laukā **Potenciālais klients**. Atjauninot šo lauku, jaunais atlasītais klients tiek pievienots kā jauns līguma klients ar karodziņa **Primārais** iestatījumu **Jā**. Iepriekšējais primārais klients joprojām ir līguma klients, taču tas vairs nav primārais klients.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Līguma klienta ieraksta izveide, atjaunināšana vai dzēšana

Varat izveidot, atjaunināt vai dzēst līguma klientu no lapas **Līgums** cilnes **Līguma klienti**. Tālāk minētie lauki ir iekļauti projekta līguma klienta ierakstā.

| **Lauks** | **Atrašanās vieta** | **Apraksts** | 
| --- | --- | --- | 
| Konts | Rediģējamais režģis cilnē **Līguma klienti** un galvenajā un ātrās izveides lapās līguma klientam. | Uzskaita visus aktīvos uzņēmumus. Pēc ieraksta izveides šis lauks tiek slēgts. Lai atjauninātu ierakstu, tas jādzēš un pēc tam jāizveido no jauna. Ja ir ierakstītas faktiskās vērtības vai ja līguma klienta ieraksts ir primārais klients, ierakstu nevar izdzēst. Kad tiek izveidota līguma rinda, līguma klienti tiek pārkopēti kā līguma rindas klienti. |
| Norēķinu sadalījuma procenti | Rediģējamais režģis cilnē **Līguma klienti** un galvenajā un ātrās izveides lapās līguma klientam. | Norādīts katra rēķinā neiekļautā pārdošanas darījuma procentuālais daudzums, kas ir piešķirts līguma klientam. Kad tiek izveidotas jaunas projekta līguma rindas, rēķina sadalījuma procentuālais daudzums tiek kopēts uz visām jaunajām līguma rindām un projekta līguma rindu klientiem. |
| Rēķina saņēmēja kontaktpersonas vārds | Rediģējamais režģis cilnē **Līguma klienti** un galvenajā un ātrās izveides lapās līguma klientam. | Šis teksta lauks ir jāizmanto, lai identificētu klienta rēķinu kontaktpersonu. Noklusējuma vērtība ir no saistītā uzņēmuma ieraksta. Kontaktpersonas vārds tiek pārkopēts uz **Rēķina saņēmēja kontaktpersonas vārds** rēķinā, kas tiek ģenerēts klientam. |
| Rēķina saņēmēja nosaukums/vārds | Rediģējamais režģis cilnē **Līguma klienti** un galvenajā un ātrās izveides lapās līguma klientam. | Izmantojiet šo lauku, lai identificētu klienta rēķinu kontaktpersonu. Noklusējuma vērtība ir no saistītā uzņēmuma ieraksta. Nosaukums tiek pārkopēts uz lauku **Rēķina saņēmēja kontaktpersonas vārds** rēķinā, kas tiek ģenerēts klientam. |
| Maksāšanas nosacījumi | Rediģējamais režģis cilnē **Līguma klienti** un galvenajā un ātrās izveides lapās līguma klientam. | Noklusējuma vērtība ir no saistītā uzņēmuma ieraksta. Noteikumi tiek pārkopēti uz **Rēķina saņēmēja kontaktpersonas vārds** rēķinā, kas tiek ģenerēts klientam. |
| Atbildīgais uzņēmums | Rediģējamais režģis cilnē **Projekta līguma klienti** un galvenajā un ātrās izveides lapās projekta līguma klientam. | Juridiskā persona, kurā klients ir iestatīts modulī **Projekta pārvaldība un uzskaite**. Šis lauks ir tikai lasāms un ir iestatīts kā uzņēmums, kam pieder projekta līgums.</br>Klientu saraksts, ko pievienot laukā **Uzņēmums**, jau tiek filtrēts kā atbildīgā uzņēmuma saraksts Project Operations modulī **Projekta pārvaldība un uzskaite**. Atbildīgais uzņēmums ir vienāds ar juridisko personu Project Operations modulī **Projekta pārvaldība un uzskaite**. Visas izmaksas un ieņēmumi, kas uzkrājušies no projekta, tiek aprēķināti īpašnieka uzņēmuma virsgrāmatā. |
| Tiek noapaļots | Rediģējamais režģis cilnē **Līguma klienti** un galvenajā un ātrās izveides lapās līguma klientam. | Norāda, vai klients ir darījuma noklusējuma noapaļošanas klients. Projekta līgumam var būt tikai viens noapaļošanas klients. Kad izmaksu un rēķinā neiekļautās pārdošanas sadalījums pēc daudzuma rada noapaļošanas starpību, šī atšķirība tiek piemērota faktiskajam daudzumam, kas tiek pieskaitīts klientam. |
| Nepārsniedzamais ierobežojums | Rediģējamais režģis cilnē **Līguma klienti** un galvenajā un ātrās izveides lapās līguma klientam. | Norāda, vai pastāv vienošanās ierobežojums vai maksājuma robežvērtība attiecībā uz kopējo summu, par kādu klientam tiks izrakstīts rēķins par piesaisti. Nepārsniedzamais ierobežojums, kas iestatīts līguma klienta līmenī, tiek vērtēts, balstoties uz rēķinā neiekļautajiem pārdošanas faktiskajiem rādītājiem, kas attiecas uz līguma klientu. |

## <a name="edit-billing-split-percentages"></a>Norēķina sadalījuma procentu rediģēšana

Rēķina sadalījuma procentuālo daudzumu var rediģēt, rediģējot režģi. Ja rēķina sadalījuma procentuālais daudzums kopā neveido 100 procentus, rodas kļūda. Pēc rēķina sadalījuma procentuālā daudzuma rediģēšanas atsvaidziniet lapu **Projekta līgums**, lai noņemtu kļūdu.

Varat arī projekta līguma klientu apakšrežģī atlasīt vienumu **Vienmērīgs sadalījums**. Rēķina sadalījums tiek vienmērīgi piešķirts visiem klientiem projekta līgumā. Ja pastāv noapaļošanas koeficients, tas tiks pievienots noapaļošanas klientam. Vienam no līguma klientiem vienmēr ir iestatīta karodziņa **Noapaļošana** opcija **Jā**. Šis klients ir noapaļošanas klients. Parasti noapaļošanas klients ir arī līguma primārais klients, bet tas nav obligāti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]