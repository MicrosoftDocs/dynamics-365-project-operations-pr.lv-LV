---
title: Kāpēc cena pēc noklusējuma ir nulle par faktiskajām laika izmaksām?
description: Novērsiet problēmu, kāpēc cena par faktiskajām laika izmaksām tiek pēc noklusējuma iestatīta uz 0.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 44d4952b77ac0a541cdf8e3e55f202c9209efdf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080463"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Kāpēc cena pēc noklusējuma ir nulle par faktiskajām laika izmaksām?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Šis bieži uzdoto jautājumu raksts attiecas uz faktiskajām vērtībām, ja transakcijas klasei ir iestatīts vienums Laiks un transakcijas tipam ir atlasīts iestatījums Izmaksas. Trīs tālāk norādītās pārbaudes darbības palīdzēs novērst problēmu, kāpēc faktisko izmaksu cena pēc noklusējuma tiek iestatīta uz 0.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>1. pārbaude: nosakiet projekta izmaksu cenrādi

Atrodiet projektu, izmantojot faktisko izdevumu projekta lauku, un pēc tam pārejiet uz projekta lapu. Noklikšķiniet uz līgumslēdzēja vienības saiti laukā. Lapā Līgumslēdzēja vienība pārbaudiet, vai līgumslēdzējai vienībai ir cenrādis režģī Izmaksu cenrāži.

Ja ir vairāk nekā viens cenrādis, esat atradis problēmu. Project Service atbalsta tikai vienu cenrādi katrai organizācijas vienībai. Noņemiet visus cenrāžus šai entītijai, līdz organizācijas vienības režģī Cenrāžu saraksti ir pievienots tikai viens cenrādis.

Ja organizācijas vienībai nav pievienots neviens cenrādis, pierakstiet organizācijas vienības valūtu. Atveriet pakalpojumu Project Service un pēc tam sadaļu Parametri un atveriet cilni Cenrāži. Pārbaudiet, vai pastāv cenrāži, kuru kontekstam ir iestatīta vērtība Izmaksas un kuru valūta atbilst organizācijas vienības valūtai.
 
Ja nav cenrāžu, kuri atbilst šiem kritērijiem, esat atradis problēmu. Pārliecinieties, ka ir vismaz viens cenrādis, kura kontekstam ir iestatīta vērtība Izmaksas un kura valūta atbilst organizācijas vienības valūtai.

Ja ir vairāk nekā viens cenrādis, kas atbilst šādiem kritērijiem, turpiniet lasīt šo dokumentu, lai veiktu citas pārbaudes.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>2. pārbaude: vai iepriekš minētie cenrāži ir derīgi faktisko laika izmaksu konkrētajam datumam?

Lai programmā Project Service cenrādis tiktu ņemts vērā noklusējuma cenas iestatīšanai, šim cenrādim ir jāatbilst faktisko laika izmaksu datumam. Pārbaudiet šādus aspektus, lai pārliecinātos, vai iepriekš noteiktie cenrāži ir atbilstoši:

- Pārbaudiet, vai pievienotajiem cenrāžiem ir aizpildīts sākuma un beigu datums cilnē Vispārīgi. Ja iepriekš noteikto cenrāžu sākuma un beigu datums nav norādīts, esat atradis problēmu. 
- Pierakstiet faktisko laika izmaksu sākuma datumu un pārbaudiet, vai kāds no cenrāžiem atbilst šim datumam. Piemēram, datumam faktiskajās laika izmaksās ir jāietilpst cenrāža sākuma vai beigu datumā. 
    - Ja nav cenrāža, kas atbilst faktisko laika izmaksu datumam, esat atradis problēmu. Mainiet cenrāža sākuma un beigu datumus, lai nodrošinātu, ka cenrādī ir ietverts faktisko laika izmaksu datums. 
    - Ja faktisko laika izmaksu datumam atbilst vairāk nekā viens cenrādis, esat atradis problēmu. To varat labot, rediģējot cenrāžu sākuma un beigu datumus, lai būtu tikai viens cenrādis, kas atbilst faktisko laika izmaksu datumam. 
    - Ja ir tikai viens cenrādis, kas attiecas uz šo faktisko laika izmaksu datumu, pārejiet pie nākamās dokumentā aprakstītās pārbaudes.
Kad esat veicis nepieciešamos labojumus, vēlreiz izveidojiet laika ierakstu, apstipriniet to un pārbaudiet, vai faktiskajām laika izmaksām ir derīga cena.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>3. pārbaude: vai cenrādī ir cena faktisko laika izmaksu izcenojuma dimensijām?

Ja esat veiksmīgi izpildījis 1. un 2. pārbaudi, jums ir jābūt tikai vienam cenrādim, kas atbilst faktisko laika izmaksu datumam. Atveriet cenrādi un pārejiet uz cilni Lomu cenas. Pārliecinieties, ka faktisko laika izmaksu cenu dimensijām režģī ir rinda.

Ja faktisko laika izmaksu cenas dimensijām režģī nav rindas, esat atradis problēmu. Lomu cenu režģī izveidojiet rindu faktisko laika izmaksu cenas dimensijām. Kad tas ir paveikts, vēlreiz izveidojiet laika ierakstu, apstipriniet to un pārbaudiet, vai faktiskajām laika izmaksām ir derīga cena.
 
Ja pēc trīs iepriekš minēto pārbaužu veikšanas joprojām neredzat derīgu cenu faktiskajām laika izmaksām, lūdzu, reģistrējiet atbalsta biļeti.



