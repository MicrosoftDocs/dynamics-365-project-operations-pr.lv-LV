---
title: Laboti projektu rēķini
description: Šajā tēmā ir sniegta informācija par labotu rēķinu izveidi un apstiprināšanu programmā Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aaa61c8473da0aab369bbb25acb10e9a3661379997737acbcc0b3d4ab33e0ce9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997165"
---
# <a name="corrective-project-based-invoices"></a>Laboti projektu rēķini

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Apstiprinātu projekta rēķinu var labot, lai apstrādātu izmaiņas vai kredītus pēc pārrunām ar klientu un projekta vadītāju.

Lai veiktu labojumus apstiprinātā rēķinā, atveriet apstiprināto rēķinu un atlasiet opciju **Labot šo rēķinu**. 

> [!NOTE]
> Šī atlase nav pieejama, ja vien netiek apstiprināts projekta rēķins vai projekta rēķinā nav avansu vai honorāru, kā arī honorāru vai avansu saskaņošanas.

No apstiprinātā rēķina tiek izveidots jauns rēķina melnraksts. Visa rēķina rindu informācija no iepriekš apstiprināta rēķina tiek iekopēta jaunajā melnrakstā. Lūk, daži no galvenajiem punktiem, lai izprastu rindu informāciju jaunajā labotajā rēķinā:

- Visi daudzumi tiek atjaunināti uz nulli. Dynamics 365 Project Operations pieņem, ka visi rēķinā iekļautie elementi tiek pilnībā kreditēti. Ja nepieciešams, šos daudzumus var atjaunināt manuāli, lai atspoguļotu daudzumu, kam izrakstīts rēķins, nevis to daudzumu, kas tiek kreditēts. Pamatojoties uz ievadīto daudzumu, lietojumprogramma aprēķina kreditēto daudzumu. Šī summa tiek atspoguļota faktiskajos datos, kas tiek izveidoti, kad tiek apstiprināts pareizais rēķins. Ja veicat izmaiņas nodokļu summā, ir jāievada atbilstošā nodokļu summa, nevis kreditētā nodokļu summa.
- Pagrieziena punktu korekcijas vienmēr tiek apstrādātas kā pilni kredīti.


> [!IMPORTANT]
> Rēķina rindas informācijai, kas ir labojumi citās jau iekļautās rēķinā iekļautās izmaksās, lauks **Labojums** ir iestatīts **Jā**. Rēķiniem ar labotu rindas informāciju lauks **Ir labojumi** ir iestatīts **Jā**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Faktiskie dati, kas izveidoti, apstiprinot labotu rēķinu

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
Rēķina izrakstīšana par pilnu kredītu iepriekš rēķinā ietvertai materiālu transakcijai.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā ietvertas pārdošanas atsaukšana par sākotnējā rēķina materiāla rindas informācijā norādīto daudzumu un summu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauna rēķinā neietverta pārdošanas vērtība par sākotnējā rēķina materiāla rindas informācijā norādīto daudzumu un summu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Rēķina izrakstīšana par daļēju kredītu materiālu transakcijai.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā ietvertas pārdošanas atsaukšana par sākotnējā rēķina materiāla rindas informācijā norādīto iekasēto daudzumu un summu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauna rēķinā neietverta pārdošanas faktiskā vērtība, par ko var iekasēt maksu par daudzumu un summu rediģētās rēķina rindas detalizētajai informācijai, kā arī par faktisko pārdošanas apjomu, par kuru izrakstīts rēķins.
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
Šāds scenārijs netiek atbalstīts.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
