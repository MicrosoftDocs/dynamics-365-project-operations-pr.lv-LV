---
title: Fiksētas cenas ieņēmumu novērtējumu projekti
description: Šajā tēmā ir sniegta informācija par fiksētas cenas ieņēmumiem projektos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 290608e5663f9c953212c156771bbf1ad6b1e901
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578717"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Fiksētas cenas ieņēmumu novērtējumu projekti 

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Izveidojot projekta līguma rindu ar tālāk norādītajiem atribūtiem Dynamics 365 Project Operations risinājumā Microsoft Dataverse, sistēma automātiski izveido fiksētas cenas ieņēmumu novērtējuma projektu. Informācija šajā projektā ir balstīta uz tālāk uzskaitītajām opcijām.

  - Fiksētas cenas norēķinu metode.
  - Saistīts projekts.
  - Vismaz viens atskaites punkts, kas definēts cilnē **Rēķina izrakstīšanas grafiks** lapā **Projekta līguma rinda**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Fiksētas cenas ieņēmumu novērtējumu projektu pārskatīšana
Lai pārskatītu fiksētas cenas ieņēmumu novērtējumu projektus, izpildiet tālāk norādītās darbības.

1. Vidē Dynamics 365 Finance dodieties uz **Projektu vadība un grāmatvedība** > **Projekti** > **Fiksētas cenas ieņēmumu tāmes projekti**.
2. Atlasiet projektu, kuru vēlaties skatīt, un veiciet dubultklikšķi uz **Novērtējuma projekta ID**, lai atvērtu ierakstu un pārskatītu detalizētu informāciju par projektu.
3. Izvērsiet cilni **Projekts**. Režģī **Atlasītie projekti** ir redzams viens projekts. Sistēma to izmanto kā noklusējuma projektu, jo šis projekts, ir saistīts ar projekta līguma rindu. 
4. Lai mainītu šo piesaisti, atlasiet papildu projektus un pievienojiet tos režģī **Atlasītie projekti**. Ja šajā režģī ir atlasīti vairāki projekti, projekta pabeigšana procentos un ieņēmumu novērtējumi tiek aprēķināti kopā visiem atlasītajiem projektiem.

  Projekta izmaksas, ieņēmumu profils, izmaksu veidne un perioda kods var tikt iestatīts manuāli. Ja šie parametri netiek iestatīti manuāli, pirmā projekta novērtējuma aprēķināšanas laikā tiek iestatītas noklusējuma vērtības, izmantojot projekta izmaksu un ieņēmumu profiliem konfigurētās kārtulas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]