---
title: Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Project Operations
description: Šajā rakstā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Project Operations.
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
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Noņemtie vai novecojušie līdzekļi programmā Dynamics 365 Project Operations

_**Attiecas uz:** Project Operations scenārijiem, kas balstīti uz resursiem/bez krājumiem, Lite izvietošana — darbs ar pro forma rēķiniem un Project Operations scenārijiem, kas balstīti uz krājumiem/ražošanu_

Šajā rakstā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Dynamics 365 Project Operations.

- *Noņemtais* līdzeklis vairs nav pieejams produktā.
- *Novecojis* līdzeklis nav aktīvā izstrādē, un to var noņemt turpmākā atjauninājumā.

Šis saraksts ir paredzēts, lai palīdzētu jums izvērtēt šos noņemtos un novecojušos līdzekļus saviem plāniem.

> [!NOTE]
> Detalizēta informācija par finanšu un operāciju lietojumprogrammām ir pieejama tēmā [**Tehniskās atsauces pārskati**](/dynamics/s-e/global/axtechrefrep_61). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā finanšu un operāciju lietojumprogrammas versijā.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Līdzekļi, kas noņemti vai novecojuši Project Operations 2022. gada marta laidienā

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projekta pārvaldības un uzskaites parametrs "Vienmēr izveidot korekcijas transakciju"

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Korekcijas transakcijas ir vajadzīgas audita nolūkos. Pēc novecošanas šis parametrs būs paslēpts. Sistēma vienmēr izveidos transakciju ar strukturēšanas darbību, tāpat kā tas notiek pašlaik, kad parametrs ir iestatīts uz **Jā**. |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem |
| **Statuss** | Novecojis: līdz 2023. gada 1. martam mēs slēpsim parametru un mainīsim sistēmas darbību, lai vienmēr tiktu izveidotas korekciju transakcijas. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projekta pārvaldības un uzskaites parametrs "Lietot datuma pielāgošanu kā jaunu projekta datumu"

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Šo parametru sākotnēji izmantoja, lai atļautu pielāgojumus, kad tika slēgts finanšu periods. Taču tas vairs nav nepieciešams, jo transakcijas uzskaites datumu var mainīt uz atvērtā perioda pirmo datumu, ja tas ir konfigurēts. Projekta datumu nedrīkst mainīt, jo tas norāda transakcijas sākuma datumu. |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem |
| **Statuss** | Novecojis: līdz 2023. gada 1. martam mēs slēpsim parametru un mainīsim sistēmas darbību, lai korekcijām nekad netiktu mainīts projekta datums. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Resursu pieprasījuma darbplūsma Project Operations krājumu/ražošanas balstītiem scenārijiem

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Novecojis, jo ir zems lietojums un transakciju apjoma ierobežojumi. |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem |
| **Statuss** | Novecojis: līdz 2023. gada 1. martam, mēs atspējosim opciju pieprasīt projektam resursus, izmantojot darbplūsmu. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projekta rēķina piedāvājuma lapa bez galvenes un rindas skatiem

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Novecojis, jo tika veikti uzlabojumi lapai, kas tika ieviesti kopā ar līdzekļa atslēgu **Lietot Projekta rēķina priekšlikumu un rēķinu žurnālu veidlapas ar Galvenes un Rindas skatu**. |
| **Vai aizstāts ar citu līdzekli?** | Jā |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Project Operations ražošanas/krājumu scenārijiem: Project Operations resursu / ne krājumu scenārijiem |
| **Statuss** | Novecojis: līdz 2023. gada 1. martam tiks izslēgta iepriekšējā (mantotā) lapa un pēc noklusējuma tiks ieslēgta līdzekļu atslēga **Izmantot Projekta rēķinu priekšlikumu un rēķinu žurnālu veidlapas ar Galvenes un Rindu skatu**. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Līdzekļi, kas noņemti vai novecojuši Project Operations 2021. gada decembra laidienā

### <a name="collaboration-workspaces"></a>Sadarbības darbvietas

[Izveidojiet sadarbības darbvietu vai sniedziet saiti uz to (Projekts)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Novecojis, jo lietojums ir zems. Klienti, kas resursu/ne krājumu scenārijiem izmanto Project Operations, var izmantot [Sadarbību ar Office Groups](../project-management/collaboration-groups.md). |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma  |
| **Izvietošanas opcija** | Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem |
| **Statuss** | Novecojis: pēc 2022. gada 1. decembra vairs netiks atbalstītas sadarbības darbvietas. |
