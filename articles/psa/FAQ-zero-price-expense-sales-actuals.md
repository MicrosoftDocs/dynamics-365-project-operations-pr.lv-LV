---
title: Kāpēc cena pēc noklusējuma ir nulle par faktiskajām pārdošanas izmaksām?
description: Trīs tālāk norādītās pārbaudes darbības palīdzēs novērst problēmu, kāpēc faktisko pārdošanas izdevumu cena pēc noklusējuma tiek iestatīta uz 0.
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
ms.openlocfilehash: 8c2270b07b6f8765a6ec1f506fe1767a1841950b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122082"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Kāpēc cena pēc noklusējuma ir nulle par faktiskajām pārdošanas izmaksām?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Šis bieži uzdoto jautājumu raksts attiecas uz faktiskajiem izdevumiem, ja transakcijas klasei ir iestatīts vienums Izdevumi un transakcijas tipam ir iestatīta vērtība Rēķinā neiekļautā pārdošana. Trīs tālāk norādītās pārbaudes darbības palīdzēs novērst problēmu, kāpēc faktisko pārdošanas izdevumu cena (rēķina likme) pēc noklusējuma tiek iestatīta uz 0.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>1. pārbaude: nosakiet projekta pārdošanas cenrādi

Atrodiet projektu, izmantojot faktisko izdevumu projekta lauku, un pārejiet uz projekta lapu. Pēc tam pārejiet uz cilni Pārdošana. Režģī Projekta līguma rindas noklikšķiniet uz saites laukā Projekta līgums. Tiks atvērta lapa Projekta līgums. Lapā Projekta līgums pārejiet uz cilni Projekta cenrāži. Pārbaudiet, vai šeit ir pievienots vismaz viens cenrādis.

Ja projekta līguma režģī Projekta cenrāži nav pievienots cenrādis, veiciet šādas darbības:

- Pievienojiet cenrādi režģī Projekta cenrāži. Cenrāžiem, kurus šeit atļauts pievienot, konteksta laukā jābūt iestatītam vienumam Pārdošana, un cenrāža valūtas laukam jāatbilst projekta līguma valūtas laukam. Kad esat veicis nepieciešamos labojumus, vēlreiz izveidojiet izdevumu ierakstu, apstipriniet to un pārbaudiet, vai rēķinā neiekļauto pārdošanu faktiskā summa ir derīga cena.
- Ja projekta līguma režģī Projekta cenrāži ir pievienots viens vai vairāki cenrāži, pārejiet pie 2. pārbaudes.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>2. pārbaude: vai iepriekš minētie cenrāži ir derīgi faktisko izdevumu konkrētajam datumam?

Lai programmā Project Service cenrādis tiktu ņemts vērā noklusējuma cenas iestatīšanai, šim cenrādim ir jāatbilst faktisko pārdošanas izdevumu datumam. Pārbaudiet šādus aspektus, lai pārliecinātos, vai iepriekš noteiktie cenrāži ir atbilstoši:

- Vispirms pārbaudiet, vai pievienotajiem cenrāžiem ir aizpildīts sākuma un beigu datums cilnē Vispārīgi. Ja iepriekš noteikto cenrāžu sākuma un beigu datums nav norādīts, esat atradis problēmu. 
- Pierakstiet faktisko pārdošanas izdevumu sākuma datumu un pārbaudiet, vai kāds no cenrāžiem atbilst šim datumam. Piemēram, datumam faktiskajos izdevumos ir jāietilpst cenrāža sākuma vai beigu datumā. 
    - Ja nav cenrāža, kas atbilst faktisko pārdošanas izdevumu datumam, esat atradis problēmu. Mainiet cenrāža sākuma un beigu datumus, lai nodrošinātu, ka cenrādī ir ietverts faktisko izdevumu datums. 
    - Ja faktisko pārdošanas izdevumu datumam atbilst vairāk nekā viens cenrādis, esat atradis problēmu. To varat labot, rediģējot cenrāžu sākuma un beigu datumus, lai būtu tikai viens cenrādis, kas atbilst faktisko izdevumu datumam. 
    - Ja ir tikai viens cenrādis, kas atbilst faktisko izdevumu datumam, pārejiet pie 3. pārbaudes.
Kad esat veicis nepieciešamos labojumus, vēlreiz izveidojiet izdevumu ierakstu, apstipriniet to un pārbaudiet, vai rēķinā neiekļauto pārdošanu faktiskā summa ir derīga cena.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>3. pārbaude: vai atbilstošajā projekta cenrādī ir derīga izdevumu kategorijas cena? 

Ja esat veiksmīgi izpildījis 1. un 2. pārbaudi, jums ir jābūt tikai vienam projekta cenrādim, kas atbilst faktisko pārdošanas izdevumu datumam. Atveriet šo projekta cenrādi un pārejiet uz cilni Kategoriju cenas. Pārliecinieties, ka faktisko izdevumu konkrētajai izdevumu kategorijai režģī ir rinda.
 
- Ja rindas nav, esat atradis problēmu. Izveidojiet rindu režģī Kategorijas cena jūsu faktisko izdevumu kategorijai. Kad tas ir paveikts, vēlreiz izveidojiet izdevumu ierakstu, apstipriniet to un pārbaudiet, vai faktiskajai rēķinā neiekļautajai pārdošanai ir derīga cena. 
- Ja kategoriju cenu režģī ir izdevumu kategorijas rinda, pārbaudiet, vai tajā ir derīga cena.

Lai saprastu, kāda ir derīga cena, izmantojiet šīs metodes:

- Ja rindas Kategorijas cena laukā Cenas noteikšanas metode ir atlasīts iestatījums Pašizmaksa, faktisko pārdošanas izdevumu vienības likme pēc noklusējuma būs izdevumu ieraksta vērtība.
- Ja rindas Kategorijas cena laukā Cenas noteikšanas metode ir atlasīts iestatījums Uzcenojuma procenti, pārbaudiet, vai laukā Procenti ir iestatīta derīga vērtība. Faktisko pārdošanas izdevumu vienības likmei tiek norādīta noklusējuma vērtība, piemērojot šos uzcenojuma procentus cenai izdevumu ierakstā.
- Ja rindas Kategorijas cena laukā Cenas noteikšanas metode ir atlasīts iestatījums Vienības cena, pārbaudiet, vai laukā Cena ir iestatīta derīga vērtība. Faktisko pārdošanas izdevumu vienības likmei tiek norādīta noklusējuma vērtība atbilstoši valūtas summai, kas norādīta laukā Cena.

Ja izdevumu kategorijas cenas iestatījums nav derīgs, esat atradis problēmu. Risinājums ir rediģēt kategorijas cenu rindu, izmantojot derīgu izdevumu kategorijas cenu saskaņā ar iepriekš paredzētajiem noteikumiem. Kad tas ir paveikts, vēlreiz izveidojiet izdevumu ierakstu, apstipriniet to un pēc tam pārbaudiet, vai faktiskajai rēķinā neiekļautajai pārdošanai ir derīga cena.

Ja pēc trīs iepriekš minēto pārbaužu veikšanas joprojām neredzat derīgu cenu faktiskajiem pārdošanas izdevumiem, lūdzu, reģistrējiet atbalsta biļeti.


