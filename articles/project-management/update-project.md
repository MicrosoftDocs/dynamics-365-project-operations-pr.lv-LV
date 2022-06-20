---
title: Projekta izveide un atjaunināšana
description: Šajā rakstā sniegta informācija par projektu atjaunināšanu Projekta operācijas.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911099"
---
# <a name="create-and-update-a-project"></a>Projekta izveide un atjaunināšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Tālāk ir kopsavilkums par laukiem, kurus var atjaunināt projektā pēc tā izveides. Pamatojoties uz šiem atjauninājumiem, tajā ir ietvertas arī jebkādas piemērojamas izmaiņas.

## <a name="project-detail-fields"></a>Projekta informācijas lauki

- **Nosaukums**: projekta nosaukums.
- **Apraksts**: projekta pārskats.
- **Klients**: uzņēmums, kam tiks nodrošināts projekts.
- **Kalendāra veidne**: projekta darba laiks. Mainot lauku, tiek pārrēķināts viss grafiks.
- **Valūta**: projekta valūta. Šī lauka noklusējuma vērtība tiek pamatota uz valūtu, kas ir definēta līguma slēgšanas vienībā. Atjauninot līgumslēdzēja vienību, tiek atjaunināts arī šis lauks.
- **Līgumslēdzēja vienība**: organizācijas struktūrvienība, kas pārstāv uzņēmuma grupu vai nodaļu, kas ir primāri atbildīga par pārdošanas darījuma iegūšanu, kā arī darba un pakalpojumu sniegšanas klientam pārvaldību.  Ja projekta vadītāja papildu vienība nav definēta, šajā laukā tiek noklusējuma vērtība, kas ir definēta projekta parametros.
- **Projekta vadītājs**: projekta darba grupas dalībnieks, kuram ir pilnvaras pārskatīt un apstiprināt laika ierakstus un izdevumus.

## <a name="estimate-fields"></a>Aprēķina lauki

- **Plānotais sākuma datums**: datums, kurā sāksies projekts. Atjauninot šo lauku, visi projekta uzdevumi tiks proporcionāli pārvietoti uz jauno sākuma datumu.
- **Beigu datums**: datums, kurā plānots pabeigt projektu.
- **Ieguldījums**: paredzamais projekta ieguldījums. Kad projektam ir pievienoti uzdevumi, šis lauks vairs nav rediģējams.
- **Novērtētās darba izmaksas**: novērtētās projekta darba izmaksas. Kad projektam ir pievienotas darba izmaksas, šis lauks vairs nav rediģējams.
- **Paredzamie izdevumi** : paredzamie projekta izdevumi. Kad projektam ir pievienoti izdevumi, šis lauks vairs nav rediģējams.

## <a name="project-actual-fields"></a>Projekta faktisko datu lauki
- **Faktiskais sākums**: projekta sākšanas datums.
- **Faktiskais beigu laiks**: ir jāatjaunina, kad projekts ir pabeigts.

## <a name="project-status-fields"></a>Projekta statusa lauki

- **Vispārējais projekta statuss**: projekta vadītāja nodrošinātā vispārējā projekta veselība.
- **Komentāri**: projekta vadītāja sniegtais apraksts par projekta pašreizējo veselību.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
