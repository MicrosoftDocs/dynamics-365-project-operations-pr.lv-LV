---
title: Valūtu nesakritības kļūda
description: Šajā tēmā ir sniegta informācija par problēmu novēršanu saistībā ar valūtu nesakritības kļūdu, kas rodas, saglabājot noteiktus ierakstu tipus.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589757"
---
# <a name="currency-mismatch-error"></a>Valūtu nesakritības kļūda 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Saglabājot projektu, līgumu, piedāvājumu vai rezervējamo resursu, iespējams, tiks parādīta kļūda, **uzņēmuma valūtas piederība neatbilst līguma vienības valūtai. Lai turpinātu, izvēlieties citu īpašumā esošu uzņēmumu vai līgumslēdzēju vienību**. Tas ir tāpēc, ka pastāv valūtas nesakritība starp ieraksta līguma vienības valūtu un uzņēmuma valūtu, kurai pieder uzņēmums.


## <a name="resolution"></a>Izšķirtspēja

Lai novērstu šo problēmu, rīkojieties šādi:
- Pārbaudiet šī ieraksta līgumslēdzējas vienības valūtu. Valūtu var apskatīt, atverot organizācijas vienības ierakstu un pārbaudot vērtību **lauka Valūta** cilnē **Vispārīgi**.
- Pārbaudiet paša uzņēmuma valūtu. Valūtu var redzēt, uzņēmuma ierakstā dodoties uz **Saistītajām** > **virsgrāmatām**. Veiciet dubultklikšķi uz Virsgrāmatas ieraksta, kas ir saistīts ar uzņēmumu, un pārbaudiet vērtību **lauka Grāmatvedības valūta** cilnē **Vispārīgi**.

Ja līguma vienībā un Virsgrāmatas ierakstā iestatītā valūta nesakrīt, saglabājot ierakstu, koriģējiet konfigurāciju vai atlasiet dažādas vērtības. Sistēma pieprasa, lai šie ieraksti atbilstu, lai nodrošinātu pareizas starpuzņēmumu rēķinu plūsmas. Plašāku informāciju par starpuzņēmumu konfigurācijām skatiet Create [intercompany transactions.](../../project-accounting/create-intercompany-transactions.md)

Ja uzņēmuma ierakstam nav saistīta Virsgrāmatas ieraksta, tas norāda, ka, iestatot vidi, trūkst konfigurācijas. Sistēmas administratoram ir jālabo konfigurācija. Sistēmas administratoram jādodas uz **divu rakstīšanas konfigurācijām** un jāaptur un jārestartē **Ledgers divrakstāšanas karte** ar šīs kartes sākotnējo sinhronizāciju, un tas ir priekšnosacījumi. Papildinformāciju skatiet sadaļā [Project Operations duālās rakstīšanas karšu versijas](../../environment/resource-dual-write-maps.md).
