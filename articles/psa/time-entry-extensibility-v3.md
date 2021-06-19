---
title: Nedēļas laika ieraksta pielāgošana
description: Šajā tēmā ir sniegta informācija par to, kā ieviest pielāgotas biznesa kārtulas, kas atbalsta organizācijas praksi.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c117e06e7a5c57c7f9b70d1380f450c0ea97cd12
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013045"
---
# <a name="customize-weekly-time-entry"></a>Nedēļas laika ieraksta pielāgošana 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 Project Service Automation 3.3 versijā ir ieviests mūsdienīgs režģis, kas projekta resursiem ļauj ātri vienlaikus ievadīt laiku līdz vienai nedēļai. Jaunais iknedēļas laika ierakstu režģis var rādīt kopsummas ierakstiem pēc datuma, rindas vai nedēļas. Resursi var izveidot laika ierakstu kopijas nedēļas laikā un arī lielapjoma kopiju no iepriekšējām nedēļām. Sistēmas pielāgotāji var pielāgot skatu, pievienojot laukus, pievienojot uzmeklēšanas citām entītijām un ieviešot pielāgotas biznesa kārtulas, lai atbalstītu savas organizācijas praksi.

Laika ieraksts un jaunais iknedēļas laika režģis ir pieejami, izmantojot vietnes karti. Nepaplašināms pielāgots laika ieraksts, kas bija atrodams iepriekšējās PSA versijās, tika aizstāts ar paplašināmo iknedēļas laika ierakstu režģi, kā arī ar alternatīvu pieredzi tikai lasāmā režģī un kalendārā. Sakarā ar šīm izmaiņām lietotāji var ievadīt laiku iknedēļas summās.

## <a name="page-layout"></a>Lapas izkārtojums
Jaunais iknedēļas laika ierakstu režģis ir pielāgota vadīkla, kurā ir rīkjosla un divas galvenās sadaļas: **Dimensijas** un **Ilgums**. Rīkjoslā ir iekļauta poga, kas attiecas tikai uz šo pielāgoto vadīklu laika ierakstu režģim. Turpretī pogas Darbību rūtī lapas augšdaļā attiecas uz trim vadīklu tipiem, ko atbalsta laika ieraksts: iknedēļas laika ieraksta vadīkla, tikai lasāma vadīkla un kalendāra vadīkla.

### <a name="dimensions"></a>Izmēri
Sadaļā **Dimensijas** kā kolonnu virsraksti tiek rādītas visas dimensijas, kurām var ievadīt laiku. Šādas dimensijas tiek sākotnēji atbalstītas.

- Projekts
- Projekta uzdevums
- Loma
- Tips
- Ieraksta statuss

Sadaļā **Dimensijas** iekļautā rediģēšana nav atļauta. Šīs sadaļas pamatā ir skats, kas iespējo pielāgotus laukus pievienošanai iknedēļas laika ierakstu režģim. Lai iegūtu informāciju par pielāgotu lauku pievienošanu, skatiet tālāk šajā tēmā sadaļu “Paplašināšana”.

### <a name="duration"></a>Ilgums
Sadaļā Ilgums ir parādītas nedēļas dienas kā kolonnu virsraksti. Šajā sadaļā iekļautā rediģēšana ir atļauta. Pēc tam, kad tiek izveidota laika ieraksta rinda ar atbilstošām dimensijām, lietotāji var ātri ievadīt, iekļaut laika periodu, ko viņi patērējuši uz šīm dimensijām.

## <a name="create-a-new-time-entry"></a>Jauna laika ieraksta izveide
Jauna laika ieraksta izveidei atlasiet **Jauns** laika ierakstu režģī. Tiek atvērts dialoglodziņš **Laika ieraksta ātrā izveide**. Šajā dialoglodziņā lietotāji var atlasīt laika ieraksta datumu un pēc tam ievadīt datus dimensijām **Projekts**, **Projekta uzdevums**, **Loma** un **Ilgums** minūtēs, stundās vai dienās, ievadot **s**, **m** vai **d** kopā ar numuru. Lietotāji var ievadīt arī aprakstu un komentārus, ko var ārēji kopīgot laika ierakstam. Kad lietotāji saglabā savas izmaiņas, pretī dimensijām ierakstītās vērtības tiek rādītas sadaļā **Dimensijas**. Informācija par ilgumu, ko viņi ievadījuši laukā **Ilgums**, tiek parādīta laika ieraksta izveidošanas datumā.

Uzmeklēšanas laukus atbalsta sistēmas skati. Piemēram, pēc tam, kad lietotājs ievada projektu, lauks **Projekta uzdevums** pēc noklusējuma tiek iestatīts uz **Kopēšanas** skatu. Lai izveidotu laika ierakstus uzdevumiem, kas nav piešķirti lietotājam, uzmeklēšanas dialoglodziņā atlasiet **Mainīt skatu** un pēc tam atlasiet skatu **Visi aktīvi projekta uzdevumi**.

## <a name="edit-a-time-entry"></a>Laika ieraksta rediģēšana
Detalizēta informācija no dažiem laukiem laika ieraksta lapā, piemēram, **Apraksts** un **Ārējie komentāri**, netiek rādīti iknedēļas laika ierakstu režģī. Tā vietā ilguma šūnās, kurās ir šāda papildinformācija, parādās neliels trīsstūra indikators. Atlasiet šūnu un pēc tam atlasiet **Rediģēt papildinformāciju**, lai skatītu datus rūtī **Ātra rediģēšana**. Lai rediģētu vai atjauninātu papildinformāciju par konkrētu laika ierakstu, kas nav nedēļas laika ierakstu režģa daļa, lietotājiem ir jāatver rūts **Ātra rediģēšana**.

## <a name="copy-a-time-entry-row"></a>Laika ieraksta rindas kopēšana
Pēc pirmās laika ieraksta rindas izveides lietotāji var atlasīt **Kopēt rindu**, lai kopētu visu rindu jaunā rindā. Ja rinda tiek kopēta šādā veidā, tiek kopētas arī dimensijas un ilgums. Lietotāji var arī atlasīt opciju **Rediģēt rindu**, lai atjauninātu dimensiju vērtības un ilgumu, kas iekļauti sadaļā **Ilgums**.

## <a name="open-a-time-entry"></a>Laika ieraksta atvēršana
Lai nodrošinātu optimālu un ātru ievadi labākajos laukos, iknedēļas laika ieraksta režģī tiek rādīta atlasīto dimensiju un laika ilguma apakškopa. Lai skatītu visu papildinformāciju par vienu laika ierakstu, sadaļā **Rediģēt ierakstu** atlasiet **Atvērt**.

## <a name="submit-a-time-entry"></a>Laika ieraksta iesniegšana
Lietotāji var iesniegt vienu laika ierakstu vai laika ierakstu grupu, atlasot šūnu bloku vai visu laika ierakstu rindu un pēc tam atlasot **Iesniegt**. Iesniegtie laika ieraksti tiek rādīti kā vēl neapstiprināti ieraksti apstiprinātāja **Apstiprinājuma** lapā. Pēc laika ierakstu sekmīgi iesniegšanas tos vairs nevar rediģēt.

## <a name="recall-a-time-entry"></a>Laika ieraksta atsaukšana
Iesniegtos laika ierakstus var atsaukt. Varat atsaukt vienu laika ierakstu, laika ierakstu bloku vai veselu laika ierakstu rindu. Resursiem atsaucamie laika ieraksti ir pieejami rediģēšanai.

## <a name="time-entry-status"></a>Laika ieraksta statuss
Jauniem laika ierakstiem automātiski tiek piešķirts statuss **Melnraksts**. Iesniedzot laika ierakstu, statuss tiek atjaunināts uz **Iesniegts**. Kad iesniegtais laika ieraksts ir apstiprināts, statuss tiek atjaunināts uz **Apstiprināts**. Ja laika ieraksts ir noraidīts, statuss tiek atjaunināts uz **Atgriezts**, un ieraksts kļūst pieejams labošanai un atkārtotai iesniegšanai. Var dzēst tikai tos laika ierakstus, kuriem ir statuss **Melnraksts**.

## <a name="view-rejection-comments"></a>Noraidīšanas komentāru skatīšana
Kad apstiprinātājs noraida laika ierakstu, apstiprinātājs var pievienot noraidīšanas komentārus, lai palīdzētu resursam izprast atteikuma iemeslu. Lai skatītu atteikuma komentārus laika ierakstam, atlasiet **Atvērt ierakstu**. Atteikuma komentāri tiks parādīti laika skalā. Laika skalā resurss var atbildēt uz atteikuma komentāriem, pirms viņš vai viņa atkārtoti iesniedz ierakstu.

## <a name="copy-week"></a>Nedēļas kopēšana
Pēc neilga laika pēc laika ierakstu izveides lietotāji var atlasīt **Kopēt nedēļu**, lai masveidā izveidotu papildu laka ierakstus. Tiek atvērts dialoglodziņš **Kopēt**. Sadaļā **No perioda** izmantojiet laukus **Sākuma datums** un **Beigu datums**, lai definētu datumu diapazonu, no kura kopēt laika ierakstus. Sadaļā **Līdz periodam**, laukā **Sākuma datums** norādiet datumu, kuram veidot laika ierakstus. Tad atlasiet **Kopēt**. Noteiktam datumam periodā “līdz” tiek izveidota laika ierakstu kopija atbilstošai nedēļas dienai periodā “no”. Piemēram, pagājušās nedēļas pirmdienas laika ieraksts tiek kopēts uz nedēļas pirmdienu, kura norādīta kā “līdz” periods.

## <a name="import"></a>Importēšana
To pašu pamata procesu izmanto importēšanai no rezervācijām, uzdevumiem un apmaiņām. Lietotāji var norādīt datu diapazonu, no kura tiek importētas rezervācijas. Pēc tam viņiem ir tieši jāatlasa rezervācijas, kas ir jākopē melnraksta laika ierakstos. Iepriekšējā laidienā ieteiktie laika ieraksti tika parādīti režģī un kalendārā, bet tika zaudēti sesijas atsvaidzināšanas laikā.

## <a name="extensibility"></a>Paplašināmība
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Pielāgotu lauku, kam ir uzmeklēšanas, pievienošana citām entītijām
Ir trīs galvenās darbības pielāgotu lauku pievienošanai iknedēļas laika ierakstu režģim.

1.  Pievienojiet pielāgoto lauku ātrās izveides dialoglodziņam.
2.  Konfigurējiet režģi, lai parādītu pielāgoto lauku.
3.  Pievienojiet pielāgotu lauku vai nu rindu rediģēšanas uzdevumu plūsmai vai šūnu rediģēšanas uzdevumu plūsmai, ja nepieciešams.

Ir jāpārliecinās arī par to, vai jaunajam laukam ir nepieciešamās pārbaudes rindas vai šūnas rediģēšanas uzdevuma plūsmā. Veicot šo darbību, lauks ir jābloķē, pamatojoties uz laika ieraksta statusu.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pielāgoto lauku pievienošana ātrās izveides dialoglodziņam
Pielāgotais lauks ir jāpievieno dialoglodziņam Laika ieraksta ātrā izveide. Lai lietotāji varētu ievadīt tā vērtību, pievienojot laika ierakstus, izmantojot pogu **Jauns**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurējiet režģi, lai parādītu pielāgoto lauku.
Ir divi veidi, kā pievienot pielāgotu lauku iknedēļas laika ierakstu režģim. Vispirms ir jāpielāgo skats **Manas iknedēļas laika ieraksti** un jāpievieno tam pielāgotais lauks. Varat izvēlēties pielāgotā lauka novietojumu un izmēru režģī, rediģējot šos rekvizītus skatā.

Otra opcija ir izveidot jaunu pielāgotu laika ierakstu skatu un iestatīt to kā noklusējuma skatu. Šajā skatā ir jābūt iekļautiem laukiem **Apraksts** un **Ārējie komentāri** papildus tām kolonnām, kuras vēlaties redzēt režģī. Varat izvēlēties režģa novietojumu, izmēru un kārtošanas secību, rediģējot šos rekvizītus skatā. Pēc tam konfigurējiet pielāgotu vadīklu šim skatam, lai tā būtu **Laika ierakstu režģa** vadīkla. Pievienojiet šo vadīklu skatam un atlasiet to tīmeklim, tālrunim un planšetdatoram. Pēc tam konfigurējiet iknedēļas laika ierakstu režģa parametrus. Iestatiet lauku **Sākuma datums** uz **msdyn_date**, iestatiet lauku **Ilgums** uz **msdyn_duration** un iestatiet lauku **Statuss** uz **msdyn_entrystatus**. Noklusējuma skatam lauks **Tikai lasāms statusa saraksts** ir iestatīts uz **192350002, 192350003, 192350004**, lauks **Rindas rediģēšanas uzdevuma plūsma** ir iestatīts uz **msdyn_timeentryrowedit** un lauks **Šūnu rediģēšanas uzdevumu plūsma** ir iestatīts uz **msdyn_timeentryedit**. Varat pielāgot šos laukus, lai pievienotu vai noņemtu tikai lasāmu statusu vai izmantotu atšķirīgu uz uzdevumu balstītu pieredzi (TBX) rindu vai šūnu rediģēšanai. Šiem laukiem ir jābūt saistītiem ar statisku vērtību.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Pielāgotā lauka pievienošana atbilstošajai rediģēšanas uzdevumu plūsmai
TBX lapas, kas tiek izmantotas rediģēšanai, var atrast sadaļā **Procesi**. Noklusējuma lapas ir **Project Service – Laika ierakstu rindas rediģēšana** un **Project Service – Laika ierakstu rediģēšana**. Varat vai nu rediģēt šīs noklusējuma lapas, vai izveidot jaunas pielāgotas TBX lapas.

> [!NOTE] 
> Abas opcijas noņems dažus neiekļautus filtrus entītijām, **Projekts** un **Projekta uzdevums**, lai būtu redzami visi entītiju uzmeklēšanas skati. Ārpus lodziņa ir redzami tikai atbilstošie uzmeklēšanas skati.

Pielāgotajam laukam ir jānosaka piemērota uzdevumu plūsma. Visticamāk, ja pievienojāt lauku režģim, tam ir jābūt rindas rediģēšanas uzdevumu plūsmā, kas attiecas uz visu laika ierakstu rindu. Ja pielāgotajam laukam katru dienu ir unikāla vērtība, piemēram, pielāgots lauks **Beigu laiks**, tam ir jābūt šūnu rediģēšanas uzdevumu plūsmā.

Lai uzdevumu plūsmai pievienotu pielāgoto lauku, velciet elementu **Lauks** uz atbilstošo atrašanās vietu lapā un pēc tam iestatiet tā rekvizītus. Iestatiet rekvizītu **Avots** uz **Laika ieraksts** un iestatiet rekvizītu **Datu lauks** pielāgotajam laukam. Rekvizīts **Lauks** norāda TBX lapā parādāmo nosaukumu. Lai saglabātu izmaiņas laukā, atlasiet **Lietot**. Pēc tam, lai saglabātu izmaiņas lapā, atlasiet **Atjaunināt**.

Lai tā vietā izmantotu jaunu pielāgotu TBX lapu, izveidojiet jaunu procesu. Iestatiet kategoriju uz **Biznesa procesa plūsma**, iestatiet entītiju uz **Laika ieraksts** un iestatiet biznesa procesa tipu uz **Palaist procesu kā uzdevuma plūsmu**. Sadaļā **Rekvizīti** ir jāiestata **Lapas nosaukums** lapas parādāmajam nosaukumam. Pievienojiet TBX lapai visus atbilstošos laukus. Saglabājiet un aktivizējiet procesu, un pēc tam procesam atjauniniet pielāgoto kontroles rekvizītu attiecīgajai uzdevumu plūsmai uz vērtību **Nosaukums**.

### <a name="add-new-option-set-values"></a>Jaunu opciju kopas vērtību pievienošana
Lai pievienotu opciju kopu vērtības neiekļautajam laukam, atveriet lauka rediģēšanas lapu un pēc tam sadaļā **Tips** atlasiet **Rediģēt**, kas atrodas blakus opciju kopai. Pēc tam pievienojiet jaunu opciju, kurai ir pielāgota etiķete un krāsa. Ja vēlaties pievienot jaunu laika ieraksta statusu, neiekļautā lauka nosaukums ir **Ieraksta statuss**, nevis **Statuss**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Jauna laika ieraksta tikai lasāma statusa norādīšana
Lai norādītu jaunu laika ieraksta statusu kā tikai lasāmu, pievienojiet jauno laika ieraksta vērtību (numuru, nevis etiķeti) rekvizītam **Tikai lasāma statusa saraksts**. Laika ieraksta režģa rediģējamā daļa tiks bloķēta rindām ar jaunu statusu.
Pēc tam pievienojiet biznesa kārtulas, lai bloķētu visus laukus TBX lapās **Laika ierakstu rindu rediģēšana** un **Laika ierakstu rediģēšana**. Šo lapu biznesa kārtulām var piekļūt, atverot lapas biznesa procesa plūsmas redaktoru un atlasot **Biznesa kārtulas**. Jaunu statusu var pievienot nosacījumam esošajās biznesa kārtulās vai jaunajam statusam varat pievienot jaunu biznesa kārtulu.

### <a name="add-custom-validation-rules"></a>Pielāgotu validācijas kārtulu pievienošana
Ir divi pārbaudes noteikumu tipi, ko varat pievienot iknedēļas laika ieraksta režģa procesam: • klienta puses biznesa kārtulas, kas darbojas ātrās izveides dialoglodziņos un TBX lapās • servera puses spraudņu pārbaudes, kas attiecas uz visiem laika ierakstu atjauninājumiem

#### <a name="business-rules"></a>Biznesa kārtulas
Izmantojiet biznesa kārtulas, lai bloķētu un atbloķētu laukus, ievadiet noklusējuma vērtības laukos un definējiet pārbaudes, kurām ir nepieciešama informācija tikai no pašreizējā laika ieraksta. TBX lapai paredzētajām biznesa kārtulām var piekļūt, atverot lapas biznesa procesa plūsmas redaktoru un atlasot **Biznesa kārtulas**. Pēc tam varat rediģēt esošās biznesa kārtulas vai pievienot jaunu biznesa kārtulu. Vēl vairāk pielāgotām pārbaudēm varat izmantot biznesa kārtulu, lai palaistu JavaScript.

#### <a name="plug-in-validations"></a>Spraudņu pārbaudes
Ir jāizmanto spraudņu pārbaudes jebkādām pārbaudēm, kurām nepieciešams vairāk konteksta, nekā pieejams vienā laika ierakstā, vai jebkādām pārbaudēm, ko vēlaties izpildīt, izmantojot režģī iekļautos atjauninājumus. Lai pabeigtu pārbaudi, izveidojiet pielāgotu spraudni entītijā **Laika ieraksts**.

> [!IMPORTANT] 
> Pašlaik zināmā problēma TBX lapās neļauj lietotājiem labot informāciju un atkārtoti atlasīt Gatavs, kad atjauninājumam neizdodas veikt spraudņa pārbaudi. Kā risinājumu iestatiet biznesa kārtulu pārbaudes, lai pēc iespējas labāk novērstu šo situāciju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]