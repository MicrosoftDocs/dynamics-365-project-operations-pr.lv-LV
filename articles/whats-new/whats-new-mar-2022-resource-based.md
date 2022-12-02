---
title: Jaunumi 2022. gada martā — Project Operations resursu/bez krājumu pamatotiem scenārijiem
description: Šajā rakstā ir sniegta informācija par kvalitātes atjauninājumiem, kas ir pieejami 2022. gada marta laidienā Project Operations resursu/bez krājumu scenārijiem.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910915"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2022. gada martā — Project Operations resursu/bez krājumu pamatotiem scenārijiem

*Attiecas uz: Project Operations resursos / noliktavā neesošos krājumos balstītiem scenārijiem*

Šis raksts attiecas uz šādiem Microsoft Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations Dataverse vides versijā 4.30.0.99
- Projektu pārvaldība un uzskaite Dynamics 365 Finance vides versijā 10.0.25.

## <a name="features-included-in-this-release"></a>Līdzekļi, kas ir ietverti šajā laidienā

Tagad dienasnaudas tiek atbalstītas jaunajā un pārstrādātajā modernajā izdevumu darbvietā. Uzņēmumi, kas izmanto dienasnaudas, var iespējot šo līdzekli, lai lietotājiem nodrošinātu vienkāršu veidu, kā iesniegt pieteikumus un saņemt atlīdzību par viņu dienasnaudas izdevumiem. Papildinformāciju skatiet tēmā [Dienasnauda](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations duālās rakstīšanas karšu atjauninājumi

Tālāk redzamajā sarakstā ir parādītas duālās rakstīšanas kartes, kas ir modificētas vai pievienotas Project Operations 2022. gada marta laidienā.

| **Entītiju karte** | **Atjauninātā versija** | **Komentāri** |
| --- | --- | --- |
| Project Operations integrācijas projekta piegādātāju rēķinu rindu eksportēšanas entītija msdyn\_projectvendorinvoicelines | 1.0.0.3 | Kartējumi atjaunināti, lai nodrošinātu atbilstību piegādātāja rēķina rindas entītijai programmā Dataverse. <br>Neaktivizējiet kartējuma versiju 1.0.0.4. Tā būs gatava lietošanai kopā ar Finance vides versiju 10.0.26 nākamajā ikmēneša atjauninājumā. |

Atjauninot Project Operations Dataverse risinājumu un finanšu risinājumu, vienmēr izmantojiet jaunāko kartes versiju savā vidē un iespējojiet visas saistītās tabulas kartes. Ja nav aktivizēta jaunākā kartes versija, daži līdzekļi un iespējas var nedarboties pareizi. Kartes aktīvā versija ir skatāma kolonnas **Versija** lapā **Duālā rakstīšana**. Lai aktivizētu jaunu kartes versiju, atlasiet **Tabulas kartes versijas**, atlasiet jaunāko versiju un pēc tam saglabājiet atlasīto versiju. Ja jums ir pielāgota parastā tabulas karte, lietojiet izmaiņas atkārtoti. Vairāk informācijas skatiet sadaļā [Lietojumprogrammu dzīves cikla pārvaldība](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ja rodas problēma, startējot karti, izpildiet instrukcijas, kas sniegtas duālās rakstīšanas problēmu novēršanas ceļveža sadaļā [Problēma ar trūkstošām tabulu kolonnām kartēs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kvalitātes atjauninājumi

### <a name="project-operations-on-dataverse"></a>Project Operations pakalpojumā Dataverse

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Laiks un izdevumi | 2388011 | Noraidījuma komentāru parādīšana laika ierakstu iesniedzējiem lielapjoma apstiprināšanas laikā. |
| Projektu plānošana un izsekošana | 2495294 | Projekta informāciju nedrīkst rediģēt lapā **Uzdevuma informācija**. |
| Cenu noteikšana un norēķini | 2499605 | Līgumu atskaites punkti, kas izveidoti no piedāvājumu atskaites punktiem, tiek nepareizi atzīmēti kā tikai lasāmi. |
| Projektu plānošana un izsekošana | 2506050 | Ja nav izmaiņu, ko saglabāt, operāciju kopa paliek gaidoša uz vienu stundu. Pēc tam kopa tiek nepareizi atzīmēta kā **Neizdevās**, kaut gan tā būtu jāpabeidz nekavējoties. |
| Cenu noteikšana un norēķini | 2507401 | Noklusējuma līgumslēdzējas vienības tiek nepareizi ievadītas projektos nepareizas kešdarbes dēļ. |
| Cenu noteikšana un norēķini | 2541660 | Opcija **Pārdošanas pasūtījumu izveides apstiprināšana** duālajā rakstīšanā ir paredzēta tikai uz projektiem balstītiem pasūtījumiem. |
| Cenu noteikšana un norēķini | 2552745 | Nodokļi netiek sadalīti starp klientiem, kuri ir iestatījuši dalītu norēķinu kārtulas. |
| Cenu noteikšana un norēķini | 2558859 | Uzlaboti kļūdu ziņojumi, iestatot izcenojuma dimensijas. |
| Cenu noteikšana un norēķini | 2558933 | Opcija **Importēt no projekta aprēķiniem** neizdodas, kad **msdyn\_project** tiek pievienots kā izcenojuma dimensija. |
| Cenu noteikšana un norēķini | 2559101 | Projekta parametru dzēšana nav bloķēta un izraisa problēmas. |
|   Iespēju pārvaldība | 2570390 | Duālās rakstīšanas spraudnis liek iestatīt piedāvājumos, pasūtījumos un iespējās konta tipu **Klients**, pat ja šis konta tips nav pareizs. |
| Cenu noteikšana un norēķini | 2586097 | Faktiskās izmaksas ar dalītajiem rēķiniem netiek atgrieztas, kad projekts tiek noņemts no projekta līguma rindas. |
| Cenu noteikšana un norēķini | 2589619 | Ierakstāmo materiālu nodoklis tiek izplatīts uz rēķinā neiekļautajām faktiskajām pārdošanām un rēķinu. |
|   Iespēju pārvaldība | 2594015 | Piedāvājumu nevar slēgt kā iegūtu klientiem, kuriem ir **Net60** maksāšanas nosacījumi. |
| Projektu plānošana un izsekošana | 2595841 | Project for the Web lietotāji saņem kļūdas ziņojumu par trūkstošu **msdyn\_actualstart**, izveidojot jaunu resursa pieprasījumu. |
| Laiks un izdevumi | 2602511 | Laika ierakstu laukā **Noraidīts** kā noraidītājs tiek rādīts **Sistēma**, nevis nosaukts lietotājs. |
| Laiks un izdevumi | 2602528 | Projekta apstiprinātājs var apstiprināt laiku projektiem, kuros viņš nav uzskaitīts kā apstiprinātājs. |
| Cenu noteikšana un norēķini | 2608550 | Korekcijas rēķinu var apstiprināt pat tad, ja oriģinālā nav izmaiņu. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektu pārvaldība un uzskaite programmā Dynamics 365 Finance

| Līdzekļu apgabals | Atsauces numurs | Kvalitātes atjauninājums |
| --- | --- | --- |
| Projektu pārvaldība un uzskaite | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Ir neatbilstība starp Finance un Project Operations attiecībā uz lauka **Kategorijas ID** atļauto garumu. |
| Projektu pārvaldība un uzskaite | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Fiksētas cenas projektus nevar likvidēt, ja lauks **Par kontu rēķinu izrakstīšanu** ir iestatīts kā **Peļņa un zaudējumi** un tiek izmantots princips **Pabeigtie procenti**. |
| Projektu pārvaldība un uzskaite | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Tiek ievadīta nepareiza noklusējuma pārdošanas nodokļu grupa no projekta iestatījuma izdevumu rindās Project Operations integrācijas žurnālā. |
| Projektu pārvaldība un uzskaite | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Nevar rediģēt projekta rēķina priekšlikuma galvenes dimensijas integrētā izvietošanā ar Project Operations. |
| Projektu pārvaldība un uzskaite | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Starpuzņēmumu piegādātāju rēķinus nevar integrēt ar Dataverse. |
| Projektu pārvaldība un uzskaite | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Klienta bilanču valūta un pārskatu valūta nesakrīt. |
| Projektu pārvaldība un uzskaite | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projekta rēķinu var grāmatot pat tad, ja klientam ir aizturēti visi rēķini. |
| Projektu pārvaldība un uzskaite | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Projektu rēķinu priekšlikumos, kuriem ir skati **Galvene** un **Rindas**, trūkst pogas **Dzēst visas rindas**. |
| Projektu pārvaldība un uzskaite | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Grāmatojot piegādātāj rēķinu, rodas šāda kļūda: “Rēķina uzskaites datumam ir jābūt tajā pašā uzskaites gadā, kurā ir saistītais iegādātais pasūtījums. Izpildiet pirkuma pasūtījuma gada beigu procesu vai mainiet datumu uz pašreizējo uzskaites gadu”. |
| Komandējumi un izdevumi | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Projekta fiksētās izmaksas netiek izlaistas pēc tam, kad tiek izlaistas ceļojuma pieprasījuma fiksētās izmaksas. |
| Komandējumi un izdevumi | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Iesniedzot izdevumu pārskatu, rodas šāda kļūda: “Steka trasēšana: Uzņēmums nepastāv.” |
| Komandējumi un izdevumi | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Noklusējuma **Projekta ID** netiek ievadīts izdevumu pārskatos, kad projektā ir atlasīts parametrs **Pieprasīt darbību žurnālam**. |
| Komandējumi un izdevumi | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Poga **Grāmatot izdevumus** nedarbojas pareizi programmā Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem. |
| Komandējumi un izdevumi | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Rodas problēma ar **Likme par jūdzi** attiecībā uz nobraukuma izdevumu pārskatu, kurā ietverti pasažieri. |
| Komandējumi un izdevumi | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Izdevumu nobraukuma likmes darbiniekiem netiek pareizi saskaitītas, kad izdevumu kategorijā **Nobraukuma likmju pakāpes** ir izmantoti divi dažādi transportlīdzekļu tipi. |
| Komandējumi un izdevumi | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Laukā **Projekts** uzmeklēšana ceļojuma pieprasījuma rindā neatgriež pareizo projektu sarakstu. |
| Komandējumi un izdevumi | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Pārskatāmais nobraukums** rāda brīdinājumu izdevumu pārskatos. |
| Komandējumi un izdevumi | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Rakstzīmju optiskā atpazīšana kvītīs (OCR) nedarbojas, jo ir radusies problēma ar izdevumu OCR pakalpojuma URL. |
| Komandējumi un izdevumi | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Ja ir iespējots līdzeklis **Iespēja ātri detalizēt periodiskos izdevumus**, summas izdevumu pārskatu detalizācijas rindās tiek mainītas katru reizi, kad tiek atvērta lapa **Uzskaitīt**. |
| Komandējumi un izdevumi | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Nevar dzēst izdevumu pārskatu, ja pagaidu sarakstam ir vairāki apstiprinātāji. |

## <a name="removed-and-deprecated-features"></a>Noņemti un novecojuši līdzekļi

Rakstā [Noņemtie vai novecojuši līdzekļi programmā Project Operations](removed-depreciated-features-project.md) ir aprakstīti līdzekļi, kas ir noņemti vai novecojuši programmā Dynamics 365 Project Operations.

- Noņemtais līdzeklis vairs nav pieejams produktā.
- Novecojis līdzeklis nav aktīvā izstrādē, un to var noņemt turpmākā atjauninājumā.

Paziņojums par līdzekļu novecošanu tiks publicēts rakstā [Noņemtie vai novecojuši līdzekļi programmā Project Operations](removed-depreciated-features-project.md) 12 mēnešus pirms jebkādu līdzekļu noņemšanas no produkta.

Svarīgām izmaiņām, kas ietekmē tikai kompilēšanas laiku, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, novecošanas laiks būs īsāks par 12 mēnešiem. Parasti tās ir funkcionālas izmaiņas, kas jāveic kompilatoram.
