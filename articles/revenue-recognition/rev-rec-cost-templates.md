---
title: Izmaksu veidņu iestatīšana
description: Šajā tēmā ir sniegta informācija par to, kā izveidot un izmanto izmaksu veidnes risinājumā Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f4a515db31a31028af4a60927ab360be6c261a3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013900"
---
# <a name="set-up-cost-templates"></a>Izmaksu veidņu iestatīšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_


Šajā tēmā ir sniegta informācija par to, kā izveidot un izmanto izmaksu veidnes risinājumā Project Operations. Izmaksu veidne nosaka:

- projekta kategorijas prognozēm un faktiskajām transakcijām, kas jāiekļauj projekta pabeigšanas aprēķina procentuālajā vērtībā. Pēc tam pabeigšanas procentuālā vērtība tiek izmantota, lai aprēķinātu, cik daudz ieņēmumu ir atzīts;
- vai pabeigšanas procentuālo vērtību var modificēt, ja tā ir aprēķināta automātiski;
- vai pabeigšanas procentuālo vērtību aprēķina, balstoties uz summām vai vienībām.

## <a name="cost-template-example"></a>Izmaksu veidnes piemērs

Jūs strādājat ar tīmekļa vietnes dizaina projektu klientam, par kuru iekasējat fiksētu maksu 10 000 USD. Jūs prognozējat, ka projekta pabeigšana prasīs 100 stundas (5000 USD). Jūs arī prognozējat, ka būs nepieciešamas divas lidmašīnas biļetes un četras naktis viesnīcā braucienam pie klienta (1800 USD). Rezultātā tiek iegūta kopējā prognozētā izmaksu summa 6800 USD.

Palaižot fiksētas cenas ieņēmumu atzīšanas procesu, lai izveidotu novērtējumu mēneša beigās, jūs konstatējat, ka projektam veltījāt 35 stundas. Tas vēl neietver lidojumus vai viesnīcas izmaksas. Jums bija nepieciešams arī palīgs, kurš veica piecu stundu pētījumu projekta vajadzībām par 100 USD, kas nebija plānoti.

Kad šim projektam tiek aprēķināta pabeigšanas procentuālā vērtība, ir pieejamas tālāk norādītās iespējas.

- Vai vēlaties iekļaut visas izmaksas (stundas un izdevumus) vai tikai stundas?
- Vai vēlaties iekļaut visas stundas vai tikai plānotās stundas?
- Vai vēlaties aprēķināt pabeigšanas procentuālo vērtību, pamatojoties uz plānotā laika izmaksām dolāros (5000 USD) vai tikai uz stundu skaitu (100)?

Atbildes uz šiem jautājumiem nosaka izmaksu veidnei iestatītās opcijas un izmaksu veidnes rindās atlasītās kategorijas.

Tālāk redzamajā tabulā ir parādīti dažādu metožu rezultāti, rēķinot pabeigšanas procentuālo vērtību šim scenārijam.

| Pabeigšanas vērtība, pamatojoties uz | Izmaksas dolāros vai vienības | Pabeigšanas procentuālā vērtība | Aprēķins |
| --- | --- | --- | --- |
| Visas stundas, bez izdevumiem | Izmaksas dolāros | 37% 35 x 50 USD + 100 USD = 1850 USD 1850 USD/5000 USD |
| Visas stundas, bez izdevumiem | Vienības | 40% | 40 stundas/100 stundas (ieskaitot piecas neplānotās stundas) |
| Plānotās stundas, bez izdevumiem | Izmaksas dolāros vai vienība | 35% | 35/100 stundas vai 35 x 50 USD/5000 |
| Visas stundas un izdevumi | Izmaksas dolāros | 27,2% | 1850 USD/6800 USD |

Lēmums par to, kuru metodi izvēlēties izmaksu veidnes izveidošanai, var būt atkarīgs no vairākiem apsvērumiem.

- Ja izmaksu veidnē iekļaujat neplānotās stundas, jūs riskējat sasniegt 100 procentu pabeigšanas vērtību pirms projekta pabeigšanas. Tas ir tāpēc, ka faktiskais stundu skaits ir lielāks nekā plānotais. Ja izmantojat kādu no pirmajām divām tabulā uzskaitītajām metodēm, tad, pamanot novirzes, ir jāmaina plāns (prognozētās vienības). Šajā gadījumā stundas var pievienot vai atņemt, pamatojoties uz jūsu zināšanām par to, kas nepieciešams, lai pabeigtu projektu. Ja projekta pabeigšanai ir nepieciešamas papildu 65 stundas, plānam var pievienot piecas stundas, sasniedzot kopēju skaitu 105. Ja zināt, ka palīgs veiks vēl vienu piecu stundu pētījumu, kopējais laiks palielinās līdz 110 stundām.
- Ja izmantojat trešo tabulā norādīto metodi, varat atjaunināt tikai plānotās stundas savam laikam, lai nodrošinātu pabeigšanas procentuālās vērtības precizitāti. Ienesīgums mainīsies pēc neplānoto stundu reģistrēšanas, taču saglabāsies zināmā pabeigšanas procentuālās vērtības trajektorija.
- Ja izmantojat ceturto tabulā norādīto metodi, pastāv risks, ka izdevumi radīsies neregulāri un var netikt atspoguļoti jūsu pabeigšanas vērtības trajektorijā. Tāpēc, ja ir iekļauti izdevumi, pabeigšanas procentuālās vērtības svārstības var pārsniegt vēlamo līmeni. Piemēram, ja vēl neizmantojāt lidojumu, jūsu pabeigšanas procentuālā vērtība ir 27 procenti, nevis 35 procenti, vai 37 procenti, ja varējāt balstīt aprēķinu tikai uz laiku. Ja devāties vienā braucienā uz divām vienām un prognozējāt lidojuma un viesnīcas izmaksas precīzi, pabeigšanas procentuālā vērtība būtu 40,4 procenti (1850 USD par darbu un 900 USD par izdevumiem = 2750USD/6800 USD = 40,4 procenti). Tāpēc, iekļaujot izdevumus tikai par vienu lidojumu, pabeigšanas procentuālā vērtība tiek nomainīta no 27 uz 40 procentiem.

## <a name="create-cost-templates"></a>Izmaksu veidņu izveide
Lai izveidotu izmaksu veidnes, izpildiet tālāk aprakstītās darbības.

1. Lai piekļūtu izmaksu veidnēm, Dynamics 365 Finance vidē pārejiet uz **Projektu pārvaldība un uzskaite** > **Iestatīšana** > **Novērtējumi** > **Izmaksu veidne**.
2. Lai izveidotu jaunu izmaksu veidni, atlasiet **Jauns**. Ievadiet nosaukumu un aprakstu.
3. Norādiet izmaksu rindas ID katram transakcijas tipam.
4. Atlasiet noklusējuma pabeigšanas metodi.

  - **Automātiski**: pabeigšanas procentuālā vērtība tiek aprēķināta automātiski projektā. Iegūto vērtību nevar mainīt.
  - **Manuāli**: pabeigšanas procentuālā vērtība tiek aprēķināta automātiski projektā. Iegūto vērtību var mainīt.

  > [!NOTE]
  > Manuālajiem aprēķiniem pabeigšanas procentuālā vērtība tiek uzturēta lapas **Novērtējums** cilnes **Vispārīgi** sadaļā **Manuāls aprēķins**.

5. Opcijai **Pabeigšanas vērtība, pamatojoties uz** atlasiet vienu no tālāk norādītajām vērtībām.

  - **Summa**: pabeigšanas procentuālā vērtība tiek aprēķināta pēc summas uzskaites valūtā.
  - **Vienība**: pabeigšanas procentuālā vērtība tiek aprēķināta pēc daudzuma.
  - **Taisna līnija**: sistēma aprēķina pabeigšanas procentuālo vērtību proporcionāli, izmantojot projekta sākuma un beigu datumu, lai noteiktu projekta ilgumu.

6. Atlasiet **Izmaksu rindas**, lai pārskatītu izmaksu veidnes izmaksu rindas. Katram transakcijas tipam ir vajadzīga vismaz viena izmaksu rinda. Bet vienam un tam pašam transakcijas tipam var izveidot vairākas izmaksu rindas un iestatīt šīm rindām vēlamos atribūtus.
7. Cilnē **Kategorijas** atlasiet projekta kategorijas, kas jāiekļauj izmaksu veidnes rindā.
8. Cilnē **Vispārīgi** norādiet, vai šī rinda tiks iekļauta pabeigšanas procentuālās vērtības aprēķinā.
9. Atlasiet pabeigšanas vērtības izmaksu metodi, kas jāizmanto, aprēķinot pabeigšanas procentuālo vērtību.


[!INCLUDE[footer-include](../includes/footer-banner.md)]