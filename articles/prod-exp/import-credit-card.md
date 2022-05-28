---
title: Kredītkaršu darījumu importēšana un uzturēšana
description: Šajā tēmā paskaidrots, kā importēt un uzturēt izdevumu kredītkaršu transakcijas. Šos darījumus var iestatīt tā, lai tie tiktu automātiski importēti pēc periodiska grafika, vai arī tos var importēt manuāli pēc nepieciešamības.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: bd7ca997e18bf3c11fa188b603c899cc470df035
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683777"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Kredītkaršu darījumu importēšana un uzturēšana

Ar izdevumiem saistītas kredītkaršu transakcijas var iestatīt tā, lai tās tiek automātiski importētas periodiskā grafikā. Transakcijas var arī manuāli importēt pēc to nepieciešamības. Kredītkaršu transakcijas tiek importētas, izmantojot kredītkaršu transakciju datu entitīju.

Papildinformāciju par datu entītijām skatiet rakstā [Datu entītijas](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Kredītkaršu transakciju importēšana

1. Lapā **Kredītkaršu transakcijas** atlasiet **Importēt transakcijas**. Ja datu pārvaldību atverat pirmoreiz, sistēmai ir jāatjaunina datu entitīju saraksts, iekams varat turpināt darbu.
2. Laukā **Nosaukums** ievadiet importēšanas darba unikālo aprakstu.
3. Laukā **Avotdatu formāts** atlasiet formātu failam, kas satur importējamās kredītkaršu transakcijas.
4. Atlasiet **Augšupielādēt** un pēc tam atrodiet un atlasiet importējamo failu.
5. Kad faila augšupielāde ir pabeigta, validējiet kredītkaršu transakcijas faila kartēšanu un kredītkaršu transakciju datu entitījas kolonnas, elementā atzīmējot saiti **Skatīt karti**. Ja ir kartēšanas kļūdas vai ja jums ir jāmaina kartējums, veiciet kartēšanas kļūdas vai nu cilnē **Kartēšanas vizualizācija** vai **Kartēšanas informācija**.
6. Lai automatizētu kredītkaršu transakcijas, atlasiet **Izveidot periodisku datu uzdevumu**. Pēc tam varat iestatīt periodiskumu, kas nosaka, cik bieži kredītkaršu transakcijas vajadzētu importēt. Kad esat pabeidzis, noklikšķiniet uz **Labi**.
7. Lai tūlīt importētu atlasīto failu, atlasiet **Importēt**.
8. Ja importēšanas laikā rodas kļūdas, varat skatīt izpildes žurnālu vai sagatavošanas posmu datus, lai redzētu kļūdas, kuras jānovērš, lai garantētu sekmīgu importēšanu.

> [!NOTE]
> Ja ir jāimportē vairāk nekā viens faila formāts, ir jāizveido atsevišķi importēšanas uzdevumi katram formāta veidam.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Kredītkaršu transakciju atkārtota piešķiršana darbiniekiem, ar kuriem pārtrauktas darba attiecības

Pēc tam, kad ir pārtraukts darbinieka ieraksts, darbinieka Active Directory Domain Services (AD DS) konts tiek atspējots. Taču var būt aktīvas kredītkaršu transakcijas, kurām joprojām jāpiešķir izdevumi un kuras jāatlīdzina. Lapā **Kredītkaršu transakcijas** varat atkārtoti piešķirt darbinieku jebkurai kredītkaršu transakcijai, ja ir pārtrauktas darba attiecības ar saistīto darbinieku.

Atlasiet vienu vai vairākas kredītkaršu transakcijas un pēc tam atlasiet **Piešķirt transakcijas atkārtoti**. Pēc tam varat atlasīt citu darbinieku, kuram piešķirt kredītkaršu transakcijas. Pēc kredītkaršu transakciju atkārtotas piešķires tās var atlasīt izdevumu atskaitei un apmaksāt, izmantojot ierasto izdevumu atskaites atlīdzināšanas procesu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]