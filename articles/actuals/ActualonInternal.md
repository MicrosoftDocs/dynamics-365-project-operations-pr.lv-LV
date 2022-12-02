---
title: Datu ietekme uz iekšējo projektu
description: Šajā rakstā ir sniegta informācija par ietekmi uz faktisko datu tabulu dažādos notikumos iekšējam projektam programmā Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921357"
---
# <a name="actuals-impact-for-an-internal-project"></a>Datu ietekme uz iekšējo projektu

_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_

Nākamajā tabulā ir uzskaitīti dažādu transakciju tipu faktiskie dati, kas tiek izveidoti dažādos notikumos iekšēja projekta darbības laikā.

| Pasākums | Faktiskās izmaksas | Piemērs |
|---|---|---|
| Tiek izveidots laiks. | Nav piemērojams | <p>Bobs Kozaks no Fabrikam US organizācijas vienības, kuras izmaksu likme ir 100 ASV dolāri (100 USD) stundā, strādā pie projekta ar nosaukumu "Robotu rokas uzstādīšana korporācijā Adatum". Šis projekts tiek kartēts ar fiksētas cenas norēķinu metodi līguma rindā. Šis ir Boba Kozaka laika ieraksta paraugs:</p><p>Bobs Kozaks — 8 stundas</p> |
| Laiks ir iesniegts. | Nav piemērojams | Tiek izveidota izmaksu žurnāla rinda laika ierakstam. Noklusējuma izmaksu likme tiek ievadīta žurnāla ierakstā. |
| Pirms apstiprināšanas laika ieraksts tiek atsaukts. | Nav piemērojams | |
| Laiks tiek apstiprināts. | Tiek izveidotas faktiskās izmaksas. | <p>Jaunie izveidotie faktiskie dati:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 h, 800 USD</li></ul> |
| Laika apstiprinājums tiek atcelts. | <p>Sākotnējo izmaksu faktisko datu koriģēšanas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidota apgriezta izmaksu faktisko datu vērtība, kura koriģēšanas statuss ir **Nekoriģējams**.</p> | <p>Atjaunināts esošo faktisko datu vienums:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 h, 800 USD, *Koriģēts*</li></ul><p>Jauna faktisko datu vērtība, kas tiek izveidota, lai apgrieztu iepriekšējo finanšu ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, (8 h), (800 USD), *Nekoriģējams*</li></ul> |
| Pēc apstiprināšanas laika ieraksts tiek atsaukts. | <p>Sākotnējo izmaksu faktisko datu koriģēšanas statuss tiek atjaunināts uz **Koriģēts**.</p><p>Tiek izveidota apgriezta izmaksu faktisko datu vērtība, kura koriģēšanas statuss ir **Nekoriģējams**.</p> | <p>Atjaunināts esošo faktisko datu vienums:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, 8 h, 800 USD, *Koriģēts*</li></ul><p>Jauna faktisko datu vērtība, kas tiek izveidota, lai apgrieztu iepriekšējo finanšu ietekmi:</p><ul><li>**Faktiskās izmaksas:** Bobs Kozaks, (8 h), (800 USD), *Nekoriģējams*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
