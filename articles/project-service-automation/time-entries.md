---
title: Laika ierakstu izveide
description: Šajā tēmā ir sniegta informācija par to, kā izveidot laika ierakstus.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 90f6450b-e0c4-4d86-b8f5-ffb1a2b1e38a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ae3af7d62d93884c7fa9881394b7129daeb8bf7e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753528"
---
# <a name="create-time-entries"></a>Laika ierakstu izveide

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation iepriekšējās versijās laika ieraksti tika ievadīti katru nedēļu. Programmas Project Service Automation 3. versijā laika ieraksti tiek ievadīti katru dienu. Tomēr pēc dažu laika ierakstu izveidošanas tos var masveidā izveidot vai kopēt.

## <a name="create-a-time-entry"></a>Laika ieraksta izveide

Lai izveidotu laika ierakstu, veiciet šādas darbības.

1. Lapā **Laika ieraksti** atlasiet **Jauns**.
2. Dialoglodziņā **Ātrā izveide: laika ieraksts**, ievadiet laika ieraksta ilgumu minūtēs, stundās vai dienās. Ilgums ir jāievada šādā formātā: *x* minūtes, *x* stundas vai *x* dienas. Stundas un dienas var ievadīt arī kā decimālās vērtības, piemēram, *x,x* stundas vai *x,x* dienas.
3. Atlasiet laika ieraksta tipu un projektu, kuram ievadāt laika ierakstu.
4. Laukā **Projekta uzdevums** atrodiet šī laika ieraksta uzdevumu.

    > [!NOTE]
    > Ja izveidojat laika ierakstu uzdevumam, kas nav piešķirts lietotājam, laukā **Projekta uzdevums** atlasiet pogu **Meklēšana**, atlasiet **Mainīt skatu** un pēc tam atlasiet **Visus aktīvus projekta uzdevumus**, lai uzskaitītu visus uzdevumus.

5. Ievadiet aprakstu, ja ir nepieciešams apraksts, un pēc tam atlasiet vienumu **Saglabāt un aizvērt**.

Pēc laika ieraksta izveidošanas un saglabāšanas to var rediģēt laika ierakstu režģī. Laika ierakstu režģī tiek atbalstīti divi formāti.

- Laika ierakstus var ievadīt **ss: mm** formātā. Šis formāts pēc tam tiek pārvērsts stundās un daļskaitļos.
- Stundas un daļskaitļus var ievadīt tieši.

Ņemiet vērā, ka stundas daļskaitļi nav minūtes. Tāpēc 1,5 stundas apzīmē 1 stundu un 30 minūtes. Tas pats noteikums attiecas uz dienas daļskaitļiem. Viena diena ir 24 stundas, un 0,5 dienas apzīmē 12 stundas.

## <a name="bulk-create-time-entries"></a>Lielapjoma laika ierakstu izveide

Pēc dažu laika ierakstu izveides varat tos kopēt, lai izveidotu papildu lielapjoma laika ierakstus.

1. Lapā **Laika ieraksti** atlasiet **Kopēt nedēļu**.
2. Lauka grupā **No perioda**, laukos **Sākuma datums** un **Beigu datums**, definējiet datumu diapazonu, no kura kopēt laika ierakstus.
3. Lauka grupā **Līdz periodam**, laukā **Sākuma datums** norādiet datumu, kuram izveidot laika ierakstus.
4. Atlasiet **Kopēt**, lai izveidotu to laika ierakstu kopiju, kas atbilst tās nedēļas dienai, kura norādīta lauka grupā **Līdz periodam**. Piemēram, pagājušās nedēļas pirmdienas laika ieraksts tiek kopēts uz tās nedēļas pirmdienu, kas norādīta lauka grupā **Līdz periodam**.

## <a name="import-data-for-time-entries"></a>Datu importēšana laika ierakstiem

Varat importēt datus no projektu rezervācijām un piešķirēm. Importējot datus, var norādīt importējmo rezervāciju datumu diapazonu un pēc tam tieši atlasīt rezervācijas, kas jāizveido kā **Melnraksta** laika ieraksti.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Grupēšanas, kārtošanas, meklēšanas un filtrēšanas iespējas

Varat grupēt un filtrēt laika ierakstus pēc dimensijām, kas ir norādītas kolonnās. Laukā **Grupēt pēc** atlasiet izmantojamo dimensiju laika ierakstu filtrēšanai. Laika ierakstus var kārtot augošā vai dilstošā secībā, izmantojot kārtošanas bultiņu kolonnu virsrakstos. Turklāt varat rādīt vai paslēpt ierakstus, atlasot pogu **Filtrēt** kolonnu virsrakstos un pēc tam lodziņā **Meklēšana** ievadīt tekstu, kas jālieto laika ierakstu meklēšanai pēc projekta nosaukuma, projekta uzdevuma, laika ieraksta vai resursa.
