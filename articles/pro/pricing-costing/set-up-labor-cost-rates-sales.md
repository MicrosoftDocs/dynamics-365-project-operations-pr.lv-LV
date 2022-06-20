---
title: Darba izmaksu likmju iestatīšana — Lite
description: Šajā rakstā sniegta informācija par to, kā iestatīt darbaspēka izmaksu likmes projektu operācijās.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 77e47fb1e76229bb7f52deb9b5472d04bb180623
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926003"
---
# <a name="set-up-labor-cost-rates---lite"></a>Darba izmaksu likmju iestatīšana — Lite

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Katram cenrādim ir darba likmju (lomu cenu) kopa, kas atbilst cenrāža saturam un datuma efektivitātei.

1. Izveidojiet cenrādi un apakšrežģa cilnē **Lomas cena** atlasiet **Jauna loma**.
2. Lapā **Ātrās izveides** atlasiet lomu un organizācijas vienību.
3. Ievadiet citu nepieciešamo lauka informāciju.

Šajā tabulā ir iekļauti daži lauki, kas ir svarīgi, veidojot darba likmes izmaksu cenrādī.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| Loma | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Atlasiet lomu, uz kuru attiecas izmaksu likme. | Loma ienākošajā tāmē vai faktiskajos datos tiks saskaņota ar šo rindu, lai noklusētu lomas izmaksas. |
| Resursu vienība | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Atlasiet uzņēmuma struktūrvienību vai struktūrvienību, no kuras tiks izmantota šī loma. Piemēram, izstrādātājs no Fabrikam India Robotics nodaļas vai izstrādātājs no Fabrikam USA programmatūras nodaļas. | Ienākošās aplēses vai faktiskās resursu veidošanas vienība tiks saskaņota ar šo rindu, lai noklusētu lomas izmaksas. |
| Cenrādis | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Iestatiet izmaksu likmi lomai, uzņēmumam, kas nodrošina resursus, un vienību kombinācijai, kas nodrošina resursus. Piemēram, izstrādātājs no Fabrikam India maksā 1000 INR vai izstrādātājs no Fabrikam USA maksā 150 USD. | Cena ir izmaksu likme, kas pēc noklusējuma attiecas uz ienākošā novērtējuma vai faktiskās rindas vienības izmaksām transakciju klasē **Laiks**. |
| Valūta | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Pēc noklusējuma valūtas vērtība tiek iegūta no valūtu izmaksu cenrāža galvenē, bet to var ignorēt. Piemēram, izstrādātājs no Fabrikam India maksā 1000 INR. Izstrādātājs dzīvo no Fabrikam USA maksā 150 USD. | Šī valūta noklusē ienākošās faktiskās izmaksu rindas vienības pašizmaksu darbības klasē **Laiks**. Projekta novērtējumā valūtas vērtība tiek konvertēta projekta valūtā, un tā tiek parādīta novērtējuma skatā “Laika posms”. |
| Vienības grafiks | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Vienību plāns pēc noklusējuma ir Laiks, un to nevar mainīt uz entītiju Lomas cena, jo to izmanto noteiktās laika vienībās. | Tas neietekmē lejupstraumi. |
| Vienība | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Pēc noklusējuma vērtība tiek iegūta no izmaksu cenrāža galvenes lauka **Laika vienība**. Vērtību var ignorēt. Piemēram, izstrādātājs no Fabrikam India maksā 1000 INR saskaņā ar **Indijas dienu**. Izstrādātājs dzīvo no Fabrikam USA maksā 150 USD saskaņā ar **ASV dienu**. | Sistēma izmanto vienību un konvertēšanas sistēmu bāzes vienībās, lai aprēķinātu vienības pašizmaksu, lai aprēķinātu vienības noklusējuma cenu ienākošajā novērtējumā vai faktiskajā rindā. Piemēram, tāme ir 10 **India Days** vērts darbs izstrādātājam no Indijas, un vienība **Indijas diena** tiek definēta kā 10 stundas. Aprēķinot šo novērtējuma rindu, programma aprēķina vienības pašizmaksu tāmē kā: 1000 INR/10 stundas = 100 INR stundā, kas tiek konvertēta par ASV dolāriem un parādīta kā vienības pašizmaksa lapā **Projekta novērtējumi**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Iekšējo cenu noteikšana un izmaksas par resursiem ārpus jūsu nodaļas vai juridiskās personas

Projektu uzņēmumos parasti izmanto dažādu juridisku personu vai nodaļu darbiniekus projektos. Projektu var veikt viena juridiska persona, bet darbinieki vai konsultanti, kas strādā pie projekta, var būt no tās pašas juridiskas personas vai no citas, vai var būt abu kombinācija. Programmā Dynamics 365 Project Operations juridiska persona, kuras rīcībā ir projekta piegāde, ir **Atbildīgais uzņēmums** un nodaļa, kas nodrošina piegādi, ir **Līgumslēdzēja vienība**. Citas juridiskas personas, kas nodrošina resursus, ir resursu **Resursu uzņēmumi**, un nodaļas, kas nodrošina resursus, ir **Resursu struktūrvienības**. Lielākajā daļā valstu uzņēmumiem ir jānodrošina, ka juridiskās personas vai nodaļas, kas nodrošina resursus, maksā uzņēmējsabiedrībai un līgumslēdzējai vienībai par resursu izmantošanu.

Piemēram, Fabrikam uzņēmumam ir jānodrošina, lai Fabrikam India-Robotics būtu panākta vienošanās par izmaksu likmes karti ar Fabrikam US-Robotics vai Fabrikam UK-Robotics.

Izstrādātājs no Fabrikam India-Robotic maksā 100 ASV dolāru, sniedza aizdevumu Fabrikam US-Robotics, un 150 ASV dolāru, kad sniedza aizdevumu Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Ārējo resursu izmaksu iestatīšana

1. Izveidojiet izmaksu cenrāža nosaukumu *Fabrikam US-Robotics izmaksu likmes* un iestatiet datumu efektīvo diapazonu.
2. Izmaksu cenrādī iestatiet likmes, izmantojot informāciju no tālāk norādītās tabulas. 

| Loma | Resursu uzņēmums | Resursu vienība | Izmaksu likme |
| --- | --- | --- | --- |
| Izstrādātājiem | Fabrikam India | Fabrikam India-Robotics | USD 100 |
| Izstrādātājiem | Fabrikam Philippines | Fabrikam Philippines-Robotics | 90 ASV dolāru |
| Izstrādātājiem | Fabrikam US | Fabrikam US-Robotics | 150 ASV dolāru |

3. Pievienojiet šo izmaksu cenrādi Fabrikam US-Robotics organizācijas vienībai.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Resursa pārsūtīšanas cenu iestatīšana atbilstošajā valūtā 

Risinājumā Project Operations resursu cenu var iestatīt jebkurā valūtā. Noklusējuma valūtas ir norādītas cenrāža galvenē, bet tās var mainīt.

Izmantojot piemēru pārsūtīšanas cenas iestatījumam, informāciju var mainīt uz:

Fabrikam uzņēmumam ir jānodrošina, lai Fabrikam India-Robotics būtu panākta vienošanās par izmaksu likmes karti ar Fabrikam US-Robotics vai Fabrikam UK-Robotics.

Izstrādātājs no Fabrikam India-Robotic maksā 5000 INR, kad sniedza aizdevumu Fabrikam US-Robotics, un 5500 INR, kad sniedza aizdevumu Fabrikam UK-Robotics.

Izmaksu cenrādī, kas paredzēts Fabrikam US-Robotics, izmaksu likmes var izteikt šādi:

| Loma | Resursu uzņēmums | izdevumi |
| --- | --- | --- |
| Izstrādātājiem | Fabrikam India | 5000 INR |
| Izstrādātājiem | Fabrikam US | 115 USD |

Izmaksu cenrādī, kas paredzēts Fabrikam UK-Robotics, izmaksu likmes var izteikt šādi:

| Loma | Resursu uzņēmums | izdevumi |
| --- | --- | --- |
| Izstrādātājiem | Fabrikam India | 5500 INR |
| Izstrādātājiem | Fabrikam UK | 115 GBP |

Izmaksu cenrādis var nodrošināt darba likmes vairākās valūtās. Ja projektam tiek ģenerēts izmaksu novērtējums, Project Operations šos izmaksu kursus pārvērtīs projekta valūtā un parādīs to lietotājam. Kad laika ieraksts ir apstiprināts un tiek izveidota faktiskā pašizmaksa, faktiskās izmaksas tiek maksātas šīs atbilstošās lomas cenas rindas valūtā izmaksu cenrādī. Izmaksu faktiskajiem izdevumiem vienā projektā var ierakstīt vairākās valūtās. Tomēr, apkopojot vai summējot faktiskās darba izmaksas projekta līmenī, Project Operations konvertē visas darba izmaksu summas projekta valūtā, kuru lietotājs var skatīt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]