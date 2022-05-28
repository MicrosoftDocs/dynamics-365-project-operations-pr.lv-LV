---
title: Izrakstīšanas rezervju pārvaldība
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt skatīt uzkrātos rēķinus risinājumā Project Operations un strādāt ar tiem.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9837af0d3c0b2476edab35a53092cf95a44e5244
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599999"
---
# <a name="manage-billing-backlog"></a>Izrakstīšanas rezervju pārvaldība

_ **Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem

Dynamics 365 Project Operations līdzeklī ir īpaši skati, kas palīdz pārvaldīt norēķinu neizpildīto darbību žurnālu. Lai pārvaldītu norēķinu neizpildīto darbību žurnālu, atlasiet saites apgabalā **Pārdošana**, kas atrodas sadaļā **Norēķini**. 

Ir pieejami šādi skatu režīmi:

- Honorāri un avansi
- Pieejamie honorāri un avansi
- Fiksētu cenu atskaites punkti
- Laika un materiālu rēķinu izrakstīšanas rezerve

## <a name="retainers-and-advances"></a>Honorāri un avansi

Skatā **Honorāri un avansi** ir uzskaitīti honorāri un avansi visos projekta līgumos. Pēc tam kad honorārs vai avanss ir izrakstīts rēķinā, avansa summa kļūst pieejama izmantošanai.

## <a name="available-retainers-and-advances"></a>Pieejamie honorāri un avansi

Skatā **Pieejamie honorāri un avansi** ir uzskaitīti visi pieejamie honorāri un avansi visos projekta līgumos. Pēc tam kad honorārs vai avanss ir izrakstīts rēķinā, avansa summa kļūst pieejama izmantošanai un tiek pievienots sarakstam. Pēc tam, kad honorārs vai avanss ir pilnībā izmantots, tas tiek noņemts no saraksta.

## <a name="fixed-price-milestones"></a>Fiksētu cenu atskaites punkti

Skatā **Fiksētas cenas atskaites punkti** tiek uzskaitīti visi fiksētas cenas atskaites punkti visās projekta līguma rindās. Šajā skatā atsevišķus vai vairākus atskaites punktus var atzīmēt kā **Gatavs rēķinam** vai **Nav gatavs rēķinam**. Ja atskaites punkts tiek atzīmēts kā **Gatavs rēķina izrakstīšanai**, tas kļūst pieejams ievietošanai rēķina melnrakstā.

Ja vairāku klientu līguma rindām ir fiksētas cenas rēķina izrakstīšanas metode, katram klientam līguma rindā tiek izveidots atskaites punkts. Atskaites punktu var izveidot un pēc tam sadalīt atsevišķiem konkrētu klientu atskaites punktu ierakstiem. Šī sadalīšana ir iekšēja un atbilst rēķina procentu sadalījumam, kas katram klientam noteikts līguma rindā. Skatā **Fiksētu cenu atskaites punkti** tiks parādīti atsevišķi klientam specifiski atskaites punktu ieraksti. Šajā skatā katru no šiem atskaites punktu ierakstiem var atsevišķi atzīmēt kā **Gatavs rēķina izrakstīšanai**. Kad viens vai vairāki saistītie atskaites punkta dalījumi ir atzīmēti kā **Gatavs rēķinam**, galvenes statuss tiek atjaunināts no **Nav sākts** uz **Notiek izpilde**. Kad tiek izrakstīts rēķins par visu atskaites punktu sadalījumu, galvenes atskaites punkta statuss tiek atjaunināts uz **Pabeigts**.

Šajā skatā tiek rādīts atskaites punkts rēķina melnrakstā ar statusu **Izveidots klienta rēķins**. Kad tiek apstiprināts melnraksta rēķins, norēķinu statuss ierakstā tiek atjaunināts uz **Klienta rēķins iegrāmatots**. 

> [!NOTE] 
> Neatjauniniet šo statusa vērtību, izmantojot pielāgotu kodu. Project Operations nefunkcionē pareizi, ja šīs statusa vērtības tiek atjauninātas ar pielāgotu kodu.

## <a name="time-and-material-billing-backlog"></a>Laika un materiālu rēķinu izrakstīšanas rezerve

Skatā **Nepabeigtā rēķinu izrakstīšana par laiku un materiālu** tiek uzskaitīti visi nepārdoto preču pārdošanas ieņēmumi, kas iekļauti visos sistēmas projekta līgumos, kam nav izrakstīts rēķins. Šajā skatā vienu vai vairākus rēķinā neiekļautās pārdošanas faktiskos datus var atzīmēt kā **Gatavs rēķina izrakstīšanai** vai **Nav gatavs rēķina izrakstīšanai**. Atzīmējot rēķinā neiekļautas pārdošanas faktiskos datus kā **Gatavs rēķina izrakstīšanai**, to var ievietot rēķina melnrakstā.

Rēķinā neiekļautās pārdošanas ar ailes **Nepārsniegt** statusu **Neizdevās** nevar atzīmēt kā **Gatavs rēķina izrakstīšanai**. Ja faktiskie iestatījumi ir jāatzīmē kā **Gatavs rēķinam**, atiestatiet statusu uz citiem faktiskajiem līguma rindā, kas ir veikti, un pēc tam atkārtoti novērtējiet statusu **Nepārsniegt**.

Ja vairāku klientu līguma rindām ir laika un materiālu norēķinu metode, kad tiek apstiprināts laiks un izdevumi, katram klientam līguma rindā tiek izveidots viens neiekasēts pārdošanas apjoms atbilstoši katram klientam definētajai norēķinu procenta sadalījumam. Skatā **Nepabeigtā rēķinu izrakstīšana par laiku un materiālu** būs redzami šie atsevišķie klientam specifiskie neapstrādātie pārdošanas darījumi. Šajā skatā katru no šiem rēķinā neiekļautās pārdošanas faktisko datu ierakstiem var atsevišķi atzīmēt kā **Gatavs rēķina izrakstīšanai**.

Rēķinā neietverta pārdošanas faktiskā vērtība, kas ir rēķina melnrakstā, šajā skatā tiek rādīta ar norēķinu statusu **Izveidots klienta rēķins**. Kad ir apstiprināts rēķina melnraksts, šī ieraksta norēķinu statuss tiek atjaunināts uz **Iegrāmatots klienta rēķins**. 

> [!NOTE] 
> Neatjauniniet šo statusa vērtību, izmantojot pielāgotu kodu. Project Operations nefunkcionē pareizi, ja šīs statusa vērtības tiek atjauninātas ar pielāgotu kodu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
