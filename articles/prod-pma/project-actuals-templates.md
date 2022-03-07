---
title: Projekta faktisko datu sinhronizēšana tieši no Project Service Automation uz projekta integrācijas žurnālu publicēšanai Finance and Operations
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta faktisko datu sinhronizēšanai tieši no Microsoft Dynamics 365 Project Service Automation uz Finance and Operations.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85b6c07464e919e363f28d8bc62115e8fb4c72ea6631269b98fd00f324a01cba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988120"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Projekta faktisko datu sinhronizēšana tieši no Project Service Automation uz projekta integrācijas žurnālu publicēšanai Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta faktisko datu sinhronizēšanai tieši no Dynamics 365 Project Service Automation uz Dynamics 365 Finance.

Veidne sinhronizē transakcijas no Project Service Automation uz izstādīšanas tabulu risinājumā Finance. Kad sinhronizācija ir pabeigta, jums **jāimportē** dati no izstādīšanas tabulas integrācijas žurnālā.

> [!NOTE]
> - Projekta faktisko datu integrācija ir pieejama, sākot ar versiju 8.0.1.
> - Ja izmantojat Enterprise edition 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu aprēķinus, izdevumu aprēķinus un faktiskos datus un konfigurēt funkcionalitātes bloķēšanu. Ja ir jāatiestata uzskaites sadales, ieteicams instalēt arī KB 4131710.
> - Ja izmantojat versiju 7.3.0 un no Project Service Automation ir jāievieš maksas transakcijas, jums ir jāinstalē KB 4345320, lai projekta rēķinā iekļautu šīs maksas.
> - Ja ievadāt PVN summas laika vai izdevumu transakcijās Project Service Automation, ir jāinstalē Project Service Automation 7. atjauninājums. Pretējā gadījumā nodokļu faktiskie dati netiks saistīti ar saistītajiem laika vai izdevumu faktiskajiem datiem, un tie netiks sinhronizēti ar Finance. Lai iegūtu papildinformāciju, sazinieties ar atbalsta dienestu.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datu plūsma Project Service Automation uz Finance

Project Service Automation uz Finance integrācijas risinājumam tiek izmantots datu integrācijas līdzeklis, lai sinhronizētu datus starp Project Service Automation un Finance. Integrācijas veidnes, kas ir pieejamas kopā ar datu integrācijas līdzekli, iespējo datu plūsmu par projekta faktiskajiem datiem no Project Service Automation uz Finance.

Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti starp Project Service Automation un Finance.

[![Datu plūsma Project Service Automation integrācijai ar Finance and Operations.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projekta faktiskie dati no Project Service Automation

### <a name="template-and-tasks"></a>Veidne un uzdevumi

Lai piekļūtu pieejamajām veidnēm, Microsoft Power Apps administrēšanas centrā atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskas veidnes.

Šajā tēmā ir aprakstīta veidne un pamata uzdevumi, kas tiek izmantoti projekta faktisko datu sinhronizēšanai tieši no Project Service Automation uz Finance:

- **Veidnes nosaukums datu integrācijā:** Projekta faktiskie dati (PSA uz Fin un Ops)
- **Projekta uzdevumu nosaukums:**

    - Faktiskās vērtības
    - TransactionConnections

### <a name="entity-set"></a>Entītiju kopa

| Project Service Automation | Finanses                                   |
|----------------------------|----------------------------------------------------------|
| Faktiskās vērtības                    | Projekta faktisko datu integrācijas entītija                   |
| Transakcijas savienojumi    | Integrāciju entitīja projekta transakciju relācijām |

### <a name="entity-flow"></a>Entītijas plūsma

Projekta faktiskie dati tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti ar projekta integrācijas žurnālu risinājumā Finance. Uzskaite tiks izmantota, pamatojoties uz noklusējuma finanšu dimensijām un publicēšanas iestatījumiem.

### <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu sinhronizēt faktiskos datus, ir jākonfigurē Project Service Automation integrācijas parametri un jāsinhronizē projektu, projektu uzdevumu un projektu izdevumu transakciju kategorijas.

### <a name="power-query"></a>Power Query

Projekta faktisko datu veidnē ir jāizmanto Microsoft Power Query for Excel, lai izpildītu šos uzdevumus:

- Pārvērtiet transakcijas tipu risinājumā Project Service Automation  uz pareizo transakcijas tipu Finance. Šī transformācija jau ir definēta projekta faktisko datu atjaunināšanas (PSA uz Fin un Ops) veidnē.
- Pārvērtiet norēķinu tipu risinājumā Project Service Automation uz pareizo norēķinu tipu Finance. Šī transformācija jau ir definēta projekta faktisko datu atjaunināšanas (PSA uz Fin un Ops) veidnē. Norēķinu tips pēc tam tiek kartēts uz rindas rekvizītu, pamatojoties uz lapas **Project Service Automation integrācijas parametri** konfigurāciju.
- Filtrējiet ar noteiktām resursu organizācijas struktūrvienībām, kas ir jāsinhronizē ar šo veidni.
- Ja starpuzņēmumu laika vai starpuzņēmumu izdevumu faktiskie dati tiek sinhronizēti ar Finance, līguma organizācijas struktūrvienība ir jātransformē pareizajā juridiskajā personā risinājumā Finance. Projekta faktisko datu (PSA uz Fin un Ops) veidnē nosacījuma kolonna tiek definēta, pamatojoties uz demonstrācijas datiem. Pēdējā ievietotā nosacījuma kolonna ir jāatjaunina ar pareizajām juridiskajām personām. Pretējā gadījumā var rasties integrācijas kļūda, vai arī uz Finance var tikt importētas nepareizas faktiskās transakcijas.
- Ja starpuzņēmumu laika vai starpuzņēmumu izmaksu faktiskie dati netiks sinhronizēti ar Finance, no veidnes ir jāizdzēš pēdējā ievietotā nosacījuma kolonna. Pretējā gadījumā var rasties integrācijas kļūda, vai arī uz Finance var tikt importētas nepareizas faktiskās transakcijas.

#### <a name="contract-organizational-unit"></a>Līguma uzņēmuma vienība
Lai veidnē atjauninātu ievietoto nosacījuma kolonnu, noklikšķiniet uz bultiņas **Karte**, lai atvērtu kartējumu. Atlasiet **Detalizēto vaicājumu un filtrēšanas** saiti, lai atvērtu Power Query.

- Ja izmantojat noklusējuma Projekta faktisko datu (PSA uz Fin un Ops) veidni, Power Query sadaļā **Piemērojamās darbības** atlasiet pēdējo **Ievietoto nosacījumu**. Ierakstā **Funkcija** aizstājiet **USSI** ar tās juridiskās personas nosaukumu, kuru vajadzētu izmantot ar integrāciju. Pievienojiet ierakstam **Funkcija** papildu nosacījumus, kad tas ir nepieciešams, un atjauniniet **USMF** nosacījumu **cits** uz pareizo juridisko personu.
- Ja izveidojat jaunu veidni, šī kolonna ir jāpievieno, lai atbalstītu starpuzņēmumu laiku un izdevumus. Atlasiet **Pievienot nosacījuma kolonnu** un ievadiet kolonnas nosaukumu, piemēram, **JuridiskaPersona**. Ievadiet kolonnas nosacījumu, kur, ja **msdyn\_contractorganizationalunitid.msdyn\_nosaukums** ir \<organizational unit\>, tad \<enter the legal entity\>; pretējā gadījumā tas ir Null.

### <a name="template-mapping-in-data-integration"></a>Veidņu kartēšana datu integrācijā

Nākamajās ilustrācijās ir redzams piemērs no veidnes uzdevumu kartējuma datu integrācijā. Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.

[![Veidņu kartēšana — faktiskie dati.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Veidņu kartēšana — transakciju savienojumi.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importēšana no izstādīšanas tabulas pēc integrēšanas no Project Service Automation

Periodiskā importēšana no izstādīšanas tabulas ir jāveic pēc faktisko datu sinhronizācijas no Project Service Automation uz Finance. Šis process importē projekta transakcijas no izstādīšanas tabulas uz Project Service Automation integrācijas žurnālu, kur tiek lietota uzskaite un var publicēt importētās transakcijas. Šo procesu ieteicams izpildīt sērijveida režīmā; var iestatīt, lai to palaistu kā periodisku paketi.

## <a name="update-actuals-from-finance"></a>Faktisko datu atjaunināšana no Finance

### <a name="template-and-tasks"></a>Veidne un uzdevumi

Tālāk norādītā veidne un tās pakārtotie uzdevumi tiek lietoti, lai sinhronizētu publicēto projekta transakciju dokumenta numuru un PVN no Finance uz Project Service Automation:

- **Veidnes nosaukums datu integrācijā:** Projekta faktisko datu atjauninājums (Fin Ops uz PSA)
- **Projekta uzdevumu nosaukums:**

    - Faktiskās vērtības 
    - TransactionConnections

### <a name="entity-set"></a>Entītiju kopa

| Finanses                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Projekta faktisko datu integrācijas entītija                   | Faktiskās vērtības                    |
| Integrāciju entitīja projekta transakciju relācijām | Transakcijas savienojumi    |

### <a name="entity-flow"></a>Entītijas plūsma

Projekta faktiskie dati tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti ar projekta integrācijas žurnālu risinājumā Finance. Kad faktiskie dati ir publicēti risinājumā Finance, tie tiek atjaunināti Project Service Automation, norādot dokumenta numuru no Finance. Ja risinājumā Finance tiek pievienots PVN, Project Service Automation tiek izveidoti jauni nodokļu faktiskie dati.

### <a name="power-query"></a>Power Query

Projekta faktisko datu atjaunināšanas veidnē ir jāizmanto Power Query, lai izpildītu šos uzdevumus:

- Pārvērtiet transakcijas tipu risinājumā Finance uz pareizo transakcijas tipu Project Service Automation. Šī transformācija jau ir definēta projekta faktisko datu atjaunināšanas (Fin Ops uz PSA) veidnē.
- Pārvērtiet norēķinu tipu risinājumā Finance uz pareizo norēķinu tipu Project Service Automation. Šī transformācija jau ir definēta projekta faktisko datu atjaunināšanas (Fin Ops uz PSA) veidnē.

### <a name="template-mapping-in-data-integration"></a>Veidņu kartēšana datu integrācijā

Nākamajās ilustrācijās ir redzami piemēri no veidnes uzdevumu kartējumiem datu integrācijā. Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Finance uz Project Service Automation.

[![Veidņu kartēšana — faktisko datu atjauninājums.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Veidņu kartēšana — transakciju atjauninājums.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]