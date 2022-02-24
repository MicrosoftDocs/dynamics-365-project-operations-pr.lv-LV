---
title: Projekta kopēšana
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumiem risinājumā Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479528"
---
# <a name="copy-a-project"></a>Projekta kopēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Izmantojot opciju Dynamics 365 Project Operations, varat ātri izveidot jaunus projektus, atlasot **Kopēt projektu** veidlapā **Projekti**. Lai kopētu projektu, atveriet to projektu, ko vēlaties kopēt, un pēc tam atlasiet **Kopēt projektu**. Ar šo darbību tiks kopēta šāda informācija:

- Projekta rekvizīti (prognozētais sākuma datums tiek kopēts no avota projekta)
- Darba sadalījuma struktūra
- Projekta darba grupas dalībnieki
- Projekta aprēķins
- Projekta izmaksu aplēses

## <a name="project-properties"></a>Projekta rekvizīti

Kopējot projektu, tiek kopētas šādu lauku vērtības:

- Nosaukums/vārds, uzvārds
- Apraksts
- Klients
- Kalendāra veidne
- Valūta
- Līgumslēdzēja vienība
- Projekta vadītājs
- Statuss
- Vispārējs projekta statuss
- Komentāri
- Novērtējumi
- Prognozējamais sākuma datums
- Beigu datums
- Ieguldījums (stundas)
- Novērtētās darba izmaksas
- Novērtētās izdevumu izmaksas

## <a name="work-breakdown-structure"></a>Darba sadalījuma struktūra

Kopējot projektu, tiek kopēts visa ar resursu ielādētā darba sadalījuma struktūra. Nosauktie resursi tiek aizstāti ar vispārējiem resursiem. Ja nosauktajiem resursiem nav tādas pašas darba stundas kā vispārējam resursam, grafiks tiks pārrēķināts, un var mainīties uzdevumu ilgums.

## <a name="project-team-members"></a>Projekta darba grupas dalībnieki

Kad tiek kopēta projekta darba grupa no avota projekta, tiek kopēti vispārējie resursi. Arī vispārējo resursu piešķires tiek paturētas tādas, kādas tās bija avota projektā. Nosauktie resursi tiks konvertēti par vispārīgiem darba grupas dalībniekiem.

## <a name="estimates"></a>Novērtējumi

Kopējot projektu, gan resursu, gan izmaksu aprēķinu rindas tiek kopētas no avota projekta. 

Informāciju par to, kā programmiski piekļūt projekta kopēšanai, skatiet rakstā [Projekta veidņu izstrāde, izmantojot projekta kopēšanu](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
