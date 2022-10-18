---
title: Project Service Automation uz Project Operations projekta plānošanas konvertēšanas procesu
description: Šajā rakstā ir sniegts pārskats par līdzekļu izmaiņām Microsoft Dynamics 365 Project Service Automation uz Dynamics 365 Project Operations.
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
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Project Service Automation uz Project Operations projekta plānošanas konvertēšanas procesu

Pēc tam, kad projekts ir veiksmīgi jaunināts no Microsoft Dynamics 365 Project Service Automation 3.X uz Dynamics 365 Project Operations Lite, projekta uzdevumu rediģēšana uzdevumu režģa darba sadalījuma struktūrā (WBS) nav iespējama. Klienti varēs pārskatīt WBS izsekošanas režģī, kur ir pievienoti jauni lauki, lai sniegtu visu informāciju, kas ir saistīta ar uzdevumu. Projektiem, kuros ir nepieciešami WBS labojumi, varat selektīvi pārvērst piemērotus projektus par jauno Project tīmekļa plānošanas pieredzei.

## <a name="project-conversion-process"></a>Projekta pārveidošanas process

Lai pārveidotu projektu, veiciet tālāk norādītās darbības.

1. Atveriet projekta galveno lapu un darbību rūtī atlasiet **Konvertēt**.
1. Apstiprinājuma ziņojuma lodziņā atlasiet **Labi**, lai sāktu projekta konvertēšanu. Notiek šādas darbības:

    1. Ziņojuma joslā, kas tiek parādīta projekta galvenajā lapā, ir teikts: "Projekta grafiks tiek pārveidots. Jūs nevarat veikt izmaiņas projektā, kamēr konvertēšana nav pabeigta."
    1. Jūs tiekat novirzīts uz projektu sarakstu.

    Kad projekta konvertēšana ir pabeigta, notiek šādas darbības:

    1. Piešķirtais projekta vadītājs saņem paziņojumu pieteikuma labajā pusē.
    1. Ziņojumu josla, kurā norādīts, ka notiek reklāmguvums, tiek noņemta.
    1. Cilnē **Grafiks** tiek rādīta jaunā plānošanas pieredze programmā Project tīmeklī. Jebkurš lietotājs, kuram ir atbilstošas licences un drošības lomas, var rediģēt WBS.
    1. Lauks **Plānošanas programma** tiek atjaunināts uz **Project tīmeklim**.
    1. Poga **Konvertēt** tiek noņemta no darbību rūts.

> [!IMPORTANT]
> Projektu lielapjoma konvertēšana nav atļauta. Jebkurš mēģinājums vienlaikus atjaunināt lielu projektu apjomu tiks ierobežots. Šis ierobežojums palīdz nodrošināt augstu veiktspēju visiem klientiem.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuāli uzdevumi salīdzinājumā ar automātiskiem uzdevumiem

Kad vide tiek jaunināta no Project Service Automation uz Project Operations, visi WBS uzdevumi tiek uzskatīti par automātiski ieplānotiem. Manuāli ieplānotu uzdevumu jēdziens nav pieejams programmā Project tīmeklim. Tomēr varat definēt vēlamo plānošanas darbību saviem projektiem, izmantojot plānošanas režīma [iestatījumu,](/project-management/scheduling-modes.md) kad veidojat jaunus projektus.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Ierobežotas darbības pirmspārveidošanas projektiem

Šajā sadaļā ir izklāstītas funkcionālās atšķirības, ko varat sagaidīt, ja projekti nav konvertēti.

### <a name="copy-project"></a>Projekta kopēšana

Kopēšanas **operācija** tiek atbalstīta tikai konvertētiem projektiem. Jauninātos projektus pirms konvertēšanas nevar kopēt.

### <a name="move-project"></a>Pārvietot projektu

Projekta sākuma datuma izmaiņas proporcionāli nepārvietos uzdevumu sākumu, ja vien projekts nav pārveidots.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Kāda ir atšķirība starp pārveidotiem projektiem un jauniem projektiem, kas tiek izveidoti pēc jaunināšanas pabeigšanas?

Projektiem, kas tiek konvertēti pēc vides jaunināšanas, tiks iestatīts karodziņš, kas norāda, ka grafikam ir jāievēro tikai projekta kalendārs. Šī darbība atbilst Project Service Automation darbībai. Tomēr karodziņš netiks iestatīts jauniem projektiem, kas tiek izveidoti pēc jaunināšanas. Tāpēc grafikā tiks ievērots resursu darba laiks, kad tie tiks piešķirti uzdevumam.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Kā rīkoties, ja manu projektu neizdodas konvertēt?

Ja jūsu projektu neizdodas konvertēt, vispirms ir jāpārskata kļūdu žurnāli, lai noteiktu visas bieži sastopamās problēmas, kas saistītas ar jūsu WBS. Ja žurnālos nav norādīta konkrēta kļūda, ar kuru varat rīkoties, sazinieties ar klientu atbalsta dienestu, lai jūsu pieteikumu varētu pārskatīt sīkāk.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kā tiek risināta uzņēmumu slēgšana programmā Project tīmeklī?

Project tīmeklī neievēro uzņēmumu slēgšanu, ko uzņēmums definē organizācijas līmenī. Tomēr tas ņems vērā citus brīvdienu veidus, kas ir definēti konkrētā darba stundas veidnē.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Kādi ir programmas Project tīmeklī ierobežojumi?

Skatiet sadaļu [Darba sadalījuma struktūras izveide: Projekta ierobežojumi](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Vai varu sagaidīt izmaiņas izmaksu un pārdošanas aprēķinos?

Retos gadījumos, kad resursu piešķīruma kontūras tiek pārrēķinātas vai ja tās atbilst datuma robežai, kas atšķiras no avota projekta, pārdošanas un izmaksu aprēķinos var tikt novērotas atšķirības. Jaunināšanas procesa ietvaros no klientiem tiek sagaidīts, ka viņi testēs reprezentatīvu projektu izlases kopu, lai viņi varētu izprast visas iespējamās grafika izmaiņas.
