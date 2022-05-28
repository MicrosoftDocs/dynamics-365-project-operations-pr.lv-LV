---
title: Pierakstīšanās priekšskatījuma abonementam — Lite
description: Šajā tēmā ir sniegta informācija par to, kā abonēt un izvietot Project Operations Lite izvietošanu — pāreju uz proforma rēķinu izrakstīšanu.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3b06ac29e8021967490534d3aefc8b5ce733413b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588009"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Priekšskatījuma abonementa reģistrācija — Lite 

Šajā tēmā izskaidrots, kā reģistrēties izmēģinājumversijas piedāvājumam un izvietot Dynamics 365 Project Operations Lite izvietošanu — piedāvājums pro forma rēķinu izrakstīšanai.

> [!NOTE]
> Šis process tiks mainīts nākamajā Project Operations laidienā.

## <a name="prerequisites"></a>Priekšnosacījumi
- Lietotājam, kurš izvieto priekšskatījumu, ir jābūt Azure nomnieka globālā administratora tiesībām. Pirmā piedāvājuma izmantošanas laikā var izveidot nomnieku.

> [!IMPORTANT]
> Šis uzdevums organizācijā ir jāveic tikai vienai personai, t.i., nomnieka administratoram. Ja neesat šī laidiena abonents, nogaidiet, līdz organizācija būs reģistrējusies un būsit saņēmis savus lietotāja akreditācijas datus.
> 
> Izmēģinājumversijas nomnieka statusā ir vienreizējai lietošanai. Izmēģinājumversiju var palaist tikai vienu reizi. Izmēģinājumversijas nolūkiem ieteicams izveidot jaunu nomnieku.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations izmēģinājumversija 

Pirms sākšanas pārliecinieties, vai esat pieteicies pārlūkprogrammā ar lietotāja darba kontu nomniekā, kurā vēlaties veikt Project Operations priekšskatīšanu.

1. Lai izmantotu pirmo piedāvājuma kodu, **Dynamics 365 Project Operations**, dodieties uz sadaļu [Project Operations izmēģinājumversija](https://aka.ms/try-po).
2. Apstipriniet pasūtījumu.

  Tiks parādīts apstiprinājums par piedāvājums veiksmīgu izmantošanu.

## <a name="assign-licenses"></a>Licenču piešķiršana

> [!IMPORTANT]
> Lai izpildītu tālāk norādītās darbības, jums ir jābūt administratīvai piekļuvei savas organizācijas Microsoft 365 portālam.


1. Dodieties uz [Microsoft 365 administrēšanas centru](https://portal.office.com/), lai lietotājiem piešķirtu licences.
2. Lapā **Aktīvie lietotāji** atlasiet lietotājus, kuriem vēlaties piešķirt licenci.
3. Pārbaudiet, vai ir atlasīta **Dynamics 365 Project Operations** licence. 
4. Atlasiet **Saglabāt izmaiņas**.

## <a name="create-a-new-dataverse-environment"></a>Izveidot jaunu Dataverse vidi

1. Izveidojiet jaunu Project Operations Dataverse izvietošanas vidi, izpildot norādījumus tēmā [Dataverse izvietošanas modelis](lite-deployment.md). Kad atlasāt vides tipu, noteikti izmantojiet **Izmēģinājumversija (ar abonementiem)**.

  ![Jauna vide.](./media/19CreateEnvironment.png)

2. Atlasiet iestatījumu **Iespējot Dynamics 365 programmas** un atstājiet iestatījumu **Automātiski izvietot šīs programmas**.  
3. Atlasiet **Saglabāt**, lai izveidotu vidi.

  ![Pievienot datu bāzi.](./media/20CreateEnvironment1.png)

4. Kad vide ir izveidota, instalējiet **Microsoft Dynamics 365 Project Operations** risinājumu. 

![Risinājuma instalēšana.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS konfigurācijas un iestatīšanas demonstrācijas instalēšana

Instalējiet CDS konfigurāciju un iestatiet demonstrācijas datus, izpildot norādījumus tēmā [Demonstrācijas iestatīšanu un konfigurācijas datu lietošana](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
