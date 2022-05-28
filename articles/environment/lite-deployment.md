---
title: Izvietot projekta operācijas — Lite
description: Šajā tēmā ir sniegta informācija par to, kā instalēt Project Operations Lite izvietošanu — pāreju uz proforma rēķinu izrakstīšanu.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580741"
---
# <a name="deploy-project-operations---lite"></a>Izvietot projekta operācijas — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_



Project Operations atbalsta vairākus izvietošanas modeļus. Lai noteiktu labāko izvietošanas modeli, skatiet sadaļu [Izvietošanas tipi](determine-deployment-type.md).


> [!IMPORTANT]
> Šī izvietošana jeb Lite izvietošana — pāreja uz proforma rēķinu izrakstīšanu, izraisa **Project Operations izvietošanu tikai Dataverse**.

- [Projekta operāciju instalēšana jaunā Dataverse vidē](#new)
- [Instalēšana esošā Dataverse vidē](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Projekta operāciju instalēšana jaunā Dataverse vidē

1. [Kā globālais vai Power Platform administrators](/power-platform/admin/global-service-administrators-can-administer-without-license) ar projekta operāciju licenci izveidojiet jaunu Dataverse vidi PowerPlatform administrēšanas [centrā](https://admin.powerplatform.com). Pārliecinieties, **vai ir iespējota šīs vides** datu bāzes izveide un **Dynamics 365 Programmas**. Papildinformāciju skatiet šeit: [Vides izveide un pārvaldība, izmantojot Power Platform administrēšanas centru](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Dynamics 365 programmu izvietošanas sarakstā atlasiet **Microsoft Dynamics 365 Project Operations**.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Projekta operāciju instalēšana esošā Dataverse vidē
1. Pārliecinieties, vai vide nav konfigurēta ar [dubultu rakstīšanu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), jo instalēšana pēc tam instalēs [projekta operācijas resursu/neuzkrātu scenāriju](project-operations-integrated-deployment-overview.md) iespējām.
2. Kā [Globāls vai Power Platform administrators](/power-platform/admin/global-service-administrators-can-administer-without-license) ar Project Operations licenci atrodiet vidi [PowerPlatform administrēšanas centrā](https://admin.powerplatform.com), kur vēlaties instalēt Project Operations.
3. Instalējiet **Microsoft Dynamics 365 Project Operations** no Dynamics 365 programmu izvietošanas saraksta. Papildinformāciju skatiet šeit: [Dynamics Dynamics 365 programmu pārvaldība](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
