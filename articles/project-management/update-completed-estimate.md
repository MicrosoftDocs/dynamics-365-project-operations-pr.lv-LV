---
title: Galīgo izmaksu novērtējuma atjaunināšana
description: Šajā tēmā ir sniegta informācija par projekta darba prognozes atjaunināšanu.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080627"
---
# <a name="update-estimate-at-completion"></a>Galīgo izmaksu novērtējuma atjaunināšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projektu vadītāji bieži vien pārskata sākotnējās uzdevumu aplēses. Projekta pārprojektēšana ir projektu vadītāja reaģēšana uz prognozēm, ņemot vērā projekta pašreizējo statusu. Taču mēs neiesakām projektu vadītājiem mainīt bāzlīnijas skaitļus, jo projekta bāzlīnija pārstāv noteikto patiesās informācijas avotu projekta grafikam un izmaksu tāmei, un visas projektā ieinteresētās puses par to ir vienojušās.

Projektu vadītājs uzdevumiem var pārprojektēt piepūli divos tālāk norādītajos veidos:

- Pārlabojiet noklusējuma novērtējumu līdz pabeigšanai (ETC) ar jaunu faktiskā uzdevumam atlikušā darba novērtējumu. 
- Pārlabot noklusējuma progresa procentuālo daudzumu ar jaunu uzdevuma patiesā progresa novērtējumu.

Katra no šīm metodēm izraisa uzdevuma ETC, EAC un progresa procentuālā daudzuma pārrēķināšanu, kā arī uzdevumam projektētās piepūles novirzes pārrēķināšanu. Tiek pārrēķināts EAC, ETC un progresa procentuālais daudzums kopsavilkuma uzdevumiem, un tiek izveidota jauna piepūles novirzes projektēšana.
