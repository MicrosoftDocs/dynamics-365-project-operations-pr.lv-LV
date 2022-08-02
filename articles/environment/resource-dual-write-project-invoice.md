---
title: Projekta rēķina integrācija
description: Šajā rakstā ir sniegta informācija par Project Operations divrakstu integrāciju klientu rēķinu izrakstīšanai.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029033"
---
# <a name="project-invoice-integration"></a>Projekta rēķina integrācija

Šajā rakstā ir sniegta informācija par Project Operations divrakstu integrāciju klientu rēķinu izrakstīšanai.

Programmā Project Operations projekta vadītājs pārvalda projekta norēķinu rezerves un izveido pro formas rēķinu klientam programmā Microsoft Dataverse. Pamatojoties uz šo pro forma rēķinu, debitoru ierēdnis vai projekta grāmatvedis izveido uz klientu vērstu rēķinu. Divrakstu integrācija nodrošina, ka proforma rēķinu informācija tiek sinhronizēta ar finanšu un operāciju lietotnēm. Pēc tam, kad uz klientu vērstais rēķins ir grāmatots, sistēma atjaunina attiecīgos projekta faktiskos datus programmā Dataverse ar grāmatvedības informāciju. Tālāk redzamajā diagrammā ir parādīts augsta līmeņa konceptuālais šīs integrācijas pārskats.

   ![Projekta rēķina integrācija.](./media/DW5Invoicing.png)

Pēc tam, kad projekta vadītājs ir apstiprinājis proforma rēķinu Dataverse, proforma rēķina galvenes informācija tiek sinhronizēta ar finanšu un operāciju programmām, izmantojot divrakstu tabulas karti, **projekta rēķina priekšlikumu V2 (rēķini)**. Šī ir vienvirziena integrācija no Dataverse uz finanšu un operāciju lietotnēm. Project rēķinu priekšlikumu izveide vai dzēšana tieši finanšu un operāciju programmās netiek atbalstīta.

Rēķinu apstiprināšana risinājumā Dataverse aktivizē arī biznesa loģiku, lai entītijā **Faktiskie dati** izveidotu ar rēķiniem saistītus ierakstus. Šie ieraksti tiek sinhronizēti ar finansēm un operācijām, izmantojot divrakstu tabulas karti, **Project Operations integrācijas faktiskos datus (msdyn\_ actuals).** Papildinformāciju skatiet sadaļā [Projekta aprēķini un faktisko dati](resource-dual-write-estimates-actuals.md). 

Projektu rēķinu priekšlikumu rindas izveido periodiskais process **Importēšanas veidlapu izstādīšana**. Šī procesa pamatā ir rēķinā iekļauto pārdošanas faktisko datu informācija tabulā **Faktisko datu izstādīšana**. Papildinformāciju skatiet sadaļā [Projekta rēķina priekšlikumu pārvaldība](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
