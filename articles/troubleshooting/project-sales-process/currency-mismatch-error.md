---
title: Valūtu nesakritības kļūda
description: Šajā tēmā ir sniegta problēmu novēršanas informācija par valūtu nesakritības kļūdu, kas rodas, saglabājot noteiktus ierakstu tipus.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903718"
---
# <a name="currency-mismatch-error"></a>Valūtu nesakritības kļūda 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Saglabājot projektu, līgumu, piedāvājumu vai rezervējamo resursu, var tikt parādīts kļūdas ziņojums, **kas pieder uzņēmuma valūtai, kas neatbilst līgumslēdzējas vienības valūtai. Lai turpinātu, izvēlieties citu uzņēmumu vai līguma slēdzēju**. Tas ir tāpēc, ka pastāv valūtas neatbilstība starp ieraksta līgumslēdzējas vienības valūtu un uzņēmuma valūtu.


## <a name="resolution"></a>Izšķirtspēja

Lai novērstu šo problēmu, rīkojieties šādi:
- Pārbaudiet šī ieraksta līgumslēdzējas vienības valūtu. Valūtu var apskatīt, atverot organizācijas vienības ierakstu un pārbaudot vērtību **laukā** Valūta cilnē **Vispārīgi**.
- Pārbaudiet uzņēmuma, kam pieder, valūtu. Valūtu var apskatīt, uzņēmuma ierakstā atverot **Saistītās** > **virsgrāmatas**. Veiciet dubultklikšķi uz virsgrāmatas ieraksta, kas ir saistīts ar uzņēmumu, un pārbaudiet vērtību **laukā** Uzskaites valūta cilnē **Vispārīgi**.

Ja saraušanā iestatītā valūta un Virsgrāmatas ieraksts nesakrīt, saglabājiet ierakstu, pielāgojiet konfigurāciju vai atlasiet citas vērtības. Sistēma pieprasa, lai šie ieraksti atbilstu, lai nodrošinātu pareizas starpuzņēmumu rēķinu plūsmas. Plašāku informāciju par starpuzņēmumu konfigurācijām skatiet [Create intercompany transactions](../../project-accounting/create-intercompany-transactions.md).

Ja uzņēmuma ierakstam nav saistīta Virsgrāmatas ieraksta, tas norāda, ka, iestatot vidi, trūkst konfigurācijas. Konfigurācija ir jālabo sistēmas administratoram. Sistēmas administratoram ir jādodas uz **divu rakstīšanas konfigurācijām** un jāaptur un jārestartē **Ledgers duālās rakstīšanas karte** ar šīs kartes sākotnējo sinhronizāciju, un tā ir priekšnosacījumi. Papildinformāciju skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../../environment/resource-dual-write-maps.md).
