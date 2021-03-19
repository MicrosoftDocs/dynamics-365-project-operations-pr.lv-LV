---
title: Vienību grupas un vienības
description: Šajā tēmā ir sniegta informācija par vienību grupām un vienībām.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 45e4a95b429cd9d1f174653bd28cf567f690676d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291628"
---
# <a name="unit-groups-and-units"></a>Vienību grupas un vienības

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Vienību grupas un vienības ir Microsoft Dynamics 365 pamata entītijas. Vienība ir viena mērvienība, un vairākas vienības var grupēt vienību grupās. Vienību grupa Dynamics 365 lietotāja interfeisā (UI) dažreiz tiek saukta arī par vienību grafiku. 

Tālāk sniegti daži vienību un vienību grupu piemēri.
 
- **Vienību grupa**: attālums 
    - **Vienības**: jūdze, kilometrs utt.
- **Vienību grupa**: laiks
    - **Vienības**: stunda, diena, nedēļa utt. 

Iestatot vairākas vienību grupas vienības, ir jāiestata arī pārvēršanas koeficients starp tām, norādot pirmo vienību, kas iestatīta kā vienību grupas noklusējuma vai primārā vienība. 

Piemēram, ja vienību grupā **Laiks** kā pirmo vienību iestatāt vienību **Stunda**, sistēma vienību **Stunda** apzīmē kā noklusējuma vienību. Ja nākamā vienība, ko iestatāt, ir **Diena**, jums ir jāiestata pārvēršanas koeficients starp vienībām **Diena** un **Stunda**. Ja pēc tam kā trešo vienību pievienosit vienību **Nedēļa**, jums jāiestata vienības **Nedēļa** pārvēršanas koeficients, lai to varētu izteikt vienībās **Diena** vai **Stunda**. 

Tālāk esošajā attēlā parādīts iestatīšanas piemērs vienībai **Diena**, kur laukā **Daudzums** ir parādīts stundu skaits vienā dienā, un vienībai **Nedēļa**, kur laukā **Daudzums** ir parādīts dienu skaits vienā nedēļā.

> ![Vienību grupa: informācijas lapa](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Vienību un vienību grupu izmantošana

Dynamics 365 Project Service Automation izmanto vienības un vienību grupas, lai apstrādātu gan izdevumu, gan laika novērtējumus un ierakstus. 

Attiecībā uz izdevumiem katrai izdevumu kategorijai ir noklusējuma vienību grupa un vienība. Šīs vērtības tiek ievadītas kā noklusējuma vērtības izdevumu kategoriju cenrāža ierakstos. 

Piemēram, jums ir izdevumu kategorija ar nosaukumu **Attālums**. Tai ir vienību grupa ar nosaukumu **Attālums** un noklusējuma vienība ar nosaukumu **Jūdze**. Ja vienību grupu **Distance** iestatāt tā, lai tai būtu divas vienības (**Jūdze** un **Kilometrs**), kategorijai **Attālums** varat iestatīt divas cenas vienā cenrādī: cenu par jūdzi un cenu par kilometru.

| Izdevumu kategorija  | Vienību grupa  | Vienība      | Izcenojuma metode  | Vienības cena  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Attālums           | Attālums      | Jūdze      | Vienības cena    | 10 USD            |
| Attālums           | Attālums      | Kilometrs | Vienības cena    |  6 USD            |

Kad projektā tiek ievadīti izdevumi, sistēma nosaka cenu, izmantojot kategorijas un izdevumu vienības kombināciju. 

| Izdevumu apraksts        | Izdevumu kategorija  | Vienība  | Daudzums  | Vienības cena   |
|----------------------------|---------------------|-------|-----------|----------------|
| Brauciens uz klienta atrašanās vietu | Attālums             | Jūdze  | 10        | 10 USD         |

Attiecībā uz laiku katram cenrāža virsrakstam ir lauks **Noklusējuma laika vienība**. Šī vērtība tiek iestatīta, kad izveidojat cenrāža virsrakstu. Pēc tam šī vienība tiek izmantota, lai iestatītu visas no lomas atkarīgās cenas šajā cenrādī.

Lauka **Laiks piedāvājumā** novērtējuma rindas var izteikt jebkurā laika vienībā. Taču novērtējuma rindas projektos un laika ieraksti projektos var izmantot tikai laika vienību **Stunda**. Ja vienība laika ierakstā vai novērtējuma rindā neatbilst šīs lomas vienībai cenrāža rindā, sistēma šo summu pārvērš par vienībām, kas ir definētas projekta novērtējumā vai projekta faktiskajā transakcijā.

Šajā piemērā ir parādīts, kā PSA izmanto vienību grupu, vienības un pārvēršanas koeficientus.
- Vienības

   - **Vienību grupa**: laiks 
   - **Vienības**: stunda 
    
    - **Diena** — pārvēršanas koeficients: 8 stundas       
    - **Nedēļa** — pārvēršanas koeficients: 40 stundu  
        
- Cenrāža iestatīšana projektā A.

    - **Nosaukums**: UK pārdošanas cenas 2016. gadā 
    - **Noklusējuma laika vienība**: diena 
    - **Valūta**: GBP

| Loma      | Vienību grupa | Vienība | Organizācijas vienība | Cena   |
|-----------|------------|------|---------------------|---------|
| Izstrādātājiem | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Laika ieraksts

Tālāk sniegtajā tabulā ir parādīta pārdošanas puses transakcija, kas izveidota programmā PSA trīs stundu projektam.


| Projekts   | Uzdevums    | Loma      | Daudzums | Vienība  | Vienības cena | Rēķinā neiekļautā pārdošanas summa |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekts A | Noformējums  | Izstrādātājiem | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Bieži uzdotie jautājumi par laika vienību

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Vai PSA veic pārvēršanu uz dažādām vienībām izdevumu gadījumā?
Nē. Vienību pārvēršana darbojas tikai laika vienībām. Attiecībā uz izdevumiem, ja sistēma nevar atrast cenu izdevumu kategorijas un vienības kombinācijai, cena pēc noklusējuma tiek iestatīta kā 0,00.

### <a name="why-does-psa-convert-time-units"></a>Kāpēc PSA pārvērš laika vienības?
Dažās valstīs vai reģionos ir juridiska prasība norēķinu likmes iestatīt dienās. Cenu apspriešana un atlaižu piemērošana piedāvājuma cikla laikā tiek veikta, izmantojot katras apmaksājamās lomas dienas likmes. Grafika novērtējumam un laika ierakstam tiek izmantotas stundas. Lai atbalstītu šo laika vienību atšķirību, PSA pārvērš laika vienības.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Vai laika vienības var mainīt projektu novērtējumos?
Nē. Grafika novērtējums pašlaik ir ierobežots līdz stundām, un to nevar mainīt.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Vai vienības un vienību grupas var rediģēt, dzēst un pievienot?
Jā. Izņemot vienību grupu **Laiks** un vienību **Stunda**, visas vienības var dzēst un rediģēt, kā arī var pievienot jaunas vienības. Programmā PSA nevar dzēst vienību grupu **Laiks** un **Stunda**. Tomēr tās var atjaunināt, izmantojot tulkotu tekstu laukam **Nosaukums**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]