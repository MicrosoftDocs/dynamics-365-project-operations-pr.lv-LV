---
title: Jaunas vides nodrošināšana
description: Šajā tēmā ir sniegta informācija par to, kā nodrošināt jaunu Project Operations vidi.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 03626cb1579fad7f8d8eb501905056cd13092754
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594863"
---
# <a name="provision-a-new-environment"></a>Jaunas vides nodrošināšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_



Šajā tēmā ir sniegta informācija par jaunas Dynamics 365 Project Operations vides nodrošināšanu scenārijiem, kas balstīti uz resursiem/bez krājumiem.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Project Operations automatizētās nodrošināšanas iespējošana LCS projektā

Veiciet tālāk norādītās darbības, lai iespējotu Project Operations automatizētās nodrošināšanas plūsmu savam LCS projektam.

1. Dodieties uz [LCS](https://lcs.dynamics.com/v2) un atlasiet elementu **Priekšskatījuma līdzekļa pārvaldība**.
2. Sarakstā **Priekšskatījuma līdzeklis** atlasiet **Project Operations līdzeklis** un pēc tam atlasiet **Priekšskatījuma līdzeklis iespējots**, lai iespējotu programmu Project Operations.

   > [!NOTE]
   > Šī darbība tiek veikta tikai viereiz katrā LCS projektā.

## <a name="provision-a-project-operations-environment"></a>Project Operations vides nodrošināšana

1. Atveriet jaunu Dynamics 365 Finance [demonstrācijas vidi](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) vai [smilškastes/ ražošanas vides](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) izvietošanu. 
2. Veiciet vednī **Vidnes nodrošināšana** norādītās darbības. 

   > [!IMPORTANT]
   > Pārliecinieties, vai atlasītā lietojumprogrammas versija ir 10.0.13 vai jaunāka.

3. Lai nodrošinātu Project Operations, sadaļā **Papildu iestatījumi** atlasiet **Common Data Service**. 
4. Iespējojiet **Common Data Service iestatījumu**, atlasot **Jā**, un pēc tam ievadiet informāciju obligātajos laukos:

  - Nosaukums/vārds, uzvārds
  - Reģions
  - Valoda
  - Valūta
 
5. Laukā **Common Data Service veidne** atlasiet **Project Operations** 
6. Atlasiet vides tipu savam izvietojumam. Abonementam atbilstošs izmēģinājums ļaus jums izvietot CDS vidi 30 dienas. 

     ![Izvietošanas iestatījumi.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Atlasiet **Piekrist**, lai apstiprinātu pakalpojuma noteikumus, un pēc tam atlasiet **Gatavs**, lai atgrieztos izvietošanas iestatījumos.
    >
    >![Izvietošanas piekrišana.](./media/2DeploymentConsent.png)

7. Neobligāti — Piemērojiet videi demonstrācijas datus. Dodieties uz **Papildu iestatījumi**, atlasiet **Pielāgot SQL datu bāzes konfigurāciju** un iestatiet **Noteikt datu kopu lietojumprogrammas datu bāzei** uz **Demonstrācija**.
8. Aizpildiet pārējos obligātos laukus vednī un apstipriniet izvietošanu. Laiks vides nodrošināšanai atšķiras atkarībā no vides veida. Nodrošināšana var ilgt līdz sešām stundām.

   Pēc veiksmīgas izvietošanas pabeigšanas vide tiks rādīta kā **Izvietota**.

9. Lai apstiprinātu, ka vide ir izvietota sekmīgi, atlasiet **Pieteikties** un piesakieties vidē, lai apstiprinātu.

    ![Vides informācija.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Atjauninājumu lietošana Finance vidē

Programmai Project Operations ir nepieciešama Finance vide ar lietojumprogrammas versiju **10.0.13 (10.0.569.20009)** vai jaunāku versiju.

Lai saņemtu šo versiju, iespējams, jūsu Finance videi būs jālieto kvalitātes atjauninājumi.

1. LCS lapas **Vides informācija** sadaļā **Pieejamie atjauninājumi** atlasiet **Skatīt atjauninājumu**.

    ![Atjauninājumu skatīšana.](./media/5ViewUpdates.png)

2. Lapā **Binārie atjauninājumi** atlasiet **Saglabāt pakotni.**

    ![Pakotnes saglabāšana.](./media/6SavePackage.png)

3. Noklikšķiniet uz **Atlasīt visu** un pēc tam atlasiet **Saglabāt pakotni**.

    ![Atjauninājumu pārskatīšana un saglabāšana.](./media/7ReviewAndSaveUpdates.png)

4. Ievadiet pakotnes nosaukumu un aprakstu un pēc tam atlasiet **Saglabāt**. Atkarībā no interneta savienojuma šis process var ilgt zināmu laiku.

    ![Pakotnes augšupielāde līdzekļu bibliotēkā.](./media/8UploadPackageToAssetsLibrary.png)

5. Pēc tam, kad pakotne ir saglabāta, atlasiet **Gatavs** un saglabājiet šo pakotni sava LCS projekta līdzekļu bibliotēkā.

   Pakotnes saglabāšana un validēšana var aizņemt aptuveni 15 minūtes.

6. Lai lietotu atjauninājumu, pārejiet uz LCS lapu **Vides informācija** un atlasiet **Uzturēt** > **Lietot atjauninājumus**.

    ![Vižu uzturēšana.](./media/9MaintainEnvironment.png)

7. Atjauninājumu sarakstā atlasiet izveidoto pakotni un atlasiet **Lietot**.

    ![Atjauninājumu lietošana.](./media/10ApplyUpdates.png)

   Vide apkalpošana aizņems zināmu laiku. Pēc pabeigšanas vide atgriezīsies izvietotā stāvoklī.

    ![Izvietota vide.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Duālās rakstīšanas savienojuma izveide 

1. Savā LCS projektā dodieties uz lapu **Vides informācija**.
2. Sadaļā **Common Data Service vides informācija** atlasiet **Saite uz CDS programmām**.
3. Pēc tam, kad saite ir izveidota, vēlreiz atlasiet **Saite uz CDS programmām**. Jūs tiksit novirzīts uz duālo rakstīšanu risinājumā Finance.

    ![Saite uz CDS.](./media/12LinktoCDS.png)

4. Atlasiet **Lietot risinājumu**, lai piekļūtu entītijām, kas tiks kartētas integrācijā.

    ![Risinājumu lietošana.](./media/13ApplySolutions.png)

5. Atlasiet abus risinājumus, **Dynamics 365 Finance and Operations Duālās rakstīšanas entītiju karte** un **Dynamics 365 Project Operations duālās rakstīšanas entītiju kartes**, un pēc tam atlasiet **Lietot**.

    ![Risinājumu apstiprināšana.](./media/14ConfirmSolutions.png)

    Pēc risinājumu lietošanas duālās rakstīšanas entītijas tiek lietotas videi.

    ![Risinājumu lietošana.](./media/15ApplyingSolutions.png)

    Pēc entītiju lietošanas visi pieejamie kartējumi ir uzskaitīti vidē.

    ![Duālās rakstīšanas kartējumi.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Pēc atjaunināšanas atsvaidziniet datu entītijas

1. Risinājumā Finance dodieties uz darbvietu **Datu pārvaldība**.

    ![Datu pārvaldības darbvieta.](./media/16DataManagement.png)

2. Atlasiet elementu **Struktūras parametri**.

    ![Struktūras parametri.](./media/17FrameworkParameters.png)

3. Lapā **Entītiju iestatījumi** atlasiet **Atsvaidzināt entītiju sarakstu**.

    ![Entītiju saraksta atsvaidzināšana.](./media/18RefreshEntityList.png)

Atsvaidzināšana aizņems aptuveni 20 minūtes. Kad tā būs pabeigta, saņemsit brīdinājumu.

  ![Apstiprināšanas atsvaidzināšana.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Atjauniniet drošības iestatījumus Dataverse Project Operations

1. Dodieties uz Project Operations savā Dataverse vidē. 
2. Atveriet **Iestatījumi** > **Drošība** > **Drošības lomas**. 
3. Lapā **Drošības lomas** atlasiet **duālās rakstīšanas programmas lietotājs** un atlasiet cilni **Pielāgotās entitījas**.  
4. Pārbaudiet, vai lomai ir **lasīšanas** un **pievienošanas** atļaujas šādām entītijām:
      
      - **Valūtas maiņās kursa veids**
      - **Uzņēmumu tabula**
      - **Finanšu kalendārs**
      - **Virsgrāmata**
      - **Uzņēmums**
      - **Izdevumi**

5. Pēc drošības lomas atjaunināšanas dodieties uz **Iestatījumi** > **Drošība** > **Darba grupas** un darba grupas skatā **Lokālā uzņēmuma īpašnieks** atlasiet noklusējuma darba grupu.
6. Atlasiet **Pārvaldīt lomas** un pārbaudiet, vai šai darba grupai tiek lietota drošības privilēģija **duālās rakstīšanas programmas lietotājs**.

## <a name="run-project-operations-dual-write-maps"></a>Project Operations duālās rakstīšanas kartējumu palaišana

1. Savā LCS projektā dodieties uz lapu **Vides informācija**.
2. Sadaļā **Common Data Service vides informācija** atlasiet **Saite uz CDS programmām.** Pēc saites atlasīšanas tiksit novirzīts uz entītiju sarakstu kartējumos.
3. Sāciet kartēšanu. Papildinformāciju skatiet sadaļā [Project Operations duālās rakstīšanas kartes versijas](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Pārbaudiet, vai visiem ar projektu saistītajiem kartējumiem ir statuss Darbojas.

    ![Visi kartējumi darbībā.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Konfigurācijas datu lietošana pakalpojumā CDS lietojumprogrammai Project Operations (izvēles)

Ja esat lietojis demonstrācijas datus finanšu vidē, skatiet sadaļu [Konfigurācijas datu iestatīšana un lietošana pakalpojumā Common Data Service risinājumam Project Operations](resource-apply-pro-setup-config-data.md), lai lietotu demonstrācijas datus CDS vidē.


Jūsu Project Operations vide tagad ir nodrošināta un konfigurēta. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
