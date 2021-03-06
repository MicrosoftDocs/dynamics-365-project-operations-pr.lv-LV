---
title: Project Operations demonstrācijas datu lietošana Finance mākoņpakalpojumā viesotā vidē
description: Šajā tēmā ir izskaidrots, kā lietot Project Operations demonstrācijas datus Dynamics 365 Finance mākoņpakalpojumā viesotā vidē.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948975"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>Project Operations demonstrācijas datu lietošana Finance mākoņpakalpojumā viesotā vidē

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

>[Svarīgi!] Šī tēma attiecas tikai uz Microsoft Dynamics 365 Finance versiju 10.0.13 un tajā sniegtos norādījumus var izpildīt tikai mākoņpakalpojumā viesotā vidē. Izpildiet šajā tēmā aprakstītās darbības, **PIRMS** lietojat kvalitātes atjauninājumus videi.

1. Savā LCS projektā atveriet lapu **Vides informācija**. Ņemiet vērā, ka tajā ir iekļauta informācija, kas nepieciešama, lai izveidotu savienojumu ar vidi, izmantojot attālās darbvirsmas protokolu (RDP).

![ vides informācija](./media/1EnvironmentDetails.png)

Pirmā iezīmēto akreditācijas datu kopa ir lokālā konta akreditācijas dati, un tajā ir ietverta hipersaite uz attālās darbvirsmas savienojumu. Akreditācijas dati ietver vides administratora lietotājvārdu un paroli. Otrā akreditācijas datu kopa tiek izmantota, lai šajā vidē pieteiktos programmā SQL Server.

2. Izveidojiet attālo savienojumu ar vidi, izmantojot sadaļā **Lokālie konti** esošo hipersaiti, un izmantojiet **Lokālā konta akreditācijas datus**, lai veiktu autentifikāciju.
3. Dodieties uz **Interneta informācijas pakalpojumi** > **Lietojumprogrammas kopas** > **AOSService** un apturiet pakalpojumu. Jūs pašlaik apturat pakalpojuma darbību, lai varētu turpināt aizstāt SQL datu bāzi.

![Apturēt AOS](./media/2StopAOS.png)

4. Dodieties uz **Pakalpojumi** un apturiet šādus divus elementus:

- Microsoft Dynamics 365 Unified Operations: lielapjoma pārvaldības pakalpojums
- Microsoft Dynamics 365 Unified Operations: datu importēšanas un eksportēšanas struktūra

![Apturēt pakalpojumus](./media/3StopServices.png)

5. Atveriet Microsoft SQL Server Management Studio. Piesakieties, izmantojot SQL Server akreditācijas datus, un izmantojiet LCS lapā **Vides informācija** norādīto axdbadmin lietotājvārdu un paroli.

![SQL Server Management Studio](./media/4SSMS.png)

6. Objektu pārlūka sadaļā **Datu bāzes** atrodiet **AXDB**. Datu bāze tiks aizstāta ar jaunu datu bāzi, kas atrodas [lejupielādes centrā](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Nokopējiet .zip failu virtuālajā mašīnā, ar ko ir izveidots attālais savienotjums, un izgūstiet .zip saturu.
8. Programmā SQL Server Management Studio ar peles labo pogu noklikšķiniet uz **AxDB** un pēc tam atlasiet **Uzdevumi** > **Atjaunot** > **Datu bāze**.

![Atjaunot datu bāzi](./media/5RestoreDatabase.png)

9. Atlasiet **Avota ierīce** un pārejiet uz failu, kas tika izvilkts no jūsu kopētā .zip faila.

![Avota ierīces](./media/6SourceDevice.png)

10. Atlasiet **Opcijas** un pēc tam atlasiet **Pārrakstīt esošo datu bāzi** un **Aizvērt esošos savienojumus ar mērķa datu bāzi**. 
11. Atlasiet **Labi**.

![Atjaunot iestatījumus](./media/7RestoreSetting.png)

Jūs saņemsit apstiprinājumu par to, ka AXDB atjaunošana izdevās. Pēc šī apstiprinājuma saņemšanas varat aizvērt SQL Services Management Studio.

12. Dodieties atpakaļ uz **Interneta informācijas pakalpojumi** > **Lietojumprogrammas kopas** > **AOSService** un startējiet AOSService.
13. Atveriet sadaļu **Pakalpojumi** un startējiet abus iepriekš apturētos pakalpojumus.

14. Atrodiet šajā virtuālajā mašīnā rīku AdminUserProvisioning. Meklējiet šeit: K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Palaidiet .ext failu, izmantojot savu lietotāja adresi laukā **E-pasta adrese**. 
16. Atlasiet **Iesniegt**.

![Lietotāja ar administratora atļaujām nodrošināšana](./media/8AdminUserProvisioning.png)

Procesa pabeigšanai nepieciešamas dažas minūtes. Jūs saņemsit apstiprinājuma ziņojumu par to, ka lietotājs ar administratora atļaujām tika veiksmīgi atjaunināts.

17. Visbeidzot, palaidiet komandu uzvedni kā administrators un veiciet IIS atiestatīšanu

![IIS atiestatīšana](./media/9IISReset.png)

18. Aizveriet attālās darbvirsmas sesiju un izmantojiet LCS lapu **Vides informācija**, lai pieteiktos vidē un pārliecinātos, vai tā darbojas, kā paredzēts.

![Finance and Operations](./media/10FinanceAndOperations.png)
