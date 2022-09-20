---
title: Datuma spēkā esošā cena ignorē
description: Šajā rakstā ir paskaidrots, kā iestatīt cenu ignorēšanu konkrētām cenām cenrādī.
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
# <a name="date-effective-price-overrides"></a>Datuma spēkā esošā cena ignorē 

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

*Datuma spēkā stāšanās cenu ignorēšana* nodrošina veidu, kā ignorēt vai mainīt konkrētas cenas cenrādī. Piemēram, jums ir standarta cenrādis, kas ir spēkā no 2022. gada 1. janvāra līdz 2022. gada 31. decembrim. Šajā cenrādī ir cenas daudzām lomām. Cena, kas ir iestatīta **tīkla tehniķa** lomai, ir 100 ASV dolāri (USD) stundā. Kad tīkla tehniķis reģistrē laiku no 2022. gada 1. janvāra līdz 2022. gada 31. decembrim, laika cena tiek noteikta 100 USD. 2022. gada 1. oktobrī jums ir jāpielāgo cena *tikai* tīkla tehniķa **lomai**, sākot no 100 USD stundā līdz 110 USD stundā. Datuma **efektīvās cenas ignorēšanas** līdzeklis ļauj iestatīt šīs izmaiņas kā rindas ignorēšanu konkrētajai lomas cenai. Tāpēc jums nav jākopē viss cenrādis un jāmaina tikai šīs vienas rindas cena.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Datuma spēkā esošā cena ignorē darbaspēka cenu noteikšanu

Datuma efektīvās cenas noteikšanas process projekta darba laika ignorēšanas process sastāv no diviem pamata soļiem.

1. Iespējot **datuma spēkā stāšanās cenu ignorēšanas** līdzekli.
1. Iestatiet datumam spēkā esošas cenas ignorēšanu.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Datuma spēkā stāšanās cenas ignorēšanas līdzekļa iespējošana

> [!NOTE]
> Pēc tam, kad ir iespējots **līdzeklis** Datuma efektīvās cenas ignorēšana, to nevar atspējot.

Lai iespējotu **līdzekli Datuma efektīvās cenas ignorēšana**, veiciet tālāk norādītās darbības.

1. Dodieties uz **Iestatījumu** \> **parametri.**
1. **Atveriet ierakstu Parametri**.
1. Darbību rūts **cilnē Līdzekļu kontrole** atlasiet **Iespējot datuma spēkā stāšanās cenu ignorēšanu**.
1. Apstiprinājuma dialoglodziņā atlasiet **Labi**.
1. Pēc dažiem mirkļiem atsvaidziniet pārlūkprogrammu. Tagad vajadzētu būt pieejamām datumam efektīvām cenas ignorēšanas iespējām. Jūs zināt, ka šīs iespējas ir iespējotas, ja **darbību rūtī vairs netiek rādīts** iespējošanas datuma efektīvās cenas ignorēšana.

### <a name="set-up-a-date-effective-price-override"></a>Datuma spēkā esošas cenas ignorēšanas iestatīšana

Datumu spēkā esošu cenu ignorēšanu var iestatīt **izmaksu**, **pārdošanas** vai **pirkšanas** cenrāžos.

> [!NOTE]
>Datuma spēkā stāšanās cenas ignorēšanas **darbībai** pašlaik ir šādi ierobežojumi:
>
> - Tikai lomu cenas un lomu cenu uzcenojumi atbalsta **datumu spēkā stāšanās cenas ignorēšanas** līdzekli project operations.
> - Kad kopējat cenrādi, izmantojot **darbību Kopēšana** lapā Detalizēta informācija **par** cenrādi, un kad līguma izveides laikā izveidojat projekta cenrādi no standarta vai pielāgota cenrāža, datuma spēkā esošo cenu ignorēšana **netiek** kopēta no avota cenrāža.

Lai iestatītu datumu efektīvas cenas ignorēšanu lomas cenai vai lomas cenas uzcenojumam, veiciet tālāk norādītās darbības.

1. Atveriet tā cenrāža lapu, kuram vēlaties iestatīt datumu spēkā stāšanās dienas cenas ignorēšanu.
1. **Atlasiet cilni Lomu cenas**. Šajā cilnē ir uzskaitīti visi lomas **cenu** ieraksti cenrādī.
1. Atlasiet lomas **cenas** ierakstu, kuram vēlaties iestatīt jaunu datumam efektīvu ignorēšanas cenu, un pēc tam veiciet dubultskārienu (vai dubultklikšķi uz) **Lomas cena**, lai atvērtu **lapu Detalizēta informācija par** lomu cenu.
1. Atlasiet cilni Datums, **kas stājas spēkā, ignorējot** . Šīs cilnes režģī ir uzskaitīti visi atlasītā lomas **cenas** ieraksta datuma efektīvās cenas ignorējumi.
1. Rīkjoslā virs režģa atlasiet **Jauna lomu cenas ignorēšana**. Tiek **atvērts slīdnis Jauna lomas** cenas ignorēšana.
1. Norādiet spēkā stāšanās datumu, vienību un jauno cenu cenas ignorēšanai. Pēc tam atlasiet **Saglabāt** un aizveriet veidlapu.

> [!NOTE]
> - Datuma efektīvo cenu ignorēšana lomas cenai vai lomas cenas uzcenojums ir piemērojams tai pašai cenu dimensiju vērtību kombinācijai, kas pastāv vecākelementa **lomas cenas** vai **lomas cenas uzcenojuma** rindā.
> - Datumam, kas ir atlasīts **laukā Spēkā no**, ir jābūt vecākcenu saraksta spēkā stāšanās datumos. Cenu ignorēšana stāsies spēkā datumā, kas atlasīts **laukā Spēkā no**, un tiks piemērota līdz vecākcenu saraksta beigu datuma beigām. Ja iestatāt citu datumu spēkā esošu cenas ignorēšanu par to pašu lomas cenu, pirmā cenu ignorēšana stāsies spēkā datumā, kas ir atlasīts **laukā Spēkā no**, un tiks lietota līdz otrā ignorēšanas sākumam.

## <a name="examples"></a>Piemēri

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>1. piemērs: Datuma efektivitātes noteikšana lomas cenai, kuras lomas cena ir svarīgāka par

Tālāk sniegtajā piemērā ir parādīts, kā datuma efektivitāte tiek noteikta konkrētai lomas cenai, kurai ir iestatīta lomas cenas ignorēšana.

**Cenrādis A: no 1. janvāra līdz 30. jūnijam**

*Lomas cena*

| Lomas cena | Vienība | Cenrādis | Ietekme uz ienākošo darījumu cenu noteikšanu |
|---|---|---|---|
| Tīkla tehniķis | stunda | 100 | Šī cena tiks izmantota visiem darījumiem, kuros darījuma datums ir no 1. janvāra līdz 14. martam. |

*Lomu cenas ignorēšana*

| Efektīva no | Vienība | Cenrādis | Ietekme uz ienākošo darījumu cenu noteikšanu |
|---|---|---|---|
| 15. gada marts | stunda | 110 | Šī cena tiks izmantota visiem darījumiem, kuros darījuma datums ir no 15. marta līdz 30. martam. |
| 1. gada aprīlis | stunda | 120 | Šī cena tiks izmantota visiem darījumiem, kuros darījuma datums ir no 1. aprīļa līdz 30. jūnijam. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>2. piemērs: Datuma efektivitātes noteikšana lomas cenas uzcenojumam, kurai ir svarīgāka lomas cenu uzcenojums

Tālāk sniegtajā piemērā ir parādīts, kā tiek noteikta datuma efektivitāte konkrētai lomas cenas atzīmei, kurai ir iestatīta lomas cenu uzcenojuma ignorēšana.

**Cenrādis A: no 1. janvāra līdz 30. jūnijam**

*Lomas cena*

| Lomas cena | Darba stundas | Vienība | Cenrādis | Ietekme uz ienākošo darījumu cenu noteikšanu |
|---|---|---|---|---|
| Tīkla tehniķis | Regulāri | stunda | 100 | Šī cena tiks izmantota visiem darījumiem, kuros darījuma datums ir no 1. janvāra līdz 14. martam. |

*Lomu cenu uzcenojums*

| Organizācijas struktūrvienība | Darba stundas | Uzcenojums % |
|---|---|---|
| Contoso ASV | Virsstundas | 10% |

*Lomu cenu uzcenojuma ignorēšana*

| Efektīva no | Cenrādis | Ietekme uz ienākošo darījumu cenu noteikšanu |
|---|---|---|
| 15. gada marts | 20% | Šis uzcenojuma procents tiks izmantots visām transakcijām, kuru transakcijas datums ir no 15. marta līdz 30. martam. |
| 1. gada aprīlis | 25% | Šis uzcenojums tiks izmantots visiem darījumiem, kuros darījuma datums ir no 1. aprīļa līdz 30. jūnijam. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
