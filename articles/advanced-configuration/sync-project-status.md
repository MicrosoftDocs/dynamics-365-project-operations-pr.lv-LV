---
title: Projekta statusa sinhronizēšana, lai nepieļautu ierakstu pret slēgtiem projektiem
description: Šajā rakstā ir izskaidrots, kā sinhronizēt projekta statusu, lai nepieļautu neaktīvu vai slēgtu projektu ievadi.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348112"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Projekta statusa sinhronizēšana, lai nepieļautu ierakstu pret slēgtiem projektiem

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

## <a name="scenario"></a>Situācija

Contoso izmanto Microsoft Dynamics 365 Project Operations scenārijiem, kas ir balstīti uz resursiem/nav balstīti uz krājumiem. Kā daļu no parastām uzņēmējdarbības darbībām projektus var pabeigt vai aizturēt. Varat deaktivizēt projektu, lai nodrošinātu, ka netiek ģenerēti izdevumi vai rēķini.

## <a name="solution"></a>Risinājums

### <a name="prerequisites"></a>Priekšnoteikumi

-   Jābūt instalētai programmai Microsoft Dynamics 365 Finance 10.0.29 vai jaunākai versijai.
-   Duālās rakstīšanas karte 1.0.0.3 for Projects V2 (msdyn\_projects) ir jāinstalē vai manuāli jākonfigurē, kā aprakstīts tālāk.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Atjauninātas Project Operations integrācijas Projects V2 duālās rakstīšanas kartes versijas izveidošana

Lai atjauninātu Project Operations Projects V2 duālās rakstīšanas karti, veiciet tālāk norādītās darbības.

1. Pārejiet uz darbvietu **Datu pārvaldība** un atlasiet **Duālā rakstīšana**.
2. Atlasiet elementu **Duālā rakstīšana**.
3. Kolonnā **Tabulas karte** atrodiet un atlasiet **Project V2 (msdyn\_projekti)** un pēc tam atlasiet Apturēt.
4. Atlasiet kartes nosaukumu, lai atvērtu karti, un pēc tam atlasiet **[Nav]**.
5. Dialoglodziņā Atlasīt kolonnu atlasiet **statecode \[Project Status\]** un pēc tam atlasiet Labi. Varat ievadīt **statuss** filtra vērtībā, lai sašaurinātu sarakstu.
6.  Atlasiet **Pievienot vai rediģēt transformāciju** kolonnā **kartes tips**, lai rediģētu transformāciju.
7.  Sadaļā **Transformācijas tips** atlasiet **ValueMap**.
8.  Atlasiet **Pievienot vērtības kartēšanu** un pēc tam pievienojiet tālāk norādītās **Atslēgas** un **Vērtības**.

   Taustiņš       | vērtība 
   ----------|-------
   InProcess | 0     
   Pabeigts | 1     

![Ekrānuzņēmums ar duālās rakstīšanas kartējumu](media/projectstage-dw-mapping.png)

9. Atlasiet **Saglabāt**.
10. Lapas **Duālā rakstīšana > Projects V2 (msdyn_projects)** augšpusē atlasiet **Saglabāt kā**.
11. Sadaļā **Pievienot tabulu** laukā **Izdevējs** atlasiet **CDS noklusējuma izdevējs**.
12. Iestatiet lauku **Versija** uz 1.0.0.3.
13. Aizpildiet lauku **Apraksts** un pēc tam atlasiet **Saglabāt**.
14. Lapas **Duālā rakstīšana > Projects V2 (msdyn_projects)** augšdaļā atlasiet **Palaist**, lai sāktu kartēšanu, un pēc tam izvēlieties **Jā**, ja pirms palaišanas tiek lūgts apstiprināt. 

### <a name="close-a-newly-completed-project"></a>Nesen pabeigta projekta slēgšana

Dynamics 365 Finance izmanto lauku **projekta posms**, lai atšķirtu projektus, kas **notiek**, no projektiem, kas ir **pabeigti**. **Pabeigtiem** projektiem nevar rasties izdevumi vai par tiem nevar izrakstīt rēķinu klientiem.

1. Atveriet projektu, lai deaktivizētu.
2. Lentē atlasiet **Deaktivizēt**.

> [!NOTE]
> Varat vai nu deaktivizēt vai slēgt projektu, jo abas šīs opcijas darbojas vienādi Finance kontekstā.

3. Programmā Finance atveriet lapu **Visu projektu saraksts**.
4. Pārliecinieties, ka deaktivizētais projekts nav redzams sarakstā.
5. Filtrā **rādīt projektus** virs saraksta mainiet vērtību no **Aktīvie** uz **Visi**.
6. Tagad būs redzams deaktivizētais projekts.

Mēģinot reģistrēt laiku vai izdevumus saistībā ar šo projektu programmā Finance, projektam nevajadzētu būt redzamam atlasē. Ja projekta numuru ievadāt manuāli izdevumiem, tiek parādīts tāds ziņojums kā “Projekta pabeigšanas posms neļauj veikt projektā ierakstus”. Rēķinu izrakstīšanas un citām norēķinu funkcijām ir jābūt atspējotām, jo tās būs slēgta projekta kontekstā.

