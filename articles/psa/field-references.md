---
title: Pielāgoti lauki cenas iestatījumam un transakciju entītijām
description: Šajā tēmā ir sniegta informācija par pielāgotu lauku pievienošanu cenas iestatījumam un transakciju entītijām.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3ca48b8d5d55b1b2178f9bd84e19d9599f057aa296a728cca57577c18fdaf307
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985780"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a>Pielāgoti lauki cenas iestatījumam un transakciju entītijām 

[!include [banner](../includes/psa-now-project-operations.md)]

Šajā tēmā tiek pieņemts, ka tēmas procedūras ir pabeigtas, [Pielāgotu lauku un entītiju izveide](create-custom-fields-entities.md). Ja šīs procedūras neesat pabeidzis, atgriezieties un pabeidziet tās, un pēc tam atgriezieties pie šīs tēmas. 

Šajā tēmā procedūras parādīs, kā pievienot vajadzīgās pielāgotās lauku atsauces entītijām un lietotāja saskarnes (UI) elementus, piemēram, veidlapas un skatus.

## <a name="add-custom-pricing-dimension-fields"></a>Pielāgotu cenas noteikšanas dimensiju lauku pievienošana 
Pēc pielāgotu lauku un entītiju izveidošanas nākamais solis ir panākt, lai cenas iestatījumi un transakciju entītijas brīdinātu par pielāgotām entītijām vai opciju kopām, izveidojot atsauču laukus. Atkarībā no tā, vai jūsu cenrāža dimensiju sarakstā ir iekļautas opciju kopas dimensijas vai entītiju dimensijas, vai arī abas, veiciet tikai tās darbības, kas ir **Uz opciju kopu pamatotas pielāgotās cenu noteiktās dimensijas** vai **Uz entītijām pamatotas pielāgotās cenu noteiktās dimensijas**, vai tās abas.

### <a name="option-set-based-custom-pricing-dimensions"></a>Uz opciju kopu pamatotas pielāgotās cenu noteiktās dimensijas
Ja ir noteikta opcija pielāgotā cenu noteikšanas dimensija, pievienojiet to kā galveno Project Service entītiju lauku. Šajā procedūrā **Resursa darba atrašanās vieta** un **Resursa darba stundas** tiek izmantotas kā opciju kopas cenas noteikšanas dimensijas. Tās vispirms ir jāpievieno kā cenu noteikšanas entītijām **Lomu cenas** un **Lomu cenas uzcenojums**.

1. Platformā Project Service Automation (PSA) noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**. 
2. Kreisajā navigācijas rūtī izvērsiet sadaļu **Entītijas > Lomas cenas**.
3. Izvērsiet entītiju **Lomas cenas** un atlasiet vienumu **Lauki**.
4. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu lauku ar nosaukumu **Resursa darba atrašanās vieta** un atlasiet vienumu **Opciju kopa** kā lauka tipu. 
5. Atlasiet **Lietot esošu opciju kopu**, atlasiet **Resursu darba atrašanās vieta** opciju kopu un pēc tam noklikšķiniet uz **Saglabāt**.
6. Atkārtojiet 1.–5. darbību, lai šo lauku pievienotu entītijai **Lomu cenas uzcenojumi**. 
7. Atkārtojiet 1.–5. darbību opciju kopai **Resursu darba stundas**.

> [!IMPORTANT]
> Ja pievienojat lauku vairāk nekā vienai entītijai, izmantojiet vienu un to pašu lauka nosaukumu visās entītijās. 

> ![Resursu darba atrašanās vietas pievienošana lomas cenai.](media/RWL-Field.png)

Projekta pārdošanas un novērtējuma fāzēs aprēķini par darba intensitāti, kas nepieciešams, lai pabeigtu **Vietēji** un **Uz vietas** darbu, kā arī **Regulārās stundās** un **Virsstundas**, tiek izmantotas, lai novērtētu piedāvājuma/projekta vērtību. Lauki **Resursa darba atrašanās vieta** un **Resursa darba stundas** tiek pievienoti novērtēšanas entītijām **Piedāvājumu rindu informācija**, **Līgumu rindu informācija**, **Projekta uzdevums**, **Projekta darba grupas dalībnieks** un **Novērtējuma rinda**.

1. Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**. 
2. Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Piedāvājuma rindu informācija**.
3. Izvērsiet entītiju **Piedāvājuma rindas** un atlasiet **Lauki**.
4. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu lauku ar nosaukumu **Resursa darba atrašanās vieta** un atlasiet **Opciju kopa** kā lauka tipu. 
5. Atlasiet **Izmantot esošu opciju kopu** un **Resursa darba atrašanās vieta** un pēc tam noklikšķiniet uz **Saglabāt**.
6. Atkārtojiet 1.–5. darbību, lai pievienotu šo lauku entītijām **Projekta līguma rindas informācija**, **Projekta uzdevums**, **Projekta darba grupas dalībnieks** un **Novērtējuma rinda**.
7. Atkārtojiet 1.–6. darbību opciju kopai **Resursa darba stundas**. 

> ![Resursu darba atrašanās vietas pievienošana Novērtējuma rindai.](media/RWL-Default-Value.png)


Piegādei un rēķinu izrakstīšanai pabeigtajam darbam ir precīzi jārēķinās, vai tas ir veikts **Vietēji** vai **Uz vietas**, kā arī to, vai tas ir pabeigts projekta faktiskajās **Regulārās stundas** laikā vai **Virsstundas**. **Resursa darba atrašanās vieta** un **Resursa darba stundas** lauki jāpievieno entītijām **Laika ievade**, **Faktiski**, **Rēķina rindas informācija** un **Žurnāla rinda**.

1. Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**.
2. Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Laika ievade**.
3. Izvērsiet **Piedāvājuma rindas informācija** un atlasiet **Lauki**.
4. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu lauku ar nosaukumu **Resursa darba atrašanās vieta** un atlasiet vienumu **Opciju kopa** kā lauka tipu. 
5. Atlasiet **Lietot esošu opciju kopu**, atlasiet **Resursu darba atrašanās vieta** opciju kopu un pēc tam noklikšķiniet uz **Saglabāt**.
6. Atkārtojiet 1.–5. darbību, lai o lauku pievienotu **Faktiski**, **Rēķina rindu informācija** un **Žurnāla rinda** entītijām.
7. Atkārtojiet 1.–6. darbību opciju kopai **Resursa darba stundas**. 

> ![Resursu darba atrašanās vietas pievienošana Laika ievadei.](media/RWL-time-entry.png)

Šādi tiek pabeigtas shēmas izmaiņas, kas nepieciešamas opciju kopas pielāgotām dimensijām.

## <a name="entity-based-custom-pricing-dimensions"></a>Uz entītijām pamatotas opciju kopas pielāgotas cenu noteikšana

Ja pielāgotā cenu noteikšanas dimensija ir entītija, jūs pievienosit 1: N attiecības starp dimensiju entītiju un galvenajām Project Service entītijām. Izmantojot iepriekš aprakstīto standarta nosaukuma piemēru, ir saprātīgi gaidīt, ka katram darbiniekam ir piešķirts standarta nosaukums. SAs rezultātā ir nepieciešama 1: N attiecība no Standarta nosaukuma līdz Rezervētajam resursam vai N:1 attiecības, ja tas ir izveidots no Rezervētā resursa uz Standarta nosaukumu.

1. Platformā PSA noklikšķiniet uz **Iestatījumi** > **Risinājumi** un pēc tam veiciet dubultklikšķi uz **\<your organization name> izcenojuma dimensijas**. 
2. Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Standarta nosaukums**.
3. Izvērsiet **Standarta nosaukums** entītiju un atlasiet **1: N attiecības**.
4. Noklikšķiniet uz **Jauns**, lai veidotu jaunu 1:N attiecību, ko sauc **Standarta nosaukums rezervējamam resursam**. Ievadiet pieprasīto informāciju un pēc tam noklikšķiniet uz vienuma **Saglabāt**.

> ![Standarta nosaukuma kā atsauces lauka pievienošana Rezervējamam resursam.](media/ST-BR.png)

Standarta nosaukums būs jāpievieno arī Project Service cenu noteikšanas entītijām **Lomas cena** un **Lomas cenas uzcenojums.** Tas tiek pabeigts arī, izmantojot 1:N attiecības starp **Standarta nosaukums** un **Lomas cena** entītijām, kā arī **Standarta nosaukums** un **Lomas cenas uzcenojums**.

1. Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Standarta nosaukums**.
2. Izvērsiet **Standarta nosaukums** entītiju un atlasiet **1: N attiecības**.
3. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu 1:N attiecību, ko sauc par **Standarta nosaukums rezervētajam resursam**. Ievadiet pieprasīto informāciju un pēc tam noklikšķiniet uz vienuma **Saglabāt**.
4. Atkārtojiet 1.–4. darbību, lai izveidotu 1: N attiecību starp **Standarta nosaukums** un **Lomu cenas uzcenojums** entītijām,

Projekta pārdošanas un novērtēšanas fāzēs cenas piedāvājumam/projektam ir nepieciešami darba intensitātes aprēķini katram standarta nosaukumam. Tas nozīmē, ka 1:N attiecības no Standarta nosaukums līdz katrai no šīm novērtēšanas entītijām pakalpojumā Project Service ir nepieciešamas: 

- **Piedāvājuma rindas informācija**
- **Projekta līguma rindas informācija**
- **Projekta uzdevums**
- **Projekta grupas dalībnieks**
- **Novērtēšanas rinda**

5. Atkārtojiet 1.–5. darbību, lai izveidotu 1:N attiecības no **Standarta nosaukums** uz **Piedāvājuma rindas informācija**, **Projekta līguma rindas informācija**, **Projekta uzdevums**, **Projekta darba grupas dalībnieks** un **Novērtētā rinda**.

> ![Standarta nosaukuma kā atsauces lauka pievienošana Novērtējuma rindai.](media/ST-Estimate-Line.png)

Piegādes un rēķinu izrakstīšanas fāzēs darbam, kas pabeigts pēc katra standarta nosaukuma, ir precīzi jāatbilst projekta faktiskajām cenām. Tas nozīmē, ka ir jābūt 1: N attiecībām no **Standarta virsraksts** uz **Laika ievade**, **Faktiskie**, **Rēķina rindas informācija** un **Žurnāla rindas entītijas**.

6. Atkārtojiet 1.–6. darbību, lai izveidotu 1: N attiecības no **Standarta virsraksts** uz **Laika ievade**, **Faktiskie**, **Rēķina rindas informācija** un **Žurnāla rindas entītijas**.

> ![Standarta nosaukuma kā atsauces lauka pievienošana Laika ievadei.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Dimensiju vērtību noklusējuma iestatīšana, izmantojot platformas kartēšanas līdzekļus
Laika ievadei būtu noderīgi, ja sistēmas būtu noklusējuma standarta ieraksts laika ievadē no rezervējamā resursa, kas reģistrē laika ierakstu. Veiciet šīs darbības, lai pievienotu lauka kartējumus 1:N attiecībā no **Rezervējams resurss** uz **Laika ievade**.

1. Risinājuma pārlūkā kreisajā navigācijas rūtī atlasiet **Entītijas > Standarta nosaukums**.
2. Izvērsiet **Standarta nosaukums** entītiju un atlasiet **1: N attiecības**.
3. Veiciet dubultklikšķi uz **Rezervējams resurss uz Laika ievade**. Lapā **Attiecības** noklikšķiniet uz **Izmantot lauku kartējumus.** 
4. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu lauka kartēšanu starp lauku **Standarta nosaukums** entītijā **Rezervējams resurss** atsauces laukā **Standarta nosaukums** lauka entītijā **Laika ievade**. 

> ![Iestatīšanas lauka kartēšana, lai atļautu Standarta nosaukuma noklusējumu no Rezervējams resurss līdz Laika ievade.](media/ST-Mapping2.png)


Šādi tiek pabeigtas shēmas izmaiņas, kas nepieciešamas uz entītijām pamatotām pielāgotām dimensijām.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Pielāgoto lauku pievienošana veidlapām, skatiem un biznesa noteikumiem

Kad esat veicis visas nepieciešamās shēmas izmaiņas, nākamā darbība ir padarīt laukus redzamus lietotāja saskarnē, pievienojot laukus veidlapām un skatiem.

1. Atveriet veidlapu vai skatu. Labajā navigācijas rūtī atlasiet lauku un velciet to uz veidlapu kanvu. 
2. Ja rediģējat skatu, izmantojiet navigācijas rūti, noklikšķiniet uz **Pievienot laukus** un dialoglodziņā **Lauku saraksts** atlasiet vajadzīgos laukus un noklikšķiniet uz **Labi**.

Tālāk sniegtajā tabulā ir sniegts visaptverošs formātu un skatu saraksts pa entītijām, kas būs jāatjaunina ar jaunajiem laukiem. Ja šajās entītijās pielāgojumos ir papildu skati vai veidlapas, pievienojiet arī jaunus laukus.

| Project Service entītijas        | Veidlapas, kurām ir vajadzīgs jauns lauks   |Skati, kuriem ir vajadzīgs jauns lauks      |
| ------------------------------|---------------------------------|----------------------------------|
|  Lomas cena|• Informācija |• Aktīvu resursu kategoriju cenas<br> • Ar resursu kategorijas cenu saistītais skats|
|  Lomas cenas uzcenojums|• Informācija|• Aktīvais lomas cenas uzcenojums<br>• Ar lomas cenas uzcenojumu saistītais skats|
|  Piedāvājuma rindas informācija|• Projekta informācija<br>• Projekta ātrā izveidošana|• Aktīva piedāvājuma rindas papildinformācija<br>Apvienota piedāvājuma rindas papildinformācija<br>Piedāvājuma rindas papildinformācijas saistītais skats|
|  Projekta līguma rindas papildinformācija|• Projekta informācija<br>• Projekta ātrā izveidošana|• Līguma rindas apvienotā informācija<br>Aktīvās līguma rindas papildinformācija<br>• Līguma rindu informācijas saistītais skats|
|  Projekta uzdevums|• Informācija<br>• Jauna veidlapa||
|  Projekta grupas dalībnieks|• Informācija<br>• Jauna veidlapa|• Aktīvie projekta darba grupas dalībnieki<br>• Projekta darba grupas dalībnieki<br>• Projekta grupas dalībnieku saistītais skats|
|  Laika ieraksts|• Informācija<br>• Laika ieraksta izveide|• Mani laika ieraksti pēc datuma<br>• Mani laika ieraksti šajā nedēļā<br>• Laika ieraksti apstiprināšanai|
|  Žurnāla rinda|• Informācija<br>• Ātrā izveide|• Aktīvās žurnāla rindas<br>• Žurnāla rindas saistītais skats|
|  Rēķina rindas informācija|• Informācija<br>• Ātrā izveide|• Aktīva rēķina rindas papildinformācija<br>• Rēķinā iekļaujamas darbības<br>• Papildu rēķina darbības<br>• Rēķina rindas papildinformācijas saistītais skats<br>• Rēķinā neiekļaujamas darbības|
|  Faktiski|• Informācija<br>• Aktīvās faktiskās vērtības|• Faktiskais saistītais skats|

Atkarībā no tā, ko esat definējis, biznesa noteikumiem, iespējams, būs jāpievieno arī pielāgoti lauki. Viens nepieejams piemērs ir biznesa noteikumam **Laika ievades rediģēšana, pamatojoties uz statusu**. Šī kārtula definē, kuri lauki ir jābloķē, ja laika ievade atrodas nerediģējamā statusā, piemēram, **Apstiprināta**. Pievienojiet laukus šai biznesa kārtulai tā, lai lauki tiktu bloķēti rediģēšanai, ja laika ievades statuss nav **Melnraksts** vai **Atgriezts**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]