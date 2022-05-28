---
title: Piedāvājuma rindas apmaksājamo komponentu konfigurēšana
description: Šajā tēmā ir sniegta informācija par apmaksājamu un neapmaksājamu komponentu iestatīšanu projekta piedāvājuma rindā.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3c9bd23f4e78e3ea5ae8f74ff1a4829a11f91929
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598405"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Piedāvājuma rindas maksas komponentu konfigurēšana 

_**Attiecas uz:** Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu, Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem_

Projekta piedāvājuma rindā ir *iekļauti* komponenti un *apmaksājami* komponenti.

Uz iekļautajiem komponentiem attiecas tālāk norādītais.

  - Norēķinu metode un klientu sadalījums
  - Nepārsniedzamie ierobežojumi 
  - Rēķina izrakstīšanas biežuma iestatījumi, kas definēti projekta piedāvājuma rindā

Iekļauto komponentu apakškopu var atzīmēt kā apmaksājamu, izmantojot lauku **Norēķinu tips**. Lauks **Norēķinu tips** ir opciju kopa, kas piedāvājuma rindas kontekstā ļauj izmantot šādas vērtības:

  - Izrakstāms rēķins
  - Nav iekļaujams rēķinā

Apmaksājamus komponentus var definēt uzdevumos, lomās un darījumu kategorijās.

Iekļaujamība rēķinā tiek definēta par piedāvājuma rindu un tā attiecas uz visām rindā iekļautajām darījumu klasēm. Ja lauks **Iekļaut uzdevumus** ir tukšs vai iestatīts uz **Viss projekts**, cilne **Apmaksājamie uzdevumi** nav pieejama.

Iekļaujamību rēķinā definē lomām piedāvājuma rindai, un tā attiecas tikai uz darījumu klasi **Laiks**. Ja lauks **Iekļaut laiku** projekta piedāvājuma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās lomas** nav pieejama.

Apmaksas apjoms tiek definēts pēc darījumu kategorijām piedāvājuma rindai, un tas attiecas tikai uz darījumu klasi **Izdevumi**. Ja lauks **Iekļaut izdevumus** projekta piedāvājuma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās kategorijas** nav pieejama.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Projekta uzdevuma atjaunināšana par apmaksājamu vai neapmaksājamu

Projekta uzdevums var būt apmaksājams vai neapmaksājam noteiktā projekta piedāvājuma rindā, kas nodrošina šādas iestatīšanas iespējas.

Ja projekta piedāvājuma rindā ir iekļauts **Laiks** un uzdevums **T1**, uzdevums tiek saistīts ar piedāvājuma rindu kā apmaksājams. Ja ir otra piedāvājuma rinda, kurā ir iekļautas lauks **Izmaksas**, varat saistīt **T1** uzdevumu piedāvājuma rindā kā neapmaksājamu. Rezultāts ir tāds, ka viss šajā uzdevumā reģistrētais laiks ir apmaksājams, un visi izdevumi uzdevumā ir neapmaksājami.

Uzdevuma norēķinu tipu var konfigurēt projekta piedāvājuma rindas cilnē **Rēķinā iekļaujamie uzdevumi**, atjauninot lauku **Norēķinu tips** apakšrežģī **Piedāvājuma rindas uzdevumi**. Vai arī varat atjaunināt projekta uzdevuma norēķinu veida lauku **Norēķinu tips** projekta norēķinu iestatījumu apakšrežģī, kas rāda ar uzdevumu saistītās piedāvājuma rindas.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Lomas atjaunināšana par apmaksājamu vai neapmaksājamu

Loma var būt apmaksājama vai neapmaksājama noteiktas projekta piedāvājuma rindas kontekstā.

Lomas norēķinu tipu var konfigurēt piedāvājuma rindas cilnē **Rēķinā iekļaujamās lomas**, atjauninot lauku **Norēķinu tips** apakšrežģī **Rēķinā iekļaujamās lomas**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu

Darījumu kategorija var būt apmaksājama vai neapmaksājama noteiktā piedāvājuma rindā.

Transakcijas norēķinu tipu var konfigurēt piedāvājuma rindas cilnē **Rēķinā iekļaujamās kategorijas**, atjauninot lauku **Norēķinu tips** apakšrežģī **Rēķinā iekļaujamās kategorijas**.

### <a name="resolve-chargeability"></a>Apmaksājamības atrisināšana
Laika novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.

   - **Laiks** ir iekļauts piedāvājuma rindā.
   - **Loma** piedāvājuma rindā ir konfigurēta kā apmaksājama.
   - **Iekļautie uzdevumi** piedāvājuma rindā ir iestatīti uz **Atlasītie uzdevumi**. 

Ja šie trīs nosacījumi ir izpildīti, **Uzdevums** arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu. 

Izdevumu novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos. 

   - **Izdevumi** ir iekļauti piedāvājuma rindā.
   - **Transakcijas kategorija** piedāvājuma rindā ir konfigurēta kā apmaksājama.
   - **Iekļautie uzdevumi** piedāvājuma rindā ir iestatīti uz **Atlasītie uzdevumi**.

Ja šie trīs nosacījumi ir izpildīti, **Uzdevums** arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu. 

Materiālu novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.

   - **Materiāli** ir iekļauti piedāvājuma rindā.
   - **Iekļautie uzdevumi** piedāvājuma rindā ir iestatīti uz **Atlasītie uzdevumi**.

Ja šie divi nosacījumi ir izpildīti, **Uzdevums** tiek konfigurēts kā tāds, par kuru var iekasēt maksu. 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Iekļauts laiks</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Iekļauti izdevumi</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Iekļauti materiāli</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Iekļautie uzdevumi</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Loma</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategorija</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Uzdevums</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Iekasēšanas ietekme</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jā </p>
            </td>
            <td width="78" valign="top">
                <p>
Jā </p>
            </td>
            <td width="63" valign="top">
                <p>
Jā </p>
            </td>
            <td width="75" valign="top">
                <p>
Viss projekts </p>
            </td>
            <td width="65" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="70" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="65" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="350" valign="top">
                <p>
Norēķini par laika faktiskajiem datiem: Apmaksājams </p>
                <p>
Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams </p>
                <p>
Rēķina tips faktiskajām materiālu vērtībām: iekasējams </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jā </p>
            </td>
            <td width="78" valign="top">
                <p>
Jā </p>
            </td>
            <td width="63" valign="top">
                <p>
Jā </p>
            </td>
            <td width="75" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="65" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="70" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="65" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="350" valign="top">
                <p>
Norēķini par laika faktiskajiem datiem: Apmaksājams </p>
                <p>
Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams </p>
                <p>
Rēķina tips faktiskajām materiālu vērtībām: iekasējams </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jā </p>
            </td>
            <td width="78" valign="top">
                <p>
Jā </p>
            </td>
            <td width="63" valign="top">
                <p>
Jā </p>
            </td>
            <td width="75" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nav iekasējams</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="65" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="350" valign="top">
                <p>
Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams </p>
                <p>
Rēķina tips faktiskajām materiālu vērtībām: iekasējams </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jā </p>
            </td>
            <td width="78" valign="top">
                <p>
Jā </p>
            </td>
            <td width="63" valign="top">
                <p>
Jā </p>
            </td>
            <td width="75" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="65" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="70" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nav iekasējams</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Rēķina tips materiālu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jā </p>
            </td>
            <td width="78" valign="top">
                <p>
Jā </p>
            </td>
            <td width="63" valign="top">
                <p>
Jā </p>
            </td>
            <td width="75" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nav iekasējams</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nav iekasējams</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Rēķina tips materiālu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jā </p>
            </td>
            <td width="78" valign="top">
                <p>
Jā </p>
            </td>
            <td width="63" valign="top">
                <p>
Jā </p>
            </td>
            <td width="75" valign="top">
                <p>
Tikai atlasītie uzdevumi </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nav iekasējams</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nav iekasējams</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="350" valign="top">
                <p>
Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Rēķina tips faktiskajām materiālu vērtībām: iekasējams </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Jā </p>
            </td>
            <td width="63" valign="top">
                <p>
Jā </p>
            </td>
            <td width="75" valign="top">
                <p>
Viss projekts </p>
            </td>
            <td width="65" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Izrakstāms rēķins</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="350" valign="top">
                <p>
Rēķins ar laika faktiskajām vērtībām: <strong>Nav pieejams</strong>
                </p>
                <p>
Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams </p>
                <p>
Rēķina tips faktiskajām materiālu vērtībām: iekasējams </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Jā </p>
            </td>
            <td width="63" valign="top">
                <p>
Jā </p>
            </td>
            <td width="75" valign="top">
                <p>
Viss projekts </p>
            </td>
            <td width="65" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nav iekasējams</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="350" valign="top">
                <p>
Rēķins ar laika faktiskajām vērtībām: <strong>Nav pieejams</strong>
                </p>
                <p>
Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Rēķina tips faktiskajām materiālu vērtībām: iekasējams </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jā </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Jā </p>
            </td>
            <td width="75" valign="top">
                <p>
Viss projekts </p>
            </td>
            <td width="65" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="70" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="350" valign="top">
                <p>
Norēķini par laika faktiskajiem datiem: Apmaksājams </p>
                <p>
Rēķina tips izdevumu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </p>
                <p>
Rēķina tips faktiskajām materiālu vērtībām: iekasējams </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jā </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Jā </p>
            </td>
            <td width="75" valign="top">
                <p>
Viss projekts </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nav iekasējams</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="350" valign="top">
                <p>
Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Rēķina tips izdevumu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </p>
                <p>
Rēķina tips faktiskajām materiālu vērtībām: iekasējams </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jā </p>
            </td>
            <td width="78" valign="top">
                <p>
Jā </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Viss projekts </p>
            </td>
            <td width="65" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="70" valign="top">
                <p>
Izrakstāms rēķins </p>
            </td>
            <td width="65" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="350" valign="top">
                <p>
Norēķini par laika faktiskajiem datiem: Apmaksājams </p>
                <p>
Norēķinu veids par izdevumu faktiskajiem datiem: Apmaksājams </p>
                <p>
Rēķina tips materiālu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jā </p>
            </td>
            <td width="78" valign="top">
                <p>
Jā </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Nr.</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Viss projekts </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nav iekasējams</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nav iekļaujams rēķinā</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nevar iestatīt </p>
            </td>
            <td width="350" valign="top">
                <p>
Rēķins par laika faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Rēķina tips izdevumu faktiskajām vērtībam: <strong>Nav iekasējams</strong>
                </p>
                <p>
Rēķina tips materiālu faktiskajām vērtībām:<strong> Nav pieejams</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
