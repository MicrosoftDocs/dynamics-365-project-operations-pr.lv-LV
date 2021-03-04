---
title: PVN atmaksa
description: Šajā tēmā ir paskaidrots, kā atgūt kompensācijas par pievienotās vērtības nodokļa (PVN) darījumiem.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49397592ea002b9da872ac1aa455719b6ca2292e
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960211"
---
# <a name="vat-recovery"></a>PVN atmaksa 

Lai saņemtu atmaksas par piemērotām pievienotās vērtības nodokļa (PVN) transakcijām, uzņēmumam vai organizācijai ir jāidentificē, jāapkopo, jāpārbauda un jāiesniedz precīza informācija. Šis process ietver vairākus uzdevumus, un atkarībā no uzņēmuma lieluma var ietvert vairākus darbiniekus vai lomas.

Lai atgūtu PVN, izmantojot izmaksu pārvaldību, jāizpilda šādi priekšnosacījumi:

- Nodokļu kodi ir jāizveido tām valstīm/reģioniem, kas ir piešķirti izdevumu kategorijām.
- Katram nodokļu kodam ir jāizveido PVN grupa.
- Katrai PVN grupai ir jāizveido krājumu PVN kods.

Kad priekšnosacījumi ir izpildīti, darbinieki veic šīs darbības, lai pieprasītu atmaksājumus par PVN transakcijām.

1. Izdevumu atskaitē ievadiet nodokļu informāciju par kredītkaršu transakcijām, lai norādītu piemērotas PVN atmaksas.
2. Pārliecinieties, vai ir ievadīta visa nodokļu informācija, un pēc tam grāmatojiet izdevumu atskaiti.
3. Apstrādājiet izdevumus, kas ir piemēroti starptautiskajai PVN atmaksai.
4. Nosūtiet PVN atmaksas datus trešās puses piegādātājam, lai iesniegtu starptautiskās atmaksas deklarācijas.
5. Apstrādājiet izdevumus vietējai PVN atmaksai.

Tālāk esošajās sadaļās ir sniegti piemēri, kas parāda, kā Contoso darbinieki izpilda katru darbību.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Izdevumu atskaitē ievadiet nodokļu informāciju par kredītkaršu transakcijām, lai norādītu piemērotas PVN atmaksas

Rūta, Contoso pārdošanas pārstāve ASV, nesen atgriezās no pārdošanas ceļojuma uz Apvienoto Karalisti. Ceļojuma laikā viņai radās daži personīgās kredītkartes izdevumi maltītēm. Rūtai tagad ir jāizveido izdevumu atskaite, lai saskaņotu savus izdevumus.

Kad Rūta ievada informāciju savā izdevumu atskaitē, viņa lapas **Rediģēt izdevumu atskaiti** laukā **Valsts/reģions** atlasa **Apvienotā Karaliste**. Pēc tam PVN grupu saraksts tiek filtrēts tā, lai tajā tiktu rādītas tikai grupas, kas attiecas uz Apvienoto Karalisti. Rūta atlasa PVN grupu **Apvienotā Karaliste 001** un pēc tam atlasa krājumu PVN grupu **Maltītes**. Pēc tam viņa pievieno jaunu transakciju par naktsmītni. Tā kā par naktsmītni Apvienotajā Karalistē ir tikai viena PVN grupa un krājumu PVN grupa, šī informācija tiek automātiski aizpildīta Rūtas izdevumu pārskatā.

Saskaņā ar Contoso politiku visiem izdevumiem ir jābūt atbilstošai kvītij. Tāpēc, kad Rūta saglabā savu izdevumu atskaiti, viņa saņem ziņojumu par to, ka viņai ir jāpievieno kvīts par katru izdevumu atskaitē uzskaitīto transakciju. Rūta pārbauda, vai viņa izdevumu atskaitē ir pievienojusi katras transakcijas kvīts digitālo attēlu, un pēc tam iesniedz atskaiti apstiprināšanai. Pēc tam viņa nosūta papīra kvītis vadības apstrādes darba grupai. Šī darba grupa nosūtīs PVN atmaksas datus trešās puses piegādātājam, kas iesniedz Contoso starptautiskās PVN atmaksas deklarācijas.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Pārliecinieties, vai ir ievadīta visa nodokļu informācija, un pēc tam grāmatojiet izdevumu atskaiti

Pirms Ieva, Contoso kreditoru koordinatore, var grāmatot izdevumu atskaiti, viņai ir jāievada tajā trūkstošā nodokļu informācija. Viņa atver lapu **Izdevumu atskaites informācija** un redz Rūtas apstiprināto izdevumu atskaiti. Pēc tam Ieva atver izdevumu atskaiti, lai skatītu informāciju par transakcijām. Viņa redz, ka Rūta nav ievadījusi krājumu PVN grupu vienai no transakcijām. Tā kā šī informācija nav sniegta, Ievas nevar grāmatot izdevumu atskaiti. Tāpēc Ieva modulī Izdevumu pārvaldība apskata lapu **Nodokļu konfigurācijas** un atrod atbilstošo krājumu PVN grupu valstij/reģionam un transakcijas tipam. Tagad Ieva var grāmatot izdevumu atskaiti virsgrāmatā.

Kad Ieva iegrāmato izdevumu atskaiti, tiek izveidots PVN atmaksas darba elements. Šis darba elements tiek piešķirts vadības apstrādes darba grupas dalībniekam. Ieva saņem ziņojumu, kas apstiprina, ka grāmatošana ir veiksmīga. Šajā ziņojumā ir norādīts arī to PVN transakciju skaits, kas tika identificētas atmaksai.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>To izdevumu apstrāde, kas ir piemēroti starptautiskajai PVN atmaksai

Arnis, Contoso vadības apstrādes darba grupas dalībnieks, ir atbildīgs par to, lai apstiprinātu, vai izdevumu atskaitēs ir sniegta visa nepieciešamā informācija PVN atmaksai. Viņš atver lapu **Izdevumu nodokļu atmaksa** un atlasa Rūtas iesniegto izdevumu atskaiti. Arnis pārbauda, vai ir pievienotas visas nepieciešamās kvītis un vai ir ievadīti pareizie PVN grupas un krājumu PVN kodi.

Kad Arnis saņem papīra kvītis no Rūtas, viņš papīra kvītis salīdzina ar digitālajām kvītīm un pēc tam maina izdevumu pārskata statusu uz **Gatavs atmaksai**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>PVN atmaksas datu sūtīšana trešās puses piegādātājam, lai iesniegtu starptautiskās atmaksas deklarācijas

Kad Arnis ir gatavs nosūtīt izdevumu atskaites datus trešās puses piegādātājam, kas iesniegs PVN atmaksas deklarācijas, viņš atver lapu **Izdevumu nodokļu atmaksa**. Viņš filtrē lapu, lai tajā būtu redzamas tikai izdevumu atskaites, kas atzīmētas kā **Gatava atmaksai**. Pēc tam Arnis atlasa **Fails** &gt; **Eksportēt uz Excel**. Izdevumu atskaišu PVN informācija tiek eksportēta uz Microsoft Excel darblapu. Arnis šo darblapu iesniedz trešās puses piegādātājam un pievieno ziņojumu par to, ka papīra kvītis ir nosūtītas ar kurjeru.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Izdevumu apstrāde vietējai PVN atmaksai

Arnim ir jāpārbauda, vai izdevumu atskaites transakcijas ir piemērotas PVN atmaksai un vai atskaitēm ir pievienotas digitālās kvītis. Lai sāktu apstrādāt attaisnotos izdevumus vietējai atmaksai, Arnis atver lapu **Izdevumu nodokļu atmaksa** un atlasa izdevumu atskaiti, kam nepieciešama pārbaude. Viņš pārbauda, vai kvītis ir izsniegtas uz uzņēmumu, nevis darbinieku. PVN atgūšanai ieņēmumiem ir jābūt uzņēmuma vārdā. Arnis pēc tam apstiprina, ka ir lietots pareizais PVN grupas un krājumu PVN kods.

Kad Arnis saņem papīra kvītis, viņš maina izdevumu atskaites statusu uz **Gatava atmaksai**. Tagad viņš var iesniegt deklarāciju atbilstošajai nodokļu iestādei. Šajā gadījumā atbilstošā nodokļu iestāde ASV ir Iekšējais ieņēmumu dienests (IID).
