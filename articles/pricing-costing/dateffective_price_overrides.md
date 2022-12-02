---
title: Datuma un spēkā esošās cenas pārlabošana
description: Šajā rakstā ir izskaidrots, kā iestatīt cenu pārlabošanu noteiktām cenām cenrādī.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446005"
---
# <a name="date-effective-price-overrides"></a>Datuma un spēkā esošās cenas pārlabošana 

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

*Datuma un spēkā esošās cenas pārlabošana* nodrošina veidu, kā pārlabot vai mainīt konkrētas cenas cenrādī. Piemēram, jums ir standarta cenrādis, kas ir spēkā no 2022. gada 1. janvāra līdz 2022. gada 31. decembrim. Šajā cenrādī ir cenas daudzām lomām. Lomai **Tīkla tehniķis** iestatītā cena ir 100 ASV dolāri (USD) stundā. Kad tīkla tehniķis reģistrē laiku periodā no 2022. gada 1. janvāra līdz 2022. gada 31. decembrim, laikam tiek noteikta cena 100 USD. 2022. gada 1. oktobrī jums ir jākoriģē cena *tikai* lomai **Tīkla tehniķis** no 100 USD stundā uz 110 USD stundā. Izmantojot līdzekli **Datuma un spēkā esošās cenas pārlabošana**, varat iestatīt šīs izmaiņas kā šīs konkrētās lomas cenas rindas pārlabojumu. Tādēļ nav jākopē viss cenrādis un jāmaina tikai šīs vienas rindas cena.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Datuma un spēkā esošās cenas pārlabošana darbaspēka izcenojumam

Datuma un spēkā esošās cenas pārlabošanas iestatīšanas process darbaspēka laikam projektā sastāv no divām darbībām.

1. Iespējojiet līdzekli **Datuma un spēkā esošās cenas pārlabošana**.
1. Iestatiet datuma un spēkā esošās cenas pārlabošanu.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Datuma un spēkā esošās cenas pārlabošanas līdzekļa iespējošana

> [!NOTE]
> Pēc līdzekļa **Datuma un spēkā esošās cenas pārlabošana** iespējošanas to nevar atspējot.

Lai iespējotu līdzekli **Datuma un spēkā esošās cenas pārlabošana**, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Iestatījumi** \> **Parametri**.
1. Atveriet ierakstu **Parametri**.
1. Darbību rūts cilnē **Līdzekļu vadība** atlasiet **Datuma un spēkā esošās cenas pārlabošana**.
1. Apstiprinājuma dialoglodziņā atlasiet **Labi**.
1. Pēc brīža atsvaidziniet pārlūkprogrammu. Datuma un spēkā esošās cenas pārlabošanas iespējām tagad ir jābūt pieejamām. Varēsiet noteikt, ka šīs iespējas ir iespējotas, ja darbību rūtī vairs nav redzama poga **Iespējot datuma un spēkā esošās cenas pārlabošanu**.

### <a name="set-up-a-date-effective-price-override"></a>Datuma un spēkā esošās cenas pārlabošanas iestatīšana

Datuma un spēkā esošās cenas pārlabošanu var iestatīt cenrāžos **Izmaksas**, **Pārdošana** vai **Pirkums**.

> [!NOTE]
>Līdzekļa **Datuma un spēkā esošās cenas pārlabošana** darbībai pašlaik ir tālāk uzskaitītie ierobežojumi.
>
> - Programmā Project Operations līdzekli **Datuma un spēkā esošās cenas pārlabošana** atbalsta tikai lomu cenas un lomu cenu uzcenojumi.
> - Kopējot cenrādi ar darbību **Kopēt** lapā **Cenrāža informācija** un veidojot projekta cenrādi no standarta vai pielāgota cenrāža līguma izveides laikā, datuma un spēkā esošās cenas pārlabojumi **netiek** kopēti no avota cenrāža.

Lai iestatītu datuma un spēkā esošās cenas pārlabošanu lomas cenai vai lomas cenas uzcenojumam, veiciet tālāk norādītās darbības.

1. Atveriet tā cenrāža lapu, kam vēlaties iestatīt datuma un spēkā esošās cenas pārlabošanu.
1. Atlasiet cilni **Lomu cenas**. Šajā cilnē ir uzskaitīti visi cenrādī esošie ieraksti **Lomas cena**.
1. Atlasiet ierakstu **Lomas cena**, kuram vēlaties iestatīt jaunu datuma un spēkā esošās cenas pārlabojumu, un pēc tam veiciet dubultskārienu (dubultklikšķi) uz **Lomas cena**, lai atvērtu lapu **Lomas cenas informācija**.
1. Atlasiet cilni **Spēkā stāšanās datuma pārlabošanas**. Šīs cilnes režģī ir uzskaitīti visi datuma un spēkā esošās cenas pārlabojumi atlasītajam ierakstam **Lomas cena**.
1. Rīkjoslā virs režģa atlasiet **Jaunas lomas cenas pārlabošana**. Tiek atvērts slīdnis **Jaunas lomas cenas pārlabošana**.
1. Norādiet cenas pārlabojuma spēkā stāšanās sākuma datumu, vienību un jauno cenu. Pēc tam atlasiet **Saglabāt** un aizveriet veidlapu.

> [!NOTE]
> - Lomas cenas vai lomas cenas uzcenojuma datuma un spēkā esošas cenas pārlabošana ir lietojama tām pašām izcenojuma dimensijas vērtībām, kas pastāv primārajā rindā **Lomas cena** vai **Lomas cenas uzcenojums**.
> - Datumam, kas atlasīts laukā **Spēkā no**, jāietilpst primārā cenrāža spēkā esamības datumos. Cenas pārlabošana stājas spēkā datumā, kas ir atlasīts laukā **Spēkā no**, un tiks lietota līdz primārā cenrāža beigu datumam. Ja iestatāt citu datuma un spēkā esošās cenas pārlabojumu tai pašai lomas cenai, pirmais cenas pārlabojums stāsies spēkā datumā, kas ir atlasīts laukā **Spēkā no** un tiks lietos līdz otrā pārlabojuma sākumam.

## <a name="examples"></a>Piemēri

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>1. piemērs. Spēkā stāšanās datuma noteikšana lomas cenai, kam ir lomas cenas pārlabojumi

Tālāk sniegtajā piemērā ir parādīts, kā tiek noteikts spēkā stāšanās datums noteiktai lomas cenai, kurai ir iestatīti lomas cenas pārlabojumi.

**Cenrādis A: no 1. janvāra līdz 30. jūnijam**

*Lomas cena*

| Lomas cena | Vienība | Cenrādis | Ietekme uz ienākošo transakciju izcenojumu |
|---|---|---|---|
| Tīkla tehniķis | stunda | 100 | Šī cena tiks lietota jebkurā transakcijā, kur transakcijas datums ir no 1. janvāra līdz 14. martam. |

*Lomas cenas pārlabošana*

| Spēkā no | Vienība | Cenrādis | Ietekme uz ienākošo transakciju izcenojumu |
|---|---|---|---|
| 15. gada marts | stunda | 110 | Šī cena tiks lietota jebkurā transakcijā, kur transakcijas datums ir no 15. marta līdz 30. martam. |
| 1. gada aprīlis | stunda | 120 | Šī cena tiks lietota jebkurā transakcijā, kur transakcijas datums ir no 1. aprīļa līdz 30. jūnijam. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>2. piemērs. Spēkā stāšanās datuma noteikšana lomas cenas uzcenojumam, kam ir lomas cenas uzcenojuma pārlabojumi

Tālāk sniegtajā piemērā ir parādīts, kā tiek noteikts spēkā esamības datums noteiktam lomas cenas uzcenojumam, kam ir iestatīti lomas cenas uzcenojuma pārlabojumi.

**Cenrādis A: no 1. janvāra līdz 30. jūnijam**

*Lomas cena*

| Lomas cena | Darba stundas | Vienība | Cenrādis | Ietekme uz ienākošo transakciju izcenojumu |
|---|---|---|---|---|
| Tīkla tehniķis | Parasti | stunda | 100 | Šī cena tiks lietota jebkurā transakcijā, kur transakcijas datums ir no 1. janvāra līdz 14. martam. |

*Lomas cenas uzcenojums*

| Organizācijas vienība | Darba stundas | Uzcenojuma % |
|---|---|---|
| Contoso ASV | Virsstundas | 10% |

*Lomas cenas uzcenojuma pārlabojums*

| Spēkā no | Cenrādis | Ietekme uz ienākošo transakciju izcenojumu |
|---|---|---|
| 15. gada marts | 20% | Šie uzcenojuma procenti tiks lietoti jebkurā transakcijā, kur transakcijas datums ir no 15. marta līdz 30. martam. |
| 1. gada aprīlis | 25% | Šis uzcenojums tiks lietots jebkurā transakcijā, kur transakcijas datums ir no 1. aprīļa līdz 30. jūnijam. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
