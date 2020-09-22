---
title: Projekta izdevumu kategoriju sinhronizēšana starp Finance and Operations un Project Service Automation
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta izdevumu kategoriju sinhronizēšanai starp Microsoft Dynamics 365 Finance un Dynamics 365 Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 7dd914dc-1913-45eb-8a67-e897b00089fa
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 757fe1dbc804b986fc3334ebae7254a3f0491f59
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753514"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projekta izdevumu kategoriju sinhronizēšana starp Finance and Operations un Project Service Automation

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta izdevumu kategoriju sinhronizēšanai starp Dynamics 365 Finance un Dynamics 365 Project Service Automation.

> [!NOTE]
> - 8.0 versijā varat izmantot projekta uzdevumu integrāciju, izdevumu darbības kategorijas, stundu aprēķinus, izdevumu aprēķinus un funkcionalitātes bloķēšanu.
> - Faktisko datu integrācija ir pieejama 8.0.1 vai jaunākās versijās.
> - Ja izmantojat Enterprise edition 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu aprēķinus, izdevumu aprēķinus un faktiskos datus un konfigurēt funkcionalitātes bloķēšanu. Ja ir jāatiestata uzskaites sadales, ieteicams instalēt arī KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Datu plūsma Project Service Automation un Finance

Project Service Automation un Finance integrācijas risinājumam tiek izmantots datu integrācijas līdzeklis, lai sinhronizētu datus starp Project Service Automation un Finance. Integrācijas veidnes, kas ir pieejamas kopā ar datu integrācijas līdzekli, iespējo datu plūsmu par projekta izdevumu transakciju kategorijām starp Finance un Project Service Automation.

Ja projekta izmaksu kategorijas ir apstrādātas risinājumā Finance, integrācijas plūsma vispirms ir no Finance uz Project Service Automation. Projekta izmaksu kategoriju integrācijas ID pēc tam tiek atjaunināti, izmantojot sinhronizāciju no Project Service Automation uz Finance.

Ja projekta izmaksu kategorijas ir apstrādātas risinājumā Project Service Automation, integrācijas plūsma vispirms ir no Project Service Automation uz Finance. Lai varētu veikt sinhronizāciju no Project Service Automation, projekta kategorijām jau ir jābūt konfigurētām Finance. Pēc tam sinhronizējiet no Finance atpakaļ uz Project Service Automation un pēc tam vēlreiz no Project Service Automation uz Finance. Šādi tiek nodrošināta garantija, ka kategorijas ir saistītas un netiek izveidoti dublikāti.

> [!NOTE]
> Parasti projekta izmaksu kategorijas tiek apstrādātas risinājumā Finance. Tomēr, ja tā nav vai ja izdevumu kategorijas jau ir izveidotas Project Service Automation, vispirms ir jāsinhronizē, izmantojot projekta izdevumu transakciju kategoriju (PSA uz Fin un OPS) veidne. Pēc tam veiciet sinhronizēšanu, izmantojot projekta izdevumu transakciju kategoriju (Fin un Ops uz PSA) veidni. Pēc tam ir jāsinhronizē no Project Service Automation uz Finance vēl vienu reizi.
>
> Ja vispirms tiek sinhronizēts no Project Service Automation, pirms sinhronizācijas izpildes risinājumā Finance ir jāizpilda šādas prasības:
>
> - Ir jāpastāv koplietojamai kategorijai, kas atbilst Project Service Automation iestatītajai projekta kategorijai, un tai ir jābūt iespējotai gan **Projekts**, gan **Izdevumi**.
> - Attiecībā uz katru Finance juridisko personu, kas ir jāintegrē, ir jāpastāv šādām projekta kategorijām:
>
>     - Pastāv **Projekta kategorija**. 
>     - Ir iespējota opcija **Lietot izdevumiem**.
>     - Ir iespējota opcija **Aktīvs žurnālā**.
>     - **Transakcijas tips** ir iestatīts uz **Izdevumi**.

Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti starp Project Service Automation un Finance.

[![Datu plūsma Project Service Automation integrācijai ar Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Projekta izdevumu kategoriju sinhronizēšana no Finance uz Project Service Automation

### <a name="template-and-task"></a>Veidne un uzdevums

Lai piekļūtu veidnei, Microsoft Power Apps administrēšanas centrā atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskas veidnes.

Lai sinhronizētu projekta izmaksu kategorijas no Finance uz Project Service Automation, tiek izmantota šāda veidne un pamata uzdevums:

- **Veidnes nosaukums datu integrācijā:** Projekta izmaksu transakciju kategorijas (Fin un Ops uz PSA)
- **Uzdevuma nosaukums projektā:** Kategoriju sinhronizācija uz PSA

### <a name="entity-set"></a>Entītiju kopa

| Finanses                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Kategoriju integrācijas entītija | Transakcijas kategorijas     |

### <a name="entity-flow"></a>Entītijas plūsma

Projekta izdevumu kategorijas tiek pārvaldītas pakalpojumā Finance, un tās tiek sinhronizētas uz Project Service Automation kā transakciju kategorijas.

### <a name="power-query"></a>Power Query

Kad veicat sinhronizēšanu uz Project Service Automation, ir jāizmanto Microsoft Power Query programmai Excel, lai transakciju kategorijā iestatītu norēķinu tipu. Projekta izdevumu transakciju kategoriju (Fin un Ops uz PSA) veidne nodrošina noklusējuma kolonnu un kartēšanu. Ja izveidojat savu veidni, ir jāpievieno nosacījuma kolonna, izmantojot Power Query. Veiciet tālāk norādītās darbības.

1. Noklikšķiniet uz bultiņas, lai atvērtu projekta izdevumu kategoriju uzdevuma kartējumu projekta izdevumu transakciju kategoriju (Fin un Ops uz PSA) veidnē.
2. Noklikšķiniet uz **Detalizēto vaicājumu un filtrēšanas** saites, lai atvērtu Power Query.
2. Atlasiet **Pievienot nosacījuma kolonnu**.
3. Ievadiet jaunās kolonnas nosaukumu, piemēram, **NorēķinuTips**.
4. Ievadiet šādu nosacījumu:Ievadiet šādu nosacījumu: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Kolonnā noklikšķiniet uz **Labi**.
6. Noteikti kartējiet šo jauno kolonnu kartēšanas lapā.

Nākamajā ilustrācijā ir redzams piemērs no veidnes uzdevumu kartējuma datu integrācijā. Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Finance uz Project Service Automation.

[![Veidņu kartēšana](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Projekta izdevumu kategoriju sinhronizēšana no Project Service Automation uz Finance

### <a name="template-and-task"></a>Veidne un uzdevums

Lai sinhronizētu projekta izmaksu kategorijas no Project Service Automation uz Finance, tiek izmantota šāda veidne un pamata uzdevums:

- **Veidnes nosaukums datu integrācijā:** Projekta izmaksu transakciju kategorijas (PSA uz Fin un Ops)
- **Uzdevuma nosaukums projektā:** Kategoriju sinhronizācija uz Fin Ops

### <a name="entity-set"></a>Entītiju kopa

| Project Service Automation | Finanses                           |
|----------------------------|-----------------------------------|
| Transakcijas kategorijas     | Kategoriju integrācijas entītija |

### <a name="entity-flow"></a>Entītijas plūsma

Projekta izdevumu kategorijas tiek pārvaldītas pakalpojumā Finance, un tās tiek sinhronizētas uz Project Service Automation kā transakciju kategorijas. Sinhronizācija atpakaļ uz Finance atjaunina projekta kategoriju pakalpojumā Finance ar integrācijas ID no Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Veidņu kartēšana datu integrācijā

Nākamajā ilustrācijā ir redzams piemērs no veidnes uzdevumu kartējuma datu integrācijā.

> [!NOTE]
> Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.

[![Veidņu kartēšana](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
