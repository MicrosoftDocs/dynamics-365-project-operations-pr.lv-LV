---
title: Laika ierakstu izvēršana
description: Šajā rakstā ir sniegta informācija par to, kā izstrādātāji var pagarināt ieraksta kontroles laiku.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914779"
---
# <a name="extending-time-entries"></a>Laika ierakstu izvēršana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Dynamics 365 Project Operations ietver paplašināmu laika ievades pielāgotu vadīklu. Šī vadīkla ietver tālāk uzskaitītos līdzekļus.

- Laika ievadīšana horizontāli nedēļas tvērumā
- Kopsummas pa dienām, rindām vai nedēļām
- Rindu vai nedēļu kopēšana
- Laika ievade, izmantojot formātu HH:mm vai HH.hh (automātiski konvertē uz HH.hh)
- Importēšana no piešķirēm, rezervācijām vai tikšanās reizēm

Laika ierakstu izvēršana ir iespējama divos apgabalos:
- [Pielāgotu laika ierakstu pievienošana savai lietošanai](#add)
- [Nedēļas Laika ierakstu vadīklas pielāgošana](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Pielāgotu laika ierakstu pievienošana savai lietošanai

Laika ieraksti ir pamata entītija, kas tiek izmantota vairākos scenārijos. 2020. gada aprīļa 1. vilnī tika ieviests TESA pamata risinājums. TESA nodrošina entītiju **Iestatījumi** un jaunu drošības lomu **Laika ieraksta lietotājs**. Tika iekļauti arī jaunie lauki **msdyn_start** un **msdyn_end**, kam ir tieša saistība ar **msdyn_duration**. Jaunā entītija, drošības loma un lauki ļauj izveidot vienotāku pieeju laikam vairākos produktos.


### <a name="time-source-entity"></a>Laika avota entītija
| Lauks | Apraksts | 
|-------|------------|
| Nosaukums/vārds, uzvārds  | Laika avota ieraksta nosaukums, kas tiek izmantots kā atlases vērtība laika ierakstu izveides laikā. |
| Noklusējuma laika avots [laika avots: isdefault] | Pēc noklusējuma tikai vienu laika avotu var atzīmēt kā noklusējumu. Šādi ierakstiem var tikt iestatīts noklusējuma laika avots, ja tas nav norādīts. |
|Laika avota tips [Laika avots: sourcetype] | Avota tips ir opcija (Laika ieraksta avota tips), kas atļauj saistīt laika avotu ar programmu. Microsoft patur vērtības, kas lielākas par 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Laika ieraksti un entītija Laika avots
Katrs laika ieraksts tiek saistīts ar laika avota ierakstu. Šis ieraksts nosaka, kurām lietojumprogrammām ir jāapstrādā laika ievadne un kā.

Laika ieraksti vienmēr ir viens nepārtraukts laika bloks ar saistītu sākuma, beigu laiku un ilgumu.

Loģika automātiski atjaunina laika ieraksta ierakstu šādos gadījumos:

- Ja ir norādīti divi no trim tālāk uzskaitītajiem laukiem, trešais tiek aprēķināts automātiski. 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Lauki **msdyn_start** un **msdyn_end** ir zināmi laika joslai.
- Laika ieraksti, kas izveidoti tikai ar norādītu **msdyn_date** un **msdyn_duration**, tiks sākti pusnaktī. Lauki **msdyn_start** un **msdyn_end** tiks atbilstoši atjaunināti.

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

1. Pievienojiet pielāgoto lauku dialoglodziņam **Ātrā izveide**.
2. Konfigurējiet režģi, lai parādītu pielāgoto lauku.
3. Pēc vajadzības pievienojiet pielāgoto lauku lapai **Rindas rediģēšana** vai **Laika ieraksta rediģēšana**.

Pārliecinieties, vai jaunajam laukam lapā Rindas rediģēšana **vai** Laika ieraksta rediģēšana **ir** nepieciešamās validācijas. Šī uzdevuma ietvaros bloķējiet lauku, pamatojoties uz laika ieraksta statusu.

Pievienojot pielāgotu lauku laika ieraksta **režģim** un pēc tam veidojot laika ierakstus tieši režģī, šo ierakstu pielāgotais lauks tiek automātiski iestatīts tā, lai tas atbilstu rindai. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pielāgotā lauka pievienošana dialoglodziņam Ātrā izveide
Pievienojiet pielāgoto lauku dialoglodziņam **Ātrā izveide: laika ieraksta** izveide. Pēc tam lietotāji var ievadīt vērtību, pievienojot laika ierakstus, atlasot **Jauns**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurējiet režģi, lai parādītu pielāgoto lauku.
Ir divi veidi, kā pievienot pielāgotu lauku iknedēļas **laika ieraksta** režģim.

- Pielāgojiet **skatu Mani iknedēļas laika ieraksti** un pievienojiet tam pielāgoto lauku. Pielāgotā lauka atrašanās vietu un lielumu režģī var norādīt, rediģējot skata rekvizītus.
- Izveidojiet jaunu pielāgota laika ieraksta skatu un iestatiet to kā noklusējuma skatu. Šajā skatā papildus kolonnām, kurās jāiekļauj režģis, ir jābūt **laukiem Apraksts** un **Ārējie komentāri**. Režģa atrašanās vietu, lielumu un noklusējuma kārtošanas secību var norādīt, rediģējot rekvizītus skatā. Pēc tam konfigurējiet pielāgotu vadīklu šim skatam, lai tā būtu **Laika ierakstu režģa** vadīkla. Pievienojiet vadīklu skatam un atlasiet to tīmeklim, tālrunim **un** planšetdatoram **·**. **·** Pēc tam konfigurējiet nedēļas laika ieraksta **režģa** parametrus. **Iestatiet lauku Sākuma datums** uz **MSDYN\_ datumu**, iestatiet **lauku Ilgums** uz **msdyn\_ ilgumu** un iestatiet **lauku Statuss** uz **msdyn\_ entrystatus**. Lauks **Tikai lasāms statusu saraksts** ir iestatīts uz **192350002 (Apstiprināts)**, **192350003 (iesniegts)** vai **192350004 (pieprasīts atsaukt)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Pielāgotā lauka pievienošana atbilstošajai rediģēšanas lapai
Lapas, kas tiek izmantotas laika ieraksta vai laika ierakstu rindas rediģēšanai, var atrast sadaļā **Veidlapas**. Poga **Rediģēt ievadni** režģī atver **lapu Rediģēt ievadni**, un **poga Rediģēt rindā** tiek atvērta **lapa Rindas rediģēšana**. Šīs lapas var rediģēt, lai tajās būtu iekļauti pielāgoti lauki.

Abas opcijas noņem dažus izvades filtrus projekta **un** projekta uzdevuma **entītijās**, lai visi entītiju uzmeklēšanas skati būtu redzami. Ārpus lodziņa ir redzami tikai atbilstošie uzmeklēšanas skati.

Ir jānosaka pielāgotā lauka atbilstošā lapa. Visticamāk, ja lauks ir pievienots režģim, tam jāiet uz **rindas rediģēšanas** lapu, kas tiek izmantota laukiem, kuri attiecas uz visu laika ierakstu rindu. Ja pielāgotajam laukam katru dienu rindā ir unikāla vērtība (piemēram, ja tas ir pielāgots lauks beigu laikam), tam jāiet uz **lapu Laika ieraksta rediģēšana**.

Lai pielāgotu lauku pievienotu lapai, velciet **lauka** elementu atbilstošajā lapas pozīcijā un pēc tam iestatiet tā rekvizītus.

### <a name="add-new-option-set-values"></a>Jaunu opciju kopas vērtību pievienošana
Lai pievienotu opciju kopa vērtības ārpus rāmja laukam, rīkojieties šādi.

1. Atveriet lauka rediģēšanas lapu un pēc tam sadaļā **Tips** atlasiet **Rediģēt** blakus opciju kopa.
2. Pievienojiet jaunu opciju, kurai ir pielāgota etiķete un krāsa. Ja vēlaties pievienot jaunu laika ieraksta statusu, gatavā lauka nosaukums **ir Ieraksta statuss**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Jauna laika ieraksta tikai lasāma statusa norādīšana
Lai norādītu jaunu laika ieraksta statusu kā tikai lasāmu, pievienojiet jauno laika ieraksta vērtību rekvizītam **Tikai lasāma statusa saraksts**. Noteikti pievienojiet numuru, nevis etiķeti. Laika ieraksta režģa rediģējamā daļa tagad tiks bloķēta rindām ar jauno statusu. Lai dažādiem **laika ieraksta** skatiem rekvizītu Tikai lasāms statusa saraksts **iestatītu** atšķirīgi, pievienojiet **laika ieraksta** režģi skata pielāgoto vadīklu **sadaļā** un pēc vajadzības konfigurējiet parametrus.

Pēc tam pievienojiet biznesa kārtulas, lai bloķētu visus laukus lapās **Rindas rediģēšana** un **Laika ieraksta rediģēšana**. Lai piekļūtu šo lapu biznesa kārtulām, atveriet katras lapas veidlapu redaktors un pēc tam atlasiet **Biznesa kārtulas**. Jaunu statusu var pievienot nosacījumam esošajās biznesa kārtulās vai jaunajam statusam varat pievienot jaunu biznesa kārtulu.

### <a name="add-custom-validation-rules"></a>Pielāgotu validācijas kārtulu pievienošana
Nedēļas laika ievades **režģa pieredzei** var pievienot divu veidu pārbaudes kārtulas:

- Klienta puses biznesa kārtulas, kas darbojas lapās
- Servera puses spraudņa validācijas, kas attiecas uz visu laiku ierakstu atjauninājumiem

#### <a name="client-side-business-rules"></a>Klienta puses biznesa noteikumi
Izmantojiet biznesa kārtulas, lai bloķētu un atbloķētu laukus, ievadiet noklusējuma vērtības laukos un definējiet pārbaudes, kurām ir nepieciešama informācija tikai no pašreizējā laika ieraksta. Lai piekļūtu lapas biznesa kārtulām, atveriet veidlapu redaktors un pēc tam atlasiet **Biznesa kārtulas**. Pēc tam varat rediģēt esošās biznesa kārtulas vai pievienot jaunu biznesa kārtulu.

#### <a name="server-side-plug-in-validations"></a>Servera puses spraudņa validācijas
Spraudņa validācijas jāizmanto jebkurām validācijām, kurām nepieciešams vairāk konteksta, nekā tas ir pieejams viena laika ieraksta ierakstā. Tie jāizmanto arī visām validācijām, kuras vēlaties palaist ar režģī iekļautajiem atjauninājumiem. Lai pabeigtu validācijas, entītijā **Time Entry** izveidojiet pielāgotu spraudni.

### <a name="limits"></a>Ierobežojumi
**Pašlaik laika ievades** režģa lieluma ierobežojums ir 500 rindas. Ja ir vairāk nekā 500 rindu, liekās rindas netiks rādītas. Šo lieluma ierobežojumu nav iespējams palielināt.

### <a name="copying-time-entries"></a>Laika ierakstu kopēšana
Izmantojiet skatu **Kopēt laika ieraksta kolonnas**, lai definētu to lauku sarakstu, kas jākopē, ievadot laiku. **Datums** un **Ilgums** ir obligāti lauki, un tos nevar noņemt no skata.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
