---
title: Projekta darba grupas izveide
description: Šajā rakstā sniegta informācija par to, kā izveidot un pārvaldīt projektu grupas.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9df8b3ee9b42a33c6031c78ff3673cad47bfe6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927337"
---
# <a name="create-a-project-team"></a>Projekta komandas izveide

[!include [banner](../includes/banner.md)]

Lai izmantotu projektā iepriekš iestatītās lomas, projekta vadītājam šīs lomas ir jāsaista ar projektu. Projektam var piešķirt vairākas lomas. Lai izvairītos no pārpratumiem, šīs lomas rezervācijas laikā tiek automātiski apzīmētas. Piemēram, ja projekta vadītājam ir nepieciešami trīs programmatūras inženieri, tiek automātiski ģenerētas trīs programmatūras inženieru lomas, kurām ir etiķetes **programmatūras inženieris 1**, **programmatūras inženieris 2** un **programmatūras inženieris 3**. Ja lomai tika iepriekš iestatīti lomu raksturlielumi, tās resursa meklēšanas laikā tiek piemērotas kā filtrs. Lai precizētu meklēšanu, var pievienot papildu raksturlielumus.

Lai nodrošinātu labāku skatu uz resursu pieejamību, var arī pielāgot skatīšanas iestatījumus. Ir pieejamas opcijas rādīt stundas, dienas, nedēļas, mēneša, ceturkšņa un gada pieejamību. Ir arī opcija rādīt pieejamo un atlikušo resursu noslodzi. Šī opcija ir noderīga laika pārvaldībā, ja aprēķināt darbībām pieejamo laiku vai resursu pieejamību.

Projekta vadītājs var lapā atlasīt lomu un pēc tam, ja ir pieejams resurss, kas atbilst prasībai, atlasīt rezervēt resursu lomas izpildei. Ņemiet vērā, ka šajā plānošanas posma brīdī resursi jārezervē. Izveidojot WBS, varat aizstāt lomas ar projekta personāla resursiem. Ja lomas WBS aizstāj ar personāla resursiem, resursa iestatījums automātiski atjaunina projekta darba grupu sarakstu un plānu.

[![Projekta darba grupu uzskaitījums, kas ietver gan lomas, gan faktiskos resursus.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projekta vadītājam ir dažādas opcijas resursa rezervēšanai projektam, piemēram, **Atlikusī noslodze**, **Pilna noslodze**, **Noslodzes daļa** un **Konkretizēt laiku**. Šīs rezervācijas opcijas var atcelt jebkurā laikā, ja resursu piešķires mainās. Tiek atbalstītas divu veidu rezervācijas:

- **Stingrā rezervācija** — Resursa rezervācija tika apstiprināta darbam ar iesaisti uz konkrēto ilgumu.
- **Vieglā rezervācija** — Resursa rezervācijas tika provizoriski iestatītam darbam ar iesaisti uz konkrēto ilgumu.

Šajā procedūrā paskaidrots, kā izveidot projekta komandu.

## <a name="create-a-project-team"></a>Projekta komandas izveide

1. Saraksta lapā **Visi projekti** atlasiet projektu un pēc tam atlasiet **Rediģēt**.
2. Lauka **Plānot beigu datumu** cilnē **Projekta komanda un plānošana** ievadiet grafika sākuma datumu, pieskaitot vienu mēnesi. Piemēram, ja grafika sākuma datums ir 2017. gada 24. jūnijs (24/06/2017), ievadiet **24/07/2017**.
3. Atlasīt **Pievienot**.
4. Lauka **Loma** rūtī **Pievienot lomas projektam** atlasiet **Vecākais projektu vadītājs**.
5. Atlasiet **Nepieciešamās kompetences**.
6. Lapā **Izvēlieties raksturlielumus** pēc noklusējuma tiek atlasīti raksturlielumi, kurus iepriekš iestatījāt vecākā projektu vadītāja lomai. Atlasiet **Labi**.
7. Lauka **Resursu skaits** lapā **Pievienot projektam lomas** ievadiet **1**.
8. Laukā **Resurss** uzmeklēšana rāda visus resursus, kuriem ir nepieciešamās kompetences. Atlasiet **Daniels Goldšmits** un pēc tam atlasiet **Izveidot**.
9. **Projekta** lapā atlasiet **Pievienot**.
10. Lauka **Loma** rūtī **Pievienot lomas projektam** atlasiet **Darba grupas dalībnieks**. Laukā **Resursu skaits** ievadiet **5**.
11. Atlasiet **Izveidot**.
12. Lapā **Projekti** atlasiet **Izpildīt resursu**.

## <a name="monitor-project-teams"></a>Projekta darba grupu uzraudzība
1. Lapā **Visi projekti** atlasiet projekta **XYZ jaunināšanas fāze 2** saiti **Projekta ID**.
2. Kopsavilkuma cilnē **Projekta komanda un plānošana** pārbaudiet, vai uzskaitītie projekta resursi ir pareizi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]