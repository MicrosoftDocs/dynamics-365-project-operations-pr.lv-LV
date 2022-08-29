---
title: Projekta statusa sinhronizēšana, lai novērstu iekļūšanu slēgtos projektos
description: Šajā rakstā ir paskaidrots, kā sinhronizēt projekta statusu, lai novērstu iekļūšanu neaktīvos vai slēgtos projektos.
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Projekta statusa sinhronizēšana, lai novērstu iekļūšanu slēgtos projektos

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

## <a name="scenario"></a>Situācija

Contoso ir pieejams pakalpojumā Microsoft Dynamics 365 Project Operations, lai iegūtu scenārijus, kuros nav resursu/krājumu. Parastās uzņēmējdarbības ietvaros projektus var pabeigt vai apturēt. Jūs varat deaktivizēt projektu, lai nodrošinātu, ka netiek ģenerēti izdevumi vai rēķini.

## <a name="solution"></a>Risinājums

### <a name="prerequisites"></a>Priekšnoteikumi

-   Microsoft Dynamics 365 Finance 10.0.29 vai jaunāka versija ir jāinstalē.
-   Duālās rakstīšanas karšu 1.0.0.3 projektiem V2 (msdyn\_ projekti) ir jāinstalē vai jākonfigurē manuāli, kā aprakstīts tālāk.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Project Operations integrācijas projektu V2 divrakstu kartes atjauninātas versijas izveide

Lai atjauninātu Project Operations Projects V2 divrakstu karti:

1. Dodieties uz darbvietu **Datu pārvaldība** un atlasiet **Dubultā rakstīšana**.
2. **Atlasiet elementu Dubultā rakstīšana**.
3. Kolonnā T **tabulas karte** atrodiet un atlasiet **Project V2 (msdyn\_ projekti)** un pēc tam atlasiet Stop( Stop).
4. Atlasiet kartes nosaukumu, lai atvērtu karti, un pēc tam atlasiet **[Nav]**.
5. Dialoglodziņā Kolonnas atlasīšana atlasiet **Statecode \[Project Status\]** un pēc tam atlasiet Labi. Filtra vērtībā var ierakstīt **stāvokli**, lai sašaurinātu sarakstu.
6.  Atlasiet **Pievienot vai rediģēt transformāciju** **kolonnā kartes tips**, lai rediģētu transformāciju.
7.  No **transformācijas tipa** atlasiet **ValueMap**.
8.  Atlasiet **Pievienotās vērtības kartēšana** un pēc tam pievienojiet šādus **taustiņus** un **vērtības**:

   Taustiņš       | vērtība 
   ----------|-------
   InProcess | 0     
   Pabeigts | 1     

![Ekrānuzņēmums, kurā redzama dubultās rakstīšanas kartēšana](media/projectstage-dw-mapping.png)

9. Atlasiet **Saglabāt**.
10. Lapas Duālā rakstīšana > projekti V2 (msdyn_projects) **augšdaļā** atlasiet **Saglabāt kā**.
11. Laukā **Publisher** sadaļā Pievienot tabulu **atlasiet** **CDS noklusējuma izdevējs**.
12. Iestatiet **lauku Versija** uz 1.0.0.3.
13. **Ierakstiet apraksts** un pēc tam atlasiet **Saglabāt**.
14. Lapas Dual-write > Projects V2 (msdyn_projects) augšdaļā **atlasiet** Palaist **, lai sāktu karti, un pēc tam atzīmējiet** Jā **, ja pirms skrējiena** tiek lūgts apstiprināt. 

### <a name="close-a-newly-completed-project"></a>Tikko pabeigta projekta slēgšana

Dynamics 365 Finance izmanto **lauka Projekta posms**, lai atšķirtu procesā esošus **vai** pabeigtus **projektus**. **Pabeigtajiem** projektiem nevar rasties izdevumi vai par tiem nevar izrakstīt rēķinus klientiem.

1. Atveriet projektu, lai deaktivizētu.
2. Lentē atlasiet **Deaktivizēt**.

> [!NOTE]
> Varat deaktivizēt vai aizvērt projektu, jo tie abi darbosies vienādi finance kontekstā.

3. Programmā Finance atveriet **saraksta** lapu Visi projekti.
4. Pārliecinieties, vai deaktivizētais projekts netiek rādīts sarakstā.
5. **Filtru Rādīt projektus** virs saraksta mainiet vērtību no **Aktīvs** uz **Visi**.
6. Tagad tiks parādīts deaktivizētais projekts.

Ja mēģināt reģistrēt laiku vai izdevumus saistībā ar šo projektu programmā Finance, jums nevajadzētu redzēt projektu atlasei. Ja manuāli ievadīsit projekta numuru par izdevumiem, tiks parādīts ziņojums, piemēram, "Pabeigts projekta posms neļauj ierakstīt projektā". Rēķinu izrakstīšanas un citas norēķinu funkcijas ir jāatspējo, jo tās būs slēgta projekta kontekstā.

