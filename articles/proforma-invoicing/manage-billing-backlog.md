---
title: Rēķinu uzkrāšanās pārvaldība
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt skatīt uzkrātos rēķinus risinājumā Project Operations un strādāt ar tiem.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088011"
---
# <a name="manage-the-billing-backlog"></a>Rēķinu uzkrāšanās pārvaldība

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Risinājumā Dynamics 365 Project Operations ir divi īpaši skati, kas palīdz strādāt ar uzkrātajiem rēķiniem un tos pārvaldīt. Tie ir **Atskaites punkti ar fiksētu cenu** un **Uzkrātie rēķini par laiku un materiāliem** Lai atlasītu skatu, Project Operations apgabalā **Pārdošana** kreisajā navigācijas lapā atlasiet **Rēķini**. Šeit tiek glabātas uzkrāto rēķinu saites.

## <a name="fixed-price-milestones"></a>Fiksētu cenu atskaites punkti

Šajā skatā ir uzskaitīti visi atskaites punkti ar fiksētu cenu visās sistēmas projekta līguma rindās. Šajā skatā vienu vai vairākus atskaites punktus var atzīmēt kā **Gatavs rēķina izrakstīšanai** vai **Nav gatavs rēķina izrakstīšanai**. Kad esat atzīmējis atskaites punktu kā **Gatavs rēķina izrakstīšanai** , atskaites punkts kļūst pieejams rēķina melnrakstam.

Ja vairāku klientu līguma rindām ir fiksētas cenas norēķinu metode, katram klientam līguma rindā tiek izveidots viens atskaites punkts. Lietotājs izveido atskaites punktu, un šis atskaites punkts tiek sadalīts klientam = noteikti atskaites punkta ieraksti iekšēji, ņemot vērā katram klientam līguma rindā norādīto norēķinu procentuālo sadalījumu. Skatā **Atskaites punkti ar fiksētu cenu** tiek parādīti atsevišķi klientu atskaites punktu ieraksti. Šajā skatā katru no šiem atskaites punktu ierakstiem var atsevišķi atzīmēt kā **Gatavs rēķina izrakstīšanai**. Ja viens vai vairāki saistīto atskaites punktu sadalījumi ir atzīmēti kā **Gatavs rēķina izrakstīšanai** , galvene no statusa **Nav sākts** tiek pārvietota uz **Notiek izpilde**. Kad ir izrakstīts rēķins par atskaites punktu sadalījumu, galvenes atskaites punktu statuss ir **Pabeigts**.

Šajā skatā tiek rādīts atskaites punkts rēķina melnrakstā ar statusu **Izveidots klienta rēķins**. Kad ir apstiprināts rēķina melnraksts, šī ieraksta norēķinu statuss tiek atjaunināts uz **Iegrāmatots rēķins**. Nav ieteicams atjaunināt šī statusa vērtību, izmantojot pielāgotu kodu. Risinājums Project Operations nedarbosies pareizi, ja šīs statusa vērtības tiks atjauninātas ar pielāgotu kodu.

## <a name="time-and-material-billing-backlog"></a>Laika un materiālu rēķinu izrakstīšanas rezerve

Šajā skatā ir uzskaitīti visi rēķinos neiekļautās pārdošanas faktiskie dati, kas sistēmā nav iekļauti rēķinos visiem projekta līgumiem. Šajā skatā vienu vai vairākus rēķinā neiekļautās pārdošanas faktiskos datus var atzīmēt kā **Gatavs rēķina izrakstīšanai** vai **Nav gatavs rēķina izrakstīšanai**. Atzīmējot rēķinā neiekļautas pārdošanas faktiskos datus kā **Gatavs rēķina izrakstīšanai** , to var ievietot rēķina melnrakstā.

Rēķinā neiekļautas pārdošanas faktiskos datus, kam **Nepārsniegt** statuss ir **Neizdevās** , nevar atzīmēt kā **Gatavs rēķina izrakstīšanai**. Ja šie faktiskie dati ir jāatzīmē kā tādi, atiestatiet statusu līguma rindas izpildītajos faktiskajos datos un pēc tam novērtējiet statusu **Nepāŗsniegt**.

Ja ir vairāku klientu līguma rindas, kuram ir laika un materiālu norēķinu metode, apstiprinot laiku un izdevumus, katram klientam tiek izveidoti rēķinā neiekļautās pārdošanas faktiskie dati līguma rindā atbilstoši katram klientam līguma rindā norādītajam norēķinu procentuālajam sadalījumam. Skatā **Laika un materiālu uzkrātie rēķini** redzēsiet šos atsevišķo klientu rēķinos neiekļautās pārdošanas faktiskos datus. Šajā skatā katru no šiem rēķinā neiekļautās pārdošanas faktisko datu ierakstiem var atsevišķi atzīmēt kā **Gatavs rēķina izrakstīšanai**.

Šajā skatā tiek rādīti rēķinā neiekļautas pārdošanas faktiskie dati ar **norēķinu statusu** **Izveidots klienta rēķins**. Kad ir apstiprināts rēķina melnraksts, šī ieraksta norēķinu statuss tiek atjaunināts uz **Iegrāmatots klienta rēķins**. Nav ieteicams atjaunināt šī statusa vērtību, ja tas ir šādā statusā, izmantojot pielāgotu kodu. Risinājums Project Operations nedarbosies pareizi, ja šīs statusa vērtības tiks atjauninātas ar pielāgotu kodu.
