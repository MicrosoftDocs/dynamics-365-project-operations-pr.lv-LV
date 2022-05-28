---
title: Izdevumu pārvaldības konfigurēšana
description: Šajā rakstā ir aprakstīti apsvērumi un lēmumi, kas jāpieņem plānošanas procesā pirms izdevumu pārvaldības konfigurēšanas programmā Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d919a26000b127dd6fb2fd8a49d79e3087f1c403
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710127"
---
# <a name="configure-expense-management"></a>Izdevumu pārvaldības konfigurēšana

Šajā tēmā ir aprakstīti apsvērumi un lēmumi, kas ir jāpieņem plānošanas procesa laikā pirms izdevumu pārvaldības konfigurēšanas. Izdevumu pārvaldībā var glabāt informāciju par maksājuma metodēm, ceļa pieprasījumiem, izdevumu atskaitēm, politikām un citu informāciju.

Tā kā daudzi no jūsu pieņemtajiem lēmumiem attiecībā uz izdevumu pārvaldības konfigurācijas plānošanu ir balstīti uz jūsu organizācijas hierarhiju un finanšu struktūru, ir jāatsaucas uz šo apgabalu plānošanas dokumentiem.

## <a name="intercompany-expenses"></a>Starpuzņēmumu izdevumi

Iespējojot starpuzņēmumu izdevumus, juridiskās personas un darbinieki tiek pilnvaroti apmaksāt izdevumus citas juridiskas personas vārdā, kā arī iekasēt samaksu no juridiskās entītijas, kas nodarbināta jūsu organizācijā. Piemēram, darbinieks juridiskajā entītijā A izpilda projektu juridiskajai personai B, un projektam rodas ar ceļojumiem saistīti izdevumi. Ja ir iespējotas starpuzņēmumu izmaksas, darbinieks pēc tam var iesniegt izdevumu atskaiti, kurā tiks grāmatoti izdevumi juridiskajai personai B, un juridiskajai personai A ir jāapmaksā izdevumi. Ja organizācijā nav vairāku juridisku entītiju, starpuzņēmumu izdevumi nav jāiespējo.

**Lēmums:**  vai vēlaties iespējot starpuzņēmumu izdevumus?

## <a name="financial-management"></a>Finanšu pārvaldība

Izdevumu pārvaldība ir cieši integrēta organizācijas finanšu pārvaldībā. Daudz jūsu izdevumu pārvaldības konfigurēšanas pamatā būs lēmumi, ko esat pieņēmis saistībā ar jūsu organizācijas finansēm. Tālāk esošajās sadaļās ir aprakstīti dažādi apgabali, kuros ir nepieciešama plānošana un lēmumi, pamatojoties uz jūsu organizācijas finanšu lēmumiem un vadlīnijām no jūsu vadības darba grupas.

### <a name="per-diems"></a>Dienasnauda

Jums ir jādefinē darbinieku dienasnauda, ko nodrošina jūsu organizācija. Tā kā dienasnauda parasti tiek izmantota, lai segtu izdevumus, piemēram, ēdināšanu, naktsmītnes un citus papildu izdevumus, varat izveidot kārtulas jūsu organizācijas piedāvātajām dienasnaudas summām. Dienasnaudas likmes var būt atkarīgas no gada laika, ceļojuma galamērķa vai abiem. Kad definējat dienasnaudas kārtulu, varat norādīt, ka noteikta procentuālā dienasnaudas likme tiek ieturēta, ja darbinieks saņem bezmaksas maltītes vai pakalpojumus. Varat definēt arī dienasnaudas likmju līmeņus, lai iestatītu minimālo un maksimālo stundu skaitu, kam var piemērot darba ņēmēja komandējuma dienasnaudas likmi.

**Lēmumi:**

- Dienasnaudas noklusējuma kārtulas pirmajai un pēdējai dienai:

    - Kāds ir minimālais stundu skaits, ko darbinieks var pieprasīt par dienu un joprojām saņemt dienasnaudu?
    - Vai ir samazināta summa, kas tiek piedāvāta par ēdienu pirmajai un pēdējai dienai? Ja ir samazinājums, kāda ir samazinājuma procentuālā daļa?
    - Vai ir samazināta summa, kas tiek piedāvāta par viesnīcu pirmajai un pēdējai dienai? Ja ir samazinājums, kāda ir samazinājuma procentuālā daļa?
    - Vai ir samazināta summa, kas tiek piedāvāta par citiem izdevumiem pirmajā un pēdējā dienā? Ja ir samazinājums, kāda ir samazinājuma procentuālā daļa?

- Dienasnaudas noklusējuma kārtulas:

    - Vai dienasnauda tiek procentuāli samazināta par katru maltīti, ja, piemēram, maltīte ir bez maksas? Ja ir samazinājums, kāda ir samazinājuma procentuālā daļa par katru maltīti?
    - Vai maltītes samazinājums ir aprēķināts dienā, ceļojumā vai pēc ēdienreižu skaita dienā?
    - Vai dienasnaudas summas ir jānoapaļo parastā veidā vai jānoapaļo uz augšu?
    - Vai dienasnauda tiek aprēķināta 24 stundu periodā vai kalendārajā dienā?

- Dienasnaudas kārtulas, kuru pamatā ir atrašanās vieta:

    - Vai dienas naudas likmes mainās atkarībā no atrašanās vietas? Kādas atrašanās vietas ir iekļautas?
    - Ja dienasnaudas likmes ir atkarīgas no atrašanās vietas, kāda procentuālā summa katrai atrašanās vietai tiek nodrošināta tālāk minētajiem izdevumu veidiem.

        - Maltītes
        - Viesnīca
        - Citi izdevumi

### <a name="expense-management-journals-and-accounts"></a>Izdevumu pārvaldības žurnāli un konti

Izmaksu pārvaldībai ir nepieciešams lietot vairākus žurnālus un kontus. Jums ir jāizlemj, piemēram, vai tas naudas avansiem un kredītkaršu strīdiem tiek izmantots viens konts.

**Lēmumi:**

- Kurā virsgrāmatas žurnālā tiek grāmatotas apstiprinātās izdevumu atskaites?
- Kurš konts tiek izmantots naudas avansiem?
- Vai naudas avansi ir jāgrāmato nekavējoties?

### <a name="payment-methods"></a>Maksāšanas metodes

Ja ļaujat darbiniekiem jūsu uzņēmuma vārdā apmaksāt izdevumus, jums ir jādefinē maksājuma metodes, kuras darbiniekiem ir atļauts lietot. Piemēram, varat atļaut darbiniekiem izmantot skaidru naudu vai uzņēmuma kredītkarti. Varat arī atļaut darbiniekiem izmantot personiskās kredītkartes un pēc tam atlīdzināt izdevumus darbiniekiem. Ir jāpieņem šādi lēmumi attiecībā uz katru atļauto maksāšanas metodi.

**Lēmumi:**

- Kādas maksāšanas metodes ir atļautas?
- Kam pieder maksājuma metodes izdevumi?
- Vai ir nobīdes konta tips? Ja ir nobīdes konta tips, kas tas ir?
- Ja ir nobīdes konta tips, kāds ir konts?
- Ja maksāšanas metode ir kredītkarte, vai maksāšanas metode ir jāizmanto tikai ar importētajiem darījumiem?

### <a name="expense-categories-and-shared-categories"></a>Izdevumu kategorijas un koplietotās kategorijas

Kad darbinieki veido izdevumu atskaiti, katram reģistrētajam izdevumu ierakstam ir jābūt saistītam ar izdevumu kategoriju. Izdevumu kategorijas ir atvasinātas no kopīgotām kategorijām, kuras var kopīgot organizācijas juridiskajās personās. Šīs kategorijas var arī kopīgot projektu vadībā un grāmatvedībā atkarībā no organizācijas definēšanas veida. Pamatojoties uz jūsu organizācijas definīciju un ieviešanas darba grupas vadlīnijām, ir jānosaka, vai modulī Izdevumu pārvaldība lietotās kategorijas tiks izmantotas tikai modulī Izmaksu pārvaldība vai arī tās būtu nepieciešams kopīgot moduļos Projektu vadība un grāmatvedība un Izdevumu pārvaldība. Ņemiet vērā, ka šīs kategorijas var koplietot projektā un izdevumos vai projektā un ražošanā, bet ne izdevumos un ražošanā. Attiecībā uz katru izdevumu kategoriju ir jāpieņem tālāk minētie lēmumi.

**Lēmumi:**

- Kas ir izdevumu kategorija? Var būt tādas kategorijas kā lidojumi, viesnīca vai nobraukums.
- Vai izdevumu kategoriju var izmantot arī projektu pārvaldībā un grāmatvedībā?
- Kāds ir izdevumu tips?
- Kāda ir izdevumu kategorijas noklusējuma maksāšanas metode?
- Vai izdevumu kategorijas izdevumi ir jāuzskaita?
- Kas ir izdevumu kategorijas galvenais noklusējuma konts?
- Kas ir izdevumu kategorijas noklusējuma krājumu PVN grupa?
- Vai izdevumu kategorijai ir atļautas papildu maksāšanas metodes? Ja ir atļautas papildu maksāšanas metodes, kādas tās ir?
- Vai šajā izdevumu kategorijā ir apakškategorijas? Ja ir apakškategorijas, jums ir jāpieņem arī šādi lēmumi:

    - Vai jebkura no apakškategorijām ir izslēgta no nodokļu atmaksas?
    - Kas ir apakškategoriju krājumu PVN grupa?

Ja izdevumu kategorija tiek izmantota arī projektu vadībā un grāmatvedībā, atbildiet uz atlikušajiem jautājumiem. Pretējā gadījumā pārejiet uz nākamo sadaļu.

- Kuri izmaksu konti tiks izmantoti tālāk norādītajiem izdevumiem?

    - izdevumi
    - Algu sadalījums
    - WIP-izmaksu vērtība
    - Izmaksas-elements
    - WIP-izmaksu vērtība-elements
    - Uzkrātie zaudējumi
    - WIP-uzkrātie zaudējumi

- Kuri ieņēmumu konti tiks izmantoti tālāk norādītajiem vienumiem?

    - Ieņēmumi, par ko izrakstīts rēķins
    - Uzkrāto ieņēmumu-pārdošanas vērtība
    - WIP-pārdošanas vērtība
    - Uzkrātie ieņēmumi-ražošana
    - WIP-ražošana
    - Uzkrātie ieņēmumi-peļņa
    - WIP-peļņa
    - Uzkrātie ieņēmumi-abonēšana
    - WIP-abonēšana

### <a name="taxes"></a>Nodokļi

Ar izdevumiem saistītos nodokļus ir jānosaka, kas ir iekļauts vai iespējots izdevumu atskaitēs.

**Lēmumi:**

- Vai pārdošanas nodoklis ir iekļauts izdevumu summās?
- Vai nodokļu atgūšana ir iespējota izdevumiem?

    > [!NOTE]
    > Ja plānojat virsgrāmatu un esat nolēmis lietot ASV pārdošanas nodokli un izmantot nodokļu kārtulas, nevarat iespējot nodokļu atmaksāšanu izdevumiem. (Lai lietotu ASV pārdošanas nodokli un izmantotu nodokļu kārtulas, opciju **Lietot pārdošanas nodokļu kārtulu** iestatiet uz **Jā**.)

## <a name="policies"></a>Politikas

Izveidojot izdevumu atskaišu politikas, varat palīdzēt organizācijai ietaupīt laiku un naudu, kad darbinieki apmaksā izdevumus organizācijas vārdā. Politikas palīdz nodrošināt, ka darbinieki ievēro budžetu, sniedz visu nepieciešamo informāciju un tērē naudu tikai tad, kad nepieciešams. Ir jāpieņem tālāk norādītie lēmumi attiecībā uz katru izdevumu atskaites politiku un katru izveidoto izmaksu atskaišu apstiprināšanas politiku.

**Lēmumi:**

- Kāds ir politikas nosaukums?
- Kam ir paredzēta izdevumu politika?
- Ja iepriekš esat nolēmis iespējot starpuzņēmumu izdevumus, uz kādiem uzņēmumiem jūsu organizācijā attieksies šī politika?
- Kad politika stājas spēkā?
- Kad beidzas politikas termiņš?
- Kāda ir politikas kārtula?
- Kāds ir politikas kārtulas rezultāts?


[!INCLUDE[footer-include](../includes/footer-banner.md)]