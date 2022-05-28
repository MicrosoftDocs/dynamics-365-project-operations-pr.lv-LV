---
title: Stāvokļa pārejas kreditora rēķinā
description: Šajā tēmā ir izskaidrotas statusa pārejas kreditora rēķinā programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584697"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Stāvokļa pārejas kreditora rēķinā

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šajā tēmā ir izskaidrotas statusa pārejas kreditora rēķinā programmā Microsoft Dynamics 365 Project Operations. Tiek izmantoti šādi stāvokļi: **Melnraksts**, **Pārskatīšana**, **Apstiprināts**, **Aizturēts** un **Atcelts**.

Tālāk ilustrācijās ir parādītas statusa pārejas.

![Apakšlīguma stāvokļa pārejas modelis.](../media/VI_State_Model.jpg)

Šajā tabulā ir izskaidrots, ko katrs štats attēlo kreditora rēķina dzīves ciklā projekta operācijās.

| Novads | Apraksts | Atļautās pārejas |
| --- | --- | --- |
| Melnraksts | Šis stāvoklis ir kreditora rēķina sākotnējais stāvoklis. Rindas un cenas var tikt mainītas. Kreditora rēķinu šajā stāvoklī var rediģēt un dzēst. | Notiek |
| Pārskatīšanā | Šis stāvoklis atspoguļo kreditora rēķina apstrādes stāvokli. Vismaz vienai kreditora rēķina rindai ir notiekoša pārbaudes **statuss**. | Apstiprināts, Aizturēts |
| Apstiprināts | Šis stāvoklis apzīmē kreditora rēķina stadiju, kurā programma ir izveidojusi izmaksu faktiskos apjomus katrai kreditora rēķina rindai. Visas saistītās izmaksu faktiskās darbības, kas tika saskaņotas ar kreditora rēķina rindām, ir atsauktas un aizstātas ar izmaksu faktiskajām izmaksām no šīm kreditora rēķina rindām. Kreditora rēķinu šajā stāvoklī nevar rediģēt vai dzēst. Lai atceltu apstiprinātu piegādātāja rēķinu, **var izmantot pogu Atcelt**. Atcelšanas darbība atceļ darbības Apstiprināt ietekmi. | Atcelta |
| Aizturēts | <p>Šis stāvoklis ir kreditora rēķina stadija, kurā kreditora rēķins nevar pārvietoties, jo ir radusies problēma ar rēķinu vai piegādātāja statusu. Kreditora rēķinu šajā stāvoklī nevar apstiprināt, atcelt, rediģēt vai dzēst.</p><p>Varat izmantot darbību Atkārtoti atvērt, lai pārvietotu kreditora rēķinu uz **statusu Melnraksts** vai **Pārskatīšana**. Ja vismaz vienai kreditora rēķina rindai ir pārbaudes statuss **Notiek** vai **Pabeigts**, kreditora rēķins tiks atvērts no jauna **pārskatīšanas** stāvoklī. Ja visām kreditora rēķina rindām pārbaudes statuss nav **sākts**, kreditora rēķins tiks atvērts no jauna **melnraksta** stāvoklī.</p> | Melnraksts, Pārskatāms |
| Atcelta | Šis stāvoklis ir apakšlīguma posms, kurā vairs nav nepieciešama faktiska materiālu piegāde un/vai darbs ar apakšuzņēmēju resursiem. Apakšuzņēmuma līgumu šajā stāvoklī nevar izmantot, lai novērtētu un personāla projekta vajadzības resursiem un materiāliem, kā arī nevar atsaukties uz projekta laiku, izdevumiem un materiālu izmantošanu. Apakšuzņēmuma līgumu šajā stāvoklī nevar rediģēt vai dzēst. | Nevienu |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
