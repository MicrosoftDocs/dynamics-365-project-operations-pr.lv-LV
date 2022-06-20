---
title: 2021. gada jūlija jaunumi — Project Operations Lite izvietošana
description: Šajā rakstā sniegta informācija par kvalitātes atjauninājumiem, kas pieejami Project Operations lite izvietošanas 2021. gada jūlija laidienā.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7964f38c1bc7a8e0440e2e922ff153fd9bede131
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913997"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>2021. gada jūlija jaunumi — Project Operations Lite izvietošana

_Attiecas uz: Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Šis raksts attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

  - Project Operations programmas Dataverse vides versijā 4.12.0.148 or 4.12.0.152.

## <a name="quality-updates"></a>Kvalitātes atjauninājumi
| **Līdzekļu apgabals**              | **Atsauces numurs** | **Kvalitātes atjauninājums**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cenu noteikšana un norēķini           | 2224046              | **Transakciju klases** lauks ir rediģējams cilnē **Piedāvājuma rindas detalizēta informācija**, bet tiek bloķēts, strādājat no lapas **Piedāvājuma rindas detalizēta informācija**.                                                                     |
| Cenu noteikšana un norēķini           | 2224400              | Darbība **Slēgt piedāvājumu kā iegūtu** neizdodas, ja piedāvājumam nav datuma atskaites punktu.                                                                                                                                    |
| Cenu noteikšana un norēķini           | 2234089              | Manuāli ievadot produkta aprakstu, pēc materiālu aprēķina daudzuma ievadīšanas tas tiek notīrīts.                                                                                                                         |
| Cenu noteikšana un norēķini           | 2234100              | Režģī **Uzdevumu norēķinu iestatījumi** nav iekļauta kolonna **Materiāli** un tās vērtība projekta cilnē **Uzdevumu norēķini**.                                                                                                       |
| Cenu noteikšana un norēķini           | 2277409              | Produkta ID nav pieejams līguma rindas detalizētajā informācijā materiālu veida rindai.                                                                                                                                        |
| Cenu noteikšana un norēķini           | 2281728              | Izveidojot līguma līniju, nevajadzīgi tiek pārvērtētas faktiskās vērtības, tādējādi ievērojami palielinot datu apjomu, kas ietekmē veiktspēju.                                                                                |
| Cenu noteikšana un norēķini           | 2298668              | Netiek noņemtas žurnāla rindas, kas saistītas ar atsauktiem un dzēstiem izdevumiem.                                                                                                                                     |
| Cenu noteikšana un norēķini           | 2300192              | Kad vairāki lietotāji rediģē rēķinu, apstiprinātā rēķinā var izveidot jaunu rēķina rindas detalizēto informāciju.                                                                                   |
| Cenu noteikšana un norēķini           | 2301569              | Rēķinus nevar izlabot, ja ir lietots \$0 summas honorārs.                                                                                                                                        |
| Cenu noteikšana un norēķini           | 2307965              | Rodas kļūda, ja kategorijas cena tiek izveidota ar trūkstošām vērtībām.                                                                                                                           |
| Cenu noteikšana un norēķini           | 2326870              | **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** rodas kļūda, ja **producttypecode** ir Null.                                                                            |
| Cenu noteikšana un norēķini           | 2332732              | Kļūda rodas, ja līguma rindas atskaites punkts tiek izveidots bez pasūtījuma rindas.                                                                                                                |
| Projektu plānošana un izsekošana | 2181094              | Projekta plānošanas API tagad atbalsta PSS žurnālus un operāciju kopu žurnālus, kas tiek glabāti 90 dienas.                                                                                                                  |
| Projektu plānošana un izsekošana | 2254201              | Etiķete **Plānošanas režīms** tiek atjaunināta ar detalizētu informāciju, kas apraksta noklusējuma loģiku.                                                                                                                                      |
| Projektu plānošana un izsekošana | 2300252              | Atbildes kešatmiņa **openProject** tiek atjaunināta un kešatmiņas atslēgā ietver marķiera īpašnieku,  **pamata URL** un **Segmenta URL**, lai **Pieprasījuma URL** vienmēr varētu tikt atkārtoti izveidots gadījumā, ja mainās **pamata URL**. |
| Projektu plānošana un izsekošana | 2301312              | **msdyn_membershipstatus** ir noņemts no skata **Projekta darba grupas dalībnieks**.                                                                                                                                        |
| Projektu plānošana un izsekošana | 2302759              | Produkti tiek nevajadzīgi ienesti cilnēs **Resursu piešķiršana**, **Aprēķini** un **Izmaksu aprēķini**.                                                                                                        |
| Projektu plānošana un izsekošana | 2308050              | **CopyProject** neizdodas šādas kļūdas dēļ: "Neizdevās iegūt marķieri, lai sazinātos ar attālo servisu".                                                                                                                           |
| Projektu plānošana un izsekošana | 2322650              | Skats **Projekta uzdevumu saraksts** ir atjaunināts, lai pēc noklusējuma parādītu uzdevuma datumu.                                                                                                            |
| Projektu plānošana un izsekošana | 2327266              | Kopējot aprēķinus, **CopyProject** ģenerē kļūdu "Atslēga nav atrasta vārdnīcā".                                                                                                      |
| Projektu plānošana un izsekošana | 2328123              | **CopyProject** ģenerē kļūdu "Neizdevās iegūt marķieri, lai sazinātos ar attālo servisu".                                                                                                                          |
| Projektu plānošana un izsekošana | 2336258              | **CopyProject** nepareizi kopē resursu pozīciju nosaukumus.                                                                                                                                                 |
| Cenu noteikšana un norēķini           | 2224476              | Lauks **Rezervējams resurss** neatbilst lietotājam, kurš ir pieteicies lapā **Materiālu lietojums**.                                                                                                            |
| Resursu pārvaldība           | 2277249              | Atjauninot resursu vajadzību, kas nav balstīta uz projektu, rodas kļūda.                                                                                                            |
| Resursu pārvaldība           | 2323869              | Resursu lietojums neatpazīst pareizi filtrētos resursus.                                                                                                                                             |
| Laiks un izdevumi              | 2176538              | Vadīklai **Laika ievade** tiek izmantoti nepareizi filtru operatori.                                                                                                                                                   |
| Laiks un izdevumi              | 2177462              | Dzēšot laika ierakstu režģī, pogu **Iesniegt**, **Atsaukt**, **Dzēst** un **Rediģēt ierakstu** statuss netiek atjaunināts kā paredzēts.                                                                                        |
| Laiks un izdevumi              | 2299985              | **TimeEntriesImportFromResourceAssignment** neuztur sākuma/beigu laiku no piešķīruma.                                                                                                  |
| Laiks un izdevumi              | 2318426              | Pēc laika ieraksta iesniegšanas bloķētus laukus joprojām var rediģēt.                                                                                                                                   |
| Laiks un izdevumi              | 2323749              | Kļūda rodas, ja izdevumi tiek izveidoti no rezervējamā resursa cilnes **Saistīts**.                                                                                                      |
| Laiks un izdevumi              | 2327678              | Izveidojot laika ierakstu no rezervējamā resursa cilnes **Saistīts**, primārais resurss netiek nodots laika ievades vadīklai.                                                                            |
| VispārīgI                       | 2296857              | Norises izsekošana ilgas darbības uzdevumiem.                                                                                                                                                                        |
| VispārīgI                       | 2253682              | Project Operations duālās rakstīšanas risinājums nav jāinstalē, ja duālās rakstīšanas kodols ir instalēts vidē bez duālās rakstīšanas saskaņošanas risinājuma.                                                |
| VispārīgI                       | 2316420              | Project Service pamata nodrošināšana neizdodas, ja tiek mainīta programmas lietotāja struktūrvienība.                                                                                                                     |
| VispārīgI                       | 2376405              | Novērsta izstrādātāja vadīta atjauninājuma problēma (kvalitātes atjauninājums ir pieejams versijā 4.12.0.152)                                                                                                                     |
