---
title: Apstiprināšanas kopas
description: Šajā rakstā ir paskaidrots, kā strādāt ar apstiprināšanas kopām, pieprasījumiem un šo darbību apakškopām.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524926"
---
# <a name="approval-sets"></a>Apstiprināšanas kopas

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Apstiprināšanas kopas sagrupē apstiprinājuma pieprasījumus mazākās darbību apakškopās. Izmantojot šo grupēšanu, apstiprinājumus var apstrādāt projekta ietvaros noteiktā secībā, kā arī var veikt atkārtotus mēģinājumus un secīgošanu. Grupējot kopā apstiprināšanas pieprasījumus, tiek uzlabota apstiprinājumu apstrādes uzticamība un izsekošana lielam apstiprinājumu apjomam.

Apstiprināšanas kopas parāda saistīto ierakstu kopējo apstrādes stāvokli. Kad apstiprinājuma ieraksts tiek apstrādāts, izmantojot apstiprināšanas kopu, ieraksts tiek pārvietots no sadaļas **Iesniegts** uz **Apstiprināts** un vairs nav saistīts ar apstiprināšanas kopu. Ja, iesniedzot apstiprināšanai, ieraksts ir nesekmīgs, tam tiek saglabāts statuss **Iesniegts**, un apstiprināšanas kopa tiek atzīmēta kā nesekmīga. Apstiprināšanas kopa reģistrē kļūmes kļūdas ziņojumu.

## <a name="processing-approvals-and-approval-sets"></a>Apstiprinājumu un apstiprināšanas kopu apstrāde
Apstiprinājumi, kas ir ievietoti rindā apstrādei, ir redzami skatā **Apstiprinājumu apstrāde**. Sistēma visus ierakstus apstrādā vairākas reizes asinhroni, ieskaitot apstiprināšanas atkārtošanu, ja iepriekšējie mēģinājumi nav sekmīgi.

Laukā **Apstiprināšanas kopas darbmūžs** tiek reģistrēts atlikušais kopas apstrādes mēģinājumu skaits, pirms tā tiek atzīmēta kā nesekmīga.

Apstiprināšanas kopas tiek apstrādātas, izmantojot periodisko aktivizēšanu, kuras pamatā ir **mākoņa plūsma** ar nosaukumu **Project Service — periodiska projektu apstiprināšanas kopu plānošana**. Tas ir atrodams risinājumā **ar** nosaukumu **Project Operations**. 

Pārliecinieties, vai plūsma ir aktivizēta, veicot tālāk norādītās darbības.

1. Kā administrators piesakieties flow.microsoft.com [...](https://powerautomate.microsoft.com).
2. Augšējā labajā stūrī pārslēdzieties uz vidi, kurai izmantojat Dynamics 365 Project Operations.
3. Atlasiet **Risinājumi**, lai uzskaitītu vidē instalētos risinājumus.
4. Risinājumu sarakstā atlasiet **Project Operations**.
5. Mainiet filtru no **Visi** uz **Mākoņa plūsmas**.
6. Pārbaudiet, **vai project service — periodiski ieplānot projekta apstiprināšanas kopu** plūsma ir iestatīta uz **Ieslēgts**. Ja tā nav, atlasiet plūsmu un pēc tam atlasiet **Ieslēgt**.
7. Pārbaudiet, vai apstrāde notiek ik pēc piecām minūtēm, pārskatot **sarakstu Sistēmas darbi** apgabalā Iestatījumi **savā Project Operations** Dataverse vidē.

## <a name="failed-approvals-and-approval-sets"></a>Nesekmīgi apstiprinājumi un apstiprināšanas kopas
Skatā **Nesekmīgie apstiprinājumi** ir uzskaitīti visi apstiprinājumi, kam nepieciešama lietotāja iejaukšanās. Atveriet saistītos apstiprināšanas kopu žurnālus, lai noteiktu kļūmes iemeslu.
Atlasot **Mēģināt vēlreiz**, tiek palielināts apstiprināšanas kopas darbmūža rādītājs, apstiprināšanas kopai tiek atjaunots statuss **Apstrādā**, un notiek mēģinājums apstrādāt atlikušos ierakstus.

## <a name="configure-approval-sets"></a>Apstiprināšanas kopu konfigurēšana

### <a name="enable-the-approval-sets-feature"></a>Apstiprināšanas kopu līdzekļa iespējošana
Pirms apstiprināšanas kopu līdzekļa iespējošanas pārliecinieties, vai pašlaik netiek apstrādāts neviens apstiprinājums. Kad šis līdzeklis ir iespējots, to nevar atspējot.

- Dodieties uz lapu **Projekta parametri** un atlasiet **Līdzekļu vadība** > **Iespējot mūsdienīgos apstiprinājumus**.

### <a name="configuring-the-asynchronous-threshold"></a>Asinhronā sliekšņa konfigurēšana 
Veidojot apstiprināšanas kopas, apstrāde tiek pārcelta fonā, kad atlasītais apstiprināšanai izvēlēto ierakstu skaits pārsniedz norādīto robežvērtību. Izmantojiet lauku **Asinhronais slieksnis**, lai konfigurētu, kad apstiprinājumu apstrāde jāveic sinhroni vai asinhroni. Atlasiet vienu no sniegtajām vērtībām.

  - nulle: visi pieprasījumi ir jāapstrādā asinhroni; 
  - skaitļi, kas ir lielāki par nulli: apstiprinājumus apstrādā asinhroni tikai tad, ja iesniegto apstiprinājumu skaits pārsniedz šo vērtību.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
