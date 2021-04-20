---
title: Maksas komponentu konfigurēšana projekta balstīta līguma rindā
description: Šajā tēmā ir sniegta informācija par to, kā projektu operācijās līguma rindām pievienot apmaksājamus komponentus.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858482"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Maksas komponentu konfigurēšana projekta balstīta līguma rindā

_**Attiecas uz:** Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu, Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem_

Projekta līguma rindā ir *iekļauti* komponenti un *apmaksājami* komponenti.

Iekļautie komponenti ir komponenti, uz kuriem attiecas tālāk minētais.

  - Norēķinu metode un klientu sadalījums
  - Nepārsniedzamie ierobežojumi 
  - Rēķina izrakstīšanas biežuma iestatījumi, kas definēti projekta līguma rindā

Iekļauto komponentu apakškopu var atzīmēt kā apmaksājamu, izmantojot lauku **Norēķinu tips**. Lauks **Rēķina tips** ir opciju kopa, kas līguma rindas kontekstā ļauj izmantot šādas vērtības:

  - Izrakstāms rēķins
  - Nav iekļaujams rēķinā

Apmaksājamus komponentus var definēt uzdevumos, lomās un darījumu kategorijās.

Iekļaujamība rēķinā tiek definēta par projekta līguma rindas uzdevumiem un tā attiecas uz visām rindā iekļautajām darījumu klasēm. Ja lauks **Iekļaut uzdevumus** līguma rindā ir tukšs vai iestatīts uz **Viss projekts**, cilne **Rēķinā iekļaujamie uzdevumi** nebūs pieejama.

Apmaksas apjoms, kas definēts pēc lomām projekta līguma rinai, attiecas tikai uz darījumu klasi **Laiks**. Ja lauks **Iekļaut laiku** līguma rindā ir tukšs vai iestatīts uz **Nē**, cilne **Apmaksājamās lomas** nebūs pieejama.

Apmaksas apjoms, kas definēts pēc darījumu kategorijām projekta līguma rindai, attiecas tikai uz darījumu klasi **Izdevumi**. Ja lauks **Iekļaut izdevumus** līguma rindā ir iestatīts uz **Nē**, cilne **Apmaksājamās kategorijas** nebūs pieejama.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Projekta uzdevuma atjaunināšana par apmaksājamu vai neapmaksājamu

Projekta uzdevums var būt apmaksājams vai neapmaksājamss noteiktā līguma rindā, kas nodrošina šādas iestatīšanas iespējas.

Ja projekta līguma rindā ir iekļauts lauks **Laiks** un noteikts uzdevums, **T1** ir saistīts ar to kā apmaksājams. Ja ir otra līguma rinda, kurā ir iekļautas lauks **Izmaksas**, varat saistīt T1 uzdevumu līguma rindā kā neapmaksājamu. Rezultāts ir tāds, ka viss šajā uzdevumā reģistrētais laiks ir apmaksājams, un visi izdevumi ir neapmaksājami.

Uzdevuma norēķinu tipu var konfigurēt līguma rindas cilnē **Rēķinā iekļaujamie uzdevumi**, atjauninot lauku **Norēķinu tips** līguma rindu uzdevumu apakšrežģī. Vai arī varat atjaunināt lauku **Norēķinu tips** projekta norēķinu iestatījumu apakšrežģī, kas rāda ar uzdevumu saistītās līguma rindas.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Lomas atjaunināšana par apmaksājamu vai neapmaksājamu

Loma var būt apmaksājama vai neapmaksājama noteiktā līguma rindā.

Lomu norēķina veidu var konfigurēt līguma rindas cilnē **Apmaksājamās lomas**. Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās lomas**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Darījumu kategorijas atjaunināšana par apmaksājamu vai neapmaksājamu

Darījumu kategorija var būt apmaksājama vai neapmaksājama noteiktā līguma rindā.

Darījuma norēķina veidu var konfigurēt projekta līguma rindas cilnē **Apmaksājamās kategorijas**. Lai to paveiktu, ir jāatjaunina lauks **Norēķinu tips**, kas atrodas apakšrežģī **Rēķinā iekļaujamās kategorijas**.

### <a name="resolve-chargeability"></a>Apmaksājamības atrisināšana

Laika novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.

   - **Laiks** ir iekļauts līguma rindā.
   - **Loma** līguma rindā ir konfigurēta kā apmaksājama.
   - **Iekļautie uzdevumi** līguma rindā ir iestatīti uz **Atlasītie uzdevumi**.
 
 Ja šie trīs nosacījumi ir izpildīti, uzdevums arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu. 

Izdevumu novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.

   - **Izdevumi** ir iekļauts līguma rindā.
   - **Transakcijas kategorija** līguma rindā ir konfigurēta kā apmaksājama.
   - **Iekļautie uzdevumi** līguma rindā ir iestatīti uz **Atlasītais uzdevums**.
  
 Ja šie trīs nosacījumi ir izpildīti,  **Uzdevums** arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu. 

Materiālu novērtētā vai faktiskā vērtība tiks uzskatīta par apmaksājamu tikai tālāk norādītajos gadījumos.

   - **Materiāli** ir iekļauts līguma rindā.
   - **Iekļautie uzdevumi** līguma rindā ir iestatīti uz **Atlasītie uzdevumi**.

Ja šie divi nosacījumi ir izpildīti, **Uzdevums** arī tiek konfigurēts kā tāds, par kuru var iekasēt maksu. 

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
Rēķins par laika faktisko vērtību: <strong>Iekasējams</strong>
                </p>
                <p>
Rēķins par izdevumu faktisko vērtību: <strong>Iekasējams</strong>
                </p>
                <p>
Rēķins par materiālu faktisko vērtību: <strong>Iekasējams</strong>
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
Rēķins par laika faktisko vērtību: <strong>Iekasējams</strong>
                </p>
                <p>
Rēķins par izdevumu faktisko vērtību: <strong>Iekasējams</strong>
                </p>
                <p>
Rēķins par materiālu faktisko vērtību: <strong>Iekasējams</strong>
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
