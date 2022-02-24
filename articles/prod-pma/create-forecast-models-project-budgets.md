---
title: Projekta budžetu prognožu modeļu izveide
description: Šajā tēmā aprakstīts, kā izveidot prognožu modeli atlikušajiem budžetiem.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271047"
---
# <a name="create-forecast-models-for-project-budgets"></a>Projekta budžetu prognožu modeļu izveide 

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot prognožu modeli atlikušajiem budžetiem. Projekts, kam tiek kontrolēts budžets, izmanto divu veidu budžetus: sākotnējo un atlikušo. Kad izveidojat projekta budžetu, ir jānorāda sākotnējā un atlikušā budžeta prognožu modeļi, kas izveidoti lapā **Prognožu modeļi**. Projekta budžeti, kuru pamatā ir noteikti modeļi, tiek izveidoti, kad izpildāt projekta budžetu.

> [!NOTE]
> Prognožu modelim, kas tiek izmantots budžeta kontrolei, nevar būt apakšmodelis, vai tas nevar tikt izmantots kā apakšmodelis.

1. Atlasiet **Projektu vadība un grāmatvedība** > **Iestatījumi** > **Prognozes**  > **Prognožu modeļi**.
2. Atlasiet **Jauns**, lai izveidotu jaunu prognožu modeli, un pēc tam ievadiet modeļa ID numuru un jaunā modeļa nosaukumu. 
3. Opciju **Apturēts** iestatiet uz **Jā**, lai neļautu veikt izmaiņas prognožu modeļa prognožu rindās. 
4. Ja prognožu rindām, ar kurām ir saistīts modelis, ir jāģenerē naudas plūsmas prognozes virsgrāmatā, vienumu **Iekļaut naudas plūsmas prognozēs** iestatiet uz **Jā**. 
5. Lai projekta datumu izmantotu kā rēķina datumu, vienumu **Prognozēt rēķina datumu** iestatiet uz **Jā**. 
6. Laukā **Budžeta tips** atlasiet vienu no šiem modeļu tipiem.

   - **Sākotnējais budžets**: izmantojiet sākotnējās budžeta summas, kas ir iestatītas, izveidojot un aprēķinot sākotnējo budžetu.
   - **Atlikušais budžets**: atlikušās budžeta summas izmantojiet projekta dzīves laikā. Bilances šajā prognožu modelī samazina faktiskie darījumi un palielina vai samazina budžeta pārskatījumi.
   - **Pārnesumi** : izmantojiet pārnesumu budžeta summas projektam. Pārnešana ir neobligāts process, ko var palaist, lai pārnestu neizmantotās budžeta summas no viena finanšu gada uz citu.

7. Pēc nepieciešamības iestatiet tālāk minētās opcijas.

   - Lai projekta datumu izmantotu kā rēķina datumu, iespējojiet vienumu **Prognozēt rēķina datumu**.
   - Iespējojiet **Prognozēt ar NP**, lai prognozētu, pamatojoties uz notiekošo darbu (NP), un pēc tam atlasiet NP tipu. 
   - Noklusējuma **budžeta tipu** var atstāt kā **Nav** vai var ievadīt jaunu tipu. Pēc ieraksta maiņas budžeta tipu nevar mainīt.     
    > [!NOTE]
    > Ja mainīsit noklusējuma budžeta tipu, visas citas opcijas būs nepieejamas atjauninājumiem un šo budžeta modeli nevarēs atkārtoti izmantot. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]