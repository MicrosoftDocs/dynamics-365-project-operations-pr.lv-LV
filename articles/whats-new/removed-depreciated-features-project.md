---
title: Noņemti vai novecojuši līdzekļi Dynamics 365 Project Operations
description: Šajā tēmā aprakstīti līdzekļi, kas ir noņemti vai ko plānots noņemt no programmas Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601579"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Noņemti vai novecojuši līdzekļi Dynamics 365 Project Operations

_**Attiecas uz:** Project Operations scenārijiem, kas balstīti uz resursiem/bez krājumiem, Lite izvietošana — darbs ar pro forma rēķiniem un Project Operations scenārijiem, kas balstīti uz krājumiem/ražošanu_

Šajā tēmā aprakstīti līdzekļi, kas ir noņemti vai ko plānots noņemt no programmas Dynamics 365 Project Operations.

- *Noņemtais* līdzeklis vairs nav pieejams produktā.
- *Novecojis* līdzeklis nav aktīvā izstrādē, un to var noņemt turpmākā atjauninājumā.

Šis saraksts ir paredzēts, lai palīdzētu jums izvērtēt šos noņemtos un novecojušos līdzekļus saviem plāniem.

> [!NOTE]
> Detalizētu informāciju par objektiem finanšu un operāciju programmās var atrast tehnisko atsauču [**atskaitēs**](/dynamics/s-e/global/axtechrefrep_61). Varat salīdzināt dažādas šo atskaišu versijas, lai uzzinātu par objektiem, kas ir mainīti vai noņemti katrā finance and operations lietotņu versijā.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Līdzekļi, kas noņemti vai novecojuši projekta darbību 2022. gada marta laidienā

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projektu vadības un uzskaites parametrs "Vienmēr izveidot korekcijas darbību"

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Korekcijas darbības ir nepieciešamas audita vajadzībām. Pēc nolietojuma šis parametrs tiks paslēpts. Sistēma vienmēr izveidos korekcijas darbības, tāpat kā tas notiek pašlaik, kad parametrs ir iestatīts uz **Jā**. |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Projekta operācijas ražošanas/uzkrātajiem scenārijiem |
| **Statuss** | Novecojis: Līdz 2023. gada 1. martam mēs paslēpsim parametru un mainīsim sistēmas darbību, lai vienmēr tiktu izveidotas korekcijas darbības. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projekta vadības un uzskaites parametrs "Izmantot korekcijas datumu kā jaunu projekta datumu"

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Šis parametrs sākotnēji tika izmantots, lai atļautu korekcijas, kad finanšu periods tika aizvērts. Tomēr tas vairs nav nepieciešams, jo darbības uzskaites datumu var mainīt uz atvērtā perioda pirmo datumu, ja tas ir konfigurēts. Projekta datumu nedrīkst mainīt, jo tas norāda darbības rašanās datumu. |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Projekta operācijas ražošanas/uzkrātajiem scenārijiem |
| **Statuss** | Novecojis: Līdz 2023. gada 1. martam mēs paslēpsim parametru un mainīsim sistēmas darbību, lai korekcijas nekad nemainītu projekta datumu. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Resursu pieprasījuma darbplūsma projekta operācijās uzkrātajiem/ražošanas scenārijiem

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Novecojis zemā lietojuma un transakciju apjoma ierobežojumu dēļ. |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Projekta operācijas ražošanas/uzkrātajiem scenārijiem |
| **Statuss** | Novecojis: līdz 2023. gada 1. martam mēs atspējosim iespēju pieprasīt resursus projektam, izmantojot darbplūsmu. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projekta rēķina priekšlikuma lapa bez galvenes un rindu skatiem

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Novecojis, jo lapa, kas tika ieviesta kopā ar **priekšlikumu Lietot projekta rēķinu un rēķinu žurnāla formas ar skatu Virsraksts un rindas skatā**, ir uzlabota. |
| **Vai aizstāts ar citu līdzekli?** | Jā |
| **Ietekmētie produktu apgabali** | Programma |
| **Izvietošanas opcija** | Projekta operācijas ražošanas/uzkrātajiem scenārijiem; Projekta operācijas resursu/ neuzkrātiem scenārijiem |
| **Statuss** | Novecojis: līdz 2023. gada 1. martam mēs izslēgsim iepriekšējo (mantoto) lapu un pēc noklusējuma ieslēgsim **izmantot projekta rēķinu priekšlikumu un rēķinu žurnāla formas ar galvenes un rindu skata** funkciju atslēgu. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Līdzekļi, kas noņemti vai novecojuši projekta darbību 2021. gada decembra laidienā

### <a name="collaboration-workspaces"></a>Sadarbības darbvietas

[Sadarbības darbvietas izveide vai saite uz to (projekts)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Novecošanas/noņemšanas iemesls** | Novecojis zemā lietojuma dēļ. Klienti, kas izmanto projekta operācijas resursu/neuzkrātiem scenārijiem, var izmantot [sadarbību ar Office grupām](../project-management/collaboration-groups.md). |
| **Vai aizstāts ar citu līdzekli?** | Nē. |
| **Ietekmētie produktu apgabali** | Programma  |
| **Izvietošanas opcija** | Projekta operācijas ražošanas/uzkrātajiem scenārijiem |
| **Statuss** | Novecojis: līdz 2022. gada 1. decembrim mēs plānojam vairs neatbalstīt sadarbības darbvietas. |
