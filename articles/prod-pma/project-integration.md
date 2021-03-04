---
title: Microsoft Project klienta integrācija
description: Projekta grafika plānošana un uzturēšana var būt sarežģīta, tāpēc projektu vadītājiem ir jāizmanto rīki, kas viņiem palīdz pārvaldīt šo uzdevumu. Integrācija ar Microsoft Project Client sniedz atbalstu, lai atvērtu un pārvaldītu projekta darba sadalījuma struktūru.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080505"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project klienta integrācija

[!include [banner](../includes/banner.md)]

Projekta grafika plānošana un uzturēšana var būt sarežģīta, tāpēc projektu vadītājiem ir jāizmanto rīki, kas viņiem palīdz pārvaldīt šo uzdevumu. Integrācija ar Microsoft Project Client sniedz atbalstu, lai atvērtu un pārvaldītu projekta darba sadalījuma struktūru. Projekta vadītājs var publicēt jebkādas izmaiņas atpakaļ Dynamics 365 Finance projekta darba sadalījuma struktūrā.

> [!NOTE]
> Ja izmantojat jūlija atjauninājumu (versija 10.0.4), ir jāinstalē KB 4054797 un 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Project Client pievienojumprogrammas konfigurēšana
Lai iespējotu integrēšanu ar programmu Microsoft Project Client, lietotāja klienta Microsoft Project lietojumprogrammā ir jābūt instalētai Microsoft Dynamics 365 pievienojumprogrammai. To var izdarīt, atverot **Projekta pārvaldības darbvietu**.

•  Noklikšķiniet uz **Konfigurēt projekta klienta pievienojumprogrammu** no darbvietas sadaļas **Saites** > **Iestatīšana**.

•  Noklikšķiniet uz **Atvērt** un pēc tam noklikšķiniet uz **Palaist** , kad tiek parādīta uzvedne.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Esoša melnraksta darba sadalījuma struktūras atvēršana un rediģēšana programmā Microsoft Project Client
Ja projektā programmā Dynamics 365 Finance jau ir izveidota darba sadalījuma struktūra, darba sadalījuma struktūru var atvērt Microsoft Project Client lietojumprogrammā, ja darba sadalījuma struktūrai ir melnraksta statuss. Lai atvērtu no **Projekta** lapas, noklikšķiniet uz **Atvērt programmā Microsoft Project** saites cilnē **Plāns**. Šo lapu var arī atvērt no Microsoft Project Client programmas, **Microsoft Dynamics 365** cilnē noklikšķinot **Atvērt**. Sarakstā atlasiet **Juridiska persona** un **Projekts**.

> [!NOTE]
> Ja izmantojat Internet Explorer kā pārlūkprogrammu, noklikšķiniet uz **Saglabāt** , lai manuāli atvērtu no atrašanās vietas, kurā fails tiek lejupielādēts. Vai noklikšķiniet uz **Saglabāt un atvērt** , lai šo failu atvērtu programmā Microsoft Project Client. Saglabājot nepārdēvējiet failu.

Pirms veicat faila labojumus, izmantojot Microsoft Project Client, no tā ir jāizrakstās. Cilnē  **Microsoft Dynamics 365** noklikšķiniet uz **Izrakstīt**. Tādējādi citi lietotāji nevarēs vienlaikus rediģēt darba sadalījuma struktūru no Finance. Lai pēc labojumu veikšanas publicētu darba sadalījuma struktūru, cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Atzīmēties**.

Ja projektam programmā Finance jau ir pievienota projekta komanda, resursu saraksts tiks aizpildīts ar darba grupas dalībniekiem. Ja projektam vēl nav pievienota projekta darba grupa, varat atlasīt resursus un veidot komandu programmā Microsoft Project Client, noklikšķinot uz pogas **Resursi** cilnē **Microsoft Dynamics 365**. 

Atzīmēšanās procesa ietvaros uz Finance tiks atpakaļ sinhronizēti šādi dati:

•   Uzdevuma nosaukums

•   Sākuma datums

•   Beigu datums

•   Pirmstecīgie uzdevumi

•   Resursa nosaukumi

•   Kategorija

•   Resursa kategorija

•   Darba laiks

•   Piezīmes

•   Prioritāte

> [!NOTE]
> Ja savam Microsoft Project Client failam pievienojat citas kolonnas, tās netiks saglabātas failā un netiks rādītas, failu atkārtoti atverot.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Darba sadalījuma struktūras izveide esošam projektam, izmantojot Microsoft Project Client
Lai izveidotu jaunu darba sadalījuma struktūru, izmantojot Microsoft Project Client, veiciet šādas darbības:


1.  Atveriet Microsoft Project Client.

2.  **Microsoft Dynamics 365** cilnē noklikšķiniet uz **Atvērt**.

3.  Atlasiet projekta **Juridisko personu**.

4.  Atlasiet **Projektu**.

5.  **Microsoft Dynamics 365** cilnē noklikšķiniet uz **Izrakstīt**.

6.  Kad esat gatavs publicēt programmā Finance, noklikšķiniet uz **Atzīmēties** cilnē **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Aizstājiet esošu darba sadalījuma struktūru esošam projektam, izmantojot Microsoft Project Client
Lai izveidotu jaunu darba sadalījuma struktūru, izmantojot Microsoft Project Client, un aizstātu esošu darba sadalījuma struktūru esošam projektam, veiciet šādas darbības:

1.  Atveriet Microsoft Project Client.

2.  Izveidojiet grafiku programmā Microsoft Project Client.

3.  Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Saglabāt izmaiņas** > **Aizstāt esošu projektu**.

4.  Atlasiet projekta **Juridisko personu**.

5.  Atlasiet **Projektu**.

6.  Noklikšķiniet uz **Labi**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Jauna projekta izveide no Microsoft Project Client


1.  Atveriet Microsoft Project Client.

2.  Izveidojiet grafiku programmā Microsoft Project Client.

3.  Cilnē **Microsoft Dynamics 365** noklikšķiniet uz **Saglabāt izmaiņas** > **Saglabāt jaunā projektā**.

4.  Atlasiet projekta **Juridisko personu**.

5.  Ja nepieciešams, ievadiet **Projekta ID**.

6.  Ievadiet **Projekta nosaukumu**.

7.  Atlasiet **Projekta veidu** , **Projekta grupu** un **Projekta līguma ID**. Varat arī izveidot jaunu projekta līgumu, noklikšķinot uz **Jauns**.

8.  Atlasiet **Kalendāru** , ko izmantot resursu piešķiršanai.

11. Noklikšķiniet uz **Labi**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]