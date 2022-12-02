---
title: Kreditoru rēķinu izrakstīšana — koncepcija un izveide
description: Šajā rakstā ir aprakstīts piegādātāju rēķinu jēdziens, lietojamie scenāriji un izskaidrots, kā piegādātāju rēķinus izveidot programmā Microsoft Dynamics 365 Project Operations.
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

Piegādātāju rēķinu izrakstīšanu programmā Microsoft Dynamics 365 Project Operations var izmantot, lai ierakstītu izmaksas, kas saistītas ar pakalpojumu piegādi un/vai materiāliem projektā, ko izpilda piegādātāji.

Kad ar piegādātāju tiek noslēgts apakšlīgums par pakalpojumiem un/vai materiāliem, apakšlīgums atspoguļo līgumisku vienošanos ar šo piegādātāju. Kamēr piegādātājs nodrošina pakalpojumus vai tiek saņemti materiāli, kas tiek izmantoti projekta uzdevumiem, izmaksas tiek ierakstītas projektā. Periodiski piegādātājs nosūta rēķinus, kas tiek pārbaudīti un saskaņoti ar izmaksām, kas ir ierakstītas projektā. Pēc pārbaudes procesa pabeigšanas piegādātāja rēķins tiek apstiprināts un izlaists maksājumam.

## <a name="scenarios-for-use"></a>Scenāriji lietošanai

Piegādātāju rēķini programmā Project Operations var tikt izmantoti, lai atbalstītu divus atsevišķus scenārijus.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klienti izmanto pilnu apakšlīgumu pieredzi

Piegādātāju rēķinu lietošanas iespējas nodrošina veidu, kā pārbaudīt un saskaņot laika ierakstus, materiālu lietojumu un izdevumu ierakstus, kas attiecas uz apakšlīguma komponentiem, ar piegādātāja rēķina rindām. Šo procesu var izmantot, lai pārbaudītu piegādātāja rēķina rindu precizitāti. Pēc pārbaudes procesa pabeigšanas un piegādātāja rēķina apstiprināšanas programma apgriež faktiskos datus, kas tika ierakstīti apstiprinātajos laika, izdevumu un materiālu lietojuma žurnālos, un izveido jaunas faktiskās izmaksas, izmantojot piegādātāja rēķina rindas.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klienti neizmanto pilnu apakšlīgumu pieredzi, bet vēlas vienotu projektu izmaksu pārskatu programmā Project Operations

Ja izsekojat apakšlīguma procesu trešās puses sistēmā, varat ierakstīt izmaksas no šīs trešās puses sistēmas uz Project Operations, izveidojot piegādātāja rēķinus, kuriem nav atsauču uz apakšlīgumiem. Tādējādi projektu vadītājiem tiek nodrošināts viens, vienots visu konkrētā projekta izmaksu skats.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Piegādātāju rēķinu izveidošana programmā Project Operations

Piegādātāju rēķinus var izveidot divējādi:

- piegādātāju rēķinu saraksta lapā vai atsevišķa piegādātāja rēķina detalizētas informācijas lapā;
- apakšlīgumu saraksta lapā vai atsevišķa apakšlīguma detalizētas informācijas lapā.

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Izveide piegādātāju rēķinu saraksta lapas vai detalizētas informācijas lapā

1. Dodieties uz **Pirkšana** \> **Piegādātāju rēķini**.
2. Lai izveidotu jaunu piegādātāja rēķinu, piegādātāju rēķinu saraksta lapā vai atsevišķa piegādātāja rēķina detalizētas informācijas lapā atlasiet **Jauns**.

Šādi izveidoti piegādātāju rēķini var arī saturēt atsauci uz apakšlīgumu.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Izveide apakšlīgumu saraksta lapas vai detalizētas informācijas lapā

1. Dodieties uz **Pirkšana** \> **Apakšlīgumi**.
2. Atlasiet vienu vai vairākus apakšlīgumus.
3. Lai izveidotu jaunu piegādātāja rēķinu, apakšlīgumu saraksta lapā vai atsevišķa apakšlīguma detalizētas informācijas lapā atlasiet **Izveidot piegādātāja rēķinu**.

Katram atlasītajam apakšlīgumam tiek izveidots jauns piegādātāja rēķins ar statusu **Melnraksts**.

Šādi izveidoti piegādātāju rēķini vienmēr satur atsauci uz apakšlīgumu piegādātāja rēķina galvenē. Katra apakšlīguma rinda, kurā ir laika un materiālu norēķinu metode, izraisa rindas izveidi piegādātāja rēķinā. Katra apakšlīguma rinda, kam ir fiksētas cenas norēķinu metode, izraisa rindas izveidošanu piegādātāja rēķinā katram apakšlīguma rindas atskaites punktam, kam ir statuss **Gatavs rēķina izrakstīšanai**.

Tālāk norādītie lauki un saistītie ieraksti tiks kopēti no apakšlīguma uz piegādātāja rēķina galveni.

- Piegādātājs.
- Saistītie cenrāži tiek kopēti piegādātāja rēķinā kā cenrāži.
- Valūta.
- Līgumslēdzēja vienība.
- Maksājumu nosacījumi.

Laika un materiālu apakšlīguma rindām tālāk norādītie lauki un saistītie ieraksti tiks kopēti no apakšlīguma rindas uz piegādātāja rēķina rindu.

- Apakšlīgums un apakšlīguma rindas atsauces
- Transakciju klase
- Loma
- Transakciju kategorija
- Produktu lauki
- Project
- Uzdevums
- Rezervējamais resurss

Fiksētas cenas apakšlīguma rindām tālāk norādītie lauki tiks kopēti no apakšlīguma rindas un apakšlīguma rindas atskaites punkta uz piegādātāja rēķina rindu.

- Apakšlīgums un apakšlīguma rindas atsauces.
- Transakcijas klase. Pēc noklusējuma šī vērtība ir **Atskaites punkts**.
- Atskaites punkta nosaukums un summa tiks kopēta no saistītā apakšlīguma rindas atskaites punkta.
- Lietotājs piegādātāja rēķina rindā varēs atlasīt projektu un uzdevumu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
