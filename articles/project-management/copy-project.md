---
title: Projekta kopēšana
description: Šajā tēmā sniegta informācija par projektu kopēšanu risinājumā Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131802"
---
# <a name="copy-a-project"></a>Projekta kopēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Izmantojot Dynamics 365 Project Operations, varat ātri izveidot jaunus projektus, atlasot **Kopēt projektu** veidlapā **Projekti**. Lai kopētu projektu, atveriet to projektu, ko vēlaties kopēt, un pēc tam atlasiet **Kopēt projektu**. Ar šo darbību tiks kopēta šāda informācija:

- Projekta rekvizīti
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