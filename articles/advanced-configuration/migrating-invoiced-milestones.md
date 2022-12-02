---
title: Pilnībā izrakstītu rēķinu atskaites punktu migrēšana apgriešanas laikā
description: Šajā rakstā izskaidrots, kā migrēt fiksētas cenas norēķinu atskaites punktus, par kuriem klientam izrakstīts rēķins, lai pirms tiešā datuma atvērtu projekta līgumus.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028711"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Pilnībā izrakstītu rēķinu atskaites punktu migrēšana apgriešanas laikā

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

## <a name="scenario"></a>Situācija

Contoso gatavojas izmantot Microsoft Dynamics 365 Project Operations resursu / ne krājumu scenārijiem. Kā daļu no izgriešanas darbībām, ieviešanas darba grupai jāmigrē atvērti projektu līgumi no vecās sistēmas. Dažos projektu līgumos ir ietvertas līgumu rindas, kas izmanto fiksēto cenu norēķinu metodi un par kurām gala klientam jau daļēji izrakstīts rēķins. Ieviešanas darba grupai jāmigrē šie norēķinu atskaites punkti kā **Grāmatots klienta rēķins**, jo tos jāiekļauj kopējā līguma vērtībā ieņēmumu atpazīšanas nolūkā. Taču nedrīkst ietekmēt klienta bilances attiecībā uz Debitoriem un Virsgrāmatu.

## <a name="solution"></a>Risinājums

### <a name="prerequisites"></a>Priekšnoteikumi

- Ir jābūt instalētai programmai Dynamics 365 Finance ar 10.0.24 vai jaunāku versiju.
- Videi, kurā tiks izpildītas migrācijas darbības, ir jābūt uzturēšanas režīmā. Atskaites punktu migrēšanas laikā citas darbības nedrīkst veikt.
- Migrēšanas darbības jāveic tieši tā, kā aprakstīts šeit, un tās var izmantot tikai izgriešanas darbībām. Microsoft neatbalsta citu šīs iespējas lietojumu.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Izveidojiet Project Operations integrācijas līguma rindas atskaites punktu duālās rakstīšanas kartes pārslēgšanas versiju 

1. Pārliecinieties, ka **Project Operations integrācijas līguma rindas atskaites punktu** entitījas mērķa kartējums ir atjaunināts. 

    1. Programmā Finance dodieties uz **Datu pārvaldība**\>**Datu entitījas** un atlasiet entitīju **Project Operations integrācijas līguma rindu atskaites punkti**. 
    2. Atlasiet **Pārveidot mērķa kartējumus**. 
    3. Lapā **Kartēt izstādīšanu uz mērķi** atlasiet **Ģenerēt kartējumu**, pēc tam apstipriniet, ka vēlaties ģenerēt kartējumu.

2. Apturiet un atsvaidziniet duālās rakstīšanas karti **Project Operations integrācijas līguma rindu atskaites punkti**(**msdyn\_contractlinescheduleofvalues**). 

    1. Dodieties uz **Datu pārvaldība**\>**Duālā rakstīšana**, atlasiet karti un atveriet tās informāciju. 
    2. Atlasiet **Apturēt** un pagaidiet, līdz sistēma aptur karti. 
    3. Atlasiet **Atsvaidzināt tabulas**.

3. Pievienojiet kartējumu transakcijas statusam.

    1. Atlasiet **Pievienot kartējumu**.
    2. Jaunajā rindā kolonnā **Finanšu un operāciju programmas** atlasiet lauku **TRANSSTATUS \[TRANSSTATUS\]**.
    3. **Microsoft Dataverse** kolonnā atlasiet msdyn **\_invoicestatus \[rēķina statuss\]**.
    4. Kolonnā **Kartes tips** atlasiet labo bultiņu (**\>**).
    5. Dialoglodziņā, kas tiek parādīts laukā **Sinhronizācijas virziens**, atlasiet **Dataverse līdz finanšu un operāciju programmas**.
    6. Atlasiet **Pievienot pārveidi**.
    7. Laukā **Pārveides tips** atlasies **ValueMap**.
    8. Atlasiet **Pievienot vērtības kartējumu**.
    9. Kreisajā laukā ievadiet **4**. Labās puses laukā ierakstiet **192350001**. 
    10. Atlasiet **Saglabāt** un tad aizveriet dialoglodziņu.

4. Atlasiet **Saglabāt kā**, lai saglabātu duālās rakstīšanas kartes versiju. 
5. Rūtī **Pievienot tabulu** laukā **Izdevējs** atlasiet **Noklusējuma izdevējs**.
6. Laukā **Versija** ievadiet versiju.
7. Laukā **Apraksts** ievadiet piezīmi par šo kartes pārslēgšanas versiju. 
8. Atlasiet **Saglabāt**.
9. Sāciet kartēšanu.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Atskaites punktu, par kuriem izrakstīts rēķins, migrācija uz Dataverse vidi

1. Project Operations Dataverse vidē izveidojiet atskaites punktus ar rēķina statusu **Gatavs rēķina izrakstīšanai**. Šajā brīdī nemigrējiet citus atskaites punktus, par kuriem nav izrakstīts rēķins.

    > [!NOTE]
    > Pirms norēķinu atskaites punktu migrēšanas pārliecinieties, vai ar projekta līguma rindu saistītās finanšu kategorijas ir iestatītas, kā paredzēts. Pēc migrēšanas pabeigšanas finanšu dimensijas nevar rediģēt.

2. Pēc visu atskaites punktu migrēšanas, apturiet tālāk uzskaitītās duālās rakstīšanas kartes:

    - Project Operations integrācija līguma rindas atskaites punktos (msdyn\_contractlinescheduleofvalues)
    - Project Operations integrācijas faktiskie dati (msdyn\_actuals)
    - Projekta rēķinu priekšlikums V2 (invoices)

    Lai apturētu kartes, izpildiet tālāk uzskaitītās darbības:

    1. Programmā Finance uz **Datu pārvaldība**\>**Duālā rakstīšana**, atlasiet karti un atveriet tās informāciju.
    2. Atlasiet **Apturēt** un pagaidiet, līdz sistēma aptur karti.

3. Project Operations Dataverse vidē izveidojiet un apstipriniet pro forma rēķinus par norēķinu atskaites punktiem. 

    1. Vietnes kartē atveriet projekta līgumus, atlasiet līgumus un pēc tam atlasiet opciju **Izveidot rēķinus**.
    2. Pēc rēķinu izveides atveriet tos no vietnes kartes izvēlnes **Rēķini**, pēc tam atlasiet **Apstiprināt**.

    Ar šo darbību Dataverse vidē tiek izveidoti vajadzīgie ieraksti. Taču tas neietekmē finanses un debitorus, jo tika apturētas iepriekš uzskaitītās duālās rakstīšanas kartes.

4. Pēc visu pro forma rēķinu apstiprināšanas, atgrieziet visas duālās rakstīšanas kartes to sākotnējā stāvoklī.

    1. Atjauniniet duālās rakstīšanas kartes **Project Operations integrācijas līguma rindu atskaites punkti**(**msdyn\_contractlinescheduleofvalues**) versiju atpakaļ uz oriģinālu. 
    2. Karšu sarakstā atlasiet duālās rakstīšanas karti, atlasiet **Tabulas kartes versija** un atlasiet tabulas kartes oriģinālo versiju.
    3. Atlasiet **Saglabāt**.
    4. Restartējiet tālāk norādītās duālās rakstīšanas kartes:

        - Project Operations integrācija līguma rindas atskaites punktos (msdyn\_contractlinescheduleofvalues)
        - Project Operations integrācijas faktiskie dati (msdyn\_actuals)
        - Projekta rēķinu priekšlikums V2 (invoices)

Atskaites punktu skaits tagad ir migrēts, un sistēma ir gatava pārejai uz nākamajām darbībām.
