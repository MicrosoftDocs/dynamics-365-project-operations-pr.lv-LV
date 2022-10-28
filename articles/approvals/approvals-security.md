---
title: Drošība un apstiprinājumi
description: Šajā rakstā ir sniegta informācija par drošības iestatījumiem darbam ar apstiprinājumiem korporācijā Microsoft Dynamics 365 Project Operations.
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

Microsoft Dynamics 365 Project Operations izmanto divas drošības lomas, lai varētu apstiprināt laika, izdevumu un materiālu ierakstus:

- Projekta apstiprinātājs
- Projekta apstiprinātāja administrators

## <a name="project-approver"></a>Projekta apstiprinātājs

Jums ir jābūt projekta apstiprinātāja **drošības loma, lai apstiprinātu projekta** laiku, izdevumus un materiālu ierakstus. Jums ir jābūt arī piekļuvei attiecīgajām saistītajām entītijām, piemēram **, Project**. Šo piekļuvi var piešķirt persona, kurai ir **projektu vadītāja** loma. Turklāt jums ir jābūt projekta komandas loceklim un atzīmētam kā apstiprinātājam.

Lai apstiprinātu ar projektu nesaistītus ierakstus, jums ir jābūt iesniedzēja vadītājam.

## <a name="project-approver-admin"></a>Projekta apstiprinātāja administrators

> [!NOTE]
> Lai [varētu izmantot Project Approver administratora funkcionalitāti, ir jābūt iespējotam līdzeklim Apstiprinājuma kopas](approval-sets.md).

Projekta **apstiprinātāja administratora** drošības loma ļauj lietotājiem apiet politikas un apstiprināt ierakstus visos projektos. Šīs lomas piešķiršana apiet validācijas loģiku, kas prasa dalību komandā un atzīmēšanu kā apstiprinātāju. Jums ir jābūt piekļuvei attiecīgajām saistītajām tabulām, piemēram **, Project**, izmantojot jums piešķirtās drošības lomas.

SISTĒMAS lietotāja konteksts apiet validācijas tāpat kā projekta apstiprinātāja administratora drošības loma.
