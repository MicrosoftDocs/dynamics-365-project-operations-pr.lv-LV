---
title: Statusa pārejas uz kreditora rēķinu
description: Šajā rakstā ir izskaidrotas statusa pārejas piegādātāja rēķinā programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261026"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Statusa pārejas uz kreditora rēķinu

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā rakstā ir izskaidrotas statusa pārejas piegādātāja rēķinā programmā Microsoft Dynamics 365 Project Operations. Tiek lietoti šādi statusi: **Melnraksts**, **Pārskatīšanā**, **Apstiprināts**, **Aizturēt** un **Atcelts**.

Šīs statusu pārejas ir attēlotas tālāk esošajās ilustrācijās.

![Apakšlīguma statusa pārejas modelis.](../media/VI_State_Model.jpg)

Tālāk redzamajā tabulā ir izskaidrots, ko katrs statuss atspoguļo piegādātāja rēķina dzīves cikla laikā programmā Project Operations.

| Novads | Apraksts | Atļautās pārejas |
| --- | --- | --- |
| Melnraksts | Šis statuss ir piegādātāja rēķina sākotnējais statuss. Rindas un izcenojums var tikt modificēts. Šajā statusā piegādātāja rēķinu var rediģēt un dzēst. | Procesā |
| Pārskatīšanā | Šis statuss atspoguļo piegādātāja rēķina apstrādes stāvokli. Vismaz vienai piegādātāja rēķina rindai ir pārbaudes statuss **Norisē**. | Apstiprināts, aizturēts |
| Apstiprināts | Šis statuss atspoguļo piegādātāja rēķina posmu, kurā lietojumprogramma katrai piegādātāja rēķina rindai ir izveidojusi faktiskās izmaksās. Visas saistītās faktiskās izmaksas, kas tika saskaņotas ar piegādātāja rēķina rindām, ir apgrieztas un aizstātas ar faktiskajām izmaksām no šīm piegādātāja rēķina rindām. Šajā statusā piegādātāja rēķinu nevar rediģēt vai dzēst. Lai atceltu apstiprinātu piegādātāja rēķinu, varat izmantot pogu **Atcelt**. Atcelšanas darbība apgriež apstiprināšanas darbības ietekmi. | Atcelta |
| Aizturēts | <p>Šis statuss atspoguļo piegādātāja rēķina posmu, kurā piegādātāja rēķinu nevar pārvietot, jo ar rēķinu vai piegādātāja statusu ir radusies problēma. Šajā statusā piegādātāja rēķinu nevar apstiprināt, atcelt, rediģēt vai dzēst.</p><p>Varat izmantot atkārtotas atvēršanas darbību, lai piegādātāja rēķinu pārvietotu uz statusu **Melnraksts** vai **Pārskatīšanā**. Ja vismaz vienai piegādātāja rēķina rindai ir pārbaudes statuss **Norisē** vai **Pabeigts**, piegādātāja rēķins tiks atkārtoti atvērts ar statusu **Pārskatīšanā**. Ja visām piegādātāja rēķina rindām ir pārbaudes statuss **Nav sākts**, piegādātāja rēķins tiek atkārtoti atvērts ar statusu **Melnraksts**.</p> | Melnraksts, pārskatīšanā |
| Atcelta | Šis statuss atspoguļo apakšlīguma posmu, kurā materiālu un/vai darba faktiskā nodrošināšana, ko veic apakšlīguma resursi, vairs nav nepieciešama. Šajā stāvoklī apakšlīgumu nevar izmantot, lai novērtētu un nokomplektētu projekta prasības resursiem un materiāliem, kā arī tam nevar izveidot atsauci uz laiku, izdevumiem un materiālu lietojumu projektā. Šajā statusā apakšlīgumu nevar rediģēt vai dzēst. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
