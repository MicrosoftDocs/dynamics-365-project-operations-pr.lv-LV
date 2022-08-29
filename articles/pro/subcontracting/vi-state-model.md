---
title: Statusa pārejas uz kreditora rēķinu
description: Šajā rakstā ir izskaidrotas štata pārejas kreditora rēķinā pakalpojumā Microsoft Dynamics 365 Project Operations.
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

Šajā rakstā ir izskaidrotas štata pārejas kreditora rēķinā pakalpojumā Microsoft Dynamics 365 Project Operations. Tiek izmantoti šādi stāvokļi: **Melnraksts**, **Pārskatīšana**, **Apstiprināts**, **Aizturēts** un **Atcelts**.

Tālāk ilustrācijās ir parādītas statusa pārejas.

![Apakšuzņēmuma līgumu valsts pārejas modelis.](../media/VI_State_Model.jpg)

Nākamajā tabulā ir paskaidrots, ko katrs štats pārstāv kreditora rēķina dzīves ciklā programmā Project Operations.

| Novads | Apraksts | Atļautās pārejas |
| --- | --- | --- |
| Melnraksts | Šis stāvoklis ir kreditora rēķina sākotnējais stāvoklis. Līnijas un cenas var tikt mainītas. Kreditora rēķinu šādā stāvoklī var rediģēt un dzēst. | Procesā |
| Pārskatīšanā | Šis stāvoklis atspoguļo kreditora rēķina apstrādes stāvokli. Vismaz vienai kreditora rēķina rindai verifikācijas statuss **ir Pašlaik**. | Apstiprināts, Aizturēts |
| Apstiprināts | Šis stāvoklis atspoguļo kreditora rēķina stadiju, kurā lietojumprogramma ir izveidojusi faktiskos izmaksu aprēķinus katrai kreditora rēķina rindai. Visas saistītās izmaksu faktiskās izmaksas, kas tika saskaņotas ar kreditoru rēķina rindām, ir anulētas un aizstātas ar faktiskajām izmaksām no šīm kreditoru rēķinu rindām. Kreditora rēķinu šādā stāvoklī nevar rediģēt vai dzēst. Varat izmantot **pogu Atcelt**, lai atceltu apstiprinātu kreditora rēķinu. Darbība Atcelt apvērš darbības Apstiprināt ietekmi. | Atcelta |
| Aizturēts | <p>Šis stāvoklis ir kreditora rēķina posms, kurā kreditora rēķins nevar tikt pārvietots rēķina problēmas vai kreditora statusa dēļ. Kreditora rēķinu šādā stāvoklī nevar apstiprināt, atcelt, rediģēt vai dzēst.</p><p>Darbību "Atkārtoti atvērt" varat izmantot, lai kreditora rēķinu pārvietotu uz **melnraksta** vai **recenzijas** stāvokli. Ja vismaz vienai rindai kreditora rēķinā verifikācijas statuss **ir Pabeigts** vai **Pabeigts**, kreditora rēķins tiks atkārtoti atvērts **pārskatīšanas** stāvoklī. Ja visām rindām kreditora rēķinā verifikācijas statuss **ir Nav sākts** **, kreditora rēķins tiks atkārtoti atvērts stāvoklī Melnraksts**.</p> | Melnraksts, tiek pārskatīts |
| Atcelta | Šī valsts ir apakšuzņēmuma līguma posms, kurā vairs nav nepieciešama faktiska materiālu piegāde un/vai darbs, izmantojot resursus, par kuriem noslēgti apakšlīgumi. Apakšlīgumu šajā štatā nevar izmantot, lai novērtētu un personāla projektu vajadzības pēc resursiem un materiāliem, kā arī nevar atsaukties uz laiku, izdevumiem un materiālu izmantošanu projektā. Apakšlīgumu šādā stāvoklī nevar rediģēt vai izdzēst. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
