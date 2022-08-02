---
title: Sagādes kategoriju izmantošana ar projektu pirkšanas pasūtījumiem un gaidošiem kreditoru rēķiniem
description: Šajā rakstā ir aprakstīts, kā konfigurēt sagādes kategorijas, ko var izmantot ar projektu pirkšanas pasūtījumiem un gaidošajiem kreditoru rēķiniem.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028619"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Sagādes kategoriju izmantošana ar projektu pirkšanas pasūtījumiem un gaidošiem kreditoru rēķiniem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Iepirkumu speciālisti var izveidot un uzturēt to krājumu un pakalpojumu katalogus, kurus var izmantot projektu pirkšanas pasūtījumos un gaidošos kreditoru rēķinos. [Sagādes katalogi](/dynamics365/supply-chain/procurement/procurement-catalogs) sniedz vienkāršu veidu, kā kategorizēt pirkumus, nekonfigurējot un neizmantojot izlaisto preču katalogu. Katru sagādes kategoriju var kartēt uz projekta kategoriju laika, izdevumu vai krājumu transakcijām. Pēc tam, kad tiek grāmatots gaidošs kreditora rēķins, kurā tiek izmantota sagādes kategorija, sistēma izveidos laika, izdevumu vai materiālu projekta faktiskos datus, projekta transakcijas un apakšzemes ierakstus.

## <a name="minimum-version-requirements"></a>Minimālās versijas prasības

Tālāk norādītās versijas ir nepieciešamas, lai izmantotu sagādes kategorijas ar projektu pirkšanas pasūtījumiem Microsoft Dynamics 365 Project Operations scenārijiem, kuru pamatā nav krājumu/resursu:

- Project Operations Dataverse risinājuma versija 4.41.0.45 vai jaunāka
- Finance and operations vides versija 10.0.26 vai jaunāka

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Divrakstu karšu palaišana sagādes kategoriju atbalstam

Pārliecinieties, vai Project Operations integrācijas **projekta kreditora rēķina rindas eksportēšanas entītijas msdyn\_ projectvendorinvoicelines** kartēšanā tiek izmantota 1.0.0.4 vai jaunāka versija.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Līdzekļa atslēgas iespējošana sagādes kategorijām

Veiciet šīs darbības, lai iespējotu funkcionalitāti sagādes kategoriju izmantošanai projektu pirkšanas pasūtījumos.

1. Programmā Dynamics 365 Finance atveriet darbvietu **Līdzekļu pārvaldība**.
1. Līdzekļu sarakstā atrodiet **līdzekli Izmantot sagādes kategorijas project operations for resource based/non-stocked scenarios** un pēc tam atlasiet **Enable (Iespējot**).

> [!IMPORTANT]
> Kā priekšnosacījums ir arī jāiespējo **līdzeklis Iespējot gaidošos kreditoru rēķinus project operations uz resursiem balstītiem/neiekrātiem scenārijiem**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projektu kategoriju kartēšana sagādes kategoriju hierarhijā

Veiciet tālāk norādītās darbības, lai sagādes kategoriju **hierarhijā projektu kategorijas** kartētu uz sagādes kategorijām.

1. Dodieties uz **sagādes un sagādes \> sagādes kategorijām**.
1. Atlasiet **Rediģēt kategoriju hierarhiju**.
1. Atlasiet vajadzīgo kategoriju hierarhijas mezglu un pēc tam **cilnē Piešķirt projekta kategorijas** saistiet mezglu ar projekta kategoriju no **kategorijas Laiks**, **Izdevumi** vai **Krājuma projekts** (tas ir, **kategorijas Noklusētais laiks** vai **Noklusējuma izdevumi**).
1. Atlasiet **Saglabāt**.
1. Aizveriet lapu.

> [!NOTE]
> Sagādes kategorijas kartēšana uz projekta kategoriju nav obligāta. Ja sagādes kategorija nav kartēta, sistēma izmantos vērtību, kas ir iestatīta **lapas Projekta vadības un grāmatvedības parametri** cilnes **Project Operations on Dynamics 365 Customer Engagement sadaļas Project Operations on Dynamics 365 Customer Engagement** laukā **Krājums** **·**.
