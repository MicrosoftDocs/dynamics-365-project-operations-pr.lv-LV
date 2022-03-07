---
title: Vairāku valūtu scenāriji (versija 3.x)
description: Šajā tēmā ir sniegta informācija par vairāku valūtu scenārijiem.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 89a91cf3dbbcf81dbb089ee88c8c177c73afb694914ca7d95eae96776d38abed
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005130"
---
# <a name="multiple-currency-scenarios"></a>Vairāku valūtu scenāriji

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Programmā Microsoft Dynamics 365 ir divas valūtu koncepcijas.

- **Transakcijas valūta** — valūta, kādā tiek veikta transakcija. 
- **Pamatvalūta** — Dynamics 365 instances valūta. Šī valūta tiek iestatīta, kad tiek nodrošināta Dynamics 365 instance. To nevar mainīt.

Piemēram, Contoso ASV pārdeva 100 T kreklus klientam Apvienotajā Karalistē par 15 sterliņu mārciņām (GBP) gabalā. Tālāk esošajā tabulā ir parādīts, kā šī transakcija tiek ierakstīta entītijā Pasūtījuma prece.

| Produkts | Daudzums | Vienības cena | Valūta | Summa | Maiņas kurss | Vienības cena (pamatvalūtā)| Summa (pamatvalūtā)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| T krekls | 100      | 15             | GBP      | 1500   | 0.94          | 17,25 $               | 1725 $       |

Kolonnā **Valūta** ir redzama transakcijas valūta, kas ir valūta, kurā notika pārdošana. Kolonnā **Maiņas kurss** ir redzams transakcijas valūtas un pamatvalūtas maiņas kurss. Pamatvalūta ir ASV dolāri (USD). Šī pamatvalūta tika iestatīta, kad tika nodrošināta Dynamics 365 instance.
Kā redzams tabulā, katra transakcija tiek ierakstīta gan transakcijas valūtā, gan pamatvalūtā. Dynamics 365 izmanto valūtas maiņas kursu, lai aprēķinātu pamatvalūtas summas.

## <a name="project-service-automation-extensions"></a>Project Service Automation paplašinājumi

Dynamics 365 Project Service Automation ietekmē transakcijas valūtu, jo biznesa transakcijām parasti ir divi aspekti: izmaksas un pārdošana.

Tālāk norādītās entītijas tiek uzskatītas par biznesa transakcijām.

- Piedāvājuma rindas informācija
- Projekta līguma rindas detaļas
- Novērtējuma rinda
- Žurnāla rinda
- Rēķina rindas detaļas
- Faktiski

Katrā no šīm entītijām ir ieraksts, kas norāda izmaksu summu vai pārdošanas summu. Katrai Dynamics 365 entītijai, kurai ir lauks **Summa** katrs ieraksts ietver summas gan transakcijas valūtā, gan pamatvalūtā. 

PSA paplašina transakcijas valūtas koncepciju izmaksām un pārdošanai tālāk aprakstītajos veidos.

- Izmaksu transakcijas valūta laika transakcijām vienmēr tiek iegūta no tās organizācijas struktūrvienības valūtas, kurai pieder projekts vai kas to pārvalda. Šo organizācijas struktūrvienību sauc par līgumslēdzēja struktūrvienību.
- Pārdošanas transakcijas valūta laika un izdevumu transakcijām vienmēr tiek iegūta no projekta līguma valūtas.
- Izmaksu transakcijas valūta izdevumiem tiek iegūta no valūtas, kurā tika izveidots izdevumu ieraksts.

## <a name="multiple-currency-scenario"></a>Vairāku valūtu scenārijs

Šajā sadaļā ir aprakstīts projekta piemērs, kurā Contoso UK veic piegādi klientam ar nosaukumu Fabrikam — Japāna. Tālāk norādīti scenārija parametri.

1. Sadaļās **Iestatījumi** \> **Uzņēmuma pārvaldība** \> **Valūtas** tiek iestatītas valūtas GBP un Japānas jēna (JPY). 
2. Tiek iestatīts klienta uzņēmums ar nosaukumu **Fabrikam — Japāna**, un kā uzņēmuma valūta tiek atlasīta JPY.
3. Tiek iestatīta organizācijas struktūrvienība ar nosaukumu **Contoso UK**, un kā valūta tiek atlasīta GBP.
4. Tiek izveidots projekta līgums, kurā **Contoso UK** ir norādīta kā līgumslēdzēja struktūrvienība, bet uzņēmums **Fabrikam — Japāna** ir norādīts kā klients.
5. Projekta līguma rindas tiek izveidotas, pamatojoties uz dažādo projekta transakciju klašu rēķinu izkārtojumiem, piemēram, rēķina izrakstīšana par laiku un rēķina izrakstīšana par izdevumiem.
6. Tiek izveidots projekts, kurā **Contoso UK** ir norādīta kā līgumslēdzēja struktūrvienība. Šis projekts tiek izveidots un kartēts uz projekta līguma rindām.


Novērtējuma laikā, kurā tiek izmantotas piedāvājuma rindas detaļas, projekta līguma rindas detaļas vai grafika novērtējuma rinda, entītijā vienmēr tiek izveidoti divi ieraksti. Viens ieraksts ir izmaksām, bet otrs ieraksts ir paredzēts pārdošanai.

- Pēc noklusējuma izmaksu ierakstā transakcijas valūta tiek iestatīta uz projekta līgumslēdzēja struktūrvienības valūtu. Šajā piemērā šī valūta ir GBP.
- Pēc noklusējuma pārdošanas ierakstā transakcijas valūta tiek iestatīta uz projekta līguma valūtu. Šajā piemērā šī valūta ir JPY.

Kad tiek izveidoti laika faktiskie dati, izmantojot laika ierakstu vai žurnāla rindu, rodas tālāk norādītā uzvedība.

- Pēc noklusējuma izmaksu ierakstā transakcijas valūta tiek iestatīta uz projekta līgumslēdzēja struktūrvienības valūtu.
- Pēc noklusējuma pārdošanas ierakstā transakcijas valūta tiek iestatīta uz projekta līguma valūtu.

Kad tiek izveidoti izdevumu faktiskie dati, izmantojot izmaksu ierakstu vai žurnāla rindu, rodas tālāk norādītā uzvedība.

- Izdevumu summu var reģistrēt jebkurā valūtā. Atlasiet valūtu, izmantojot valūtas atlasītāju lapā **Izdevumu ieraksts** vai lapā **Žurnāla rinda**. Pēc noklusējuma izmaksu ierakstā transakcijas valūta tiek iestatīta uz izdevumu ieraksta valūtu. 
- Pēc noklusējuma pārdošanas ierakstā transakcijas valūta ir projekta līguma valūta. Lai iestatītu šo valūtu, sistēma vispirms pārvērš transakcijas summu valūtā, kādu lietotājs ir ievadījis pamatvalūtā. Pēc tam tā pārvērš summu projekta līguma valūtā. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Apkopojumu aprēķināšana, kad projekta faktiskie ieraksti tiek ierakstīti vairākās transakciju valūtās

Dynamics 365 automātiski apstrādā dažādās valūtās esošu summu apkopojumus. Tālāk sniegts piemērs.

| Transakciju klase | Transakcijas tips| Date   | Resurss | Transakciju kategorija | Daudzums | Vienības cena | Summa      | Maiņas kurss | Summa pamatvalūtā |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Rēķinā neiekļautā pārdošana   | 14. jūn. | Konrāds  |                      | 8 st.    | 20 000 JPY    | 160 000 JPY | 123           | 1300,81 USD    |
| Time              | Rēķinā neiekļautā pārdošana   | 15. jūn. | Konrāds  |                      | 8 st.    | 20 000 JPY    | 160 000 JPY | 123           | 1300,81 USD    |
| Izdevumi           | Rēķinā neiekļautā pārdošana   | 16. jūn. | Konrāds  | Viesnīca                | 1 EA     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Izdevumi           | Rēķinā neiekļautā pārdošana   | 17. jūn. | Konrāds  | Automašīnu noma           | 1 EA     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Lai projektā aprēķinātu kopējo rēķinā neiekļauto pārdošanas darījumu vērtību, varat izveidot apkopojuma lauku, kas paredzēts laukam **Summas** visiem saistītajiem rēķinā neiekļautās pārdošanas faktiskajiem datiem. Apkopojuma lauks ir Dynamics 365 konstrukcija, kas ļauj izpildīt ātrās formulas saistītajiem ierakstiem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]