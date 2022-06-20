---
title: Migrēt pilnībā rēķinos iekļautos norēķinu atskaites punktus, veicot pārslēgšanu
description: Šajā rakstā paskaidrots, kā migrēt fiksētas cenas norēķinu atskaites punktus, par kuriem klientam izrakstīts rēķins par atvērtiem projekta līgumiem pirms darbības beigu datuma.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d7bb3dbb5acd9be447c405ec17f18d00c500f655
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912249"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrēt pilnībā rēķinos iekļautos norēķinu atskaites punktus, veicot pārslēgšanu

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

## <a name="scenario"></a>Situācija

Contoso notiek tiešraidē ar Microsoft Dynamics 365 Project Operations resursu/neuzkrātu scenāriju gadījumā. Pārejas pasākumu ietvaros īstenošanas komandai ir jāmigrē atvērtie projektu līgumi no vecās sistēmas. Daži no projekta līgumiem ietver līguma rindas, kas izmanto fiksētas cenas norēķinu metodi un jau ir daļēji iekļautas rēķinā gala debitoram. Ieviešanas grupai šie norēķinu atskaites punkti ir jāmigrē kā **iegrāmatots** debitora rēķins, jo ieņēmumu atzīšanas nolūkos tie ir jāiekļauj kopējā līguma vērtībā. Tomēr klientu bilances debitoru un Virsgrāmatā nedrīkst ietekmēt.

## <a name="solution"></a>Risinājums

### <a name="prerequisites"></a>Priekšnoteikumi

- Dynamics 365 Finance 10.0.24 vai jaunāka versija ir jāinstalē.
- Videi, kurā tiks pabeigti migrācijas soļi, jābūt uzturēšanas režīmā. Kamēr tiek migrēti atskaites punkti, nevajadzētu veikt citas darbības.
- Migrācijas darbības ir jāveic tieši tā, kā aprakstīts šeit, un tās var izmantot tikai pārslēgšanas darbībai. Microsoft neatbalsta citu šīs iespējas izmantošanu.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Izveidot projekta operāciju integrācijas līguma rindas atskaites punktu divrakstījuma kartes pārslēgšanas versiju 

1. Pārliecinieties, vai mērķa kartējums projekta operāciju **integrācijas līguma rindas atskaites punktu entītijai ir atjaunināts**. 

    1. Sadaļā Finanses dodieties uz **datu pārvaldības** \> **datu entītijām** un atlasiet entītiju **Projekta operāciju integrācijas līguma rindas atskaites punkti.** 
    2. Atlasiet **Modificēt mērķa kartējumus**. 
    3. **Lapā Kartēšanas sagatavošana mērķa** sasniegšanai atlasiet **Ģenerēt kartējumu** un pēc tam apstipriniet, ka vēlaties ģenerēt kartējumu.

2. Apturiet un atsvaidziniet **projekta operāciju integrācijas līguma rindas atskaites punktus** (**msdyn\_ contractlinescheduleofvalues**) divu rakstīšanas karti. 

    1. Dodieties uz **Datu pārvaldība** \> **Dual-write**, atlasiet karti un atveriet tās informāciju. 
    2. Atlasiet **Apturēt** un pagaidiet, līdz sistēma aptur karti. 
    3. Atlasiet **Atsvaidzināt tabulas**.

3. Pievienojiet darbības statusa kartējumu.

    1. Atlasiet **Pievienot kartējumu**.
    2. Jaunās rindas **kolonnā Finanšu un operāciju programmas** atlasiet **lauku TRANSSTATUS TRANSSTATUS \[TRANSSTATUS\]**.
    3. **Microsoft Dataverse** Kolonnā atlasiet **msdyn\_ invoicestatus \[invoice status\]**.
    4. **Kolonnā Kartes tips** atlasiet labo bultiņu (**\>**).
    5. Parādītajā dialoglodziņā laukā Sinhronizācijas **virziens** atlasiet **Dataverse uz Finance and Operations programmas**.
    6. Atlasiet **Pievienot transformāciju**.
    7. Laukā **Transformēšanas tips** atlasiet **ValueMap**.
    8. Atlasiet **Pievienot vērtību kartējumu**.
    9. Kreisajā laukā ievadiet **4**. Labajā laukā ievadiet **192350001**. 
    10. Atlasiet **Saglabāt** un pēc tam aizveriet dialoglodziņu.

4. Atlasiet **Saglabāt kā**, lai saglabātu divrakstā rakstītās kartes versiju. 
5. **Tabulas** pievienošanas laukā **Publisher** atlasiet **Noklusējuma izdevējs**.
6. Laukā **Versija** ievadiet versiju.
7. Laukā **Apraksts** ievadiet piezīmi par šo kartes pārslēgšanas versiju. 
8. Atlasiet **Saglabāt**.
9. Sāciet karti.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrēt rēķinos iekļautos atskaites punktus uz Dataverse vidi

1. Projekta operāciju Dataverse vidē izveidojiet atskaites punktus, kuru rēķina statuss **ir Gatavs rēķinu izrakstīšanai**. Šajā brīdī neemigrējiet nevienu atskaites punktu, par kuru nav izrakstīts rēķins.

    > [!NOTE]
    > Pirms norēķinu atskaites punktu migrēšanas pārliecinieties, vai ar projekta līguma rindu saistītās finanšu dimensijas ir iestatītas, kā paredzēts. Finanšu dimensijas nevar rediģēt pēc migrācijas pabeigšanas.

2. Pēc tam, kad visi atskaites punkti ir migrēti, pārtrauciet šādas divu rakstīšanas kartes:

    - Projekta operāciju integrācijas līguma rindas atskaites punkti (msdyn\_ contractlinescheduleofvalues)
    - Project Operations integrācijas faktiskie dati (msdyn\_actuals)
    - Projekta rēķinu priekšlikums V2 (invoices)

    Lai apturētu kartes, rīkojieties šādi:

    1. Sadaļā Finanses dodieties uz **Datu pārvaldība** \> **Dubultā rakstīšana**, atlasiet karti un atveriet tās informāciju.
    2. Atlasiet **Apturēt** un pagaidiet, līdz sistēma aptur karti.

3. Projekta operāciju Dataverse vidē izveidojiet un apstipriniet pro-forma rēķinus norēķinu atskaites punktiem. 

    1. Vietnes kartē dodieties uz projekta līgumiem, atlasiet līgumus un pēc tam atlasiet **Izveidot rēķinus**.
    2. Pēc rēķinu izveides atveriet tos **vietnes kartes izvēlnē Rēķini** un pēc tam atlasiet **Apstiprināt**.

    Ar šo darbību vidē tiek izveidoti nepieciešamie ieraksti Dataverse. Tomēr tas neietekmē finanses un debitoru parādus, jo iepriekš uzskaitītās divciparu rakstīšanas kartes tika apturētas.

4. Pēc tam, kad visi pro-forma rēķini ir apstiprināti, atgrieziet visas dubultās rakstīšanas kartes sākotnējā stāvoklī.

    1. **Atjauniniet projekta operāciju integrācijas līguma rindas atskaites punktu** versiju (**msdyn\_ contractlinescheduleofvalues**) duālās rakstīšanas karti atpakaļ uz oriģinālu. 
    2. Kartes sarakstā atlasiet divu rakstīšanas karti, atlasiet **Tabulas kartes versija** un pēc tam atlasiet tabulas kartes sākotnējo versiju.
    3. Atlasiet **Saglabāt**.
    4. Restartējiet šādas duālās rakstīšanas kartes:

        - Projekta operāciju integrācijas līguma rindas atskaites punkti (msdyn\_ contractlinescheduleofvalues)
        - Project Operations integrācijas faktiskie dati (msdyn\_actuals)
        - Projekta rēķinu priekšlikums V2 (invoices)

Atskaites punkti tagad ir migrēti, un sistēma ir gatava nākamajiem pārslēgšanas darbības soļiem.
