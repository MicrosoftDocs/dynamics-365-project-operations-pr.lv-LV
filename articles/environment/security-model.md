---
title: Drošības modelis
description: Šajā tēmā ir sniegta informācija par drošības modeli programmā Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e875d1765b5038e60830d626abb5bcd61749ece1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080329"
---
# <a name="security-model"></a>Drošības modelis

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Programmā Microsoft Dynamics 365 Project Operations ir iekļauts unikāls drošības modelis, kurš ļauj izmantot uz lomām balstītu biznesa drošības modeli, kas sadarbojas ar Microsoft Office grupām. 


## <a name="security-roles"></a>Drošības lomas
Project Operations priekšgalsistēmas iespējas ietver šādas lomas:

| Loma                          | Apraksts                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Prakses pārvaldnieks              | Atbalsta starpprojektu atskaišu veidošanu.                                                                                                            | Uzņēmuma daļa              |
| Projekta apstiprinātājs              | Apstiprina laiku un izdevumus, izmantojot projektu.                                                                                                                              | Uzņēmuma daļa |
| Projekta norēķinu administrators | Izveido rēķina priekšlikumu.                                                                                                                                                 | Uzņēmuma daļa |
| Projekta vadītājs               | Izveido projekta plānu un pieprasa resursus.                                                                                                                              | Uzņēmuma daļa |
| Projekta resurss              | Darba grupas dalībnieki, kurus var rezervēt un kam var iekļaut atskaitē laiku.                                                                                                          | Uzņēmuma daļa|
| Resursu pārvaldnieks              | Visas resursu pārvaldības funkcijas, piemēram, resursu pieprasījumu un rezervāciju izpilde, ir atdalītas, lai atbalstītu hibrīdu projekta vadītāja un resursu pārvaldnieka konfigurāciju, kā arī vienotu un centralizētu resursu pārvaldnieka lomu. | Uzņēmuma daļa |


Microsoft Project tīmeklim ir šādas lomas:

| Loma           | Apraksts                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Projekta lietotājs   | Projekta sadarbības lietotājs, kas var izveidot savus projektus un apskatīt ar tiem koplietotos projektus. | Lietotājs   |
| Projekta sistēma | Pieteikuma kontekstam lietota loma. Klientiem nedrīkst izmantot šo sistēmas lomu.                                    | Globāls |

## <a name="security-enforcement"></a>Drošības ieviešana
Projekta līmenī veiktās darbības tiek veiktas pieteiktā lietotāja kontekstā. Tas nozīmē, ka, lai izveidotu, atvērtu vai dzēstu projektu, lietotājam CDS ir jābūt pieejamai piekļuvei. Piekļuvi CDS var piešķirt, izmantojot jebkuru no platformā iekļautajiem iespējamajiem mehānismiem. Piemēram, lietotājs var piekļūt projektam, ja viņam ir lielāks tvērums vai arī ir veikta konkrēta kopīgošanas darbība, kas piešķir lietotājam piekļuvi.

To ir svarīgi ņemt vērā, veidojot projektus programmā Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Moderno grupu sadarbība ar Project Operations
Project tīmeklim un Project Operations atbalsta modernās grupas sadarbībai. Lietotāji, kas pievienoti projektam, izmantojot grupu, var rediģēt projekta plānu.

Project tīmeklim automātiski pievieno lietotājus grupai pēc to piešķiršanas.

Grupas ļauj kopīgi strādāt ar projekta atļaujām un atbalsta sadarbības artefaktiem. Tālāk redzamajā digrammā ir parādīti notikumi un statusa izmaiņas, kas rodas grupas piešķiršanas procesā.

Project Operations neveido grupu, veicot netiešu darbību. Programma grupu veido, veicot skaidru grupu saspiešanas darbību.

Grupas dalībnieku meklēšana dialogā **Grupas pārvaldība** ir ierobežota tiem, kas ir iestatīti kā daļa no vides drošības grupas. Papildinformāciju skatiet tēmā [Lietotāju piekļuves vidēm kontrolēšana: drošības grupas un licences](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Grupas režīms](./media/groupsmode.png)

1. Izveidotais projekts pieder lietotājam, kas to izveidoja.
2. Projekta īpašnieks tiek atjaunināts darba grupā.
3. Īpašnieka darba grupa tiek kartēta uz norādīto vai izveidoto Office grupu.
4. Projekta sākotnējais īpašnieks tiek pievienots Office grupai.

## <a name="deployment-recommendation"></a>Izvietošanas ieteikums
Attīstoties Office grupas sadarbības modelim, tiks pievienotas funkcijas, lai laika gaitā nodrošinātu detalizētāku kontroli. Klienti, kas pašlaik izvieto Project Operations, tiek mudināti koncentrēties uz tradicionālu Microsoft Dynamics 365 drošības modeli.

Papildinformāciju skatiet tēmā [Drošība pakalpojumā Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations un Microsoft Dynamics 365 Finance drošība
Programmā Project Operations ir šādas lomas:

- Projekta vadītājs
- Projekta grāmatvedis

Papildinformāciju par drošību risinājumā Finance skatiet tēmā [Uz lomām balstīta drošība](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


