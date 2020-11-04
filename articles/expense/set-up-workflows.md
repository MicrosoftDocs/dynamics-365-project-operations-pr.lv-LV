---
title: Izdevumu pārvaldības darbplūsmu iestatīšana
description: Varat iestatīt darbplūsmas procesu, kas tiek izmantots, lai pārskatītu komandējumu un izdevumu dokumentus.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080471"
---
# <a name="set-up-workflows-for-expense-management"></a>Izdevumu pārvaldības darbplūsmu iestatīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Varat iestatīt darbplūsmas procesu, lai pārskatītu komandējumu un izdevumu dokumentus. Varat definēt darbplūsmas izdevumu atskaitēm, komandējumu pieprasījumiem un avansa pieprasījumiem.

Darbplūsma reprezentē biznesa procesu un nosaka, kā dokuments plūst pa sistēmu. Darbplūsma arī norāda, kam ir jāizpilda uzdevums vai jāapstiprina dokuments. Darbplūsmas sistēmas lietošanai jūsu organizācijā ir vairākas priekšrocības:

- **Konsekventi procesi** : Jūs varat definēt konkrētu dokumentu apstiprināšanas procesu, piemēram, iegādes pieprasījumus un izdevumu atskaites. Darbplūsmas sistēmas lietošana palīdz nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti konsekventi un efektīvi.
- **Procesa redzamība** : Varat izsekot konkrētās darbplūsmas instances statusam, vēsturei un veiktspējas metrikai. Tādējādi varat noteikt, vai darbplūsmā vajadzētu veikt izmaiņas, lai uzlabotu efektivitāti.
- **Centralizēts darba saraksts** : Lietotāji var skatīt centralizētu darba sarakstu, lai skatītu darbplūsmu uzdevumus un tiem piešķirtos apstiprinājumus. 

## <a name="workflow-types"></a>Darbplūsmu veidi

Šajā tabulā uzskaitīti darbplūsmu veidi, kuras varat izveidot **Izdevumu pārvaldībā**.


|              <strong>Tips</strong>              |                   <strong>Izmantojiet šo veidu, lai</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Izdevumu atskaišu automātiska apstiprināšana</strong> |            Izveidojiet izdevumu atskaišu apstiprināšanas darbplūsmas.             |
|  <strong>Izdevumu atskaišu automātiska publicēšana</strong>   |        Izveidojiet automātiskas publicēšanas darbplūsmas izdevumu atskaitēm.        |
|       <strong>Izdevumu rindas elements</strong>        |     Izveidojiet apstiprināšanas darbplūsmas rindas elementiem izdevumu atskaitēs.      |
| <strong>Izdevumu rindas elementa automātiska publicēšana</strong> | Izveidojiet automātiskas publicēšanas darbplūsmas rindas elementiem izdevumu atskaitēs. |
|       <strong>Ceļojuma pieprasījums</strong>       |          Izveidojiet apstiprināšanas darbplūsmas komandējumu pieprasījumiem.           |
|      <strong>Avansa maksājuma pieprasījums</strong>      |         Izveidojiet apstiprināšanas darbplūsmas avansa maksājumu pieprasījumiem.          |
|        <strong>PVN atmaksa</strong>        | Izveidojiet apstiprināšanas darbplūsmas pievienotās vērtības nodokļa (PVN) atmaksai.  |
