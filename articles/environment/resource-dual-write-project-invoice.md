---
title: Projekta rēķina integrācija
description: Šajā rakstā sniegta informācija par projektu operāciju divrakstņu integrāciju debitoru rēķinu izrakstīšanai.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912111"
---
# <a name="project-invoice-integration"></a>Projekta rēķina integrācija

Šajā rakstā sniegta informācija par projektu operāciju divrakstņu integrāciju debitoru rēķinu izrakstīšanai.

Programmā Project Operations projekta vadītājs pārvalda projekta norēķinu rezerves un izveido pro formas rēķinu klientam programmā Microsoft Dataverse. Pamatojoties uz šo pro forma rēķinu, debitoru ierēdnis vai projekta grāmatvedis izveido uz klientu vērstu rēķinu. Duālās rakstīšanas integrācija nodrošina, ka proforma rēķina detaļas tiek sinhronizētas ar finanšu un operāciju programmām. Pēc tam, kad uz klientu vērstais rēķins ir grāmatots, sistēma atjaunina attiecīgos projekta faktiskos datus programmā Dataverse ar grāmatvedības informāciju. Tālāk redzamajā diagrammā ir parādīts augsta līmeņa konceptuālais šīs integrācijas pārskats.

   ![Projekta rēķina integrācija.](./media/DW5Invoicing.png)

Pēc tam, kad projekta vadītājs ir apstiprinājis proformas rēķinu programmā Dataverse, proforma rēķina virsraksta informācija tiek sinhronizēta ar Finance and Operations programmām, izmantojot divu rakstīšanas tabulas karti Projekta **rēķina priekšlikums V2 (rēķini)**. Šī ir vienvirziena integrācija no Dataverse finanšu un operāciju lietotnēm. Projekta rēķinu priekšlikumu izveide vai dzēšana tieši finanšu un operāciju programmās netiek atbalstīta.

Rēķinu apstiprināšana risinājumā Dataverse aktivizē arī biznesa loģiku, lai entītijā **Faktiskie dati** izveidotu ar rēķiniem saistītus ierakstus. Šie ieraksti tiek sinhronizēti ar Finanses un operācijas, izmantojot divu rakstīšanas tabulu karti, **Project Operations integration actuals (msdyn\_ actuals).** Papildinformāciju skatiet sadaļā [Projekta aprēķini un faktisko dati](resource-dual-write-estimates-actuals.md). 

Projektu rēķinu priekšlikumu rindas izveido periodiskais process **Importēšanas veidlapu izstādīšana**. Šī procesa pamatā ir rēķinā iekļauto pārdošanas faktisko datu informācija tabulā **Faktisko datu izstādīšana**. Papildinformāciju skatiet sadaļā [Projekta rēķina priekšlikumu pārvaldība](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
