---
title: Problēmu novēršana, strādājot ar uzdevuma režģi
description: Šajā rakstā ir sniegta problēmu novēršanas informācija, kas nepieciešama, strādājot uzdevumu režģī.
author: ruhercul
ms.date: 07/22/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 208ed55abf4cdf0ad2b035bd923e183ff3cae660
ms.sourcegitcommit: e91136d3335ee03db660529eccacd48907774453
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/22/2022
ms.locfileid: "9188241"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Problēmu novēršana, strādājot ar uzdevuma režģi 


_**Attiecas uz:** Project Operations resursu balstītiem / krājumu nebalstītiem scenārijiem, Lite izvietošana — darījums ar proformas rēķinu izrakstīšanu Project for the web_

Uzdevumu režģis, ko Dynamics 365 Project Operations izmanto, ir mitināts iframe iekšā Microsoft Dataverse. Šīs izmantošanas rezultātā ir jāievēro īpašas prasības, lai nodrošinātu autentifikāciju, un autorizācija darbojas pareizi. Šajā rakstā ir izklāstītas bieži sastopamās problēmas, kas var ietekmēt iespēju atveidot režģi vai pārvaldīt uzdevumus darba sadalījuma struktūrā (WBS).

Bieži sastopamās problēmas ir:

- **Uzdevumu** cilne Uzdevuma režģī ir tukša.
- Atverot projektu, netiek ielādēts projekts, un lietotāja interfeiss (UI) ir iestrēdzis skaitītājā.
- **Project for the Web** administrēšanas atļauja.
- Izmaiņas netiek saglabātas uzdevuma izveides, atjaunināšanas vai dzēšanas laikā.

## <a name="issue-the-task-tab-is-empty"></a>Problēma: Uzdevuma cilne ir tukša

### <a name="mitigation-1-enable-cookies"></a>Mazināšana 1: Iespējot sīkfailus

Project Operations pieprasa, lai trešās puses sīkfaili tiktu iespējoti, lai atveidotu darba sadalījumu struktūru. Ja trešo pušu sīkfaili nav iespējoti, tā vietā, lai skatītu uzdevumus, jūs redzēsit tukšu lapu, kad lapā Projekts atlasīsit **cilni** Uzdevumi **.**

Microsoft Edge vai Google Chrome pārlūkiem šīs procedūras izklāsta, kā atjaunināt pārlūka iestatījumu, lai iespējotu trešo pušu sīkfailus.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Atveriet pārlūkprogrammu Edge.
2. Augšējā labajā stūrī atlasiet **daudzpunkti** (...) un pēc tam atlasiet **Iestatījumi**.
3. Sadaļā **Sīkfaili un vietnes atļaujas** atlasiet **Sīkfaili un vietnes dati**.
4. Izslēdziet opciju **Bloķēt trešās puses sīkfailus**.
5. Atsvaidziniet pārlūkprogrammu. 

#### <a name="google-chrome"></a>Google Chrome

1. Atveriet pārlūkprogrammu Chrome.
2. Augšējā labajā stūrī atlasiet trīs vertikālus punktus un pēc tam atlasiet **Iestatījumi**.
3. Sadaļā **Privātums un drošība** atlasiet **Sīkfaili un citi vietnes dati**.
4. Atlasiet **Atļaut visus sīkfailus**.
5. Atsvaidziniet pārlūkprogrammu. 

> [!NOTE]
> Ja bloķējat trešo pušu sīkfailus, tiks bloķēti visi sīkfaili un vietnes dati no citām vietnēm pat, ja vietne ir atļauta jūsu izņēmumu sarakstā.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Mazināšana 2: validēt PEX galapunktu, kas ir pareizi konfigurēts

Project Operations vajadzībām projekta parametrs norāda uz PEX galapunktu. Šis galapunkts ir nepieciešams, lai sazinātos ar servisu, kas tiek izmantots, lai atveidotu darba sadalījumu struktūru. Ja parametrs nav iespējots, tiks parādīts kļūdas ziņojums "Projekta parametrs nav derīgs". Lai atjauninātu PEX galapunktu, veiciet tālāk norādītās darbības.

1. Pievienojiet **PEX galapunkta** lauku **Projekta parametru** lapai.
2. Nosakiet produkta veidu, kuru izmantojat. Šī vērtība tiek izmantota, iestatot PEX galapunktu. Izguves brīdī produkta tips jau ir definēts PEX galapunktā. Paturiet šo vērtību.
3. Atjauniniet lauku ar šādu vērtību: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Šajā tabulā ir norādīts tipa parametrs, kas ir jāizmanto, pamatojoties uz produkta tipu.

      | **Produkta tips**                     | **Parametra tips** |
      |--------------------------------------|--------------------|
      | Project for the Web noklusējuma organizācijā   | tips=0             |
      | Project for the Web CDS nosauktā organizācijā | tips=1             |
      | Project Operations                   | tips=2             |

4. Noņemiet lauku no **Projekta parametru** lapas.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>3. mazināšana: piesakieties project.microsoft.com

Pārlūkprogrammā atveriet jaunu cilni, dodieties uz project.microsoft.com un piesakieties ar lietotāja lomu, ko izmantojat, lai piekļūtu Project Operations. Ir svarīgi, lai tikai viens lietotājs pārlūkprogrammā būtu pieteicies Microsoft produktā. Kļūdas ziņojums "login.microsoftonline.com atteicās izveidot savienojumu" visbiežāk rodas, ja ir pieteikušies vairāki lietotāji, kā parādīts nākamajā attēlā.

![Izvēlieties konta pierakstīšanās lapu, kurā redzams, ka divi lietotāji ir pieteikušies.](media/MULTIPLE_USERS_LOGGED_IN.png)

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problēma: projekts netiek ielādēts, un lietotāja interfeiss ir iestrēdzis skaitītājā

Autentifikācijas vajadzībām ir jāiespējo uznirstošie logi, lai uzdevumu režģis tiktu ielādēts. Ja uznirstošie logi nav iespējoti, ekrāns iestrēgs ielādēšanas skaitītājā. Nākamajā grafikā adreses joslā ir redzams URL ar bloķētu uznirstošo elementu, kā rezultātā vērpējs iestrēgst, mēģinot ielādēt lapu. 

   ![Iestrēdzis skaitītājs un uznirstošo logu bloķētājs.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Mazināšana 1: Iespējot uznirstošos logus

Kad jūsu projekts ir iestrēdzis skaitītājā, tad, iespējams, uznirstošie logi netiks iespējoti.

#### <a name="microsoft-edge"></a>Microsoft Edge

Ir divi veidi, kā pārlūkprogrammā Edge iespējot uznirstošos logus.

1. Pārlūkprogrammā Edge atlasiet paziņojumus pārlūkprogrammas augšējā labajā stūrī.
2. Atlasiet **Vienmēr atļaut uznirstošos logus un pārvirzīšanu no** konkrētas Dataverse vides.
 
     ![Uznirstošie logi bloķēja logu.](media/enablepopups.png)

Varat arī veikt vienu no tālāk minētajām darbībām.

1. Atveriet pārlūkprogrammu Edge.
2. Augšējā labajā stūrī atlasiet **Daudzpunkti** (...), un pēc tam atlasiet **Iestatījumi** > **Vietnes atļaujas** > **Uznirstošie logi un pārvirzīšana**.
3. Pārslēdziet **Uznirstošos logus un pārvirzīšanu** uz izslēgts, lai bloķētu uznirstošos logus vai pārslēgtu uz atļauts, lai atļautu uznirstošos logus jūsu ierīcē. 
4. Pēc uznirstošo logu iespējošanas atsvaidziniet jūsu pārlūkprogrammu. 

#### <a name="google-chrome"></a>Google Chrome
1. Atveriet pārlūkprogrammu Chrome.
2. Pārejiet uz lapu, kurā tiek bloķēti uznirstošie logi.
3. Adreses joslā atlasiet **Uznirstošais logs bloķēts**.
4. Atlasiet to uznirstošo logu saiti, kuru vēlaties skatīt.
5. Pēc uznirstošo logu iespējošanas atsvaidziniet jūsu pārlūkprogrammu. 

> [!NOTE]
> Lai vienmēr skatītu šīs vietnes uznirstošos logus, atzīmējiet opciju **Vienmēr atļaut uznirstošos logus un pārvirzīšanu no [vietnes]** un pēc tam atlasiet **Gatavs**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problēma 3: Project for the Web administrēšanas atļaujas

Project Operations ir atkarīgs no ārēja plānošanas servisa. Pakalpojumam ir nepieciešams, lai lietotājam būtu piešķirtas vairākas lomas, kas ļauj viņam lasīt un rakstīt entītijām, kas saistītas ar WBS. Šīs entitījas ietver projekta uzdevumus, resursu piešķiri un uzdevumu atkarības. Ja lietotājs nevar atveidot WBS, kad viņš naviģē uz **cilni Uzdevumi**, iespējams, tas ir tāpēc **, ka nav iespējota programma Project** for **Project Operations**. Lietotājs var saņemt vai nu drošības lomas kļūdu vai kļūdu, kas saistīta ar piekļuves liegumu.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Mazināšana 1: validēt lietojumprogrammas lietotāja un lietotāja drošības lomas

1. Dodieties uz **Iestatījumi** > **Drošība** > **Lietotāji** > **Lietojumprogrammas lietotāji**.  

   ![Lietojumprogrammas lasītājs.](media/applicationuser.jpg)
   
2. Veiciet dubultklikšķi uz lietojumprogrammas lietotāja ieraksta, lai pārbaudītu:

     - Lietotājam ir piekļuve projektam. To var izdarīt, pārbaudot, vai lietotājam ir **Projekta vadītāja** drošības loma.
     - Microsoft Project lietojumprogrammas lietotājs pastāv un ir pareizi konfigurēts.
 
3. Ja šis lietotājs neeksistē, tad izveidojiet jaunu lietotāja ierakstu. 
4. Atlasiet **Jauni lietotāji**, mainiet ievades formu uz **Lietojumprogrammas lietotājs** un pēc tam pievienojiet **Lietojumprogrammas ID**.

   ![Lietojumprogrammas lietotāja informācija.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problēma 4: Izmaiņas netiek saglabātas uzdevuma izveides, atjaunināšanas vai dzēšanas laikā

Veicot vienu vai vairākus WBS atjauninājumus, izmaiņas neizdodas un netiek saglabātas. Plānošanas režģī rodas kļūda, un tiek parādīts ziņojums "Pēdējās veiktās izmaiņas nevarēja saglabāt".

### <a name="mitigation-1-validate-the-license-assignment"></a>Mazināšana 1: validēt licences piešķiršanu

1. Pārbaudiet, vai lietotājam ir piešķirta pareizā licence un vai serviss ir iespējots licences servisa plānu informācijā.  
2. Pārbaudiet, vai lietotājs var atvērt **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Mazināšana 2: projekta lietojumprogrammas lietotāja validācijas konfigurācija
1. Pārbaudiet, vai ir izveidots projekta lietojumprogrammas lietotājs.
2. Piemērojiet lietotājam šādas drošības lomas:
  
  - Dataverse lietotājs vai pamatlietotājs
  - Project Operations sistēma
  - Projekta sistēma
  - Project Operations dubultā rakstīšanas sistēma. Šī loma ir nepieciešama Project Operations resursu balstītu/krājumu nebalstītu scenāriju izvietošanai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
