---
title: Drošība un apstiprinājumi
description: Šajā rakstā ir sniegta informācija par drošības iestatījumiem darbam ar apstiprinājumiem Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709407"
---
# <a name="security-and-approvals"></a>Drošība un apstiprinājumi

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Microsoft Dynamics 365 Project Operations izmanto divas drošības lomas, lai atļautu laika, izdevumu un materiālu ierakstu apstiprināšanu.

- Projekta apstiprinātājs
- Projekta apstiprinātājs administrators

## <a name="project-approver"></a>Projekta apstiprinātājs

Lai apstiprinātu projekta laika, izdevumu un materiālu ierakstus, ir nepieciešama drošības loma **Projekta apstiprinātājs**. Ir jābūt piekļuvei arī attiecīgajām saistītajām entītijām, piemēram, **Projekts**. Šādu piekļuvi var piešķirt kāds lietotājs, kuram ir loma **Projekta vadītājs**. Turklāt jums ir jābūt projekta darba grupas dalībniekam un atzīmētam kā apstiprinātājam.

Lai apstiprinātu ar projektu nesaistītus ierakstus, ir jābūt iesniedzēja vadītājam.

## <a name="project-approver-admin"></a>Projekta apstiprinātājs administrators

> [!NOTE]
> Lai varētu izmantot projekta apstiprinātāja administratora funkcionalitāti, vispirms ir jāiespējo līdzeklis [Apstiprināšanas kopas](approval-sets.md).

Drošības loma **Projekta apstiprinātājs administrators** lietotājiem ļauj apiet politikas un ļauj apstiprināt ierakstus visos projektos. Piešķirot šo lomu, tiek apieta validācijas loģika, kurai ir nepieciešama darba grupas dalība un apstiprinātāja apzīmējums. Ir jābūt piekļuvei attiecīgajām saistītajām tabulām, piemēram, **Projekts**, izmantojot jums piešķirtās drošības lomas.

Sistēmas lietotāja konteksts apiet validācijas tāpat kā projekta apstiprinātāja administratora drošības loma.
