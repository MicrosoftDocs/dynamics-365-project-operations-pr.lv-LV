---
title: Piegādātāja ieturēšanas pārskats
description: Šajā tēmā ir sniegts pārskats par piegādātāju ieturēšanas iespējām.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594607"
---
# <a name="vendor-retention-overview"></a>Piegādātāja ieturēšanas pārskats

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Jūsu organizācijas ietvaros var tikt saglabāta daļa no piegādātājiem, kas strādā ar jūsu organizācijas projektiem. Piemēram, pirms apmaksas piegādātājam jūs, iespējams, vēlēsieties pārliecināties, vai nodrošinātās preces un pakalpojumi atbilst jūsu prognozēm.

Vienojoties par projektu iepirkumiem ar piegādātājiem, var norādīt piegādātāja ieturēšanas nosacījumus, kas ietver ieturamo procentu vai summu. Kad piegādātājs piegādā preces un pakalpojumus, jūs no jūsu maksājuma piegādātājam atskaitāt norādīto ieturēšanas procentu vai summu. Kad projekti ir pabeigti vai tiek sasniegts pagaidu posms, kā norādīts piegādātāja līgumā, ieturētā summa ir jāatskaita un jāizveido maksājums piegādātājam.

## <a name="vendor-retention-example"></a>Piegādātāja ieturēšanas piemērs

Šajā piemērā parādīts, kā tiek ieturēta piegādātāja rēķina summas procentuālā vērtība, pamatojoties uz projekta pabeigto procentuālo posmu.

Contoso Robotics ASV ir noslēgts līgums ar ar piegādātāju Fabrikam, lai piegādātu 100 stundu apmācību aprīkojuma atjaunošanas projektam. Līguma kopējā vērtība ir USD 30000 ar noteiktu pirkuma cenu, kas ir USD 300 stundā.

Apmācība tiks piegādāta trīs posmos, izmantojot šādu grafiku:

- Posms 1: 50 stundas vai 50 procenti no projekta
- Posms 2: 30 stundas vai 80 procenti no kopējā projekta
- Posms 3: 20 stundas vai 100 procenti no projekta

Tālāk sniegtajā tabulā ir norādīti ieturēšanas nosacījumi.

| **Piegādāto vienību procentuālā vērtība** | **Ieturamā procentuālā vērtība** | **Atskaitāmā procentuālā vērtība** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

Šo transakciju rezultātā tiek iegūtas šādas summas:

- Posms 1:
  - Maksājamā summa ir 50 x 300 vai 15 000.
  - 20 procenti no summas jeb 3 000 tiek ieturēti un tiks atskaitīti vēlākā posmā.
  - Piegādātājam samaksātā summa ir 12 000.
- Posms 2:
  - Maksājamā summa ir 30 x 300 vai 9 000.
  - Tiek ieturēti 10 procenti no summas jeb 900.
  - Tiek atskaitīti 10 procenti no 3000, kas tika ieturēti 1. posmā vai 300.
  - Piegādātājam samaksātā summa ir 8 400. Šī summa ir par 9 000 mazāka par 900 ieturēto plus 300, kas tika atskaitīti 1. posma ieturēšanā.
- Posms 3:
  - Maksājamā summa ir 20 x 300 vai 6 000.
  - Nekas netiek ieturēts.
  - Atskaitītā summa ir 3 600. Šo summu veido 3 000, kas tika ieturēti 1. posmā, atskaitot 300 no 1. posma, kas tika ieturēti 2. posmā plus 900, kas tika ieturēti 2. posmā.
  - Piegādātājam samaksātā summa ir 9 600. Šo summu veido ieturētā summa 3 600 plus 6 000, lai pabeigtu 3. posmu.

Kopējā piegādātājam samaksātā summa pēc trīs punktu posmu pabeigšanas ir 30 000, kas ir pirkuma pasūtījuma kopsumma (15 000 + 9 000 + 6 000).
