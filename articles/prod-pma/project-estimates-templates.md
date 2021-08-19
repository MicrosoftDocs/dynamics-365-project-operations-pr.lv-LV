---
title: Projekta aprēķinu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta stundu aprēķinu un projekta izmaksu aprēķinu sinhronizēšanai tieši no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 6696449d80e0915a0c878dbe75cfdf6e268b98ad9f6453bcfc4b424db68021e4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988210"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Projekta aprēķinu sinhronizēšana tieši no Project Service Automation uz Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta stundu aprēķinu un projekta izmaksu aprēķinu sinhronizēšanai tieši no Dynamics 365 Project Service Automation uz Dynamics 365 Finance.

> [!NOTE]
> - 8.0 versijā varat izmantot projekta uzdevumu integrāciju, izdevumu darbības kategorijas, stundu aprēķinus, izdevumu aprēķinus un funkcionalitātes bloķēšanu.
> - Faktisko datu integrācija ir pieejama 8.0.1 vai jaunākās versijās.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datu plūsma Project Service Automation uz Finance

Project Service Automation uz Finance integrācijas risinājumam tiek izmantots datu integrācijas līdzeklis, lai sinhronizētu datus starp Project Service Automation un Finance. Integrācijas veidnes, kas ir pieejamas kopā ar datu integrācijas līdzekli, iespējo datu plūsmu par projekta stundu aprēķiniem un projekta izmaksu aprēķiniem no Project Service Automation līdz Finance.

Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti starp Project Service Automation un Finance.

[![Datu plūsma Project Service Automation integrācijai ar Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projekta stundu aprēķini

### <a name="template-and-tasks"></a>Veidne un uzdevumi

Lai piekļūtu pieejamajām veidnēm, Microsoft Power Apps administrēšanas centrā atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskas veidnes.

Lai sinhronizētu projekta stundu aprēķinus no Project Service Automation uz Finance, tiek izmantota šāda veidne un pamata uzdevumi:

- **Veidnes nosaukums datu integrācijā:** Projekta stundu aprēķini (PSA uz Fin un Ops)
- **Projekta uzdevumu nosaukums:**

    - Transakciju saistības
    - Izdevumu tāmes

### <a name="entity-set"></a>Entītiju kopa

| Project Service Automation | Finance                                       |
|----------------------------|-----------------------------------------------|
| Projekta uzdevumi              | Integrācijas entitīja projekta stundu aprēķiniem |

### <a name="entity-flow"></a>Entītijas plūsma

Projekta stundu aprēķini tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta stundu prognozes.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms var notikt projekta stundu aprēķinu sinhronizēšana, ir jāsinhronizē projekti, projekta uzdevumi un projekta izdevumu transakciju kategorijas.

### <a name="power-query"></a>Power Query

Projekta stundu aprēķinu veidnē ir jāizmanto Microsoft Power Query for Excel, lai izpildītu šos uzdevumus:

- Iestatiet noklusējuma prognozes modeļa ID, kas tiks izmantots, kad integrācija veidos jaunas stundu prognozes.
- Izfiltrējiet visus resursiem specifiskos ierakstus uzdevumā, kas nevarēs integrēties stundu prognozēs.
- Izfiltrējiet visas tukšās transakcijas kategoriju rindas. Ja šo uzdevumu nevar izpildīt, var rasties nepareizas stundu prognozes.

#### <a name="set-the-default-forecast-model-id"></a>Iestatiet noklusējuma prognozes modeļa ID

Lai veidnē atjauninātu noklusējuma prognozes modeļa ID, noklikšķiniet uz bultiņas **Karte**, lai atvērtu kartējumu. Pēc tam atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti.

- Ja izmantojat noklusējuma Projekta stundu aprēķinu (PSA uz Fin un Ops) veidni, **Piemērojamo darbību** sarakstā atlasiet **Ievietoto nosacījumu**. **Funkciju** ierakstā aizstājiet **O\_prognozi** ar tā prognozes modeļa ID, kuru vajadzētu izmantot ar integrāciju. Noklusējuma veidnei ir prognozes modeļa ID no demonstrācijas datiem.
- Ja izveidojat jaunu veidni, šī kolonna ir jāpievieno. Power Query atlasiet **Pievienot nosacījuma kolonnu** un ievadiet jaunās kolonnas nosaukumu, piemēram, **ModelID**. Ievadiet kolonnas nosacījumu, kur, ja projekta uzdevums nav Null, tad \<enter the forecast model ID\>; pretējā gadījumā tas ir Null.

#### <a name="filter-out-resource-specific-records"></a>Resursiem specifisku ierakstu izfiltrēšana

Projekta stundas aprēķinu (PSA uz Fin un Ops) veidnei ir noklusējuma filtrs, kas noņem jebkādus resursiem specifiskos ierakstus. Ja izveidojat savu veidni, šis filtrs ir jāpievieno. Atlasiet **Detalizētā vaicājuma un filtrēšanas** saiti, lai filtrētu **msdyn\_islinetask** kolonnā, lai tiek iekļauti vienīgi ieraksti **False**.

#### <a name="filter-out-empty-transaction-category-rows"></a>Izfiltrējiet tukšās transakcijas kategoriju rindas

Lai noņemtu rindas, kurās ir tukšas transakciju kategorijas, ir jāpievieno filtrs. Šis uzdevums ir obligāts neatkarīgi no tā, vai izmantojat noklusējuma veidni, vai izveidojat paši savu. Ar šo filtru tiek noņemtas visas kopsavilkuma rindas no Project Service Automation, kuras varētu radīt nepareizas stundu prognozes risinājumā Finance. Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti, lai izfiltrētu tukšos ierakstus kolonnā **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Veidņu kartēšana datu integrācijā

Nākamajā ilustrācijā ir redzams piemērs no veidnes uzdevumu kartējuma datu integrācijā. Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.

[![Veidnes uzdevuma kartēšana datu integrācijā.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projekta izmaksu aplēses

### <a name="template-and-tasks"></a>Veidne un uzdevumi

Lai sinhronizētu projekta izmaksu aprēķinus no Project Service Automation uz Finance, tiek izmantota šāda veidne un pamata uzdevumi:

- **Veidnes nosaukums datu integrācijā:** Projekta izmaksu aprēķini (PSA uz Fin un Ops)
- **Projekta uzdevumu nosaukums:**

    - Transakciju saistības 
    - Izdevumu tāmes

### <a name="entity-set"></a>Entītiju kopa

| Project Service Automation | Finance                                                  |
|----------------------------|----------------------------------------------------------|
| Transakcijas savienojumi    | Integrāciju entitīja projekta transakciju relācijām |
| Novērtējuma rindas             | Integrācijas entitīja projekta izmaksu aprēķiniem         |

### <a name="entity-flow"></a>Entītijas plūsma

Projekta izmaksu aprēķini tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta izmaksu prognozes.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms var notikt projekta stundu izmaksu sinhronizēšana, ir jāsinhronizē projekti, projekta uzdevumi un projekta izdevumu transakciju kategorijas.

### <a name="power-query"></a>Power Query

Projekta izmaksu aprēķinu veidnē ir jāizmanto Power Query, lai izpildītu šos uzdevumus:

- Filtrēt, lai iekļautu tikai izmaksas aprēķinu rindas ierakstus.
- Iestatiet noklusējuma prognozes modeļa ID, kas tiks izmantots, kad integrācija veidos jaunas stundu prognozes.
- Pārvērstu norēķinu veidus.
- Pārvērstu transakciju veidus.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrēt, lai iekļautu vienīgi izmaksu aprēķinu rindas

Projekta izmaksu aprēķinu (PSA uz Fin un Ops) veidnei ir noklusējuma filtrs, kas integrācijā iekļauj vienīgi izmaksu rindas. Ja izveidojat savu veidni, šis filtrs ir jāpievieno. Atlasiet uzdevumu **Transakciju relācijas** un pēc tam noklikšķiniet uz bulttaustiņa **Karte**, lai atvērtu kartējumu. Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti. Filtrējiet kolonnu **msdyn\_transactiontype1** tā, lai tā ietver vienīgi **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Iestatiet noklusējuma prognozes modeļa ID

Lai veidnē atjauninātu noklusējuma prognozes modeļa ID, atlasiet uzdevumu **Izmaksu aprēķini** un pēc tam noklikšķiniet uz bulttaustiņa **Karte**, lai atvērtu kartējumu. Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti.

- Ja izmantojat noklusējuma Projekta izmaksu aprēķinus (PSA uz Fin un Ops) veidni, Power Query sadaļā **Piemērojamās darbības** atlasiet pirmo **Ievietoto nosacījumu**. **Funkciju** ierakstā aizstājiet **O\_prognozi** ar tā prognozes modeļa ID, kuru vajadzētu izmantot ar integrāciju. Noklusējuma veidnei ir prognozes modeļa ID no demonstrācijas datiem.
- Ja izveidojat jaunu veidni, šī kolonna ir jāpievieno. Power Query atlasiet **Pievienot nosacījuma kolonnu** un ievadiet jaunās kolonnas nosaukumu, piemēram, **ModelID**. Ievadiet kolonnas nosacījumu, kur, ja novērtējuma rindas ID nav Null, tad \<enter the forecast model ID\>; pretējā gadījumā tas ir Null.

#### <a name="transform-the-billing-types"></a>Pārvērtiet norēķinu veidus

Projekta izmaksu aprēķinu (PSA uz Fin un Opc) veidne ietver nosacījuma kolonnu, kas tiek izmantota, lai pārvērstu norēķinu veidus, kuri integrēšanas laikā tiek saņemti no Project Service Automation. Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna. Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti un pēc tam atlasiet **Pievienot nosacījuma kolonnu**. Ievadiet jaunās kolonnas nosaukumu, piemēram, **NorēķinuTips**. Pēc tam ievadiet šādu nosacījumu:

Ja **msdyn\_billingtype** = 192350000, tad **NonChargeable**  
pretējā gadījumā, ja **msdyn\_billingtype** = 192350001, tad **Chargeable**  
pretējā gadījumā, ja **msdyn\_billingtype** = 192350002, tad **Complimentary**  
pretējā gadījumā **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Pārvērtiet transakciju veidus

Projekta izmaksu aprēķinu (PSA uz Fin un Opc) veidne ietver nosacījuma kolonnu, kas tiek izmantota, lai pārvērstu transakciju veidus, kuri integrēšanas laikā tiek saņemti no Project Service Automation. Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna. Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti un pēc tam atlasiet **Pievienot nosacījuma kolonnu**. Ievadiet jaunās kolonnas nosaukumu, piemēram, **TransactionType**. Pēc tam ievadiet šādu nosacījumu:

Ja **msdyn\_transactiontypecode** = 192350000, tad **Cost**  
pretējā gadījumā, ja **msdyn\_transactiontypecode** = 192350005, tad **Sales**  
pretējā gadījumā **tukšs**

### <a name="template-mapping-in-data-integration"></a>Veidņu kartēšana datu integrācijā

Nākamajās ilustrācijās ir redzami piemēri no veidnes uzdevumu kartējumiem datu integrācijā. Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.

[![Izmaksu novērtējuma transakciju veidnes kartēšana.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Izmaksu novērtējuma veidnes kartēšana.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]