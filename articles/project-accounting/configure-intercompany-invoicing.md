---
title: Starpuzņēmumu rēķinu izrakstīšanas konfigurēšana
description: Šajā tēmā ir sniegta informācija un piemēri par starpuzņēmumu rēķinu izrakstīšanas konfigurēšanu projektiem.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bdb6122d8aba84d2b449f9f17a4093388b585614
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595514"
---
# <a name="configure-intercompany-invoicing"></a>Starpuzņēmumu rēķinu izrakstīšanas konfigurēšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Izpildiet tālāk aprakstītās darbības, lai iestatītu starpuzņēmumu rēķinu izrakstīšanu projektiem programmā Dynamics 365 Project Operations. Starpuzņēmumu darbības ir laika un izdevumu darbības no projekta līguma, kas pieder vienam uzņēmumam vai organizācijas vienībai, savukārt projekta līguma resursi ir daļa no cita uzņēmuma vai organizācijas vienības.

## <a name="example-configure-intercompany-invoicing"></a>Piemērs: starpuzņēmumu rēķinu izrakstīšanas konfigurēšana

Tālāk sniegtajā piemērā Contoso Robotics USA (USPM) ir aizņēmuma juridiskā persona, bet Contoso Robotics UK (GBPM) — aizdevuma juridiskā persona. 

1. **Konfigurējiet starpuzņēmumu uzskaiti starp juridiskajām personām**. Katram aizņēmuma un aizdevuma juridisko personu pārim ir jābūt konfigurētam virsgrāmatas lapā [Starpuzņēmumu uzskaite](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. Programmā Dynamics 365 Finance dodieties uz **Virsgrāmata** > **Grāmatošanas iestatīšana** > **Starpuzņēmumu uzskaite**. Izveidojiet ierakstu, ievadot tajā tālāk norādīto informāciju.

        - **Izveides uzņēmums** = **GBPM**
        - **Mērķa uzņēmums** = **USPM**

2. **Konfigurējiet tirdzniecības attiecības starp juridiskajām personām**. Klienta ieraksts, kas atbilst aizņēmuma juridiskajai personai, ir jāizveido aizdevuma juridiskajā personā. Piegādātāja ieraksts, kas atbilst aizdevuma juridiskajai personai, ir jāizveido aizņēmuma juridiskajā personā.

     1. Programmā Finance atlasiet juridisko personu **GBPM**.
     2. Dodieties uz **Debitori** > **Klients** > **Visi klienti**. Izveidojiet jaunu juridiskās personas ierakstu: **USPM**.
     3. Izvērsiet sadaļu **Nosaukums**, filtrējiet ierakstus pēc kategorijas **Tips** un atlasiet **Juridiskās personas**. 
     4. Atrodiet un atlasiet **Contoso Robotics USA (USPM)** klienta ierakstu.
     5. Atlasiet **Lietot atbilstību**. 
     6. Atlasiet klientu grupu un pēc tam saglabājiet ierakstu.
     7. Atlasiet juridisko personu **USPM**.
     8. Dodieties uz **Kreditori** > **Piegādātāji** > **Visi piegādātāji**. Izveidojiet jaunu juridiskās personas ierakstu: **GBPM**.
     9. Izvērsiet sadaļu **Nosaukums**, filtrējiet ierakstus pēc kategorijas **Tips** un atlasiet **Juridiskās personas**. 
     10. Atrodiet un atlasiet **Contoso Robotics UK (GBPM)** klienta ierakstu.
     11. Atlasiet **Lietot atbilstību**, atlasiet piegādātāju grupu un pēc tam saglabājiet ierakstu.
     12. Piegādātāja ierakstā atlasiet **Vispārīgi** > **Iestatīt** > **Starpuzņēmumu**.
     13. Cilnē **Tirdzniecības attiecības** iestatiet **Aktīvas** uz **Jā**.
     14. Atlasiet piegādātāja uzņēmumu **GBPM** un sadaļā **Mans uzņēmuma ieraksts** atlasiet klienta ierakstu, kuru iepriekš izveidojāt procedūrā.

3. **Konfigurējiet starpuzņēmumu iestatījumus lapā Projektu pārvaldības un uzskaites parametri**. 

    1. Atlasiet juridisko personu **USPM** un dodieties uz **Projektu pārvaldība un uzskaite** > **Iestatīšana** > **Projektu pārvaldības un uzskaites parametri**.
    2. Cilnē **Starpuzņēmumu** atlasiet sagādes kategoriju, kas atbilst automātiski ģenerētajiem piegādātaja rēķiniem.
    3. Sadaļā **Noklusējuma kategorija** atlasiet **Starpuzņēmumu resursi**.
    4. Atlasiet juridisko personu **GBPM** un dodieties uz **Projektu pārvaldība un uzskaite** > **Iestatīšana** > **Projektu pārvaldības un uzskaites parametri**.
    5. Cilnē **Starpuzņēmumu** atlasiet noklusējuma projekta kategoriju katram darbības tipam. Projekta kategorijas tiek izmantotas nodokļu konfigurēšanai, ja starpuzņēmumu transakcijās iekļautā kategorija, par kuru izrakstīts rēķins, pastāv tikai aizņemošajā juridiskajā personā. Varat izvēlēties, vai jāuzkrāj ieņēmumi no starpuzņēmumu transakcijām. Uzkrāšana notiek, kad darbības tiek grāmatotas, izmantojot Project Operations integrācijas žurnālu aizdevuma juridiskajā personā. Žurnāls tiek apvērsts, kad tiek grāmatots starpuzņēmumu rēķins.
    6. Grupā **Resursu aizdošana** atlasiet **...** > **Jauns**. 
    7. Režģī atlasiet tālāk norādīto informāciju.

          - **Aizņēmuma juridiskā persona** = **GBPM**
          - **Uzkrāt ieņēmumus** = **Jā**
          - **Noklusējuma darba laika uzskaites tabulas kategorija** = **Noklusējums — stunda**
          - **Noklusējuma izdevumu kategorija** = **Noklusējums — izdevumi**

4. **Iestatiet starpuzņēmumu izmaksu un ieņēmumu kontus virsgrāmatas grāmatošanas iestatījumos**. Starpuzņēmumu ieņēmumu konts tiek kreditēts, kad starpuzņēmumu klienta rēķins tiek grāmatots aizdevuma juridiskajā personā. Starpuzņēmumu izmaksu konts tiek debitēts, kad atbilstošais gaidošais piegādātāja rēķins tiek grāmatots aizņēmuma juridiskajā personā. Šie konti tiek iestatīti atbilstošajās juridiskajās personās. 
      
     1. Programmā Finance atlasiet aizņēmuma juridisko personu **USPM**. 
     2. Dodieties uz **Projektu pārvaldība un uzskaite** > **Iestatīšana** > **Grāmatošana** > **Virsgrāmatas grāmatošanas iestatīšana**. 
     3. Cilnes **Izmaksu konti** sadaļā **Virsgrāmatas konta tips** atlasiet **Starpuzņēmumu izmaksas**. Izveidojiet jaunu ierakstu, ievadot tajā tālāk norādīto informāciju.
      
        - **Aizdevuma juridiskā persona** = **GBPM**
        - **Galvenais konts** = Atlasiet starpuzņēmumu izmaksu galveno kontu
        
     4. Atlasiet aizdevuma juridisko personu **GBPM**. 
     5. Dodieties uz **Projektu pārvaldība un uzskaite** > **Iestatīšana** > **Grāmatošana** > **Virsgrāmatas grāmatošanas iestatīšana**. 
     6. Cilnes **Ieņēmumu konti** sadaļā **Virsgrāmatas konta tips** atlasiet **Starpuzņēmumu ieņēmumi**. Izveidojiet jaunu ierakstu, ievadot tajā tālāk norādīto informāciju.

        - **Aizņēmuma juridiskā persona** = **USPM**
        - **Galvenais konts** = Atlasiet starpuzņēmumu ieņēmumu galveno kontu 

5. **Iestatiet nodošanas cenu noteikšanu par darbu**. Starpuzņēmumu nodošanas cenas tiek konfigurētas risinājumā Project Operations programmā Dataverse. Konfigurējiet [darba izmaksu likmes](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) un [darba norēķinu likmes](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) starpuzņēmumu rēķinu izrakstīšanai. Nodošanas cenas netiek atbalstītas starpuzņēmumu izmaksu darbībām. Starporganizāciju vienības pārdošanas cena vienmēr būs iestatīta uz to pašu vērtību, uz kuru iestatīta resursa vienības izmaksu cena.

      Izstrādātāja resursa izmaksas uzņēmumā Contoso Robotics UK ir 88 GBP stundā. Contoso Robotics UK izrakstīs rēķinu uzņēmumam Contoso Robotics USA 120 USD apmērā par katru stundu, ko šis resurss ir veltījis USA projektiem. Contoso Robotics USA izrakstīs rēķinu klientam Adventure Works 200 USD par Contoso Robotics UK izstrādātāja resursa paveikto darbu.

      1. Risinājumā Project Operations programmā Dataverse dodieties uz **Pārdošana** > **Cenrāži**. Izveidojiet jaunu izmaksu cenrādi ar nosaukumu **Contoso Robotics UK izmaksu likmes.** 
      2. Izmaksu cenrādī izveidojiet ierakstu ar tālāk norādīto informāciju.
         - **Loma** = **Izstrādātājs**
         - **Izmaksas** = **88 GBP**
      3. Dodieties uz **Iestatījumi** > **Organizācijas vienības** un pievienojiet šo izmaksu cenrādi organizācijas vienībai **Contoso Robotics UK**.
      4. Dodieties uz **Pārdošana** > **Cenrāži**. Izveidojiet izmaksu cenrādi ar nosaukumu **Contoso Robotics USA izmaksu likmes**. 
      5. Izmaksu cenrādī izveidojiet ierakstu ar tālāk norādīto informāciju.
          - **Loma** = **Izstrādātājs**
          - **Resursu uzņēmums** = **Contoso Robotics UK**
          - **Izmaksas** = **120 USD**
      6. Dodieties uz **Iestatījumi** > **Organizācijas vienības** un pievienojiet izmaksu cenrādi **Contoso Robotics USA izmaksu likmes** organizācijas vienībai **Contoso Robotics USA**.
      7. Dodieties uz **Pārdošana** > **Cenrāži**. Izveidojiet pārdošanas cenrādi ar nosaukumu **Adventure Works norēķinu likmes**. 
      8. Pārdošanas cenrādī izveidojiet ierakstu ar tālāk norādīto informāciju.
          - **Loma** = **Izstrādātājs**
          - **Resursu uzņēmums** = **Contoso Robotics UK**
          - **Norēķinu likme** = **200 USD**
      9. Dodieties uz **Pārdošana** > **Projektu līgumi** un pievienojiet cenrādi **Adventure Works norēķinu likmes** Adventure Works projekta līguma projekta cenrādim.


[!INCLUDE[footer-include](../includes/footer-banner.md)]