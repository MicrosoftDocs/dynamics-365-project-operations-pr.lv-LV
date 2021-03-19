---
title: Pārvaldīt nepārsniedzošu statusu un pārbaudes
description: Šajā tēmā ir sniegta informācija par risinājumā Project Operations veiktajām nepārsniedzamā ierobežojuma pārbaudēm.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c491d4014ffc2568d7df72b542761ec9b1a90b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274035"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Pārvaldīt nepārsniedzošu statusu un pārbaudes 

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

## <a name="not-to-exceed-on-approvals"></a>Nepārsniedzamie ierobežojumi apstiprinājumos

Kad tiek iesniegts laika vai izdevumu ieraksts, tiek izveidots apstiprinājuma ieraksts. Ja apstiprinājums ir iekasējams un kartēts uz laika un materiālu līguma rindu, sistēma pabeidz nepārsniegšanas validācijas pārbaudi šādos līmeņos:

  - Pārbauda, ņemot vērā šajā projekta līguma rindā iestatīto ierobežojumu klientam
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts līguma rindai
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts klientam
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts līgumam

Pārbaudes katrā līmenī paredz nodrošināt, ka pārdošanas vērtības summa šajā apstiprinājumā nepārkāps nepārsniedzamo ierobežojumu šajā līmenī pēc jau reģistrētās norēķinu summas un līdz šim rēķinā norādītās summas uzskaites šajā līmenī.

Ja pārbaude ir veiksmīga, apstiprinājumam tiek piešķirts validācijas statuss **Izdevās**.

Ja pārbaude ir neveiksmīga, apstiprinājumam tiek piešķirts validācijas statuss **Neizdevās**. Nepārsniedzamā līmeņa validācijas informācijā būs skaidrojums lietotājam par to, kurā līmenī validācija neizdevās.

Kad iesniegtais laiks vai izdevumu ieraksts tiek uzskatīts par neiekļaujamu rēķinā, nepārsniedzamās vērtības validācijas statuss ir iestatīts kā **Nav piemērojams** un validācijas informācijas laukā ir rakstīts **Nav piemērojams**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Nepārsniedzamās vērtības rēķinos neiekļautajos faktiskajos pārdošanas datos

Kad ir apstiprināts laiks vai izdevumu ieraksts, tiek izveidotas izmaksu un rēķinā neiekļauto faktisko pārdošanas datu ieraksti. Ja izveidotie rēķinos neiekļautie faktiskie pārdošanas dati ir iekasējams un kartēti uz laika un materiālu līguma rindu, lietojumprogramma veic nepārsniegšanas validācijas pārbaudi šādos līmeņos:

  - Pārbauda, ņemot vērā šajā projekta līguma rindā iestatīto ierobežojumu klientam
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts līguma rindai
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts klientam
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts līgumam

Pārbaudes katrā līmenī nodrošina, ka pārdošanas vērtības summa faktiskajos datos nepārkāps nepārsniedzamo ierobežojumu šajā līmenī pēc jau reģistrētās norēķinu summas un līdz šim rēķinā norādītās summas uzskaites šajā līmenī.

Ja pārbaude ir veiksmīga, rēķinā neiekļautajiem faktiskajiem pārdošanas datiem tiek piešķirts nepārsniegšanas statuss **Iesniegts**.

Ja pārbaude nav veiksmīga, rēķinā neiekļautajiem faktiskajiem pārdošanas datiem tiek piešķirts nepārsniegšanas statuss **Neizdevās**. Validācijas informācijā ir skaidrojums lietotājam par to, kurā līmenī validācija neizdevās.

Ja neiekasēts pārdošanas apjoms tiek uzskatīts par neiekļaujamu rēķinā vai bezmaksas, ja nevienā no četriem līmeņiem nav iestatīts nepārsniegšanas ierobežojums vai ja tiek izveidotas faktiskās Izmaksas, Honorārs, Resursu vienība vai Starporganizāciju pārdošana, laukiem **Nepārsniegšanas statuss** un **Nepārsniegšanas validācijas detalizētā informācija** jābūt iestatītiem uz **Nav piemērojams**.

## <a name="reset-the-not-to-exceed-status"></a>Nepārsniegšanas statusa atiestatīšana

Nepārsniegšanas ierobežojuma statusam var veikt lielapjoma atiestatīšanu. Šādi projekta vadītāji var pielāgot nepārsniegšanas ierobežojuma validāciju, lai par prioritāti izvirzītu rēķinu izrakstīšanu par vienu konkrētu darbu, laiku vai izdevumiem, salīdzinot ar citiem, kuri jau ir iesniegti no pieejamās nepārsniedzamās summas.

Pēc tam kad rēķinā neiekļauto faktisko pārdošanas datu nepārsniegšanas statuss ir atiestatīts, saistību summa tiek samazināta. Projekta vadītājs var izvēlēties citu darba, laika vai izdevumu kopumu, kas iepriekš nav ticis veiksmīgi validēts attiecībā pret nepārsniedzamo vērtību, un tos pārvērtēt. Līdz ar iesniegtās summas samazināšanu šie faktiskie apjomi varēs tikt veiksmīgi validēti. Tas palīdz projekta vadītājam saņemt lielāku ietekmi un kontroli pār rēķinā iekļautajām transakcijām šajā periodā.

Lai atiestatītu nepārsniegšanas statusu, atlasiet vienu vai vairākas faktiskās vērtības no skata **Laika un materiālu rēķinu izrakstīšanas rezerve** vai **Faktiskās vērtības** un pēc tam atlasiet opciju **Atiestatīt nepārsniegšanas statusu**.

Visām atbilstošajām atlasītajām faktiskajām vērtībām nepārsniegšanas statuss tiek atiestatīts uz **Nav novērtēts**. Faktiskās vērtības, kurām ir atiestatīts nepārsniedzamais statuss, ir rēķinos neiekļautie faktiskie pārdošanas dati, par kuriem vēl nav izrakstīti rēķini, kas nav rēķina projektā un ir atzīmēti kā iekasējami. Citas atlasītās faktiskās vērtības tiek ignorētas.

## <a name="reevaluate-not-to-exceed-status"></a>Nepārsniegšanas statusa pārvērtēšana

Nepārsniegšanas ierobežojuma statusam var veikt lielapjoma pārvērtēšanu. Nepārsniegšanas statusa pārvērtēšana ir lietderīga, ja:

  - Bija atkārtotas sarunas par nepārsniedzamajiem ierobežojumiem ar klientu, un faktiskās vērtības būs jāpārvērtē.
  - Projekta vadītājs vēlas precīzi noteikt rēķinu par rēķinos neiekļautajām pārdošanas neizpildītajām darbībām, nosakot viena darba kopuma prioritāti pār citu.

Lai pārvērtētu nepārsniegšanas statusu, atlasiet vienu vai vairākas faktiskās vērtības no skata **Laika un materiālu rēķinu izrakstīšanas rezerve** vai **Faktiskās vērtības** un pēc tam atlasiet opciju **Nepārsniegšanas statusa pārvērtēšana**.

Visas attiecīgās atlasītās faktiskās vērtības, kurām ir nepārsniegšanas limits, tiks vērtētas attiecībā pret nepārsniedzamā limita iestatījumu. Faktiskās vērtības, kuras ir atbilstošas atkārtotai nepārsniedzamā statusa pārvērtēšanai, ir rēķinos neiekļautie faktiskie pārdošanas dati, par kuriem nav izrakstīti rēķini, kas nav rēķina projektā un ir atzīmēti kā iekasējami. Visi citi pēc izvēles atlasītie faktiskie dati.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]