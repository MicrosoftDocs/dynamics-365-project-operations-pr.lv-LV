---
title: Elementu prasības projekta līgumiem ar vairākiem avotiem+
description: Šajā rakstā ir sniegta informācija par to, kā konfigurēt un izmantot krājumu vajadzības ar vairākiem finansējuma avotiem.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a54ca1ec5e78d9d0af7b67914f6a63154c7347d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931201"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Elementu prasības projekta līgumiem ar vairākiem avotiem+

_**Attiecas uz:** Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem_

Dažiem līgumiskiem nolīgumiem par projektu rezultātiem var būt vajadzīgi vairāki finansējuma avoti. Šajā rakstā paskaidrots, kā atlasīt un konfigurēt vēlamos finansējuma avotus, ja projektam vai projekta līgumam ir nepieciešami vairāki avoti.

## <a name="terminology"></a>Terminoloģija

- **Finansējuma avots** — entītija, kas finansē projekta līgumdarbus. Šī entītija var būt iekšēja organizācija vai ārējā rēķina konts (debitors vai grants).
- **Projekta debitors** — entītija, kurai tiek piegādāts projekta darbs.
- **Rēķina konts** — ārējā entītija, kas maksā par projekta darbu.

## <a name="example"></a>Piemērs

Contoso ir ieguvis aprīkojuma atjaunošanas līgumu ar diviem saviem klientiem: Adatum US un Adatum Corporate. Līgums ietver aparatūras un instalēšanas pakalpojumus, kas tiks piegādāti Adatum US (projekta klientam). Aparatūru finansēs Adatum Corporate (rēķina konts 1), un uzstādīšanas darbus finansēs Adatum US (rēķina konts 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Iestatīt rēķina konta noklusējuma noteikumus krājumu vajadzībām

### <a name="prerequisites"></a>Priekšnoteikumi

- Microsoft Dynamics 365 Finanšu un operāciju **versija 10.0.27 vai jaunāka** versija ir nepieciešama, lai izmantotu krājumu vajadzības, kurām ir vairāki rēķinu konti.
- Sistēmas administratoram līdzekļu pārvaldības darbvietā **ir jāiespējo** prasības Atļaut vienumu ar vairākiem finansējuma avotiem projektu operāciju uzkrātajiem/uz ražošanu balstītajiem scenārijiem **.**

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Iestatīt rēķina konta noklusējuma kārtulas

Lai iestatītu rēķina konta noklusējuma noteikumus, rīkojieties šādi.

1. Dodieties uz **Projekta pārvaldība un uzskaite** \> **Iestatīšana** \> **Projekta pārvaldības un grāmatvedības parametri**.
1. Cilnes Vispārīgi sadaļā Pārdošanas pasūtījumi un Preces vajadzības **iestatiet opciju** Atļaut projektiem ar vairākiem finansējuma avotiem **uz** Jā **.** **·**
1. Laukā **Noklusētais klients** norādiet, no kurienes pēc noklusējuma nāk projekta piegādes klients krājuma pieprasījumā:

    - **No finansējuma avota** — noklusējuma projekta piegādes klients nāk no finansējuma avota. Ja ar projekta līgumu ir saistīti vairāki finansējuma avoti, tiks izmantots pirmais finansējuma avots sarakstā.
    - **No projekta** — noklusējuma projekta piegādes klients nāk no debitora, kas atlasīts **laukā Projekta ieraksta konts**.

1. Neobligāti: iestatiet vai mainiet noklusējuma rēķina kontu projekta ierakstos:

    1. Dodieties uz **Projektu vadība un grāmatvedība** \> **Projekti** \> **Visi projekti** un atveriet detalizētu informāciju par projekta ierakstu.
    2. Cilnē **Vispārīgi** iestatiet vai atjauniniet **lauku Noklusējuma rēķina konts**. Norādītais konts tiks izmantots kā noklusējuma rēķina konts jaunām krājuma vajadzībām, kas izveidotas projektam. Atstājot lauku tukšu, pēc noklusējuma tiks izmantots pirmā projekta līguma finansējuma avota rēķina konts. Tomēr lietotāji varēs mainīt kontu, saglabājot ierakstu.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Atlasiet rēķina kontu, kas jāizmanto, veidojot krājuma vajadzību

Lai atlasītu rēķina kontu, ko izmantot, veidojot krājuma vajadzību, rīkojieties šādi.

1. Dodieties uz **Projektu vadība un grāmatvedība** \> **Projekti** \> **Visi projekti** un atlasiet projekta ierakstu.
1. Cilnē **Plāns** atlasiet **Preces vajadzības**.
1. Izveidojiet jaunu krājuma vajadzības ierakstu.

    - Pēc noklusējuma **ieraksta lauks Rēķina konts** ir iestatīts uz rēķina kontu, kas iestatīts projektam. Varat mainīt lauka Rēķina konts **vērtību** un pēc tam saglabāt ierakstu. Pēc ieraksta saglabāšanas vairs nevar atjaunināt **rēķina konta** vērtību. Ja preces vajadzībai ir jāatjaunina **rēķina konta** vērtība, dzēsiet esošo krājuma vajadzību un pēc tam izveidojiet jaunu, kam ir vēlamā vērtība.
    - Pēc noklusējuma preces vajadzības lauks Klients tiek iestatīts, **pamatojoties uz** noklusējuma klienta **vērtību, kas iestatīta** lapā Projekta vadības un uzskaites parametri **.**

    Kad krājuma vajadzības ieraksts ir saglabāts, sistēma to saista **ar krājuma vajadzības pārdošanas pasūtījuma** virsraksta ierakstu. Ja nevienam atvērtam pārdošanas pasūtījuma virsrakstam nav atlasītā rēķina konta, sistēma to izveido un saista ar to krājumu vajadzības rindu.

> [!NOTE]
> Krājumu vajadzības vienmēr tiek pilnībā iekļautas rēķinā ar ierakstā iestatīto rēķina kontu. Sistēma pašlaik neatbalsta finansējuma piešķiršanas kārtulas, kurām ir krājumu vajadzības, un tā nesadalīs grāmatošanu, pamatojoties uz finansējuma piešķiršanas kārtulu iestatījumiem.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Izveidot krājuma vajadzību no krājumu budžeta ieraksta

Lai izveidotu krājuma vajadzību no krājumu budžeta ieraksta, rīkojieties šādi.

1. Dodieties uz **Projektu vadība un grāmatvedība** \> **Projekti** \> **Visi projekti** un atlasiet projekta ierakstu.
1. Cilnē **Plāns** atlasiet **Krājumu prognozes**.
1. Izveidojiet jaunu krājumu budžeta ierakstu.
1. Neobligāti: cilnes **Projekts** **laukā Finansējuma avots** atlasiet vēlamo rēķina kontu.
1. Atlasiet **Izveidot krājuma vajadzību** un apstipriniet saņemto ziņojumu.

    > [!NOTE]
    > Sistēma kopē **finansējuma avota** vērtību no krājuma budžeta ieraksta uz jaunizveidoto krājuma vajadzības ierakstu.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Noklusējuma rēķina konts, kad sistēma automātiski izveido krājumu vajadzības no pirkšanas pasūtījuma rindas

**Ja lapā Projekta vadības un uzskaites parametri** opcija Izveidot krājumu vajadzības **ir iestatīta uz** **Jā**, sistēma automātiski izveido krājuma vajadzību, saglabājot jauna projekta pirkšanas pasūtījuma rindu. Pēc noklusējuma **lauki Rēķina konts** un **Preces vajadzība** tiek iestatīti uz projekta ieraksta lauka Noklusējuma rēķina konts **vērtību**. Sistēma pašlaik neatbalsta šī tipa ierakstu rēķina konta atjaunināšanu vai maiņu.
