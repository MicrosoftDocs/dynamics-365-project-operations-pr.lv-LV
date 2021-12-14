---
title: Kredītkaršu iesniegšanas iestatīšana
description: Šajā tēmā izskaidrots, kā strādāt ar izmaksi kredītkartes transakcijām.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 49c8f2369a8be41fbc04c74bdb6b565b4f4b7b79
ms.sourcegitcommit: 9f26cf8bb640af1eb9f7f0872805965d7ffcb9d3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/19/2021
ms.locfileid: "7826265"
---
# <a name="set-up-credit-card-integration"></a>Kredītkaršu iesniegšanas iestatīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Ar izdevumiem saistītas kredītkaršu transakcijas var iestatīt tā, lai tās tiek automātiski importētas periodiskā grafikā. Transakcijas var arī manuāli importēt pēc to nepieciešamības. Kredītkaršu transakcijas tiek importētas, izmantojot kredītkaršu transakciju datu entitīju.

## <a name="import-credit-card-transactions"></a>Kredītkaršu transakciju importēšana

Lai importētu kredītkartes transakcijas, veiciet šīs darbības:

1. Lapā **Kredītkaršu transakcijas** atlasiet **Importēt transakcijas**. Ja datu pārvaldību atverat pirmo reizi, lai varētu turpināt, sistēmai ir jāatjaunina datu entītiju saraksts.
2. Laukā **Nosaukums** ievadiet unikālu importēšanas uzdevuma aprakstu.
3. Laukā **Avotdatu formāts** atlasiet formātu failam, kas satur importējamās kredītkaršu transakcijas.
4. Atlasiet **Augšupielādēt** un pēc tam atrodiet un atlasiet importējamo failu.
5. Kad faila augšupielāde ir pabeigta, validējiet kredītkaršu transakcijas faila kartēšanu un kredītkaršu transakciju datu entitījas kolonnas, elementā atzīmējot saiti **Skatīt karti**. Ja ir kartēšanas kļūdas vai ja jums ir jāmaina kartējums, veiciet kartēšanas kļūdas vai nu cilnē **Kartēšanas vizualizācija** vai **Kartēšanas informācija**.
6. Lai automatizētu kredītkaršu transakcijas, atlasiet **Izveidot periodisku datu uzdevumu**. Pēc tam varat iestatīt periodiskumu, kas nosaka, cik bieži kredītkaršu transakcijas vajadzētu importēt. Kad esat pabeidzis, atlasiet **Labi**.
7. Lai tūlīt importētu atlasīto failu, atlasiet **Importēt**.
8. Ja importēšanas laikā rodas kļūdas, varat skatīt izpildes žurnālu vai izvietošanas datus, lai redzētu novēršamās kļūdas un nodrošinātu veiksmīgu importēšanu.

> [!NOTE]
> Ja ir jāimportē vairāki failu formāti, katram formāta tipam ir jāizveido atsevišķi importēšanas uzdevumi.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Kredītkaršu transakciju atkārtota piešķiršana darbiniekiem, ar kuriem pārtrauktas darba attiecības

Pēc darbinieka ieraksta pārtraukšanas darbinieka Active Directory domēna pakalpojumu (AD DS) konts ir atspējots. Taču var būt aktīvas kredītkaršu transakcijas, kurām joprojām jāpiešķir izdevumi un kuras jāatlīdzina. Lapā **Kredītkartes transakcijas** varat atkārtoti piešķirt darbinieku jebkurai kredītkartes transakcijai, no kuras ir noņemts saistītais darbinieks.

Atlasiet vienu vai vairākas kredītkaršu transakcijas un pēc tam atlasiet **Piešķirt transakcijas atkārtoti**. Pēc tam varat atlasīt citu darbinieku, kuram piešķirt kredītkaršu transakcijas. Pēc kredītkaršu transakciju atkārtotas piešķires tās var atlasīt izdevumu atskaitei un apmaksāt, izmantojot ierasto izdevumu atskaites atlīdzināšanas procesu.

## <a name="delete-credit-card-transactions"></a>Kredītkartes transakciju dzēšana 

Dažkārt pēc kredītkartes transakciju importēšanas var būt nepieciešams dzēst noteiktas transakcijas. Tas var būt tāpēc, ka darbības ir dublikāti vai dati nav precīzi. Administratori var izmantot līdzekli **Dzēst kredītkartes transakcijas**, lai atlasītu un dzēstu kredītkartesthat transakcijas, kas **nav saidtītas** ar izdevumu pārskatu. 

1. Atveriet **Periodiski uzdevumi** > **Dzēst kredītkartes transakcijas**.
2. Atlasiet **Filtrēt** un norādiet informāciju, lai identificētu iekļaujamos ierakstus.
3. Lai dzēstu ierakstus, atlasiet **Labi**. 

## <a name="storing-credit-card-numbers"></a>Kredītkaršu numuru glabāšana

Kredītkaršu numuru glabāšanai ir pieejamas trīs iespējas. Kredītkaršu numuri tiek glabāti **lapā Izdevumu pārvaldības** parametri.

- **Novērst kartes numura ievadīšanu** – kredītkaršu numuri netiek saglabāti.
- **Jauc karšu numuri (saglabā pēdējos četrus ciparus)** – kredītkaršu numuru pēdējie četri cipari tiek glabāti šifrētā formātā.
- **Veikala karšu numuri** – Kredītkaršu numuri tiek glabāti nešifrētā formātā. Šī opcija neatbilst maksājumu karšu nozares (PCI) datu drošības standartam (DSS). Tāpēc, lai saglabātu savu organizāciju atbilstošu PCI DSS noteikumiem, organizācijas administratoriem ir jāizvēlas vai nu neglabāt kredītkaršu numurus, vai saglabāt jauc.k. karšu numurus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
