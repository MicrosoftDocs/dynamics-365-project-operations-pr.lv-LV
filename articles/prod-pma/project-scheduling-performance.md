---
title: Projekta resursu plānošanas veiktspēja
description: Šajā tēmā ir sniegta informācija par to, kā uzlabot resursu plānošanas veiktspēju lielam skaitam projektu.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010030"
---
# <a name="project-resource-scheduling-performance"></a>Projekta resursu plānošanas veiktspēja

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Veiktspējas problēmas, kas saistītas ar resursu plānošanu, var rasties, ja projektu skaits sasniedz tūkstošus. Lai uzlabotu resursu plānošanas veiktspēju, ir pieejams līdzeklis, kas ļauj lietotājiem samazināt laiku, kas nepieciešams, lai palaistu resursu pieejamības veidlapu. Precīzāk — tas noņem resursu ietilpības apkopošanas sinhronizācijas procesu un izmanto tabulu **ResProjectResource**, lai paātrinātu resursu pārlūkošanu. Ņemiet vērā, ka tabula **ResRollup** vairs netiks izmantota.

> [!IMPORTANT]
> Ja ir atkarība no resursu noslodzes apkopojuma sinhronizācijas procesa vai tabulas **ResProjectResource**, neizmantojiet šo līdzekli.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Resursu plānošanas veiktspējas uzlabojuma iespējošana
Lai iespējotu resursu plānošanas veiktspējas uzlabošanu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Līdzekļu pārvaldība** > **Visi** un līdzekļu sarakstā atrodiet **Iespējot projekta resursu plānošanas veiktspējas uzlabošanas līdzekli**.
2. Atlasiet **Iespējot tagad**.

> [!NOTE]
> Ja sarakstā nevarat atrast šo līdzekli, atlasiet **Pārbaudīt, vai nav atjauninājumu**, lai atsvaidzinātu sarakstu.

3. Atsvaidziniet pārlūkprogrammu un pēc tam apmeklējiet sadaļu **Projekta pārvaldība un uzskaite** > **Periodisks** > **Projekta resursi** > **Sinhronizēt resursu kalendāru noslodzi visiem uzņēmumiem**.
4. Lai noņemtu iepriekšējos datus, iestatiet **Esošu noslodzes ierakstu noņemšana** uz **Jā**. Ja vēlaties ģenerēt inkrementālos datus, iestatiet to uz **Nē**.
5. Laukā **Perioda kods** atlasiet datu ģenerēšanas periodu. Ja atlasāt perioda kodu, ir jādefinē sākuma un beigu datumi.
6. Ja lauks **Perioda kods** netiek aizpildīts, atlasiet noteiktus sākuma un beigu datumus, lai ģenerētu datus.
7. Atlasiet **Labi**.

 > [!NOTE]
 > Šādi vispārējie dati tiks izplatīti tabulā **ResCalendarCapacity** visos uzņēmumos jūsu apkārtnē, tāpēc pakešuzdevumam ir jābūt izpildītam tikai vienā juridiskā entītijā. Šī pakešuzdevuma dati ir nepieciešami, lai aprēķinātu resursa noslodzi caur saistīto kalendāru.

8. Atveriet **Projekta pārvaldība un uzskaite** > **Periodisks** > **Projekta resursi** > **Projekta resursu aizpildīšana visos uzņēmumos** un pēc tam atlasiet **Labi**. Šis ir datu jaunināšanas skripts vispārējiem datiem tabulās **ResProjectResource**, **ResCalendarDateTimeRange** un **ResEffectiveDateTimeRange**. Arī lauka **PSAPRojSchedRole.RootActivity** vērtības tiek atjauninātas. Ja tas netiek izpildīts, kad mēģināsit izpildīt resursu plānošanas operācijas, saņemsit brīdinājumu.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Resursu plānošanas veiktspējas uzlabojuma izslēgšana

1. Dodieties uz **Līdzekļu pārvaldība** > **Visi** un meklējiet **Iespējot projekta resursu plānošanas veiktspējas uzlabošanas līdzekli**.
2. Atlasiet līdzekli un pēc tam noklikšķiniet uz pogas **Atspējot**.
3. Atsvaidziniet pārlūkprogrammu.
4. Dodieties uz **Projekta pārvaldība un uzskaite** > **Periodisks** > **Noslodzes sinhronizācija** > **Sinhronizēt resursu noslodzes apkopojumus**.
5. Lapā **Noslodzes apkopojuma sinhronizācija** iestatiet **Esošo noslodzes ierakstu noņemšana** uz **Jā**, lai noņemtu iepriekšējos datus. Ja vēlaties ģenerēt inkrementālos datus, iestatiet to uz **Nē**.
6. Laukā **Perioda kods** atlasiet datu ģenerēšanas periodu. Ja atlasāt perioda kodu, ir jādefinē sākuma un beigu datumi.
7. Ja lauks **Perioda kods** netiek aizpildīts, atlasiet noteiktus sākuma un beigu datumus, lai ģenerētu datus.
8. Atlasiet **Labi**.

> [!NOTE]
> Šādi vispārējie dati tiks izplatīti tabulā **ResRollup** visos uzņēmumos jūsu apkārtnē, tāpēc pakešuzdevumam ir jābūt izpildītam tikai vienā juridiskā entītijā. Šis pakešuzdevums ir nepieciešams visiem **Resursa pieejamība** skatiem. Ja šis pakešuzdevums netiek izpildīts, **ResRollup** dati tiek ģenerēti izveides laikā, kas var prasīt laiku.


[!INCLUDE[footer-include](../includes/footer-banner.md)]