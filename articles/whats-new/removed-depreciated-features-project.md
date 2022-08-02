---
title: Noņemtie vai novecojušie līdzekļi Dynamics 365 Project Operations
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir noņemti vai kurus ir plānots noņemt no Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028338"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Noņemtie vai novecojušie līdzekļi Dynamics 365 Project Operations

_**Attiecas uz:** Project Operations scenārijiem, kas balstīti uz resursiem/bez krājumiem, Lite izvietošana — darbs ar pro forma rēķiniem un Project Operations scenārijiem, kas balstīti uz krājumiem/ražošanu_

Šajā rakstā ir aprakstīti līdzekļi, kas ir noņemti vai kurus ir plānots noņemt no Dynamics 365 Project Operations.

- *Noņemtais* līdzeklis vairs nav pieejams produktā.
- *Novecojis* līdzeklis nav aktīvā izstrādē, un to var noņemt turpmākā atjauninājumā.

Šis saraksts ir paredzēts, lai palīdzētu jums izvērtēt šos noņemtos un novecojušos līdzekļus saviem plāniem.

> [!NOTE]
> Detalizētu informāciju par objektiem finanšu un operāciju lietotnēs var atrast [**tehnisko uzziņu atskaitēs**](/dynamics/s-e/global/axtechrefrep_61). Varat salīdzināt šo pārskatu dažādās versijas, lai uzzinātu par objektiem, kas ir mainīti vai noņemti katrā finanšu un operāciju programmu versijā.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Līdzekļi, kas noņemti vai novecojuši Project Operations 2022. gada marta laidienā

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projekta vadības un grāmatvedības parametrs "Vienmēr izveidojiet korekcijas transakciju"

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Korekcijas darījumi ir nepieciešami revīzijas vajadzībām. Pēc novecošanas šis parametrs tiks paslēpts. Sistēma vienmēr izveidos korekcijas transakcijas, tāpat kā tā pašlaik, kad parametrs ir iestatīts uz **Jā**. |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Projektu operācijas ražošanas/krājumu scenārijiem |
| **Statuss** | Novecojis: līdz 2023. gada 1. martam mēs paslēpsim parametru un mainīsim sistēmas darbību, lai vienmēr tiktu izveidotas korekcijas transakcijas. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projekta vadības un uzskaites parametrs "Izmantot koriģēšanas datumu kā jaunu projekta datumu"

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Šis parametrs sākotnēji tika izmantots, lai varētu veikt korekcijas, kad finanšu periods tika aizvērts. Tomēr tas vairs nav nepieciešams, jo transakcijas uzskaites datumu var mainīt uz atvērtā perioda pirmo datumu, ja tas ir konfigurēts. Projekta datumu nedrīkst mainīt, jo tas norāda datumu, kad notika transakcija. |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Projektu operācijas ražošanas/krājumu scenārijiem |
| **Statuss** | Novecojis: līdz 2023. gada 1. martam mēs paslēpsim parametru un mainīsim sistēmas uzvedību, lai projekta datums nekad netiktu mainīts, veicot korekcijas. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Resursu pieprasījuma darbplūsma project operations krājumos/ražošanas scenārijos

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Novecojis zema lietojuma un transakciju apjoma ierobežojumu dēļ. |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Projektu operācijas ražošanas/krājumu scenārijiem |
| **Statuss** | Novecojis: līdz 2023. gada 1. martam mēs atspējosim iespēju pieprasīt resursus projektam, izmantojot darbplūsmu. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projekta rēķina priekšlikuma lapa bez galvenes un līniju skatiem

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Novecojis, jo ir veikti uzlabojumi lapā, kas tika ieviesta kopā ar **priekšlikumu Izmantot projekta rēķinu un rēķinu žurnāla veidlapām ar galvenes un līniju skata** līdzekļa atslēgu. |
| **Vai aizstāts ar citu līdzekli?** | Jā |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Projekta operācijas ražošanas/krājumu scenārijiem; Projekta operācijas resursu/ nesakārtotiem scenārijiem |
| **Statuss** | Novecojis: līdz 2023. gada 1. martam mēs izslēgsim iepriekšējo (mantoto) lapu un ieslēgsim **priekšlikumu Izmantot projekta rēķinu un rēķinu žurnāla veidlapas ar galvenes un līniju skata** līdzekļa atslēgu pēc noklusējuma. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Līdzekļi, kas noņemti vai novecojuši project operations 2021. gada decembra laidienā

### <a name="collaboration-workspaces"></a>Sadarbības darbvietas

[Sadarbības darbvietas izveide vai saistīšana ar to (Project)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Novecojis zema lietojuma dēļ. Klienti, kas izmanto Project Operations resursos/nekrātos scenārijos, var izmantot [sadarbību ar Office grupām](../project-management/collaboration-groups.md). |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma  |
| **Izvietošanas opcija** | Projektu operācijas ražošanas/krājumu scenārijiem |
| **Statuss** | Novecojis: līdz 2022. gada 1. decembrim mēs plānojam vairs neatbalstīt sadarbības darbvietas. |
