---
title: Kreditoru rēķinu izrakstīšana — koncepcija un izveide
description: Šajā rakstā ir aprakstīts kreditoru rēķinu jēdziens, lietošanas scenāriji un kreditoru rēķinu izveide korporācijā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261953"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Kreditoru rēķinu izrakstīšana — koncepcija un izveide

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Kreditoru rēķinus korporācijā Microsoft Dynamics 365 Project Operations var izmantot, lai reģistrētu izmaksas, kas saistītas ar piegādātāju veiktajām pakalpojumu un/vai materiālu piegādēm projektā.

Ja pakalpojumi un/vai materiāli ir noslēgti ar pārdevēju, apakšlīgums ir līgums ar šo pārdevēju. Kad pārdevējs sniedz pakalpojumus vai materiāli tiek saņemti un izmantoti projekta uzdevumos, izmaksas tiek reģistrētas projektā. Periodiski kreditors sūta rēķinus, kas ir verificēti un saskaņoti ar izmaksām, kas tiek reģistrētas projektā. Kad verifikācijas process ir pabeigts, kreditora rēķins tiek apstiprināts un izlaists apmaksai.

## <a name="scenarios-for-use"></a>Lietošanas scenāriji

Kreditoru rēķinus project operations var izmantot, lai atbalstītu divus atšķirīgus scenārijus.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klienti izmanto visas apakšuzņēmuma līgumu slēgšanas iespējas

Kreditoru rēķinu lietošanas iespējas nodrošina veidu, kā pārbaudīt un saskaņot laika ierakstus, materiālu lietojumu un izdevumu ierakstus, kuros ir atsauce uz apakšuzņēmēju komponentiem, ar kreditoru rēķina rindām. Šo procesu var izmantot, lai pārbaudītu kreditora rēķina rindu rindu precizitāti. Kad verifikācijas process ir pabeigts un kreditora rēķins ir apstiprināts, lietojumprogramma apvērsīs faktiskās vērtības, kas tika reģistrētas ar apstiprinātajiem laika, izdevumu un materiālu lietojuma žurnāliem, un izveidos jaunas izmaksu faktiskās izmaksas, izmantojot kreditora rēķina rindas.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klienti neizmanto pilnas apakšuzņēmuma līgumu slēgšanas iespējas, bet vēlas iegūt vienotu priekšstatu par projektu izmaksām project darbībās

Ja izsekojat apakšuzņēmuma līgumu slēgšanas procesu trešās puses sistēmā, varat reģistrēt izmaksas no šīs trešās puses sistēmas uz Project Operations, izveidojot kreditoru rēķinus, kuros nav atsauces uz apakšuzņēmuma līgumiem. Tādā veidā jūsu projektu vadītājiem var būt vienots, vienots skatījums uz visām izmaksām konkrētā projektā.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Kreditoru rēķinu izveide programmā Project Operations

Kreditoru rēķinus var izveidot divos veidos:

- No kreditora rēķina saraksta lapas vai detalizētas informācijas lapas par vienu kreditora rēķinu
- No apakšuzņēmuma līgumu saraksta lapas vai detalizētas informācijas lapas par vienu apakšlīgumu

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Izveide no kreditora rēķina saraksta lapas vai detalizētas informācijas lapas

1. Dodieties uz **pirkšanas** \> **kreditora rēķini**.
2. Kreditora rēķina saraksta lapā vai viena kreditora rēķina detalizētas informācijas lapā atlasiet **Jauns**, lai izveidotu jaunu kreditora rēķinu.

Šādā veidā izveidotajos kreditoru rēķinos var būt arī atsauce uz apakšlīgumu.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Izveide no apakšuzņēmuma līgumu saraksta lapas vai detalizētas informācijas lapas

1. Dodieties uz Apakšuzņēmuma **līgumu iegādi** \> **.**
2. Atlasiet vienu vai vairākus apakšuzņēmuma līgumus.
3. Apakšuzņēmuma līgumu saraksta lapā vai viena apakšuzņēmuma līguma detalizētas informācijas lapā atlasiet **Izveidot kreditora rēķinu**, lai izveidotu jaunu kreditora rēķinu.

Katram atlasītajam apakšlīgumam tiek izveidots jauns kreditora rēķins melnraksta **statusā**.

Šādā veidā izveidotajos kreditoru rēķinos vienmēr ir atsauce uz apakšlīgumu kreditora rēķina galvenē. Katra apakšuzņēmuma līguma rinda, kurai ir laika un materiālu norēķinu metode, kreditora rēķinā liks izveidot rindu. Katra apakšuzņēmuma līguma rinda, kurai ir fiksētas cenas norēķinu metode, liks kreditora rēķinā izveidot rindu katram apakšlīguma rindas atskaites punktam, kura statuss **ir Gatavs rēķinam**.

Tālāk norādītie lauki un saistītie ieraksti tiks kopēti no apakšuzņēmuma līguma uz kreditora rēķina galveni:

- Kreditora.
- Saistītie cenrāži tiks kopēti kreditora rēķinā kā cenrāži.
- Valūta.
- Līgumslēdzēja vienība.
- Apmaksas noteikumi.

Laika un materiālu apakšlīgumu rindām no apakšlīguma rindas uz kreditora rēķina rindu tiks kopēti šādi lauki un saistītie ieraksti:

- Atsauces uz apakšuzņēmuma līgumiem un apakšuzņēmuma līgumiem
- Transakciju klase
- Loma
- Transakciju kategorija
- Produktu lauki
- Project
- Uzdevums
- Rezervējamais resurss

Fiksētas cenas apakšlīgumu rindām tālāk norādītie lauki tiks kopēti no apakšuzņēmuma līguma rindas un apakšlīguma rindas atskaites punkta uz kreditora rēķina rindu:

- Atsauces uz apakšuzņēmuma līgumiem un apakšuzņēmuma līgumiem.
- Darījumu klase. Pēc noklusējuma vērtība būs **Milestone**.
- Atskaites punkta nosaukums un summa tiks kopēta no attiecīgās apakšlīguma rindas atskaites punkta.
- Lietotājs varēs atlasīt projektu un uzdevumu kreditora rēķina rindā.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
