---
title: Kāpēc nevar izdzēst ierakstus no faktisko entītijas?
description: Šajā tēmā ir sniegta informācija par to, kāpēc nevar izdzēst ierakstus no faktisko entītijas.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286077"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Kāpēc nevar izdzēst ierakstus no entītijas Faktiskās vērtības?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) neļauj dzēst faktiskos ierakstus, jo tie kalpo kā patiesības avots transakcijām, kurām ir finansiāla ietekme uz pakārtotajām sistēmām, piemēram, virsgrāmatu. Ja faktiskās vērtības nevar dzēst, var tikt apšaubīta finanšu atskaišu transakciju integritāte. Lai izveidotu audita pierakstu, klientiem jāizmanto žurnāli, lai izveidotu kompensācijas transakcijas.



[!INCLUDE[footer-include](../includes/footer-banner.md)]