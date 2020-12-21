---
title: Pabeigšanas izmaksu metodes
description: Šajā tēmā ir sniegta informācija par metodēm, kas tiek izmantotas projekta pabeigšanas izmaksu aprēķināšanai.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531490"
---
# <a name="cost-to-complete-methods"></a>Pabeigšanas izmaksu metodes

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā tēmā ir sniegta informācija par metodēm, kas tiek izmantotas projekta pabeigšanas izmaksu aprēķināšanai. Projekta pabeigšanas izmaksu aprēķināšanai var izmantot vairākas metodes. 

Kad izveidojat projekta aprēķinu, lapas **Izveidot aprēķinu** laukā **Pabeigšanas izmaksu metode** varat atlasīt kādu no tālāk norādītajām pabeigšanas izmaksu metodēm.

| Pabeigšanas izmaksu metode    | Apraksts                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kopējās izmaksas — faktiskās            | Ievadiet izmaksu aprēķinu manuāli laukā **Kopējās izmaksas** vai **Kopējais daudzums**, izmantojot pogu **Izmaksu aprēķins**, kas atrodas **Aprēķinu lapā**. Sistēma no ievadītajām kopsummām atņems faktiskās izmaksas. Kopsumma ir projekta pabeigšanas izmaksas. Šī metode neizmanto izdevumu aprēķinus un resursu piešķīrumus, kas ievadīti programmā Microsoft Dataverse integrētajā risinājumā Project Operations. Kopējās izmaksas vai kopējo daudzumu var pēc nepieciešamības atjaunināt manuāli.  |
| Kopējā prognoze — faktiskā        | Resursu piešķīrumu un izmaksu aprēķini tiek izmantoti, lai noteiktu projekta prognozes kopsummu. Faktiskās izmaksas tiek salīdzinātas ar šo prognozi, lai aprēķinātu pabeigšanas izmaksas.                                                                                                                                                                                                                                                                          |
| Kā iepriekšējs novērtējums         | Šajā gadījumā tiek izmantotas tās pašas aprēķinu metodes, kas tika izmantotas iepriekšējā periodā. Ja iepriekšējam periodam bija nepieciešams prognozes modelis, arī šai metodei ir nepieciešams prognozes modelis.                                                                                                                                                                                                                                                                                                                           |
| Pabeigšanas izmaksu iestatīšana uz nulli | Šo metodi parasti izmanto pirms projekta aprēķina dzēšanas, un tajā tiek salīdzinātas aprēķinu kopsummas ar grāmatotajām faktiskajām darbībām un tiek notīrīta kolonna **Pabeigšanas izmaksas**. Pēc pabeigšanas rezultāts vienmēr ir 100 procentu. Katrai izveidotajai izmaksu rindai tiek notīrīta izvēles rūtiņa **Prognozēšana**, un aprēķina kopsumma tiek kopēta no iepriekšējā izmaksu aprēķina. Faktiskais patēriņš prognožu periodā tiek atskaitīts no projekta pabeigšanas izmaksām.              |
| No izmaksu veidnes           | Šī pabeigšanas izmaksu metode tiek iestatīta izmaksu veidnē, kas ir saistīta ar atlasīto projekta aprēķinu.                                                                                                                                                                                                                                                                                                                                                                          |
