---
title: Faktiskā ietekme fiksētas cenas piesaistīšanā
description: Šajā rakstā sniegta informācija par ietekmi uz tabulu Faktiski dažādos Microsoft fiksētas cenas piesaistes dzīves cikla laikā dažādos notikumos Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918137"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Faktiskā ietekme fiksētas cenas piesaistīšanā

_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_

Šajā tabulā ir uzskaitīti dažādu darbību tipu faktiskie dati, kas tiek izveidoti dažādos pasākumos fiksētas cenas piesaistīšanā.

| Pasākums | Faktiskās izmaksas | Rēķinā neiekļautā faktiskā pārdošana | Faktiskā rēķinā iekļautā pārdošana | Piemērs |
|---|---|---|---|---|
| Laiks ir izveidots. | Nav piemērojams | Nav piemērojams | Nav piemērojams | <p>Bobs Kozaks no Fabrikam ASV organizatoriskās vienības, kuras izmaksu likme ir 100 ASV dolāri (100 ASV dolāri) stundā, strādā pie projekta ar nosaukumu "Roku uzstādīšana Adatumā". Šis projekts ir kartēts uz fiksētas cenas norēķinu metodi līguma rindā. Šeit ir parauga laika ieraksts no Bob Kozak:</p><p>Bobs Kozaks - 8 stundas</p> |
| Laiks ir iesniegts. | Nav piemērojams | Nav piemērojams | Nav piemērojams | Laika ierakstam tiek izveidota izmaksu žurnāla rinda. Noklusētā izmaksu likme tiek ievadīta žurnāla ierakstā. |
| Laika ieraksts tiek atsaukts, pirms tas tiek apstiprināts. | Nav piemērojams | Nav piemērojams | Nav piemērojams | |
| Laiks ir apstiprināts. | Tiek izveidots faktiskais izmaksu aprēķins. | Nav piemērojams | Nav piemērojams | <p>Izveidots jauns faktiskais:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 stundas, USD 800</li></ul> |
| Laika apstiprināšana ir atcelta. | <p>Sākotnējās faktiskās izmaksu korekcijas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidota anulēšanas izmaksu faktiskā vērtība, kuras korekcijas statuss **ir Neattaisnojams**.</p> | Nav piemērojams | Nav piemērojams | <p>Esošais faktiskais, kas tiek atjaunināts:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 h, USD 800, *Pielāgots*</li></ul><p>Jauns faktiskais, kas izveidots, lai mainītu iepriekšējo finansiālo ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, (8 h), (USD 800), *Neattaisnojams*</li></ul> |
| Laika ieraksts tiek atsaukts pēc tā apstiprināšanas. | <p>Sākotnējās faktiskās izmaksu korekcijas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidota anulēšanas izmaksu faktiskā vērtība, kuras korekcijas statuss **ir Neattaisnojams**.</p> | Nav piemērojams | Nav piemērojams | <p>Esošais faktiskais, kas tiek atjaunināts:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 h, USD 800, *Pielāgots*</li></ul><p>Jauns faktiskais, kas izveidots, lai mainītu iepriekšējo finansiālo ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, (8 h), (USD 800), *Neattaisnojams*</li></ul> |
| Līgums ir apstiprināts. | <p>Veco izmaksu faktisko korekcijas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidotas anulēšanas izmaksu faktiskās vērtības, kuru korekcijas statuss **ir Neattaisnojams**.</p><p>Jauni izmaksu fakti tiek izveidoti pēc līguma noteikumu pārvērtēšanas.</p> | Nav piemērojams | Nav piemērojams | <p>Esošais faktiskais, kas tiek atjaunināts:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 h, USD 800, *Pielāgots*</li></ul><p>Jauns faktiskais, kas izveidots, lai mainītu iepriekšējo finansiālo ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, (8 h), (USD 800), *Neattaisnojams*</li></ul><p>Jauns faktiskais, kas izveidots pārvērtētajai finansiālajai ietekmei:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 stundas, USD 800</li></ul> |
| Tiek izveidots rēķins. | Nav piemērojams | Nav piemērojams | Nav piemērojams | |
| Rēķins tiek apstiprināts ar atskaites punktu. | Nav piemērojams | Nav piemērojams | Tiek izveidotas jaunas uz atskaites punktu balstītas rēķinā iekļautās pārdošanas faktiskās versijas. | <p>Esošais faktiskais, kas paliek nemainīgs:</p><ul><li>**Faktiskās izmaksas:** Bob Kozack, 8 stundas, USD 800</li></ul><p>Jauns faktiskais, kas izveidots, lai ierakstītu rēķinā iekļautās pārdošanas vērtības:</p><ul><li>**Faktiskā rēķinā norādītā pārdošana:** atskaites punkts, USD 5,000</li></ul> |
| Rēķins tiek labots, lai kreditētu atskaites punktu. | Nav piemērojams | Nav piemērojams | Tiek izveidoti anulētie rēķinos iekļautie pārdošanas fakti. | <p>Esošais faktiskais, kas paliek nemainīgs:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 stundas, 800 USD</li></ul><p>Esošais faktiskais, kas tiek atjaunināts:</p><ul><li>**Faktiski aprēķinātie pārdošanas apjomi:** atskaites punkts, USD 5,000, *koriģēts*</li></ul><p>Jauns faktiskais, kas izveidots, lai atsauktu iepriekšējās rēķinā iekļautās pārdošanas vērtības:</p><ul><li>**Faktiskā rēķinā norādītā pārdošana:** Atskaites punkts, (5000 USD), *neattaisnojams*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
