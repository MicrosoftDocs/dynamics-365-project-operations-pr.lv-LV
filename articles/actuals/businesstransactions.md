---
title: 'Biznesa transakcijas šeit: Project Operations'
description: Šajā rakstā sniegts pārskats par biznesa transakciju koncepciju programmā Microsoft Dynamics 365 Project Operations.
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

Programmā Microsoft Dynamics 365 Project Operations *biznesa transakcija* ir abstrakta koncepcija, ko nepārstāv neviena entītija. Taču daži kopējie lauki un procesi entītijās ir izstrādāti biznesa transakciju koncepcijas izmantošanai. Šo abstrakciju izmanto tālāk norādītās entītijas.

- Piedāvājuma rindas detaļas
- Līguma rindas detaļas
- Novērtējuma rindas
- Žurnāla rindas
- Faktiski

No šīm entītijām Piedāvājuma rindas informācija, Līguma rindas informācija un Aprēķinu rindas tiek kartētas uz projekta dzīves cikla *aprēķinu fāzi*. Entītijas Žurnāla rindas un Faktiskās entītijas tiek kartētas uz projekta dzīves cikla *izpildes fāzi*.

Project Operations ierakstus visās šajās piecās entītijās apstrādā kā biznesa transakcijas. Vienīgā atšķirība ir tāda, ka ieraksti entītijās, kas ir kartētas uz aprēķinu fāzi (piedāvājuma rindu informācija, līgumu rindu informācija un aprēķinu rindas), tiek uzskatīti par *finanšu prognozēm*, bet ieraksti entītijās, kas ir kartētas uz izpildes fāzi (žurnāla rindas un faktiskie dati), tiek uzskatīti par *finanšu faktiem*, kas jau ir notikuši.

Papildinformāciju skatiet sadaļās [Novērtējumi](../project-management/estimating-projects-overview.md) un [Faktiskie dati](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepcijas, kas ir unikālas biznesa transakcijām

Biznesa transakciju koncepcijai ir unikālas tālāk norādītās koncepcijas.

- Transakcijas tips
- Transakciju klase
- Transakcijas izcelsme
- Transakcijas savienojums

### <a name="transaction-type"></a>Transakcijas tips

Transakcijas tips norāda projekta finansiālās ietekmes laiku un kontekstu projektā. To definē opciju kopa, kam programmā Project Operations ir tālāk norādītās atbalstītās vērtības.

- izdevumi
- Projekta līgums
- Rēķinā neiekļautā pārdošana
- Rēķinā iekļautā pārdošana
- Starporganizāciju pārdošana
- Resursu struktūrvienības izmaksas

### <a name="transaction-class"></a>Transakciju klase

Transakciju klase norāda dažādus izmaksu tipus, kas rodas projektos. To definē opciju kopa, kam programmā Project Operations ir tālāk norādītās atbalstītās vērtības.

- Laiks
- Izdevumi
- Materiāls
- Maksa
- Atskaites punkts
- Nodoklis

> [!NOTE]
> Vērtību **Atskaites punkts** parasti izmanto biznesa loģika fiksētas cenas norēķiniem programmā Project Operations.

### <a name="transaction-origin"></a>Transakcijas izcelsme

Transakcijas izcelsme ir entītija, kas saglabā katras biznesa transakcijas izcelsmes vietu, lai palīdzētu veidot pārskatus un veikt izsekošanu. Kad tiek sākta projekta izpilde, katra biznesa transakcija izveido vēl vienu biznesa transakciju, kas savukārt izveido vēl vienu biznesa transakciju un tā tālāk.

### <a name="transaction-connection"></a>Transakcijas savienojums

Transakcijas savienojums ir entītija, kas glabā attiecības starp divām līdzīgām biznesa transakcijām, piemēram, izmaksām un saistītajiem pārdošanas faktiskajiem datiem vai transakciju anulēšanu, ko izraisa tādas norēķinu darbības kā rēķina apstiprinājums vai rēķina labojumi.

Kopā entītijas Transakcijas izcelsme un Transakcijas savienojums palīdz izsekot relācijas starp biznesa transakcijām un darbībām, kas izraisa noteiktas biznesa transakcijas izveidi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
