---
title: Fiksētas cenas ieņēmumu novērtējumu projekti
description: Šajā tēmā ir sniegta informācija par fiksētas cenas ieņēmumiem projektos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 451f0403f0111b5ea4de6c91b54eae157830e413d3a21f23bd841a66905e147b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006435"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Fiksētas cenas ieņēmumu novērtējumu projekti 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Izveidojot projekta līguma rindu ar tālāk norādītajiem atribūtiem Dynamics 365 Project Operations risinājumā Microsoft Dataverse, sistēma automātiski izveido fiksētas cenas ieņēmumu novērtējuma projektu. Informācija šajā projektā ir balstīta uz tālāk uzskaitītajām opcijām.

  - Fiksētas cenas norēķinu metode.
  - Saistīts projekts.
  - Vismaz viens atskaites punkts, kas definēts cilnē **Rēķina izrakstīšanas grafiks** lapā **Projekta līguma rinda**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Fiksētas cenas ieņēmumu novērtējumu projektu pārskatīšana
Lai pārskatītu fiksētas cenas ieņēmumu novērtējumu projektus, izpildiet tālāk norādītās darbības.

1. Dynamics 365 Finance vidē pārejiet uz **Projektu pārvaldība un uzskaite** > **Projekti** > **Fiksētas cenas ieņēmumu novērtējumu projekti**.
2. Atlasiet projektu, kuru vēlaties skatīt, un veiciet dubultklikšķi uz **Novērtējuma projekta ID**, lai atvērtu ierakstu un pārskatītu detalizētu informāciju par projektu.
3. Izvērsiet cilni **Projekts**. Režģī **Atlasītie projekti** ir redzams viens projekts. Sistēma to izmanto kā noklusējuma projektu, jo šis projekts, ir saistīts ar projekta līguma rindu. 
4. Lai mainītu šo piesaisti, atlasiet papildu projektus un pievienojiet tos režģī **Atlasītie projekti**. Ja šajā režģī ir atlasīti vairāki projekti, projekta pabeigšana procentos un ieņēmumu novērtējumi tiek aprēķināti kopā visiem atlasītajiem projektiem.

  Projekta izmaksas, ieņēmumu profils, izmaksu veidne un perioda kods var tikt iestatīts manuāli. Ja šie parametri netiek iestatīti manuāli, pirmā projekta novērtējuma aprēķināšanas laikā tiek iestatītas noklusējuma vērtības, izmantojot projekta izmaksu un ieņēmumu profiliem konfigurētās kārtulas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]