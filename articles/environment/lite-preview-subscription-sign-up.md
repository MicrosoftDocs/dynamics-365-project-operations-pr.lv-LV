---
title: Pierakstīšanās priekšskatījuma abonementam — Lite
description: Šajā tēmā ir sniegta informācija par to, kā abonēt un izvietot Project Operations Lite izvietošanu — pāreju uz proforma rēķinu izrakstīšanu.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997430"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Pierakstīšanās priekšskatījuma abonementam — Lite 

Šajā tēmā izskaidrots, kā abonēt priekšskatījuma partnera piedāvājumu un izvietot Dynamics 365 Project Operations lite izvietošanu — darījumu, lai izrakstītu rēķinu proformai.

> [!NOTE]
> Šis process tiks mainīts nākamajā Project Operations laidienā.

## <a name="prerequisites"></a>Priekšnosacījumi

- Jūs saņemsit e-pasta ziņojumu, kurā jūs uzaicinās piedalīties priekšskatījumā. Varat pieprasīt priekšskatījumu [Project Operations vietnē](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Lietotājam, kurš izvieto priekšskatījumu, ir jābūt Azure nomnieka globālā administratora tiesībām.
- Iepazīstieties ar visiem noteikumiem un nosacījumiem.

## <a name="subscribe"></a>Abonēt

Kad saņemsit [priekšskatījuma pieprasījuma](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) apstiprinājumu, e-pastā saņemsit divus piedāvājumus no Microsoft. Šie piedāvājumi jums ļauj izvietot Project Operations priekšskatījumu:

- Dynamics 365 Project Operations (CRM) — priekšskatījuma izmēģinājumversija
- Office 365 Project Operations — priekšskatījuma izmēģinājumversija

> [!IMPORTANT]
> Šis uzdevums organizācijā ir jāveic tikai vienai personai, t.i., nomnieka administratoram. Ja neesat šī laidiena abonents, nogaidiet, līdz organizācija būs reģistrējusies un būsit saņēmis savus lietotāja akreditācijas datus.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) — priekšskatījuma izmēģinājumversija 

Pirms sākšanas pārliecinieties, vai esat pieteicies pārlūkprogrammā ar lietotāja darba kontu nomniekā, kurā vēlaties veikt Project Operations priekšskatīšanu.

1. Izmantojiet pirmo piedāvājuma kodu **Dynamics 365 Project Operations (CRM) — priekšskatījuma izmēģinājumversija**, ielīmējot to pārlūkprogrammas URL.

![Izmantot piedāvājumu](./media/16RedeemFirstOfferNew.png)

2. Apstipriniet pasūtījumu.
![Pasūtījuma apstiprināšana](./media/17ConfirmOrderNew.png)

Jūs redzēsit, ka apstiprinājuma piedāvājums ir veiksmīgi izpirkts.

![Apstiprinājums](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations — priekšskatījuma izmēģinājumversija

Veiciet tās pašas darbības kā ar pirmo piedāvājuma kodu. Pārliecinieties, vai pievienojat otro piedāvājuma kodu, izmantojot to pašu lietotāja kontu, kas tika izmantots ar pirmo piedāvājuma kodu.

## <a name="assign-licenses"></a>Licenču piešķiršana

> [!IMPORTANT]
> Lai izpildītu tālāk norādītās darbības, jums ir jābūt administratīvai piekļuvei savas organizācijas Microsoft 365 portālam.


1. Dodieties uz [Microsoft 365 administrēšanas centru](https://portal.office.com/), lai piešķirtu licences saviem lietotājiem.

![Administrēšanas centra sākumlapa](./media/14AdminPortal.png)

2. Lapā **Aktīvie lietotāji** atlasiet lietotājus, kuriem vēlaties piešķirt licenci.

![Licenču piešķiršana](./media/15AssignLicenses.png)

3. Pārbaudiet, vai ir atlasītas licences **Dynamics 365 Project Operations (CRM) priekšskatījums** un **Office 365 Project Operations — priekšskatījums**. 
4. Atlasiet **Saglabāt izmaiņas**.

## <a name="create-a-new-cds-environment"></a>Jaunas CDS vides izveide

1. Izveidojiet jaunu Project Operations CDS izvietošanas vidi, izpildot norādījumus tēmā [CDS izvietošanas modelis](lite-deployment.md). Kad atlasāt vides tipu, noteikti izmantojiet **Izmēģinājumversija (ar abonementiem)**.
![Jauna vide](./media/19CreateEnvironment.png)

2. Atlasiet iestatījumu **Iespējot Dynamics 365 programmas** un atstājiet iestatījumu **Automātiski izvietot šīs programmas**.  
3. Atlasiet **Saglabāt**, lai izveidotu vidi.

![Pievienot datu bāzi](./media/20CreateEnvironment1.png)

4. Kad vide ir izveidota, instalējiet **Microsoft Dynamics 365 Project Operations** risinājumu. 

![Risinājuma instalēšana](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS konfigurācijas un iestatīšanas demonstrācijas instalēšana

Instalējiet CDS konfigurāciju un iestatiet demonstrācijas datus, izpildot norādījumus tēmā [Demonstrācijas iestatīšanu un konfigurācijas datu lietošana](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]