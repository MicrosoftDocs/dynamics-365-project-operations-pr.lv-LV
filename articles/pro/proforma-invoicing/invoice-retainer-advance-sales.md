---
title: Rēķina izrakstīšana par honorāru vai avansu
description: Šajā tēmā sniegta informācija par to, kā programmā Project Operations izrakstīt rēķinus par honorāru vai avansu.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 12bf3822227badcf8c83d84d6aef6c0fdc7a972a
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596201"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Honorāra vai avansa rēķina izrakstīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations atbalsta līgumus, kuru pamatā ir honorārs, un vienreizējus avansus. Projekta līgumam varat ierakstīt honorāru grafiku vai vienreizēju avansu. Tomēr ieraksts projekta līguma līmenī nekavējoties neveido honorāru vai avansu, kas pieejams lietošanai. Lai izmantotu honorāru vai avansu rēķinam, kas faktiski iekasē maksu no klienta, vispirms ir jāizraksta rēķins par honorāru vai avansu.

Veiciet tālāk norādītās darbības, lai izrakstītu rēķinu par honorāru vai avansu.

1. Atlasiet **Pārdošana** > **Norēķini** > **Honorāri un avansi**. 
2. Lapā **Avansi un honorāri** izmantojiet filtrēšanu, lai atlasītu noteiktu honorāru vai avansu rēķinam, un atzīmējiet to kā **Gatavs rēķina izrakstīšanai**.
3. Izveidojiet rēķinu manuāli, izmantojot sarakstu **Projekta līgumi** vai detalizētās informācijas lapu. Honorārs vai avanss tiek rādīts lapas **Rēķins** sadaļas **Avansi un honorāri** rēķina melnrakstā.
4. Apstipriniet rēķinu. Tādējādi honorārs vai avanss būs pieejams izmantošanai. Rēķinu var pārbaudīt saraksta lapā **Honorāri un avansi**. Izrakstītā avansa vai honorāra pieejamā summa tiek rādīta režģī.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Honorāra vai avansa izveide no rēķina režģa

Var izveidot honorāru vai avansu tieši rēķinā.

1. Rēķina melnraksta apakšrežģī **Avansi un honorāri** atlasiet vienumu **Jauns**, lai izveidotu jaunu honorāru vai avansu. 
2. Lapā **Ātrā izveide** pievienojiet nepieciešamo informāciju un pēc tam atlasiet vienumu **Saglabāt**. Tiek izveidots honorārs vai avanss ar rēķinu saistītajam projekta līgumam. Honorārs vai avanss tiek automātiski atzīmēts kā **Gatavs rēķina izrakstīšanai** un pēc tam pievienots apakšrežģim **Avansi un honorāri** lapā **Rēķins**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Rēķinā izrakstīta honorāra vai avansa saskaņošana

Kad honorārs vai avanss ir izrakstīts rēķinā, tos var izmantot vai saskaņot rēķinā kopā ar laika, izdevumu, atskaites punktu vai citām projekta izmaksām. Klients redzēs rēķina summu, kas samazināta, atskaitot šajā rēķinā izmantoto honorāra vai avansa summu.

Katram rēķinam, kas ir izveidots projekta līgumam, kuram ir izrakstīts rēķins avansiem vai honorāriem, Project Operation automātiski rēķinā lieto honorāru vai avansu.

To var redzēt lapas **Rēķins** režģī **Lietotie honorāri un avansi**. Tālāk atrodamajā tabulā ir sniegta informācija par laukiem, kas atrodas lapas **Projekta rēķins** režģī **Lietotie honorāri un avansi**.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| Apraksts | Režģis **Lietotie honorāri un avansi** lapā **Projekta rēķins** |Šis tikai lasāmais lauks nodrošina avansa vai honorāra aprakstu, kas tiek izmantots šajā rēķinā. Šo vērtību rēķinā nevar mainīt. Šo vērtību var atjaunināt lapas **Projekta līgums** apakšrežģī. | Šo lauku var parādīt klientam drukātajā rēķinā, lai norādītu, kurš honorārs vai avanss tiek izmantots rēķinā. |
| Kad piegādāts | Režģis **Lietotie honorāri un avansi** lapā **Projekta rēķins**  | Šis tikai lasāmais lauks nodrošina avansa vai honorāra rēķina datumu, kas tiek izmantots šajā rēķinā. Šo vērtību rēķinā nevar mainīt. Šo vērtību var atjaunināt lapas **Projekta līgums** apakšrežģī. | Šo lauku var parādīt klientam drukātajā rēķinā, lai norādītu datumu, kad honorārs vai avanss tika vispirms izrakstīts klienta rēķinā. |
| Apjoms/summa | Režģis **Lietotie honorāri un avansi** lapā **Projekta rēķins**  | Šis tikai lasāmais lauks nodrošina avansa vai honorāra summu, kas tiek izmantots šajā rēķinā. Šo vērtību rēķinā nevar mainīt. Šo vērtību var atjaunināt lapas **Projekta līgums** apakšrežģī. | Šo lauku var parādīt klientam drukātajā rēķinā, lai norādītu honorāra vai avansa sākotnējo summu, ko apmaksāja klients. |
| Izmantotā summa | Režģis **Lietotie honorāri un avansi** lapā **Projekta rēķins**  | Šis tikai lasāmais lauks nodrošina aprēķināto vērtību, kas apkopo, kāds daudzums honorāra vai avansa ir izmantots. | Šo lauku var parādīt klientam drukātajā rēķinā, lai norādītu šī honorāra vai avansa summu, kas jau tika izmantots. |
| Kopējā summa | Režģis **Lietotie honorāri un avansi** lapā **Projekta rēķins**  | Šis rediģējamais lauks nodrošina tā avansa vai honorāra summu, kas tiek izmantots šajā projekta rēķinā. Šī summa nevar būt lielāka par avansā pieejamo summu. Sistēma automātiski aprēķina to kā atšķirību starp režģa laukiem **Summa** un **Izmantotā summa**. Jūs varat samazināt summu, lai izmantotu mazāk nekā pieejams, tomēr nevarat palielināt summu, lai izmantotu vairāk nekā pieejams. | Šo lauku var parādīt klientam drukātajā rēķinā, lai norādītu šī honorāra vai avansa summu, kas tiek izmantots rēķinā. |
| Honorāra bilances summa. | Režģis **Lietotie honorāri un avansi** lapā **Projekta rēķins**  | Šis tikai lasāmais lauks nodrošina vērtību, cik daudz honorāra vai avansa atliks pēc rēķina apstiprināšanas. | Šo lauku var parādīt klientam drukātajā rēķinā, lai norādītu šī honorāra vai avansa summu, kas paliks no šī honorāra vai avansa pēc rēķina apstiprināšanas un apmaksāšanas. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]