---
title: Pilnībā rēķinā norādīto norēķinu atskaites punktu migrēšana pārslēgšanas laikā
description: Šajā rakstā ir paskaidrots, kā migrēt fiksētas cenas norēķinu atskaites punktus, par kuriem debitoram ir izrakstīti rēķini par atvērtiem projektu līgumiem pirms tiešraides datuma.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Pilnībā rēķinā norādīto norēķinu atskaites punktu migrēšana pārslēgšanas laikā

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

## <a name="scenario"></a>Situācija

Contoso sāk darboties ar Microsoft Dynamics 365 Project Operations, lai iegūtu resursresursus/ scenārijus, kas nav krājumi. Kā daļa no pārslēgšanas pasākumiem īstenošanas komandai ir jāmigrē atvērtie projektu līgumi no vecās sistēmas. Dažos projekta līgumos ir iekļautas līgumu rindas, kurās tiek izmantota fiksētas cenas norēķinu metode un par kurām jau ir izrakstīts daļējs rēķins gala klientam. Ieviešanas darba grupai šie norēķinu atskaites punkti ir jāmigrē kā **klienta rēķins, kas tiek grāmatoti**, jo ieņēmumu atzīšanas nolūkos tie ir jāiekļauj kopējā līguma vērtībā. Tomēr nedrīkst ietekmēt debitoru parādu un virsgrāmatas debitoru parādu atlikumus.

## <a name="solution"></a>Risinājums

### <a name="prerequisites"></a>Priekšnoteikumi

- Dynamics 365 Finance 10.0.24 vai jaunākai versijai.
- Videi, kurā tiks pabeigtas migrācijas darbības, ir jābūt uzturēšanas režīmā. Citas darbības nedrīkst veikt, kamēr tiek migrēti atskaites punkti.
- Migrācijas soļi ir jāievēro tieši tā, kā aprakstīts šeit, un tos var izmantot tikai pārslēgšanas darbībai. Microsoft neatbalsta citu šīs iespējas izmantošanu.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Projekta operāciju integrācijas līguma rindiņas atskaites punktu pārgriezuma versijas izveide ar dubultrakstīšanas karti 

1. Pārliecinieties, vai projekta operāciju integrācijas **līguma rindiņas entītijas mērķa kartējums ir atjaunināts**. 

    1. Programmā Finance dodieties uz **Datu pārvaldības** \> **datu entītijas** un atlasiet entītiju **Project Operations integrācijas līguma rindiņas atskaites** punkti. 
    2. Atlasiet **Modificēt mērķa kartējumus**. 
    3. **Lapā Kartes izstādīšana, lai atlasītu** atlasiet **Ģenerēt kartēšanu** un pēc tam apstipriniet, ka vēlaties ģenerēt kartēšanu.

2. Apturiet un atsvaidziniet **Project Operations integrācijas līguma rindiņu atskaites punktus** (**msdyn\_ contractlinescheduleofvalues**) divu rakstīšanas karti. 

    1. Dodieties uz **Datu pārvaldība** \> **Dubultā rakstīšana**, atlasiet karti un atveriet tās detaļas. 
    2. Atlasiet **Apturēt** un pagaidiet, līdz sistēma aptur karti. 
    3. Atlasiet **Atsvaidzināt tabulas**.

3. Pievienojiet transakcijas statusa kartējumu.

    1. Atlasiet **Pievienot kartējumu**.
    2. Jaunās rindas **kolonnā Finance and operations programmas** atlasiet **lauku TRANSSTATUS \[TRANSSTATUS\]**.
    3. **Microsoft Dataverse** Kolonnā atlasiet **msdyn\_ invoicestatus \[rēķina statusu\]**.
    4. **Kolonnā Kartes tips** atlasiet labo bultiņu (**\>**).
    5. Parādītajā dialoglodziņā laukā Sinhronizācijas virziens **atlasiet** **Dataverse finance and operations lietojumprogrammas**.
    6. Atlasiet **Pievienot transformāciju**.
    7. **Laukā Transformācijas tips** atlasiet **ValueMap**.
    8. Atlasiet **Pievienotās vērtības kartēšana**.
    9. Kreisajā laukā ievadiet **4**. Labajā laukā ievadiet **192350001**. 
    10. Atlasiet **Saglabāt** un pēc tam aizveriet dialoglodziņu.

4. Atlasiet **Saglabāt kā**, lai saglabātu dubultās rakstīšanas kartes versiju. 
5. Tabulas pievienošanas **rūts** **laukā Publisher** atlasiet **Noklusējuma izdevējs**.
6. Laukā **Versija** ievadiet versiju.
7. **Laukā Apraksts** ievadiet piezīmi par šo kartes pārslēgšanas versiju. 
8. Atlasiet **Saglabāt**.
9. Sāciet karti.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Rēķinā norādīto atskaites punktu migrēšana uz Dataverse vidi

1. Vidē Project Operations Dataverse izveidojiet atskaites punktus, kuru rēķina statuss **ir Gatavs rēķinu izrakstīšanai**. Šajā brīdī nemigrējiet atskaites punktus, par kuriem nav izrakstīts rēķins.

    > [!NOTE]
    > Pirms norēķinu atskaites punktu migrēšanas pārliecinieties, vai finanšu dimensijas, kas ir saistītas ar projekta līguma rindiņu, ir iestatītas, kā paredzēts. Finanšu dimensijas nevar rediģēt pēc migrācijas pabeigšanas.

2. Pēc tam, kad visi atskaites punkti ir migrēti, pārtrauciet šādas divējāda rakstīšanas kartes:

    - Projekta operāciju integrācijas līguma rindiņu atskaites punkti (msdyn\_ kontraktalīnijasviduālās vērtības)
    - Project Operations integrācijas faktiskie dati (msdyn\_actuals)
    - Projekta rēķinu priekšlikums V2 (invoices)

    Lai apturētu kartes, rīkojieties šādi:

    1. Programmā Finance dodieties uz **Datu pārvaldība** \> **Divreiz rakstiet**, atlasiet karti un atveriet tās detaļas.
    2. Atlasiet **Stop (Stop)** un pagaidiet, līdz sistēma aptur karti.

3. Vidē Project Operations Dataverse izveidojiet un apstipriniet pro-forma rēķinus par norēķinu atskaites punktiem. 

    1. Vietnes kartē dodieties uz projektu līgumiem, atlasiet līgumus un pēc tam atlasiet **Izveidot rēķinus**.
    2. Kad rēķini ir izveidoti, atveriet tos **vietnes kartes izvēlnē Rēķini** un pēc tam atlasiet **Apstiprināt**.

    Veicot šo darbību, tiek izveidoti nepieciešamie ieraksti Dataverse vidē. Tomēr tas neietekmē finanšu un debitoru parādus, jo iepriekš uzskaitītās dubultās rakstīšanas kartes tika apturētas.

4. Pēc tam, kad visi pro-forma rēķini ir apstiprināti, atgrieziet visas dubultās rakstīšanas kartes sākotnējā stāvoklī.

    1. Atjauniniet Project Operations integrācijas līguma rindiņu **atskaites** punktu (**msdyn\_ contractlinescheduleofvalues**) versiju ar dubultrakstīšanas karti atpakaļ uz oriģinālu. 
    2. Karšu sarakstā atlasiet divu rakstu karti, atlasiet **Tabulas kartes versija** un pēc tam atlasiet tabulas kartes sākotnējo versiju.
    3. Atlasiet **Saglabāt**.
    4. Restartējiet šādas divrakstu kartes:

        - Projekta operāciju integrācijas līguma rindiņu atskaites punkti (msdyn\_ kontraktalīnijasviduālās vērtības)
        - Project Operations integrācijas faktiskie dati (msdyn\_actuals)
        - Projekta rēķinu priekšlikums V2 (invoices)

Atskaites punkti tagad ir migrēti, un sistēma ir gatava nākamajiem pārslēgšanas darbības soļiem.
