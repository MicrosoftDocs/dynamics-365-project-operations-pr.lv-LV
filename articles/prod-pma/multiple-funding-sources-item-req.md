---
title: Elementu prasības projekta līgumiem ar vairākiem avotiem+
description: Šajā rakstā ir sniegta informācija par to, kā konfigurēt un izmantot elementu prasības ar vairākiem finansējuma avotiem.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028497"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Elementu prasības projekta līgumiem ar vairākiem avotiem+

_**Attiecas uz:** Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem_

Daži līgumi, kuru pamatā ir projektos balstīti nodevumi, nosaka vajadzību pēc vairākiem finansējuma avotiem. Šajā rakstā izskaidrots, kā atlasīt un konfigurēt vēlamos avotus, ja projektam vai projekta līgumam ir vajadzīgi vairāki avoti.

## <a name="terminology"></a>Terminoloģija

- **Finansējuma avots** — entitīja, kas finansē projekta līguma darbu. Šī entitīja var būt iekšēja organizācija vai ārējs rēķina konts (klients vai piešķīrums).
- **Projekta klients** — entītija, kurai tiek sniegts projekta darbs.
- **Rēķina uzņēmums** — ārēja entītija, kas maksā par projekta darbu.

## <a name="example"></a>Piemērs

Contoso ir ieguvis aprīkojuma atjaunošanas līgumu ar diviem no tā klientiem: Adatum US un Adatum Corporate. Līgumā ir iekļauti aparatūras un instalēšanas pakalpojumi, kas tiks piegādāti Uz Adatum US (projekta klients). Aparatūras darbību finansē Adatum Corporate (1. rēķina uzņēmums), un instalācijas darbu finansēs Adatum US (2. rēķina uzņēmums).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Rēķina uzņēmuma noklusējuma kārtulu iestatīšana elementu prasībām

### <a name="prerequisites"></a>Priekšnoteikumi

- Lai lietotu elementu prasības ar vairākiem rēķinu uzņēmumiem, ir vajadzīga Microsoft Dynamics 365 Finance **10.0.27. versija vai jaunāka versija**.
- Sistēmas administratoram ir jāiespējo līdzeklis **Atļaut elementu prasības ar vairākiem finansējuma avotiem Project Operations krājumu/ražošanas scenārijos**, kas pieejams darbvietā **Līdzekļu pārvaldība**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Rēķina uzņēmuma noklusējuma kārtulu iestatīšana

Lai rēķina uzņēmumam iestatītu noklusējuma kārtulas, veiciet tālāk uzskaitītās darbības.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Projekta pārvaldības un grāmatvedības parametri**.
1. Cilnē **Vispārīgi**, sadaļā **Pārdošanas pasūtījumi un elementu prasības** iestatiet opciju **Atļaut projektus ar vairākiem finansējuma avotiem** uz vērtību **Jā**.
1. Laukā **Noklusējuma klients** norādiet, no kurienes pēc noklusējuma tiek ņemts elementa prasības projekta piegādes klients:

    - **No finansējuma avota** — Noklusējuma projekta piegādes klients tiek ņemts no finansējuma avota. Ja ar projekta līgumu ir saistīti vairāki finansējuma avoti, kas saistīti ar projektu, tiks izmantots pirmais sarakstā parādītais finansējuma avots.
    - **No projekta** — noklusējuma projekta piegādes klients tiek ņemts no klienta, kas ir atlasīts laukā **Projekta ieraksta uzņēmums**.

1. Neobligāti: Iestatiet vai mainiet projekta ierakstu noklusējuma rēķina uzņēmumu:

    1. Dodieties uz **Projektu pārvaldība un uzskaits** \>**Projekti** \>**Visi projekti** un atveriet projekta ieraksta informāciju.
    2. Cilnē **Vispārīgi** iestatiet vai atjauniniet lauku **Noklusējuma rēķina uzņēmums**. Jūsu norādītais konts tiks izmantots kā noklusējuma rēķina konts jaunām elementu prasībām, kas izveidotas projektam. Ja lauku atstājat tukšu, pēc noklusējuma tiks izmantots pirmā projekta līguma finansējuma avota rēķina uzņēmums. Taču lietotāji varēs mainīt uzņēmumu, kad tiks saglabāts ieraksts.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Atlasiet rēķina uzņēmumu, kuru lietot, kad tiek izveidota elementa prasība.

Lai atlasītu rēķina uzņēmumu, ko lietot, kad izveidojat elementa prasību, veiciet tālāk uzskaitītās darbības.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \>**Projekti** \>**Visi projekti** un atlasiet projekta ierakstu.
1. Cilnē **Plāns** atlasiet **Elementa prasības**.
1. Izveidojiet jaunu elementa prasības ierakstu.

    - Ieraksta lauks **Rēķina uzņēmums** pēc noklusējuma ir iestatīts uz projektam iestatīto rēķina uzņēmumu. Varat mainīt lauka **Rēķina uzņēmums** vērtību un pēc tam ierakstu saglabāt. Pēc ieraksta saglabāšanas vairāk nevarēsit jaunināt **Rēķina uzņēmuma** vērtību. Ja elementa prasībai jāatjaunina **Rēķina uzņēmuma** vērtība, dzēsiet esošo elementa prasību un izveidojiet jaunu ar vajadzīgo vērtību.
    - Elementa prasības lauks **Klients** pēc noklusējuma tiek balstīts **Noklusējuma klienta** vērtībā, kas tiek iestatīta lapā **Projekta pārvaldības un uzskaites parametri**.

    Kad tiek saglabāts elementa prasības ieraksts, sistēma to saista ar galvenes ierakstu **Elementa prasības pārdošanas pasūtījums**. Ja nevienai atvērta pārdošanas pasūtījuma galvenei nav atlasīts rēķina uzņēmums, sistēma tādu izveidos un ar to saistīs elementa prasības rindu.

> [!NOTE]
> Par elementa prasībām vienmēr pilnībā tiek izrakstīts rēķins ierakstā iestatītajam rēķina uzņēmumam. Pašlaik sistēma neatbalsta finansējuma sadalījuma kārtulas ar elementa prasībām, un tās nedalīs grāmatojumu, balstoties finansējuma sadalījuma kārtulu iestatījumos.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Elementa prasības izveidošana no elementa prognozes ieraksta

Lai izveidotu elementa prasību no elementa prognozes ieraksta, veiciet tālāk uzskaitītās darbības.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \>**Projekti** \>**Visi projekti** un atlasiet projekta ierakstu.
1. Cilnē **Plāns** atlasiet **Elementa prognozes**.
1. Izveidojiet jaunu elementa prognozes ierakstu.
1. Neobligāti: Cilnes **Projekts** laukā **Finansējuma avots** atlasiet vēlamo rēķina uzņēmumu.
1. Atlasiet **Izveidot elementa prasību** un apstipriniet saņemto ziņojumu.

    > [!NOTE]
    > Sistēma kopē vērtību **Finansējuma avots** no elementa prognozes ieraksta uz jaunizveidoto elementa prasības ierakstu.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Noklusējuma rēķina uzņēmums, kas sistēma automātiski izveido elementa prasību no pirkuma pasūtījuma rindas

Ja opcija **Izveidot elementa prasību** ir iestatīta uz vērtību **Jā** lapā **Projekta pārvaldības un uzskaites parametri**, sistēma automātiski izveido elementa prasību, kad tiek saglabāta jauna projekta pirkuma pasūtījuma rinda. Lauki **Rēķina uzņēmums** un **Elementa prasība** pēc noklusējuma tiek iestatīta uz **Noklusējuma rēķina uzņēmuma** vērtību projekta ierakstā. Pašlaik sistēma neatbalsta rēķina uzņēmuma jaunināšanu vai maiņu šī tipa ierakstiem.
