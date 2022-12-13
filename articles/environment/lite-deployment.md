---
title: Izvietot Project Operations Lite
description: Šajā rakstā ir sniegta informācija par to, kā instalēt Project Operations Lite izvietošanu — pāreju uz proforma rēķinu izrakstīšanu.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810988"
---
# <a name="deploy-project-operations-lite"></a>Izvietot Project Operations Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_



Project Operations atbalsta vairākus izvietošanas modeļus. Lai noteiktu labāko izvietošanas modeli, skatiet sadaļu [Izvietošanas tipi](determine-deployment-type.md).


> [!IMPORTANT]
> Šī izvietošana jeb Lite izvietošana — pāreja uz proforma rēķinu izrakstīšanu, izraisa **Project Operations izvietošanu tikai Dataverse**.

- [Project Operations instalēšana jaunā Dataverse vidē](#new)
- [Instalēšana esošā Dataverse vidē](#existing)
- [Instalēšana esošā Dataverse vidē, kurā ir divējādas rakstīšanas komponenti](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Project Operations Lite instalēšana jaunā Dataverse vidē

1. Kā [Globālās vai Power Platform administrators](/power-platform/admin/global-service-administrators-can-administer-without-license) ar Project Operations licenci, izveidojiet jaunu Dataverse vidi [PowerPlatform administrēšanas centrā](https://admin.powerplatform.com). Pārliecinieties ka ir iespējota funkcija **Izveidot datubāzi šai videi** un **Dynamics 365 lietojumprogrammas**. Papildinformāciju skatiet šeit: [Vides izveide un pārvaldība, izmantojot Power Platform administrēšanas centru](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Dynamics 365 programmu izvietošanas sarakstā atlasiet **Microsoft Dynamics 365 Project Operations**.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Project Operations Lite instalēšana esošā Dataverse vidē 
1. Kā [Globāls vai Power Platform administrators](/power-platform/admin/global-service-administrators-can-administer-without-license) ar Project Operations licenci atrodiet vidi [PowerPlatform administrēšanas centrā](https://admin.powerplatform.com), kur vēlaties instalēt Project Operations.
1. Instalējiet **Microsoft Dynamics 365 Project Operations** no Dynamics 365 programmu izvietošanas saraksta. Papildinformāciju skatiet šeit: [Dynamics Dynamics 365 programmu pārvaldība](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Instalējiet Project Operations Lite esošā Dataverse vidē, kur jau ir pieejami dubultās rakstīšanas risinājumi

Ja vēlaties turpināt Project Operations palaišanu Lite izvietošanas režīmā, rīkojieties šādi:

1. Kā [Globāls vai Power Platform administrators](/power-platform/admin/global-service-administrators-can-administer-without-license) ar Project Operations licenci atrodiet vidi [PowerPlatform administrēšanas centrā](https://admin.powerplatform.com), kur vēlaties instalēt Project Operations.
1. Instalējiet **Microsoft Dynamics 365 Project Operations** no Dynamics 365 programmu izvietošanas saraksta. Papildinformāciju skatiet šeit: [Dynamics Dynamics 365 programmu pārvaldība](/power-platform/admin/manage-apps).
1. Tā kā jūsu vidē ir instalēti duālās rakstīšanas komponenti, kas palīdz integrēties finance and operations programmās, Project Operations instalācija instalēs arī iespējas un paplašinājumus, kas nepieciešami, lai integrētu ar projektu saistītos datus finance and operations programmās. Tā kā vēlaties palaist Project Operations Lite izvietojumā, šie integrācijas komponenti ir jānoņem, jo tie radīs ierobežojumus un pieskaitāmās izmaksas Lite izvietošanas scenārijiem. Manuāli atinstalējiet risinājumus **Dynamics 365 Project Operations Dual Write un** Dual Write **Dynamics 365 Project Operations entītiju kartes**, lai noņemtu šos komponentus.
1. Dodieties uz Projekta **operācijas -> Iestatījumi -> parametri**. Atveriet lapu Detalizēta informācija par **projekta parametru** un iestatiet **lauka Risinājuma jaunināšanas darbība** vērtību **Tikai lite**. Tādējādi tiek nodrošināts, ka turpmākie Project Operations jauninājumi neatgriezīs integrācijas komponentus programmā Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
