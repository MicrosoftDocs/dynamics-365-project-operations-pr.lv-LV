---
title: Demonstrācijas datu lietošana Finance mākoņpakalpojumā viesotā vidē
description: Šajā tēmā ir izskaidrots, kā lietot Project Operations demonstrācijas datus Dynamics 365 Finance mākoņpakalpojumā viesotā vidē.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c04aab6ffb332a3095ca2a7890deb73f15a8b5e3713021c60eec02eb13dbd0cb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009675"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Demonstrācijas datu lietošana Finance mākoņpakalpojumā viesotā vidē

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

> [!IMPORTANT]
> Šī tēma attiecas tikai uz Microsoft Dynamics 365 Finance versiju 10.0.13, un tajā sniegtos norādījumus var izpildīt tikai mākoņpakalpojumā viesotā vidē. Izpildiet šajā tēmā aprakstītās darbības, **PIRMS** lietojat kvalitātes atjauninājumus videi.

1. Savā LCS projektā atveriet lapu **Vides informācija**. Ņemiet vērā, ka tajā ir iekļauta informācija, kas nepieciešama, lai izveidotu savienojumu ar vidi, izmantojot attālās darbvirsmas protokolu (RDP).

![Vides informācija.](./media/1EnvironmentDetails.png)

Pirmā iezīmēto akreditācijas datu kopa ir lokālā konta akreditācijas dati, un tajā ir ietverta hipersaite uz attālās darbvirsmas savienojumu. Akreditācijas dati ietver vides administratora lietotājvārdu un paroli. Otrā akreditācijas datu kopa tiek izmantota, lai šajā vidē pieteiktos programmā SQL Server.

2. Izveidojiet attālo savienojumu ar vidi, izmantojot sadaļā **Lokālie konti** esošo hipersaiti, un izmantojiet **Lokālā konta akreditācijas datus**, lai veiktu autentifikāciju.
3. Dodieties uz **Interneta informācijas pakalpojumi** > **Lietojumprogrammas kopas** > **AOSService** un apturiet pakalpojumu. Jūs pašlaik apturat pakalpojuma darbību, lai varētu turpināt aizstāt SQL datu bāzi.

![AOS apturēšana.](./media/2StopAOS.png)

4. Dodieties uz **Pakalpojumi** un apturiet šādus divus elementus:

- Microsoft Dynamics 365 Unified Operations: lielapjoma pārvaldības pakalpojums
- Microsoft Dynamics 365 Unified Operations: datu importēšanas un eksportēšanas struktūra

![Pakalpojumu apturēšana.](./media/3StopServices.png)

5. Atveriet Microsoft SQL Server Management Studio. Piesakieties, izmantojot SQL Server akreditācijas datus, un izmantojiet LCS lapā **Vides informācija** norādīto axdbadmin lietotājvārdu un paroli.

![SQL Server Management Studio.](./media/4SSMS.png)

6. Objektu pārlūka sadaļā **Datu bāzes** atrodiet **AXDB**. Datu bāze tiks aizstāta ar jaunu datu bāzi, kas atrodas [lejupielādes centrā](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Nokopējiet .zip failu virtuālajā mašīnā, ar ko ir izveidots attālais savienotjums, un izgūstiet .zip saturu.
8. Programmā SQL Server Management Studio ar peles labo pogu noklikšķiniet uz **AxDB** un pēc tam atlasiet **Uzdevumi** > **Atjaunot** > **Datu bāze**.

![Datu bāzies atjaunošana.](./media/5RestoreDatabase.png)

9. Atlasiet **Avota ierīce** un pārejiet uz failu, kas tika izvilkts no jūsu kopētā .zip faila.

![Avota ierīces.](./media/6SourceDevice.png)

10. Atlasiet **Opcijas** un pēc tam atlasiet **Pārrakstīt esošo datu bāzi** un **Aizvērt esošos savienojumus ar mērķa datu bāzi**. 
11. Atlasiet **Labi**.

![Iestatījumu atjaunošana.](./media/7RestoreSetting.png)

Jūs saņemsit apstiprinājumu par to, ka AXDB atjaunošana izdevās. Pēc šī apstiprinājuma saņemšanas varat aizvērt SQL Services Management Studio.

12. Dodieties atpakaļ uz **Interneta informācijas pakalpojumi** > **Lietojumprogrammas kopas** > **AOSService** un startējiet AOSService.
13. Atveriet sadaļu **Pakalpojumi** un startējiet abus iepriekš apturētos pakalpojumus.

14. Atrodiet šajā virtuālajā mašīnā rīku AdminUserProvisioning. Meklējiet šeit: K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Palaidiet .ext failu, izmantojot savu lietotāja adresi laukā **E-pasta adrese**. 
16. Atlasiet **Iesniegt**.

![Lietotāja ar administratora atļaujām nodrošināšana.](./media/8AdminUserProvisioning.png)

Procesa pabeigšanai nepieciešamas dažas minūtes. Jūs saņemsit apstiprinājuma ziņojumu par to, ka lietotājs ar administratora atļaujām tika veiksmīgi atjaunināts.

17. Visbeidzot, palaidiet komandu uzvedni kā administrators un veiciet IIS atiestatīšanu

![IIS atiestatīšana.](./media/9IISReset.png)

18. Aizveriet attālās darbvirsmas sesiju un izmantojiet LCS lapu **Vides informācija**, lai pieteiktos vidē un pārliecinātos, vai tā darbojas, kā paredzēts.

![Finance and Operations.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]