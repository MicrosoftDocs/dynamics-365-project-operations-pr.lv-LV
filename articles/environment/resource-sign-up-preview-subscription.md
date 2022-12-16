---
title: Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem
description: Šajā rakstā ir sniegta informācija par to, kā abonēt un izvietot Project Operations uz resursiem/krājumiem nebalstītiem scenārijiem.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842025"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Reģistrēšanās Project Operations priekšskatījuma abonementiem scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_



Šajā rakstā izskaidrots, kā pierakstīties izmēģinājumversijas piedāvājumam un izvietot Project Operations vidi resursos /noliktavā neesošos krājumos balstītiem scenārijiem.

## <a name="prerequisites"></a>Priekšnosacījumi
- Lietotājam, kurš izvieto priekšskatījumu, ir jābūt Azure nomnieka globālā administratora tiesībām. Pirmā piedāvājuma izmantošanas laikā var izveidot nomnieku. 
- Finance vides izvietošanai ir nepieciešams derīgs Azure abonements, kam rēķins tiks izrakstīts par katru vidi. Lai sāktu darbu, varat izmantot esošu organizācijas abonementu vai izmantot [Azure izmēģinājumversiju](https://azure.microsoft.com/free/). CDS vide tiks nodrošināta bez maksas ierobežotā 30 dienu periodā.

> [!IMPORTANT]
> Šis uzdevums organizācijā ir jāveic tikai vienai personai, t.i., nomnieka administratoram. Ja neesat šī laidiena abonents, nogaidiet, līdz organizācija būs reģistrējusies un būsit saņēmis savus lietotāja akreditācijas datus.
> 
> Izmēģinājumversijas nomnieka statusā ir vienreizējai lietošanai. Izmēģinājumversiju var palaist tikai vienu reizi. Izmēģinājumversijas nolūkiem ieteicams izveidot jaunu nomnieku.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) — izmēģinājumversijas priekšskatīšana 

Pirms sākšanas pārliecinieties, vai esat pieteicies pārlūkprogrammā ar lietotāja darba kontu nomniekā, kurā vēlaties veikt Project Operations priekšskatīšanu.

1. Izmantojiet pirmo piedāvājuma kodu **Dynamics 365 Project Operations** šeit [Project Operations izmēģinājumversija](https://aka.ms/try-po).
2. Apstipriniet pasūtījumu.

  Jūs redzēsit, ka apstiprinājuma piedāvājums ir veiksmīgi izpirkts.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance priekšskatījuma izmēģinājums

Dodieties uz sadaļu [Dynamics 365 for Finance izmēģinājumversijas priekšskatījums](https://aka.ms/trypoche) un atkārtojiet iepriekšējā sadaļā norādītās darbības piedāvājumam Reģistrēšanās mākonī viesotai videi.  

## <a name="assign-licenses"></a>Licenču piešķiršana

> [!IMPORTANT]
> Lai izpildītu tālāk norādītās darbības, jums ir jābūt administratīvai piekļuvei savas organizācijas Microsoft 365 portālam.

1. Dodieties uz [Microsoft 365 administrēšanas centru](https://portal.office.com/), lai lietotājiem piešķirtu licences.

2. Lapā **Aktīvie lietotāji** atlasiet lietotājus, kuriem vēlaties piešķirt licenci.

3. Pārbaudiet, vai ir atlasīta **Dynamics 365 Project Operations** licence un atlasiet **Saglabāt izmaiņas**.

> [!NOTE]
> Finance izmēģinājumversijas piedāvājums nav jāpiešķir lietotājam.

## <a name="start-a-new-project-in-lcs"></a>Jauna projekta sākšana LCS

Izveidojiet jaunu LCS projektu, kā aprakstīts rakstā [Jauna projekta sākšana LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Azure abonementa pievienošana LCS projektam

Lai izpildītu šo uzdevumu, veiciet darbības, kas aprakstītas rakstā [Azure abonementa pievienošana LCS projektam](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Finance demonstrācijas vides izvietošana ar Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem

Lai pabeigtu izvietošanu, izpildiet norādījumus, kas sniegti rakstā [Jaunas vides nodrošināšana](resource-provision-new-environment.md). Izmantojiet priekšskatījumam [demonstrācijas vides](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) izvietošanas tipu. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS iestatīšanas un konfigurācijas datu instalēšana

Instalējiet CDS iestatīšanas un konfigurācijas datus, kā aprakstīts rakstā [Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service](resource-apply-pro-setup-config-data.md).
Pabeidziet šo darbību tikai pēc tam, kad Ir Finance demonstrācijas vide ir izvietota un demonstrācijas dati ir gatavi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
