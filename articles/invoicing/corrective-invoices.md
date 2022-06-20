---
title: Labojošu projektā balstītu rēķinu izveide
description: Šajā rakstā sniegta informācija par koriģējošiem rēķiniem projektu operācijās.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 86bb05242c74e97533c7555ffa645278c8519430
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927889"
---
# <a name="create-corrective-project-based-invoices"></a>Labojošu projektā balstītu rēķinu izveide 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Apstiprinātu projekta rēķinu var labot, lai apstrādātu izmaiņas vai kredītus pēc pārrunām ar klientu un projekta vadītāju.

Lai veiktu labojumus apstiprinātā rēķinā, atveriet apstiprināto rēķinu un atlasiet opciju **Labot šo rēķinu**. 

> [!NOTE]
> Šī atlase nav pieejama, ja vien nav apstiprināts projekta rēķins.

No apstiprinātā rēķina tiek izveidots jauns rēķina melnraksts. Visa rēķina rindu informācija no iepriekš apstiprināta rēķina tiek iekopēta jaunajā melnrakstā. Tālāk ir apskatīti daži galvenie punkti, kas palīdzēs saprast papildinformāciju par rindas informāciju jaunajā labotajā rēķinā.

- Visi daudzumi tiek atjaunināti uz nulli. Tiek pieņemts, ka visi rēķinā iekļautie elementi tiek pilnībā kreditēti. Ja nepieciešams, šos daudzumus var atjaunināt manuāli, lai atspoguļotu daudzumu, kam izrakstīts rēķins, nevis to daudzumu, kas tiek kreditēts. Pamatojoties uz ievadīto daudzumu, lietojumprogramma aprēķina kreditēto daudzumu. Šī summa tiek atspoguļota faktiskajos datos, kas tiek izveidoti, kad tiek apstiprināts pareizais rēķins. Ja veicat izmaiņas nodokļu summā, ir jāievada atbilstošā nodokļu summa, nevis kreditētā nodokļu summa.
- Pagrieziena punktu korekcijas vienmēr tiek apstrādātas kā pilni kredīti.
- Honorārus vai avansa summas var labot, ja klientam izrakstīts rēķins par nepareizu summu.
- Honorāru un avansu saskaņošanu var labot, ja ir izmantota nepareiza summa, lai salīdzinātu ar iepriekš apstiprināta rēķina maksu.

> [!IMPORTANT]
> Rēķina rindas informācijai, kas ir labojumi citās jau iekļautās rēķinā iekļautās izmaksās, lauks **Labojums** ir iestatīts **Jā**. Rēķiniem, kam ir labotas rēķina rindas detaļas, ir lauks **Ir labojumi**, kas arī ir iestatīts uz **Jā**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Faktiskie dati, kas izveidoti, apstiprinot labotu rēķinu

Tālāk sniegtajā tabulā ir uzskaitīti faktiskie dati, kas tiek izveidoti, apstiprinot labojošo rēķinu.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenārijs</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Pēc apstiprināšanas izveidotie faktiskie dati</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Apstipriniet izrakstīta avansa vai honorāra korekciju.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana honorāram vai avansam, kas tika izveidots saskaņošanai. Šī summa ir pozitīva, jo tā ir paredzēta, lai atceltu negatīvo summu, kas tika izveidota tad, kad tika izrakstīts rēķins par honorāru vai avansu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas atsaukšanas faktiskie dati tiek izveidoti par summu honorārā vai avansā, lai atsauktu sākotnējo rēķinā iekļauto pārdošanu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Tiek izveidoti jauni rēķinā iekļautās pārdošanas faktiskie dati ar labotu summu honorāra vai avansa labotajā rēķina rindā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautas pārdošanas faktiskie dati par negatīvu summu labotām honorāra vai avansa rēķina rindām, kas tiks izmantotas saskaņošanai.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Iepriekš saskaņota honorāra vai avansa labošanas apstiprinājums.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana honorāram vai avansam, kas tika izveidots saskaņošanai. Šī summa ir pozitīva un ir paredzēta, lai atceltu negatīvo summu, kas tika izveidota tad, kad notika iepriekšējā saskaņošana.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas atsaukšanas faktiskie dati par summu iepriekšējā rēķinā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Tiek izveidoti jauni rēķinā iekļautās pārdošanas faktiskie dati ar labotu honorāra summu, kas tiek izmantota labotajā rēķinā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautas pārdošanas faktiskie dati ar negatīvu summu no labotā atlikušā honorāra vai avansa, kas tiks izmantots saskaņošanai turpmākos rēķinos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Pilna iepriekš rēķinā izrakstīta laika darījuma kredīta iekļaušana rēķinā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas atsaukšana stundām un summai sākotnējā rēķina rindā laikam.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas faktiskie dati par stundām un summu sākotnējā rēķina rindā laikam.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Daļēja kredīta iekļaušana rēķinā par laika darījumu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas atsaukšana stundām un summai, kas iekļauta sākotnējā rēķina rindā laikam.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa stundām un summu rediģētā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jaunas rēķinā neiekļautas pārdošanas faktiskie dati, kas ir iekasējama par atlikušajām stundām un summu pēc laboto summu atvilkšanas rēķina rindu informācijā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Pilna iepriekš rēķinā izrakstīta izdevumu darījuma kredīta iekļaušana rēķinā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā izdevumiem.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jaunas rēķinā neiekļautās pārdošanas faktiskie dati par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā izdevumiem.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Daļēja iepriekš rēķinā izrakstīta izdevumu darījuma kredīta iekļaušana rēķinā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā par izdevumiem.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa daudzumu un summu labotā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jaunas rēķinā neiekļautas pārdošanas faktiskie dati, kas ir iekasējama par atlikušo daudzumu un summu pēc laboto summu atvilkšanas rēķina rindu informācijā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Pilna iepriekš rēķinā izrakstīta maksas darījuma kredīta iekļaušana rēķinā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā maksai.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jaunas rēķinā neiekļautās pārdošanas faktiskie dati par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā maksai.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Daļēja iepriekš rēķinā izrakstīta maksas darījuma kredīta iekļaušana rēķinā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas atsaukšana par daudzumu un summu, kas iekļauta sākotnējā rēķina rindā par maksu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa daudzumu un summu rediģētā rēķina rindu informācijā, tās atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Pilna iepriekš rēķinā izrakstīta atskaites punkta kredīta iekļaušana rēķinā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas atsaukšana summai sākotnējā rēķina rindā atskaites punktam.
                </p>
                <p>
Rēķina statuss atskaites punktā tiek atjaunināts no <b>Klienta rēķins iegrāmatots</b> uz <b>Gatavs rēķina izrakstīšanai</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Daļēja iepriekš rēķinā izrakstīta atskaites punkta kredīta iekļaušana rēķinā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Neatbalsta </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
