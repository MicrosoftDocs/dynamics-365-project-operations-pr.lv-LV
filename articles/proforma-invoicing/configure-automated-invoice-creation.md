---
title: Automātiskas rēķina izveides konfigurēšana
description: Šajā tēmā sniegta informācija par to, kā konfigurēt sistēmu, lai automātiski izveidotu rēķinus.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0dddd963e79f8ecd91a96a6e684ab79e1b95bd6d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287922"
---
# <a name="configure-automatic-invoice-creation"></a>Automātiskas rēķina izveides konfigurēšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_


Izpildiet šīs darbības, lai konfigurētu automatizētu rēķinu izpildi risinājumā Dynamics 365 Project Operations.

1. Dodieties uz **Iestatījumi** > **Lielapjoma darbi**.
2. Izveidojiet lielapjoma darbu un nosauciet to **Projekta darbību rēķinu izveide**. Lielapjoma darba nosaukumā jābūt iekļautiem vārdiem “rēķinu izveide”.
3. Laukā **Darba tips** atlasiet vienumu **Nav**. **Pēc noklusējuma** Biežuma aizkave **Aktīvs** opcijas ir iestatītas uz **Jā.**
4. Atlasiet **Palaist darbplūsmu**. Dialoglodziņā **Meklēt ierakstu** redzēsiet trīs darbplūsmas.

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Atlasiet vienumu **ProcessRunCaller** un pēc tam **Pievienot**.
6. Nākamajā dialoglodziņā atlasiet **Labi**. Darbplūsma **Miegs** seko darbplūsmai **Apstrādāt**.

  > [!NOTE]
  > 5. darbībā varat arī atlasīt **ProcessRunner**. Pēc tam, kad atlasā **Labi** **Apstrādāt** darbplūsmai seko **Miegs** darbplūsma.

**ProcessRunCaller** un **ProcessRunner** darbplūsmas veido rēķinus. **ProcessRunCaller** izsauc **ProcessRunner**. **ProcessRunner** ir darbplūsma, kas faktiski izveido rēķinus. Tā darbojas caur visām līguma rindām, kurām ir jāizveido rēķini, un izveido rēķinu šīm rindām. Lai noteiktu līguma rindas, kurām jāizveido rēķini, darbs tiek apskatīts līguma rindu rēķina izpildes datumos. Ja līguma rindām, kas attiecas uz vienu līgumu, ir vienāds rēķina izpildes datums, darījumi tiek apvienoti vienā rēķinā, kurā ir divas rēķina rindas. Ja nav nevienas transakcijas rēķinu izveidei, darbs izlaiž rēķina veidošanu.

Kad **ProcessRunner** ir beidzis darboties, tas izsauc **ProcessRunCaller**, nodrošina beigu laiku un ir slēgts. **ProcessRunCaller** pēc tam sāk skaitīt laiku, kas darbojas 24 stundas no norādītā beigu laika. Taimera laika skaitīšanas beigās **ProcessRunCaller** tiek slēgts.

Lielapjoma izpildes darbs rēķinu izveidošanai ir kārtējais darbs. Ja šis pakešapstrādes process ir palaists vairākas reizes, tiek izveidoti vairāki darba gadījumi un var tikt izraisītas kļūdas. Tāpēc pakešapstrāde jāsāk tikai vienu reizi, un tā ir jārestartē tikai tad, ja tā pārstāj darboties.

> [!NOTE]
> Lielapjomu rēķinu izveide darbojas vienīgi projekta līguma rindām, kuras ir konfigurējuši rēķinu grafiki. Līguma rindai ar fiksētu cenas aprēķina metodi jābūt konfigurētiem atskaites punktiem. Projekta līguma rindai ar laika un materiālu aprēķinu metodi ir jābūt iestatītam datuma bāzes rēķina grafikam. Tas pats attiecas uz līguma rindu, kuras pamatā ir projekts.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]