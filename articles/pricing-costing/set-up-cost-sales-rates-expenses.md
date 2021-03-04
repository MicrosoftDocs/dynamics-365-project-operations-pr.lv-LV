---
title: Izmaksu un pārdošanas likmju iestatīšana izdevumiem
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt izmaksu un pārdošanas likmes darbību un izdevumu kategorijām.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b518c9eda00bef4d342dd66677344af516012749
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180291"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Izmaksu un pārdošanas likmju iestatīšana izdevumiem

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Darbību kategorijām var iestatīt izmaksu un pārdošanas cenas risinājumā Dynamics 365 Project Operations. Tā kā izmaksu un pārdošanas cenas ir paredzētas izdevumiem, katra darbību kategorija, kurā tās ir iekļautas, arī ir jāiestata kā izdevumu kategorija. Šis iestatījums nodrošina pakārtotās funkcionalitātes precizitāti. Izmaksu un pārdošanas cenas darbību kategorijām var uzskaitīt tikai vienā valūtā, kurai jābūt valūtai cenrāža virsrakstā.

Lai iestatītu izmaksu un pārdošanas likmes darbību kategorijām, veiciet tālāk norādītās darbības. 

1. Izveidojiet cenrāža sarakstu, pamatojoties uz cenrāža galveni. 
2. Apakšrežģa izvēlnē **Kategoriju cenas** atlasiet **+ Jauna kategorijas cena**. 
3. Lapā **Ātrā izveide** ievadiet to transakciju kategoriju un vienību, kurai veidojat jauno cenu.

Šajā tabulā ir uzskaitīti lauki cilnē **Vispārīgi** un **Ātrā izveide** kategorijas cenas rindā, kas jāņem vērā, veidojot kategoriju cenas pārdošanas vai izmaksu cenrādī.

| Lauks | Atrašanās vieta | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- | --- |
| Darījuma kategorija | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Atlasiet transakciju kategoriju, kurai veidojat pārdošanas vai izmaksu cenu. | Ienākošā novērtējuma vai izdevumu faktiskās transakcijas kategorija tiks saskaņota ar šo rindu, lai noklusētu darbības kategorijas izmaksu vai pārdošanas likmi. |
| Vienības grafiks | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Vienību plāns pēc noklusējuma ir norādīts darbības kategorijas vienību grafikā. | Šim laukam nav lejupstraumes ietekmes. |
| Vienība | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Atlasiet vienību, kurai tiek iestatītas likmes. | Vienība ienākošajā tāmē vai faktiskajā ir saskaņota ar vienību šajā rindā, lai noklusētu likmi izdevumu novērtējumā vai faktiskajā. |
| Cenas noteikšanas metode | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Iespējamās vērtības laukā **Cenas noteikšanas metode** ir **Cena par vienību**, **Par izmaksu** un **Uzcenojuma izmaksas**. | Cenas iestatīšanas laukā atlasot opciju **Cena par vienību**, tiek bloķēts lauks **Procenti** kategoriju cenu rindā. Ja ir atlasīta vērtība **Par izmaksu**, lauki **Cena** un **Procenti** pārdošanas cenrādī tiek bloķēti. Atlasot **Uzcenojums augstāks par izmaksu** bloķē lauku **Cena** pārdošanas cenrāža lauks cena. Ienākošajā faktiskajā rindā attiecībā uz izdevumiem **Pašizmaksa** vai **Uzcenojums augstāks par izmaksu** cenas noteikšanas metodes rezultātā atbilstošajai pārdošanas rindai bez rēķina tiek piešķirta cena, kas ir vienāda ar faktisko izmaksu cenu vai aprēķināta kā uzcenojums virs cenas. |
| Cenrādis | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Iestatiet katram transakciju kategorijas un vienību kombinācijas vienību likmei. Piemēram, nobraukuma likme ir 10 ASV dolāru par jūdzi un 8 ASV dolāru par kilometru. | Nobraukuma likme būs likme, kas pēc noklusējuma atbilst vienības cenai vai ienākošā novērtējuma vai faktiskās rindas izmaksām izdevumu darbības klasē.|
| Procents | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Iestatiet procentu virs darbības kategorijas un vienības kombinācijas izmaksām. Piemēram, aviobiļešu pārdošanas apjomam jābūt atzīmam par 10 procentiem salīdzinājumā ar radušos aviobiļešu izmaksām. | Šis izmaksu procentuālais daudzums pārdošanas cenu sarakstā ir piemērojams tikai tad, ja atlasītā cenu noteikšanas metode ir **Uzcenojums augstāks par izmaksu**. |
| Valūta | Cilne **Vispārīgi** un lapas **Ātrā izveide** | Pēc noklusējuma šī vērtība tiek iegūta no valūtas, kas atrodas pārdošanas cenu saraksta galvenē. Attiecībā uz transakciju kategoriju izcenojumiem valūtu nevar ignorēt. | Šī valūta noklusē ienākošās faktiskās rindas vienības cenu izmaksu un pārdošanas transakciju klasei. |

## <a name="pricing-methods-for-expenses"></a>Izmaksu noteikšanas metodes

Ja iestatāt kategoriju cenas, kas ir būtiskas tikai izmaksu cenu kontekstā, varat izmantot vienu no šīm trim cenu noteikšanas metodēm:

- **Vienības cena**
- **Pašizmaksa**
- **Uzcenojums augstāks par izmaksu**

### <a name="price-per-unit"></a>Vienības cena
Ja šī cenu noteikšanas metode ir atlasīta kategorijas cenu rindā, kas ir saistīta ar pārdošanas cenu sarakstu, kategorijas un vienības kombinācijas cenu noklusējumi gan novērtējumā, gan faktiskajā. Novērtējums attiecas uz projekta budžeta rindām izdevumiem, piedāvājuma rindas detalizēto informāciju un līguma rindas detalizēto informāciju par izdevumiem.

### <a name="at-cost"></a>Pašizmaksa
Ja šī cenu noteikšanas metode ir atlasīta kategorijas cenu rindā, kas ir saistīta ar pārdošanas cenu sarakstu, cenas noklusējumi kategorijas un vienības kombinācijai tiek iestatīti tikai faktiskajiem izdevumiem. Piemēram, bez rēķina pārdošanas faktiskie dati izdevumu darbības klasei. Vienības cena tiek iestatīta neizrēķinātajai pārdošanas cenai, kas ir faktiska no vienības cenas par šo izdevumu faktisko izmaksu. Izmaksu izmaksas pamatā esošā cenu nesegšana netiek veikta projekta izdevumu novērtējumos vai piedāvājuma rindā un detalizētā informācija par izdevumiem līguma rindā.

### <a name="markup-over-cost"></a>Uzcenojums augstāks par izmaksu
Ja šī cenu noteikšanas metode ir atlasīta kategorijas cenu rindā, kas ir saistīta ar pārdošanas cenu sarakstu, cenas noklusējumi kategorijas un vienības kombinācijai tiek iestatīti tikai izdevumiem, kas ir faktiskie. Piemēram, bez rēķina pārdošanas faktiskie dati izdevumu darbības klasei. Šī vienības cena tiek iestatīta neizrēķinātajai pārdošanai, kas ir faktiska, līdz aprēķinātai vērtībai no vienības cenas par izdevumiem faktisko izmaksu pēc tam, kad ir piemērots definētais uzcenojuma procents. Izmaksas pamatā esošā cenu neizpilde netiek veikta projekta tāmē izdevumu vai piedāvājuma rindai un līguma rindas detalizētai informācijai par izdevumiem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]