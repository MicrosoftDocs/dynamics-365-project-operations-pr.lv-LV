---
title: Projekta rēķina integrācija
description: Šajā tēmā ir sniegta informācija par Project Operations duālās rakstīšanas integrāciju klientu rēķinu izrakstīšanai.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581247"
---
# <a name="project-invoice-integration"></a>Projekta rēķina integrācija

Šajā tēmā ir sniegta informācija par Project Operations duālās rakstīšanas integrāciju klientu rēķinu izrakstīšanai.

Programmā Project Operations projekta vadītājs pārvalda projekta norēķinu rezerves un izveido pro formas rēķinu klientam programmā Microsoft Dataverse. Pamatojoties uz šo pro forma rēķinu, debitoru ierēdnis vai projekta grāmatvedis izveido uz klientu vērstu rēķinu. Duālās rakstīšanas integrācija nodrošina, ka proforma rēķina detaļas tiek sinhronizētas ar finanšu un operāciju programmām. Pēc tam, kad uz klientu vērstais rēķins ir grāmatots, sistēma atjaunina attiecīgos projekta faktiskos datus programmā Dataverse ar grāmatvedības informāciju. Tālāk redzamajā diagrammā ir parādīts augsta līmeņa konceptuālais šīs integrācijas pārskats.

   ![Projekta rēķina integrācija.](./media/DW5Invoicing.png)

Pēc tam, kad projekta vadītājs ir apstiprinājis proformas rēķinu programmā Dataverse, proforma rēķina virsraksta informācija tiek sinhronizēta ar Finance and Operations programmām, izmantojot divu rakstīšanas tabulas karti Projekta **rēķina priekšlikums V2 (rēķini)**. Šī ir vienvirziena integrācija no Dataverse finanšu un operāciju lietotnēm. Projekta rēķinu priekšlikumu izveide vai dzēšana tieši finanšu un operāciju programmās netiek atbalstīta.

Rēķinu apstiprināšana risinājumā Dataverse aktivizē arī biznesa loģiku, lai entītijā **Faktiskie dati** izveidotu ar rēķiniem saistītus ierakstus. Šie ieraksti tiek sinhronizēti ar Finanses un operācijas, izmantojot divu rakstīšanas tabulu karti, **Project Operations integration actuals (msdyn\_ actuals).** Papildinformāciju skatiet sadaļā [Projekta aprēķini un faktisko dati](resource-dual-write-estimates-actuals.md). 

Projektu rēķinu priekšlikumu rindas izveido periodiskais process **Importēšanas veidlapu izstādīšana**. Šī procesa pamatā ir rēķinā iekļauto pārdošanas faktisko datu informācija tabulā **Faktisko datu izstādīšana**. Papildinformāciju skatiet sadaļā [Projekta rēķina priekšlikumu pārvaldība](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
