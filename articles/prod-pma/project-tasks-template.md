---
title: Sinhronizējiet projekta uzdevumus tieši no Project Service Automation uz finansēm un operācijām
description: Šajā rakstā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta uzdevumu sinhronizēšanai tieši no Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ed559fcd9e0e666f68e7d9f4f1fca91417fe4970
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028370"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sinhronizējiet projekta uzdevumus tieši no Project Service Automation uz finansēm un operācijām

[!include[banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta uzdevumu sinhronizēšanai tieši no Dynamics 365 Project Service Automation uz Dynamics 365 Finance.

> [!NOTE]
> - 8.0 versijā varat izmantot projekta uzdevumu integrāciju, izdevumu darbības kategorijas, stundu aprēķinus, izdevumu aprēķinus un funkcionalitātes bloķēšanu.
> - Ja izmantojat Enterprise edition 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu aprēķinus, izdevumu aprēķinus un faktiskos datus un konfigurēt funkcionalitātes bloķēšanu. Ja ir jāatiestata uzskaites sadales, ieteicams instalēt arī KB 4131710.
> - Faktisko datu integrācija ir pieejama 8.0.1 vai jaunākās versijās.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datu plūsma Project Service Automation uz Finance

Project Service Automation uz Finance integrācijas risinājumam tiek izmantots datu integrācijas līdzeklis, lai sinhronizētu datus starp Project Service Automation un Finance. Integrācijas veidne, kas ir pieejama kopā ar datu integrācijas līdzekli, iespējo datu plūsmu par projekta uzdevumiem no Project Service Automation uz Finance.

Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti starp Project Service Automation un Finance.

[![Datu plūsma Project Service Automation integrācijai ar Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Veidne un uzdevums

Lai piekļūtu veidnei, Microsoft Power Apps administrēšanas centrā atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskas veidnes.

Šajā tēmā ir aprakstīta veidne un pamata uzdevums, kas tiek izmantots projekta uzdevumu sinhronizēšanai tieši no Project Service Automation uz Finance:

- **Veidnes nosaukums datu integrācijā:** Projekta uzdevumi (PSA uz Fin un Ops)
- **Projekta uzdevuma nosaukums:** Projekta uzdevumi

Pirms projekta uzdevumu sinhronizēšanas, ir jāsinhronizē projekta līgumi un projekti.

## <a name="entity-set"></a>Entītiju kopa

| Project Service Automation | Finanses                             |
|----------------------------|-------------------------------------|
| Projekta uzdevumi              | Projekta uzdevuma integrācijas entītija |

## <a name="entity-flow"></a>Entītijas plūsma

Projekta uzdevumi tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta darbības.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartēšanas iestatīšana

Pirms projekta uzdevumu sinhronizēšanas, ir jāsinhronizē projekta līgumi un projekti.

## <a name="power-query"></a>Power Query

Ja ir izpildīts šis nosacījums, ir jāizmanto Power Query programmai Excel, lai filtrētu datus:

- Projekta uzdevumā ir resursam specifiski ieraksti.

Ja ir jāizmanto Power Query, ievērojiet šīs vadlīnijas:

- Projekta uzdevumu (PSA uz Fin un Ops) veidnei ir noklusējuma filtrs, kas projekta uzdevumam neietver resursu specifiskos ierakstus, iestatot filtru sadaļā **IsLineTask** uz **Aplams**. Ja izveidojat savu veidni, šis filtrs ir jāpievieno.

## <a name="template-mapping-in-data-integration"></a>Veidņu kartēšana datu integrācijā

Nākamajā ilustrācijā ir redzams piemērs no veidnes uzdevumu kartējumiem datu integrācijā. Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.

[![Veidņu kartēšana.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]