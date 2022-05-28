---
title: Izmantot sagādes kategorijas ar projekta pirkšanas pasūtījumiem un neizlemtajiem kreditoru rēķiniem
description: Šajā tēmā aprakstīts, kā konfigurēt sagādes kategorijas, kuras var izmantot ar projekta pirkšanas pasūtījumiem un gaidošajiem kreditoru rēķiniem.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613360"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Izmantot sagādes kategorijas ar projekta pirkšanas pasūtījumiem un neizlemtajiem kreditoru rēķiniem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Iepirkumu speciālisti var izveidot un uzturēt to preču un pakalpojumu katalogus, kurus var izmantot projektu pirkšanas pasūtījumos un gaidošos kreditoru rēķinos. [Iepirkumu katalogi sniedz vienkāršu veidu, kā kategorizēt pirkumus](/dynamics365/supply-chain/procurement/procurement-catalogs), nekonfigurējot un neizmantojot izlaisto preču katalogu. Katru sagādes kategoriju var kartēt uz projekta kategoriju laika, izdevumu vai krājumu darbībām. Pēc tam, kad ir iegrāmatots gaidošais kreditora rēķins, kas izmanto sagādes kategoriju, sistēma izveido laika, izdevumu vai materiālu projekta faktiskos, projekta darbības un apakšgrāmatas ierakstus.

## <a name="minimum-version-requirements"></a>Minimālās versijas prasības

Lai izmantotu sagādes kategorijas ar projektu pirkšanas pasūtījumiem Microsoft Dynamics 365 Project Operations neuzkrātiem/uz resursiem balstītiem scenārijiem, ir nepieciešamas šādas versijas:

- Projekta operāciju Dataverse risinājuma versija 4.41.0.45 vai jaunāka versija
- Finanšu un operāciju vides versija 10.0.26 vai jaunāka versija

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Dubultrakstīšanas karšu palaišana sagādes kategoriju atbalstam

Pārliecinieties, vai projekta operāciju integrācijas projekta kreditora rēķina rindas eksporta entītijas msdyn **projectvendorinvoicelines\_ kartējums** izmanto versiju 1.0.0.4 vai jaunākai versijai.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Iespējot funkcionalitātes atslēgu sagādes kategorijām

Veiciet šīs darbības, lai iespējotu funkcionalitāti sagādes kategoriju izmantošanai ar projekta pirkšanas pasūtījumiem.

1. Programmā Dynamics 365 Finance atveriet **līdzekļu pārvaldības** darbvietu.
1. Līdzekļu sarakstā atrodiet **līdzekli Izmantot sagādes kategorijas projektā Projekta operācijas uz resursiem balstītiem/neuzkrātiem scenārijiem** un pēc tam atlasiet **Iespējot**.

> [!IMPORTANT]
> Priekšnosacījums ir jāiespējo **arī līdzeklis Iespējot gaidošos kreditoru rēķinus projekta operācijās uz resursiem balstītiem/neuzkrātiem scenārijiem**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Kartēt projektu kategorijas sagādes kategoriju hierarhijā

Veiciet tālāk norādītās darbības, lai kartētu projektu kategorijas uz sagādes kategorijām sagādes **kategoriju** hierarhijā:

1. Dodieties uz **Sagādes un sagādes \> kategorijas** Iepirkumi.
1. Atlasiet **Rediģēt kategoriju hierarhiju**.
1. Atlasiet vēlamo kategoriju hierarhijas zaru un pēc tam cilnē **Projektu kategoriju** piešķiršana saistiet zaru ar projekta kategoriju no **kategorijas Laiks**, Izdevumi**vai **,Preces projekts** (t.i., **kategorijā Noklusētais laiks** vai **Noklusētie izdevumi**).
1. Atlasiet **Saglabāt**.
1. Aizveriet lapu.

> [!NOTE]
> Sagādes kategorijas kartēšana uz projekta kategoriju nav obligāta. Ja sagādes **kategorija nav kartēta, sistēma izmantos vērtību, kas iestatīta** **lapas** Projektu vadība un grāmatvedības parametri cilnes Project Operations on Dynamics 365 Customer engagement (Projekta vadības un grāmatvedības parametri) cilnes Project Operations on Dynamics 365 Customer engagement **(Projekta vadības un grāmatvedības parametri**) **sadaļā** Prece.
