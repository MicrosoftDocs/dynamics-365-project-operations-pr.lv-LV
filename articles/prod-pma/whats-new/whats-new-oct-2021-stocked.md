---
title: Jaunumi vai izmaiņas projekta operācijās, 2021. gada oktobris uz krājumiem/ražošanas scenārijiem
description: Šajā tēmā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2021. gada oktobra projekta operāciju laidienā uz krājumiem/ražošanā balstītiem scenārijiem.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818323"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Jaunumi vai izmaiņas projekta operācijās, 2021. gada oktobris uz krājumiem/ražošanas scenārijiem

_**Attiecas uz:** Project Operations scenārijiem, kas ir balstīti uz krājumiem/ražošanas pasūtījumiem_

Šī tēma attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.22
 
## <a name="quality-updates"></a>Kvalitātes atjauninājumi

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
|--------------|------------------|----------------|
| Projektu pārvaldība un uzskaite | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Projekta nepabeigtie darbi (NP) un uzkrāto ieņēmumu summas netiek pareizi atsauktas, grāmatojot starpuzņēmumu debitora rēķinu. |
| Projektu pārvaldība un uzskaite | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | **Projekta slēgšanas novēršana, ja pastāv atvērto darbību** funkcionalitāte, nedarbojas. |
| Projektu pārvaldība un uzskaite | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Norēķinu klasifikācija brīva teksta rēķinā automātiski neaizpilda projektu dimensijas, ja šī funkcionalitāte ir iespējota. |
| Projektu pārvaldība un uzskaite | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Scenārijos, kas nav starpuzņēmumi, NP un uzkrāto ieņēmumu summas netiek pareizi atsauktas, grāmatojot projekta rēķinu. |
| Projektu pārvaldība un uzskaite | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debeta un kredīta vērtības tiek pārslēgtas, kad Microsoft Excel pievienojumprogramma tiek izmantota projekta izdevumu žurnālā un **lauks Korespondējošā konta tips** ir iestatīts uz **Projekts**. |
| Projektu pārvaldība un uzskaite | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Projekta darbībās grāmatotā summa ir pārspīlēta projekta pirkšanas pasūtījumā, kurā iekļauti uzkrātie krājumi un kuram ir neatskaitāmas nodokļu summas, **ja ir atzīmēta UseTax.** |
| Projektu pārvaldība un uzskaite | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistēma sadala summu starp projekta peļņas un zaudējumu pārskatiem un projekta NP pārskatiem. |
| Projektu pārvaldība un uzskaite | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Rīcībā esošie krājumi nav pareizi pēc tam, kad ir koriģēta daļēji atgrieztā krājumu vajadzība. |
| Projektu pārvaldība un uzskaite | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Resursu nosaukumi tiek dublēti projekta operācijās, kad tie tiek rediģēti programmā Microsoft Project. |
| Projektu pārvaldība un uzskaite | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Starpuzņēmumu izdevumu pārskati, kuru kreditoru starpuzņēmumu gaidas kreditora rēķina izmaksas vispirms tiek grāmatotas **projekta NP izmaksu** grāmatošanas tipā. Tomēr apstrādes laikā ar budžetu saistītās izmaksas tiek grāmatotas **projekta izmaksu** grāmatošanas tipā, nevis paredzētajā **starpuzņēmumu izmaksu** grāmatošanas tipā. |
| Projektu pārvaldība un uzskaite | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Kreditora uzkrājumu rezultāti projekta izdevumu darbībās netiek rādīti. |
| Projektu pārvaldība un uzskaite | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Darba laika uzskaites tabulai transakcijas summa ir jānoapaļo līdz noteiktam decimāldaļu skaitam visos grāmatvedības sadalījumos un virsgrāmatas žurnāla sadalījuma ierakstos. |
| Projektu pārvaldība un uzskaite | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Projekta krājumu vajadzību daudzumi tiek automātiski atjaunināti, kad plānotie pasūtījumi tiek apstiprināti. |
| Projektu pārvaldība un uzskaite | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Dokumenta numuru, darbības tipu kreditora bilanci un konta numuru nevar atsaukt pirkšanas pasūtījuma priekšapmaksas rēķinā. |
| Projektu pārvaldība un uzskaite | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Starpuzņēmumu kreditora rēķins tiek pārtraukts, ja ir ieslēgta kreditora rēķinu integrācija. |
| Projektu pārvaldība un uzskaite | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Veidojot projekta izdevumu žurnālu, izmaksu summa tiek parādīta **laukā** Kredīts. |
| Projektu pārvaldība un uzskaite | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projekta rēķinu apmaksas nosacījumi nedarbojas, kā paredzēts. |
| Projektu pārvaldība un uzskaite | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Darba laika uzskaites tabulas dokumentus var atkārtoti izmantot, ja numuru sērija ir iestatīta kā nepārtraukta. |
| Projektu pārvaldība un uzskaite | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCIJA: **Manuālās saglabāšanas summas** loģika neatbilst **automātiskās saglabāšanas summas** loģikai projekta līguma rēķina priekšlikumā. |
| Projektu pārvaldība un uzskaite | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kad kreditora ieturējums ir nodots izpildei, dokumenta grāmatošanai ir nepareizas papildu rindas. |
| Projektu pārvaldība un uzskaite | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Mainot **rēķina priekšlikuma izveides lauka Rēķina datums** **lauku**, var rasties šāda kļūda: "Objekta atsauce nav iestatīta uz objekta gadījumu." |
| Projektu pārvaldība un uzskaite | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Mēģinot apstiprināt darba laika uzskaites tabulu no **TSLine** darbplūsmas, rodas kļūda, un sestdienai un svētdienai ir darba laika uzskaites tabulas politika. |
| Projektu pārvaldība un uzskaite | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Sākotn bilances projekta krājuma tips tiek izslēgts no **rēķina priekšlikuma darbību kopsavilkumiem,** kad tiek aprēķināta rēķina priekšlikuma rēķina kopsumma. |
| Projektu pārvaldība un uzskaite | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ja projekta ražošanas pasūtījuma patēriņa izmaksas ir 0 (nulle), mēģinot novērtēt, rodas šāda kļūda: "Mēģināja dalīt ar nulli". |
| Projektu pārvaldība un uzskaite | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Project Darba laika uzskaites tabulas mobilā programma Android pārstāj reaģēt. Problēma ir saistīta ar **TimeEntryDataManager ArgumentNullException**. |
| Projektu pārvaldība un uzskaite | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Projekta operāciju integrācijas žurnāls neizdodas, to grāmatojot, jo kontā trūkst dimensiju. Tomēr konts, kam trūkst dimensiju, nav konts, uz kuru grāmatojat. |
| Projektu pārvaldība un uzskaite | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | **Meklēšanas filtrs ToDate** netiek notīrīts, kad tas tiek noņemts no **dialoglodziņa Atlasīt lapā Grāmatot** **izmaksas**. |
| Projektu pārvaldība un uzskaite | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Atiestatīt visu sadali** neizdodas un tiek parādīta kļūda darba laika uzskaites tabulās, kas izveidotas tikai laika **tipa** projektam. |
| Projektu pārvaldība un uzskaite | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Cilne Projekts nav** rediģējama gaidošā kreditora rēķinā, kad precei ir piešķirta sagādes kategorija. |
| Projektu pārvaldība un uzskaite | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Ja neesat pieteicies projekta operācijās Dataverse, trūkst navigācijas rūts. |
| Projektu pārvaldība un uzskaite | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Starpuzņēmumu projekta korekcijas darbībām mērķa uzņēmumā ir problēmas. |
| Projektu pārvaldība un uzskaite | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Projekta fiksētās izmaksas aprēķina nepareizu daudzumu un izmaksu cenu, ja pirkšanas pasūtījumu apstrādāja **pirkšanas pasūtījuma gada beigu process** Virsgrāmatā. |
| Projektu pārvaldība un uzskaite | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Ja projekta ražošanas pasūtījums, kuram ir kvalitātes pasūtījumi, tiek pabeigts, rodas šāda kļūda: "Nav virtuālas transakcijas, kas atzīmēta ar krājumu darbību." |
| Projektu pārvaldība un uzskaite | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Grāmatojot ar projektu saistītu kreditoru rēķinu, rodas šāda kļūda: "Uzskaitījuma teksts Projekts - izmaksas - krājums nepastāv." |
| Projektu pārvaldība un uzskaite | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Netiešās izmaksas tiek dubultota, manuāli uzkrājot ieņēmumus. |
| Projektu pārvaldība un uzskaite | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Uzkrāt ieņēmumus un NP grāmatošana nerada darbības. |
| Projektu pārvaldība un uzskaite | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Ja pastāv saņemts projekta pirkšanas pasūtījums, standarta izmaksu krājuma gaidošās cenas aktivizēšana neizdodas. |
| Projektu pārvaldība un uzskaite | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Rēķina grāmatošanas DIS anulētā vērtība atšķiras no sākotnēji iegrāmatotās NP vērtības laika ierakstā. |
| Projektu pārvaldība un uzskaite | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Pastāv grāmatošanas izejas plūsma projekta rēķinos iekļautajiem ieņēmumiem lietotajos aizturētāju gadījumos, kad dokumenta darbības nelīdzsvarojas. |
| Projektu pārvaldība un uzskaite | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Budžeta izveide pēc rēķina priekšlikuma grāmatošanas bloķē labojuma rindu importēšanu projekta operācijās. |
| Projektu pārvaldība un uzskaite | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Pilnībā izrakstīta starpposma ieraksta modificēšanai nevajadzētu būt iespējamai. |
| Projektu pārvaldība un uzskaite | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Ja tiek izmantotas automātiskās maksas, starpuzņēmumu debitora rēķinu darba laika uzskaites tabulai nevar grāmatot un tiek parādīts kļūdas ziņojums. |
| Projektu pārvaldība un uzskaite | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Apakšprojekta adrese nav pareizi atjaunināta. |
| Projektu pārvaldība un uzskaite | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Krājumu vajadzību izmaksu cena tiek atjaunināta ar konsolidēto pirkšanas pasūtījumu pirkšanas cenu. |
| Projektu pārvaldība un uzskaite | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Pēc pirkšanas cenas atjaunināšanas un parametra Aktivizēt izmaiņu pārvaldību aktivizēšanas iegrāmatotās izmaksas nav **pareizas**. |
| Komandējumi un izdevumi | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visus lietotāja izdevumus var redzēt, meklējot kategoriju mobilajā lietotnē Izdevumi. |
| Komandējumi un izdevumi | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepareizas summas kreditoru darbībām un PVN darbībām tiek grāmatotas no izdevumiem, kas izveidoti no kredītkartes darbības. |
| Komandējumi un izdevumi | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Atsvaidzinot izdevumu pārskata lapas, tiek parādīts neatbilstošs brīdinājuma ziņojums. |
| Komandējumi un izdevumi | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Dzēšot pagaidu apstiprinātāju un pēc tam atkārtoti iesniedzot darbplūsmu, tiek izmantots nepareizs pagaidu apstiprinātājs. |
| Komandējumi un izdevumi | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Rodas grāmatošanas kļūda, kas saistīta ar nobraukuma iestatījumiem. |
| Komandējumi un izdevumi | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Sadale neatjaunina juridisko personu, ja nepievienota darbība tiek atkārtoti pievienota izdevumu pārskatam par starpuzņēmumu izdevumiem. |

### <a name="regulatory-updates"></a>Reglamentējoši atjauninājumi

Informāciju par finanšu un operāciju programmu regulatīvajiem atjauninājumiem skatiet [sadaļā Regulatīvie atjauninājumi](/dynamics365/finance/localizations/regulatory-updates). Varat arī pieteikties, lai Microsoft Dynamics dzīves cikla pakalpojumus (LCS) un izmantotu problēmu meklēšanas rīku, lai skatītu plānotos regulatīvos atjauninājumus. Problēmu meklēšana ļauj meklēt pēc valsts vai reģiona, līdzekļa veida un izlaišanas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
