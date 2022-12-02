---
title: Project Operations atjaunināšana Finance vidē
description: Šajā rakstā ir sniegta informācija par to, kā atjaunināt uz Project Operations jūsu Dynamics 365 Finance vidē.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: aedfd815521054d58944496500aa03a27be9267b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030044"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Project Operations atjaunināšana Finance vidē

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_


Šajā rakstā ir sniegta informācija par to, kā atjaunināt Dynamics 365 Project Operations jūsu Dynamics 365 Finance vidē. Lai atjauninātu Project Operations uz 5. atjauninājumu (UR5): ir nepieciešams veikt trīs procedūras:

- [Importējiet pakotni jūsu iepriekšējā priekšskatījuma projektā](#import)
- [Lietojiet atjauninājumu](#apply)
- [Atjauniniet Dataverse vidi](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importējiet pakotni savā LCS projektā

1. Piesakieties [Lifecycle Services (LCS)](https://lcs.dynamics.com/) kā projekta īpašnieks vai vides vadītājs.
2. Projektu sarakstā atlasiet savu LCS projektu.
3. Lapā **Projekts**, grupā **Vides** atveriet vidi, kuru vēlaties atjaunināt.
4. Pārbaudiet, vai vide darbojas. Ja tā nav sāknēta, sāknējiet vidi.
5. Sadaļas **Pieejami atjauninājumi** sadaļā **Jauns laidiens** atlasiet **Skatīt atjauninājumu** 10.0.15.

![Skatīt atjaunināšanas pogu.](media/view-update.png)

6. Lapā **Binārie atjauninājumi** atlasiet **Saglabāt pakotni**.
7. Lapā **Pārskatīt un saglabāt atjauninājumus** atlasiet **Saglabāt pakotni**.
8. Rūtī **Saglabāt pakotni līdzekļu bibliotēkā**, kura tiek atvērta, ievadiet pakotnes nosaukumu un pēc tam atlasiet **Saglabāt pakotni**.
9. Kad LCS ir pabeidzis pakotnes saglabāšanu, tiek iespējota poga **Gatavs**. Atlasiet **Gatavs**. LCS pārbaudīs pakotni. Pārbaude var ilgt dažas minūtes vai līdz pat vienu stundu.


## <a name="apply-the-package-update"></a><a name="apply"></a>Lietojiet pakotnes atjauninājumu

1. LCS lapā **Vides informācija** atlasiet **Uzturēt** > **Lietot atjauninājumus**.
2. Sarakstā atlasiet pakotni, kuru saglabājāt iepriekš un pēc tam atlasiet **Lietot**.
3. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties izvietot pakotni.

![Apstipriniet pakotnes izvietošanas dialoglodziņu.](media/confirm-package-deployment.png)

4. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atjaunināt lietojumprogrammu.

![Apstipriniet lietojumprogrammas atjaunināšanas dialoglodziņu.](media/confirm-application-update.png)

Tiks sākta izvietošana un lietojumprogrammas atjaunināšana. 

Lapas **Vides informācija** augšējā labajā stūrī vides statuss tiks atjaunināts uz **Apkalpošana**. Atjaunināšana tiks pabeigta pēc aptuveni divām stundām. Lietojumprogrammas laidiena informācija tiks atjaunināta uz  **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** un vides statuss tiks atjaunināts uz **Izvietota**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Atjauniniet savu Dataverse vidi

1. Pierakstieties [Power Platform administrēšanas centrā](https://admin.powerplatform.com/).
2. Sarakstā atrodiet un atveriet vidi, kuru izmantojāt, lai instalētu Project Operations.
3. Lapā **Vides** atlasiet **Resurss** > **Dynamics 365 lietojumprogrammas**.
4. Sarakstā atrodiet **Microsoft Dynamics 365 Project Operations** un kolonnā **Statuss** atlasiet **Pieejamais atjauninājums**.
5. Atzīmējiet izvēles rūtiņu **Piekrītu servisa nosacījumiem** un pēc tam atlasiet **Atjaunināt**. Tiks instalēta risinājuma jaunākā versija.

Pēc instalēšanas pabeigšanas būs uzinstalēta versija 4.5.0.134.

## <a name="configure-new-features"></a>Jaunu līdzekļu konfigurēšana

### <a name="enable-dual-write-mapping"></a>Duālās rakstīšanas kartēšanas iespējošana

Pēc tam, kad pabeidzat atjaunināšanu Finance un Dataverse vidēs, varat iespējot nepieciešamos duālās rakstīšanas kartējumus. Izpildiet šīs procedūras, lai iespējotu duālās rakstīšanas kartējumus.

- [Atjauniniet drošības iestatījumus Customer Engagement vidē](#security)
- [Atsvaidziniet datu vienības](#refresh)
- [Atjauniniet un palaidiet duālās rakstīšanas kartējumus](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Atjauniniet drošības iestatījumus Dataverse vidē

Kā daļa no UR5 atjaunināšanas ir nepieciešami šādi entitīju drošības privilēģiju atjauninājumi.

1. Savā Dataverse vidē dodieties uz **Iestatījumi** un grupā **Sistēma** atlasiet **Drošība**.

![Dataverse vides iestatījumi.](media/Picture21.png)

2. Atlasiet **Drošības lomas**.
3. Lomu sarakstā atlasiet **duālās rakstīšanas programmas lietotājs** un atlasiet cilni **Pielāgotās entitījas**. 
4. Pārbaudiet, vai lomai ir **Lasīšanas** un **Pievienošanas atļaujas** elementiem:

      - **Valūtas maiņās kursa veids**
      - **Uzņēmumu tabula** 
      - **Finanšu kalendārs** 
      - **Virsgrāmata**

5. Pēc drošības lomas atjaunināšanas dodieties uz **Iestatījumi** > **Drošība** > **Darba grupas**. Pārbaudiet, vai darba grupai tiek lietota loma **duālās rakstīšanas programmas lietotājs**. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Atsvaidziniet datu entitījas no atjauninājuma

1. Finance vidē atveriet **Datu pārvaldības** darbvietu un pēc tam atveriet lapu **Struktūras parametri**.
2. Cilnē **Entitījas iestatījumi** atlasiet **Atsvaidzināt entitīju sarakstu**.
3. Lai apstiprinātu entitījas atsvaidzināšanu atlasiet **Aizvērt**.

 > [!NOTE]
 > Šī procesa pabeigšanai būs nepieciešamas aptuveni 20 minūtes. Kad atsvaidzināšana būs pabeigta, jūs saņemsit ziņojumu.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Duālās rakstīšanas kartējumu atjaunināšana

1. Darbvietā **Datu pārvaldība** atlasiet **Duālā rakstīšana**.
2. Atlasiet **Lietot risinājumus**, atlasiet sarakstā abus risinājumus un pēc tam atlasiet **Lietot**.
3. Lapā **Duālā rakstīšana** attlasiet šādus tabulu kartējumus, pēc tam atlasiet **Apturēt**.

    - **Project Operations integrācijas faktiskie dati (msdyn_actuals)**
    - **Project Operations integrācijas projekta izmaksu kategorijas (msdyn_expensecategories)**
    - **Project Operations integrācijas faktisko datu projekta izmaksu eksporta entitīja (msdyn_expenses)**

4. Lapā **Tabulas kartes versija** lietojiet jauno kartes versiju katrai no trim entitījām.
5. Lapā **Duālā rakstīšana** atlasiet palaišanu, lai restartētu kartes.
6. Karšu sarakstā atlasiet karti **Virsgrāmata (msdyn_ledgers)** ar visiem priekšnosacījumiem un atzīmējiet izvēles rūtiņu **Sākotnējā sinhronizācija**. 
7. Laukā **Sākotnējās sinhronizācijas šablons** atlasiet **Finanšu un operāciju programmas** un pēc tam atlasiet **Palaist**.
 
 ![Virsgrāmatas kartes sinhronizācija.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]