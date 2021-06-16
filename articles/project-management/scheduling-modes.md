---
title: Plānošanas režīmi
description: Šajā tēmā ir sniegta informācija par plānošanas režīmiem.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981444"
---
# <a name="scheduling-modes"></a>Plānošanas režīmi

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Dynamics 365 Project Operations sniedz organizācijām iespēju definēt, kā pārvaldīt galveno mainīgo izmaiņas darba sadalījuma struktūras uzdevumos. Pamatojoties uz organizācijas specifiskajām vajadzībām, projekta vadītāji var veikt plānošanas režīma izmaiņas projekta izveides laikā.

Programmā Project Operations ir pieejami trīs plānošanas režīmi.

  - Fiksēts ilgums (šis ir noklusējuma režīms)
  - Fiksēts darbs
  - Fiksētas vienības

Vērtības, ko ietekmē noteikta plānošanas režīma definēšana, nosaka šāda formula:

  Ieguldījums (*Darbs*) = Ilgums x vienības

Definējot projekta plānošanas režīmu, tiek iestatīta viena no šīm vērtībām, ko pēc tam nevar mainīt. Paturot šo vērtību kā nemainīgu, tā tiek iestatīta kā prioritāte, kas nozīmē, ka sistēma to nemaina, kad tiek mainītas abas pārējās vērtības. Tālāk redzamajā tabulā ir sniegta informācija par katra konkrētā režīma atlases ietekmi.

| **Šajā uzdevumā**             | **Ja tiek pārskatītas vienības**   | **Ja tiek pārskatīts ilgums** | **Ja tiek pārskatīts ieguldījums**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Fiksētu vienību uzdevums     | Ilgums tiek pārrēķināts. | Ieguldījums tiek pārrēķināts.    | Ilgums tiek pārrēķināts. |
| Fiksēta ieguldījuma uzdevums    | Ilgums tiek pārrēķināts. | Vienības tiek pārrēķinātas.    | Ilgums tiek pārrēķināts. |
| Fiksēta ilguma uzdevums  | Ieguldījums tiek pārrēķināts.   | Ieguldījums tiek pārrēķināts.    | Vienības tiek pārrēķinātas.   |

Papildinformāciju par konkrētā režīma nosacījumiem skatiet sadaļā [Uzdevuma tipa mainīšana precīzākai plānošanai](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). Tēmā tiek lietots vārds **Darbs**, nevis **Ieguldījums**.

## <a name="change-the-organizations-scheduling-mode"></a>Organizācijas plānošanas režīma maiņa

Lai definētu organizācijas plānošanas režīmu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Iestatījumi** \> **Vispārīgi** \> **Parametri** un pēc tam atlasiet projekta parametru. 
2. Lapā **Projekta parametri** atlasiet organizācijas noklusējuma plānošanas režīmu un pēc tam definējiet projekta vadītāja iespēju pārlabot iestatījumu, izveidojot jaunu projektu.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Plānošanas režīma iestatījuma maiņa projektam

Ja organizācija ļauj projekta vadītājam pārlabot noklusējuma plānošanas režīmu, projekta vadītājs var veikt šīs izmaiņas, izveidojot jaunu projektu. Tomēr pēc projekta saglabāšanas plānošanas režīmu nevar mainīt.

## <a name="copied-projects"></a>Kopēti projekti

Tā kā projekts tiek izveidots, veicot projekta kopēšanas darbību, projekta vadītājs nevar iestatīt plānošanas režīmu. Mērķa projekta režīms vienmēr tiek iestatīts pēc noklusējuma, kas definēts organizācijas līmenī.

## <a name="copied-tasks"></a>Kopētie uzdevumi

Kad uzdevums tiek kopēts no viena projekta uz citu, uzdevums pārmanto mērķa projekta plānošanas režīmu.