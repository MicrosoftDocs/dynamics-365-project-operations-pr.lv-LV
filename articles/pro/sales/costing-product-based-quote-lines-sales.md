---
title: Cenu noteikšanas produktu piedāvājuma rindas
description: Šajā rakstā ir sniegta informācija par izmaksu piemērošanu produktu piedāvājumu rindai.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825621"
---
# <a name="costing-product-based-quote-lines"></a>Cenu noteikšanas produktu piedāvājuma rindas

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_


Produkta piedāvājuma rindās ir Dynamics 365 Project Operations arī lauks **Izmaksu cena**. Šo lauku izmanto, lai sekotu produkta izmaksām piedāvājuma rindā un lejupstraumes ienesīguma aprēķiniem.

Ja kataloga precei ir izveidota produkta piedāvājuma rinda, produkta piedāvājuma rindas izmaksas pēc noklusējuma tiek ņemta no preču kataloga lauka **Standarta izmaksas**. Preču kataloga lauks Standarta izmaksas tiek iestatīts Organizācijas pamatvalūtā. Produkta piedāvājuma rindas noklusējuma vienības izmaksas piedāvājumā tiek konvertētas pārdošanas valūtā.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Vienības izmaksas produktu piedāvājuma rindā

Produkta piedāvājuma rindas vienības izmaksu mērķis ir tas, lai katrā pārdošanas reizē precei var būt dažādas izmaksas. Šis nav tipisks scenārijs, taču reizēm piegādātājs var piemērot preces izmaksu atlaidi atkarībā no galīgās pārdošanas klienta.

Piemērs.

Uzņēmums Fabrikam Robotics uzstāda robotu rokas korporācijas Adatum konveijeros. Uzņēmums Fabrikam nodrošina uzstādīšanas pakalpojumus, taču robotu rokas tiek iegādātas no uzņēmuma Trey robotics. Ja robotu roku uzstādīšana korporācijā Adatum paver jaunu nozares vertikāli uzņēmuma Trey ražotajām robotu rokām, Trey varētu šim darījumam noteikt īpašu atlaidi uzņēmumam Fabrikam.

Šajā gadījumā Fabrikam izveidos produkta piedāvājuma rindu “Robotu rokas” un ievadīs šim piedāvājumam īpašas vienības izmaksas. Šīs izmaksas atšķiras no Trey ražoto robotu roku standarta izmaksām.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
