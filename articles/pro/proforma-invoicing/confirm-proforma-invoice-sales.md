---
title: Pro formas rēķinu apstiprināšana — Lite
description: Šajā tēmā ir sniegta informācija par proforma rēķinu apstiprināšanu risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274287"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Pro formas rēķinu apstiprināšana — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_


Pēc tam, kad ir apstiprināts proforma rēķins, projekta rēķina statuss tiek atjaunināts uz **Apstiprināts**. Kad rēķins ir apstiprināts, tas kļūst tikai lasāms. Turpmāk rēķinu varēs labot tikai tad, ja pastāvēs klienta iniciēti labojumi vai kredīti vai arī rēķins būs atzīmēts kā apmaksāts.

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
Rēķinā neiekļautas pārdošanas faktiskie dati par negatīvu summu honorāram vai avansam, kas tiks izmantota saskaņošanai.
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
Jauni rēķinā neiekļautas pārdošanas faktiskie dati, kas nav iekasējami par atlikušajām stundām un summu pēc laboto ciparu atvilkšanas rediģētā rēķina rindu informācijā, pārdošanas faktisko datu atgriešana un ekvivalents rēķinā iekļautās pārdošanas faktiskajos datos.
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
Rēķinā iekļautās pārdošanas faktiskie dati daudzumam un summai sākotnējā izdevumu apstiprinājumā </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Rēķina izrakstīšana projekta līguma rindai.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Rēķinā iekļautas pārdošanas faktiskie dati produkta rindai ar daudzumu un summu, kas iegūta no produkta līguma rindas.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]