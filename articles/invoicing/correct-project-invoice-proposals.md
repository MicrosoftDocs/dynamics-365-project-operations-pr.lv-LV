---
title: Projekta rēķina melnraksta priekšlikumu uzskaites labošana
description: Šajā tēmā izskaidrots, kā pielāgot ar uzskaiti saistītu informāciju rēķina melnraksta priekšlikumā.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999325"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Projekta rēķina melnraksta priekšlikumu uzskaites labošana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Projekta rēķinu *Operāciju informāciju* uztur projekta vadītājs pro forma rēķinā. Šī detalizētā informācija ietver lēmumu par stundām, izmaksām, materiāliem vai atskaites punktiem, par kuriem jāizraksta rēķins, likmes, kā arī avansa maksājumu un honorāru summu lietojumu. Pēc sākotnējā pro forma rēķina apstiprināšanas varat pielāgot operāciju informāciju, izveidojot un apstiprinot [labojošo pro forma rēķinu](../proforma-invoicing/corrective-invoices.md).

*Uzskaites informācija* projekta rēķiniem tiek uzturēta pret debitoru vērstā rēķina dokumentā. Šī informācija ietver PVN aprēķinu un rēķinā lietotās finanšu dimensijas. Šajā tēmā ir sniegta detalizēta informācija par to, kā šo uzskaites informāciju var pielāgot projekta rēķina melnrakstā.

## <a name="adjust-sales-tax"></a>PVN pielāgošana

Noklusējuma norēķinu PVN grupas un krājumu PVN grupas var pielāgot tieši rēķina priekšlikuma dokumentā. Lai pielāgotu šīs grupas, atlasiet **Rediģēt** un pēc tam katrā projekta rēķina priekšlikuma rindā ievadiet jaunu vērtību laukā **PVN grupa** vai **Krājumu PVN grupa**.

## <a name="adjust-financial-dimensions"></a>Finanšu dimensiju pielāgošana

Finanšu dimensijas nevar rediģēt tieši projekta rēķina priekšlikuma rindā. Tā vietā veiciet tālāk aprakstītās darbības, lai pielāgotu finanšu dimensijas projekta rēķina priekšlikumā.

1. Lai noņemtu projekta rēķina priekšlikuma rindas, projekta rēķina priekšlikumā atlasiet **Dzēst visu**.

    > [!NOTE]
    > Poga **Dzēst visu** ir pieejama tikai pēc tam, kad sistēmas administrators iespējo līdzekli **Dzēst rēķina priekšlikuma rindas, izmantojot Project Operations uz resursiem bāzētos / neuzkrātos scenārijos** darbvietā **Līdzekļu pārvaldība**.

2. Finanšu dimensiju pielāgošana.

    - Sadaļā **Starpkonta darbības (rēķina izrakstīšanas atskaites punkti):** dodieties uz **Visi projekti** \>  **Pārvaldīt** \> **Starpkonta darbības** un atlasiet atskaites punktu, kuru nepieciešams pielāgot. Pēc tam cilnē **Finanšu kategorijas** pēc nepieciešamības atjauniniet vērtības.
    - **Laiks, izmaksas un materiālu transakcijas:** lapā **Publicētās projekta darbības** atlasiet **Pielāgot uzskaiti**, lai atjauninātu finanšu dimensijas.

3. Kad finanšu dimensiju vērtību pielāgošana ir pabeigta, dodieties uz **Projektu pārvaldība un uzskaite** \> **Periodiski** \> **Project Operations integrācija** un atlasiet **Importēt no sagatavošanas tabulas**, lai palaistu periodisko procesu. Šajā procesā tiek izmantotas atjauninātās finanšu dimensiju vērtības, lai atkārtoti izveidotu projekta rēķina priekšlikuma rindas. Pēc projekta rēķina publicēšanas atjauninātās vērtības tiek lietotas projekta apakšgrāmatā un virsgrāmatā.
