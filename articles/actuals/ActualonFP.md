---
title: Datu ietekme uz fiksētu cenu piesaistīšanu
description: Šajā rakstā ir sniegta informācija par ietekmi uz faktisko datu tabulu dažādos notikumos fiksētu cenu piesaistīšanas dzīves cikla laikā risinājumā Microsoft Dynamics 365 Project Operations.
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
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Datu ietekme uz fiksētu cenu piesaistīšanu

_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_

Nākamajā tabulā ir uzskaitīti dažādu transakciju tipu faktiskie dati, kas tiek izveidoti dažādos notikumos fiksētu cenu piesaistīšanas laikā.

| Pasākums | Faktiskās izmaksas | Rēķinā neiekļautā faktiskā pārdošana | Rēķinā iekļauta faktiskā pārdošana | Piemērs |
|---|---|---|---|---|
| Tiek izveidots laiks. | Nav piemērojams | Nav piemērojams | Nav piemērojams | <p>Bobs Kozaks no Fabrikam US organizācijas vienības, kuras izmaksu likme ir 100 ASV dolāri (100 USD) stundā, strādā pie projekta ar nosaukumu "Robotu rokas uzstādīšana korporācijā Adatum". Šis projekts tiek kartēts ar fiksētas cenas norēķinu metodi līguma rindā. Šis ir Boba Kozaka laika ieraksta paraugs:</p><p>Bobs Kozaks — 8 stundas</p> |
| Laiks ir iesniegts. | Nav piemērojams | Nav piemērojams | Nav piemērojams | Tiek izveidota izmaksu žurnāla rinda laika ierakstam. Noklusējuma izmaksu likme tiek ievadīta žurnāla ierakstā. |
| Pirms apstiprināšanas laika ieraksts tiek atsaukts. | Nav piemērojams | Nav piemērojams | Nav piemērojams | |
| Laiks tiek apstiprināts. | Tiek izveidotas faktiskās izmaksas. | Nav piemērojams | Nav piemērojams | <p>Jaunie izveidotie faktiskie dati:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 h, 800 USD</li></ul> |
| Laika apstiprinājums tiek atcelts. | <p>Sākotnējo izmaksu faktisko datu koriģēšanas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidota apgriezta izmaksu faktisko datu vērtība, kura koriģēšanas statuss ir **Nekoriģējams**.</p> | Nav piemērojams | Nav piemērojams | <p>Atjaunināts esošo faktisko datu vienums:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 h, 800 USD, *Koriģēts*</li></ul><p>Jauna faktisko datu vērtība, kas tiek izveidota, lai apgrieztu iepriekšējo finanšu ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, (8 h), (800 USD), *Nekoriģējams*</li></ul> |
| Pēc apstiprināšanas laika ieraksts tiek atsaukts. | <p>Sākotnējo izmaksu faktisko datu koriģēšanas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidota apgriezta izmaksu faktisko datu vērtība, kura koriģēšanas statuss ir **Nekoriģējams**.</p> | Nav piemērojams | Nav piemērojams | <p>Atjaunināts esošo faktisko datu vienums:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 h, 800 USD, *Koriģēts*</li></ul><p>Jauna faktisko datu vērtība, kas tiek izveidota, lai apgrieztu iepriekšējo finanšu ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, (8 h), (800 USD), *Nekoriģējams*</li></ul> |
| Līgums ir apstiprināts. | <p>Iepriekšējo izmaksu faktisko datu koriģēšanas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidoti apgriezti izmaksu faktiskie dati, kuru koriģēšanas statuss ir **Nekoriģējams**.</p><p>Jaunie izmaksu faktiskie dati tiek izveidoti pēc tam, kad tiek atkārtoti izvērtētas līguma kārtulas.</p> | Nav piemērojams | Nav piemērojams | <p>Atjaunināts esošo faktisko datu vienums:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 h, 800 USD, *Koriģēts*</li></ul><p>Jauna faktisko datu vērtība, kas tiek izveidota, lai apgrieztu iepriekšējo finanšu ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, (8 h), (800 USD), *Nekoriģējams*</li></ul><p>Jauna faktisko datu vērtība, kas tiek izveidota, lai atkārtoti noteiktu finanšu ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 h, 800 USD</li></ul> |
| Tiek izveidots rēķins. | Nav piemērojams | Nav piemērojams | Nav piemērojams | |
| Rēķins tiek apstiprināts ar atskaites punktu. | Nav piemērojams | Nav piemērojams | Tiek izveidoti uz atskaites punktu balstīti rēķinā iekļautie pārdošanas faktiskie dati. | <p>Esošs faktisko datu vienums, kas nemainās:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 h, 800 USD</li></ul><p>Jauns faktisko datu vienums, kas izveidots, lai ierakstītu rēķinā iekļautās pārdošanas vērtības:</p><ul><li>**Rēķinā iekļautās pārdošanas faktiskie dati:** atskaites punkts, 5000 USD</li></ul> |
| Rēķins tiek labots, lai izveidotu atskaites punkta kredītu. | Nav piemērojams | Nav piemērojams | Tiek izveidotas apgrieztas rēķinā iekļautas faktiskās pārdošanas. | <p>Esošs faktisko datu vienums, kas nemainās:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 h, 800 USD</li></ul><p>Atjaunināts esošo faktisko datu vienums:</p><ul><li>**Rēķinā iekļautās pārdošanas faktiskie dati:** atskaites punkts, 5000 USD, *Koriģēts*</li></ul><p>Jauns faktisko datu vienums, kas izveidots, lai apgrieztu iepriekšējās rēķinā iekļautās pārdošanas vērtības:</p><ul><li>**Rēķinā iekļautās pārdošanas faktiskie dati:** atskaites punkts, 5000 USD, *Nekoriģējams*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
