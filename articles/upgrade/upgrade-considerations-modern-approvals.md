---
title: Jaunināšanas apsvērumi par mūsdienu apstiprinājumiem
description: Rakstā ir aplūkoti punkti, kas administratoriem jāņem vērā, iespējojot mūsdienu apstiprinājumu funkcionalitāti.
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
# <a name="upgrade-considerations-for-modern-approvals"></a>Jaunināšanas apsvērumi par mūsdienu apstiprinājumiem 

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

2022. gada aprīļa 1. viļņa laidiena ietvaros mūsdienu apstiprinājumu funkcionalitāte tiks iespējota pēc noklusējuma. Šī funkcionalitāte uzlabo apstiprināšanas loģikas uzticamību un nodrošina, ka varat noteikt iemeslu, ja apstiprinājuma loģika neizdodas.

Šo izmaiņu ietvaros tiek atjauninātas projektu apstiprinājumu statusa izmaiņas. Tagad statuss ir tieši no **Iesniegts** uz **Apstiprināts**. **Gaida** vairs nav apstiprinājumu statuss. Lai noteiktu, vai apstiprinājums vēl nav saņemts, pārbaudiet, vai apstiprinājums ir daļa no apstiprinājuma kopas, un pārskatiet pievienotās apstiprinājuma kopas stāvokli.

## <a name="before-you-upgrade"></a>Pirms jaunināšanas

Pirms jaunināšanas uz modernajiem apstiprinājumiem pārliecinieties, vai jums nav gaidošu apstiprinājumu. Mūsdienu apstiprinājumi neizmanto **statusu Gaida**. Tāpēc visi apstiprinājumi, kas pēc jaunināšanas joprojām ir atzīmēti kā **gaidoši**, netiks apstrādāti.

## <a name="after-you-upgrade"></a>Pēc jaunināšanas

Pēc jaunināšanas uz mūsdienu apstiprinājumiem administratoram ir jāpārbauda, vai ir iespējota mākoņa plūsma, kas apstrādā apstiprinājumus.

1. Piesakieties [flow.microsoft.com](https://flow.microsoft.com)
2. Lapas augšējā labajā stūrī pārslēdziet vidi uz jaunināto vidi.
3. Atlasiet **Risinājumi**, lai uzskaitītu vidē instalētos risinājumus.
4. Risinājumu sarakstā atlasiet **Projekta operācijas** vai **Projekta pakalpojums**.
5. Mainiet filtru no **Visas** uz **Mākoņa plūsmas**.
6. Pārbaudiet, **vai opcija Project Service — Recurrently Schedule Project Approval Sets (Projekta pakalpojums — atkārtoti plānot projektu apstiprināšanas kopas**) ir iestatīta uz **Ieslēgta**. Ja tā nav, atlasiet plūsmu un pēc tam atlasiet **Ieslēgt**.
7. Pārbaudiet, vai apstrāde notiek ik pēc piecām minūtēm, pārskatot **sistēmas uzdevumu** sarakstu apgabalā **Iestatījumi**.

## <a name="short-term-rollback"></a>Īstermiņa atcelšana

Ja nevarat veikt izmaiņas vai rodas nopietna problēma ar šo līdzekli, varat īslaicīgi atgriezties pie sākotnējās apstiprinājuma plūsmas, veicot šādas darbības:
1. Pierakstieties savā vidē un pārbaudiet, vai nav gaidošu apstiprinājumu.
2. Dodieties uz **Iestatījumi** > **Projekta parametri**.
3. Atlasiet **Līdzekļu kontrole** un pēc tam atlasiet **Mūsdienīgi apstiprinājumi**, lai izslēgtu līdzekli.

## <a name="removing-the-feature-flag"></a>Notiek līdzekļa karodziņa noņemšana

2022. gada oktobra 2. viļņa atjauninājumā tiks noņemta iespēja izslēgt šo funkciju.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
