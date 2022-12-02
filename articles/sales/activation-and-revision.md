---
title: Projekta piedāvājuma aktivizēšana un pārskatīšana
description: Šajā rakstā ir sniegta informācija par piedāvājumu aktivizēšanu un pārskatīšanu programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410380"
---
# <a name="activate-and-revise-a-project-quote"></a>Projekta piedāvājuma aktivizēšana un pārskatīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Aktivizēšanas un pārskatīšanas iespējas palīdz izsekot projekta piedāvājumu versijām aprēķinu un apspriešanas laikā. Kad piedāvājuma melnraksts ir aktivizēts, tas kļūst tikai lasāms.

Aktivizēšanas un pārskatīšanas iespējas ļauj šādus uzdevumus:

- iegūt vai zaudēt piedāvājumus tikai pēc aktivizēšanas;
- pārskatīt piedāvājumu, lai veiktu izmaiņas esošajā piedāvājumā vai izveidotu jaunu versiju.

> [!NOTE]
> Pēc piedāvājumu aktivizēšanas un pārskatīšanas līdzekļa iespējošanas to nevar atspējot.

Lai ieslēgtu iespēju aktivizēt un pārskatīt projekta piedāvājumus, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Iestatījumi** \> **Parametri**.
1. Atveriet ierakstu **Parametri**.
1. Darbību rūts cilnē **Līdzekļu vadība** atlasiet **Iespējot piedāvājumu aktivizēšanu un pārskatīšanu**.
1. Apstiprinājuma dialoglodziņā atlasiet **Labi**.
1. Pēc brīža atsvaidziniet pārlūkprogrammu. Tagad aktivizēšanas un pārskatīšanas iespējām ir jābūt pieejamām. Varēsiet noteikt, ka šīs iespējas ir iespējotas, ja darbību rūtī vairs nav redzama poga **Iespējot piedāvājumu aktivizēšanu un pārskatīšanu**.

## <a name="activating-a-quote"></a>Piedāvājuma aktivizēšana

Pēc piedāvājumu aktivizēšanas un pārskatīšanas līdzekļa iespējošanas pogas **Iegūta piedāvājuma slēgšana** un **Zaudēta piedāvājuma slēgšana** darbību rūtī projektu piedāvājumu melnrakstiem nav pieejamas. Tās ir pieejamas tikai pēc tam, kad piedāvājums ir aktivizēts.

Aktivizēšana ir piedāvājuma procesa posms, kad vēlaties novērst papildu izmaiņas piedāvājumā. Šajā posmā piedāvājums tiek nosūtīts iekšējai pārskatīšanai vai klientam.

Aktivizētajiem piedāvājumiem darbību rūtī ir pieejamas pogas **Iegūta piedāvājuma slēgšana** un **Zaudēta piedāvājuma slēgšana**. Atkarībā no iekšējās vai klienta pārskatīšanas rezultāta varat izmantot vienu no šīm pogām, lai slēgtu aktivizētu piedāvājumu. Aktivizētajiem piedāvājumiem varat veikt apspriešanu un izmaiņas, atlasot opciju **Pārskatīt piedāvājumu**.

## <a name="revising-a-quote"></a>Piedāvājuma pārskatīšana

Ja aktivizētā piedāvājumā jāveic izmaiņas, atlasiet **Pārskatīt piedāvājumu**. Piedāvājums tiek slēgts, un tiek izmantots iemesla kods **pārskatīts**. Pēc tam tiek izveidots jauns piedāvājums ar tādu pašu ID un palielinātu pārskatīšanu skaitu. Visa detalizētā informācija no sākotnējā piedāvājuma tiek pārkopēta uz jauno piedāvājumu. Jaunajam piedāvājumam ir melnraksta statuss, un to var rediģēt pēc vajadzības.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
