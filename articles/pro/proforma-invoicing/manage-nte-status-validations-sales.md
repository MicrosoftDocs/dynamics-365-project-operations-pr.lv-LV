---
title: Pārvaldīt nepārsniedzošu statusu un pārbaudes
description: Šajā rakstā ir sniegta informācija par risinājumā Project Operations veiktajām nepārsniedzamā ierobežojuma pārbaudēm.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d10a88305339a84b36d8606631ea9761806098a1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932765"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Pārvaldīt nepārsniedzošu statusu un pārbaudes 

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

## <a name="not-to-exceed-on-approvals"></a>Nepārsniedzamie ierobežojumi apstiprinājumos

Kad tiek iesniegts laiks, izmaksas vai materiālu lietojuma ieraksts, tiek izveidots apstiprinājuma ieraksts. Ja apstiprinājums ir iekasējams un kartēts uz laika un materiālu līguma rindu, sistēma pabeidz nepārsniegšanas validācijas pārbaudi šādos līmeņos:

  - Pārbauda, ņemot vērā šajā projekta līguma rindā iestatīto ierobežojumu klientam
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts līguma rindai
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts klientam
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts līgumam

Pārbaudes katrā līmenī paredz nodrošināt, ka pārdošanas vērtības summa šajā apstiprinājumā nepārkāps nepārsniedzamo ierobežojumu šajā līmenī pēc jau reģistrētās norēķinu summas un līdz šim rēķinā norādītās summas uzskaites šajā līmenī.

Ja pārbaude ir veiksmīga, apstiprinājumam tiek piešķirts validācijas statuss **Izdevās**.

Ja pārbaude ir neveiksmīga, apstiprinājumam tiek piešķirts validācijas statuss **Neizdevās**. Nepārsniedzamā līmeņa validācijas informācijā būs skaidrojums lietotājam par to, kurā līmenī validācija neizdevās.

Ja iesniegtais laiks, izdevumi vai materiālu lietojuma ieraksts tiek uzskatīts par neiekļaujamu rēķinā, nepārsniegšanas validācijas statuss tiek iestatīts uz **Nav piemērojams** un validācijas informācija ir **Nav piemērojams**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Nepārsniedzamās vērtības rēķinos neiekļautajos faktiskajos pārdošanas datos

Kad tiek apstiprināts laika, izmaksu vai materiālu lietojuma ieraksts, tiek izveidoti izmaksu un rēķinā neiekļauto faktisko pārdošanas datu ieraksti. Ja izveidotie rēķinos neiekļautie faktiskie pārdošanas dati ir iekasējams un kartēti uz laika un materiālu līguma rindu, lietojumprogramma veic nepārsniegšanas validācijas pārbaudi šādos līmeņos:

  - Pārbauda, ņemot vērā šajā projekta līguma rindā iestatīto ierobežojumu klientam
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts līguma rindai
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts klientam
  - Pārbauda, ņemot vērā ierobežojumu, kas noteikts līgumam

Pārbaudes katrā līmenī nodrošina, ka pārdošanas vērtības summa faktiskajos datos nepārkāps nepārsniedzamo ierobežojumu šajā līmenī pēc jau reģistrētās norēķinu summas un līdz šim rēķinā norādītās summas uzskaites šajā līmenī.

Ja pārbaude ir veiksmīga, rēķinā neiekļautajiem faktiskajiem pārdošanas datiem tiek piešķirts nepārsniegšanas statuss **Iesniegts**.

Ja pārbaude nav veiksmīga, rēķinā neiekļautajiem faktiskajiem pārdošanas datiem tiek piešķirts nepārsniegšanas statuss **Neizdevās**. Validācijas informācijā ir skaidrojums lietotājam par to, kurā līmenī validācija neizdevās.

Ja neiekasēts pārdošanas apjoms tiek uzskatīts par neiekļaujamu rēķinā vai bezmaksas, ja nevienā no četriem līmeņiem nav iestatīts nepārsniegšanas ierobežojums vai ja tiek izveidotas faktiskās Izmaksas, Honorārs, Resursu vienība vai Starporganizāciju pārdošana, laukiem **Nepārsniegšanas statuss** un **Nepārsniegšanas validācijas detalizētā informācija** jābūt iestatītiem uz **Nav piemērojams**.

## <a name="reset-the-not-to-exceed-status"></a>Nepārsniegšanas statusa atiestatīšana

Nepārsniegšanas ierobežojuma statusam var veikt lielapjoma atiestatīšanu. Projekta vadītāji var pielāgot nepārsniegšanas validāciju, lai noteiktu prioritāti rēķinu izrakstīšanai par vienu noteiktu darbu, laiku, izdevumiem vai materiālu izlietojumu, nevis par to, kas jau ir iesniegts no pieejamās nepārsniedzamās summas.

Pēc tam kad rēķinā neiekļauto faktisko pārdošanas datu nepārsniegšanas statuss ir atiestatīts, saistību summa tiek samazināta. Projekta vadītājs var atlasīt citu darba, laika, izdevumu vai materiālu izlietojuma ierakstu, kas iepriekš neizturēja nepārsniegšanas validāciju un atkārtotu izvērtēšanu. Samazinot piešķirto summu, šie faktiskie dati tagad iztur validāciju, kas palīdz projekta vadītājam vairāk ietekmēt un kontrolēt rēķinos iekļaujamās transakcijas šajā periodā.

Lai atiestatītu nepārsniegšanas statusu, atlasiet vienu vai vairākas faktiskās vērtības no skata **Laika un materiālu rēķinu izrakstīšanas rezerve** vai **Faktiskās vērtības** un pēc tam atlasiet opciju **Atiestatīt nepārsniegšanas statusu**.

Visām atbilstošajām atlasītajām faktiskajām vērtībām nepārsniegšanas statuss tiek atiestatīts uz **Nav novērtēts**. Faktiskās vērtības, kurām ir atiestatīts nepārsniedzamais statuss, ir rēķinos neiekļautie faktiskie pārdošanas dati, par kuriem vēl nav izrakstīti rēķini, kas nav rēķina projektā un ir atzīmēti kā iekasējami. Citas atlasītās faktiskās vērtības tiek ignorētas.

## <a name="reevaluate-not-to-exceed-status"></a>Nepārsniegšanas statusa pārvērtēšana

Nepārsniegšanas ierobežojuma statusam var veikt lielapjoma pārvērtēšanu. Nepārsniegšanas statusa pārvērtēšana ir lietderīga, ja:

  - Bija atkārtotas sarunas par nepārsniedzamajiem ierobežojumiem ar klientu, un faktiskās vērtības būs jāpārvērtē.
  - Projekta vadītājs vēlas precīzi noteikt rēķinu par rēķinos neiekļautajām pārdošanas neizpildītajām darbībām, nosakot viena darba kopuma prioritāti pār citu.

Lai pārvērtētu nepārsniegšanas statusu, atlasiet vienu vai vairākas faktiskās vērtības no skata **Laika un materiālu rēķinu izrakstīšanas rezerve** vai **Faktiskās vērtības** un pēc tam atlasiet opciju **Nepārsniegšanas statusa pārvērtēšana**.

Visas attiecīgās atlasītās faktiskās vērtības, kurām ir nepārsniegšanas limits, tiks vērtētas attiecībā pret nepārsniedzamā limita iestatījumu. Faktiskās vērtības, kuras ir atbilstošas atkārtotai nepārsniedzamā statusa pārvērtēšanai, ir rēķinos neiekļautie faktiskie pārdošanas dati, par kuriem nav izrakstīti rēķini, kas nav rēķina projektā un ir atzīmēti kā iekasējami. Visi citi pēc izvēles atlasītie faktiskie dati.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
