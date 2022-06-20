---
title: Jaunumi 2020. novembrī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem
description: Šajā rakstā sniegta informācija par kvalitātes atjauninājumiem, kas pieejami 2020. gada novembra projekta operāciju laidienā uz resursiem/neuzkrātiem scenārijiem.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b98c968a040c14f4d11c350885e2cbb984596c48
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923427"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Jaunumi 2020. novembrī — Project Operations scenārijiem, kas ir balstīti uz resursiem/bez krājumiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Šis raksts attiecas uz šādiem Dynamics 365 Project Operations komponentiem un versijām:

- Project Operations CDS vides versijā 4.4.0.70
- Projektu vadība un uzskaite Dynamics 365 Finance vides versijā 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Atjauninājumi Project Operations scenārijiem, kas balstīti uz resursiem/bez krājumiem

### <a name="project-operations-on-cds"></a>Project Operations pakalpojumā CDS

| Līdzekļu apgabals                 | Atsauces numurs | Kvalitātes atjauninājums                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Iespēju pārvaldība       | 2036993          | Uzvarējušajā piedāvājumā novērtējuma rinda un resursa piešķīruma līguma rindas tiek atjauninātas, ja piedāvājuma rindas veids ir **Visi uzdevumi**.                                                 |
| Cenu noteikšana un norēķini          | 2070392          | Rēķinā projekta līguma rindas tiek palielinātas ikreiz, kad tiek atlasīts vienums **Atsvaidzināt rēķina darbības**.                                                                         |
| Projektu plānošana             | 2043336          | Nevar dzēst projekta darba grupas dalībnieka ierakstu.                                                                                                                                  |
| Projektu plānošana             | 2046013          | Nekonsekventa uzvedība attiecībā uz aprēķinu atzīmi kolonnām ielādes laikā pret laika posma veida maiņu.                                                                                   |
| Projektu plānošana             | 2046647          | Sākuma un beigu laiks tiek izslēgti pēc stundas, kad no projekta darba grupas dalībniekiem tiek ģenerētas resursu prasības.                                                                      |
| Projektu plānošana             | 2053879          | (Saskaņā ar gaidāmo CDs izvēršanu) PublishUnassignedAssignments pārtrauc mēģinājumus saglabāt uzdevumu, kad rodas kļūda "ConditionOperator.In nodotā vērtība ir tukša."                       |
| Projektu plānošana             | 2055501          | Atstājot ierakstu **Projekta sākuma datums** tukšu, radīsies grafika kļūme.                                                                                                      |
| Projektu plānošana             | 2066817          | Cilnē **Uzdevumi**, izmantojot personu atlasi, nevar izveidot vispārīgu resursu.                                                                                                   |
| Projektu plānošana             | 2067034          | Lapā **Detalizēta informācija par uzdevumu** nav pieejama poga **Skatīt detalizētu informāciju**.                                                                                                       |
| Resursu pārvaldība          | 2046667          | Vispārējie komandas dalībnieki netiek izdzēsti pat pēc visu resursu izmantošanas.                                                                                                    |
| Laiks un ātra izdevumu ievade | 2047499          | Poga **Jauns** lapā Laika ieraksts atver lapu **Jauns e-pasta paraksts**.                                                                                               |
| Laiks un ātra izdevumu ievade | 2059859          | Veidojot izdevumu ierakstu, tiek atvērts negaidīts uznirstošais logs.                                                                                                                         |
| Cita                        | 2044181          | (Pirkuma pasūtījuma atinstalēšana) — Mēģinot atinstalēt msdyn_ProjectServiceCore_Patch un msdyn projekta pakalpojumu pamata risinājumus, rodas kļūda "Ieraksts nav pieejams".  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektu vadība un grāmatvedība Dynamics 365 Finance

| Līdzekļu apgabals        | Atsauces numurs | Kvalitātes atjauninājums                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ieņēmumu atzinība | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Projekta tāmes procentuālās attiecības aizpildīšana ir nepareiza, ja aizpildīšanas metodei līgums izmanto ārvalstu valūtu un darba norises procentuālo attiecību.                     |
| Ieņēmumu atzinība | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Nevar grāmatot budžetus ar **Faktisko izmaksu** pabeigšanas metodi.                                                                                                    |
| Ieņēmumu atzinība | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Likvidēšana neizdodas, jo rodas dokumenta disbalansa kļūda, ja uzņēmuma valūta un transakcijas valūta atšķiras.                                              |
| Izdevumu pārvaldība  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Lietotājiem, kas nav administratori, uzmeklēšanas vērtības izdevumu rindu kolonnas, piemēram, **Projekta ID** un **Izdevumu kategorija**, netiek rādītas pareizi datu savienotāja kadrā. |
| Izdevumu pārvaldība  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Rindu rekvizītu noklusējums netiek rādīts izmaksu kategorijām.                                                                                                         |
| Izdevumu pārvaldība  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Izdevumu integrācijā jāiekļauj rindas rekvizīti no izdevumu pārskata.                                                                                             |
| Rēķinu izrakstīšana           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Nevar grāmatot projekta rēķina piedāvājumus, jo ir parādīts kļūdas ziņojums, kurā teikts, ka FD kombinācija netika validēta.                                                    |
| Rēķinu izrakstīšana           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | **Rēķina** detalizētās informācijas lapā nevar skatīt darbības.                                                                                                              |
| Rēķinu izrakstīšana           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Rēķina priekšlikuma rindas var dzēst.                                                                                                                                  |
| Projekta uzskaite  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Izvēlnes **Prognoze** vienumi nav redzami **Projektu** saraksta lapā.                                                                                                   |
| Projekta uzskaite  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Nevar atvērt **Projekta paziņojums**   > **Darbības un prognoze**.                                                                                                       |
| Projekta uzskaite  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | Opcija **Pielāgot uzskaiti** nav iespējota projekta darbībām, par kurām ir izrakstīts rēķins.                                                                                                  |
| Projekta uzskaite  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Ja **Integrācijas** žurnāls ir iegrāmatots, informācija par uzskaiti nav iekļauta tabulā **ProjCDSActualsImport**.                                                  |
| Projekta uzskaite  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Projekta prognozes ieraksts tiek dubultots, kad noņemat un pēc tam atkārtoti pievienojat resursu piešķiršanu.                                                                            |
| Projekta uzskaite  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Atlasot projekta ID saiti, nevar atvērt CDS dziļo saišu URL.                                                                                                         |
| Projekta uzskaite  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Pakalpojumā CDS nevar atjaunināt uzdevuma sākuma datumu.                                                                                                                           |
| Projekta uzskaite  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Iespējojot līdzekli, vairākas līguma rindas nav iespējamas bez CDS integrācijas.                                                                                   |

### <a name="regulatory-updates"></a>Reglamentējoši atjauninājumi
Informāciju par finanšu un operāciju lietotņu regulatīvajiem atjauninājumiem skatiet rakstā [Regulatīvie atjauninājumi](/dynamics365/finance/localizations/regulatory-updates). Varat arī pieteikties LCS un skatīt plānotos reglamentējošos atjauninājumus, izmantojot problēmu meklēšanas rīku. Problēmu meklēšana ļauj meklēt pēc valsts, līdzekļa tipa un laidiena.


[!INCLUDE[footer-include](../includes/footer-banner.md)]