---
title: PVN atmaksa modulī Izdevumu pārvaldība
description: Šajā rakstā paskaidrots, kā saņemt atmaksu par attiecināmiem pievienotās vērtības nodokļa (PVN) darījumiem.
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 1df921bbef4c11c7e07ed38775644117215a50fb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927935"
---
# <a name="vat-recovery-in-expense-management"></a>PVN atmaksa modulī Izdevumu pārvaldība

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Lai saņemtu atmaksas par piemērotām pievienotās vērtības nodokļa (PVN) transakcijām, uzņēmumam vai organizācijai ir jāidentificē, jāapkopo, jāpārbauda un jāiesniedz precīza informācija. Šis process ietver vairākus uzdevumus, un atkarībā no uzņēmuma lieluma var ietvert vairākus darbiniekus vai lomas.

Lai modulī **Izdevumu pārvaldība** atgūtu PVN, ir jābūt izpildītiem šādiem priekšnosacījumiem:

- Nodokļu kodi ir jāizveido tām valstīm/reģioniem, kas ir piešķirti izdevumu kategorijām.
- Katram nodokļu kodam ir jāizveido PVN grupa.
- Katrai PVN grupai ir jāizveido krājumu PVN kods.

Pēc priekšnosacījumu izpildes ir jāveic tālāk norādītās darbības, lai pieprasītu atmaksas par PVN transakcijām.

1. Izdevumu atskaitē ievadiet nodokļu informāciju par kredītkaršu transakcijām, lai norādītu piemērotas PVN atmaksas.
2. Pārbaudiet, vai ir ievadīta visa nodokļu informācija, un pēc tam grāmatojiet izdevumu atskaiti.
3. Apstrādājiet izdevumus, kas ir piemēroti starptautiskajai PVN atmaksai.
4. Nosūtiet PVN atmaksas datus trešās puses piegādātājam, lai iesniegtu starptautiskās atmaksas deklarācijas.
5. Apstrādājiet izdevumus vietējai PVN atmaksai.

Tālāk esošajās sadaļās ir sniegti piemēri, kas parāda, kā Contoso darbinieki izpilda katru darbību.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Nodokļu informācijas ievadīšana par kredītkaršu transakcijām, lai norādītu piemērotas PVN atmaksas

Rūta, Contoso pārdošanas pārstāve Amerikas Savienotajās valstīs, nesen atgriezās no pārdošanas ceļojuma uz Apvienoto Karalisti. Ceļojuma laikā Rūtai radās daži personīgie kredītkartes izdevumi par maltītēm. Rūtai tagad ir jāizveido izdevumu atskaite, lai saskaņotu izdevumus.

Kad Rūta ievada informāciju izdevumu atskaitē, viņa lapas **Rediģēt izdevumu atskaiti** laukā **Valsts/reģions** atlasa **Apvienotā Karaliste**. Pēc tam PVN grupu saraksts tiek filtrēts tā, lai tajā tiktu rādītas tikai grupas, kas attiecas uz Apvienoto Karalisti. Rūta atlasa PVN grupu **Apvienotā Karaliste 001** un pēc tam atlasa krājumu PVN grupu **Maltītes**. Pēc tam Rūta pievieno jaunu transakciju par naktsmītni. Tā kā naktsmītnēm Apvienotajā Karalistē ir tikai viena PVN grupa un viena krājumu PVN grupa, šī informācija tiek automātiski aizpildīta Rūtas izdevumu atskaitē.

Saskaņā ar Contoso politiku visiem izdevumiem ir jābūt atbilstošai kvītij. Tāpēc, kad Rūta saglabā izdevumu atskaiti, viņa saņem ziņojumu par to, ka viņai ir jāpievieno kvīts par katru viņas izdevumu atskaitē uzskaitīto transakciju. Rūta pārbauda, vai viņa izdevumu atskaitē ir pievienojusi katras transakcijas kvīts digitālo attēlu, un pēc tam iesniedz atskaiti apstiprināšanai. Pēc tam viņa nosūta papīra kvītis vadības apstrādes darba grupai. Šī darba grupa nosūtīs PVN atmaksas datus trešās puses piegādātājam, kas iesniedz Contoso starptautiskās PVN atmaksas deklarācijas.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Nodokļu informācijas pārbaude un izdevumu atskaites grāmatošana

Pirms Ieva, Contoso kreditoru koordinatore, var grāmatot izdevumu atskaiti, viņai ir jāievada tajā trūkstošā nodokļu informācija. Viņa atver lapu **Izdevumu atskaites informācija** un redz Rūtas apstiprināto izdevumu atskaiti. Pēc tam Ieva atver izdevumu atskaiti, lai skatītu informāciju par transakcijām. Viņa redz, ka Rūta nav ievadījusi krājumu PVN grupu vienai no transakcijām. Tā kā šī informācija nav sniegta, Ievas nevar grāmatot izdevumu atskaiti. Tāpēc viņa modulī Izdevumu pārvaldība apskata lapu **Nodokļu konfigurācijas** un atrod atbilstošo krājumu PVN grupu valstij/reģionam un transakcijas tipam. Tagad Ieva var grāmatot izdevumu atskaiti virsgrāmatā.

Kad Ieva iegrāmato izdevumu atskaiti, tiek izveidots PVN atmaksas darba elements. Šis darba elements tiek piešķirts vadības apstrādes darba grupas dalībniekam. Ieva saņem ziņojumu, kas apstiprina, ka grāmatošana ir veiksmīga. Šajā ziņojumā ir norādīts arī to PVN transakciju skaits, kas tika identificētas atmaksai.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>To izdevumu apstrāde, kas ir piemēroti starptautiskajai PVN atmaksai

Arnis, Contoso vadības apstrādes darba grupas dalībnieks, ir atbildīgs par to, lai pārbaudītu, vai izdevumu atskaitēs ir sniegta visa nepieciešamā informācija PVN atmaksai. Viņš atver lapu **Izdevumu nodokļu atmaksa** un atlasa Rūtas iesniegto izdevumu atskaiti. Pēc tam Arnis pārbauda, vai ir pievienotas visas nepieciešamās kvītis vai ir ievadīti pareizie PVN grupas un krājumu PVN kodi.

Kad Arnis saņem papīra kvītis no Rūtas, viņš tās salīdzina ar digitālajām kvītīm un pēc tam maina izdevumu atskaites statusu uz **Gatava atmaksai**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>PVN atmaksas datu nosūtīšana trešās puses piegādātājam

Kad Arnis ir gatavs nosūtīt izdevumu atskaites datus trešās puses piegādātājam, kas iesniegs PVN atmaksas deklarācijas, viņš atver lapu **Izdevumu nodokļu atmaksa**. Viņš filtrē lapu, lai tajā būtu redzamas tikai izdevumu atskaites, kas atzīmētas kā **Gatava atmaksai**. Pēc tam Arnis atlasa **Fails** &gt; **Eksportēt uz Excel**. Izdevumu atskaišu PVN informācija tiek eksportēta uz Microsoft Excel darblapu. Arnis šo darblapu iesniedz trešās puses piegādātājam un pievieno ziņojumu par to, ka papīra kvītis ir nosūtītas ar kurjeru.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Izdevumu apstrāde vietējai PVN atmaksai

Arnim ir jāpārbauda, vai izdevumu atskaites transakcijas ir piemērotas PVN atmaksai un vai atskaitēm ir pievienotas digitālās kvītis. Lai sāktu apstrādāt attaisnotos izdevumus vietējai atmaksai, Arnis atver lapu **Izdevumu nodokļu atmaksa** un atlasa izdevumu atskaiti, kam nepieciešama pārbaude. Viņš pārbauda, vai kvītis ir izsniegtas uz uzņēmumu, nevis darbinieku. (Lai saņemtu PVN atmaksu, kvītīm ir jābūt izsniegtām uz uzņēmumu.) Pēc tam Arnis pārbauda, vai ir ievadīti pareizie PVN grupas un krājumu PVN kodi.

Kad Arnis saņem papīra kvītis, viņš maina izdevumu atskaites statusu uz **Gatava atmaksai**. Tagad viņš var iesniegt deklarāciju atbilstošajai nodokļu iestādei. Šajā gadījumā atbilstošā nodokļu iestāde Amerikas Savienotajās valstīs ir Iekšējais ieņēmumu dienests (IID).


[!INCLUDE[footer-include](../includes/footer-banner.md)]