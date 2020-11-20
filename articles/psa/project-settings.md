---
title: Projekta iestatījumi
description: Šajā tēmā ir sniegta informācija par projekta pārvaldības iestatījumiem.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123117"
---
# <a name="project-settings"></a>Projekta iestatījumi

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Lai piekļūtu projekta plānošanas līdzekļiem, izmantojiet tālāk norādītos iestatījumus.

## <a name="work-template"></a>Darba veidne

Lai izveidotu projekta grafiku, jums ir jāizveido projekta kalendāra veidne, kas nosaka darba stundu skaitu vienā dienā un visus uzņēmuma slēgšanas gadījumus. Lai izveidotu projekta kalendāra veidni, jums ir jāsasaista darba veidne un lauks **Kalendāra veidne** šim projektam. Lai izveidotu darba veidni, izpildiet tālāk aprakstītās darbības.

1. Programmatūras PSA kreisajā navigācijas rūtī noklikšķiniet uz **Resursi**. 
2. Saraksta lapā **Resursi** atveriet lietotāja ierakstu un pēc tam atlasiet vienumu **Rādīt darba stundas**.

  > [!NOTE]
  > Pārliecinieties, ka pārlūkprogrammas lapā ir atļauti uznirstošie elementi. Šādi jūs varat apskatīt attiecīgajam resursam iestatītās darba stundas.
  
3. Cilnē **Mēneša skats** noklikšķiniet uz **Iestatīt**. Tiek parādīts saraksts ar trīs opcijām: 

  - Jauns nedēļas grafiks
  - Darba grafiks vienai dienai
  - Brīvais laiks

> ![Iestatīšanas opcijas](media/project-13.png)

4. Atlasiet **Jauns nedēļas grafiks** un pēc tam iestatiet opcijas šī resursa grafikam. Varat iestatīt periodisku nedēļas grafiku, dienas stundu parametrus, uzņēmuma slēgšanas gadījumus un citus rādītājus.
5. Iestatiet datumu diapazonu, atlasiet **Saglabāt** un pēc tam noklikšķiniet uz **Aizvērt**. 
6. Atgriezieties saraksta lapā **Resursi** un atlasiet resursu, kuram iestatījāt darba stundas. 
7. Atlasiet **Iestatīt kalendāru kā**, lai iestatītu darba veidni. 
8. Dialoglodziņā **Darba veidne** ievadiet nosaukumu šai darba veidnei un pēc tam atlasiet **Lietot**. 

Tagad šo darba veidni varat sasaistīt ar projekta kalendāra veidni.

## <a name="resource-roles"></a>Resursu lomas

Termins *resursa loma* attiecas uz prasmju, kompetenču un sertifikāciju kopu, kas personai ir nepieciešams, lai projektā varētu veikt noteiktu uzdevumu kopu. Programmatūra PSA ļauj jums noteikt izmaksas un norēķinus resursa laikam, pamatojoties uz lomu, ar kādu šis resurss ir saistīts. Katrai organizācijai ir jāiestata šīs lomas, izmantojot kreiso navigāciju izvēlnē **Project Service**.

Katrai organizācijai šīs lomas ir jāiestata lapā **Aktīvās resursu kategorijas**. Lai atvērtu šo lapu, kreisajā navigācijas rūtī atlasiet **Resurss lomas**.

## <a name="price-lists"></a>Cenrāži

Cenrāži ļauj jums iestatīt izmaksas un pārdošanas cenas resursu lomām, izmaksu kategorijām, produktiem un citiem elementiem kādā organizācijā. Pirms iestatāt finanšu tāmes darbam, kurš ir jāizpilda kādam projektam, jums ir jāizveido dublējuma izmaksu un pārdošanas cenrādis. Parametru sadaļā jums ir jāiestata arī noklusējuma izmaksu un pārdošanas cenrādis, kas attiecas uz visiem šajā organizācijā izveidotajiem projektiem. Lapā **Aktīvie projektu parametri** pārliecinieties, ka iestatāt noklusējuma izmaksu un pārdošanas cenrādi.
