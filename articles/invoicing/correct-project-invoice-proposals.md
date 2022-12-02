---
title: Projekta rēķina melnraksta priekšlikumu uzskaites labošana
description: Šajā rakstā izskaidrots, kā pielāgot ar uzskaiti saistītu informāciju rēķina melnraksta priekšlikumā.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921219"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Projekta rēķina melnraksta priekšlikumu uzskaites labošana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Projekta rēķinu *Operāciju informāciju* uztur projekta vadītājs pro forma rēķinā. Šī detalizētā informācija ietver lēmumu par stundām, izmaksām, materiāliem vai atskaites punktiem, par kuriem jāizraksta rēķins, likmes, kā arī avansa maksājumu un honorāru summu lietojumu. Pēc sākotnējā pro forma rēķina apstiprināšanas varat pielāgot operāciju informāciju, izveidojot un apstiprinot [labojošo pro forma rēķinu](../proforma-invoicing/corrective-invoices.md).

*Uzskaites informācija* projekta rēķiniem tiek uzturēta pret debitoru vērstā rēķina dokumentā. Šī informācija ietver PVN aprēķinu un rēķinā lietotās finanšu dimensijas. Šajā rakstā ir sniegta detalizēta informācija par to, kā šo uzskaites informāciju var pielāgot projekta rēķina melnrakstā.

## <a name="adjust-sales-tax"></a>PVN pielāgošana

Noklusējuma norēķinu PVN grupas un krājumu PVN grupas var pielāgot tieši rēķina priekšlikuma dokumentā. Lai pielāgotu šīs grupas, atlasiet **Rediģēt** un pēc tam katrā projekta rēķina priekšlikuma rindā ievadiet jaunu vērtību laukā **PVN grupa** vai **Krājumu PVN grupa**.

## <a name="adjust-financial-dimensions"></a>Finanšu dimensiju pielāgošana

### <a name="header-dimensions"></a>Galvenes izmēri

Pēc noklusējuma rēķina finanšu dimensijas ir atvasinātas no rēķinā neiekļautajiem projekta transakciju ierakstiem, par kuriem tiek izrakstīts rēķins. Taču sistēmas iestatījumi ļauj projekta rēķinu priekšlikumu galvenē izmantot finanšu dimensijas, lai publicētu klientu bilances. Lai iespējotu šo funkcionalitāti, atlasiet **Atļaut projektu dimensiju atjauninājumus debitoriem** cilnē **Finanšu dati**, kas atrodas lapā **Projektu pārvaldības un uzskaites parametri**.

Rēķinu galveņu finanšu dimensijas var rediģēt pirms rēķina grāmatošanas. Lapā **Projekta rēķinu priekšlikums** pārslēdzieties uz skatu **Galvene** un pēc tam rediģējiet vērtības cilnē **Finanšu dimensijas**.

Skats **Galvene** ir pieejams tikai pēc tam, kad sistēmas administrators iespējo līdzekli **Izmantot Projekta rēķinu priekšlikumu un rēķinu žurnālu veidlapas ar Galvenes un Rindu skatu** darbvietā **Līdzekļu pārvaldība**. Šim līdzeklim ir nepieciešams Finance atjauninājums 10.0.25 vai jaunāka versija.

### <a name="line-dimensions"></a>Rindas dimensijas

Finanšu dimensijas nevar rediģēt tieši projekta rēķina priekšlikuma rindā. Tā vietā veiciet tālāk aprakstītās darbības, lai pielāgotu finanšu dimensijas projekta rēķina priekšlikumā.

1. Lai noņemtu projekta rēķina priekšlikuma rindas, projekta rēķina priekšlikumā atlasiet **Dzēst visu**.

    Poga **Dzēst visu** ir pieejama tikai pēc tam, kad sistēmas administrators iespējo līdzekli **Dzēst rēķina priekšlikuma rindas, izmantojot Project Operations uz resursiem bāzētos / neuzkrātos scenārijos** darbvietā **Līdzekļu pārvaldība**.

2. Finanšu dimensiju pielāgošana.

    - Sadaļā **Starpkonta darbības (rēķina izrakstīšanas atskaites punkti):** dodieties uz **Visi projekti** \>  **Pārvaldīt** \> **Starpkonta darbības** un atlasiet atskaites punktu, kuru nepieciešams pielāgot. Pēc tam cilnē **Finanšu kategorijas** pēc nepieciešamības atjauniniet vērtības.
    - **Laiks, izmaksas un materiālu transakcijas:** lapā **Publicētās projekta darbības** atlasiet **Pielāgot uzskaiti**, lai atjauninātu finanšu dimensijas.

3. Kad finanšu dimensiju vērtību pielāgošana ir pabeigta, dodieties uz **Projektu pārvaldība un uzskaite** \> **Periodiski** \> **Project Operations integrācija** un atlasiet **Importēt no sagatavošanas tabulas**, lai palaistu periodisko procesu. Šajā procesā tiek izmantotas atjauninātās finanšu dimensiju vērtības, lai atkārtoti izveidotu projekta rēķina priekšlikuma rindas. Pēc projekta rēķina publicēšanas atjauninātās vērtības tiek lietotas projekta apakšgrāmatā un virsgrāmatā.
