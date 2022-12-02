---
title: Project Service Automation uz Project Operations projekta plānošanas pārvēršanas process
description: Šajā rakstā sniegts pārskats par projekta pakalpojumu automatizācijas līdzekļu izmaiņām programmā Microsoft Dynamics 365 Project Service Automation līdz Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642578"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Project Service Automation uz Project Operations projekta plānošanas pārvēršanas process

Pēc tam, kad projekts ir sekmīgi atjaunināts no Microsoft Dynamics 365 Project Service Automation 3.X uz Dynamics 365 Project Operations Lite, projektu uzdevumu rediģēšana uzdevumu režģa darbu sadalījuma struktūrā (WBS) nav iespējama. Klienti varēs pārskatīt WBS izsekošanas reźǵī, kurā ir pievienoti jauni lauki, lai nodrošinātu visu ar uzdevumu saistīto informāciju. Projektiem, kuros ir nepieciešamas WBS rediģēšanas iespējas, varat izlases veidā pārvērst piemērotos projektus par jauno Project for the Web pieredzei.

## <a name="project-conversion-process"></a>Projektu pārvēršanas process

Lai pārveidotu projektu, izpildiet tālāk uzskaītās darbības.

1. Atveriet projekta galveno lapu un darbību rūtī atlasiet **Pārveidot**.
1. Parādītajā apstiprinājuma lodziņā atlasiet vienumu **Labi**, lai uzsāktu projekta pārveidi. Notiek tālāk uzskaitītās darbības:

    1. Ziņojuma josla, kas tiek rādīta projekta galvenajā lapā: "Projekta grafiks tiek pārvērsts. Kamēr pārvēršana nav pabeigta, projekta izmaiņas nevar veikt."
    1. Jūs tiekat novirzīts uz projektu sarakstu.

    Pēc projekta pārvēršanas pabeigšanas tiek veiktas šādas darbības:

    1. Piešķirtais projekta vadītājs saņem paziņojumu lietojumprogrammas labajā pusē.
    1. Ziņojumu josla, kurā ir noteikts, ka notiek pārvēršana, ir noņemta.
    1. Cilnē **Grafiks** ir parādītas jaunās plānošanas iespējas, izmantojot Project for the Web. Jebkurš lietotājs, kam ir atbilstošas licences un drošības lomas, var rediģēt šo WBS.
    1. Lauks **Plānošanas programma** tiek atjaunināts uz **Project for the Web**.
    1. Poga **Pārvērst** tiek noņemta no darbību rūts.

> [!IMPORTANT]
> Nav atļauta projektu lielapjoma pārvēršana. Visi mēģinājumi vienlaikus atjaunināt lielu projektu apjomu tiks droselēta. Šis ierobežojums palīdz nodrošināt augstu veiktspēju visiem klientiem.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuālie uzdevumi pret automātiskajiem uzdevumiem

Kad vide tiek jaunināta no Project Service Automation uz Project Operations, visi WBS uzdevumi tiek uzskatīti par automātiski ieplānotiem. Project for the Web nav pieejams manuāli ieplānotu uzdevumu jēdziens. Tomēr vēlamo plānošanas scenāriju saviem projektiem var definēt, izmantojot [plānošanas režīma](/project-management/scheduling-modes.md) iestatījumu, izveidojot jaunus projektus.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Ierobežotas operācijas pirms pārvēršanas projektiem

Šajā sadaļā ir aprakstītas funkcionālas atšķirības, kuras var sagaidīt, ja projekti nav pārvērsti.

### <a name="copy-project"></a>Projekta kopēšana

**Kopēšanas** operācija tiek atbalstīta tikai pārvērstajiem projektiem. Jauninātos projektus pirms pārvēršanas nevar kopēt.

### <a name="move-project"></a>Projekta pārvietošana

Projekta sākuma datuma maiņa proporcionāli nepārvirzīs uzdevumu sākumu, ja vien projekts nav pārvērsts.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Kādas ir atšķirības starp pārvērstajiem projektiem un jaunajiem projektiem, kas izveidoti pēc jaunināšanas pabeigšanas?

Projektiem, kas tiek pārvērsti pēc vides jaunināšanas, tiks iestatīts karodziņš, kas norāda, ka grafikā tiek ievērots tikai projekta kalendārs. Šī darbība atbilst Project Service Automation scenārijam. Tomēr karodziņš netiks iestatīts jauniem projektiem, kas tiks izveidoti pēc jaunināšanas. Tāpēc, kad resursi ir piešķirti uzdevumam, grafikā tiek ievērots resursu darba laiks.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Ko darīt, ja neizdodas pārvērst savu projektu?

Ja projekta pārvēršana neizdodas, vispirms ir jāpārskata kļūdu žurnālus, lai identificētu biežāk izplatītās problēmas, kas saistītas ar jūsu WBS. Ja žurnāli neuzrāda konkrētu kļūdu, kurai varat veikt darbību, sazinieties ar klientu atbalsta dienestu, lai jūsu lietu varētu izskatīt tālāk.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kā Project for the Web tiek apstrādāta uzņēmuma slēgšana?

Project for the Web neņem vērā uzņēmuma slēgšanu, ko uzņēmums definējis organizācijas līmenī. Taču tiks ņemti vērā citu brīvdienu tipi, kas definēti noteiktajā darba stundu veidnē.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Kādi ir Project for the Web ierobežojumi?

Skatiet [Izveidot darba sadalījuma struktūru: projekta ierobežojumi](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Vai varu sagaidīt izmaksu un pārdošanas aprēķinu izmaiņas?

Retos gadījumos, kad resursu piešķires kontūras tiek pārrēķinātas vai ja to datumu robežas atšķiras no avotprojekta, var tikt rādītas pārdošanas un izmaksu aprēķinu atšķirības. Jaunināšanas procesa ietvaros klientiem paredzams reprezentatīvu projekta kopu tests, lai viņi varētu izprast iespējamas izmaiņas grafikā.
