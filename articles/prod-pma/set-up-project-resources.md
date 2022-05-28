---
title: Projekta resursu iestatīšana
description: Šajā tēmā sniegta informācija par projekta resursu iestatīšanu vai pieprasīšanu.
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
ms.openlocfilehash: a9af71fe0638a5601ded3f0e80301ae5dfa198c1
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682584"
---
# <a name="set-up-project-resources"></a>Projekta resursu iestatīšana

[!include [banner](../includes/banner.md)]

Ir jāiestata kalendārs un tas jāsaista ar darbinieku vai darba ņēmēju. Tiek izmantots kalendārs, lai ieplānotu projektu un projektam rezervēto resursu darba laiku. Kalendāra iestatīšanas laikā projekta vadītāji var resursu optimizācijas ietvaros veikt resursu pielāgošanu. Atkarībā no kalendāra grafika resursiem var piemērot ierobežojumus. Kalendāru varat iestatīt lapā **Kalendāri**.

Iestatot darba ņēmēju kā projekta resursu, varat izvēlēties no darba ņēmējiem, kuri strādā uzņēmumā, kuram iestatāt resursus. Vai arī varat atlasīt darba ņēmējus no citiem savas organizācijas uzņēmumiem. Šie darba ņēmēji ir pazīstami kā starpuzņēmumu resursi.

Tālāk aprakstītajās procedūrās ir paskaidrots, kā jūsu uzņēmumā iestatīt darba ņēmēju kā projekta resursu un kā iestatīt starpuzņēmumu projekta resursu.

## <a name="set-up-a-worker-as-a-project-resource"></a>Darba ņēmēja kā projekta resursa iestatīšana

1. Lapas **Darba ņēmēji** sarakstā **Darba ņēmēji** atlasiet darba ņēmēju, kuru pievienojat kā projekta resursu, un atveriet darba ņēmēja ierakstu.
2. Darbību rūtī atlasiet **Projekts**&gt; **Iestatīšana** &gt; **Projekta iestatīšana**.
3. Atlasiet kalendāru un pēc tam aizveriet lapu.

Resursam noklusējuma projektus var arī norādīt kā iepriekšējas piešķiršanas tipu. Iepriekšējo piešķiri var izmantot, ja resursu pārvaldnieks vai projekta vadītājs iepriekš zina, ar kuriem resursiem projekts strādās. Iepriekšējo piešķiri var arī balstīt projekta sponsora vai klienta pieprasījumā. Lai iepriekš piešķirtu projektu, lapas **Piešķirt projektu** cilnes **Projekti** sarakstā **Atlikušie projekti** atlasiet atbilstošo projektu.

## <a name="set-up-an-intercompany-resource"></a>Starpuzņēmumu resursa iestatīšana

Iestatot darba ņēmēju kā starpuzņēmumu resursu, iestatīšana ir jāizpilda gan gan patapinošajam uzņēmumam, gan uzņēmumam, kas aizņemas.

### <a name="in-the-lending-company"></a>Patapinošajā uzņēmumā

1. Risinājumā Finance pārbaudiet, vai ir atlasīts patapinošais uzņēmums, un pēc tam izpildiet iepriekšējā sadaļā "Darba ņēmēja kā projekta resursa iestatīšana" aprakstītās darbības.
2. Lapā **Starpuzņēmumu uzskaite** atlasiet **Jauna**.
3. Laukā **Juridiskās personas ID** atlasiet patapinošo uzņēmumu. Atbilstoši aizpildiet atlikušos laukus un pēc tam atlasiet **Saglabāt**.
4. Lapā **Pārnest cenu** atlasiet **Jauna**.
5. Laukā **Juridiskā persona, kas aizņemas** atlasiet atbilstošo uzņēmumu.
6. Lai patapinātu uzņēmumam, kas aizņemas, tikai to resursu, kuru izveidojāt šīs sadaļas sākumā, laukā **Resurss** atlasiet izveidotā resursa nosaukumu. Lai uzņēmumam, kas aizņemas, varētu būt pieejami visi patapinošā uzņēmuma resursi, atstājiet lauku **Resurss** tukšu.
7. Lapas **Projekta pārvaldības un uzskaites parametri** cilnē **Starpuzņēmumu** iestatiet opciju **Iespējot starpuzņēmumu resursu plānošanu un darba laika uzskaites tabulas** uz **Jā**.

### <a name="in-the-borrowing-company"></a>Uzņēmumā, kas aizņemas

- Lapas **Resursu saraksts** meklēšanas filtrā ievadiet patapinošajam uzņēmumam izveidotā resursa nosaukumu, lai apstiprinātu, ka nosaukums tiek iekļauts uzņēmuma, kas aizņemas, resursu sarakstā.

## <a name="request-project-resources"></a>Projekta resursu pieprasīšana
Projekta resursa plānošanas funkcionalitāte tikai ļauj resursu pārvaldniekiem izplatīt personāla resursus iesaistēm vai projektiem. Lai iespējotu šo funkcionalitāti, izpildiet tālāk norādītos uzdevumus vai pārbaudiet, vai tie ir izpildīti:

- Iestatiet numuru secības.
- Iestatiet projekta vadības un uzskaites darbplūsmas.
- Iespējojiet resursa pieprasījumu darbplūsmas.

Pēc tam, kad ir izpildīti iepriekšējie uzdevumi, jūs varat pēc nepieciešamības izpildīt šādus uzdevumus:

- Izveidot resursa pieprasījumu no vieglās rezervācijas resursa.
- Uzraudzīt resursu pieprasījumus.
- Izpildīt resursu pieprasījumus.
- Pieprasīt personāla resursu no WBS.
- Rezervēt resursus projektam bez personāla resursa pieprasīšanas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]