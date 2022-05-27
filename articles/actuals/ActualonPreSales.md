---
title: Faktiskā ietekme iesaistīšanās pirmspārdošanas posmā
description: Šajā tēmā ir sniegta informācija par ietekmi uz tabulu Faktiski dažādos pasākumos, kamēr engagment atrodas Microsoft pirmspārdošanas posmā Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577245"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Faktiskā ietekme iesaistīšanās pirmspārdošanas posmā

_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_

Šajā tabulā ir uzskaitīti dažādu darbību tipu fakti, kas izveidoti dažādos pasākumos projekta iesaistes pirmspārdošanas posmā.

| Pasākums | Faktiskās izmaksas | Piemērs |
|---|---|---|
| Laiks ir izveidots. | Nav piemērojams | <p>Bobs Kozaks no Fabrikam ASV organizatoriskās vienības, kuras izmaksu likme ir 100 ASV dolāri (100 ASV dolāri) stundā, strādā pie projekta ar nosaukumu "Roku uzstādīšana Adatumā". Šis projekts ir kartēts uz fiksētas cenas norēķinu metodi līguma rindā. Šeit ir parauga laika ieraksts no Bob Kozak:</p><p>Bobs Kozaks - 8 stundas</p> |
| Laiks ir iesniegts. | Nav piemērojams | Laika ierakstam tiek izveidota izmaksu žurnāla rinda. Noklusētā izmaksu likme tiek ievadīta žurnāla ierakstā. |
| Laika ieraksts tiek atsaukts, pirms tas tiek apstiprināts. | Nav piemērojams | |
| Laiks ir apstiprināts. | Tiek izveidots faktiskais izmaksu aprēķins. | <p>Izveidots jauns faktiskais:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 stundas, USD 800</li></ul> |
| Laika apstiprināšana ir atcelta. | <p>Sākotnējās faktiskās izmaksu korekcijas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidota anulēšanas izmaksu faktiskā vērtība, kuras korekcijas statuss **ir Neattaisnojams**.</p> | <p>Esošais faktiskais, kas tiek atjaunināts:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 h, USD 800, *Pielāgots*</li></ul><p>Jauns faktiskais, kas izveidots, lai mainītu iepriekšējo finansiālo ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, (8 h), (USD 800), *Neattaisnojams*</li></ul> |
| Laika ieraksts tiek atsaukts pēc tā apstiprināšanas. | <p>Sākotnējās faktiskās izmaksu korekcijas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidota anulēšanas izmaksu faktiskā vērtība, kuras korekcijas statuss **ir Neattaisnojams**.</p> | <p>Esošais faktiskais, kas tiek atjaunināts:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 h, USD 800, *Pielāgots*</li></ul><p>Jauns faktiskais, kas izveidots, lai mainītu iepriekšējo finansiālo ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, (8 h), (USD 800), *Neattaisnojams*</li></ul> |
| Piedāvājums tiek uzvarēts, un tiek izveidots līgums. | <p>Veco izmaksu faktisko korekcijas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidotas anulēšanas izmaksu faktiskās vērtības, kuru korekcijas statuss **ir Neattaisnojams**.</p><p>Jauni izmaksu fakti tiek izveidoti pēc līguma noteikumu pārvērtēšanas.</p> | <p>Esošais faktiskais, kas tiek atjaunināts:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 h, USD 800, *Pielāgots*</li></ul><p>Jauns faktiskais, kas izveidots, lai mainītu iepriekšējo finansiālo ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, (8 h), (USD 800), *Neattaisnojams*</li></ul><p>Jauni faktiskie dati, kas tiek izveidoti pārvērtētajai finansiālajai ietekmei, kad piedāvājums tiek laimēts un līgums tiek izveidots:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 stundas, USD 800</li><li>**Nemainīga pārdošana faktiskā:** Bob Kozack, 8 stundas, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
