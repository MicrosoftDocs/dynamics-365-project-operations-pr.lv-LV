---
title: Izveidojiet cenrādi
description: Cenrāža izveide programmā Project Service
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8bbb73405ed29957810c559a235e5ac07a63baa3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589941"
---
# <a name="create-a-price-list-project-service"></a>Cenrāža izveide (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Cenrāži nodrošina veidni, kuru uzņēmumu pārvaldnieki var izmantot, lai izveidotu piedāvājumus un projektus un noteiktu projekta izmaksas. Tie nodrošina lomu un izdevumu rindas elementu sarakstu un jūsu pieprasīto cenu. Varat izveidot vairākus cenrāžus, lai uzturētu atsevišķas cenu struktūras dažādiem reģioniem, kuros pārdodat produktus, vai dažādiem pārdošanas kanāliem. Ieteicams izveidot vismaz vienu cenrādi katrai valūtai, kuru paredzēts izmantot rēķinu izrakstīšanai klientiem.  
  
Lai izveidotu tāmi veicamajam darbam, pārliecinieties, ka katram projektam ir dublēšanas izmaksu un pārdošanas cenu saraksts. Izveidojiet noklusējuma izmaksu un pārdošanas cenrādi, kas attiecas uz visiem projektiem, kuri izveidoti jūsu organizācijā.  
  
Cenrāži balstās uz lomām un izdevumu kategorijām, tāpēc, pirms veidojat cenrādi, pārliecinieties, ka jau esat konfigurējis lomas un izdevumu kategorijas, ko vēlaties izmantot, veidojot cenrādi.  
  
1.  Dodieties uz **Project Service > Cenrāži**.  
  
2.  Noklikšķiniet uz **Jauns**.  
  
3.  Sadaļā **Konteksts** atlasiet, vai šis cenrādis ir vienumam **Izmaksas**, **Iegāde** vai **Pārdošana**.  
  
4.  Laukā **Nosaukums** ievadiet cenrāža nosaukumu.  
  
5.  Laukā **Valūta** atlasiet valūtu, kuru izmantosiet rēķinu izrakstīšanai vai izmaksu grāmatošanai.  
  
6.  Laukā **Laika vienībā** norādiet laika periodu, uz kuru attiecas cena, piemēram, diena vai stunda.  
  
7.  Atbilstoši aizpildiet laukus **Sākuma datums**, **Beigu datums** un **Aapraksts**.  
  
8.  Noklikšķiniet uz **Saglabāt**, lai izveidotu ierakstu un pēc tam varētu veikt tā rediģēšanu.  
  
9. Lai cenrādim pievienotu lomas cenu, noklikšķiniet uz **+** sadaļā **Lomu cenas**.  
  
10. Rūtī **Lomas cena** aizpildiet datus un pēc tam noklikšķiniet uz **Saglabāt**. Ja nepieciešams, turpiniet pievienot lomu cenas. Kad esat pabeidzis, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.  
  
11. Lai cenrādim pievienotu izdevumu kategoriju, noklikšķiniet uz **+** sadaļā **Kategoriju cenas**.  
  
12. Rūtī **Transakcijas kategorijas cena** aizpildiet datus un pēc tam noklikšķiniet uz **Saglabāt**. Ja nepieciešams, turpiniet pievienot kategoriju cenas. Kad esat pabeidzis, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.  
  
13. Lai cenrādim pievienotu cenrāža elementus, noklikšķiniet uz **+** sadaļā **Cenrāža elementi**.  
  
14. Rūtī **Cenrāža elements** aizpildiet datus un pēc tam noklikšķiniet uz **Saglabāt**. Ja nepieciešams, turpiniet pievienot cenrāža elementus. Kad esat pabeidzis, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.  
  
15. Lai cenrādim pievienotu teritoriju relācijas, noklikšķiniet uz **+** sadaļā **Teritoriju relācijas**.  
  
16. Logā **Jauns savienojums** aizpildiet datus un pēc tam noklikšķiniet uz **Saglabāt**. Ja nepieciešams, turpiniet pievienot teritoriju relācijas. Kad esat pabeidzis, ekrāna apakšējā labajā stūrī noklikšķiniet uz **Saglabāt**.  
  
### <a name="see-also"></a>Skatiet arī  
 [Project Service Automation konfigurēšana](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
