---
title: Darbs ar programmas Project Service Automation datu modeli
description: Šajā tēmā ir sniegta informācija par to, kā strādāt ar datu modeli.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25f1af15c03001a92f96689ff36a3159a5352a46
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283242"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Darbs ar programmas Project Service Automation datu modeli

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation paplašina citu programmu entītijas un ievieš savas entītijas Common Data Service datu modelī. Šajā tēmā ir aprakstītas dažas entītijas, kas atrodamas tipiskos PSA atskaišu izveides scenārijos.

## <a name="reporting-on-opportunities"></a>Atskaišu izveide par iespējām

Project Service Automation paplašina Dynamics 365 Sales entītiju **Iespēja**, pievienojot laukus, kas iespējo uz projektu balstītus scenārijus. Šie lauki tiek identificēti ar shēmas nosaukumu, pirms kura norādīts prefikss **msdyn\_**. **Pasūtījuma tips** ir jauns lauks, kas ir svarīgs atskaišu izveidei par PSA iespējām. Šī lauka vērtība **Balstīts uz darbu** norāda, ka attiecīgā iespēja ir PSA iespēja. Cita starpā entītijai ir pievienoti lauki **Līgumslēdzēja organizācija**, kas norāda organizāciju, kurai pieder iespēja, un **Uzņēmumu pārvaldnieks**, kas norāda uzņēmumu pārvaldnieku, kurš ir atbildīgs par iespēju.

Entītija **Iespējas rinda** arī ietver laukus, kas ir saistīti ar Project Service. **Norēķinu metode** norāda, vai iespējas rindai ir jāizraksta rēķins, balstoties uz laiku un materiālu vai fiksētu cenu, un lauks **Projekts** norāda tāda projekta nosaukumu, kas ir iespējas pamatā. Citi lauki, par kuriem var izveidot atskaiti, norāda un rindas elementa izmaksas un klienta budžeta summas.

## <a name="reporting-on-quotes"></a>Atskaišu izveide saistībā ar piedāvājumiem

PSA paplašina programmas Sales entītiju **Piedāvājums**, pievienojot ar projektiem saistītos laukus. **Pasūtījuma tips** atšķir PSA piedāvājumus no piedāvājumiem, kas nav PSA piedāvājumi. Šī lauka vērtība **Balstīts uz darbu** norāda, ka attiecīgais piedāvājums ir PSA piedāvājums. Lauki, kas var būt nozīmīgi atskaišu izveidei par PSA piedāvājumiem, ietver summas laukus, piemēram, **Rēķinā iekļaujamās izmaksas**, **Rēķinā neiekļaujamās izmaksas**, **Bruto peļņa**, **Prognozes** un **Budžets**. Citi noderīgi lauki norāda, vai piedāvājums ir rentabls, vai tas tiks pabeigts pēc grafika un vai tas atbilst klienta budžeta prasībām.

PSA arī paplašina programmas Sales entītiju **Piedāvājuma rinda**. Viens lauks, ko pievieno PSA, ir **Rēķinu izrakstīšanas metode**, kas norāda, kā tiks izrakstīts rēķins par piedāvājuma rindu (laiks un materiāli vai fiksēta cena). Citi lauki, kas ir pievienoti entītijai, norāda saistīto projektu, kas ir piedāvājuma rindas, rēķinu izrakstīšanas, izmaksu un budžeta pamatā.

PSA arī pievieno jaunas ar piedāvājumu saistītas entītijas Dynamics 365 datu modelim. Lūk, daži piemēri:

- **Piedāvājuma rindas informācija** — šī entītija ietver projekta tāmes informāciju par piedāvājuma rindu. Tajā ir divi ieraksti katrai piedāvājuma rindai. Vienā ierakstā tiek glabātas piedāvājuma rindas izmaksas un izmaksu informācija, bet otrajā ierakstā tiek glabāta piedāvājuma rindas pārdošanas summa un pārdošanas informācija.
- **Piedāvājuma rindas rēķinu izrakstīšanas grafiks** — šī entītija ietver piedāvājuma rindas norēķinu grafiku. Šis grafiks tiek ģenerēts, pamatojoties uz rēķinu izrakstīšanas biežumu, kas piešķirts piedāvājuma rindai.
- **Piedāvājuma rindas atskaites punkts** — šī entītija ietver rēķina izrakstīšanas atskaites punktu fiksētas cenas piedāvājuma rindām.
- **Piedāvājuma rindas analītikas sadalījums** — šī entītija ietver piedāvājuma rindas finanšu datus. Šī informācija var būt noderīga atskaišu izveidei par piedāvājumā minētajām pārdošanas un novērtēto izmaksu summām dažādās dimensijās.

Citas entītijas, ko PSA pievieno piedāvājumiem, ir **Piedāvājuma rindas projekta cenrādis**, **Piedāvājuma rindas resursu kategorija** un **Piedāvājuma rindas transakcijas kategorija**.

![Shēma, kurā redzamas piedāvājuma, piedāvājuma rindas un projekta relācijas](media/PS-Reporting-image2.png "Shēma, kurā redzamas piedāvājuma, piedāvājuma rindas un projekta relācijas")

## <a name="reporting-on-project-contracts"></a>Atskaišu izveide par projekta līgumiem

PSA paplašina programmas Sales entītiju **Pasūtījums**, kas tiek izmantota, ierakstot projekta līgumus. Tā pievieno svarīgu jaunu lauku **Pasūtījuma tips**, kas identificē līgumu kā PSA projekta līgumu, nevis pārdošanas pasūtījumu. Šī lauka vērtība **Balstīts uz darbu** norāda, ka attiecīgais pasūtījums ir PSA pasūtījuma līgums. Citi jauni lauki, kas pievienoti entītijai **Pasūtījums**, norāda informāciju par izmaksām, PSA līguma statusu un organizāciju, kurai pieder līgums.

PSA arī paplašina programmas Sales entītiju **Pasūtījuma rinda**. Cita starpā ir pievienoti lauki, kuri norāda rēķinu izrakstīšanas metodi (laiks un materiāli vai fiksēta cena), klienta budžeta summas un pakārtoto projektu.

PSA pievieno arī jaunas entītijas, kas ir paredzētas projekta līgumiem. Lūk, daži piemēri:

- **Projekta līguma rindas informācija** — šī entītija ietver rindas līmeņa informāciju, kas ir apkopota atbilstoši līguma rindu summai. Tā var būt tikpat detalizēta kā rindas elementi, kas tiek ģenerēti, izmantojot projekta grafiku uzdevumu līmenī.
- **Līguma rindas rēķinu izrakstīšanas grafiks** — šī entītija ietver norēķinu grafiku, kurš tiek ģenerēts, pamatojoties uz rēķinu biežumu, kas piešķirts līguma rindai.
- **Līguma atskaites punkts** — šī entītija ietver rēķina izrakstīšanas atskaites punktus līgumu rindām, kurām ir fiksētas cenas rēķina izrakstīšanas termiņš.

Citas entītijas, ko PSA pievieno līgumiem, ir **Projekta līguma rindas projekta cenrādis**, **Projekta līguma rindas resursu kategorija** un **Projekta līguma rindas transakcijas kategorija**.

![Shēma, kurā redzamas pasūtījuma, pasūtījuma rindas un projekta relācijas](media/PS-Reporting-image3.png "Shēma, kurā redzamas pasūtījuma, pasūtījuma rindas un projekta relācijas")

## <a name="reporting-on-projects"></a>Atskaišu izveide par projektiem

Entītija **Projekts** un tās saistītās entītijas tiek izmantotas tikai programmā PSA. **Projekts** ir augšējā līmeņa entītija, ko izmanto, lai norādītu operāciju darbu un izmaksas. Tālāk minētas saistītās entītijas:

- **Projekta darba grupas dalībnieks** — šī entītija ietver informāciju par rezervējamiem resursiem, kas piešķirti projektam. Šie resursi var būt vispārēji rezervējami resursi, vai arī tie var būt nosaukti rezervējamie resursi, ko ievada projekta vadītājs vai kas ģenerēti no projekta grafika.
- **Projekta uzdevums** — šī entītija ietver uzdevumus, kas veido projekta plānu vai grafiku.
- **Resursu piešķiršana** — šajā entītijā ir iekļauta rezervējamā resursa uzdevuma piešķire.
- **Resursu vajadzība** — šī entītija ietver prasības attiecībā uz vispārējās resursu grupas dalībniekiem.
- **Novērtējums** un **Novērtējuma rinda** — šīm entītijām ir virsraksta/rindas attiecības, un tās ietver projekta izdevumu novērtējumus. Uzdevuma novērtējumi tiek glabāti entītijā **Resursu prognoze**.

![Shēma, kurā redzamas resursa prasību un projekta relācijas](media/PS-Reporting-image4.png "Shēma, kurā redzamas resursa prasību un projekta relācijas")

## <a name="reporting-on-resources"></a>Atskaišu izveide par resursiem

Projekta resursi izmanto entītijas **Rezervējamais resurss** no Universal Resource Scheduling (URS), kuras tiek kopīgotas ar citām lietojumprogrammām, piemēram, Microsoft Dynamics 365 Field Service. Tālāk ir norādīts to entītiju saraksts, kuras, iespējams, būs jāizmanto, izveidojot atskaites par projekta resursiem:

- **Rezervējamais resurss** — šī entītija norāda lietotāju, kontaktpersonu, vispārējo resursu, uzņēmumu, grupu vai aprīkojumu, kas tiek izmantots projekta darba grupā.
- **Rezervējamā resursa īpašības** — šī entītija ietver resursa prasmes, sertifikāciju vai izglītību. Īpašībām var būt vērtējuma vērtības, kas ir definētas vērtējuma modelī.
- **Rezervējamo resursu kategorija** — šī entītija norāda rezervējamā resursa lomu.
- **Rezervējamo resursu rezervācijas** — šī entītija norāda laiku, kas attiecīgajam resursam ir rezervēts projektiem. Katrai rezervācijai ir gan virsraksta entītija, gan rindas entītijas, un katrai rindai ir statuss, kas norāda rezervācijas statusu.

![Shēma, kurā parādītas rezervējamo resursu raksturlielumu relācijas](media/PS-Reporting-image5.png "Shēma, kurā parādītas rezervējamo resursu raksturlielumu relācijas")

## <a name="reporting-on-actual-transactions"></a>Atskaišu izveide par faktiskajām transakcijām

Apstiprinot darba laika uzskaites tabulu vai izdevumus vai izrakstot rēķinu līgumam programmā PSA, biznesa transakcija tiek ietverta entītijā **Faktiski**. Šī entītija var būt par pamatu gandrīz visām ar finansēm saistītajām atskaitēm programmā PSA. Entītijā **Faktiski** ir ietvertas attiecīgā biznesa notikuma izmaksas un pārdošana transakcijas. Tajā ir tverti arī daudzi svarīgi atribūti.

Strādājot ar entītiju **Faktiski**, ir svarīgi saprast, kādas transakcijas tiek ierakstītas entītijā un kad transakcijas tiek ierakstītas. Strādājot ar laika ierakstiem, tipiskā plūsma ir šāda (plūsma izdevumu ierakstiem ir līdzīga):

1. Kad tiek saglabāts laika ieraksts, entītijā **Faktiski** netiek izveidoti ieraksti.
2. Kad tiek iesniegts laika ieraksts, entītijā **Faktiski** netiek izveidoti ieraksti.
3. Kad tiek apstiprināts laika ieraksts, entītijā **Faktiski** tiek izveidots viens ieraksts, un var izveidot arī otru ierakstu. Pirmajā ierakstā tiek glabātas laika ieraksta izmaksas. Otrajā ierakstā tiek glabāts laika ieraksta rēķinā neiekļautais pārdošanas apjoms. Otrais ieraksts ir atkarīgs no tā, vai projektam ir piešķirta klienta, piedāvājuma vai līguma rinda.

    | Dokumenta datums | Transakcijas tips | Transakciju klase | Klients         | Līgums   | Resurss     | Resursa loma | Norēķinu tips | Daudzums | Vienības cena | Summa |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 3.2.2018.        | Izmaksas             | Time              | Alpu slēpošanas nams | Alpu CRM | Alise Kaņepe | Projektu vadītājs   | Izrakstāms rēķins   | 8.0      | 50.00      | 400.00 |
    | 3.2.2018.        | Rēķinā neiekļautā pārdošana   | Time              | Alpu slēpošanas nams | Alpu CRM | Alise Kaņepe | Projektu vadītājs   | Izrakstāms rēķins   | 8.0      | 100.00     | 800.00 |

    Šie divi ieraksti ir atsevišķi, bet saistīti ieraksti. Tie nav ne debeta, ne kredīta ieraksti.

4. Ja līgums ir saistīts ar projektu, tad, iekļaujot laika ierakstu rēķinā, entītijā **Faktiski** tiek izveidoti vēl divi ieraksti. Vispirms tiek izveidota negatīva summa par rēķinā neiekļauto pārdošanas ierakstu. Šis ieraksts būtībā atceļ rēķinā neiekļauto pārdošanas darījumu. Otrkārt, tiek izveidota transakcija rēķinā iekļautajai pārdošanai. Šie ieraksti ir atsevišķi, bet saistīti ieraksti, kā arī tie nav debeta un kredīta ieraksti.

    | Dokumenta datums | Transakcijas tips | Transakciju klase | Klients         | Līgums   | Resurss     | Resursa loma | Norēķinu tips | Daudzums | Vienības cena | Summa   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 4.2.2018.        | Rēķinā neiekļautā pārdošana   | Time              | Alpu slēpošanas nams | Alpu CRM | Alise Kaņepe | Projektu vadītājs   | Izrakstāms rēķins   | - 8,0    | 100.00     | - 800,00 |
    | 4.2.2018.        | Rēķinā iekļautā pārdošana     | Time              | Alpu slēpošanas nams | Alpu CRM | Alise Kaņepe | Projektu vadītājs   | Izrakstāms rēķins   | 8.0      | 100.00     | 800.00   |

Entītija **Transakcijas izcelsme** reģistrē ieraksta **Faktiski** izcelsmi, un entītija **Transakcijas savienojums** reģistrē ieraksta **Faktiski** saistītos ierakstus. Turklāt ieraksts **Faktiski** ietver atsauces uz projektu, projekta līgumu (pasūtījumu), rezervējamo resursu un klientu.

![Shēma, kurā parādītas transakciju savienojumu, izcelsmes un faktiskās relācijas](media/PS-Reporting-image6.png "Shēma, kurā parādītas transakciju savienojumu, izcelsmes un faktiskās relācijas")


[!INCLUDE[footer-include](../includes/footer-banner.md)]