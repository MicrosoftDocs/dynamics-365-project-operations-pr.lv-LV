---
title: 'Obligāto pielāgoto lauku pievienošana cenu iestatījumiem un transakciju entītijām '
description: Šajā tēmā sniegta informācija par to, kā pievienot obligātās pielāgoto lauku atsauces entitījām un veidlapām un skatiem.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a27bfe881fdb6431941fa860d279e3e7b526f623
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898315"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Obligāto pielāgoto lauku pievienošana cenu iestatījumiem un transakciju entītijām 

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Šajā tēmā tiek pieņemts, ka tēmas procedūras ir pabeigtas procedūras, kas aprakstītas tēmā [Pielāgotu lauku un entītiju izveide, ko izmantot kā cenu noteikšanas dimensijas](create-custom-fields-entities-pricing-dimensions.md). Ja šīs procedūras neesat pabeidzis, atgriezieties un pabeidziet tās, un pēc tam atgriezieties pie šīs tēmas. 

Šajā tēmā procedūras parādīs, kā pievienot vajadzīgās pielāgotās lauku atsauces entītijām un lietotāja saskarnes (UI) elementus, piemēram, veidlapas un skatus.

## <a name="add-custom-pricing-dimension-fields"></a>Pielāgotu cenas noteikšanas dimensiju lauku pievienošana 
Pēc pielāgotu lauku un entītiju izveidošanas nākamais solis ir panākt, lai cenas iestatījumi un transakciju entītijas brīdinātu par pielāgotām entītijām vai opciju kopām, izveidojot atsauču laukus. Atkarībā no tā, vai jūsu cenrāža dimensiju sarakstā ir iekļautas opciju kopas dimensijas vai entītiju dimensijas, vai arī abas, veiciet tikai tās darbības, kas ir **Uz opciju kopu pamatotas pielāgotās cenu noteiktās dimensijas** vai **Uz entītijām pamatotas pielāgotās cenu noteiktās dimensijas**, vai tās abas.

### <a name="option-set-based-custom-pricing-dimensions"></a>Uz opciju kopu pamatotas pielāgotās cenu noteiktās dimensijas
Ja ir noteikta opcija pielāgotā cenu noteikšanas dimensija, pievienojiet to kā galveno entītiju lauku. Šajā procedūrā **Resursa darba atrašanās vieta** un **Resursa darba stundas** tiek izmantotas kā opciju kopas cenas noteikšanas dimensijas. Tās vispirms ir jāpievieno kā cenu noteikšanas entītijām **Lomu cenas** un **Lomu cenas uzcenojums**.

1. Programmā Project Operations atlasiet **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**. 
2. Kreisajā navigācijas rūtī izvērsiet sadaļu **Entītijas > Lomas cenas**.
3. Izvērsiet entītiju **Lomas cenas** un atlasiet vienumu **Lauki**.
4. Atlasiet **Jauns**, lai izveidotu jaunu lauku ar nosaukumu **Resursa darba atrašanās vieta** un atlasiet vienumu **Opciju kopa** kā lauka tipu. 
5. Atlasiet **Lietot esošu opciju kopu**, atlasiet **Resursu darba atrašanās vieta** opciju kopu un pēc tam atlasiet **Saglabāt**.
6. Atkārtojiet 1.–5. darbību, lai šo lauku pievienotu entītijai **Lomu cenas uzcenojumi**. 
7. Atkārtojiet 1.–5. darbību opciju kopai **Resursu darba stundas**.

> [!IMPORTANT]
> Ja pievienojat lauku vairāk nekā vienai entītijai, izmantojiet vienu un to pašu lauka nosaukumu visās entītijās. 

Projekta pārdošanas un novērtējuma fāzēs aprēķini par darba intensitāti, kas nepieciešams, lai pabeigtu **Vietēji** un **Uz vietas** darbu, kā arī **Regulārās stundās** un **Virsstundas**, tiek izmantotas, lai novērtētu piedāvājuma/projekta vērtību. Lauku **Resursa darba atrašanās vieta** un **Resursa darba stundas** tiek pievienotas novērtēšanas entītijām, **Piedāvājumu rindu informācija**, **Līgumu rindu informācija**, **Projekta darba grupas dalībnieki**un **Novērtējuma rinda**.

1. Programmā Project Operations atlasiet **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**. 
2. Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Piedāvājuma rindu informācija**.
3. Izvērsiet entītiju **Piedāvājuma rindas** un atlasiet **Lauki**.
4. Atlasiet **Jauns**, lai izveidotu jaunu lauku ar nosaukumu **Resursa darba atrašanās vieta** un atlasiet lauka veidu **Opciju kopa**. 
5. Atlasiet **Izmantot esošu opciju kopu** un **Resursa darba atrašanās vieta** un pēc tam atlasiet **Saglabāt**.
6. Atkārtojiet 1.–5. darbību, lai pievienotu šo lauku **Projekta līguma rindu informācija**, **Projekta darba grupas dalībnieks** un **Novērtējuma rinda** entītijām.
7. Atkārtojiet 1.–6. darbību opciju kopai **Resursa darba stundas**. 

Piegādei un rēķinu izrakstīšanai pabeigtajam darbam ir precīzi jārēķinās, vai tas ir veikts **Vietēji** vai **Uz vietas**, kā arī to, vai tas ir pabeigts projekta faktiskajās **Regulārās stundas** laikā vai **Virsstundas**. **Resursa darba atrašanās vieta** un **Resursa darba stundas** lauki jāpievieno entītijām **Laika ievade**, **Faktiski**, **Rēķina rindas informācija**un **Žurnāla rinda**.

1. Atlasiet **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**.
2. Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Laika ievade**.
3. Izvērsiet **Piedāvājuma rindas informācija** un atlasiet**Lauki**.
4. Atlasiet **Jauns**, lai izveidotu jaunu lauku ar nosaukumu **Resursa darba atrašanās vieta** un atlasiet vienumu **Opciju kopa** kā lauka tipu. 
5. Atlasiet **Lietot esošu opciju kopu**, atlasiet **Resursu darba atrašanās vieta** opciju kopu un pēc tam atlasiet **Saglabāt**.
6. Atkārtojiet 1.–5. darbību, lai o lauku pievienotu **Faktiski**, **Rēķina rindu informācija**un **Žurnāla rinda** entītijām.
7. Atkārtojiet 1.–6. darbību opciju kopai **Resursa darba stundas**. 

Šādi tiek pabeigtas shēmas izmaiņas, kas nepieciešamas opciju kopas pielāgotām dimensijām.

## <a name="entity-based-custom-pricing-dimensions"></a>Uz entītijām pamatotas opciju kopas pielāgotas cenu noteikšana

Ja pielāgotā cenu noteikšanas dimensija ir entītija, jūs pievienosit 1: N attiecības starp dimensiju entītiju un galvenajām entītijām. Izmantojot iepriekš aprakstīto standarta nosaukuma piemēru, ir saprātīgi gaidīt, ka katram darbiniekam ir piešķirts standarta nosaukums. SAs rezultātā ir nepieciešama 1: N attiecība no Standarta nosaukuma līdz Rezervētajam resursam vai N:1 attiecības, ja tas ir izveidots no Rezervētā resursa uz Standarta nosaukumu.

1. Programmā Project Operations atlasiet **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> cenu noteikšanas dimensijas**. 
2. Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Standarta nosaukums**.
3. Izvērsiet **Standarta nosaukums** entītiju un atlasiet **1: N attiecības**.
4. Atlasiet **Jauns**, lai veidotu jaunu 1:N attiecību, ko sauc **Standarta nosaukums rezervējamam resursam**. Ievadiet nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.

Standarta nosaukums būs jāpievieno arī cenu noteikšanas entītijām **Lomas cena** un **Lomas cenas uzcenojums.** Tas tiek pabeigts arī, izmantojot 1:N attiecības starp **Standarta nosaukums** un **Lomas cena** entītijām, kā arī **Standarta nosaukums** un **Lomas cenas uzcenojums**.

1. Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Standarta nosaukums**.
2. Izvērsiet **Standarta nosaukums** entītiju un atlasiet **1: N attiecības**.
3. Atlasiet **Jauns**, lai izveidotu jaunu 1:N attiecību, ko sauc par **Standarta nosaukums rezervētajam resursam**. Ievadiet nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**.
4. Atkārtojiet 1.–4. darbību, lai izveidotu 1: N attiecību starp **Standarta nosaukums** un **Lomu cenas uzcenojums** entītijām,

Projekta pārdošanas un novērtēšanas fāzēs cenas piedāvājumam/projektam ir nepieciešami darba intensitātes aprēķini katram standarta nosaukumam. Tas nozīmē, ka 1:N attiecības no Standarta nosaukuma līdz katrai no šīm novērtēšanas entītijām ir nepieciešamas: 

- **Piedāvājuma rindas informācija**
- **Projekta līguma rindas informācija**
- **Projekta grupas dalībnieks**
- **Novērtējuma rinda**

5. Atkārtojiet 1.–5. darbību, lai izveidotu 1: N attiecības no **Standarta nosaukums** uz **Piedāvājuma rindas informācija**, **Projekta līguma rindas informācija**, **Projekta darba grupas dalībnieks** un **Novērtētā rinda**.

  Piegādes un rēķinu izrakstīšanas fāzēs darbam, kas pabeigts pēc katra standarta nosaukuma, ir precīzi jāatbilst projekta faktiskajām cenām. Tas nozīmē, ka ir jābūt 1: N attiecībām no **Standarta virsraksts** uz **Laika ievade**, **Faktiskie**, **Rēķina rindas informācija** un **Žurnāla rindas entītijas**.

6. Atkārtojiet 1.–6. darbību, lai izveidotu 1: N attiecības no **Standarta virsraksts** uz **Laika ievade**, **Faktiskie**, **Rēķina rindas informācija** un **Žurnāla rindas entītijas**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Dimensiju vērtību noklusējuma iestatīšana, izmantojot platformas kartēšanas līdzekļus
Laika ievadei būtu noderīgi, ja sistēmas būtu noklusējuma standarta ieraksts laika ievadē no rezervējamā resursa, kas reģistrē laika ierakstu. Veiciet šīs darbības, lai pievienotu lauka kartējumus 1:N attiecībā no **Rezervējams resurss** uz **Laika ievade**.

1. Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Standarta nosaukums**.
2. Izvērsiet **Standarta nosaukums** entītiju un atlasiet **1: N attiecības**.
3. Veiciet dubultklikšķi uz **Rezervējams resurss uz Laika ievade**. Lapā **Attiecības** atlasiet **Izmantot lauku kartējumus.** 
4. Atlasiet **Jauns**, lai izveidotu jaunu lauka kartēšanu starp lauku **Standarta nosaukums** entītijā **Rezervējams resurss** atsauces laukā **Standarta nosaukums** lauka entītijā **Laika ievade**. 

Šādi tiek pabeigtas shēmas izmaiņas, kas nepieciešamas uz entītijām pamatotām pielāgotām dimensijām.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Pielāgoto lauku pievienošana veidlapām, skatiem un biznesa noteikumiem

Kad esat veicis visas nepieciešamās shēmas izmaiņas, nākamā darbība ir padarīt laukus redzamus lietotāja saskarnē, pievienojot laukus veidlapām un skatiem.

1. Atveriet veidlapu vai skatu. Labajā navigācijas rūtī atlasiet lauku un velciet to uz veidlapu kanvu. 
2. Ja rediģējat skatu, izmantojiet navigācijas rūti, atlasiet **Pievienot laukus** un dialoglodziņā **Lauku saraksts** atlasiet vajadzīgos laukus un atlasiet **Labi**.

Tālāk sniegtajā tabulā ir sniegts visaptverošs formātu un skatu saraksts pa entītijām, kas būs jāatjaunina ar jaunajiem laukiem. Ja šajās entītijās pielāgojumos ir papildu skati vai veidlapas, pievienojiet arī jaunus laukus.

| Elements        | Veidlapas, kurām ir vajadzīgs jauns lauks   |Skati, kuriem ir vajadzīgs jauns lauks      |
| ------------------------------|---------------------------------|----------------------------------|
|  Lomas cena|• Informācija |• Aktīvu resursu kategoriju cenas<br> • Ar resursu kategorijas cenu saistītais skats|
|  Lomas cenas uzcenojums|• Informācija|• Aktīvais lomas cenas uzcenojums<br>• Ar lomas cenas uzcenojumu saistītais skats|
|  Piedāvājuma rindas informācija|• Projekta informācija<br>• Projekta ātrā izveidošana|• Aktīva piedāvājuma rindas papildinformācija<br>Apvienota piedāvājuma rindas papildinformācija<br>Piedāvājuma rindas papildinformācijas saistītais skats|
|  Projekta līguma rindas papildinformācija|• Projekta informācija<br>• Projekta ātrā izveidošana|• Līguma rindas apvienotā informācija<br>Aktīvās līguma rindas papildinformācija<br>• Līguma rindu informācijas saistītais skats|
|  Projekta grupas dalībnieks|• Informācija<br>• Jauna veidlapa|• Aktīvie projekta darba grupas dalībnieki<br>• Projekta darba grupas dalībnieki<br>• Projekta grupas dalībnieku saistītais skats|
|  Laika ieraksts|• Informācija<br>• Laika ieraksta izveide|• Mani laika ieraksti pēc datuma<br>• Mani laika ieraksti šajā nedēļā<br>• Laika ieraksti apstiprināšanai|
|  Žurnāla rinda|• Informācija<br>• Ātrā izveide|• Aktīvās žurnāla rindas<br>• Žurnāla rindas saistītais skats|
|  Rēķina rindas informācija|• Informācija<br>• Ātrā izveide|• Aktīva rēķina rindas papildinformācija<br>• Rēķinā iekļaujamas darbības<br>• Papildu rēķina darbības<br>• Rēķina rindas papildinformācijas saistītais skats<br>• Rēķinā neiekļaujamas darbības|
|  Faktiski|• Informācija<br>• Aktīvās faktiskās vērtības|• Faktiskais saistītais skats|

Atkarībā no tā, ko esat definējis, biznesa noteikumiem, iespējams, būs jāpievieno arī pielāgoti lauki. Viens nepieejams piemērs ir biznesa noteikumam **Laika ievades rediģēšana, pamatojoties uz statusu**. Šī kārtula definē, kuri lauki ir jābloķē, ja laika ievade atrodas nerediģējamā statusā, piemēram, **Apstiprināta**. Pievienojiet laukus šai biznesa kārtulai tā, lai lauki tiktu bloķēti rediģēšanai, ja laika ievades statuss nav **Melnraksts** vai **Atgriezts**.
