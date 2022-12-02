---
title: Projekta kopēšana
description: Šajā rakstā ir sniegta informācija par projektu kopēšanu programmā Microsoft Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925773"
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
- Projekta kontrolsaraksti
- Projekta bloki

## <a name="project-properties"></a>Projekta rekvizīti

Kopējot projektu, tiek kopētas šādu lauku vērtības.

| Kolonna | Project Operations ārpus noliktavas materiāliem | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Nosaukums/vārds | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Apraksts | :heavy_check_mark: | :heavy_check_mark: | |
| klient | :heavy_check_mark: | :heavy_check_mark: | |
| Kalendāra veidne | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valūta | :heavy_check_mark: | :heavy_check_mark: | |
| Līgumslēdzēja vienība | :heavy_check_mark: | :heavy_check_mark: | |
| Atbildīgais uzņēmums | :heavy_check_mark: | | |
| Projekta vadītājs | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Statuss | :heavy_check_mark: | :heavy_check_mark: | |
| Vispārējs projekta statuss | :heavy_check_mark: | :heavy_check_mark: | |
| Komentāri | :heavy_check_mark: | :heavy_check_mark: | |
| Aprēķini | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Prognozējamais sākuma datums</p><p><strong>Piezīme.</strong> Šis lauks norāda paredzamo sākuma datumu, kad projekts tiek izveidots no kopijas. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Plānotais beigu datums</p><p><strong>Piezīme.</strong> Datums šajā laukā tiek pielāgots atkarībā no jaunā jeb no kopijas izveidotā projekta sākuma datuma.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Ieguldījums (stundas) | :heavy_check_mark: | :heavy_check_mark: | |
| Novērtētās darba izmaksas | :heavy_check_mark: | :heavy_check_mark: | |
| Novērtētās izdevumu izmaksas | :heavy_check_mark: | :heavy_check_mark: | |
| Prognozēto materiālu izmaksas | | :heavy_check_mark: | |

> [!NOTE]
> Projekta kopēšana ir ilgstoša darbība. Tiek kopēti arī projekta ieraksti, saistītie atribūti un daudzas saistītās entītijas. Darbības ilguma dēļ pēc kopēšanas sākšanas mērķa projekta lapa tiek bloķēta rediģēšanai, līdz kopēšanas darbība ir pabeigta.

## <a name="work-breakdown-structure"></a>Darba sadalījuma struktūra

Kopējot projektu, tiek kopēts visa ar resursu ielādētā darba sadalījuma struktūra. Nosauktie resursi tiek aizstāti ar vispārējiem resursiem. Ja nosauktajiem resursiem nav tādas pašas darba stundas kā vispārējam resursam, grafiks tiks pārrēķināts, un var mainīties uzdevumu ilgums.

## <a name="project-team-members"></a>Projekta darba grupas dalībnieki

Kad tiek kopēta projekta darba grupa no avota projekta, tiek kopēti vispārējie resursi. Arī vispārējo resursu piešķires tiek paturētas tādas, kādas tās bija avota projektā. Nosauktie resursi tiks konvertēti par vispārīgiem darba grupas dalībniekiem.

> [!NOTE]
> Darba grupas dalībnieki un piešķīrumi netiek kopēti Project for the Web.

## <a name="estimates"></a>Aprēķini

Kad tiek kopēts projekts, izdevumu un materiālu aprēķinu rindas tiek kopētas no avota projekta. 

Informāciju par to, kā programmiski piekļūt projekta kopēšanai, skatiet rakstā [Projekta veidņu izstrāde, izmantojot projekta kopēšanu](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Piedāvājumi un līgumi

Piedāvājumi un līgumi nav saistīti ar mērķa projektu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
