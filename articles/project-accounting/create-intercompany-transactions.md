---
title: Starpuzņēmumu darbību izveide
description: Šajā rakstā ir sniegta informācija par to, kā izveidot starpuzņēmumu darbības.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: da6fd8e0e6bfe2e2543f5c4a453ed769e412f1e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919379"
---
# <a name="create-intercompany-transactions"></a>Starpuzņēmumu darbību izveide

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Starpuzņēmumu darbības ir laika un izdevumu darbības no projekta līguma, kas pieder vienam uzņēmumam vai organizācijas vienībai, savukārt projekta līguma resursi ir daļa no cita uzņēmuma vai organizācijas vienības.

Kad starpuzņēmumu darbība ir apstiprināta, tiek izveidotas tālāk norādītās faktiskās darbības.

| **Transakcijas veids** | **Lietotais cenrādis** | **Transakcijas valūta** |
| --- | --- | --- |
| izdevumi | Līgumslēdzēja vienības izmaksu cenrādis | Valūta cenas rindā |
| Rēķinā neiekļautā pārdošana. Tā tiek izveidota tikai faktiskajiem datiem, kas saistīti ar līguma rindu, kurā norādīts norēķinu tips, laiks un materiāls. | Līguma projekta pārdošanas cenrādis | Līguma valūta |
| Resursu struktūrvienības izmaksas | Resursu vienības izmaksu cenrādis | Valūta cenas rindā |
| Starporganizāciju vienības pārdošana | Līgumslēdzēja vienības izmaksu cenrādis | Valūta cenas rindā |

Izmaksas, resursu vienības izmaksas un starporganizāciju vienības pārdošanas darbību cenas un valūtu nosaka **Organizācijas vienība**. To ir svarīgi atcerēties, lemjot par to, kā strukturēt uzņēmumus un organizācijas struktūrvienības savā ieviešanā.

Kad izveidojat iespēju, piedāvājumu, projekta līgumu un projekta ierakstus, sistēma pārbauda, vai līgumslēdzēja vienības valūta atbilst līgumslēdzēja uzņēmuma uzskaites valūtai. Ja tās nav vienādas, šos ierakstus nevar izveidot. Organizācijas vienības valūta jānorāda programmā Dynamics 365 Project Operations, dodoties uz **Dataverse** > **Iestatījumi** > **Organizācijas vienības**. Uzņēmuma uzskaites valūta jānorāda programmā Dynamics 365 Finance, dodoties uz **Virsgrāmata** > **Virsgrāmatas iestatīšana** > **Virsgrāmata**. Valūta tiek sinhronizēta ar jūsu Dataverse vidi, izmantojot virsgrāmatu duālās rakstīšanas karti.

Sistēma izveido resursu vienības izmaksas un starporganizāciju vienības pārdošanas faktiskos datus tālāk norādītajās situācijās.

  - Ja resursu vienība atšķiras no līgumslēdzēja vienības
  - Ja resursu uzņēmums atšķiras no līgumslēdzēja uzņēmuma

Taču uz Dynamics 365 Finance vidi papildu uzskaitei tiks pārnestas tikai darbības, kuru resursu uzņēmums atšķiras no līgumslēdzēja uzņēmuma.

Projekta faktisko datu uzskaite tiek reģistrēta Project Operations integrācijas žurnālā programmā Finance. Sistēma izveido tālāk norādītās žurnāla rindas.

| **Transakcijas veids** | **Juridiskā persona** | **Grāmatošanas laikā izveido projekta darbību** | **Finanšu dimensiju noklusējums no** | **Noklusējuma norēķinu PVN grupa un norēķinu vienuma PVN grupa** |
| --- | --- | --- | --- | --- |
| izdevumi | Netiek pievienoti integrācijas žurnālam | N/A | N/A | N/A |
| Rēķinā neiekļautā pārdošana | Aizņēmuma juridiskās personas integrācijas žurnāls | Jā | Project | **Norēķinu PVN grupa**: pamatā ir **līguma klients** <br/> **Norēķinu vienuma PVN grupa**: pamatā ir pašreizējā juridiskās personas projekta kategorija žurnāla rindā. |
| Resursu struktūrvienības izmaksas | Aizdevuma juridiskās personas integrācijas žurnāls | Nr. | Starpuzņēmumu klients | **Norēķinu PVN grupa**: pamatā ir **starpuzņēmumu klients** <br/> **Norēķinu vienuma PVN grupa**: pamatā ir pašreizējā juridiskās personas projekta kategorija žurnāla rindā. |
| Starporganizāciju pārdošana | Aizdevuma juridiskās personas integrācijas žurnāls | Nr. | Starpuzņēmumu klients | **Norēķinu PVN grupa**: pamatā ir **starpuzņēmumu klients** <br/> **Norēķinu vienuma PVN grupa**: pamatā ir pašreizējā juridiskās personas projekta kategorija žurnāla rindā. |

### <a name="example-intercompany-transactions"></a>Piemērs: starpuzņēmumu darbības

Līga Krūmiņa, GBPM izstrādātāja, reģistrē 10 stundu darbu USPM Adventure Works projektā, ko ir apstiprinājis projekta vadītājs. Izstrādātāja izmaksas uzņēmumā GBPM ir 88 GBP stundā. GBPM izrakstīs rēķinu uzņēmumam USPM 120 USD apmērā par katru izstrādātāja stundu. USPM izrakstīs rēķinu klientam Adventure Works 200 USD apmērā par GBPM resursa paveikto darbu. Papildinformāciju skatiet sadaļā [Starpuzņēmumu rēķinu izrakstīšanas konfigurēšana](configure-intercompany-invoicing.md).

1. Risinājumā Project Operations dodieties uz **Resursi** un sarakstā atlasiet **Līga Krūmiņa**. Cilnes **Plānošana** laukā **Uzņēmums** atlasiet **GBPM**.
2. Dodieties uz **Pārdošana** > **Klienti** un atlasiet **Jauns**, lai izveidotu jaunu klienta ierakstu uzņēmumam Adventure Works.
    1. Iestatiet uzņēmumu uz **USPM**.
    2. Iestatiet vienumu **Attiecību tips** uz **Klients**.
    3. Atlasiet **Klientu grupa 10 — vietējā**.
    4. Iestatiet valūtu uz **USD**.
    5. Saglabājiet ierakstu.
3. Dodieties uz **Pārdošana** > **Projektu līgumi** un izveidojiet jaunu projekta līgumu uzņēmumam Adventure Works.
    1. Iestatiet atbildīgo uzņēmumu uz **USPM**, bet līgumslēdzēja vienību uz **Contoso Robotics US**.
    2. Atlasiet Adventure Works kā klientu.
    3. Atlasiet produkta cenrādi un saglabājiet ierakstu.
    4. Cilnē **Līguma rindas** izveidojiet jaunu līguma rindu. Iestatiet jebkādu nosaukumu un atlasiet **Laiks un materiāli** kā norēķinu metodi.
    5. Izveidojiet jaunu projektu un saistiet to ar šo līguma rindu.
4. Pierakstieties kā resurss **Līga Krūmiņa**. Dodieties uz **Projekti** > **Laika ieraksti** un izveidojiet laika ierakstu Adventure Works projektam.
5. Pierakstieties kā projekta vadītājs. Dodieties uz **Projekti** > **Apstiprinājumi** un apstipriniet Līgas Krūmiņas reģistrēto laika ieraksta darbību.
6. Pārejiet uz Adventure Works projektu un atlasiet **Saistītie** > **Faktiskie**. Tiek izveidotas tālāk norādītās faktiskās darbības.

| **Transakcijas veids** | **Cenrādis** | **Transakcijas valūta** | **Summa** |
| --- | --- | --- | --- |
| izdevumi | 120 | USD | 1200 |
| Rēķinā neiekļautā pārdošana | Vairāk nekā 200 | USD | 2000 |
| Resursu struktūrvienības izmaksas | 88 | GBP | 880 |
| Starporganizāciju vienības pārdošana | 120 | USD | 1200 |

7. Pierakstieties kā USPM grāmatvedis. Atveriet Project Operations Finance instanci un atlasiet uzņēmumu **USPM**. 
8. Dodieties uz **Projektu pārvaldība un uzskaite** > **Periodiski** > **Project Operations programmā Customer Engagement** > **Importēt no sagatavošanas tabulas** un atlasiet, lai palaistu periodisko procesu. Šis periodiskais process aizpildīs Project Operations integrācijas žurnālu.
9. Dodieties uz **Projektu pārvaldība un uzskaite** > **Žurnāli** > **Project Operations integrācijas žurnāls** un pārskatiet žurnāla rindas. Sistēma izveido tālāk norādīto žurnāla rindu.

    | **Transakcijas veids** | **Cenrādis** | **Transakcijas valūta** | **Summa** |
    | --- | --- | --- | --- |
    | Rēķinā neiekļautā pārdošana | Vairāk nekā 200 | USD | 2000 |

    Ja sistēma ir iestatīta tā, lai uzkrātu šī projekta ieņēmumus, tiek grāmatotas tālāk norādītās darbības.

    - Debets: projekts — NP pārdošanas vērtība 200 USD
    - Kredīts: projekts — uzkrātie ieņēmumi 200 USD

    Šī rēķinā neiekļautā pārdošana tagad ir gatava rēķina izrakstīšanai. Klienta Adventure Works rēķinu var finansiāli grāmatot, kad nepieciešams.

10. Pierakstieties kā **GBPM** grāmatvedis. Atveriet Project Operations Finance instanci un atveriet uzņēmumu **GBPM**. 
11. Dodieties uz **Projekta pārvaldības un uzskaites pārskats** > **Periodiski** > **Project Operations integrācija** > **Importēt no izstādīšanas tabulas** un izpildiet periodisko procesu, lai aizpildītu Project Operations integrācijas žurnālu.
12. Dodieties uz **Projektu pārvaldība un uzskaite** > **Žurnāli** > **Project Operations integrācijas žurnāls** un pārskatiet rindas. Sistēma izveido tālāk norādītās žurnāla rindas.

    | **Transakcijas veids** | **Cenrādis** | **Transakcijas valūta** | **Summa** |
    | --- | --- | --- | --- |
    | Resursu struktūrvienības izmaksas | 88 | GBP | 880 |
    | Starporganizāciju vienības pārdošana | 120 | USD | 1200 |

    Grāmatojot šos ierakstus, rodas tālāk norādītās dokumentu darbības.

    - Debets: projekta izmaksas 88 GBP
    - Kredīts: algu piešķiršana 88 GBP

    Ja sistēma ir iestatīta tā, lai uzkrātu starpuzņēmumu ieņēmumus, tiek grāmatotas tālāk norādītās darbības.

    - Debets: projekts — NP pārdošanas vērtība 120 USD
    - Kredīts: projekts — uzkrātie ieņēmumi 120 USD

    Tagad sistēma ir sagatavota starpuzņēmumu klienta rēķina izveidei.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
