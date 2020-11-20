---
title: Kāpēc cena pēc noklusējuma ir nulle par faktiskajām pārdošanas laika izmaksām?
description: Novērsiet problēmu, kāpēc cena par faktiskajām pārdošanas laika izmaksām tiek pēc noklusējuma iestatīta uz 0.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5106e8c1a059bbb0efbeb73dc63e03e8bc9e4b7b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125952"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Kāpēc cena pēc noklusējuma ir nulle par faktiskajām pārdošanas laika izmaksām?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Šis bieži uzdoto jautājumu raksts attiecas uz faktiskajām vērtībām, ja transakcijas klase ir iestatīta uz Laiks un transakcijas tips ir iestatīts uz Rēķinā neiekļautā pārdošana. Trīs tālāk norādītās pārbaudes darbības palīdzēs novērst problēmu, kāpēc faktisko pārdošanas laika izmaksu cena (rēķina likme) pēc noklusējuma tiek iestatīta uz 0.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>1. pārbaude: nosakiet projekta pārdošanas cenrādi

Atrodiet projektu, izmantojot faktisko izdevumu projekta lauku, un pārejiet uz projekta lapu. Pēc tam režģī Projekta līguma rindas pārejiet uz cilni Pārdošana un noklikšķiniet uz saites laukā Projekta līgums. Tiks atvērta lapa projekta līgums. Lapā Projekta līgums pārejiet uz cilni Projekta cenrāži. Pārbaudiet, vai šeit ir pievienots vismaz viens cenrādis. Ja projekta līguma režģī projekta cenrādis nav pievienots cenrādis, esat atradis problēmu. Pievienojiet cenrādi režģī Projekta cenrāži. Cenrāžiem, kurus šeit atļauts pievienot, konteksta laukā jābūt iestatītam vienumam Pārdošana, un cenrāža valūtas laukam jāatbilst projekta līguma valūtas laukam. Kad esat veicis nepieciešamos labojumus, izveidojiet laika ierakstu, apstipriniet to un pārbaudiet, vai rēķinā neiekļauto pārdošanu faktiskā summa ir derīga cena. 

Ja projekta līguma režģī Projekta cenrāži ir pievienots viens vai vairāki cenrāži, pārejiet pie nākamās pārbaudes, kas norādīta šajā dokumentā.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>2. pārbaude: vai iepriekš minētie cenrāži ir derīgi faktisko pārdošanas laika izmaksu konkrētajam datumam?

Lai programmā Project Service cenrādis tiktu ņemts vērā noklusējuma cenas iestatīšanai, šim cenrādim ir jāatbilst faktisko pārdošanas laika izmaksu datumam. Pārbaudiet šādus aspektus, lai pārliecinātos, vai iepriekš noteiktie cenrāži ir atbilstoši:
- Pārbaudiet, vai pievienotajiem cenrāžiem ir aizpildīts sākuma un beigu datums cilnē Vispārīgi. Ja iepriekš noteikto cenrāžu sākuma un beigu datums nav norādīts, esat atradis problēmu. 
- Pierakstiet faktisko pārdošanas laika izmaksu sākuma datumu un pārbaudiet, vai kāds no cenrāžiem atbilst šim datumam. Piemēram, datumam faktiskajās pārdošanas laika izmaksās ir jāietilpst cenrāža sākuma vai beigu datumā. 
    - Ja nav cenrāža, kas atbilst faktisko pārdošanas laika izmaksu datumam, esat atradis problēmu. Mainiet cenrāža sākuma un beigu datumus, lai nodrošinātu, ka cenrādī ir ietverts faktisko pārdošanas laika izmaksu datums. 
    - Ja faktisko pārdošanas laika izmaksu datumam atbilst vairāk nekā viens cenrādis, esat atradis problēmu. To varat labot, rediģējot cenrāžu sākuma un beigu datumus, lai būtu tikai viens cenrādis, kas atbilst faktisko pārdošanas laika izmaksu datumam. 
    - Ja ir tikai viens cenrādis, kas atbilst faktisko pārdošanas laika izmaksu datumam, pārejiet pie 3. pārbaudes.
Kad esat veicis nepieciešamos labojumus, izveidojiet laika ierakstu, apstipriniet to un pārbaudiet, vai faktiskajām pārdošanas laika izmaksām ir derīga cena.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>3. pārbaude: vai cenrādī ir cena faktisko pārdošanas laika izmaksu izcenojuma dimensijām?

Ja esat veiksmīgi izpildījis 1. un 2. pārbaudi, jums ir jābūt tikai vienam cenrādim, kas atbilst faktisko pārdošanas laika izmaksu datumam. Atveriet cenrādi un pārejiet uz cilni Lomu cenas. Pārliecinieties, ka faktisko pārdošanas laika izmaksu cenu dimensijām režģī ir rinda.

Ja faktisko pārdošanas laika izmaksu cenas dimensijām režģī nav rindas, esat atradis problēmu. Lomu cenu režģī izveidojiet rindu faktisko pārdošanas laika izmaksu cenas dimensijām. Kad tas ir paveikts, izveidojiet laika ierakstu, apstipriniet to un pārbaudiet, vai faktiskajām pārdošanas laika izmaksām ir derīga cena.

Ja pēc trīs iepriekš minēto pārbaužu veikšanas joprojām neredzat derīgu cenu faktiskajām pārdošanas laika izmaksām, lūdzu, reģistrējiet atbalsta biļeti. 

