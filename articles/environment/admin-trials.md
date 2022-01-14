---
title: Reģistrēšanās Project Operations izmēģinājumversijām
description: Šajā tēmā ir sniegta informācija par to, kā izvietot Dynamics 365 Project Operations izmēģinājumversiju.
author: ruhercul
ms.date: 12/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e40b4ac23241730f5c2db89f0dc674083f9e7abe
ms.sourcegitcommit: 8f970b46d0303dafaa75fc7d00567d232e1e600b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901626"
---
# <a name="sign-up-for-project-operations-trials"></a>Reģistrēšanās Project Operations izmēģinājumversijām 

_**Attiecas uz:** Project Operations resursu balstītiem/krājumu nebalstītiem scenārijiem, Lite izvietošanu — darbu ar pro forma rēķiniem, Project Operations krājumu/ražošanas balstītiem scenārijiem_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā ir izskaidrots, kā abonēt priekšskatījuma partneru piedāvājumu un izvietot Dynamics 365 Project Operations vidi.

Izmantojot jauno Project Operations izmēģinājumversiju, varat automātiski izvietot jebkuru no trim atbalstītajiem izvietošanas scenārijiem, aizpildot anketu, kas iesaka labāko izvietošanas pieeju. Šajā tēmā ir sniegta informācija par to, kā:

- izmantot izmēģinājumversijas piedāvājumu;
- sākt nodrošināšanu;
- konfigurēt duālo rakstīšanu;
- iegūt papildinformāciju par Project Operations. 

Tālāk redzamajā tabulā ir sniegta detalizēta informācija par jauno izmēģinājumversijas piedāvājumu.

| **Piedāvājuma vienums**               | **Detalizēta informācija**                                  |
|------------------------------|----------------------------------------------|
| Piedāvājuma tips                   | Šis piedāvājuma tips ir Administratora interesents, tādēļ ir nepieciešams nomnieka administrators, lai piedāvājumu izmantotu. |
| Piedāvājuma izmantošana                    | Vienu reizi katram nomniekam                          |
| Piedāvājuma ilgums               | 30 kalendārās dienas                             |
| Izmantošana katram nomniekam       | 1                                            |
| Lietotāju skaits              | 25                                           |
| Paplašinājums                    | 1 paplašinājums, 30 kalendārās dienas               |
| Izmēģinājuma vižu skaits | 3                                            |


## <a name="admin-trial-details"></a>Detalizēta informācija par administratora izmēģinājumversiju
Tālāk redzamajā tabulā ir sniegta detalizēta informācija par izmēģinājumversijām un to piemērošanu katram izvietošanas tipam.

| **Vienums**                      | **Lite**                                     | **Uz krājumiem nebalstīti materiāli** | **Uz krājumiem balstīti materiāli** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Nodrošinātie iestatīšanas dati           | Jā                                          | Jā                       | Jā (USSI)            |
| Transakciju dati            | Nē.                                           | Nē.                        | Nē.                    |
| Nodrošināšanas laiks minūtēs  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Priekšnosacījumi
Lai izvietotu Dynamics 365 Project Operations izmēģinājumversiju, nepieciešami tālāk norādītie priekšnosacījumi.

- Reģistrējieties [Dynamics 365 Project Operations — izmēģinājumversijas priekšskatīšana](https://www.aka.ms/try-po).
- Lietotājam, kurš izvieto priekšskatījumu, ir jābūt Azure nomnieka globālā administratora tiesībām.

> [!IMPORTANT]
> Šis uzdevums ir jāveic tikai vienai personai organizācijā — nomnieka administratoram. Ja neesat šī laidiena abonents, nogaidiet, līdz organizācija būs reģistrējusies un būsit saņēmis savus lietotāja akreditācijas datus.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations — priekšskatījuma izmēģinājumversija 

Pirms darba sākšanas piesakieties pārlūkprogrammā ar lietotāja darba kontu tajā nomniekā, kur vēlaties Project Operations priekšskatījumu.

1. Izmantojiet pirmo piedāvājuma kodu **Dynamics 365 Project Operations — priekšskatījuma izmēģinājumversija**, ielīmējot to pārlūkprogrammas URL.

    ![Izmantot piedāvājumu](./media/16RedeemFirstOfferNew.png)

2. Apstipriniet pasūtījumu.

    ![Pasūtījuma apstiprināšana](./media/17ConfirmOrderNew.png)

  Tiks parādīts apstiprinājums par piedāvājums veiksmīgu izmantošanu.

   ![Apstiprinājums](./media/18OrderConfirmationNew.png)

  Jūs tiksiet novirzīts uz [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Anketa un nodrošināšana

1.  Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.com/projectoperationstrial) un aizpildiet anketu.  
2.  Pārskatiet ieteikto izvietošanas tipu un atlasiet **Sākt iestatīšanu**, lai sāktu nodrošināšanu.
3.  Pārskatiet noteikumus un nosacījumus un tad atlasiet **Sākt**.

   Pēc nodrošināšanas sākšanas jūs tiekat novirzīts uz vižu sarakstu Power Platform administrēšanas centrā. Nodrošināšanas laikā vides stāvoklis ir **PreparingInstance**.
 
  Kad nodrošināšana ir pabeigta, vides statuss ir **Gatavs**. Vides nodrošināšana iekļauj demonstrācijas datu izvietošanu.
 
4.  Atlasiet attiecīgo Microsoft Dataverse URL un Finance and Operations programmas URL, lai validētu izvietošanu.

## <a name="configuring-dual-write"></a>Duālās rakstīšanas konfigurēšana
- Lai konfigurētu drošības lomas divrakstīšana, skatiet [rakstu Drošības iestatījumu atjaunināšana projekta operācijās programmā Dataverse](resource-provision-new-environment.md).
- Lai konfigurētu divrakstīšu kartes, skatiet rakstu [Projekta operāciju divrakstīšu karšu palaišana](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Licenču piešķiršana

Lai izpildītu tālāk norādītās darbības, jums ir jābūt administratīvai piekļuvei savas organizācijas Microsoft 365 portālam.

1. Dodieties uz [Microsoft 365 administrēšanas centru](https://portal.office.com/), lai lietotājiem piešķirtu licences.

   ![Administrēšanas centra sākumlapa](./media/14AdminPortal.png)

2. Lapā **Aktīvie lietotāji** atlasiet lietotājus, kuriem vēlaties piešķirt licenci.

   ![Licenču piešķiršana](./media/15AssignLicenses.png)

3. Pārbaudiet, vai ir atlasīta **Dynamics 365 Project Operations priekšskatījums** licence, un pēc tam atlasiet **Saglabāt izmaiņas**.

## <a name="additional-resources"></a>Papildu resursi

Sākot lietot Project Operations, tālāk sniegtajos resursos atradīsiet noderīgas norādes.

- [Videoklipu sērija — Project Operations pārskats, padziļināta informācija par līdzekļiem un ceļvedis](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Izvietošanas veida noteikšana](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Ko darīt, ja manā Finance and Operations programmu vidē ir nepieciešama ALM vai ELM?

- Partneriem, kuriem nepieciešamas pilna vides dzīves cikla pārvaldības iespējas, skatiet sadaļu [Partneru smilškastes licences pieprasījums](https://experience.dynamics.com/requestlicense), lai pārskatītu jauno partneru piedāvājumu. 
- Partneriem, kas meklē papildinformāciju par iekšējās lietošanas tiesībām, skatiet sadaļu [Iekšējās lietošanas tiesību mākoņa un programmatūras priekšrocības (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Vai izmēģinājumversijas termiņu var pagarināt pēc 30 dienām?
Lai pagarinātu izmēģinājumversijas termiņu, veiciet tālāk norādītās darbības.

1. **Microsoft 365 administrēšanas centrā** pārejiet uz lapu **Norēķini** > **Jūsu produkti**.
2. Atlasiet **Dynamics 365 Project Operations (CE) — izmēģinājumversijas priekšskatīšana**.
3. Sadaļā **Derīguma beigu datums** atlasiet **Pagarināt termiņu**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Vai var veikt jaunināšanu no Lite izvietojuma uz resursu/krājumos nebalstītu bāzes scenārija izvietojumu?
Pašlaik netiek atbalstīta vides jaunināšana no Lite uz krājumos nebalstītu izvietojumu.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Vai es varu piekļūt savu Finance vižu pakalpojumiem Lifecycle Services (LCS)?  
Nē. Šo izmēģinājumversiju izvietošana tiek veikta, izmantojot Power Platform administrēšanas centru. Piekļuve Finance videi ir ierobežota.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Vai izmēģinājumversiju var instalēt esošā vidē?
Ja jums ir esoša vide, būs atļauts instalēt Lite izvietojumu esošā pārdošanas Dataverse vidē no Power Platform administrēšanas centra.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
