---
title: Apakšsadarbību pārvaldība programmā Project Operations
description: Šajā tēmā sniegts pārskats par pilnīgu apakšlīgumu pārvaldības procesu programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994240"
---
# <a name="subcontract-management-in-project-operations"></a>Apakšsadarbību pārvaldība programmā Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Apakšlīgumu slēgšana programmā Microsoft Dynamics 365 Project Operations atbalsta tālāk norādīto biznesa procesa plūsmu.

![Apakšlīgumu slēgšanas procesa plūsma](../media/SubcontractingProcessFlow.png)

Tālāk ir sniegts detalizēts apakšlīgumu slēgšanas procesa apraksts.

1. Projekta vadītājs izveido apakšlīgumu ar pārdevēju. Pēc noklusējuma apakšlīgumam tiek izmantoti pārdevēja ierakstam pievienotie cenrāži. Pārdevēja uzņēmuma attiecību tips ir **Pārdevējs** vai **Piegādātājs**.
2. Projekta vadītājs var norādīt visus pirkumus kā apakšlīguma rindas elementus. Apakšlīguma rindas var būt laiks, izmaksas vai produkti. Katrā apakšlīguma rindā atlasītā transakciju klase nosaka, kam šī rinda ir paredzēta.
3. Pārdevēja uzņēmuma pārvaldnieks un projekta vadītājs var atkārtoti veikt darbības apakšlīgumā. Cenu noteikšanu var pielāgot apakšlīgumam pievienotajos pirkumu cenrāžos.
4. Šajā posmā vai vēlāk procesā, ja apakšlīguma rinda paredzēta laikam, pārdevēja uzņēmuma pārvaldnieks saista kontaktpersonas ar katru apakšlīguma rindu. Šī saistība nodrošina informāciju projekta vadītājam, kurš strādā pie apakšlīguma izveides. Kad kontaktpersona ir saistīta ar apakšlīguma rindu, sistēma automātiski izveido rezervējamu resursu no kontaktpersonas, ja rezervējamais resurss vēl nepastāv.
5. Katras apakšlīguma rindas norēķinu metode var būt **Fiksēta cena** vai **Laiks un materiāli**. Fiksētas cenas apakšlīgumu rindām var iestatīt uz atskaites punktu balstītu rēķinu grafiku.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
