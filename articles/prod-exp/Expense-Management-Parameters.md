---
title: Izdevumu pārvaldības parametri
description: Tālāk minētie parametri kontrolē darbību izdevumu pārvaldībā.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 41d78726f6d0aa6b5e647dbb359824950cb6ca72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993739"
---
# <a name="expense-management-parameters"></a>Izdevumu pārvaldības parametri


Parametri kontrolē vispārējo darbību izdevumu pārvaldībā.

### <a name="general"></a>VispārīgI

| **Lauks**                                                | **Apraksts**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Nobraukuma standarta likme**                             | Ievadiet atlīdzināšanas likmi par nobraukuma izdevumiem. Likme tiks reizināta ar nobraukumu, kas ievadīts pie izdevumiem, lai aprēķinātu summu, kas tiks atlīdzināta par ceļa izdevumiem.                       |
|**Personiskie izdevumi, ko apmaksā**                             | Atlasiet personu, kas atbildīga par visu to kredītkaršu darījumu summu apmaksu, kas klasificēti kā personiski.                                                                                                     |
|**Parādīt visu izdevumu atskaiti ar atgriešanu**               | Atlasiet šo opciju, lai rādītu visus izdevumus izdevumu atskaitē, kad tiek skatīta sākotnējā dokumenta detalizētā informācija par konkrētu dokumentu, kas tika ģenerēts, grāmatojot izdevumu atskaiti.              |
|**Atļauja pirms ceļošanas ir obligāta**                 | Atlasiet šo opciju, lai pieprasītu, ka, pirms darbinieks var iesniegt izdevumu atskaiti, tiek iesniegts un apstiprināts ceļojuma pieteikums.                                                                    |
|**Atļaut sadalījuma rediģēšanu pirms grāmatošanas**            | Atlasiet, vai izdevumu atskaites sadalījumu var rediģēt pirms grāmatošanas.                                                                                                                 |
|**Izvērtēt izdevumu pārvaldības politikas**                     | Atlasiet šo opciju, kad izdevumi tiek izvērtēti, lai noteiktu, vai ir pārkāpta izdevumu politika. Izdevumus var pārbaudīt saistībā ar pārkāpumiem, kad tiek ievadīti un saglabāti izmaksu ieraksti, vai arī brīdī, kad izdevumi tiek iesniegti apstiprināšanai. Politiku kārtulas par nepieciešamajiem čekiem tiek pārbaudītas, kad tiek saglabāta izdevumu rinda.                   |
|**Atļaut starpuzņēmumu izmaksu rindas**                         | Atlasiet, vai atļaut izdevumu ievadīšanu izdevumu atskaitē citām juridiskajām personām.                                                                                                          |
|**Atļaut rediģēt kredītkaršu izmaksu valūtas kursu** | Atlasiet šo opciju, lai ļautu lietotājam rediģēt valūtas kursu importētajiem kredītkaršu izdevumiem.                                                                        |
|**Rādāmie vairāklīmeņu hierarhijas lauki**                  | Atlasiet, kuri apstiprinātāja lauki tiek rādīti, kad izdevumu atskaites darbplūsmas piešķiršanas tips ir iestatīts kā hierarhija, un hierarhijas atlase ir iestatīta, lai izmantotu izdevumu vairāklīmeņu apstiprināšanu. Ja darbplūsmai tiek izmantota vairāklīmeņu apstiprināšanas hierarhija, atlasītie lauki tiks rādīti un būs rediģējami izdevumu atskaitē. |
|**Darbinieka kredītkartes numura ievadīšana (2017. gada jūlija atjauninājums)**     | Atlasiet, vai darbinieka lapā **Kredītkartes** laukā **Kartes ID** var ievadīt un saglabāt 15 rakstzīmju vai 16 rakstzīmju numuru.                                                                          |

### <a name="financial"></a>Izglītība

| **Lauks**                                                            | **Apraksts**     |
|----------------------------------------------------------------------|------------------------------------|
|**Virsgrāmatas dienas žurnāla nosaukums**                                         | Atlasiet tā virsgrāmatas žurnāla nosaukumu, kurā tiek grāmatotas apstiprinātās izdevumu atskaites.            |
|**Iespējot nodokļu atmaksu no izdevumiem**                                  | Atlasiet šo opciju, lai iespējotu izdevumu nodokļu atmaksu attaisnotajiem izdevumiem. Šo opciju nevar iespējot, ja ir iespējoti ASV pārdošanas un ekspluatācijas nodokļu noteikumi.      |
|**Grāmatot naudas avansus uzreiz**                                     | Atlasiet šo opciju, lai grāmatotu apstiprinātu naudas avansu, kad ir pabeigts process Apmaksāt un pārsūtīt. Ja šī opcija nav atlasīta, process Apmaksāt un pārsūtīt ģenerēs neiegrāmatotu virsgrāmatas žurnālu. |
|**Labot uzskaites datumu grāmatošanas laikā**                             | Atlasiet šo opciju, lai atjauninātu uzskaites datumu, kurā tiek grāmatoti izdevumi, ja pašreizējais periods ir aizturēts vai slēgts. Uzskaites datums tiks iestatīts uz nākamo atvērto periodu.   |
|**Atļaut darījumu grupēšanu, pamatojoties uz maksāšanas metodē norādīto ieskaita kontu**      | Atlasiet šo opciju, lai apkopotu izmaksu darījumus no izdevumu atskaites, pamatojoties uz ieskaita kontu, kas ir norādīts izdevumu maksāšanas metodē.   
|**Ar nodokli**                                                   | Atlasiet šo opciju, lai izmaksu summā pēc noklusējuma iekļautu pārdošanas nodokli.             |
|**Atbrīvot apgrūtinājumus, slēdzot ceļojumu pieteikumus**            | Atlasiet šo opciju, lai atbrīvotu apgrūtinātos līdzekļus, kad tiek slēgts apstiprināts ceļojuma pieteikums.                                                                                   |
|**Atļaut ceļojuma pieteikuma iesniegšanu ar budžeta reģistra un projekta budžeta pārsniegšanu** | Atlasiet šo opciju, lai ļautu darbiniekiem iesniegt ceļojuma pieteikumus apstiprināšanai, kas pārsniedz vai nu atļauto budžetu, kas noteikts budžeta reģistrā, vai projekta atļauto budžetu.            |
|**Atļaut izdevumu atskaites iesniegšanu ar budžeta reģistra un projekta budžeta pārsniegšanu**    | Atlasiet šo opciju, lai ļautu darbiniekiem iesniegt izdevumu atskaites apstiprināšanai, kas pārsniedz vai nu atļauto budžetu, kas noteikts budžeta reģistrā, vai projekta atļauto budžetu.                |
|**Atļaut izdevumu atskaites apstiprināšanu tikai ar budžeta reģistra pārsniegšanu**                | Atlasiet šo opciju, lai atļautu apstiprinātājiem apstiprināt izdevumu atskaites, kas pārsniedz budžeta reģistrā iestatīto atļauto budžetu.                                                                       |

### <a name="per-diem"></a>Dienasnauda

| **Lauks**                             | **Apraksts**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimālais stundu skaits dienasnaudai**           | Ievadiet noklusējuma minimālo stundu skaitu, kas darbiniekam ir jānostrādā dienā, lai saņemtu dienasnaudu ar ceļojumiem saistītiem izdevumiem.  Šo vērtību izmanto tikai kā noklusējuma vērtību attiecībā uz lauku Minimālais stundu skaits dienasnaudas likmju līmeņiem.                                                                                      |
|**Maltīšu procentuālā daļa**                          | Ievadiet dienasnaudas noklusējuma procentuālo vērtību maltītēm, ko izmanto ar ceļojumu saistīto izdevumu pirmajā un pēdējā dienā, kad lauks **Aprēķināt maltīšu samazināšanu par** ir iestatītas kā **Maltītes veids pēc dienas** vai **Maltīšu skaits dienā**. Pirmā un pēdējā darba dienā var būt īsāka nekā standarta darba diena. Tāpēc šajās dienās dienasnaudas summa var atšķirties no standarta summas. Ja procentuālā vērtība ir iestatīta uz 0, ieturējumi pirmajā un pēdējā dienā būs 0,00. |
|**Izmitināšanas procentuālā vērtība**                        | Ievadiet dienasnaudas noklusējuma procentuālo vērtību, kas tiek izmantota ar ceļa izdevumiem saistīto izdevumu pirmajā un pēdējā dienā izmitināšanai. Pirmā un pēdējā darba dienā var būt īsāka nekā standarta darba diena. Tāpēc šajās dienās dienasnaudas summa var atšķirties no standarta summas. Ja procentuālā vērtība ir iestatīta uz 0, ieturējumi pirmajā un pēdējā dienā būs 0,00.                                              |
|**Citu izdevumu procentuālā vērtība**                        | Ievadiet dienasnaudas noklusējuma procentuālo vērtību, kas tiek izmantota ar ceļa izdevumiem saistīto izdevumu pirmajā un pēdējā dienā dažādiem izdevumiem. Pirmā un pēdējā darba dienā var būt īsāka nekā standarta darba diena. Tāpēc šajās dienās dienasnaudas summa var atšķirties no standarta summas. Ja procentuālā vērtība ir iestatīta uz 0, ieturējumi pirmajā un pēdējā dienā būs 0,00.                                                                                                     |
|**Procentuālās vērtības samazinājums uz brokastu rēķina** | Ievadiet summu, par kādu dienasnaudas summu samazina uz brokastu rēķina. Piemēram, ja darbinieks saņem bezmaksas brokastis, varat samazināt dienasnaudas summu par 10 procentiem.                               |
|**Procentuālās vērtības samazinājums uz pusdienu rēķina**    | Ievadiet summu, par kādu dienasnaudas summu samazina uz pusdienu rēķina. Piemēram, ja darbinieks saņem bezmaksas pusdienas, varat samazināt dienasnaudas summu par 15 procentiem.                                       |
|**Procentuālās vērtības samazinājums uz vakariņu rēķina**   | Ievadiet summu, par kādu dienasnaudas summu samazina uz vakariņu rēķina. Piemēram, ja darbinieks saņem bezmaksas vakariņas, varat samazināt dienasnaudas summu par 25 procentiem.                                     |
|**Aprēķināt maltīšu izdevumu samazinājumu par**         | Atlasiet kā sistēmai jāaprēķina dienasnaudas samazināšana uz maltīšu rēķina, atlasot, vai samazinājums ir atkarīgs no ēdienreizes veida vienam braucienam vai vienai dienai, vai samazinājums ir atkarīgs no dienā atļauto maltīšu skaita.|
|**Dienasnaudas noapaļošana**                  | Atlasiet noapaļošanas veidu, kas tiek izmantots dienasnaudas izdevumiem. Ja atlasāt parastu noapaļošanu, dienasnaudas izdevumu, kura summa ir 0,50, noapaļo uz augšu līdz 1,00, un jebkuru dienasnaudas izdevumu, kura summa ir mazāka par 0,50, noapaļo uz leju līdz 0,00.                                                                                              |
|**Balstīt dienasnaudas aprēķinu uz**         | Atlasiet, vai dienasnaudas summa ir atkarīga no kalendāra dienas vai 24 stundu perioda.       |

### <a name="fax-cover-pages"></a>Faksa titullapas

| **Lauks**                      | **Apraksts**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Norādījumi**                   | Ievadiet norādījumus, kas darbiniekiem ir jāievēro, veidojot titullapu faksam, ko izmanto, lai nosūtītu ar izdevumu atskaiti saistītos čekus. Lai ievadītu rādāmo tekstu konkrētā valodā, pamatojoties uz lietotāja valodu, atlasiet pogu **Tulkojumi**. |
|**Lietotāja ID (svītrkoda +informācija)** | Atlasiet šo opciju, lai saglabātu darbinieka unikālo identifikatoru svītrkodā, ko izmanto faksa titullapā.                 |
|**Svītrkods**                      | Atlasiet svītrkodu, ko izmanto faksa titullapā. Izdevumu pārvaldībā tiek atbalstīti svītrkodi 39 un 128.               |

### <a name="anti-corruption"></a>Korupcijas apkarošana

|                 <strong>Lauks</strong>                 |                                                                                                                                                                                            <strong>Apraksts</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Parādīt apliecinājumu par korupcijas apkarošanu</strong>  | Atlasiet šo opciju, lai parādītu tekstu par korupcijas apkarošanu, kad tiek izveidota izdevumu atskaite. Var iespējot konkrētas izdevumu kategorijas, kuru gadījumā izdevumu atskaitē būtu obligātu jāatlasa apliecinājums par korupcijas apkarošanu. Piemēram, dāvanu kategorijai, kas saistīta ar valsts amatpersonu izdevumiem, var pieprasīt, lai darbinieks apstiprinātu, ka izdevumi atbilst uzņēmuma politikai saistībā ar valsts amatpersonām. |
| <strong>Paziņojums iesniedzējam par korupcijas apkarošanu</strong> |                                                                                             Ievadiet tekstu, kas tiks rādīts darbiniekam, izveidojot jaunu izmaksu atskaiti. Lai ievadītu rādāmo tekstu konkrētā valodā, pamatojoties uz lietotāja valodu, atlasiet pogu <strong>Tulkojumi</strong>.                                                                                             |
| <strong>Paziņojums apstiprinātājam par korupcijas apkarošanu</strong>  |                                                                                             Ievadiet tekstu, kas tiks rādīts apstiprinātājam, izveidojot jaunu izmaksu atskaiti. Lai ievadītu rādāmo tekstu konkrētā valodā, pamatojoties uz lietotāja valodu, atlasiet pogu <strong>Tulkojumi</strong>.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]