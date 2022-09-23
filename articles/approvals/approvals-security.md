---
title: Drošība un apstiprinājumi
description: Šajā rakstā ir sniegta informācija par drošības iestatījumiem darbam ar Microsoft apstiprinājumiem Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525408"
---
# <a name="security-and-approvals"></a>Drošība un apstiprinājumi

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Microsoft Dynamics 365 Project Operations izmanto divas drošības lomas, lai varētu apstiprināt laika, izdevumu un materiālu ierakstus:

- Projekta apstiprinātājs
- Projekta apstiprinātāja administrators

## <a name="project-approver"></a>Projekta apstiprinātājs

Lai apstiprinātu projekta laiku, izdevumus un materiālu ierakstus **, jums ir jābūt drošības loma projekta apstiprinātājam**. Jums ir jābūt arī piekļuvei attiecīgajām saistītajām entītijām, piemēram **, Project**. Šo piekļuvi var piešķirt persona, kurai ir **projekta vadītāja** loma. Turklāt jums ir jābūt projekta komandas loceklim un jāatzīmē kā apstiprinātājs.

Lai apstiprinātu ar projektu nesaistītus darbus, jums ir jābūt iesniedzēja vadītājam.

## <a name="project-approver-admin"></a>Projekta apstiprinātāja administrators

> [!NOTE]
> Lai [varētu izmantot project approver admin funkcionalitāti, ir jābūt iespējotam līdzeklim Apstiprināšanas kopas](approval-sets.md).

**Project Approvalr Administrator** drošības loma ļauj lietotājiem apiet politikas un ļauj apstiprināt ierakstus visos projektos. Piešķirot šo lomu, tiks apieta validācijas loģika, kas prasa dalību darba grupā un atzīmēšanu kā apstiprinātāju. Jums ir jābūt piekļuvei attiecīgajām saistītajām entītijām, piemēram **, Project**. Šo piekļuvi var piešķirt persona, kurai ir **projekta vadītāja** loma.

SISTĒMAS lietotāja konteksts apiet validācijas tādā pašā veidā kā projekta apstiprinātāja administratora drošības loma.
