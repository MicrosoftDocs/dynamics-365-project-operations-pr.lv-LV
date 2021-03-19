---
title: Piedāvājumi — pamata koncepti
description: Šajā tēmā sniegta informācija par projektu piedāvājumiem un pārdošanas piedāvājumiem, kas pieejami Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 899279b33f4fe8780d110d7c18a097407bd8d839
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277527"
---
# <a name="quotes---key-concepts"></a>Piedāvājumi — pamata koncepti

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Programmā Dynamics 365 Project Operations ir divu tipu piedāvājumi — projekta piedāvājumi un pārdošanas piedāvājumi. Abi piedāvājumu veidi atšķiras šādi:

- **Rindas elementu režģi**: Pārdošanas piedāvājumā rindas elementiem ir tikai viens režģis. Projekta piedāvājumā rindas elementiem ir divi režģi. Viens režģis ir projekta rindām, bet otrs — produktu rindām.
- **Aktivizēšana un pārskatīšana**: Pārdošanas piedāvājumu atbalsta aktivizēšana un pārskatīšana. Šie procesi netiek atbalstīt projekta piedāvājumā.
- **Pievienotie pasūtījumi**: Pārdošanas piedāvājumam varat pievienot vairākus pasūtījumus. Projekta piedāvājumam var pievienot tikai vienu projekta līgumu.
- **Piedāvājuma iegūšana**: Iegūstot pārdošanas piedāvājumu, saistīta iespēja var palikt atvērta. Pēc tam, kad projekta piedāvājums ir iegūts, saistītā iespēja tiek slēgta.
- **Lauki un koncepti**: Pārdošanas piedāvājumā nav iekļauti daži lauki un koncepcijas, kas ir iekļautas projekta piedāvājumā. Šie lauki ir, piemēram, **Līgumslēdzēja struktūrvienība**, **Uzņēmumu pārvaldnieks** un **Rēķina saņēmēja kontaktpersonas vārds**.  
- **Veids**: Pārdošanas piedāvājumus un projekta piedāvājumus norāda arī pēc opciju kopā balstīta lauka **Veids**. Pārdošanas piedāvājumā šim laukam ir vērtība **Balstīts uz elementu**. Projekta piedāvājumā tam ir vērtība **Balstīts uz darbu**.

Šajā tēmā galvenā uzmanība tiks pievērsta detalizētai informācijai par projekta piedāvājumiem.

Projekta piedāvājumam Project Operations var būt vairāki rindas elementi vai piedāvājuma rindas. Projekta piedāvājumā ir divi režģi rindas elementiem. Viens režģis ir paredzēts uz projektu balstītām rindām, kas nodrošina detalizētus novērtējumus. Otrs režģis ir paredzēts uz preci balstītām rindām, kas izmanto vienkāršu vienības cenas un uz daudzumu balstītu metodi.

- **Balstīts uz projektu**: Piedāvātā vērtība tiek noteikta pēc tam, kad ir novērtēts, cik daudz darba ir nepieciešams. Izmantojot projektu un projekta plānu, varat aprēķināt darbu augstā līmenī, tieši kā rindas informāciju zem katras piedāvājuma rindas vai, pamatojoties uz sākotnējiem aprēķiniem, izmantojot projektu un projekta plānu. Uz projektu balstītas piedāvājuma rindas ir atrodamas tikai uz projektu balstītos piedāvājumos, kas izveidoti, izmantojot Project Operations. Šī tipa piedāvājuma rinda ir pielāgota programmā Microsoft Dynamics 365 Sales pieejamo ierakstāmo piedāvājuma rindu forma.

- **Balstīts uz preci**: Piedāvātā vērtība tiek noteikta, pamatojoties uz pārdoto vienību daudzumu un vienības pārdošanas cenu. Prece uz preci balstītā rindā var būt iegūta no Sales preču kataloga vai arī tā var būt jūsu definētā prece. Šī tipa piedāvājuma rinda ir pieejama arī uz projektu balstītos piedāvājumos, kas izveidoti, izmantojot Project Operations.

Piedāvājumā ietvertā summa ir uz preci balstīto rindu un uz projektu balstīto rindu kopsumma.

> [!NOTE]
> Piedāvājumi un piedāvājuma rindas programmā Project Operations nav obligātas. Projekta procesu var sākt ar projekta līgumu (pārdotais projekts). Tomēr vienmēr ir nepieciešama iespēja neatkarīgi no tā, vai sākat darbu ar piedāvājumu vai projekta līgumu.

## <a name="project-based-quote-lines"></a>Projekta piedāvājuma rindas

Uz projektu balstītai piedāvājuma rindai programmā Project Operations ir tālāk norādītās norēķinu metodes.

- Laiks un materiāli
- Fiksētas cenas

### <a name="time-and-material"></a>Laika un materiālu

Laika un materiālu norēķinu metodes pamatā ir patēriņš. Kad atlasāt šo norēķinu metodi, klientam tiek izrakstīts rēķins par projekta izmaksām. Rēķini tiek izveidoti periodiski, pamatojoties uz datumu. Pārdošanas procesa laikā laika un materiālu komponenta piedāvātā vērtība klientam sniedz tikai galīgo izmaksu novērtējumu. Kreditors neuzņemas saistības izpildīt projektu precīzi atbilstoši piedāvātajai vērtībai. Laika un materiālu komponenti palielina klienta risku. Klienti, iespējams, vēlēsies apspiest papildu klauzulas par nepārsniegšanu, lai samazinātu to risku. Project Operations neatbalsta klauzulu par nepārsniegšanu iestatīšanu.

### <a name="fixed-price"></a>Fiksētas cenas

Izmantojot fiksētas cenas norēķinu metodi, kreditors apņemas nodrošināt projektu klientam par fiksētu samaksu. Klientam tiek izrakstīts rēķins par fiksētas cenas piedāvājuma rindas piedāvāto vērtību neatkarīgi no izmaksām, kas kreditoram rodas, nodrošinot šo piedāvājuma rindu. Rēķins par fiksētas cenas piedāvājuma rindas vērtību tiek izrakstīts vienā no tālāk norādītajiem veidiem. 

- Kā vienreizējās izmaksas summa projekta sākumā vai beigās vai tad, kad ir sasniegts projekta atskaites punkts. 
- No datuma atkarīgos intervālos, veicot vienlīdzīgus piedāvājuma rindas fiksētās vērtības maksājumus. Šie maksājumi ir pazīstami kā periodiskie atskaites punkti.
- Maksājumi, kam ir naudas vērtība, tiek saskaņoti ar darba norisi vai konkrētiem projektā sasniegtiem atskaites punktiem. Šajā gadījumā katra maksājuma vērtība var atšķirties, bet tiem kopā ir jāveido piedāvājuma rindas fiksētā vērtība.

Project Operations atbalsta visus trīs rēķinu grafiku tipus fiksētas cenas piedāvājuma rindām.

## <a name="transaction-classification"></a>Transakciju klasifikācija

Profesionālo pakalpojumu organizācijas parasti sniedz piedāvājumus un izraksta rēķinus saviem klientiem, izmantojot izmaksu klasifikāciju. Izmaksas tiek apzīmētas ar tālāk norādītajām transakciju klasifikācijām.

- **Laiks**: Šī klasifikācija norāda darba vai cilvēkresursu laika izmaksas projektā.
- **Izdevumi**: Šī klasifikācija norāda visus pārējos izdevumus projektā. Tā kā izdevumus var plaši klasificēt, lielākā daļā organizāciju izveido apakškategorijas, piemēram, ceļojumi, automašīnu īre, viesnīca vai biroja preces.
- **Maksa**: Šī klasifikācija norāda dažādas pieskaitāmās izmaksas, soda naudas un citas no klienta iekasējamās maksas. 
- **Nodoklis**: Šī klasifikācija norāda nodokļu summas, ko lietotāji pievieno, ievadot izdevumus.
- **Materiālu transakcija**: Šī klasifikācija norāda faktiskās vērtības no preču rindām apstiprinātā projekta rēķinā.
- **Atskaites punkts**: Šo klasifikāciju izmanto fiksētas cenas norēķinu loģika.

Vienu vai vairākas no šīm transakciju klasifikācijām var saistīt ar katru piedāvājuma rindu. Pēc tam, kad piedāvājums ir iegūts, kartējums starp transakciju klasifikāciju un piedāvājuma rindu tiek pārsūtīts uz līguma rindu.
  
Piedāvājumā var būt ietvertas, piemēram, tālāk norādītās divas piedāvājuma rindas. 

- Konsultāciju darbs, kas izmanto laika un materiālu norēķinu metodi, kurā ir piemērojamas laika un maksu transakciju klasifikācijas. Piemēram, par visām projekta parauga **Dynamics AX ieviešana** laika un maksu transakcijām rēķins klientam tiek izrakstīts, pamatojoties uz patērēto laiku un materiāliem. 
- Saistītie ceļa izdevumi, kas izmanto fiksētu cenas norēķinu metodi. Piemēram, par visiem projekta parauga **Dynamics AX ieviešana** ceļa izdevumiem rēķins tiek izrakstīts, izmantojot fiksētu naudas vērtību.

> [!NOTE]
> Projekta un transakciju klasifikāciju **Laiks**, **Izdevumi** un **Maksa** kombinācijai, kas saistīta ar piedāvājuma rindu vai līguma rindu, ir jābūt unikālai. Ja viena un tā pati projekta un transakciju klases kombinācija būs saistīta ar vairāk nekā vienu līguma rindu vai piedāvājuma rindu, Project Operations nedarbosies pareizi.

## <a name="billing-types"></a>Norēķinu tipi

Lauks **Norēķinu tips** definē rēķinā iekļaujamības koncepciju. Tas ir opciju kopa ar tālāk norādītajām iespējamajām vērtībām.

- **Rēķinā iekļaujams**: Izmaksas, kas tiek uzkrātas, izmantojot šo lomu/kategoriju, ir tiešās izmaksas, kas virza projekta izpildi, un klientam ir jāmaksā par šo darbu. Maksājumu var administrēt kā laika un materiālu vai fiksētas cenas apmaksu. Tomēr darbinieks, kas veltīs šo laiku, saņems atbilstošo kredītu par savu apmaksājamo izmantošanu.
- **Rēķinā iekļaujams**: Izmaksas, kas tiek uzkrātas, izmantojot šo lomu/kategoriju, ir tiešās izmaksas, kas virza projekta izpildi, lai gan klients šo faktu neatzīst un nevēlas maksāt par šo darbu. Darbinieks, kas veltīs šo laiku, nesaņems atbilstošo kredītu par savu apmaksājamo izmantošanu.
- **Bezmaksas**: Izmaksas, kas tiek uzkrātas, izmantojot šo lomu/kategoriju, ir tiešās izmaksas, kas virza projekta izpildi, un klients atzīst šo faktu. Darbinieks, kas veltīs šo laiku, saņems kredītu par savu apmaksājamo izmantošanu. Taču šīs izmaksas netiks iekasētas no klienta.
- **Nav pieejams**: Izmaksas, kas rodas iekšējos projektos un kam nav nepieciešama ieņēmumu izsekošana, tiek izsekotas, izmantojot šo opciju.

## <a name="invoice-schedule"></a>Rēķina izrakstīšanas grafiks

Rēķina izrakstīšanas grafiks ir datumu sērija, kas attiecas uz rēķinu izrakstīšanu projektā. Pēc izvēles varat izveidot rēķina izrakstīšanas grafiku piedāvājuma rindā. Katrai piedāvājuma rindai var būt savs rēķina izrakstīšanas grafiks. Lai izveidotu rēķina izrakstīšanas grafiku, ir jānorāda tālāk norādītās atribūtu vērtības.

- Rēķina perioda sākuma datums 
- Piegādes datums, kas norāda rēķina perioda beigu datumu projektā
- Rēķinu izrakstīšanas biežums

Šīs trīs atribūtu vērtības izmanto, lai ģenerētu varbūtēju datumu kopu, kam izveidot rēķinu izrakstīšanu.

## <a name="invoice-frequency"></a>Rēķinu izrakstīšanas biežums

Rēķinu izrakstīšanas biežums ir entītija, kas glabā atribūtu vērtības, kuras palīdz izteikt rēķinu izveides biežumu. Tālāk norādītie atribūti izsaka vai definē rēķinu izrakstīšanas biežuma entītiju.

- **Periods**: Tiek atbalstīti mēneša, divu nedēļu un nedēļas periodi. 
- **Izpildes katrā periodā**: Nedēļas un divu nedēļas periodiem var definēt tikai vienu izpildi katrā periodā. Mēneša periodiem var definēt no vienas līdz četrām izpildēm katrā periodā. 
- **Izpildes dienas**: Dienas, kurās jāveic rēķinu izrakstīšana. Šo atribūtu var konfigurēt divos veidos.
  - **Darbadienas**: Varat, piemēram, norādīt, ka rēķini tiek izrakstīti katru pirmdienu vai katru otro pirmdienu. Klienti, kuriem jāiestata rēķinu izrakstīšana darbadienā, var dod priekšroku šāda veida konfigurācijai. 
  - **Kalendārās dienas**: Varat, piemēram, norādīt, ka rēķini tiek izrakstīti katra mēneša septītajā un divdesmit pirmajā dienā. Dažas organizācijas var izvēlēties šāda veida konfigurāciju, jo tā palīdz garantēt, ka rēķini tiek izrakstīti, izmantojot fiksētu grafiku katru mēnesi.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Fiksētas cenas piedāvājuma rindas rēķina izrakstīšanas grafiks

Fiksētas cenas piedāvājuma rindai varat izmantot režģi **Rēķina izrakstīšanas grafiks**, lai izveidotu rēķina izrakstīšanas atskaites punktus, kas ir līdzvērtīgi piedāvājuma rindas vērtībai.

- Lai izveidotu rēķina izrakstīšanas atskaites punktus, kas ir vienādi sadalīti, atlasiet rēķinu izrakstīšanas biežumu, piedāvājuma rindā ievadiet rēķina perioda sākuma datumu un atlasiet piedāvājumam opciju **Pieprasītais pabeigšanas datums** piedāvājuma virsraksta sadaļā **Kopsavilkums**. Pēc tam atlasiet opciju **Izveidot periodiskus atskaites punktus**, lai izveidotu vienādi sadalītus atskaites punktus, pamatojoties uz atlasīto rēķinu izrakstīšanas biežumu. 
- Lai izveidotu vienreizējās izmaksas rēķina izrakstīšanas atskaites punktu, izveidojiet atskaites punktu un pēc tam ievadiet piedāvājuma rindas vērtību kā atskaites punkta summu.
- Lai izveidotu rēķinu izrakstīšanas atskaites punktus, kuru pamatā ir noteikti uzdevumi projekta plānā, izveidojiet atskaites punktu un kartējiet to uz projekta grafika elementu rēķina izrakstīšanas atskaites punkta UI.


[!INCLUDE[footer-include](../includes/footer-banner.md)]