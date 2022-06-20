---
title: Apstiprināšanas kopas
description: Šajā rakstā ir paskaidrots, kā strādāt ar apstiprinājumu kopām, pieprasījumiem un šo operāciju apakškopām.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 5e030c1aa4a41b428a0f4541fd204a7a3deaba08
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918091"
---
# <a name="approval-sets"></a>Apstiprināšanas kopas

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Apstiprināšanas kopas sagrupē apstiprinājuma pieprasījumus mazākās darbību apakškopās. Izmantojot šo grupēšanu, apstiprinājumus var apstrādāt projekta ietvaros noteiktā secībā, kā arī var veikt atkārtotus mēģinājumus un secīgošanu. Grupējot kopā apstiprināšanas pieprasījumus, tiek uzlabota apstiprinājumu apstrādes uzticamība un izsekošana lielam apstiprinājumu apjomam.

Apstiprināšanas kopas parāda saistīto ierakstu kopējo apstrādes stāvokli. Kad apstiprinājuma ieraksts tiek apstrādāts, izmantojot apstiprināšanas kopu, ieraksts tiek pārvietots no sadaļas **Iesniegts** uz **Apstiprināts** un vairs nav saistīts ar apstiprināšanas kopu. Ja, iesniedzot apstiprināšanai, ieraksts ir nesekmīgs, tam tiek saglabāts statuss **Iesniegts**, un apstiprināšanas kopa tiek atzīmēta kā nesekmīga. Apstiprināšanas kopa reģistrē kļūmes kļūdas ziņojumu.

## <a name="processing-approvals-and-approval-sets"></a>Apstiprinājumu un apstiprināšanas kopu apstrāde
Apstiprinājumi, kas ir ievietoti rindā apstrādei, ir redzami skatā **Apstiprinājumu apstrāde**. Sistēma visus ierakstus apstrādā vairākas reizes asinhroni, ieskaitot apstiprināšanas atkārtošanu, ja iepriekšējie mēģinājumi nav sekmīgi.

Laukā **Apstiprināšanas kopas darbmūžs** tiek reģistrēts atlikušais kopas apstrādes mēģinājumu skaits, pirms tā tiek atzīmēta kā nesekmīga.

Apstiprinājumu kopas tiek apstrādātas, izmantojot periodisko aktivizēšanu, **pamatojoties uz mākoņa plūsmas** projektu pakalpojumu ar nosaukumu **Project Service - Atkārtoti plānot projektu apstiprināšanas kopas**. Tas ir atrodams risinājumā **ar** nosaukumu **Project Operations**. 

Pārliecinieties, vai plūsma ir aktivizēta, veicot tālāk norādītās darbības.

1. Kā administrators piesakieties [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Augšējā labajā stūrī pārslēdzieties uz vidi, kurai izmantojat Dynamics 365 Project Operations.
3. Atlasiet **Risinājumi**, lai uzskaitītu vidē instalētos risinājumus.
4. Risinājumu sarakstā atlasiet **Projekta operācijas**.
5. Mainiet filtru no **Visas** uz **Mākoņa plūsmas**.
6. Pārbaudiet, **vai projekta pakalpojuma atkārtota grafika projektu apstiprināšanas kopu** plūsma ir iestatīta uz **Ieslēgta**. Ja tā nav, atlasiet plūsmu un pēc tam atlasiet **Ieslēgt**.
7. Pārbaudiet, vai apstrāde notiek ik pēc piecām minūtēm, pārskatot **sistēmas uzdevumu** sarakstu projektu operāciju **vides apgabalā** Iestatījumi Dataverse.

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
