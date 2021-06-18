---
title: Projekta rēķina integrācija
description: Šajā tēmā ir sniegta informācija par Project Operations duālās rakstīšanas integrāciju klientu rēķinu izrakstīšanai.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996575"
---
# <a name="project-invoice-integration"></a>Projekta rēķina integrācija

Šajā tēmā ir sniegta informācija par Project Operations duālās rakstīšanas integrāciju klientu rēķinu izrakstīšanai.

Programmā Project Operations projekta vadītājs pārvalda projekta norēķinu rezerves un izveido pro formas rēķinu klientam programmā Microsoft Dataverse. Pamatojoties uz šo pro forma rēķinu, debitoru ierēdnis vai projekta grāmatvedis izveido uz klientu vērstu rēķinu. Duālās rakstīšanas integrācija garantē, ka pro formas rēķina informācija tiek sinhronizēta ar Finance and Operations programmām. Pēc tam, kad uz klientu vērstais rēķins ir grāmatots, sistēma atjaunina attiecīgos projekta faktiskos datus programmā Dataverse ar grāmatvedības informāciju. Tālāk redzamajā diagrammā ir parādīts augsta līmeņa konceptuālais šīs integrācijas pārskats.

   ![Projekta rēķina integrācija](./media/DW5Invoicing.png)

Kad projekta vadītājs apstiprina pro forma rēķinu programmā Dataverse, pro formas rēķina galvenes informācija tiek sinhronizēta ar Finance and Operations programmām, izmantojot duālās rakstīšanas tabulas karti **Projekta rēķina priekšlikuma izpilde V2 (rēķini)**. Tā ir vienvirziena integrācija no Dataverse uz Finance and Operations programmām. Projektu rēķinu priekšlikumu izveide vai dzēšana tieši Finance and Operations programmās netiek atbalstīta.

Rēķinu apstiprināšana risinājumā Dataverse aktivizē arī biznesa loģiku, lai entītijā **Faktiskie dati** izveidotu ar rēķiniem saistītus ierakstus. Šie ieraksti tiek sinhronizēti ar Finance and Operations, izmantojot duālās rakstīšanas tabulas karti **Project Operations integrācijas faktiskie dati (msdyn\_actuals)**. Papildinformāciju skatiet sadaļā [Projekta aprēķini un faktisko dati](resource-dual-write-estimates-actuals.md). 

Projektu rēķinu priekšlikumu rindas izveido periodiskais process **Importēšanas veidlapu izstādīšana**. Šī procesa pamatā ir rēķinā iekļauto pārdošanas faktisko datu informācija tabulā **Faktisko datu izstādīšana**. Papildinformāciju skatiet sadaļā [Projekta rēķina priekšlikumu pārvaldība](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
