---
title: Izdevumu pārvaldības parametru konfigurēšana
description: Šajā tēmā ir aprakstīti parametri, kas kontrolē Izmaksu pārvaldības vispārējo darbību.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 93cb95ffc0348a1ad1905fbf308477d18e589185
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276672"
---
# <a name="configure-expense-management-parameters"></a>Izdevumu pārvaldības parametru konfigurēšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šajā tēmā ir aprakstīti parametri, kas kontrolē Izmaksu pārvaldības vispārējo darbību.

## <a name="general"></a>VispārīgI

| Lauks                                                    | Apraksts |
|----------------------------------------------------------|-------------|
| Nobraukuma standarta likme                                 | Ievadiet atlīdzināšanas likmi par nobraukuma izdevumiem. Šo likmi reizina ar nobraukumu, kas tiek ievadīts par izdevumiem, lai aprēķinātu summu, kas tiek atlīdzināta par ceļa izdevumiem. |
| Izdevumu mērķa validācija                                 | Ieslēdziet šo opciju, lai ierobežotu lietotājus ar esošu vērtību kopu, kas ir konfigurēta laukā **Izdevumu atskaites mērķis**, kad tie veido izdevumu atskaites. |
| Personiskie izdevumi, ko apmaksā                                | Atlasiet personu, kas atbildīga par visu to kredītkaršu darījumu summu apmaksu, kas klasificēti kā personiski. |
| Parādīt visu izdevumu atskaiti ar atgriešanu               | Atlasiet šo opciju, lai rādītu visus izdevumus izdevumu atskaitē, kad tiek skatīta sākotnējā dokumenta detalizētā informācija par konkrētu dokumentu, kas tika ģenerēts, grāmatojot izdevumu atskaiti. |
| Atļauja pirms ceļošanas ir obligāta                 | Atlasiet šo opciju, lai pieprasītu, ka, pirms darbinieks var iesniegt izdevumu atskaiti, tiek iesniegts un apstiprināts ceļojuma pieteikums. |
| Atļaut sadalījuma rediģēšanu pirms grāmatošanas            | Atlasiet, vai izdevumu atskaites sadalījumu var rediģēt pirms tā grāmatošanas. |
| Izvērtēt izdevumu pārvaldības politikas                     | Atlasiet šo opciju, kad izdevumi tiek izvērtēti, lai noteiktu, vai ir pārkāpta izdevumu politika. Izdevumus var izvērtēt saistībā ar pārkāpumiem, kad tiek ievadīti un saglabāti izmaksu ieraksti, vai arī brīdī, kad izdevumi tiek iesniegti apstiprināšanai. Politiku kārtulas par nepieciešamajiem čekiem tiek izvērtēti, kad tiek saglabāta izdevumu rinda. |
| Atļaut starpuzņēmumu izmaksu rindas                         | Atlasiet, vai izdevumu atskaitē var ievadīt citu juridisko personu izdevumus. |
| Atļaut rediģēt kredītkaršu izmaksu valūtas kursu | Atlasiet šo opciju, lai ļautu lietotājam rediģēt valūtas kursu importētajiem kredītkaršu izdevumiem. |
| Rādāmie vairāklīmeņu hierarhijas lauki                  | Atlasiet, kuri apstiprinātāja lauki tiek rādīti, kad darbplūsmas piešķiršanas tips ir iestatīts kā hierarhija, un atlase **Hierarhija** ir iestatīta tādējādi, lai izmantotu apstiprinājuma hierarhiju, izdevumu vairāklīmeņu apstiprināšanu. Ja darbplūsmai tiek izmantota vairāklīmeņu apstiprināšanas hierarhija, atlasītie lauki tiks rādīti izdevumu atskaitē un tos var rediģēt. |
| Ievadīt darbinieka kredītkartes numuru                        | Atlasiet, vai darbinieka lapā **Kredītkartes** laukā **Kartes ID** var ievadīt un saglabāt 15 rakstzīmju vai 16 rakstzīmju numuru. |
| Validēt ceļojuma pieteikuma mērķi                      | Ieslēdziet šo opciju, lai ierobežotu lietotājus ar esošu vērtību kopu, kas ir konfigurēta laukā **Izdevumu atskaites mērķis**, kad tie veido ceļojumu pieteikumus. |

## <a name="financial"></a>Izglītība

| Lauks                                                                                    | Apraksts |
|------------------------------------------------------------------------------------------|-------------|
| Virsgrāmatas dienas žurnāla nosaukums                                                                | Atlasiet tā virsgrāmatas žurnāla nosaukumu, kurā tiek grāmatotas apstiprinātās izdevumu atskaites. |
| Iespējot nodokļu atmaksu no izdevumiem                                                        | Atlasiet šo opciju, lai iespējotu izdevumu nodokļu atmaksu attaisnotajiem izdevumiem. Šo opciju nevar atlasīt, ja ir iespējoti ASV pārdošanas un ekspluatācijas nodokļu noteikumi. |
| Grāmatot naudas avansus uzreiz                                                           | Atlasiet šo opciju, lai grāmatotu apstiprinātu naudas avansu, kad ir pabeigts process Apmaksāt un pārsūtīt . Ja šī opcija nav atlasīta, process Apmaksāt un pārsūtīt ģenerē neiegrāmatotu virsgrāmatas žurnālu. |
| Labot uzskaites datumu grāmatošanas laikā                                                   | Atlasiet šo opciju, lai atjauninātu uzskaites datumu, kurā tiek grāmatoti izdevumi, ja pašreizējais periods ir aizturēts vai slēgts. Uzskaites datums tiks iestatīts uz nākamo atvērto periodu. |
| Atļaut darījumu grupēšanu, pamatojoties uz maksāšanas metodē norādīto ieskaita kontu       | Atlasiet šo opciju, lai apkopotu izmaksu darījumus no izdevumu atskaites, pamatojoties uz ieskaita kontu, kas ir norādīts izdevumu maksāšanas metodē. |
| Ar nodokli                                                                             | Atlasiet šo opciju, lai izmaksu summā pēc noklusējuma iekļautu pārdošanas nodokli. |
| Atbrīvot apgrūtinājumus, slēdzot ceļojumu pieteikumus                                      | Atlasiet šo opciju, lai atbrīvotu apgrūtinātos līdzekļus, kad tiek slēgts apstiprināts ceļojuma pieteikums. |
| Atļaut ceļojuma pieteikuma iesniegšanu ar budžeta reģistra un projekta budžeta pārsniegšanu | Atlasiet šo opciju, lai ļautu darbiniekiem iesniegt ceļojuma pieteikumus apstiprināšanai, kaut arī tie pārsniedz vai nu atļauto budžetu, kas noteikts budžeta reģistrā, vai projekta atļauto budžetu. |
| Atļaut izdevumu atskaites iesniegšanu ar budžeta reģistra un projekta budžeta pārsniegšanu     | Atlasiet šo opciju, lai ļautu darbiniekiem iesniegt izdevumu atskaites apstiprināšanai, kaut arī tās pārsniedz vai nu atļauto budžetu, kas noteikts budžeta reģistrā, vai projekta atļauto budžetu. |
| Atļaut izdevumu atskaites apstiprināšanu tikai ar budžeta reģistra pārsniegšanu                 | Atlasiet šo opciju, lai atļautu apstiprinātājiem apstiprināt izdevumu atskaites, kas pārsniedz budžeta reģistrā iestatīto atļauto budžetu. |

## <a name="per-diem"></a>Dienasnauda

| Lauks                                 | Apraksts |
|---------------------------------------|-------------|
| Minimālais stundu skaits dienasnaudai            | Ievadiet noklusējuma minimālo stundu skaitu, kas darbiniekam ir jānostrādā dienā, lai saņemtu dienasnaudu ar ceļojumiem saistītiem izdevumiem. Šo vērtību izmanto kā noklusējuma vērtību tikai attiecībā uz lauku **Minimālais stundu skaits** dienasnaudas likmju līmeņiem. |
| Maltīšu procentuālā daļa                          | Ievadiet dienasnaudas noklusējuma procentuālo vērtību maltītēm, ko izmanto ar ceļojumu saistīto izdevumu pirmajā un pēdējā dienā, kad lauks **Aprēķināt maltīšu samazināšanu par** ir iestatītas kā **Maltītes veids pēc dienas** vai **Maltīšu skaits dienā**. Pirmā un pēdējā darba dienā var būt īsāka nekā standarta darba diena. Tāpēc šajās dienās dienasnaudas summa var atšķirties no standarta summas. Ja procentuālā vērtība ir iestatīta uz **0** (nulli), ieturējumi pirmajā un pēdējā dienā būs 0,00. |
| Izmitināšanas procentuālā vērtība                         | Ievadiet dienasnaudas noklusējuma procentuālo vērtību, kas tiek izmantota ar ceļa izdevumiem saistīto izdevumu pirmajā un pēdējā dienā izmitināšanai. Pirmā un pēdējā darba dienā var būt īsāka nekā standarta darba diena. Tāpēc šajās dienās dienasnaudas summa var atšķirties no standarta summas. Ja procentuālā vērtība ir iestatīta uz **0** (nulli), ieturējumi pirmajā un pēdējā dienā būs 0,00. |
| Citu izdevumu procentuālā vērtība                         | Ievadiet dienasnaudas noklusējuma procentuālo vērtību, kas tiek izmantota ar ceļa izdevumiem saistīto izdevumu pirmajā un pēdējā dienā dažādiem izdevumiem. Pirmā un pēdējā darba dienā var būt īsāka nekā standarta darba diena. Tāpēc šajās dienās dienasnaudas summa var atšķirties no standarta summas. Ja procentuālā vērtība ir iestatīta uz **0** (nulli), ieturējumi pirmajā un pēdējā dienā būs 0,00. |
| Procentuālās vērtības samazinājums uz brokastu rēķina | Ievadiet summu, par kādu dienasnaudas summu samazina uz brokastu rēķina. Piemēram, ja darbinieks saņem bezmaksas brokastis, varat samazināt dienasnaudas summu par 10 procentiem. |
| Procentuālās vērtības samazinājums uz pusdienu rēķina     | Ievadiet summu, par kādu dienasnaudas summu samazina uz pusdienu rēķina. Piemēram, ja darbinieks saņem bezmaksas pusdienas, varat samazināt dienasnaudas summu par 15 procentiem. |
| Procentuālās vērtības samazinājums uz vakariņu rēķina    | Ievadiet summu, par kādu dienasnaudas summu samazina uz vakariņu rēķina. Piemēram, ja darbinieks saņem bezmaksas vakariņas, varat samazināt dienasnaudas summu par 25 procentiem. |
| Aprēķināt maltīšu izdevumu samazinājumu par           | Norādiet, kā sistēmai jāaprēķina dienasnaudas samazināšana uz maltīšu rēķina, atlasot, vai samazinājums ir atkarīgs no ēdienreizes veida vienam braucienam vai vienai dienai, vai atkarībā no dienā atļauto maltīšu skaita. |
| Dienasnaudas noapaļošana                     | Atlasiet noapaļošanas veidu, kas tiek izmantots dienasnaudas izdevumiem. Ja atlasāt parastu noapaļošanu, dienasnaudas izdevumu, kura summa ir 0,50, noapaļo uz augšu līdz 1,00, un jebkuru dienasnaudas izdevumu, kura summa ir mazāka par 0,50, noapaļo uz leju līdz 0,00. |
| Balstīt dienasnaudas aprēķinu uz          | Atlasiet, vai dienasnaudas summa ir atkarīga no kalendāra dienas vai 24 stundu perioda. |

## <a name="fax-cover-pages"></a>Faksa titullapas

| Lauks                          | Apraksts |
|--------------------------------|-------------|
| Norādījumi                   | Ievadiet norādījumus, kas darbiniekiem ir jāievēro, veidojot titullapu faksam, ko izmanto, lai nosūtītu ar izdevumu atskaiti saistītos čekus. Lai ievadītu rādāmo tekstu konkrētā valodā, pamatojoties uz lietotāja valodu, atlasiet vienumu **Tulkojumi**. |
| Lietotāja ID (svītrkoda +informācija) | Atlasiet šo opciju, lai saglabātu darbinieka unikālo identifikatoru svītrkodā, ko izmanto faksa titullapā. |
| Svītrkods                       | Atlasiet svītrkodu, ko izmanto faksa titullapā. Izdevumu pārvaldībā tiek atbalstīti svītrkodi 39 un 128. |

## <a name="anti-corruption"></a>Korupcijas apkarošana

| Lauks                                 | Apraksts |
|---------------------------------------|-------------|
| Parādīt apliecinājumu par korupcijas apkarošanu   | Atlasiet šo opciju, lai parādītu tekstu par korupcijas apkarošanu, kad tiek izveidota izdevumu atskaite. Var iespējot konkrētas izdevumu kategorijas, kuru gadījumā izdevumu atskaitē būtu obligātu jāatlasa apliecinājums par korupcijas apkarošanu. Piemēram, dāvanu kategorijai, kas saistīta ar valsts amatpersonu izdevumiem, var pieprasīt, lai darbinieks apstiprinātu, ka izdevumi atbilst uzņēmuma politikai saistībā ar valsts amatpersonām. |
| Paziņojums iesniedzējam par korupcijas apkarošanu | Ievadiet tekstu, kas jārāda darbiniekam, kurš veido izdevumu atskaiti. Lai ievadītu rādāmo tekstu konkrētā valodā, pamatojoties uz lietotāja valodu, atlasiet vienumu **Tulkojumi**. |
| Paziņojums apstiprinātājam par korupcijas apkarošanu  | Ievadiet tekstu, kas jārāda apstiprinātājam, kad tiek veidota izdevumu atskaite. Lai ievadītu rādāmo tekstu konkrētā valodā, pamatojoties uz lietotāja valodu, atlasiet vienumu **Tulkojumi**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]