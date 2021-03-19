---
title: Ieņēmumu atpazīšanas pārskats
description: Šajā tēmā ir sniegta informācija par ieņēmumu atpazīšanu risinājumā Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278877"
---
# <a name="revenue-recognition-overview"></a>Ieņēmumu atpazīšanas pārskats

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Risinājumā Dynamics 365 Project Operations ieņēmumu atpazīšanas principi atšķiras atkarībā no atlasītās norēķinu metodes projektam vai projekta daļai. Šajā tēmā ir sniegta informācija par ieņēmumu atpazīšanu risinājumā Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transakcijas, kas uzskaitītas, izmantojot laika un materiālu norēķinu metodi

- Izmaksu un ieņēmumu atpazīšana ir saistīta. Transakciju izmaksas un rēķinā neiekļautās pārdošanas transakcijas tiek grāmatotas, izmantojot [Project Operations integrācijas žurnālu](../project-accounting/project-operations-integration-journal.md).
- Projekta izmaksu un ieņēmumu profils nosaka, vai rēķinā neiekļautās pārdošanas transakcijas tiek grāmatotas virsgrāmatā. Ja atlasīta opcija **Uzkrāt ieņēmumus**, sistēma grāmatošanas laikā izmanto kontus **NP pārdošanas vērtība** un **Uzkrāto ieņēmumu pārdošanas vērtība**. Tālāk sniegts šīs metodes piemērs.  

  | Transakcijas veids | Debets/kredīts | Apjoms/summa |
  | --- | --- | --- |
  | NP pārdošanas vērtība | Debets | 100 |
  | Uzkrāto ieņēmumu pārdošanas vērtība | Kredīts | 100 |

- Ieņēmumi tiek atpazīti, izrakstot rēķinus. Grāmatošanas laikā sistēma izmanto kontu **Rēķinā iekļautie ieņēmumi**. Tālāk sniegts šīs metodes piemērs.  

  | Transakcijas veids | Debets/kredīts | Apjoms/summa |
  | --- | --- | --- |
  | Klienta bilance | Debets | 120 |
  | Maksājamais PVN | Kredīts | 20 |
  | Ieņēmumi, par ko izrakstīts rēķins | Kredīts | 100 |

- Ja ieņēmumi tika uzkrāti, grāmatojot rēķinā neiekļautās pārdošanas transakcijas, sistēma atsauc uzkrātos ieņēmumus rēķina izrakstīšanas laikā.

  | Transakcijas veids | Debets/kredīts | Apjoms/summa |
  | --- | --- | --- |
  | NP pārdošanas vērtība | Kredīts | 100 |
  | Uzkrāto ieņēmumu pārdošanas vērtība | Debets | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transakcijas, kas uzskaitītas, izmantojot fiksētas cenas norēķinu metodi

- Izmaksu un ieņēmumu atpazīšana ir atdalīta. Transakciju izmaksas tiek grāmatotas, izmantojot [Project Operations integrācijas žurnālu](../project-accounting/project-operations-integration-journal.md). Netiek izveidotas rēķinā neiekļautas pārdošanas transakcijas.
- Ieņēmumus var atpazīt rēķinu izrakstīšanas laikā, ja projekta izmaksu un ieņēmumu profila opcija **Projekta pabeigšanas aprēķiniem izmantotais princips** ir iestatīta uz **Bez NP**. Izmantojiet šo metodi tikai vienkāršiem īstermiņa projektiem.
- Ieņēmumus var atpazīt, izmantojot fiksētas cenas ieņēmumu novērtējumus ar metodi **Pabeigts līgums** vai **Ieņēmumu atpazīšana, izmantojot pabeigšanas procentuālo vērtību**.

## <a name="additional-resources"></a>Papildu resursi
[Raksts Apmaksājamo projektu uzskaites konfigurēšana](../project-accounting/configure-accounting-billable-projects.md)

[Fiksētas cenas ieņēmumu novērtējumu projekti](rev-rec-percentage-completion-method.md)

[Ieņēmumu novērtējumu pārvaldība](rev-rec-completed-contract-method.md)

[Pabeigšanas izmaksu metodes](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]