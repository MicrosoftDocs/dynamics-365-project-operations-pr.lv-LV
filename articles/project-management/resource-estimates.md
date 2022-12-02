---
title: Resursu laika finanšu aprēķini projektiem
description: Šajā rakstā ir sniegta informācija par to, kā tiek aprēķināti laika finanšu aprēķini.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03416feb178d883bba57dc14692049503b151ffd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913537"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Resursu laika finanšu aprēķini projektiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Finanšu aprēķinus laika aprēķina, pamatojoties uz trim faktoriem: 

- Vispārējs vai nosaukts darba grupas dalībnieks, kas piešķirts katram projekta plāna lapas mezgla uzdevumam. 
- Darba tips vai sarežģītība.
- Ieguldījuma sadalījums uzdevuma resursa piešķīrumam. 

Pirmie divi faktori ietekmē resursa piešķīruma vienības izmaksas vai rēķina likmi. Resursa piešķīruma vienības izmaksas vai rēķina likmi nosaka piešķirtā resursa atribūti. Šie atribūti ietver organizācijas vienību, kurai resurss pieder, un resursa standarta lomu. Varat arī pievienot resursam uzņēmumam atbilstošus pielāgotus atribūtus, piemēram, standarta amatu vai pieredzes līmeni, un tie ietekmē piešķires vienības izmaksas vai rēķina likmi.
Papildus resursa atribūtiem darba atribūti, piemēram, uzdevums, var ietekmēt arī vienības rēķina likmi vai piešķiršanas izmaksu likmi. Piemēram, ja noteikti uzdevumi ir daudz sarežģītāki, resursa piešķiršana šiem uzdevumiem rada augstākas vienības izmaksas vai rēķinu likmi nekā uzdevumi, kas nav tik sarežģīti.   

Trešajam faktoram tiek nodrošināts stundu daudzums ar šādu likmi. Ja uzdevums ietver divus cenu periodus, visticamāk, ka šī uzdevuma resursa piešķiršanas pirmā daļa tiek izcenota un tās cena ir atšķirīga nekā uzdevuma otrā daļa. Katra resursu piešķīruma ieguldījuma novērtējums ir sarežģīta vērtība, kas tiek glabāta kopā ar ieguldījuma dienas sadalījumu.

Detalizētus norādījumus par to, kā iestatīt pielāgotus darba un resursu atribūtus kā cenas noteikšanu un izmaksu noteikšanu, skatiet rakstā [Kopsavilkums par cenu dimensijām](../pricing-costing/pricing-dimensions-overview.md).

Katra resursa piešķiršanas finanšu novērtējums tiek aprēķināts kā **uzdevuma likme stundā, reizinot to ar stundu skaitu.**  Līdzīgi kā ieguldījuma novērtējumam, arī katra resursu piešķīruma izmaksu un ieņēmumu finanšu novērtējums ir sarežģīta vērtība, kas tiek glabāta kā dienas summa naudas izteiksmē. 

## <a name="summarizing-financial-estimates-for-time"></a>Laika fnanšu aprēķinu apkopošana
Laika finanšu novērtējums lapas mezgla uzdevumam ir finanšu aprēķinu summa par visiem šī uzdevuma resursu piešķīrumiem.

Laika finanšu novērtējums kopsavilkuma vai galvenajam uzdevumam ir finanšu aprēķinu summa par visiem tā apakšuzdevumiem. Šis ir projekta darbaspēka izmaksu novērtējums. 

![Resursu aprēķini.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Noklusējuma izmaksas un izmaksu valūta

Noklusējuma izmaksas tiek ņemtas no cenrāžiem, kas pievienoti projekta līguma slēgšanas vienībai. Projekta izmaksu valūta vienmēr ir projekta līguma slēgšanas vienības valūta. Resursu piešķīrumam izmaksu finanšu novērtējums tiek glabāts projekta izmaksu valūtā. Dažkārt cenrāža valūta var atšķirties no projekta izmaksu valūtas. Šajos gadījumos lietojumprogramma konvertē valūtu, kurā projekta valūtai ir iestatīta izmaksu cena. Režģī **Novērtējums** visi izmaksu aprēķini tiek parādīti un apkopoti projekta izmaksu valūtā. 

## <a name="default-bill-rate-and-sales-currency"></a>Noklusējuma rēķina likme un pārdošanas valūta

Noklusējuma pārdošanas cena tiek ņemta no projekta cenrāžiem, kas pievienoti saistītam projekta līgumam, ja darījums ir uzvarēts, vai no saistītā projekta piedāvājuma, ja darījums joprojām ir pirms pārdošanas posma. Projekta pārdošanas valūta vienmēr ir projekta piedāvājuma vai projekta līguma valūta. Resursu piešķīrumam pārdošanas finanšu novērtējums tiek glabāts projekta pārdošanas valūtā. Atšķirībā no izmaksām cenrādī iestatītā pārdošanas cena nekad nevar atšķirties no projekta pārdošanas valūtas. Nav scenārija, kurā nepieciešama valūtas konvertēšana. Režģī **Novērtējums** visi pārdošanas aprēķini tiek parādīti un apkopoti projekta pārdošanas valūtā. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
