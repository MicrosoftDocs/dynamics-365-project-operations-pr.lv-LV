---
title: Valūtu nesaderības kļūda
description: Šajā rakstā ir sniegta informācija par problēmu novēršanu saistībā ar valūtu nesaderības kļūdu, kas rodas, saglabājot noteiktus ierakstu tipus.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914733"
---
# <a name="currency-mismatch-error"></a>Valūtu nesaderības kļūda 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Saglabājot projektu, līgumu, piedāvājumu vai rezervējamu resursu, var tikt parādīta kļūda **Projekta līgums, kuram pieder uzņēmuma valūta, neatbilst līgumslēdzējas vienības valūtai. Izvēlēties projekta līgumam citu atbildīgā uzņēmuma vai līgumslēdzēja vienību, lai turpinātu**. Tā rodas, jo pastāv valūtu nesaderība starp līgumslēdzējas vienības valūtu ierakstā un atbildīgā uzņēmuma valūtu.


## <a name="resolution"></a>Izšķirtspēja

Lai apietu šo problēmu, veiciet tālāk norādītās darbības.
- Pārbaudiet līgumslēdzējas vienības valūtu šim ierakstam. Valūtu var redzēt, atverot organizācijas vienības ierakstu un pārbaudot vērtību cilnē **Vispārīgi** laukā **Valūta**.
- Pārbaudiet atbildīgā uzņēmuma valūtu. Valūtu var redzēt uzņēmuma ieraksta sadaļā **Saistīts** > **Virsgrāmatas**. Veiciet dubultklikšķi uz virsgrāmatas ieraksta, kas ir saistīts ar uzņēmumu, un pārbaudiet vērtību cilnē **Vispārīgi** laukā **Uzskaites valūta**.

Ja valūta, kas ir iestatīta līgumslēdzējas vienībā, un virsgrāmatas ierakstā nesakrīt, pielāgojiet konfigurāciju vai atlasiet citas vērtības, kad saglabājat ierakstu. Sistēmai nepieciešams, lai šie ieraksti atbilstu pareizām starpuzņēmumu rēķinu izrakstīšanas plūsmām. Papildinformāciju par starpuzņēmumu konfigurācijām skatiet sadaļā [Starpuzņēmumu darbību izveide](../../project-accounting/create-intercompany-transactions.md).

Ja uzņēmuma ierakstam nav piesaistīta virsgrāmatas ieraksta, tas norāda, ka vides iestatīšanas laikā ir iztrūkusi konfigurācija. Konfigurācija ir jākoriģē sistēmas administratoram. Sistēmas administratoram ir jādodas uz **Duālās rakstīšanas konfigurācijām**, jāaptur un jārestartē **Virsgrāmatu duālās rakstīšanas karte** ar šīs kartes sākotnējo sinhronizāciju un tās priekšnosacījumiem. Papildinformāciju skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../../environment/resource-dual-write-maps.md).
