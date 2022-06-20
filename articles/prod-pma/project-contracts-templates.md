---
title: Sinhronizējiet projekta līgumus un projektus tieši no Project Service Automation uz Finance
description: Šajā rakstā ir aprakstīta veidne un pamatā esošie uzdevumi, kas tiek izmantoti, lai sinhronizētu projektu līgumus un projektus tieši no Microsoft Dynamics 365 Project Service Automation Dynamics 365 Finance.
author: Yowelle
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 62a24f3af823d474cbb4d63f8d079c708256a75e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933869"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Sinhronizējiet projekta līgumus un projektus tieši no Project Service Automation uz Finance 

[!include[banner](../includes/banner.md)]



Šajā rakstā ir aprakstīta veidne un pamatā esošie uzdevumi, kas tiek izmantoti, lai sinhronizētu projektu līgumus un projektus tieši no Dynamics 365 Project Service Automation Dynamics 365 Finance.

> [!NOTE] 
> Ja izmantojat Enterprise edition 7.3.0, ir jāinstalē KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datu plūsma Project Service Automation uz Finance

> [!NOTE]
> Lai varētu izmantot Project Service Automation uz Finance integrācijas risinājumu, ir jāpārzina Dynamics 365 datu integrācijas līdzeklis.

Project Service Automation uz Finance integrācijas risinājumam tiek izmantots datu integrācijas līdzeklis, lai sinhronizētu datus starp Project Service Automation un Finance. Integrēšanas veidne, kas ir pieejama ar datu integrācijas līdzekli, iespējo datu plūsmu par projektu līgumiem, projektiem, projekta līguma rindām un projekta līgumu rindu atskaites punktiem no Project Service Automation uz Finance.

Nākamajā ilustrācijā parādīts, kā dati tiek sinhronizēti starp Project Service Automation un Finance.

[![Datu plūsma Project Service Automation integrācijai ar Finance.](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, Microsoft Power Apps administrēšanas centrā atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskas veidnes.

Lai sinhronizētu projekta līgumus un projektus no Project Service Automation uz Finance, tiek izmantotas šādas veidnes un pamata uzdevumi:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrēšana ar Dynamics 365 Project Service Automation v2.x
- **Veidnes nosaukums datu integrēšanā:** Projekti un līgumi (no Project Service Automation uz Finance)
- **Projekta uzdevumu nosaukums:**

    - Projekta līgumi no Project Service Automation uz Finance
    - Projekti no Project Service Automation uz Finance
    - Projekta līguma rindas no Project Service Automation uz Finance
    - Projekta līguma rindas atskaites punkti no Project Service Automation uz Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrēšana ar Dynamics 365 Project Service Automation v3.x
Project Service Automation ir shēmas izmaiņas, kas ietekmē projekta līguma rindu atskaites punktu veidni, un Project Service Automation v3.x integrēšanai ar Dynamics 365 nepieciešams izmantot veidnes v2 versiju.

- **Veidnes nosaukums datu integrēšanā:** Projekti un līgumi (no Project Service Automation 3.x uz Finance) - v2
- **Projekta uzdevumu nosaukums:**

    - Projekta līgumi no Project Service Automation uz Finance
    - Projekti no Project Service Automation uz Finance
    - Projekta līguma rindas no Project Service Automation uz Finance
    - Projekta līguma rindas atskaites punkti no Project Service Automation uz Finance

Pirms projekta līgumu un projektu sinhronizēšanas ir jāsinhronizē uzņēmumi.

## <a name="entity-set"></a>Entītiju kopa

| Project Service Automation       | Finanses                                                |
|----------------------------------|--------------------------------------------------------|
| Pasūtījumi                           | Projekta līguma integrācijas entītija                |
| Projekti                         | Projekta integrācijas entītija                         |
| Pasūtījuma rindas                      | Projekta līguma rindas integrācijas entītija           |
| Projekta līguma rindas atskaites punkti | Projekta līguma rindas atskaites punkta integrācijas entītija |

## <a name="entity-flow"></a>Entītijas plūsma

Projekta līgumi tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta līgumi. Kā integrācijas veidnes daļu risinājumā Finance var iestatīt integrācijas avotu projekta līgumam.

Laika un materiālu un fiksētās cenas projektus pārvalda programmā Project Service Automation un sinhronizē uz Finance kā projektus. Kā daļu no veidņu integrācijas varat iestatīt integrācijas avotu Finance projektam. Pašlaik tiek atbalstīti vienīgi laika un materiālu un fiksētas cenas projekti.


Projekta līgumu rindas tiek pārvaldītas pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta līgumu norēķinu kārtulas. Ja norēķinu metode atšķiras no noklusējuma projekta tipa, sinhronizācija atjaunina projekta tipu līguma rindas projektam un projekta grupai.

Projekta līgumu rindas atskaites punkti tiek pārvaldīti pakalpojumā Project Service Automation, un tie tiek sinhronizēti uz Finance kā projekta līgumu norēķinu kārtulu atskaites punkti.

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation uz Finance integrācijas risinājums

Lauks **Projekta līguma ID** ir pieejams lapā **Projekta līgumi**. Šis lauks ir padarīts par dabisku un unikālu integrācijas atbalsta atslēgu.

Kad tiek izveidots jauns projekta līgums, ja vērtība **Projekta līguma ID** vēl nepastāv, tā tiek automātiski ģenerēta, izmantojot numuru sēriju. Vērtība sastāv no **ORD** un pēc tam no pieaugušas skaitļu secības, un pēc tam no sešu rakstzīmju sufiksa. Lūk, piemērs: **ORD-01022-Z4M9Q0**.

Lauks **Projekta numurs** ir pieejams lapā **Projekti**. Šis lauks ir padarīts par dabisku un unikālu integrācijas atbalsta atslēgu.

Kad tiek izveidots jauns projekts, ja vērtība **Projekta numurs** vēl nepastāv, tā tiek automātiski ģenerēta, izmantojot numuru sēriju. Vērtība sastāv no **PRJ** un pēc tam no pieaugušas skaitļu secības, un pēc tam no sešu rakstzīmju sufiksa. Lūk, piemērs: **PRJ-01049-CCNID0**.

Kad tiek lietots Project Service Automation uz Finance integrācijas risinājums, jaunināšanas skripts iestata lauku **Projekta līguma ID** esošiem projekta līgumiem un lauku **Projekta numurs** esošiem projektiem Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartēšanas iestatīšana

- Pirms projekta līgumu un projektu sinhronizēšanas ir jāsinhronizē uzņēmumi.
- Savienojuma kopā pievienojiet integrācijas atslēgas lauka kartējumu **msdyn\_organizationalunits** uz **msdyn\_name \[Name\]**. Iespējams, ka savienojuma kopai vispirms ir jāpievieno projekts. Papildinformāciju skatiet rakstā [Datu integrācija pakalpojumā Common Data Service programmām](/powerapps/administrator/data-integrator).
- Savienojuma kopā pievienojiet integrācijas atslēgas lauka kartējumu **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**. Iespējams, ka savienojuma kopai vispirms ir jāpievieno projekts. Papildinformāciju skatiet rakstā [Datu integrācija pakalpojumā Common Data Service programmām](/powerapps/administrator/data-integrator).
- **SourceDataID** projektu līgumiem un projektiem var atjaunināt uz citu vērtību vai noņemt no kartējuma. Noklusējuma veidnes vērtība ir **Project Service Automation**.
- **PaymentTerms** kartējums ir jāatjaunina, lai tas atspoguļotu derīgus maksājuma nosacījumus risinājumā Finance. Varat arī noņemt kartējumu no projekta uzdevuma. Noklusējuma vērtību kartē ir demonstrācijas datu noklusējuma vērtības. Nākamajā tabulā ir parādītas Project Service Automation vērtības.

    | vērtība | Apraksts   |
    |-------|---------------|
    | 1     | Apmaksa pēc 30 dienām        |
    | 2     | Apmaksa pēc 30 dienām ar 2% atlaidi, ja apmaksa veic 10 dienu laikā |
    | 3     | Apmaksa pēc 45 dienām        |
    | 4     | Apmaksa pēc 60 dienām        |

## <a name="power-query"></a>Power Query

Izmantojiet Microsoft programmai Excel Power Query, lai filtrētu datus, ja ir izpildīti šādi nosacījumi:

- Jums ir pārdošanas pasūtījumi risinājumā Dynamics 365 Sales.
- Jums ir vairākas organizācijas struktūrvienības Project Service Automation, un šīs organizācijas struktūrvienības tiks kartētas uz vairākām juridiskām personām risinājumā Finance.

Ja jums ir nepieciešams izmantot Power Query, ievērojiet šīs vadlīnijas:

- Projektu un līgumu (PSA uz Fin un Ops) veidnei ir noklusējuma filtrs, kas ietver tikai pārdošanas pasūtījumus ar tipu **Darba vienums (msdyn\_ordertype = 192350001)**. Šis filtrs palīdz nodrošināt, lai projekta līgumi netiktu izveidoti pārdošanas pasūtījumiem risinājumā Finance. Ja izveidojat savu veidni, šis filtrs ir jāpievieno.
- Power Query Izveidojiet filtru, kurā iekļautas tikai tās līguma organizācijas, kas jāsinhronizē ar integrācijas savienojumu kopas juridisko personu. Piemēram, projekta līgumi, kas jums ir ar līguma organizācijas struktūrvienību Contoso US, ir jāsinhronizē ar USSI juridisko personu, bet projekta līgumi, kas jums ir ar organizācijas struktūrvienību Contoso Global, ir jāsinhronizē ar USMF juridisko personu. Ja nepievienosit šo filtru jūsu uzdevumu kartējumam, visi projekta līgumi tiks sinhronizēti ar juridisko personu, kas ir definēta savienojuma kopai, neatkarīgi no līguma organizācijas struktūrvienības.

## <a name="template-mapping-in-data-integration"></a>Veidņu kartēšana datu integrācijā

> [!NOTE] 
> Lauki **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** un **AddressZipCode** nav iekļauti projektu līgumu noklusējuma kartējumā. Varat pievienot kartējumus, ja jums nepieciešams, lai šie dati tiktu sinhronizēti projekta līgumiem.
>
> Lauki **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** un **ProjectType** nav iekļauti projektu noklusējuma kartējumā Varat pievienot kartējumus, ja jums nepieciešams, lai šie dati tiktu sinhronizēti projektiem.

Nākamajās ilustrācijās ir redzami piemēri no veidnes uzdevumu kartējumiem datu integrācijā. Kartējumā tiek parādīta lauka informācija, kas tiks sinhronizēta no Project Service Automation uz Finance.

[![Projekta līguma veidnes kartēšana.](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Projekta veidnes kartēšana.](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Projekta līguma rindu veidnes kartēšana.](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Projekta līguma rindu atskaites punkta veidnes kartēšana.](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Projekta līguma rindu atskaites punktu kartēšana projektos un līgumos (PSA 3.x uz Dynamics) — v2 veidne:

[![Projekta līguma rindu atskaites punkta kartēšana ar versiju, kurā ir divas veidnes.](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]