---
title: Jaunumi 2021. janvārī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2021. gada janvāra laidienā Project Operations resursu/bez krājumu scenārijiem.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24a6f3b49b9c67b7c2d97461ab0f23a9a704dbc7
ms.sourcegitcommit: ef7d498bf80b0bcc1245dc42f30c410c31f891bb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/13/2021
ms.locfileid: "4958931"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2021. janvārī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_


Šī tēma attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

  - Project Operations Dataverse vides versijā 4.6.0.154
  - Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.16

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| **Izvietošana un konfigurācija** | 2106818 | Tīmekļa resursa pārdēvēšana, kas radīja problēmas ar lapas pielāgošanu tika novērsta. |
| **Cenu noteikšana un norēķini** | 2091908 | Novērsta **Cenu noteikšanas bloķēšanas** un **Pašreizējās cenu noteikšanas izmantošanas** opciju lietošana lapā **Rēķins**, ja Project Operations instalē kopā ar Dynamics 365 Field Service. |
| **Cenu noteikšana un norēķini** | 2103058 | Atsvaidzinātas **Projekta kopsummas**, lai apstrādātu uzdevuma faktisko izmaksu tukšās vērtības. |
| **Cenu noteikšana un norēķini** | 2116100 | Uzlaboti kļūdu ziņojumi, kas izmantoti ar funkcionalitāti **Labot ierakstu faktiskajiem datiem**. |
| **Cenu noteikšana un norēķini** | 2116129 | Uzlabota izdevumu aprēķinu redzamība lapas **Projekti** cilnē **Aprēķini**. |
| **Cenu noteikšana un norēķini** | 2119112 | Salabota faktiskās pārdošanas un faktisko izmaksu apkopošana, ja tiek izmantoti atšķirīgi valūtas kursi. |
| **Cenu noteikšana un norēķini** | 2134705 | Novērsta kļūda "Nevar lasīt rekvizītu **getResourceString** no nedefinētajiem", kad tiek atvērta lapa **Rēķins** un ir uzinstalēts Field Service. |
| **Iespēju pārvaldība** | 2022195 | Uzdevuma norēķinu režģis lapā **Projekts** ietver ikonu, kas norāda, ka ar šo uzdevumu ir saistīts līgums vai piedāvājums. |
| **Iespēju pārvaldība** | 2029135 | Novērsta biznesa procesa kļūda, kas rodas, ja lietotājs mēģina atvērt rēķina rindu apstiprinātā rēķinā, kurā ir iekļauta avansa summa. |
| **Iespēju pārvaldība** | 2040713 | Novērsta skripta kļūda, kas rodas, izveidojot rēķinu no līguma un ir instalēts Field Service. |
| **Projektu plānošana un izsekošana** | 2090202 | Tās biznesa kārtulas, kuras vairs neizmanto, tiek atzīmētas kā **Novecojušas**. |
| **Laiks un izdevumi** | 2091249 | Pastiprināta kontrole, lai lietotāji nevar mainīt uzdevumu iesniegtā vai apstiprinātā laika ierakstā. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Pārskats par projektu pārvaldību un uzskaiti pakalpojumā Dynamics 365 Finance

| **Līdzekļu apgabals** | **Atsauces numurs** | **Kvalitātes atjauninājums** |
| --- | --- | --- |
| **Projektu pārvaldība un uzskaite** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Nepareiza līguma summa lapā **Starpkonts** fiksētas cenas projektam ar vairākiem finansējuma avotiem. |
| **Projektu pārvaldība un uzskaite** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Vietturis **Invoiceproposal.PSAnfRefProjId** nerāda projekta ID darbplūsmai, **Pārskatīt projekta rēķina priekšlikumus**. |
| **Projektu pārvaldība un uzskaite** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Tiek izmantots nepareizs skaidras naudas atlaides datums, izliekot projekta rēķina priekšlikumus. |
| **Projektu pārvaldība un uzskaite** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Piešķiru noņemšana un lasīšana programmā Project Operations dublējas ar Finance projekta prognožu ierakstiem. |
| **Projektu pārvaldība un uzskaite** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Programmā Project Operations jūs nevarat izveidot projekta aprēķinus pakalpojumā Dataverse, ja projektam nav līguma rindas. |
| **Projektu pārvaldība un uzskaite** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Projekta izdevumu transakcijas finanšu dimensija nav sinhronizēta ar saistīto dokumentu un izdevumu atskaites uzskaites sadali, kad izmaksas tiek izliktas bilancē. |
| **Projektu pārvaldība un uzskaite** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | **Rēķina statusa** filtrs fiksētas cenas projektu grāmatotajām projekta transakcijām nedarbojas. |
| **Projektu pārvaldība un uzskaite** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Apgriezto aprēķinu korekcijas nedarbojas sadaļā **Periodisks**. |
| **Projektu pārvaldība un uzskaite** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Rēķina priekšlikuma rindas Project Operations nevar dzēst, ja integrēts ar Dataverse. |
| **Projektu pārvaldība un uzskaite** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Novērsta vairāku līguma rindu funkciju iespējošana bez Dataverse integrācijas. |
| **Projektu pārvaldība un uzskaite** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Ja starpkontu rēķini ir vienādi ar peļņu un zudumu, rēķinā iekļautā peļņa aprēķinu lapā tiek uzskaitīta kā nulle. |
| **Projektu pārvaldība un uzskaite** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Rēķina korekcijas nedarbojas integrētās vidēs. |
| **Projektu pārvaldība un uzskaite** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Izliekot NP — pārdošanas vērtību grāmatošanas funkcija, izrakstot starpuzņēmumu projektā rēķinu, atlasa nepareizu uzņēmumu. |
| **Projektu pārvaldība un uzskaite** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | Programmā Project Operations atkarības no aprēķinu uzdevumiem programmā Dataverse nevar atjaunināt. |
| **Projektu pārvaldība un uzskaite** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Atkārtoti dzēšot Project Operations integrācijas žurnālus programmā Finance, tiek zaudēti dati. |
| **Projektu pārvaldība un uzskaite** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Izliekot projekta rēķina priekšlikumu, rodas šāda kļūda: "Transakcija nesaskan ar atskaites valūtu, ja tiek pievienots noņemtais avansa rēķins." |
| **Projektu pārvaldība un uzskaite** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Ieturējumos tiek iekļauts nepareizs projekta ID pēc tam, kad noklusējuma projekta līgums ir atjaunināts Project Operations. |
| **Projektu pārvaldība un uzskaite** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Aprēķinu un peļņas atpazīšanu nevar pabeigt, ja ir iespējots Project Operations. |
| **Projektu pārvaldība un uzskaite** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Programmā Project Operations, noņemot projektu no līguma, netiek atiestatīts līguma noklusējuma projekts. |
| **Projektu pārvaldība un uzskaite** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Programmā Project Operations starpuzņēmumu rēķinā sarakstā **Pievienot rindu** tiek rādītas nepareizās izdevumu rindas. |
| **Komandējumi un izdevumi** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Izmaksu rindas nevar izlikt, jo līguma rindā trūkst stundu iestatījuma. |
| **Komandējumi un izdevumi** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Ja projekta/kategorijas validācija ir obligāta, ar projektu saistītās izdevumu kategorijas nav redzamas izdevumu atskaitē. |
| **Komandējumi un izdevumi** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Skaidrās naudas avansa bilance netiek atjaunināta, ja izdevumu atskaiti izliek pēc rindas. |
| **Komandējumi un izdevumi** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Darbs **Atjaunināt maksājuma informāciju** neizdodas pēc saistīto darbību apgriešanas, kurās rēķinu sedza ar divām vai vairākām maksājumu transakcijām. |
| **Komandējumi un izdevumi** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Ir problēma ar pēdējās dienas maltītes samazinājuma aprēķinu katrai dienasnaudas izmaksu kategorijai. |
| **Komandējumi un izdevumi** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Atskaite **Izmaksu veids katram darbiniekam** nerāda uzskaitītos izdevumus, ja lietotāja pirmais savienojums bija es-MX valodā. |
| **Komandējumi un izdevumi** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Pārdevēja maksājums par izdevumu atskaites rēķinu izmanto nepareizu kopsavilkuma kontu seguma izlikšanai. |
| **Komandējumi un izdevumi** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Ja izdevumu atskaiti iegrāmatoto ar iespējotu opciju **Atļauj transakciju grupēšanu, pamatojoties uz nobīdes maksājumu kontu** un **Labojams uzskaites datums grāmatošanas laikā**, redzamie uzskaites datumi nav grupēti tabulā **Uzskaites sadale**, kas ietekmē pārdošanas nodokļu ierakstus. |
| **Komandējumi un izdevumi** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Izdevumu apakškategorijas kartēšana tiek noņemta, ja tiek notīrīta un atkal atlasīta izvēles rūtiņa Izmantot izdevumus. |
| **Komandējumi un izdevumi** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Nevar izveidot starpuzņēmumu atskaiti, ja projekta ID tiek pievienots virsraksta līmenī. |
| **Komandējumi un izdevumi** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Rodas problēma ar izdevumu maksājumiem, ja izdevumu summa pārsniedz skaidrās naudas avansa summu. |
| **Komandējumi un izdevumi** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Lauks **Projekta ID** informācija starpuzņēmumu izdevumu atskaitē nav norādīts, ja lietotāja loma ir piešķirta noteiktai organizācijai. |
| **Komandējumi un izdevumi** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Izdevumu kategorija ir bloķēta, ja pievieno jaunu izdevumu rindu. |
| **Komandējumi un izdevumi** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Uzskaitītās izdevumu atskaites rindas, kuras jau ir atdalītas, rada nepilnīgi izlikto debitora/Virsgrāmatas dokumentu. Tā kā **TRVEXPTRANS.SOURCEDOCUMENTLINE** dublējas, tiek pārtraukts arī Uzskaites avota pārlūks. |
| **Komandējumi un izdevumi** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Indekss, kas pievienots tabulā **TRVREQUISITIONLINE**, kurai klientam ir dublikāti, atjaunināšanas laikā rada kļūdu. |
| **Komandējumi un izdevumi** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Programmā Project Operations laiku ar starpuzņēmuma uzdevumiem pakalpojumā Dataverse nevar izveidot vai apstiprināt. |

## <a name="regulatory-updates"></a>Reglamentējoši atjauninājumi

Informāciju par reglamentējošajiem atjauninājumiem programmās Finance and Operations skatiet sadaļā [Reglamentējošie atjauninājumi](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Varat arī pieteikties LCS un skatīt plānotos reglamentējošos atjauninājumus, izmantojot problēmu meklēšanas rīku. Problēmu meklēšana ļauj meklēt pēc valsts, līdzekļa tipa un laidiena.
