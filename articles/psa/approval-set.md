---
title: Project Service Automation apstiprināšanas kopas
description: Šajā tēmā ir sniegta informācija par apstiprināšanas kopu, pieprasījumiem un šo darbību apakškopām.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9a7a9efbd8615f4923c6795a16c9cf98a40362b6
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323560"
---
# <a name="approval-sets-in-project-service-automation"></a>Project Service Automation apstiprināšanas kopas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Apstiprināšanas kopas sagrupē apstiprinājuma pieprasījumus mazākās darbību apakškopās. Šī grupēšana ļauj apstrādāt apstiprinājumus pasūtījumā pēc projekta, kā arī ļauj atkārtotus mēģinājumus un secības noteikšanu. Grupēšana uzlabo apstiprināšanas apstrādes uzticamību un izsekojamību lielam apstiprinājumu apjomam.

Apstiprināšanas kopas parāda saistīto ierakstu kopējo apstrādes stāvokli. Kad apstiprinājuma ieraksts tiek apstrādāts, izmantojot apstiprināšanas kopu, ieraksts tiek pārvietots no **Iesniegts** uz **Apstiprināts** un tiek atsaistīts no apstiprināšanas kopas. Ja, iesniedzot apstiprināšanai, ieraksts ir nesekmīgs, tam tiek saglabāts statuss **Iesniegts**, un apstiprināšanas kopa tiek atzīmēta kā nesekmīga. Apstiprināšanas kopa reģistrē kļūmes kļūdas ziņojumu.

## <a name="processing-approvals-and-approval-sets"></a>Apstiprinājumu un apstiprināšanas kopu apstrāde
Apstiprinājumi, kas ir ievietoti rindā apstrādei, ir redzami skatā **Apstiprinājumu apstrāde**. Sistēma mēģina apstrādāt visus ierakstus vairākas reizes asinhroni, tostarp mēģina vēlreiz veikt apstiprināšanu, ja iepriekšējie mēģinājumi nav izdevušies.

Laukā **Apstiprināšanas kopas darbmūžs** tiek reģistrēts atlikušais kopas apstrādes mēģinājumu skaits, pirms tā tiek atzīmēta kā nesekmīga.

## <a name="failed-approvals-and-approval-sets"></a>Nesekmīgi apstiprinājumi un apstiprināšanas kopas
Skatā **Nesekmīgie apstiprinājumi** ir uzskaitīti visi apstiprinājums, kam nepieciešama lietotāja iejaukšanās. Atveriet saistītos apstiprināšanas kopu žurnālus, lai noteiktu kļūmes iemeslu.
Atlasot **Mēģināt vēlreiz**, tiek palielināts apstiprināšanas kopas darbmūža rādītājs, apstiprināšanas kopai tiek atjaunots statuss **Apstrādā**, un notiek mēģinājums apstrādāt atlikušos ierakstus.

## <a name="configure-approval-sets"></a>Apstiprināšanas kopu konfigurēšana

###  <a name="enable-the-approval-sets-feature"></a>Apstiprināšanas kopu līdzekļa iespējošana
Pirms apstiprināšanas kopu līdzekļa iespējošanas pārliecinieties, vai pašlaik netiek apstrādāts neviens apstiprinājums.

- Dodieties uz lapu **Projekta parametri** un atlasiet **Līdzekļu vadība** > **Iespējot mūsdienīgos apstiprinājumus**.

### <a name="turn-off-the-approval-sets-feature"></a>Apstiprināšanas kopu līdzekļa izslēgšana
Pirms apstiprināšanas kopu līdzekļa izslēgšanas pārliecinieties, vai pašlaik netiek apstrādāts neviens apstiprinājums.

- Dodieties uz lapu **Projekta parametri** un atlasiet **Līdzekļu vadība** > **Atspējot mūsdienīgos apstiprinājumus**.

### <a name="configuring-the-asynchronous-threshold"></a>Asinhronā sliekšņa konfigurēšana 
Veidojot apstiprināšanas kopas, apstrāde tiek pārcelta fonā, kad atlasītais apstiprināšanai izvēlēto ierakstu skaits pārsniedz norādīto robežvērtību. Izmantojiet lauku **Asinhronais slieksnis**, lai konfigurētu, kad apstiprinājumu apstrāde jāveic sinhroni vai asinhroni.
Derīgas vērtības ir:

  - nulle: visi pieprasījumi ir jāapstrādā asinhroni; 
  - skaitļi, kas ir lielāki par nulli: apstiprinājumus apstrādā asinhroni tikai tad, ja iesniegto apstiprinājumu skaits pārsniedz šo vērtību.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
