---
title: Izdevumu pārvaldības darbplūsma
description: Šajā tēmā ir paskaidrots, kā sistēmā Microsoft Dynamics 365 Finance izmantot darbplūsmas sistēmu, lai izmaksu pārvaldībā iestatītu atsauksmju sniegšanas procesu par izmaksu atskaitēm.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2a2cae435342139f32d1bb5d38d68acd920453f5e6f6551e1f6d57967d8053
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001305"
---
# <a name="expense-management-workflow"></a>Izdevumu pārvaldības darbplūsma

Varat izmantot darbplūsmas sistēmu, lai izmaksu pārvaldībā iestatītu atsauksmju sniegšanas procesu par izmaksu atskaitēm. Varat iestatīt darbplūsmu, kas izmanto tālāk norādītos kritērijus, lai noteiktu, kurš apstiprina izmaksu atskaites.

- Darbinieku atskaišu izveides hierarhija un iepriekš noteikti apstiprināšanas ierobežojumi
- Vairāku līmeņu apstiprināšana, kas atbalsta pagaidu apstiprinātājus un galīgo apstiprinātāju
- Finanšu rādītāji un projekta atbildība
- Piešķiršana noteiktiem lietotājiem vai lietotāju grupām

Darbplūsmas apstiprinājumus var izveidot izdevumu atskaitēm, ceļojumu pieprasījumiem, naudas avansiem un pievienotās vērtības nodokļa (PVN) atmaksāšanai.

**Piemērs**

Tālāk minētais process ir izmaksu atskaites izmaksu pārvaldības darbplūsmas piemērs.

1. Darbinieks izveido un saglabā izmaksu atskaiti.
2. Darbinieks iesniedz izdevumu atskaiti apstiprināšanai. Apstiprinātājs tiek noteikts, pamatojoties uz kārtulām, kas tika definētas, iestatot darbplūsmu.
3. Apstiprinātājs saņem paziņojumu, ka izdevumu atskaite ir gatava apstiprināšanai. Apstiprinātājs pārskata izmaksu atskaiti un pārbauda, vai ir izpildīti tālāk minētie nosacījumi.

    - Izdevumi nepārkāpj nevienu izdevumu politiku. Ja izdevumi pārkāpj politiku, apstiprinātājs pārbauda, vai izmaksu atskaitē ir iekļauts derīgs komerciāls pamatojums.
    - Izmaksu atskaitei ir pievienotas elektroniskas kvītis.

4. Apstiprinātājs apstiprina izdevumu atskaiti.
5. Izdevumu atskaite tiek piešķirta kreditoru koordinatoram grāmatošanai.
6. Tiek veikta viena no tālāk minētajām darbībām atkarībā no tā, vai ir konfigurēta automātiskā grāmatošana.

    - Ja ir konfigurēta automātiskā grāmatošana, izmaksu atskaite tiek apstrādāta maksājumam un izmaksu atskaites statuss tiek atjaunināts.
    - Ja automātiskā grāmatošana nav konfigurēta, kreditoru koordinators pārbauda, vai ir iesniegtas visi oriģinālās kvītis un vai kvītis atbilst izdevumu atskaitē norādītajiem izdevumiem. Visiem nodokļu kodiem, kas ievadīti izdevumu atskaitē, arī ir jābūt pārbaudītiem.

Kad šīs prasības ir pārbaudītas, izmaksu atskaite tiek iegrāmatota.

Pēc tam, kad izmaksu atskaite ir iegrāmatota, maksājums ir atļauts izdevumu atskaitei, un darbiniekam tiek piešķirta atmaksa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]