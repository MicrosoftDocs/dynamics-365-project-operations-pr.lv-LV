---
title: 'Biznesa transakcijas šeit: Project Operations'
description: Šajā rakstā sniegts pārskats par biznesa darījumu jēdzienu programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923289"
---
# <a name="business-transactions-in-project-operations"></a>Biznesa transakcijas šeit: Project Operations

_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_

Programmā Microsoft Dynamics 365 Project Operations biznesa darījums *ir* abstrakts jēdziens, ko nepārstāv neviena entītija. Taču daži kopējie lauki un procesi entītijās ir izstrādāti biznesa transakciju koncepcijas izmantošanai. Šo abstrakciju izmanto tālāk norādītās entītijas.

- Piedāvājuma rindas detaļas
- Līguma rindas detaļas
- Novērtējuma rindas
- Žurnāla rindas
- Faktiski

No šīm entītijām piedāvājuma rindas detaļas, Līguma rindas detaļas un Novērtējuma rindas tiek kartētas uz *projekta dzīves cikla novērtēšanas fāzi*. Žurnāla rindas un faktiskās entītijas tiek kartētas uz *projekta dzīves cikla izpildes fāzi*.

Projekta operācijas visās piecās no šīm entītijām ierakstus uzskata par biznesa darījumiem. Vienīgā atšķirība ir tā, ka ieraksti entītijās, kas ir kartēti uz novērtēšanas fāzi (Detalizēta informācija par piedāvājuma rindu, Līguma rindas detaļas un Budžeta rindas), tiek uzskatīti par *finanšu prognozēm*, savukārt ieraksti entītijās, kas ir kartēti uz izpildes fāzi (Žurnāla rindas un Faktiskie), tiek uzskatīti par *finanšu faktiem*, kas jau ir notikuši.

Papildinformāciju skatiet sadaļās [Novērtējumi](../project-management/estimating-projects-overview.md) un [Faktiskie dati](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepcijas, kas ir unikālas biznesa transakcijām

Biznesa transakciju koncepcijai ir unikālas tālāk norādītās koncepcijas.

- Transakcijas tips
- Transakciju klase
- Transakcijas izcelsme
- Transakcijas savienojums

### <a name="transaction-type"></a>Transakcijas tips

Transakcijas tips norāda projekta finansiālās ietekmes laiku un kontekstu projektā. To definē opciju kopa projekta operācijās ir šādas atbalstītās vērtības:

- izdevumi
- Projekta līgums
- Rēķinā neiekļautā pārdošana
- Rēķinā iekļautā pārdošana
- Starporganizāciju pārdošana
- Resursu struktūrvienības izmaksas

### <a name="transaction-class"></a>Transakciju klase

Transakciju klase norāda dažādus izmaksu tipus, kas rodas projektos. To definē opciju kopa projekta operācijās ir šādas atbalstītās vērtības:

- Laiks
- Izdevumi
- Materiāls
- Maksa
- Atskaites punkts
- Nodoklis

> [!NOTE]
> **Atskaites punkta** vērtību parasti izmanto biznesa loģika fiksētas cenas norēķiniem projektu operācijās.

### <a name="transaction-origin"></a>Transakcijas izcelsme

Darījuma izcelsme ir entītija, kas saglabā katra biznesa darījuma izcelsmi, lai palīdzētu nodrošināt ziņošanu un izsekojamību. Sākoties projekta izpildei, katra biznesa darbība izveido citu biznesa transakciju, kas savukārt izveidos citu biznesa transakciju utt.

### <a name="transaction-connection"></a>Transakcijas savienojums

Transakcijas savienojums ir entītija, kas saglabā saistību starp divām līdzīgām biznesa darbībām, piemēram, izmaksām un saistītajām pārdošanas faktiskajām darbībām vai darbību anulēšanu, ko izraisa norēķinu darbības, piemēram, rēķina apstiprinājums vai rēķinu labojumi.

Kopā transakcijas izcelsme un transakciju savienojuma entītijas palīdz izsekot attiecībām starp biznesa darījumiem un darbībām, kuru dēļ tika izveidota noteikta biznesa darbība.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
