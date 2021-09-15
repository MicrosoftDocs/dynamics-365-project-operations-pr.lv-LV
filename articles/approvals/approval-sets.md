---
title: Apstiprināšanas kopas
description: Šajā tēmā ir izskaidrots, kā strādāt ar apstiprināšanas kopām, pieprasījumiem un šo operāciju apakškopām.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323245"
---
# <a name="approval-sets"></a>Apstiprināšanas kopas

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Apstiprināšanas kopas sagrupē apstiprinājuma pieprasījumus mazākās darbību apakškopās. Izmantojot šo grupēšanu, apstiprinājumus var apstrādāt projekta ietvaros noteiktā secībā, kā arī var veikt atkārtotus mēģinājumus un secīgošanu. Grupējot kopā apstiprināšanas pieprasījumus, tiek uzlabota apstiprinājumu apstrādes uzticamība un izsekošana lielam apstiprinājumu apjomam.

Apstiprināšanas kopas parāda saistīto ierakstu kopējo apstrādes stāvokli. Kad apstiprinājuma ieraksts tiek apstrādāts, izmantojot apstiprināšanas kopu, ieraksts tiek pārvietots no sadaļas **Iesniegts** uz **Apstiprināts** un vairs nav saistīts ar apstiprināšanas kopu. Ja, iesniedzot apstiprināšanai, ieraksts ir nesekmīgs, tam tiek saglabāts statuss **Iesniegts**, un apstiprināšanas kopa tiek atzīmēta kā nesekmīga. Apstiprināšanas kopa reģistrē kļūmes kļūdas ziņojumu.

## <a name="processing-approvals-and-approval-sets"></a>Apstiprinājumu un apstiprināšanas kopu apstrāde
Apstiprinājumi, kas ir ievietoti rindā apstrādei, ir redzami skatā **Apstiprinājumu apstrāde**. Sistēma visus ierakstus apstrādā vairākas reizes asinhroni, ieskaitot apstiprināšanas atkārtošanu, ja iepriekšējie mēģinājumi nav sekmīgi.

Laukā **Apstiprināšanas kopas darbmūžs** tiek reģistrēts atlikušais kopas apstrādes mēģinājumu skaits, pirms tā tiek atzīmēta kā nesekmīga.

## <a name="failed-approvals-and-approval-sets"></a>Nesekmīgi apstiprinājumi un apstiprināšanas kopas
Skatā **Nesekmīgie apstiprinājumi** ir uzskaitīti visi apstiprinājumi, kam nepieciešama lietotāja iejaukšanās. Atveriet saistītos apstiprināšanas kopu žurnālus, lai noteiktu kļūmes iemeslu.
Atlasot **Mēģināt vēlreiz**, tiek palielināts apstiprināšanas kopas darbmūža rādītājs, apstiprināšanas kopai tiek atjaunots statuss **Apstrādā**, un notiek mēģinājums apstrādāt atlikušos ierakstus.

## <a name="configure-approval-sets"></a>Apstiprināšanas kopu konfigurēšana

### <a name="enable-the-approval-sets-feature"></a>Apstiprināšanas kopu līdzekļa iespējošana
Pirms apstiprināšanas kopu līdzekļa iespējošanas pārliecinieties, vai pašlaik netiek apstrādāts neviens apstiprinājums.

- Dodieties uz lapu **Projekta parametri** un atlasiet **Līdzekļu vadība** > **Iespējot mūsdienīgos apstiprinājumus**.

### <a name="turn-off-the-approval-sets-feature"></a>Apstiprināšanas kopu līdzekļa izslēgšana
Pirms apstiprināšanas kopu līdzekļa izslēgšanas pārliecinieties, vai pašlaik netiek apstrādāts neviens apstiprinājums.

- Dodieties uz lapu **Projekta parametri** un atlasiet **Līdzekļu vadība** > **Atspējot mūsdienīgos apstiprinājumus**.

### <a name="configuring-the-asynchronous-threshold"></a>Asinhronā sliekšņa konfigurēšana 
Veidojot apstiprināšanas kopas, apstrāde tiek pārcelta fonā, kad atlasītais apstiprināšanai izvēlēto ierakstu skaits pārsniedz norādīto robežvērtību. Izmantojiet lauku **Asinhronais slieksnis**, lai konfigurētu, kad apstiprinājumu apstrāde jāveic sinhroni vai asinhroni. Atlasiet vienu no sniegtajām vērtībām.

  - nulle: visi pieprasījumi ir jāapstrādā asinhroni; 
  - skaitļi, kas ir lielāki par nulli: apstiprinājumus apstrādā asinhroni tikai tad, ja iesniegto apstiprinājumu skaits pārsniedz šo vērtību.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
