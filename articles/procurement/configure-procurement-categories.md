---
title: Iepirkumu kategoriju izmantošana ar projekta pirkuma pasūtījumiem un neizpildītiem piegādātāja rēķiniem
description: Šajā rakstā ir aprakstīts, kā konfigurēt iepirkuma kategorijas, ko var izmantot ar projekta pirkuma pasūtījumiem un neizpildītiem piegādātāja rēķiniem.
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
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Iepirkumu kategoriju izmantošana ar projekta pirkuma pasūtījumiem un neizpildītiem piegādātāja rēķiniem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Iepirkumu speciālisti var izveidot un uzturēt preču un pakalpojumu katalogus, ko var izmantot projekta pirkumu pasūtījumos un neizpildītos piegādātāja rēķinos. [Iepirkumu katalogi](/dynamics365/supply-chain/procurement/procurement-catalogs) sniedz vienkāršu veidu, kā kategorizēt pirkumus bez nepieciešamības konfigurēt un izmantot izlaistu produktu katalogu. Katru iepirkuma kategoriju var kartēt uz projekta kategoriju laika, izmaksu vai preču transakcijām. Pēc tam, kad ir iegrāmatots neizpildīts rēķins, kurā izmantota iepirkumu kategorija, sistēma izveido laika, izmaksu vai materiālu projekta faktiskos datus, projekta transakcijas un apakšgrāmatas ierakstus.

## <a name="minimum-version-requirements"></a>Nepieciešamās minimālās prasības

Lai izmantotu iepirkumu kategorijas ar projekta pirkumu pasūtījumiem Microsoft Dynamics 365 Project Operations krājumos neesošo materiālu/uz resursiem balstītos scenārijos, ir nepieciešamas tālāk norādītās versijas.

- Project Operations Dataverse risinājuma versija 4.41.0.45 vai jaunāka
- Finanšu un operāciju vides versija 10.0.26 vai jaunāka

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Duālās rakstīšanas karšu palaišana iepirkumu kategoriju atbalstam

Pārliecinieties, ka **Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija msdyn\_projectvendorinvoicelines** izmanto versiju 1.0.0.4 vai jaunāku.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Līdzekļa atslēgas iespējošana iepirkumu kategorijām

Veiciet šīs darbības, lai iespējotu funkcionalitāti iepirkumu kategoriju izmantošanai ar projekta pirkumu pasūtījumiem.

1. Programmā Dynamics 365 Finance atveriet darbvietu **Līdzekļu pārvaldība**.
1. Līdzekļu sarakstā atrodiet līdzekli **Izmantot iepirkumu kategorijas programmā Project Operations uz resursiem balstītu/krājumos neesošu materiālu scenārijiem** un pēc tam atlasiet **Iespējot**.

> [!IMPORTANT]
> Kā priekšnoteikums ir jāiespējo arī līdzeklis **Iespējot neapstiprināto piegādātāju rēķinus risinājumā Project Operations uz resursiem balstītiem/krājumos neesošu materiālu scenārijiem**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projektu kategoriju kartēšana iepirkumu kategoriju hierarhijā

Izpildiet šīs darbības, lai kartētu projekta kategorijas uz iepirkumu kategorijām hierarhijā **Iepirkumu kategorija**.

1. Pārejiet uz **Sagāde un avoti \> Iepirkumu kategorijas**.
1. Atlasiet **Rediģēt kategoriju hierarhiju**.
1. Atlasiet vēlamo kategorijas hierarhijas mezglu un pēc tam cilni **Piešķirt projekta kategorijas**, saistiet mezglu ar projekta kategoriju no kategorijas **Laiks**, **Izdevumi** vai **Preču projekts** (proti, kategorijas **Noklusējums - laiks** vai **Noklusējums - izdevumi**).
1. Atlasiet **Saglabāt**.
1. Aizveriet lapu.

> [!NOTE]
> Iepirkumu kategorijas kartēšana uz projekta kategoriju nav obligāta. Ja iepirkumu kategorija nav kartēta, sistēma izmantos vērtību, kas ir iestatīta laukā **Vienums** sadaļā **Projektu kategoriju noklusējumi** cilnē **Project Operations pakalpojumā Dynamics 365 Customer Engagement**, kas atrodas lapā **Projekta pārvaldības un uzskaites parametri**.
