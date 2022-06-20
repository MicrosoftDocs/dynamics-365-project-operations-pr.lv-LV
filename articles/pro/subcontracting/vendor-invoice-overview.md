---
title: Kreditoru rēķinu izrakstīšana — koncepcija un izveide
description: Šajā rakstā ir aprakstīta kreditoru rēķinu koncepcija, lietošanas scenāriji un tas, kā izveidot kreditoru rēķinus programmā Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911467"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Kreditoru rēķinu izrakstīšana — koncepcija un izveide

[!include [banner](../../includes/dataverse-preview.md)]

_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Kreditoru rēķinus sistēmā Microsoft Dynamics 365 Project Operations var izmantot, lai reģistrētu izmaksas, kas radušās, piegādātājiem piegādājot pakalpojumus un/vai materiālus projektā.

Ja par pakalpojumiem un/vai materiāliem tiek slēgts apakšlīgums ar piegādātāju, apakšuzņēmuma līgums ir līgums ar šo kreditoru. Tā kā piegādātājs sniedz pakalpojumus vai materiāli tiek saņemti un izmantoti projekta uzdevumos, izmaksas tiek reģistrētas projektā. Periodiski piegādātājs nosūta rēķinus, kas ir pārbaudīti un saskaņoti ar projektā reģistrētajām izmaksām. Pēc pārbaudes procesa pabeigšanas kreditora rēķins tiek apstiprināts un nodots apmaksai.

## <a name="scenarios-for-use"></a>Lietošanas scenāriji

Kreditoru rēķinus projekta operācijās var izmantot, lai atbalstītu divus atšķirīgus scenārijus.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klienti izmanto visas apakšlīgumu slēgšanas iespējas

Piegādātāju rēķinu pieredze nodrošina veidu, kā pārbaudīt un saskaņot laika ierakstus, materiālu lietojumu un izdevumu ierakstus, kas atsaucas uz apakšuzņēmēju komponentiem ar piegādātāja rēķina rindām. Šo procesu var izmantot, lai pārbaudītu kreditora rēķina rindu precizitāti. Kad pārbaudes process ir pabeigts un kreditora rēķins ir apstiprināts, programma apvērsīs faktiskos datus, kas reģistrēti pēc apstiprinātā laika, izdevumiem un materiālu lietojuma žurnāliem, un izveidos jaunas izmaksu faktiskās darbības, izmantojot kreditora rēķina rindas.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klienti neizmanto pilnu apakšuzņēmuma līgumu pieredzi, bet vēlas, lai viņiem būtu vienots skatījums uz projektu izmaksām projektu darbībās

Ja izsekojat apakšuzņēmuma procesu trešās puses sistēmā, varat reģistrēt izmaksas no šīs trešās puses sistēmas projektu operācijās, izveidojot kreditoru rēķinus, kuros nav atsauces uz apakšuzņēmuma līgumiem. Tādā veidā jūsu projektu vadītājiem var būt vienots, vienots skatījums uz visām konkrētā projekta izmaksām.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Kreditoru rēķinu izveide projekta operācijās

Kreditoru rēķinus var izveidot divos veidos:

- Kreditora rēķinu saraksta lapā vai detalizētās informācijas lapā vienam kreditora rēķinam
- Apakšuzņēmuma saraksta lapā vai detalizētas informācijas lapā par vienu apakšuzņēmuma līgumu

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Izveide no kreditora rēķinu saraksta lapas vai detalizētās informācijas lapas

1. Dodieties uz **Pirkšanas** \> **kreditora rēķini**.
2. Lapā Kreditoru rēķinu saraksts vai viena kreditora rēķina detalizētās informācijas lapā atlasiet **Jauns**, lai izveidotu jaunu kreditora rēķinu.

Šādā veidā izveidotie kreditoru rēķini var atsaukties arī uz apakšuzņēmuma līgumu.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Izveide no apakšuzņēmuma saraksta lapas vai detalizētas informācijas lapas

1. Dodieties uz **Apakšuzņēmuma līgumu** iegāde \>**·**.
2. Atlasiet vienu vai vairākus apakšuzņēmuma līgumus.
3. Lapā Apakšuzņēmuma līgumu saraksts vai viena apakšlīguma detalizētās informācijas lapā atlasiet **Izveidot kreditora rēķinu**, lai izveidotu jaunu kreditora rēķinu.

Katram atlasītajam **apakšuzņēmuma līgumam tiek izveidots jauns kreditora rēķins melnraksta** statusā.

Šādi izveidotie kreditoru rēķini vienmēr atsaucas uz apakšuzņēmuma līgumu kreditora rēķina virsrakstā. Katra apakšuzņēmuma rinda, kurai ir laika un materiālu norēķinu metode, izraisīs rindas izveidi kreditora rēķinā. Katra apakšlīguma rinda, kurai ir fiksētas cenas norēķinu metode, izraisīs rindas izveidi kreditora rēķinā katram apakšuzņēmuma rindas atskaites punktam, kura statuss **ir Gatavs rēķinam**.

No apakšlīguma uz kreditora rēķina virsrakstu tiks kopēti šādi lauki un saistītie ieraksti:

- Kreditora.
- Saistītie cenrāži tiks kopēti kreditora rēķinā kā cenrāži.
- Valūta.
- Līgumslēdzēja vienība.
- Apmaksas nosacījumi.

Laika un materiālu apakšuzņēmuma rindām no apakšuzņēmuma rindas uz kreditora rēķina rindu tiks kopēti šādi lauki un saistītie ieraksti:

- Apakšuzņēmuma un apakšuzņēmuma līniju atsauces
- Transakciju klase
- Loma
- Transakciju kategorija
- Preces lauki
- Project
- Uzdevums
- Rezervējamais resurss

Fiksētas cenas apakšuzņēmuma rindām šādi lauki tiek kopēti no apakšuzņēmuma rindas un apakšuzņēmuma rindas atskaites punkta uz kreditora rēķina rindu:

- Apakšuzņēmuma un apakšuzņēmuma rindu atsauces.
- Darbības klase. Pēc noklusējuma vērtība būs **Milestone**.
- Atskaites punkta nosaukums un summa tiks kopēta no saistītā apakšuzņēmuma rindas atskaites punkta.
- Lietotājs var atlasīt projektu un uzdevumu kreditora rēķina rindā.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
