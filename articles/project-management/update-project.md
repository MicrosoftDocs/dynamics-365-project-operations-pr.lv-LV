---
title: Projekta atjaunināšana
description: Šajā tēmā ir sniegta informācija par projektu atjaunināšanu programmā Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897821"
---
# <a name="update-a-project"></a>Projekta atjaunināšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Tālāk ir sniegts kopsavilkums par laukiem, ko var atjaunināt projektā pēc tā izveides, kā arī jebkādu spēkā esošu atjauninājumu ietekmi.

## <a name="project-detail-fields"></a>Projekta informācijas lauki

- **Nosaukums**: projekta nosaukums.
- **Apraksts**: projekta pārskats.
- **Klients**: uzņēmums, kam tiks nodrošināts projekts.
- **Kalendāra veidne**: projekta darba laiks. Mainot lauku, tiek pārrēķināts viss grafiks.
- **Valūta**: projekta valūta. Šī lauka pamatā pēc noklusējuma ir līgumslēdzēja vienībai definētā valūta. Atjauninot līgumslēdzēja vienību, tiek atjaunināts arī šis lauks.
- **Līgumslēdzēja vienība**: organizācijas struktūrvienība, kas pārstāv uzņēmuma grupu vai nodaļu, kas ir primāri atbildīga par pārdošanas darījuma iegūšanu, kā arī darba un pakalpojumu sniegšanas klientam pārvaldību. 
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

