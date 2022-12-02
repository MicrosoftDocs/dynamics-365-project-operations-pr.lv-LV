---
title: Faktiskie dati
description: Šajā rakstā ir sniegta informācija par to, kā veikt darbības ar faktiskajiem darbiem programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924807"
---
# <a name="actuals"></a>Faktiskie dati

_**Attiecas uz:** Project Operations resursos balstītiem/krājumos nebalstītiem scenārijiem, Lite izvietošana — pāreja uz pro forma rēķina izrakstīšanu_

Faktiskie dati attiecas uz pārskatīto un apstiprināto finanšu un plānošanas norisi projektā. Tie tiek izveidoti, kad tiek apstiprināti laika, izmaksu un materiālu lietojuma ieraksti, žurnālu ieraksti un rēķini.

> [!IMPORTANT]
> Faktiskos datus nedrīkst rediģēt vai dzēst no sistēmas. Pretējā gadījumā var tikt ietekmēta finanšu integritāte un integrācija ar citām finanšu un grāmatvedības sistēmām. Microsoft Dynamics 365 Project Operations ļauj izmantot faktisko datu atsaukšanu un aizstāšanu, lai rediģētu faktiskos datus dažādos projekta biznesa procesa dzīves cikla punktos.

## <a name="recording-actuals-based-on-project-events"></a>Faktisko datu ierakstīšana, pamatojoties uz projekta notikumiem

Project Operations ieraksta finanšu transakcijas, kas notiek projekta darbības dzīves cikla laikā, kā faktiskos datus. Faktisko datu izveide dažādos dzīves cikla notikumos atšķiras atkarībā no tā, vai projekta darbības laikā tiek izmantots laika un materiālu norēķinu modelis vai fiksētas cenas norēķinu modelis, kā arī no tā, vai tas ir pirmspārdošanas posms vai iekšējs projekts.

Tālāk sniegtajos rakstos ir izskaidrots, kāda būs ietekme uz faktisko datu tabulu dažādos notikumos dažādās atšķirīgās situācijās.

- [Datu ietekme uz laiku un materiālu piesaisti](ActualsonTM.md)
- [Datu ietekme uz fiksētu cenu piesaistīšanu](ActualonFP.md)
- [Datu ietekme pirms pārdošanas piesaistes posmā](ActualonPreSales.md)
- [Datu ietekme uz iekšējo projektu](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
