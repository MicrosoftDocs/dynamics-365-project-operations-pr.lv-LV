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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127167"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Kāpēc nevar izdzēst ierakstus no entītijas Faktiskās vērtības?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) neļauj dzēst faktiskos ierakstus, jo tie kalpo kā patiesības avots transakcijām, kurām ir finansiāla ietekme uz pakārtotajām sistēmām, piemēram, virsgrāmatu. Ja faktiskās vērtības nevar dzēst, var tikt apšaubīta finanšu atskaišu transakciju integritāte. Lai izveidotu audita pierakstu, klientiem jāizmanto žurnāli, lai izveidotu kompensācijas transakcijas.

