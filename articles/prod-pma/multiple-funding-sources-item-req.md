---
title: Elementu prasības projekta līgumiem ar vairākiem avotiem+
description: Šajā rakstā ir sniegta informācija par to, kā konfigurēt un izmantot krājumu prasības, izmantojot vairākus finansējuma avotus.
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

Dažām līgumiskām vienošanām par projektu nodevumiem var būt nepieciešami vairāki finansējuma avoti. Šajā rakstā ir paskaidrots, kā atlasīt un konfigurēt vēlamos finansējuma avotus, ja projektam vai projekta līgumam ir nepieciešami vairāki avoti.

## <a name="terminology"></a>Terminoloģija

- **Finansējuma avots** — uzņēmums, kas finansē projekta līgumdarbu. Šī entītija var būt iekšēja organizācija vai ārējs rēķina konts (debitors vai dotācija).
- **Projekta klients** — entītija, kurai projekta darbs tiek piegādāts.
- **Rēķina konts** — ārējā entītija, kas maksā par projekta darbu.

## <a name="example"></a>Piemērs

Contoso ir ieguvusi aprīkojuma atjaunošanas līgumu ar diviem saviem klientiem: Adatum US un Adatum Corporate. Līgums ietver aparatūras un uzstādīšanas pakalpojumus, kas tiks piegādāti Adatum US (projekta klientam). Aparatūru finansēs Adatum Corporate (rēķina konts 1), un uzstādīšanas darbus finansēs Adatum US (rēķina konts 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Rēķina konta noklusējuma kārtulu iestatīšana krājumu prasībām

### <a name="prerequisites"></a>Priekšnoteikumi

- Microsoft Dynamics 365 Finance **versija 10.0.27 vai jaunāka** ir nepieciešama, lai izmantotu krājumu prasības, kurām ir vairāki rēķinu konti.
- Sistēmas administratoram ir jāiespējo līdzekļa **Atļaut krājumus ar vairākiem finansējuma avotiem project operations krājuma/ražošanas scenārijiem** līdzekļa līdzekļa Līdzekļa pārvaldība līdzekļa Atļaut krājumus ar vairākiem finansējuma avotiem darbvietā **Līdzekļu pārvaldība**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Rēķina konta saistību neizpildes kārtulu iestatīšana

Lai iestatītu rēķina konta noklusējuma kārtulas, veiciet tālāk norādītās darbības.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Projekta pārvaldības un grāmatvedības parametri**.
1. Cilnes Vispārīgi sadaļā Pārdošanas pasūtījumi un krājumu prasības **iestatiet opciju** Atļaut projektiem ar vairākiem finansējuma avotiem **vērtību** Jā **.** **·**
1. **Laukā Noklusējuma debitors** norādiet, no kurienes pēc noklusējuma nāk projekta piegādes debitors, kuram nepieciešams krājums:

    - **No finansējuma avota** — noklusējuma projekta piegādes klients nāk no finansējuma avota. Ja projekta līgumā ir iesaistīti vairāki finansējuma avoti, tiks izmantots pirmais finansējuma avots sarakstā.
    - **No projekta** — noklusējuma projekta piegādes klients nāk no klienta, kas ir atlasīts **laukā Projekta ieraksta konts**.

1. Neobligāti: noklusējuma rēķina konta iestatīšana vai mainīšana projekta ierakstos:

    1. Dodieties uz **Projektu vadība un grāmatvedība** \> **Projekti** \> **Visi projekti** un atveriet detalizētu informāciju par projekta ierakstu.
    2. Cilnē **Vispārīgi** iestatiet vai atjauniniet **lauku Noklusējuma rēķina konts**. Norādītais konts tiks izmantots kā noklusējuma rēķina konts jaunām krājumu prasībām, kas izveidotas projektam. Ja atstāsit lauku tukšu, pēc noklusējuma tiks izmantots pirmā projekta līguma finansējuma avota rēķina konts. Tomēr lietotāji varēs mainīt kontu, saglabājot ierakstu.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Atlasiet rēķina kontu, ko izmantot, veidojot krājumu prasību

Lai atlasītu rēķina kontu, ko izmantot, veidojot krājumu vajadzības, veiciet tālāk norādītās darbības.

1. Dodieties uz **Projektu vadība un grāmatvedība** \> **Projekti** \> **Visi projekti** un atlasiet projekta ierakstu.
1. Cilnē **Plāns** atlasiet **Vienumu prasības**.
1. Izveidojiet jaunu vienuma prasību ierakstu.

    - Pēc noklusējuma ieraksta lauks **Rēķina konts** tiek iestatīts uz rēķina kontu, kas ir iestatīts projektam. Varat mainīt rēķina konta **lauka vērtību** un pēc tam saglabāt ierakstu. Kad ieraksts ir saglabāts, jūs vairs nevarat atjaunināt **rēķina konta** vērtību. Ja krājuma **prasībai ir jāatjaunina rēķina konta** vērtība, izdzēsiet esošo krājumu prasību un pēc tam izveidojiet jaunu, kam ir vēlamā vērtība.
    - Pēc noklusējuma krājuma prasību lauks **Klients** tiek iestatīts, pamatojoties uz **noklusējuma klienta** vērtību, kas ir iestatīta **lapā Projektu vadības un uzskaites parametri**.

    Kad krājuma prasību ieraksts ir saglabāts, sistēma to saista ar **krājumu prasību pārdošanas pasūtījuma** galvenes ierakstu. Ja atlasītajam rēķina kontam nav atvērta pārdošanas pasūtījuma galvenes, sistēma to izveidos un saistīs ar to krājumu prasību rindu.

> [!NOTE]
> Krājumu prasības vienmēr tiek pilnībā iekļautas rēķinā rēķinā rēķinā norādītajā rēķina kontā, kas ir iestatīts ierakstā. Sistēma pašlaik neatbalsta finansējuma piešķiršanas noteikumus, kuriem ir posteņu prasības, un tā nesadalīs norīkošanu, pamatojoties uz finansējuma piešķiršanas noteikumu noteikšanu.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Vienuma prasības izveide no krājumu prognozes ieraksta

Lai izveidotu vienuma prasību no vienuma prognozes ieraksta, veiciet tālāk norādītās darbības.

1. Dodieties uz **Projektu vadība un grāmatvedība** \> **Projekti** \> **Visi projekti** un atlasiet projekta ierakstu.
1. **Cilnē Plāns** atlasiet **Vienumu prognozes**.
1. Izveidojiet jaunu vienumu prognozes ierakstu.
1. Neobligāti: **cilnes** Projekts **laukā Finansējuma avots** atlasiet vajadzīgo rēķina kontu.
1. Atlasiet **Izveidot vienuma nepieciešamību** un apstipriniet saņemto ziņojumu.

    > [!NOTE]
    > Sistēma kopē **finansējuma avota** vērtību no krājuma prognozes ieraksta uz jaunizveidoto krājumu prasību ierakstu.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Noklusējuma rēķina konts, kad sistēma automātiski izveido krājumu prasību no pirkšanas pasūtījuma rindas

**Ja opcijai Izveidot krājumu nepieciešamību** lapā Projektu vadības un uzskaites parametri **ir iestatīta vērtība** Jā **·**, sistēma automātiski izveido krājumu nepieciešamību, kad tiek saglabāta jauna projekta pirkšanas pasūtījuma rinda. Pēc noklusējuma laukiem **Rēķina konts** un **Krājuma prasība** ir iestatīta **lauka Noklusējuma rēķina vērtība** projekta ierakstā. Sistēma pašlaik neatbalsta šāda veida ierakstu rēķina konta atjaunināšanu vai maiņu.
