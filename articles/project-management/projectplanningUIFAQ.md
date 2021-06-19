---
title: Problēmu novēršana, strādājot ar uzdevuma režģi
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kura ir nepieciešama, strādājot uzdevumu režģī.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213409"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Problēmu novēršana, strādājot ar uzdevuma režģi 

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Šajā tēmā aprakstīts, kā novērst problēmas, ar kurām, iespējams, saskarsities, strādājot ar izmaksu pārvaldību.

## <a name="enable-cookies"></a>Sīkfaili iespējoti

Project Operations ir nepieciešams, lai būtu iespējoti trešo pušu sīkfaili, lai atveidotu darba sadalījuma struktūru. Ja nav iespējoti trešo pušu sīkfaili, jūs redzēsit nevis uzdevumus, bet gan tukšu lapu, ja lapā **Projekts** atlasīsit cilni **Uzdevumi**.

![Tukša cilne, ja nav iespējoti trešo pušu sīkfaili](media/blankschedule.png)


### <a name="workaround"></a>Risinājums
Microsoft Edge vai Google Chrome pārlūkiem šīs procedūras izklāsta, kā atjaunināt pārlūka iestatījumu, lai iespējotu trešo pušu sīkfailus.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Atveriet pārlūkprogrammu Edge.
2. Augšējā labajā stūrī atlasiet **daudzpunkti** (...) un pēc tam atlasiet **Iestatījumi**.
3. Sadaļā **Sīkfaili un vietnes atļaujas** atlasiet **Sīkfaili un vietnes dati**.
4. Izslēdziet opciju **Bloķēt trešās puses sīkfailus**.

#### <a name="google-chrome"></a>Google Chrome

1. Atveriet pārlūkprogrammu Chrome.
2. Augšējā labajā stūrī atlasiet trīs vertikālus punktus un pēc tam atlasiet **Iestatījumi**.
3. Sadaļā **Privātums un drošība** atlasiet **Sīkfaili un citi vietnes dati**.
4. Atlasiet **Atļaut visus sīkfailus**.

> [!IMPORTANT]
> Ja bloķējat trešo pušu sīkfailus, tiks bloķēti visi sīkfaili un vietnes dati no citām vietnēm pat, ja vietne ir atļauta jūsu izņēmumu sarakstā.

## <a name="pex-endpoint"></a>PEX galapunkts

Project Operations vajadzībām projekta parametrs norāda uz PEX galapunktu. Šis galapunkts ir nepieciešams, lai sazinātos ar servisu, kas tiek izmantots darba sadalījuma struktūras atveidošanas nolūkam. Ja parametrs nav iespējots, saņemsit kļūdu "Projekta parametrs nav derīgs". 

### <a name="workaround"></a>Risinājums
 ![Projekta parametra lauks PEX galapunkts](media/projectparameter.png)

1. Pievienojiet **PEX galapunkta** lauku **Projekta parametru** lapai.
2. Atjauniniet lauku ar šādu vērtību: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`
3. Noņemiet lauku no **Projekta parametru** lapas.

## <a name="privileges-for-project-for-the-web"></a>Projekta atļaujas tīmeklī

Project Operations ir atkarīgs no ārēja plānošanas servisa. Šim servisam ir nepieciešams, ka lietotājam ir piešķiras vairākas lomas lasīt un rakstīt entitījās, kas saistītas ar darba sadalījuma struktūru. Šīs entitījas ietver projekta uzdevumus, resursu piešķiri un uzdevumu atkarības. Ja lietotājs nevar atveidot darba sadalījuma struktūru, dodoties uz cilni **Uzdevumi**, tas visdrīzāk ir tāpēc, ka nav iespējots Project Operations projekts. Lietotājs var saņemt vai nu drošības lomas kļūdu vai kļūdu, kas saistīta ar piekļuves liegumu.


## <a name="workaround"></a>Risinājums

1. Dodieties uz **Iestatījumi > Drošība > Lietotāji > Programmas lietotāji**.  

   ![Lietojumprogrammas lasītājs](media/applicationuser.jpg)
   
2. Veiciet dubultklikšķi uz lietojumprogrammas lietotāja ieraksta, lai pārbaudītu tālāk norādīto.

 - Lietotājam ir piekļuve projektam. Šo pārbaudi parasti veic, nodrošinot, ka lietotājam ir drošības loma **Projekta vadītājs**.
 - Microsoft Project lietojumprogrammas lietotājs pastāv un ir pareizi konfigurēts.
 
3. Ja šis lietotājs nepastāv, varat izveidot jauna lietotāja ierakstu. Atlasiet **Jauni lietotāji**. Mainiet ievades veidlapu uz **Lietojumprogrammas lietotājs** un pēc tam pievienojiet **Lietojumprogrammas ID**.

   ![Lietojumprogrammas lietotāja informācija](media/applicationuserdetails.jpg)

4. Pārbaudiet, vai lietotājam ir piešķirta pareizā licence un vai serviss ir iespējots licences servisa plānu informācijā.
5. Pārbaudiet, vai lietotājs var atvērt project.microsoft.com.
6. Ar projekta parametriem pārbaudiet, vai sistēma norāda uz pareizo projekta galapunktu.
7. Pārbaudiet, vai ir izveidots projekta lietojumprogrammas lietotājs.
8. Piemērojiet lietotājam šādas drošības lomas:

  - Dataverse lietotājs
  - Project Operations sistēma
  - Projekta sistēma

## <a name="error-when-updating-the-work-breakdown-structure"></a>Kļūda, atjauninot darba sadalījuma struktūru

Ja darba sadalījuma struktūrai tiek izdarīts viens vai vairāki atjauninājumi, izmaiņas beigās neizdodas un netiek saglabātas. Grafika režģī rodas kļūda, ziņojot ka "Jūsu veiktās pēdējās izmaiņas nevarēja saglabāt."

### <a name="workaround"></a>Risinājums

1. Pārbaudiet, vai lietotājam ir piešķirta pareizā licence un vai serviss ir iespējots licences servisa plānu informācijā.
2. Pārbaudiet, vai lietotājs var atvērt project.microsoft.com.
3. Pārbaudiet, vai sistēma norāda uz pareizo projekta galapunktu.
4. Pārbaudiet, vai ir izveidots projekta lietojumprogrammas lietotājs.
5. Piemērojiet lietotājam šādas drošības lomas:
  
  - Dataverse lietotājs vai Base lietotājs
  - Project Operations sistēma
  - Projekta sistēma
  - Project Operations duālās rakstīšanas sistēma (Šī loma ir nepieciešama, ja izvietojat Project Operations resursu/nekrājumu scenāriju.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
