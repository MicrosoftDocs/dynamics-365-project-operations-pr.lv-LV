---
title: Projekta prognozes un budžeti
description: Microsoft Dynamics 365 Finance nodrošina projekta prognozes un projekta budžetus projektu pārvaldībai un vadībai.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85a5577968024bf42449c50d72a11414f9207eec
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753511"
---
# <a name="project-forecasts-and-budgets"></a>Projekta prognozes un budžeti

[!include [banner](../includes/banner.md)]

Ir divi veidi, kā pārvaldīt un vadīt projektus: projektu prognozes un projektu budžeti. 

Izmantojiet projektu prognozēšanu, ja jūsu organizācijai ir darbības perspektīva un ja tā koncentrējas uz ieņēmumiem un izmaksām, kas rodas no noteiktām transakcijām. Ja jūsu organizācija vairāk koncentrējas uz finanšu summām, izmantojiet projekta budžeta veidošanu. 

Gan projekta prognozēs, gan projekta budžetos tiek izmantoti prognožu modeļi, lai ieturētu plānotās transakciju summas. 

Katrai metodei ir savas priekšrocības. Pirms atlasāt metodi savai organizācijai, vajadzētu ņemt vērā šādus elementus.

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **Projekta prognožu veidošana**                  | **Projekta budžeta veidošana**                              |
| **Perioda piešķiršana**     | Finanšu periodā nevar tieši piešķirt transakcijas. Tā vietā prognoze un tās vadība tiek balstīta projekta dzīvē. Tā kā prognozes tiek balstītas konkrētā datumā, periods ir jāizsecina no datuma. | Transakcijas varat piešķirt visā projektā vai finanšu periodā. Ja piešķiret periodā, varat pārnest neizmantotās summas uz nākamo finanšu periodu. |
| **Transakciju skatīšana**  | Transakcijas varat skatīt prognožu veidlapās, kurās redzat prognozes visam uzņēmumam un visiem projektiem neatkarīgi no hierarhijas. Lai koncentrētos un konkrētu projektu, ir jāfiltrē dati.                                       | Budžetā iekļautās transakcijas var skatīt skatīt vienai projekta hierarhijai. Tādējādi varat skatīt transakciju informāciju primārajam projektam vai tā apakšprojektiem.                 |
| **Transakciju mainīgie** | Ievadot prognozes transakcijas, varat izmantot visus atribūtus, kas pastāv faktiskajai transakcijai. Tādējādi prognoze var būt detalizētāka. Piemēram, varat ievadīt informāciju par daudzumiem, darba ņēmējiem, precēm vai rindas rekvizītiem.         | Ievadot budžeta informāciju, varat izmantot vienīgi summas, kategorijas un darbības.                    |
| **Drošība**              | Prognozēšanu balsta transakcijās, kuras ievadāt prognožu veidlapās, un kuras neietver procesa kontroles mehānismus. Jebkurš darba ņēmējs, kuram ir prognozes veidlapas atļaujas, var bez apstiprinājuma pārskatīt informāciju.                                        | Budžeta izveidē tiek izmantota darbplūsmas sistēma, kura iespējot izmaiņu pārvaldību un ļauj uzturēt pārskatījumu vēsturi.         |
| **Ievades veidi**           | Prognozes transakciju ievades balstās vienību skaitā un izmaksu un pārdošanas vienību cenās.  | Budžeta informācija tiek balstīta summās, kuras tiek dalītas starp izmaksām un ieņēmumiem.                                          |
| **Prognožu modeļi**       | Tā kā katru prognozi ir jāsaista ar modeli, jūs varat izveidot vairākus prognožu modeļus, kā arī iestatīt apakšmodeļus.           | Projekta budžeta izveide ierobežo prognožu modeļus, kas tiek izmantoti budžeta izveidošanā. Samazinot prognožu modeļu skaitu, var palielināties prognožu konsekvence.                           |
| **Izmaksu pārsniegumi**         | Varat vienīgi atļaut vai aizliegt tādu transakciju ievadi, kuras izraisīs izmaksu pārsniegumu.   | Projekta budžeta izveide lietotājiem nodrošina papildu kontroles opcijas. Varat atļaut brīdinājumus un pārsniegumus.                    |
| **Vadīkla**               | Budžeta kontroli veic, izmantojot prognožu samazināšanu. Faktiskās summas atvelk no prognožu transakciju bilancēm bez auditācijas pierakstiem. Tas var apgrūtināt izsekošanu tam, kur ir notikušās faktiskās transakcijas.                   | Projekta budžeta vadībā faktiskās summas atvelk no atlikušā budžeta summām. Tādējādi var veikt skaidrākus auditācijas pierakstus.                                   |

## <a name="project-forecasts"></a>Projekta prognozes
Izmantojot projekta prognozēšanu, varat ievadīt prognozes transakcijas katra transakcijas veida prognožu veidlapās. Katru atribūtu, kas ir pieejams faktiskajai transakcijai, var izmantot prognozes transakcijai — piemēram, rindu rentabilitātei, rindu atribūtiem, darba ņēmējiem vai aprakstiem. Varat arī prognozēt, cik ilgi pēc izmaksu rašanās jūs klientam izrakstīsit rēķinu. 

Projekta prognozēšanas transakcijas tiek balstītas vienībās un skaitos. 

Katru projekta prognozi ir jāsaista ar prognozes modeli. Ievadot prognozes transakciju, automātiski tiek ierosināts prognozes modelis. Budžeta modelis darbojas kā prognožu transakciju konteiners. 

Prognozētos modeļus var norādīt kā modeļa apakšmodeļus. Tas ļauj prognozēt pēc reģiona, laika perioda vai nodaļas. Prognozes darbības var kopēt modelī, lai izveidotu jaunu modeli, un transakcijas var arī pārsūtīt uz virsgrāmatu. Tā kā starp prognozi un modeli pastāv tieša relācija, katrs prognozes modelis projektam veido atsevišķu budžetu. 

Prognožu modeļi var izmantot prognožu samazināšanu kā projektu kontroles mehānismu. Prognožu samazināšanā faktiskās transakcijas samazina prognožu transakciju bilances. Taču, tā kā prognožu samazināšana tiek piemērota hierarhijā visaugstāk esošajam projektam, tā sniedz ierobežotu skatu uz izmaiņām prognozē. Piemēram, ja ar apakšprojektu tiek saistīts darba ņēmējs, darba ņēmēja faktiskās transakcijas tiek grāmatotas primārajā projektā. Tas var apgrūtināt izmaiņu izsekošanu, jo nevarat vienkārši noteikti, kura transakcija kurā apakšprojektā izraisījusi prognozes summas samazināšanos. Tāpēc ir ieteicams izveidot budžeta samazināšanai izmantojamā budžeta modeļa kopiju. Pēc tam varat izmantot atskaites, lai skatītu sākotnējās prognozes. 

Projekta prognozes var pārskatīt, kopēt, dzēst vai pārsūtīt uz virsgrāmatas budžetu. Taču nav nekādas procesa kontroles. Jebkurš darba ņēmējs, kuram ir prognozes veidlapas atļauja, var bez atsauksmes veikt pārskatīšanu.

-   **Pārskatīt** — Varat pārskatīt prognozes transakciju tajās pašās veidlapās, kurās tika veikta sākotnējā ievade.
-   **Kopēt vai dzēst** — Kopējot prognožu transakcijas, viena prognozes modeļa transakciju rindas tiek kopētas citā prognozes modelī. Dzēšot prognozi, tiek dzēstas prognožu transakcijas no prognozes modeļa. Lai ierobežotu prognožu transakcijas, kas tiek kopētas vai dzēstas, atlasiet konkrētus transakciju veidus un datumus. Tādējādi varat kopēt vai dzēst vienīgi konkrētas prognozes daļas.
-   **Pārsūtīšana** — Pārsūtot projekta prognozi uz virsgrāmatas budžetu, prognozes modeļa prognožu transakcijas tiek pārsūtītas uz virsgrāmatas budžetu. Varat pārrakstīt visas iepriekš pārsūtītās transakcijas virsgrāmatas budžetā, uz kuru pārsūtāt projekta prognozi.

## <a name="project-budgets"></a>Projekta budžeti
Projekta budžetu izveide ir vienkāršāka metode, nekā prognožu izveide, lai arī to var integrēt ar prognožu modeļiem. Tajā izmanto vienas ievad veidlapu sākotnējai budžeta informācijai un labojumiem, un ar to var veikt prognozes, kas tiek balstītas vienīgi summā, kategorijā vai darbībā. 

Veidojot projekta budžetu, visus sākotnējos budžetus un labojumus ir jāsūta uz projekta darbplūsmu, lai tos apstiprinātu. Darbplūsmas nodrošina lielāku kontroli pār procesu un izveido izmaiņu vēstures ierakstus. 

Projekta budžeta izveide atgādina virsgrāmatas budžeta izveidi, taču to var iestatīt ātrāk un vienkāršāk. Daudzas virsgrāmatas budžeta izveides opcijas, piemēram, skaitļu secība vai valūta, nav jāiestata projektiem atsevišķi.

Projekta budžetus automātiski saista ar diviem prognožu modeļiem — vienu sākotnējam budžetam un vienu atlikušajam budžetam. Tāpēc atskaites, kuru pamatā ir budžeta modeļi, var izmantot budžeta datus. Kad tiek izpildīts projekta budžets, sistēma izveido prognozes transakcijas, pamatoties uz saistītajiem modeļiem, kurus izmanto ziņošanas un kontroles nolūkiem.

## <a name="forecast-models"></a>Prognožu modeļi
Prognožu modeļiem ir viena slāņa hierarhija. Tas nozīmē, ka vienu projekta prognozi ir jāsaista ar vienu prognozes modeli.

Ja izmantojat projekta prognozēšanu, modeļus varat identificēt kā apakšmodeļus. Pēc tam varat izveidot prognozes pēc nodaļas, laika perioda vai reģiona. Piemēram, varat izveidot budžeta modeli gadam, un pēc tam izveidot apakšmodeļus ziemeļaustrumu, dienvidaustrumu, ziemeļrietumu un dienvidrietumu reģionālajām prognozēm, kuras iesniedz reģionālie vadītāji. Atlasot dažādas opcijas pieejamajās atskaitēs, informāciju var skatīt pēc kopējās prognozes vai apakšmodeļa.



