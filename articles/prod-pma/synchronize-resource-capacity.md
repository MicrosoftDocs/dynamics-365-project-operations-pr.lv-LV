---
title: Resursu noslodzes sinhronizēšana
description: Šajā tēmā ir sniegta informācija par to, kā sinhronizēt resursa noslodzi kalendāros un projektos.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f2e9b8e189be0594569e14ebc41c6ed452afd10aba34ea1397b3e3f66cd2e96
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005625"
---
# <a name="synchronize-resource-capacity"></a>Resursu noslodzes sinhronizēšana

[!include [banner](../includes/banner.md)]

Resursa sinhronizēšanas procesi palīdz nodrošināt, ka kalendāra un bāzes kalendāra informācija nonāk projekta resursa plānošanā. Ja kalendārs ir mainīts, procesi veic nepieciešamos projekta resursu plānošanas atjauninājumus. Šie procesi arī palīdz uzlabot veiktspēju, jo kalendāra resursa informācija tiek iepriekš sinhronizēta. Tāpēc resursa plānošanas informācijas atjauninājumi tiek veikti ātrāk. Mēs jums iesakām plānot procesus kā paketi, nevis pa vienam. Pretējā gadījumā pastāv risks, ka kāds aizmirsīs iekļaujošos datumus, kuros informācija pēdējo reizi tika sinhronizēta. Ja iekļaujošie datumi netiek lietoti, datumu sinhronizācijas laikā var rasties atstarpes.

![Kalendāra sinhronizācija.](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sinhronizējiet resursa noslodzes apkopojumus

Sinhronizācijas process ir paredzēts, lai sinhronizētu visu resursa kalendāra informāciju. Šī informācija ietver bāzes kalendāra informāciju par jebkādām izmaiņām, kas veiktas projekta resursa kalendāra noslodzes tabulā. Ja projektam tiek pievienoti jauni resursi, sinhronizācija palīdz nodrošināt, ka ir pieejama atjaunināta informācija par kalendāru. Šo sinhronizāciju var veikt jebkurā laikā.

Mēs iesakām lietot paketi. Opcijas ir pieejamas noslodzes rezervāciju sinhronizācijas laikā.

1. Atlasiet **Projekta pārvaldība un uzskaite** &gt; **Periodiski** &gt; **Noslodzes sinhronizācija** &gt; **Sinhronizēt resursu noslodzes apkopojumus**.
2. Iestatiet opcijas no šīs tabulas.

    | Opcija      | Apraksts |
    |-------------|-------------|
    | Perioda kods | Ja vēlaties, atlasiet virsgrāmatas datuma intervāla kodu, lai iestatītu sākuma un beigu datumus resursu noslodzes apkopojumu sinhronizācijas procesam. |
    | Sākuma datums  | Ievadiet resursa noslodzes apkopojuma sinhronizācijas procesa sākuma datumu. |
    | Beigu datums    | Ievadiet resursa noslodzes apkopojuma sinhronizācijas procesa beigu datumu. |

[![Sinhronizācijas process.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]