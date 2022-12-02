---
title: Pro forma projektā balstīta rēķina apstiprināšana
description: Šajā rakstā ir sniegta informācija par projektu pro forma rēķinu apstiprināšanu.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a4ad243e8959af61993e2ff6ce89209be378f7df
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929453"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Pro forma projektā balstīta rēķina apstiprināšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Pēc tam, kad ir apstiprināts proforma rēķins, projekta rēķina statuss tiek atjaunināts uz **Apstiprināts**. Kad rēķins ir apstiprināts, tas kļūst tikai lasāms. Turpmāk rēķinu var labot tikai tad, ja ir veiktas klientam ierosinātas korekcijas vai kredīti.

Tālāk sniegtajā tabulā ir uzskaitīti sistēmā izveidotie faktiskie dati. Šie faktiskie dati tiek izveidoti, kad projekta rēķina melnrakstā pirms apstiprināšanas tiek veiktas noteiktas darbības.

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
Rēķina izrakstīšana par honorāru vai avansu </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautas pārdošanas faktiskie dati ar tipu <strong>Honorārs</strong> tiek izveidoti par avansa vai honorāra summu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Saskaņošanai tiks izmantotas rēķinā neietvertas pārdošanas faktiskās vērtības ar negatīvu honorāra vai avansa summu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Pēc honorāra vai avansa pilnīgas saskaņošanas rēķinā.
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
Rēķinā iekļautās pārdošanas faktiskie dati par summu šajā rēķinā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Pēc honorāra vai avansa daļējas saskaņošanas rēķinā.
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
Rēķinā iekļautās pārdošanas faktiskie dati par summu šajā rēķinā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Negatīva rēķinā neiekļautas pārdošanas faktiskā summa no atlikušā honorāra vai avansa summas, kas tiks izmantota saskaņošanai turpmākos rēķinos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Rēķina izveide laika darījumam bez labojumiem rēķina melnrakstā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana stundām un summai sākotnējā laika apstiprinājumā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas faktiskie dati stundām un summai sākotnējā laika apstiprinājumā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Rēķina izveide laika darījumam, kas tika rediģēts, lai samazinātu daudzumu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana stundām un summai sākotnējā laika apstiprinājumā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa stundām un summu rediģētā rēķina rindu informācijā, pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauna rēķinā neietverta un neiekasējama faktiskā pārdošanas summa par atlikušajām stundām un summa pēc labotās summas atņemšanas labotajā rēķina rindu informācijā, faktiskās pārdošanas vērtības atsaukšana, līdzvērtīga faktiskā pārdošanas vērtība.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Rēķina izveide laika darījumam, kas tika rediģēts, lai palielinātu daudzumu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana stundām un summai sākotnējā laika apstiprinājumā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama pa stundām un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Rēķina izveide izdevumu darījumam bez labojumiem rēķina melnrakstā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana daudzumam un summai sākotnējā izdevumu apstiprinājumā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas faktiskie dati daudzumam un summai sākotnējā izdevumu apstiprinājumā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Rēķina izveide izdevumu darījumam, kas tika rediģēts, lai samazinātu daudzumu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana daudzumam un summai sākotnējā izdevumu apstiprinājumā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama par daudzumu un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas nav iekasējami par atlikušo daudzumu un summu pēc laboto ciparu atvilkšanas rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajiem datiem.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Rēķina izveide izdevumu darījumam, kas tika rediģēts, lai palielinātu daudzumu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana daudzumam un summai sākotnējā izdevumu apstiprinājumā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama par daudzumu un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Materiāla transakcijas bez labojumiem ietveršana melnraksta rēķinā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana par sākotnējā materiālu lietojuma apstiprināšanā norādīto daudzumu un summu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautā pārdošanas vērtība par sākotnējā materiālu lietojuma apstiprināšanā norādīto daudzumu un summu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Tādas materiālu transakcijas ietveršana rēķinā, kas tika rediģēta, lai samazinātu daudzumu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana par sākotnējā laika apstiprināšanā norādīto daudzumu un summu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama par daudzumu un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas nav iekasējami par atlikušo daudzumu un summu pēc laboto ciparu atvilkšanas rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajiem datiem.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Tādas materiālu transakcijas ietveršana rēķinā, kas tika rediģēta, lai palielinātu daudzumu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana par sākotnējā materiālu lietojuma apstiprināšanā norādīto daudzumu un summu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas iekasējama par daudzumu un summu rediģētā rēķina rindu informācijā, rēķinā neiekļautās pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Maksas iekļaušana rēķinā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā neiekļautās pārdošanas atsaukšana maksas summai sākotnējā žurnāla rindā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas faktiskie dati daudzumam un summai sākotnējā maksas žurnāla rindā.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Atskaites punkta iekļaušana rēķinā.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautās pārdošanas faktiskie dati atskaites punkta summai sākotnējā atskaites punktā projekta līguma rindā.
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
