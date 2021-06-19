---
title: Projekta kopēšana
description: Šajā tēmā ir sniegta informācija par projekta piedāvājumiem risinājumā Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091263"
---
# <a name="copy-a-project"></a>Projekta kopēšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Izmantojot opciju Dynamics 365 Project Operations, varat ātri izveidot jaunus projektus, atlasot **Kopēt projektu** veidlapā **Projekti**. Lai kopētu projektu, atveriet to projektu, ko vēlaties kopēt, un pēc tam atlasiet **Kopēt projektu**. Ar šo darbību tiek nokopēti tālāk norādītie vienumi.

- Projekta rekvizīti 
- Darba sadalījuma struktūra
- Projekta darba grupas dalībnieki
- Projekta aprēķins
- Projekta izmaksu aplēses
- Projekta materiālu aprēķini

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
- Aprēķini
- Paredzamais sākuma datums: šis ir datums, kad projekts tiek izveidots no kopijas.
- Paredzamais beigu datums: šis datums tiek pielāgots atkarībā no jaunā jeb no kopijas izveidotā projekta sākuma datuma.
- Ieguldījums (stundas)
- Novērtētās darba izmaksas
- Novērtētās izdevumu izmaksas
- Prognozēto materiālu izmaksas

> [!NOTE]
> Projekta kopēšana ir ilgstoša darbība. Tiek kopēti arī projekta ieraksti, saistītie atribūti un daudzas saistītās entītijas. Darbības ilguma dēļ pēc kopēšanas sākšanas mērķa projekta lapa tiek bloķēta rediģēšanai, līdz kopēšanas darbība ir pabeigta.

## <a name="work-breakdown-structure"></a>Darba sadalījuma struktūra

Kopējot projektu, tiek kopēts visa ar resursu ielādētā darba sadalījuma struktūra. Nosauktie resursi tiek aizstāti ar vispārējiem resursiem. Ja nosauktajiem resursiem nav tādas pašas darba stundas kā vispārējam resursam, grafiks tiks pārrēķināts, un var mainīties uzdevumu ilgums.

## <a name="project-team-members"></a>Projekta darba grupas dalībnieki

Kad tiek kopēta projekta darba grupa no avota projekta, tiek kopēti vispārējie resursi. Arī vispārējo resursu piešķires tiek paturētas tādas, kādas tās bija avota projektā. Nosauktie resursi tiks konvertēti par vispārīgiem darba grupas dalībniekiem.

## <a name="estimates"></a>Aprēķini

Kad tiek kopēts projekts, izdevumu un materiālu aprēķinu rindas tiek kopētas no avota projekta. 

Informāciju par to, kā programmiski piekļūt projekta kopēšanai, skatiet rakstā [Projekta veidņu izstrāde, izmantojot projekta kopēšanu](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
