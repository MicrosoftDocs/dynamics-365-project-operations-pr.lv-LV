---
title: Pabeigšanas izmaksu metodes
description: Šajā rakstā ir sniegta informācija par metodēm, kas tiek izmantotas projekta pabeigšanas izmaksu aprēķināšanai.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920299"
---
# <a name="cost-to-complete-methods"></a>Pabeigšanas izmaksu metodes

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā rakstā ir sniegta informācija par metodēm, kas tiek izmantotas projekta pabeigšanas izmaksu aprēķināšanai. Projekta pabeigšanas izmaksu aprēķināšanai var izmantot vairākas metodes. 

Kad izveidojat projekta aprēķinu, lapas **Izveidot aprēķinu** laukā **Pabeigšanas izmaksu metode** varat atlasīt kādu no tālāk norādītajām pabeigšanas izmaksu metodēm.

| Pabeigšanas izmaksu metode    | Apraksts                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kopējās izmaksas — faktiskās            | Ievadiet izmaksu aprēķinu manuāli laukā **Kopējās izmaksas** vai **Kopējais daudzums**, izmantojot pogu **Izmaksu aprēķins**, kas atrodas **Aprēķinu lapā**. Sistēma no ievadītajām kopsummām atņems faktiskās izmaksas. Kopsumma ir projekta pabeigšanas izmaksas. Šī metode neizmanto izdevumu aprēķinus un resursu piešķīrumus, kas ievadīti programmā Microsoft Dataverse integrētajā risinājumā Project Operations. Kopējās izmaksas vai kopējo daudzumu var pēc nepieciešamības atjaunināt manuāli.  |
| Kopējā prognoze — faktiskā        | Resursu piešķīrumu un izmaksu aprēķini tiek izmantoti, lai noteiktu projekta prognozes kopsummu. Faktiskās izmaksas tiek salīdzinātas ar šo prognozi, lai aprēķinātu pabeigšanas izmaksas.                                                                                                                                                                                                                                                                          |
| Kā iepriekšējs novērtējums         | Šajā gadījumā tiek izmantotas tās pašas aprēķinu metodes, kas tika izmantotas iepriekšējā periodā. Ja iepriekšējam periodam bija nepieciešams prognozes modelis, arī šai metodei ir nepieciešams prognozes modelis.                                                                                                                                                                                                                                                                                                                           |
| Pabeigšanas izmaksu iestatīšana uz nulli | Šo metodi parasti izmanto pirms projekta aprēķina dzēšanas, un tajā tiek salīdzinātas aprēķinu kopsummas ar grāmatotajām faktiskajām darbībām un tiek notīrīta kolonna **Pabeigšanas izmaksas**. Pēc pabeigšanas rezultāts vienmēr ir 100 procentu. Katrai izveidotajai izmaksu rindai tiek notīrīta izvēles rūtiņa **Prognozēšana**, un aprēķina kopsumma tiek kopēta no iepriekšējā izmaksu aprēķina. Faktiskais patēriņš prognožu periodā tiek atskaitīts no projekta pabeigšanas izmaksām.              |
| No izmaksu veidnes           | Šī pabeigšanas izmaksu metode tiek iestatīta izmaksu veidnē, kas ir saistīta ar atlasīto projekta aprēķinu.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]