---
title: Kredītkaršu iesniegšanas iestatīšana
description: Šajā rakstā izskaidrots, kā strādāt ar izdevumu kredītkaršu transakcijām.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d32754548af67bdd5b9f7345f6363bd6193b36d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924504"
---
# <a name="set-up-credit-card-integration"></a>Kredītkaršu iesniegšanas iestatīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Ar izdevumiem saistītas kredītkaršu transakcijas var iestatīt tā, lai tās tiek automātiski importētas periodiskā grafikā. Transakcijas var arī manuāli importēt pēc to nepieciešamības. Kredītkaršu transakcijas tiek importētas, izmantojot kredītkaršu transakciju datu entitīju.

## <a name="import-credit-card-transactions"></a>Kredītkaršu transakciju importēšana

Lai importētu kredītkartes transakcijas, veiciet šīs darbības:

1. Lapā **Kredītkaršu transakcijas** atlasiet **Importēt transakcijas**. Ja datu pārvaldību atverat pirmoreiz, sistēmai ir jāatjaunina datu entītiju saraksts, iekams varat turpināt darbu.
2. Laukā **Nosaukums** ievadiet unikālu importēšanas uzdevuma aprakstu.
3. Laukā **Avotdatu formāts** atlasiet formātu failam, kas satur importējamās kredītkaršu transakcijas.
4. Atlasiet **Augšupielādēt** un pēc tam atrodiet un atlasiet importējamo failu.
5. Kad faila augšupielāde ir pabeigta, validējiet kredītkaršu transakcijas faila kartēšanu un kredītkaršu transakciju datu entitījas kolonnas, elementā atzīmējot saiti **Skatīt karti**. Ja ir kartēšanas kļūdas vai ja jums ir jāmaina kartējums, veiciet kartēšanas kļūdas vai nu cilnē **Kartēšanas vizualizācija** vai **Kartēšanas informācija**.
6. Lai automatizētu kredītkaršu transakcijas, atlasiet **Izveidot periodisku datu uzdevumu**. Pēc tam varat iestatīt periodiskumu, kas nosaka, cik bieži kredītkaršu transakcijas vajadzētu importēt. Kad esat pabeidzis, noklikšķiniet uz **Labi**.
7. Lai tūlīt importētu atlasīto failu, atlasiet **Importēt**.
8. Ja importēšanas laikā rodas kļūdas, varat skatīt izpildes žurnālu vai izvietošanas datus, lai redzētu novēršamās kļūdas un nodrošinātu veiksmīgu importēšanu.

> [!NOTE]
> Ja ir jāimportē vairāki failu formāti, katram formāta tipam ir jāizveido atsevišķi importēšanas uzdevumi.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Kredītkaršu transakciju atkārtota piešķiršana darbiniekiem, ar kuriem pārtrauktas darba attiecības

Pēc tam, kad ir pārtraukts darbinieka ieraksts, darbinieka Active Directory Domain Services (AD DS) konts tiek atspējots. Taču var būt aktīvas kredītkaršu transakcijas, kurām joprojām jāpiešķir izdevumi un kuras jāatlīdzina. Lapā **Kredītkartes transakcijas** varat atkārtoti piešķirt darbinieku jebkurai kredītkartes transakcijai, no kuras ir noņemts saistītais darbinieks.

Atlasiet vienu vai vairākas kredītkaršu transakcijas un pēc tam atlasiet **Piešķirt transakcijas atkārtoti**. Pēc tam varat atlasīt citu darbinieku, kuram piešķirt kredītkaršu transakcijas. Pēc kredītkaršu transakciju atkārtotas piešķires tās var atlasīt izdevumu atskaitei un apmaksāt, izmantojot ierasto izdevumu atskaites atlīdzināšanas procesu.

## <a name="delete-credit-card-transactions"></a>Kredītkartes transakciju dzēšana 

Dažkārt pēc kredītkartes transakciju importēšanas var būt nepieciešams dzēst noteiktas transakcijas. Tas var būt tāpēc, ka transakcijām ir dublikāti vai dati nav precīzi. Administratori var izmantot līdzekli **Dzēst kredītkartes transakcijas**, lai atlasītu un dzēstu kredītkartesthat transakcijas, kas **nav saidtītas** ar izdevumu pārskatu. 

1. Atveriet **Periodiski uzdevumi** > **Dzēst kredītkartes transakcijas**.
2. Atlasiet **Filtrēt** un norādiet informāciju, lai identificētu iekļaujamos ierakstus.
3. Lai dzēstu ierakstus, atlasiet **Labi**. 

## <a name="storing-credit-card-numbers"></a>Kredītkaršu numuru glabāšana

Ir pieejamas trīs kredītkaršu numuru glabāšanas opcijas. Kredītkaršu numuri tiek glabāti lapā **Izdevumu pārvaldības parametri**.

- **Kartes numura ievades nepieļaušana** — kredītkaršu numuri netiek saglabāti.
- **Jaukt karšu numurus (saglabāt pēdējos četrus ciparus)**  — pēdējie četri kredītkaršu numuru cipari tiek glabāti šifrētā formātā.
- **Glabāt karšu numurus** — kredītkaršu numuri tiek glabāti nešifrētā formātā. Šī opcija neatbilst maksājumu karšu nozares (PCI) datu drošības standartam (DSS). Tāpēc, lai organizācija nodrošinātu atbilstību PSI DSS noteikumiem, organizācijas administratoriem ir jāizvēlas neglabāt kredītkaršu numurus vai glabāt jauktus karšu numurus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
