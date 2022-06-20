---
title: Projekta aprēķinu un faktisko datu integrācija
description: Šajā rakstā sniegta informācija par projektu operāciju divējādo rakstīšanas integrāciju projektu aplēsēm un faktiskajiem datiem.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914595"
---
# <a name="project-estimates-and-actuals-integration"></a>Projekta aprēķinu un faktisko datu integrācija

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā rakstā sniegta informācija par projektu operāciju divējādo rakstīšanas integrāciju projektu aplēsēm un faktiskajiem datiem.

## <a name="project-estimates"></a>Projekta aprēķins

Projekta darbaspēka, izdevumu un materiālu novērtējumi tiek izveidoti un uzturēti Microsoft Dataverse un sinhronizēti ar finanšu un operāciju programmām grāmatvedības vajadzībām. Darbības izveide, atjaunināšana un dzēšana netiek atbalstītas, izmantojot finanšu un operāciju programmas.

Lai izveidotu aprēķinus, projektam ir nepieciešama derīga grāmatvedības konfigurācija. Ar līguma rindām saistītajiem projektiem ir jābūt derīgam projekta izmaksu un ieņēmumu profilam, kas definēts projekta izmaksu un ieņēmumu profila kārtulās. Papildinformāciju skatiet rakstā [Apmaksājamo projektu uzskaites konfigurēšana](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Darba aprēķini

Darba aprēķinus izveido projekta vadītājs vai resursu vadītājs, kurš projekta uzdevumam piešķir arī vispārēju vai nosauktu resursu. Resursu piešķiršanas ierakstus var pārskatīt cilnē **Resursu norīkojumi** Dataverse lapā **Detalizēta informācija par projektu**. Resursu piešķiršanas ieraksti Dataverse, veidojot stundu budžeta ierakstus finanšu un operāciju programmās, izmantojot **projektu operāciju integrācijas entītiju stundu aprēķiniem (msdyn\_ resourceassignments)**.

   ![Darba aprēķinu integrācija.](./Media/DW4LaborEstimates.png)

Duālā rakstīšana sinhronizē resursu piešķiršanas ierakstus ar izstādīšanas tabulu (**ProjCDSEstimateHoursImport**) un pēc tam izmanto biznesa loģiku, lai izveidotu un atjauninātu stundu prognožu ierakstus (**ProjForecastEmpl**).

Projekta grāmatvedis pārskata budžeta stundu ierakstus, kas izveidoti finanšu un operāciju programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Visi projekti** > **Plānot** > **stundu prognozes**.

## <a name="expense-estimates"></a>Izdevumu tāmes

Izmaksu aprēķinus izveido projekta vadītājs cilnē **Izdevumu aprēķini** Dataverse lapā **Detalizēta informācija par projektu**. Izmaksu aprēķinu ieraksti tiek glabāti Dataverse entītijā **Novērtēšanas rinda**. Šiem budžeta ierakstiem ir darbību klase Izdevumi **,** un tie tiek sinhronizēti ar izdevumu budžeta ierakstiem finanšu un operāciju programmās, izmantojot **projektu operāciju integrācijas entītiju izdevumu aplēsēm (msdyn\_ estimatelines)**.

   ![Izdevumu aprēķinu integrācija.](./Media/DW4ExpenseEstimates.png)

Duālā rakstīšana sinhronizē izdevumu aprēķinu ierakstus ar izstādīšanas tabulu (**ProjCDSEstimateExpenseImport**) un pēc tam izmanto biznesa loģiku, lai izveidotu un atjauninātu izdevumu prognožu ierakstus (**ProjForecastCost**). Aprēķinu rindās pārdošanas aprēķinu un izmaksu aprēķinu ieraksti tiek glabāti atsevišķi. Biznesa loģika finanšu un operāciju programmās aizpilda vienu izdevumu prognozes ierakstu, izmantojot šo detalizētu informāciju sagatavošanas tabulā.

Projekta grāmatvedis var pārskatīt izdevumu prognozes ierakstus finanšu un operāciju programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Visi projekti** > **Plānot** > **izdevumu prognozes**.

## <a name="material-estimates"></a>Materiālu aprēķini

Materiālu aprēķinus izveido projekta vadītājs cilnē **Materiālu aprēķini** Dataverse lapā **Detalizēta informācija par projektu**. Materiālu aprēķinu ieraksti tiek glabāti Dataverse entītijā **Novērtēšanas rinda**. Šiem novērtējuma ierakstiem ir darbību klase **Materiāls** un tie tiek sinhronizēti ar krājumu budžeta ierakstiem finanšu un operāciju programmās, izmantojot **projekta integrācijas tabulu materiālu aplēsēm (msdyn\_ estimatelines)**.

   ![Materiālu aprēķinu integrācija.](./Media/DW4MaterialEstimates.png)

Duālā rakstīšana sinhronizē materiālu aprēķinu ierakstus ar izstādīšanas tabulu **ProjForecastSalesImpor** un pēc tam izmanto biznesa loģiku, lai izveidotu un atjauninātu vienumu prognožu ierakstus (**ForecastSales**). Aprēķinu rindās pārdošanas aprēķinu un izmaksu aprēķinu ieraksti tiek glabāti atsevišķi. Biznesa loģika finanšu un operāciju programmās aizpilda vienu vienumu prognozes ierakstu, izmantojot šo detalizētu informāciju sagatavošanas tabulā.

Projekta grāmatvedis var pārskatīt preču budžeta ierakstus finanšu un operāciju programmās, dodoties uz **Projektu pārvaldība un uzskaite** > **Visi projekti** > **Plānot** > **preču prognozes**.

## <a name="project-actuals"></a>Projekta faktiskie dati

Projekta faktiskie dati tiek izveidoti risinājumā Dataverse, pamatojoties uz laiku, izdevumiem, materiāliem un norēķinu darbībām. Šajā Dataverse entītijā ir tverti visi šo transakciju darbības atribūti, tostarp daudzums, izmaksas, pārdošanas cena un projekts. Papildinformāciju skatiet sadaļā [Faktiskie dati](../actuals/actuals-overview.md). Faktiskie ieraksti tiek sinhronizēti ar finance and operations programmām, izmantojot divrakstā tabulas karti **Project Operations integration actuals (msdyn\_ actuals)** pakārtotajai grāmatvedībai.

   ![Faktisko datu integrācija.](./Media/DW4Actuals.png)

Tabulas karte **Project Operations integrācijas faktiskie dati** sinhronizē visus ierakstus no entītijas **Faktiski dati** programmā Dataverse, kamēr atribūts **Izlaist sinhronizāciju (tikai iekšējai lietošanai)** ir iestatīts uz **Aplams**. Šī atribūta vērtība tiek iestatīta risinājumā Dataverse automātiski ieraksta izveides laikā. Piemēri, kuros šim atribūtam ir iestatīta vērtība **Patiess**:

  - Projekta izmaksu faktiskās vērtības starpuzņēmumu transakcijām. Papildinformāciju skatiet sadaļā [Starpuzņēmumu transakciju izveide](../project-accounting/create-intercompany-transactions.md). Šie ieraksti tiek izlaisti, jo sistēma atjauno projekta faktiskās izmaksas finanšu un operāciju programmās, grāmatojot starpuzņēmumu kreditora rēķinu.
  - Negatīvie rēķinā neiekļautie pārdošanas ieraksti tiek izveidoti, kad tiek apstiprināts pro formas rēķins. Šie ieraksti tiek izlaisti, jo projekta apakšgrāmata finanšu un operāciju programmās neatsauc nemainīgo pārdošanas ierakstu, izrakstot rēķinu, bet maina statusu uz pilnībā izrakstītu rēķinu.

Duālās rakstīšanas tabulas karte sinhronizē faktisko datu ierakstus ar izstādīšanas tabulu **ProjCDSActualsImport**. Šos ierakstus apstrādā periodiskais process **Importēt no izstādīšanas tabulas**, veidojot Project Operations integrācijas žurnāla rindas un projektu rēķinu priekšlikumu rindas. Papildinformāciju skatiet sadaļā [Project Operations integrācijas žurnāls](../project-accounting/project-operations-integration-journal.md).

Turklāt Dataverse tver saites starp projektu faktisko datu transakcijām entītijā **Transakcijas savienojums**. Papildinformāciju skatiet sadaļā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](../actuals/linkingactuals.md). Saites starp faktiskajām darbībām tiek sinhronizētas arī ar Finance and Operations programmām, izmantojot divrakstījuma tabulas karti Integrācijas **entītija projektu transakciju relācijām (msdyn\_ transactionconnections)**. Šos ierakstus izmanto periodiskais process **Importēt no izstādīšanas tabulas**, veidojot Project Operations integrācijas žurnāla rindas un projektu rēķinu priekšlikumu rindas.

Project Operations integrācijas žurnāla un projekta rēķina priekšlikuma grāmatošanas aktivizē atjauninājumu atbilstošajos ierakstos izstādīšanas tabulā **ProjCDSActualsImport**. Sistēma tver un ieraksta tālāk norādītos faktisko transakciju grāmatvedības atribūtus.

- Uzskaites valūtas summa
- Maiņas kurss
- Dokumenta numurs
- PVN summa

Tabulas karte **Project Operations integrācijas faktiskie dati** atjaunina atbilstošos faktisko datu ierakstus risinājumā Dataverse, izmantojot šo informāciju.
