---
title: Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā tēmā ir sniegta informācija par to, kā abonēt un izvietot Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a6dfa51f59119834230b7c9f8859a9d85eaae999
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642976"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā ir izskaidrots, kā abonēt priekšskatījuma/partnera piedāvājumu un izvietot Project Operations vidi scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.

## <a name="prerequisites"></a>Priekšnosacījumi

- Jūs saņemsit e-pasta ziņojumu, kurā jūs uzaicinās piedalīties priekšskatījumā. Varat pieprasīt priekšskatījumu [Project Operations vietnē](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Lietotājam, kurš izvieto priekšskatījumu, ir jābūt Azure nomnieka globālā administratora tiesībām.
- Finance vides izvietošanai ir nepieciešams derīgs Azure abonements, kam rēķins tiks izrakstīts par katru vidi. Lai sāktu darbu, varat izmantot esošu organizācijas abonementu vai izmantot [Azure izmēģinājumversiju](https://azure.microsoft.com/en-us/free/). CDS vide tiks nodrošināta bez maksas ierobežotā 30 dienu periodā.

## <a name="subscribe"></a>Abonēt

Kad jūsu [priekšskatījuma pieprasījums](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) tiks apstiprināts, e-pastā saņemsit trīs piedāvājumus no Microsoft. Šie piedāvājumi jums ļauj izvietot Project Operations priekšskatījumu:

- Dynamics 365 Project Operations (CRM) — priekšskatījuma izmēģinājumversija
- Office 365 Project Operations — priekšskatījuma izmēģinājumversija
- Dynamics 365 Finance — priekšskatījuma izmēģinājumversija

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

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance priekšskatījuma izmēģinājumversija

Atkārtojiet tās pašas darbības pēdējam iepazīšanās e-pasta ziņojumā ietvertajam piedāvājumam.

## <a name="assign-licenses"></a>Licenču piešķiršana

> [!IMPORTANT]
> Lai izpildītu tālāk norādītās darbības, jums ir jābūt administratīvai piekļuvei savas organizācijas Microsoft 365 portālam.

1. Dodieties uz [Microsoft 365 administrēšanas centru](https://portal.office.com/), lai piešķirtu licences saviem lietotājiem.

![Administrēšanas centra sākumlapa](./media/14AdminPortal.png)

2. Lapā **Aktīvie lietotāji** atlasiet lietotājus, kuriem vēlaties piešķirt licenci.

![Licenču piešķiršana](./media/15AssignLicenses.png)

3. Pārbaudiet, vai ir atlasīta **Dynamics 365 Project Operations (CRM) priekšskatījums** un **Office 365 Project Operations — priekšskatījums** licence, un atlasiet **Saglabāt izmaiņas**.

> [!NOTE]
> Finance izmēģinājumversijas piedāvājums nav jāpiešķir lietotājam.

## <a name="start-a-new-project-in-lcs"></a>Jauna projekta sākšana LCS

Izveidojiet jaunu LCS projektu, kā aprakstīts tēmā [Jauna projekta sākšana LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure abonementa pievienošana LCS projektam

Lai izpildītu šo uzdevumu, veiciet darbības, kas aprakstītas tēmā [Azure abonementa pievienošana LCS projektam](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Finance demonstrācijas vides izvietošana ar Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

Lai pabeigtu izvietošanu, izpildiet norādījumus, kas sniegti tēmā [Jaunas vides nodrošināšana](resource-provision-new-environment.md). Izmantojiet priekšskatījumam [demonstrācijas vides](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) izvietošanas tipu. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS iestatīšanas un konfigurācijas datu instalēšana

Instalējiet CDS iestatīšanas un konfigurācijas datus, kā aprakstīts tēmā [Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service](resource-apply-pro-setup-config-data.md).
Pabeidziet šo darbību tikai pēc tam, kad finanšu demonstrācijas vide ir izvietota un demo dati FO ir gatavi.
