---
title: Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā tēmā ir sniegta informācija par to, kā abonēt un izvietot Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948972"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā tēmā ir izskaidrots, kā abonēt priekšskatījuma/partnera piedāvājumu un izvietot Project Operations vidi scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem.

## <a name="prerequisites"></a>Priekšnosacījumi

- Jūs saņemsit e-pasta ziņojumu, kurā jūs uzaicinās piedalīties priekšskatījumā. Varat pieprasīt priekšskatījumu [Project Operations vietnē](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Lietotājam, kurš izvieto priekšskatījumu, ir jābūt Azure nomnieka globālā administratora tiesībām.
- Finance vides izvietošanai ir nepieciešams derīgs Azure abonements, kam rēķins tiks izrakstīts par katru vidi. Lai sāktu darbu, varat izmantot esošu organizācijas abonementu vai izmantot [Azure izmēģinājumversiju](https://azure.microsoft.com/en-us/free/). CDS vide tiks nodrošināta bez maksas ierobežotā 30 dienu periodā.

## <a name="subscribe"></a>Abonēt

Kad jūsu [priekšskatījuma pieprasījums](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) tiks apstiprināts, e-pastā saņemsit divus piedāvājumus no Microsoft. Šie piedāvājumi jums ļauj izvietot Project Operations priekšskatījumu:

- Dynamics 365 Project Operations — priekšskatījuma izmēģinājumversija
- Dynamics 365 for Finance and Operations priekšskatījuma izmēģinājumversija.

> [!IMPORTANT]
> Šis uzdevums organizācijā ir jāveic tikai vienai personai, t.i., nomnieka administratoram. Ja neesat šī laidiena abonents, nogaidiet, līdz organizācija būs reģistrējusies un būsit saņēmis savus lietotāja akreditācijas datus.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations — priekšskatījuma izmēģinājumversija

1. Izmantojiet pirmo piedāvājumu, **Dynamics 365 Project Operations izmēģinājumversiju**, ar iepazīšanās e-pasta ziņojumā sniegto vietrādi URL.

![Pirmais piedāvājums](./media/1FirstOffer.png)

2. Pārbaudiet, vai esat pieteicies kā lietotājs, kurš pieder organizācijai, kas abonēs pakalpojumu.
3. Pēc tam izmantojiet piedāvājumu. 
4. Atlasiet **Jā, pievienot manam kontam**.

![Izmantot piedāvājumu](./media/2RedeemFirstOffer.png)

![Apstiprināt piedāvājumu](./media/3ConfirmFirstOffer.png)

![Piedāvājums izmantots](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance priekšskatījuma izmēģinājumversija

Atkārtojiet tās pašas darbības otrajam iepazīšanās e-pasta ziņojumā ietvertajam piedāvājumam.

## <a name="assign-licenses"></a>Licenču piešķiršana

> [!IMPORTANT]
> Lai izpildītu tālāk norādītās darbības, jums ir jābūt administratīvai piekļuvei savas organizācijas Office 365 portālam.

1. Dodieties uz [Microsoft 365 administrēšanas centru](https://portal.office.com/), lai piešķirtu lietotājiem licences.

![Office administrēšanas portāls](./media/5OfficeAdminPortal.png)

2. Lapā **Aktīvie lietotāji** atlasiet lietotājus, kuriem vēlaties piešķirt licenci.

![Licenču piešķiršana](./media/6AssignLicenses.png)

3. Pārbaudiet, vai ir atlasīta Project Operations licence, un atlasiet **Saglabāt izmaiņas**. 

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

