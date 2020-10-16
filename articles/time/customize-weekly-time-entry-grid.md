---
title: Laika ierakstu izvēršana
description: Šajā tēmā ir sniegta informācija par to, kā izstrādātāji var izvērst laika ieraksta vadīklu.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930889"
---
# <a name="extending-time-entries"></a>Laika ierakstu izvēršana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations ir ietverta izvēršama laika ierakstu pielāgotā vadīkla. Šī vadīkla ietver tālāk uzskaitītos līdzekļus.

- Laika ievadīšana horizontāli nedēļas tvērumā
- Kopsummas pa dienām, rindām vai nedēļām
- Rindu vai nedēļu kopēšana
- Laika ievade, izmantojot formātu HH:mm vai HH.hh (automātiski konvertē uz HH.hh)
- Importēšana no piešķirēm, rezervācijām vai tikšanās reizēm

Laika ierakstu izvēršana ir iespējama divos apgabalos:
- [Pielāgotu laika ierakstu pievienošana savai lietošanai](#add)
- [Nedēļas Laika ierakstu vadīklas pielāgošana](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Pielāgotu laika ierakstu pievienošana savai lietošanai.

Laika ieraksti ir pamata entītija, kas ir paredzēta lietošanai vairākiem scenārijiem. 2020. gada aprīļa 1. laidienā tika ieviests TESA pamata risinājums, kas nodrošina entītiju **Iestatījumi** un jaunu drošības lomu **Laika ierakstu lietotājs**. Tika iekļauti arī jaunie lauki **msdyn_start** un **msdyn_end**, kam ir tieša saistība ar **msdyn_duration**. Jaunā entītija, drošības loma un lauki ļauj izveidot vienotāku pieeju laikam vairākos produktos.


### <a name="time-source-entity"></a>Laika avota entītija
| Lauks | Apraksts | 
|-------|------------|
| Nosaukums/vārds, uzvārds  | Laika avota ieraksta nosaukums, kas tiek izmantots kā atlases vērtība laika ieraksta izveides laikā. |
| Noklusējuma laika avots [laika avots: isdefault] | Pēc noklusējuma kā noklusējuma laika avotu var atzīmēt tikai vienu Laika avotu. Šī iespēja nozīmē, ka ierakstiem pēc noklusējuma var būt laika avots, ja tas nav norādīts. |
|Laika avota tips [Laika avots: sourcetype] | Avota tips ir opcija (Laika ieraksta avota tips), kas atļauj saistīt laika avotu ar programmu. Šai opciju kopai tiek pievienotas papildu vērtības, kad tiek pievienotas papildu programmas. Ņemiet vērā, ka Microsoft patur vērtības, kas lielākas par 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Laika ieraksti un Laika avota entītija
Katrs laika ieraksts tiek saistīts ar laika avota ierakstu. Šis ieraksts nosaka, kā un kurām programmām jāapstrādā laika ieraksts.

Laika ieraksti vienmēr ir viens nepārtraukts laika bloks ar saistītu sākuma, beigu laiku un ilgumu.

Loģika automātiski atjaunina laika ieraksta ierakstu šādos gadījumos:

- Ja ir norādīti divi no trim tālāk uzskaitītajiem laukiem, trešais tiek aprēķināts automātiski 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Laukos **msdyn_start** un **msdyn_end** ir ņemtas vērā laika joslas.
- Laika ieraksti, kas izveidoti, norādot tikai laukus **msdyn_date** un **msdyn_duration**, tiek sākti pusnaktī, un tiek attiecīgi atjaunināti lauki **msdyn_start** **msdyn_end**.

#### <a name="time-entry-types"></a>Laika ierakstu tipi

Laika ierakstiem ir saistītais tips, kas definē darbības saistītās programmas iesniegšanas plūsmā.

|Etiķete | vērtība|
|-----|-----|
|Pārtraukums   |192,355,000|
|Ceļš | 192,355,001|
|Virsstundas   | 192,354,320|
|Darbs   | 192,350,000|
|Kavējumi    | 192,350,001|
|Atvaļinājums   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Nedēļas Laika ierakstu vadīklas pielāgošana
Izstrādātāji var pievienot papildu laukus un uzmeklēšanas rīkus citām entītijām, kā arī ieviest pielāgotas biznesa kārtulas, lai atbalstītu savus uzņēmējdarbības scenārijus.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Pielāgotu lauku ar uzmeklēšanām pievienošana citām entītijām
Ir trīs galvenās darbības pielāgotu lauku pievienošanai iknedēļas laika ierakstu režģim.

- Pievienojiet pielāgoto lauku ātrās izveides dialoglodziņam.
- Konfigurējiet režģi, lai parādītu pielāgoto lauku.
- Pievienojiet pielāgoto lauku vai nu rindu rediģēšanas uzdevumu plūsmai vai šūnu rediģēšanas uzdevumu plūsmai.

Ir jāpārliecinās arī par to, vai jaunajam laukam ir nepieciešamās pārbaudes rindas vai šūnas rediģēšanas uzdevuma plūsmā. Veicot šo darbību, lauks ir jābloķē, pamatojoties uz laika ieraksta statusu.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pielāgoto lauku pievienošana ātrās izveides dialoglodziņam
Pielāgotais lauks ir jāpievieno dialoglodziņam **Laika ieraksta ātrā izveide**. Pēc tam lietotāji var ievadīt vērtību, pievienojot laika ierakstus, atlasot **Jauns**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurējiet režģi, lai parādītu pielāgoto lauku.
Ir divi veidi, kā pievienot pielāgotu lauku iknedēļas laika ierakstu režģim.

  - Skata pielāgošana un pielāgota lauka pievienošana
  - Jauna noklusējuma pielāgota laika ieraksta izveide 


**Skata pielāgošana un pielāgota lauka pievienošana**

Varat pielāgot skatu **Mani iknedēļas laika ieraksti** un pievienot tam pielāgoto lauku. Varat izvēlēties pielāgotā lauka novietojumu un izmēru režģī, rediģējot šos rekvizītus skatā.

**Jauna noklusējuma pielāgota laika ieraksta izveide** 

Šajā skatā ir jābūt iekļautiem laukiem **Apraksts** un **Ārējie komentāri** papildus tām kolonnām, kuras vēlaties redzēt režģī. 

1. Izvēlieties režģa novietojumu, izmēru un kārtošanas secību, rediģējot šos rekvizītus skatā. 
2. Konfigurējiet pielāgotu vadīklu šim skatam, lai tā būtu vadīkla **Laika ierakstu režģis**. 
3. Pievienojiet šo vadīklu skatam un atlasiet to tīmeklim, tālrunim un planšetdatoram. 
4. Konfigurējiet iknedēļas laika ierakstu režģa parametrus. Iestatiet lauku **Sākuma datums** uz **msdyn_date**, iestatiet lauku **Ilgums** uz **msdyn_duration** un iestatiet lauku **Statuss** uz **msdyn_entrystatus**. 
5. Noklusējuma skatam lauks **Tikai lasāms statusa saraksts** ir iestatīts uz **192350002, 192350003, 192350004**, lauks **Rindas rediģēšanas uzdevuma plūsma** ir iestatīts uz **msdyn_timeentryrowedit** un lauks **Šūnu rediģēšanas uzdevumu plūsma** ir iestatīts uz **msdyn_timeentryedit**. 
6. Varat pielāgot šos laukus, lai pievienotu vai noņemtu tikai lasāmu statusu vai izmantotu atšķirīgu uz uzdevumu balstītu pieredzi (TBX) rindu vai šūnu rediģēšanai. Šiem laukiem ir jābūt saistītiem ar statisku vērtību.


> [!NOTE] 
> Abas opcijas noņems dažus neiekļautus filtrus entītijām **Projekts** un **Projekta uzdevums**, lai būtu redzami visi entītiju uzmeklēšanas skati. Ārpus lodziņa ir redzami tikai atbilstošie uzmeklēšanas skati.
Pielāgotajam laukam ir jānosaka piemērota uzdevumu plūsma. Visticamāk, ja pievienojāt lauku režģim, tam ir jābūt rindas rediģēšanas uzdevumu plūsmā, kas attiecas uz visu laika ierakstu rindu. Ja pielāgotajam laukam katru dienu ir unikāla vērtība, piemēram, pielāgots lauks **Beigu laiks**, tam ir jābūt šūnu rediģēšanas uzdevumu plūsmā.

Lai uzdevumu plūsmai pievienotu pielāgoto lauku, velciet elementu **Lauks** uz atbilstošo atrašanās vietu lapā un pēc tam iestatiet lauka rekvizītus. Iestatiet rekvizītu **Avots** uz **Laika ieraksts** un iestatiet rekvizītu **Datu lauks** pielāgotajam laukam. Rekvizīts **Lauks** norāda TBX lapā parādāmo nosaukumu. Atlasiet vienumu **Lietot**, lai laukā saglabātu izmaiņas, un pēc tam atlasiet vienumu **Atjaunināt**, lai saglabātu lapā veiktās izmaiņas.

Lai tā vietā izmantotu jaunu pielāgotu TBX lapu, izveidojiet jaunu procesu. Iestatiet kategoriju uz **Biznesa procesa plūsma**, iestatiet entītiju uz **Laika ieraksts** un iestatiet biznesa procesa tipu uz **Palaist procesu kā uzdevuma plūsmu**. Sadaļā **Rekvizīti** ir jāiestata **Lapas nosaukums** lapas parādāmajam nosaukumam. Pievienojiet TBX lapai visus atbilstošos laukus. Saglabājiet un aktivizējiet procesu, un pēc tam procesam atjauniniet pielāgoto kontroles rekvizītu attiecīgajai uzdevumu plūsmai uz vērtību **Nosaukums**.

### <a name="add-new-option-set-values"></a>Jaunu opciju kopas vērtību pievienošana
Lai pievienotu opciju kopu vērtības neiekļautajam laukam, atveriet lauka rediģēšanas lapu un pēc tam sadaļā **Tips** atlasiet **Rediģēt**, kas atrodas blakus opciju kopai. Pēc tam pievienojiet jaunu opciju, kurai ir pielāgota etiķete un krāsa. Ja vēlaties pievienot jaunu laika ieraksta statusu, neiekļautā lauka nosaukums ir **Ieraksta statuss**, nevis **Statuss**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Jauna laika ieraksta tikai lasāma statusa norādīšana
Lai norādītu jaunu laika ieraksta statusu kā tikai lasāmu, pievienojiet jauno laika ieraksta vērtību rekvizītam **Tikai lasāma statusa saraksts**. Laika ieraksta režģa rediģējamā daļa tiks bloķēta rindām ar jaunu statusu.
Pēc tam pievienojiet biznesa kārtulas, lai bloķētu visus laukus TBX lapās **Laika ierakstu rindu rediģēšana** un **Laika ierakstu rediģēšana**. Šo lapu biznesa kārtulām var piekļūt, atverot lapas biznesa procesa plūsmas redaktoru un atlasot **Biznesa kārtulas**. Jaunu statusu var pievienot nosacījumam esošajās biznesa kārtulās vai jaunajam statusam varat pievienot jaunu biznesa kārtulu.

### <a name="add-custom-validation-rules"></a>Pielāgotu validācijas kārtulu pievienošana
Ir divi validācijas kārtulu tipi, ko varat pievienot iknedēļas laika ieraksta režģa lietošanas pieredzei.

- Klienta puses biznesa kārtulas, kas darbojas ātrās izveides dialoglodziņos un TBX lapās.
- Servera puses spraudņu validācijas, kas attiecas uz visiem laika ierakstu atjauninājumiem.

#### <a name="business-rules"></a>Biznesa kārtulas
Izmantojiet biznesa kārtulas, lai bloķētu un atbloķētu laukus, ievadiet noklusējuma vērtības laukos un definējiet pārbaudes, kurām ir nepieciešama informācija tikai no pašreizējā laika ieraksta. TBX lapai paredzētajām biznesa kārtulām var piekļūt, atverot lapas biznesa procesa plūsmas redaktoru un atlasot **Biznesa kārtulas**. Pēc tam varat rediģēt esošās biznesa kārtulas vai pievienot jaunu biznesa kārtulu. Vēl vairāk pielāgotām pārbaudēm varat izmantot biznesa kārtulu, lai palaistu JavaScript.

#### <a name="plug-in-validations"></a>Spraudņu pārbaudes
Ir jāizmanto spraudņu pārbaudes jebkādām pārbaudēm, kurām nepieciešams vairāk konteksta, nekā pieejams vienā laika ierakstā, vai jebkādām pārbaudēm, ko vēlaties izpildīt, izmantojot režģī iekļautos atjauninājumus. Lai pabeigtu pārbaudi, izveidojiet pielāgotu spraudni entītijā **Laika ieraksts**.
