---
title: Mūsdienīgu apstiprinājumu jaunināšanas apsvērumi
description: Rakstā ir apskatīti punkti, kas administratoriem jāapsver, iespējojot mūsdienīgo apstiprinājumu funkcionalitāti.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931753"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Mūsdienīgu apstiprinājumu jaunināšanas apsvērumi 

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Mūsdienīgo apstiprinājumu funkcionalitāte tiks iespējota kā daļa no 2022. gada aprīļa 1. laidiena pēc noklusējuma. Šī funkcionalitāte uzlabo apstiprinājumu loģikas uzticamību un nodrošina, ka varat noteikt iemeslu, ja apstiprinājuma loģika neizdodas.

Šo izmaiņu ietvaros tiek atjauninātas projektu apstiprinājumu statusu izmaiņas. Tagad statuss tiek nomainīts tieši no **Iesniegts** uz **Apstiprināts**. **Gaida** vairs nav apstiprinājuma statuss. Lai noteiktu, vai apstiprinājums vēl gaida, pārbaudiet, vai apstiprinājums ir daļa no apstiprinājumu kopas, un pārbaudiet pievienotās apstiprinājumu kopas statusu.

## <a name="before-you-upgrade"></a>Pirms jaunināšanas

Pirms jaunināšanas uz mūsdienīgajiem apstiprinājumiem pārliecinieties, ka jums nav gaidošu apstiprinājumu. Mūsdienīgajiem apstiprinājumiem netiek izmantots statuss **Gaida**. Tāpēc visi apstiprinājums, kas pēc jaunināšanas joprojām ir atzīmēti ar **Gaida**, netiks apstrādāti.

## <a name="after-you-upgrade"></a>Pēc jaunināšanas

Pēc jaunināšanas uz mūsdienīgajiem apstiprinātajiem administratoram ir jāpārbauda, vai ir iespējota mākoņa plūsma, kas apstrādā apstiprinājumus.

1. Pierakstieties vietnē [flow.microsoft.com](https://flow.microsoft.com)
2. Lapas augšējā labajā stūrī pārslēdziet vidi uz jaunināto vidi.
3. Atlasiet **Risinājumi**, lai uzskaitītu vidē instalētos risinājumus.
4. Risinājumu sarakstā atlasiet **Project Operations** vai **Project Service**.
5. Mainiet filtru no **Visi** uz **Mākoņa plūsmas**.
6. Pārbaudiet, vai opcija **Project Service - regulāri ieplānot projektu apstiprināšanas kopas** ir iestatīta kā **Ieslēgta**. Ja tā nav, atlasiet plūsmu un pēc tam atlasiet **Ieslēgt**.
7. Pārbaudiet, vai apstrāde notiek ik pēc piecām minūtēm, pārskatot sarakstu **Sistēmas uzdevumi** apgabalā **Iestatījumi**.

## <a name="short-term-rollback"></a>Īstermiņa atrite

Ja nevarat ieviest izmaiņas vai rodas nopietnas problēmas ar šo līdzekli, varat īslaicīgi atjaunot sākotnējo apstiprinājumu plūsmu, veicot tālāk norādītās darbības.
1. Pierakstieties savā vidē un pārbaudiet, vai nav gaidošu apstiprinājumu.
2. Pārejiet uz sadaļu **Iestatījumi** > **Projekta parametri**.
3. Atlasiet **Līdzekļu vadība** un pēc tam atlasiet **Mūsdienīgie apstiprinājumi**, lai izslēgtu līdzekli.

## <a name="removing-the-feature-flag"></a>Līdzekļa karodziņa noņemšana

2022. gada oktobra 2. laidiena atjauninājumā iespēja izslēgt šo līdzekli tiks noņemta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
