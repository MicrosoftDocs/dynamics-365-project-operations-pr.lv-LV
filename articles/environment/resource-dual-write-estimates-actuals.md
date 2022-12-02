---
title: Projekta aprēķinu un faktisko datu integrācija
description: Šajā rakstā ir sniegta informācija par Project Operations duālās rakstīšanas integrāciju projektu aprēķinos un faktiskajos datos.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029089"
---
# <a name="project-estimates-and-actuals-integration"></a>Projekta aprēķinu un faktisko datu integrācija

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā rakstā ir sniegta informācija par Project Operations duālās rakstīšanas integrāciju projektu aprēķinos un faktiskajos datos.

## <a name="project-estimates"></a>Projekta aprēķins

Projekta darba, izmaksu un materiālu aprēķini tiek izveidoti un uzturēti programmā Microsoft Dataverse un sinhronizēti ar finanšu un operāciju programmām grāmatvedības nolūkos. Izmantojot finanšu un operāciju programmas, netiek atbalstītas izveides, atjaunināšanas un dzēšanas darbības.

Lai izveidotu aprēķinus, projektam ir nepieciešama derīga grāmatvedības konfigurācija. Ar līguma rindām saistītajiem projektiem ir jābūt derīgam projekta izmaksu un ieņēmumu profilam, kas definēts projekta izmaksu un ieņēmumu profila kārtulās. Papildinformāciju skatiet rakstā [Apmaksājamo projektu uzskaites konfigurēšana](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Darba aprēķini

Darba aprēķinus izveido projekta vadītājs vai resursu vadītājs, kurš projekta uzdevumam piešķir arī vispārēju vai nosauktu resursu. Resursu piešķiršanas ierakstus var pārskatīt cilnē **Resursu norīkojumi** Dataverse lapā **Detalizēta informācija par projektu**. Dataverse resursu piešķiršanas ieraksti izveido stundu prognožu ierakstus finanšu un operāciju programmās, izmantojot **Project Operations integrācijas entītija stundu aprēķiniem (msdyn\_resourceassignments)**.

   ![Darba aprēķinu integrācija.](./Media/DW4LaborEstimates.png)

Duālā rakstīšana sinhronizē resursu piešķiršanas ierakstus ar izstādīšanas tabulu (**ProjCDSEstimateHoursImport**) un pēc tam izmanto biznesa loģiku, lai izveidotu un atjauninātu stundu prognožu ierakstus (**ProjForecastEmpl**).

Projekta grāmatvedis pārskata stundu prognožu ierakstus, kas izveidoti finanšu un operāciju programmās, pārejot uz **Projekta pārvaldība un uzskaite**  >  **Visi projekti**  >  **Plāns**  >  **Stundu prognozes**.

## <a name="expense-estimates"></a>Izdevumu tāmes

Izmaksu aprēķinus izveido projekta vadītājs cilnē **Izdevumu aprēķini** Dataverse lapā **Detalizēta informācija par projektu**. Izmaksu aprēķinu ieraksti tiek glabāti Dataverse entītijā **Novērtēšanas rinda**. Šiem novērtēšanas ierakstiem ir transakciju klase **Izdevumi**, un tie tiek sinhronizēti ar izdevumu prognožu ierakstiem finanšu un operāciju programmās, izmantojot **Project Operations integrācijas entītija izdevumu aprēķiniem (msdyn\_estimatelines)**.

   ![Izdevumu aprēķinu integrācija.](./Media/DW4ExpenseEstimates.png)

Duālā rakstīšana sinhronizē izdevumu aprēķinu ierakstus ar izstādīšanas tabulu (**ProjCDSEstimateExpenseImport**) un pēc tam izmanto biznesa loģiku, lai izveidotu un atjauninātu izdevumu prognožu ierakstus (**ProjForecastCost**). Aprēķinu rindās pārdošanas aprēķinu un izmaksu aprēķinu ieraksti tiek glabāti atsevišķi. Biznesa loģika finanšu un operāciju programmās aizpilda vienu izdevumu prognožu ierakstu, izmantojot šo informāciju izstādīšanas tabulā.

Projekta grāmatvedis var pārskatīt izdevumu prognožu ierakstus, kas izveidoti finanšu un operāciju programmās, pārejot uz **Projekta pārvaldība un uzskaite**  > **Visi projekti**  > **Plāns**  > **Izdevumu prognozes**.

## <a name="material-estimates"></a>Materiālu aprēķini

Materiālu aprēķinus izveido projekta vadītājs cilnē **Materiālu aprēķini** Dataverse lapā **Detalizēta informācija par projektu**. Materiālu aprēķinu ieraksti tiek glabāti Dataverse entītijā **Novērtēšanas rinda**. Šiem novērtēšanas ierakstiem ir transakciju klase **Materiāli**, un tie tiek sinhronizēti ar vienumu prognožu ierakstiem finanšu un operāciju programmās, izmantojot **Projektu integrācijas tabula materiālu aprēķiniem (msdyn\_estimatelines)**.

   ![Materiālu aprēķinu integrācija.](./Media/DW4MaterialEstimates.png)

Duālā rakstīšana sinhronizē materiālu aprēķinu ierakstus ar izstādīšanas tabulu **ProjForecastSalesImpor** un pēc tam izmanto biznesa loģiku, lai izveidotu un atjauninātu vienumu prognožu ierakstus (**ForecastSales**). Aprēķinu rindās pārdošanas aprēķinu un izmaksu aprēķinu ieraksti tiek glabāti atsevišķi. Biznesa loģika finanšu un operāciju programmās aizpilda vienu Elementa prognožu ierakstu, izmantojot šo informāciju izstādīšanas tabulā.

Projekta grāmatvedis var pārskatīt elementa prognožu ierakstus, kas izveidoti finanšu un operāciju programmās, pārejot uz **Projekta pārvaldība un uzskaite**  > **Visi projekti**  > **Plāns**  > **Elementu prognozes**.

## <a name="project-actuals"></a>Projekta faktiskie dati

Projekta faktiskie dati tiek izveidoti risinājumā Dataverse, pamatojoties uz laiku, izdevumiem, materiāliem un norēķinu darbībām. Šajā Dataverse entītijā ir tverti visi šo transakciju darbības atribūti, tostarp daudzums, izmaksas, pārdošanas cena un projekts. Papildinformāciju skatiet sadaļā [Faktiskie dati](../actuals/actuals-overview.md). Faktiskie ieraksti tiek sinhronizēti ar finanšu un operāciju programmām, izmantojot duālās rakstīšanas tabulas karti **Project Operations** integrācijas faktiskie dati (msdyn\_actuals) lejupstraumes grāmatvedībai.

   ![Faktisko datu integrācija.](./Media/DW4Actuals.png)

Tabulas karte **Project Operations integrācijas faktiskie dati** sinhronizē visus ierakstus no entītijas **Faktiski dati** programmā Dataverse, kamēr atribūts **Izlaist sinhronizāciju (tikai iekšējai lietošanai)** ir iestatīts uz **Aplams**. Šī atribūta vērtība tiek iestatīta risinājumā Dataverse automātiski ieraksta izveides laikā. Piemēri, kuros šim atribūtam ir iestatīta vērtība **Patiess**:

  - Projekta izmaksu faktiskās vērtības starpuzņēmumu transakcijām. Papildinformāciju skatiet sadaļā [Starpuzņēmumu transakciju izveide](../project-accounting/create-intercompany-transactions.md). Šie ieraksti tiek izlaisti, jo sistēma atkārtoti izveido projekta izmaksu faktiskos datus finanšu un operāciju programmās, kad tiek grāmatots starpuzņēmumu piegādātāja rēķins.
  - Negatīvie rēķinā neiekļautie pārdošanas ieraksti tiek izveidoti, kad tiek apstiprināts pro formas rēķins. Šie ieraksti tiek izlaisti, jo projekta apakšgrāmata finanšu un operāciju lietojumprogrammās nemaina rēķinā neietverto pārdošanas ierakstu rēķina izrakstīšanas laikā, bet maina statusu uz pilnībā izrakstītu rēķinu.

Duālās rakstīšanas tabulas karte sinhronizē faktisko datu ierakstus ar izstādīšanas tabulu **ProjCDSActualsImport**. Šos ierakstus apstrādā periodiskais process **Importēt no izstādīšanas tabulas**, veidojot Project Operations integrācijas žurnāla rindas un projektu rēķinu priekšlikumu rindas. Papildinformāciju skatiet sadaļā [Project Operations integrācijas žurnāls](../project-accounting/project-operations-integration-journal.md).

Turklāt Dataverse tver saites starp projektu faktisko datu transakcijām entītijā **Transakcijas savienojums**. Papildinformāciju skatiet sadaļā [Faktisko datu saistīšana ar sākotnējiem ierakstiem](../actuals/linkingactuals.md). Saites starp faktiskajām transakcijām tiek sinhronizētas arī ar finanšu un operāciju programmām, izmantojot duālās rakstīšanas tabulas karti **Integrācijas entītija projektu transakciju relācijām (msdyn\_transactionconnections)**. Šos ierakstus izmanto periodiskais process **Importēt no izstādīšanas tabulas**, veidojot Project Operations integrācijas žurnāla rindas un projektu rēķinu priekšlikumu rindas.

Project Operations integrācijas žurnāla un projekta rēķina priekšlikuma grāmatošanas aktivizē atjauninājumu atbilstošajos ierakstos izstādīšanas tabulā **ProjCDSActualsImport**. Sistēma tver un ieraksta tālāk norādītos faktisko transakciju grāmatvedības atribūtus.

- Uzskaites valūtas summa
- Maiņas kurss
- Dokumenta numurs
- PVN summa

Tabulas karte **Project Operations integrācijas faktiskie dati** atjaunina atbilstošos faktisko datu ierakstus risinājumā Dataverse, izmantojot šo informāciju.
