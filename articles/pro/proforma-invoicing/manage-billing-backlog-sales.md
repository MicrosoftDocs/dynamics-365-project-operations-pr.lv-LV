---
title: Izrakstīšanas rezervju pārvaldība — Lite
description: Šajā tēmā ir sniegta informācija par dažādajiem skatiem, kas pieejami, lai pārvaldītu norēķinu neizpildīto darbību žurnālu.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e3ca167fa53a6923727eff3e7c34c8706dc7455
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176980"
---
# <a name="manage-the-billing-backlog---lite"></a>Izrakstīšanas rezervju pārvaldība — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Līdzeklī Dynamics 365 Project Operations ir īpaši skati, kas palīdz pārvaldīt norēķinu neizpildīto darbību žurnālu. Lai pārvaldītu norēķinu neizpildīto darbību žurnālu, atlasiet saites apgabalā **Pārdošana**, kas atrodas sadaļā **Norēķini**. 

Ir pieejami šādi skatu režīmi:

- Honorāri un avansi
- Pieejamie honorāri un avansi
- Fiksētu cenu atskaites punkti
- Preču rēķinu izrakstīšanas rezerve
- Laika un materiālu rēķinu izrakstīšanas rezerve

## <a name="retainers-and-advances"></a>Honorāri un avansi

Skatā **Honorāri un avansi** ir uzskaitīti visi honorāri un avansa maksājumi visos sistēmas projekta līgumos. Pēc tam kad honorārs vai avanss ir izrakstīts rēķinā, avansa summa kļūst pieejama izmantošanai.

## <a name="available-retainers-and-advances"></a>Pieejamie honorāri un avansi

Skatā **Pieejamie honorāri un avansi** ir uzskaitīti visi pieejamie honorāri un avansa maksājumi visos sistēmas projekta līgumos. Pēc tam kad honorārs vai avanss ir izrakstīts rēķinā, avansa summa kļūst pieejama izmantošanai un tiek pievienots sarakstam. Pēc tam kad ir pilnībā izmantots viss honorāra vai avansa apmērs, tas tiek noņemts no saraksta.

## <a name="fixed-price-milestones"></a>Fiksētu cenu atskaites punkti

Skatā **Fiksētu cenu atskaites punkti** ir uzskaitīti visi fiksētu cenu atskaites punkti visās sistēmas projekta līguma rindās. Šajā skatā vienu vai vairākus atskaites punktus var atzīmēt kā **Gatavs rēķina izrakstīšanai** vai **Nav gatavs rēķina izrakstīšanai**. Ja atskaites punkts tiek atzīmēts kā **Gatavs rēķina izrakstīšanai**, tas kļūst pieejams ievietošanai rēķina melnrakstā.

Ja vairāku klientu līguma rindām ir fiksētas cenas rēķina izrakstīšanas metode, katram klientam līguma rindā tiek izveidots atskaites punkts. Atskaites punktu var izveidot un pēc tam sadalīt atsevišķiem konkrētu klientu atskaites punktu ierakstiem. Šī sadalīšana ir iekšēja un atbilst rēķina procentu sadalījumam, kas katram klientam noteikts līguma rindā. Skatā **Fiksētu cenu atskaites punkti** tiks parādīti atsevišķi klientam specifiski atskaites punktu ieraksti. Šajā skatā katru no šiem atskaites punktu ierakstiem var atsevišķi atzīmēt kā **Gatavs rēķina izrakstīšanai**. Ja viens vai vairāki saistītās atskaites punktu dalījumi ir atzīmēti kā **Gatavs rēķina izrakstīšanai**, galvenes statuss tiek atjaunināts no **Nav sākts** uz **Notiek**. Kad visiem atskaites punktu dalījumiem ir izrakstīts rēķins, galvenes atskaites punkta statuss tiek atjaunināts uz **Pabeigts**.

Šajā skatā tiek rādīts atskaites punkts rēķina melnrakstā ar statusu **Izveidots klienta rēķins**. Kad tiek apstiprināts melnraksta rēķins, norēķinu statuss ierakstā tiek atjaunināts uz **Klienta rēķins iegrāmatots**. Neatjauniniet šo statusa vērtību, izmantojot pielāgotu kodu. Project Operations nefunkcionē pareizi, ja šīs statusa vērtības tiek atjauninātas ar pielāgotu kodu.

## <a name="product-billing-backlog"></a>Preču rēķinu izrakstīšanas rezerve

Skatā **Nepabeigtā rēķinu izrakstīšana par produktiem** ir uzskaitītas visas sistēmā izveidotās līguma rindas visos projekta līgumos. Šajā skatā vienu vai vairākas produkta līguma rindas var atzīmēt kā **Gatavs rēķina izrakstīšanai** vai **Nav gatavs rēķina izrakstīšanai**. Ja produkta līguma rinda tiek atzīmēta kā **Gatavs rēķina izrakstīšanai**, tā kļūst pieejama ievietošanai rēķina melnrakstā.

Šajā skatā tiek parādīta rēķinam atbilstošā produkta līguma rinda no rēķina melnraksta ar norēķinu statusu **Klienta rēķins izveidots**. Kad ir apstiprināts rēķina melnraksts, šī ieraksta norēķinu statuss tiek atjaunināts uz **Iegrāmatots klienta rēķins**. Neatjauniniet šo statusa vērtību, izmantojot pielāgotu kodu. Project Operations nefunkcionē pareizi, ja šīs statusa vērtības tiek atjauninātas ar pielāgotu kodu.

## <a name="time-and-material-billing-backlog"></a>Laika un materiālu rēķinu izrakstīšanas rezerve

Skatā **Nepabeigtā rēķinu izrakstīšana par laiku un materiālu** tiek uzskaitīti visi nepārdoto preču pārdošanas ieņēmumi, kas iekļauti visos sistēmas projekta līgumos, kam nav izrakstīts rēķins. Šajā skatā vienu vai vairākus rēķinā neiekļautās pārdošanas faktiskos datus var atzīmēt kā **Gatavs rēķina izrakstīšanai** vai **Nav gatavs rēķina izrakstīšanai**. Atzīmējot rēķinā neiekļautas pārdošanas faktiskos datus kā **Gatavs rēķina izrakstīšanai**, to var ievietot rēķina melnrakstā.

Rēķinā neiekļautās pārdošanas ar ailes **Nepārsniegt** statusu **Neizdevās** nevar atzīmēt kā **Gatavs rēķina izrakstīšanai**. Ja faktiskie dati ir jāatzīmē kā **Gatavs rēķina izrakstīšanai**, atiestatiet statusu attiecībā uz citiem faktiskajiem datiem līguma rindā, kas ir iestatīta. un pēc tam atkārtoti novērtējiet statusu **Nepārsniegt**.

Ja vairāku klientu līguma rindām ir laika un materiālu norēķinu metode, kad tiek apstiprināts laiks un izdevumi, katram klientam līguma rindā tiek izveidots viens neiekasēts pārdošanas apjoms atbilstoši katram klientam definētajai norēķinu procenta sadalījumam. Skatā **Nepabeigtā rēķinu izrakstīšana par laiku un materiālu** būs redzami šie atsevišķie klientam specifiskie neapstrādātie pārdošanas darījumi. Šajā skatā katru no šiem rēķinā neiekļautās pārdošanas faktisko datu ierakstiem var atsevišķi atzīmēt kā **Gatavs rēķina izrakstīšanai**.

Šajā skatā tiek parādīts rēķinā neiekļautais faktiskais pārdošanas apjoms no rēķina melnraksta ar norēķinu statusu **Klienta rēķins izveidots**. Kad ir apstiprināts rēķina melnraksts, šī ieraksta norēķinu statuss tiek atjaunināts uz **Iegrāmatots klienta rēķins**. Neatjauniniet šo statusa vērtību, izmantojot pielāgotu kodu. Project Operations nefunkcionē pareizi, ja šīs statusa vērtības tiek atjauninātas ar pielāgotu kodu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]