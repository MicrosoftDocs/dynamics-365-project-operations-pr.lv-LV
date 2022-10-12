---
title: Project Service Automation līdzekļu izmaiņas uz Project Operations
description: Šajā rakstā ir sniegts pārskats par līdzekļu izmaiņām Microsoft Dynamics 365 Project Service Automation attiecībā uz Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621339"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Project Service Automation līdzekļu izmaiņas uz Project Operations

Pēc tam, kad projekts ir veiksmīgi jaunināts no Microsoft Dynamics 365 Project Service Automation 3.X uz Dynamics 365 Project Operations Lite, projekta uzdevumu rediģēšana uzdevumu režģa darba sadalījuma struktūrā (WBS) nav iespējama. Klienti varēs pārskatīt WBS izsekošanas režģī, kur ir pievienoti jauni lauki, lai sniegtu visu informāciju, kas ir saistīta ar uzdevumu. Projektiem, kuros ir nepieciešami WBS labojumi, varat selektīvi pārvērst piemērotos projektus par jauno projektu tīmekļa plānošanas pieredzei.

## <a name="project-conversion-process"></a>Projekta konvertēšanas process

Lai pārvērstu projektu, veiciet tālāk norādītās darbības.

1. Atveriet projekta galveno lapu un darbību rūtī atlasiet **Konvertēt**.
1. Apstiprinājuma ziņojuma lodziņā atlasiet **Labi**, lai sāktu projekta konvertēšanu. Notiek šādas darbības:

    1. Ziņojumu joslā, kas tiek parādīta projekta galvenajā lapā, ir teikts: "Projekta grafiks tiek konvertēts. Jūs nevarat veikt izmaiņas projektā, kamēr reklāmguvums nav pabeigts."
    1. Jūs tiekat novirzīts uz projektu sarakstu.

    Kad projekta konvertēšana ir pabeigta, tiek veiktas tālāk norādītās darbības.

    1. Piešķirtais projektu vadītājs saņem paziņojumu lietojumprogrammas labajā pusē.
    1. Ziņojumu josla, kurā norādīts, ka notiek konvertēšana, tiek noņemta.
    1. Cilnē **Grafiks** tiek rādītas jaunās plānošanas iespējas saistībā ar Project tīmeklim. Jebkurš lietotājs, kuram ir atbilstošas licences un drošības lomas, var rediģēt WBS.
    1. Plānošanas programmas lauks **tiek atjaunināts uz** Project for the web **.**
    1. Poga **Konvertēt** tiek noņemta no darbību rūts.

> [!IMPORTANT]
> Projektu masveida pārveidošana nav atļauta. Jebkurš mēģinājums vienlaikus atjaunināt lielu projektu apjomu tiks samazināts. Šis ierobežojums palīdz nodrošināt augstu veiktspēju visiem klientiem.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuālie uzdevumi salīdzinājumā ar automātiskajiem uzdevumiem

Kad vide tiek jaunināta no Project Service Automation uz Project Operations, visi WBS uzdevumi tiek uzskatīti par automātiski ieplānotiem. Manuāli ieplānotu uzdevumu jēdziens programmā Project tīmeklim nav pieejams. Tomēr varat definēt vēlamo projektu plānošanas darbību, izmantojot [plānošanas režīma](/project-management/scheduling-modes.md) iestatījumu, kad veidojat jaunus projektus.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Ierobežotas darbības pirmskonversijas projektiem

Šajā sadaļā ir izklāstītas funkcionālās atšķirības, ko varat sagaidīt, ja projekti nav konvertēti.

### <a name="copy-project"></a>Kopēt projektu

Darbība Kopēšana **tiek** atbalstīta tikai konvertētiem projektiem. Jauninātos projektus pirms konvertēšanas nevar kopēt.

### <a name="move-project"></a>Pārvietot projektu

Projekta sākuma datuma izmaiņas proporcionāli nepārvietos uzdevumu sākumu, ja vien projekts nav pārveidots.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Kādas ir atšķirības starp pārveidotajiem projektiem un jauniem projektiem, kas tiek izveidoti pēc jaunināšanas pabeigšanas?

Projektiem, kas tiek konvertēti pēc vides jaunināšanas, tiks iestatīts karodziņš, kas norādīs grafikam ievērot tikai projekta kalendāru. Šī darbība atbilst darbībai programmā Project Service Automation. Tomēr karodziņš netiks iestatīts jauniem projektiem, kas tiek izveidoti pēc jaunināšanas. Tāpēc grafikā tiks ievērots resursu darba laiks, kad tie tiks piešķirti uzdevumam.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Kā rīkoties, ja mans projekts netiek pārveidots?

Ja jūsu projekts netiek konvertēts, vispirms ir jāpārskata kļūdu žurnāli, lai noteiktu visas bieži sastopamās problēmas, kas saistītas ar jūsu WBS. Ja žurnālos nav norādīta konkrēta kļūda, ar kuru varat veikt darbības, sazinieties ar klientu atbalsta dienestu, lai jūsu pieteikumu varētu pārskatīt tālāk.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kā tiek risināta uzņēmumu slēgšana programmā Project tīmeklim?

Projekts tīmeklim nerespektē uzņēmumu slēgšanu, ko uzņēmums definē organizācijas līmenī. Tomēr tas ievēros citus brīvdienu veidus, kas ir definēti konkrētā darba stundas veidnē.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Kādi ir Project ierobežojumi tīmeklim?

Skatiet rakstu [Darba sadalījuma struktūras izveide: projekta ierobežojumi](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Vai varu sagaidīt izmaksu un pārdošanas tāmju izmaiņas?

Retos gadījumos, kad resursu piešķiršanas kontūras tiek pārrēķinātas vai ja tās atrodas uz citas datuma robežas nekā avota projekts, var tikt parādītas atšķirības pārdošanas un izmaksu aprēķinos. Jaunināšanas procesa ietvaros klientiem ir jāpārbauda reprezentatīva projektu izlases kopa, lai viņi varētu saprast visas iespējamās grafika izmaiņas.
