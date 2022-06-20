---
title: Cenu noteikšanas produktu piedāvājuma rindas
description: Šajā rakstā sniegta informācija par izmaksu cenas attiecināšanu uz produkta piedāvājuma rindu.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 23eb3d29081769347d62098534a9863fd28fa90c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932581"
---
# <a name="costing-product-based-quote-lines"></a>Cenu noteikšanas produktu piedāvājuma rindas

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


Produkta piedāvājuma rindās ir Dynamics 365 Project Operations arī lauks **Izmaksu cena**. Šo lauku izmanto, lai sekotu produkta izmaksām piedāvājuma rindā un lejupstraumes ienesīguma aprēķiniem.

Ja kataloga precei ir izveidota produkta piedāvājuma rinda, produkta piedāvājuma rindas izmaksas pēc noklusējuma tiek ņemta no preču kataloga lauka **Standarta izmaksas**. Preču kataloga lauks Standarta izmaksas tiek iestatīts Organizācijas pamatvalūtā. Produkta piedāvājuma rindas noklusējuma vienības izmaksas piedāvājumā tiek konvertētas pārdošanas valūtā.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Vienības izmaksas produktu piedāvājuma rindā

Produkta piedāvājuma rindas vienības izmaksu mērķis ir tas, lai katrā pārdošanas reizē precei var būt dažādas izmaksas. Šis nav tipisks scenārijs, taču reizēm piegādātājs var piemērot preces izmaksu atlaidi atkarībā no galīgās pārdošanas klienta.

Piemērs.

Uzņēmums Fabrikam Robotics uzstāda robotu rokas korporācijas Adatum konveijeros. Uzņēmums Fabrikam nodrošina uzstādīšanas pakalpojumus, taču robotu rokas tiek iegādātas no uzņēmuma Trey robotics. Ja robotu roku uzstādīšana korporācijā Adatum paver jaunu nozares vertikāli uzņēmuma Trey ražotajām robotu rokām, Trey varētu šim darījumam noteikt īpašu atlaidi uzņēmumam Fabrikam.

Šajā gadījumā Fabrikam izveidos produkta piedāvājuma rindu “Robotu rokas” un ievadīs šim piedāvājumam īpašas vienības izmaksas. Šīs izmaksas atšķiras no Trey ražoto robotu roku standarta izmaksām.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]