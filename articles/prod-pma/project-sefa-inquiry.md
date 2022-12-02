---
title: Federālo apbalvojumu izmeklēšanas izdevumu plāns
description: Šajā rakstā ir sniegta informācija par Federālās balvas izmeklēšanas izdevumu plānu.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 00f9e97b9a6b3e8fe5e9cf9143e670612869b84c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916665"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Federālo apbalvojumu izmeklēšanas izdevumu plāns

[!include [banner](../includes/banner.md)]

Saskaņā ar Office pārvaldes un budžeta apkārtrakstu A-133 uz aģentūrām, kas saņem federālos līdzekļus, attiecas audita prasības, kuras arī sauc par atsevišķajiem auditiem. Audita process tiek izmantots, lai regulāri ziņotu par federālo dotāciju ieņēmumiem un izdevumiem. Atsevišķā audita atskaites daļā ir iekļauts federālo apbalvojumu izdevumu plāns (SEFA).

Federālās balvas izmeklēšanas izdevumu plāns ietver Federālās iekšzemes palīdzības katalogu (CFDA) nosaukumu un numuru, dotācijas numuru, dotācijas gadu, federālās aģentūras nosaukumu, kas nodrošina līdzekļus, un caurlaides uzņēmuma nosaukumu. Izdevumi attiecas uz noteiktu periodu. Parasti šis periods ir tāds pats kā finanšu pārskata periods, kas ir finanšu gads.

Izdevumos ir iekļautas dotācijas, kurām atlasītajā datumu diapazonā ir projekcijas datumi. Izdevumu ailē **Dotētāja aģentūra** ir norādīts dotācijas klients vai caurlaides dotācijai — dotācijas aģentūra. Attiecībā uz tiešo piešķīrumu ailē **Caurlaides aģentūra** tiek parādīts dotācijas klients. Ja dotācija nav caurlaides dotācija, aile **Caurlaides aģentūra** ir tukša.

## <a name="set-up-the-cfda-clusters"></a>CFDA klasteru iestatīšana

Ir jāiestata CFDA klasteri, kurus var saistīt ar CFDA numuriem Federālās apbalvošanas izrakstu plānā.

1. Dodieties uz **Projekta pārvaldība un uzskaite \> Iestatījumi \> Dotācijas \> Federālās iekšzemes palīdzības klasteru katalogs**.
2. Lai izveidotu CFDA klasteri, atlasiet **Jauns**.
3. Ievadiet klastera nosaukumu.
4. Lai saglabātu izmaiņas, atlasiet **Saglabāt**.

## <a name="set-up-cfda-numbers"></a>CFDA numuru iestatīšana

Ir jāiestata CFDA numuri, kurus var pievienot dotācijām un iekļaut Federālo apbalvojumu izmeklēšanas izdevumu plānā.

1. Dodieties uz **Projekta pārvaldība un uzskaite \> Iestatījumi \> Dotācijas \> Federālās iekšzemes palīdzības numuru katalogs**.
2. Lai izveidotu CFDA numuru, atlasiet **Jauns**.
3. Ailē **Numurs** ievadiet CFDA numuru.
4. Nospiediet **tabulēšanas** taustiņu.
5. Ailē **Apraksts** ievadiet CFDA nosaukumu.
6. Nospiediet **tabulēšanas** taustiņu.
7. Neobligāti: laukā **Programmas klasteris** pievienojiet atbilstošo CFDA klasteri.
8. Lai saglabātu izmaiņas, atlasiet **Saglabāt**.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Dotāciju izveide, lai ziņotu par Federālo apbalvojumu izmeklēšanas izdevumu plānu

1. Dodieties uz **Projekta pārvaldība un uzskaite \> Dotācijas \> Dotācijas** un atlasiet esošu dotāciju.
2. Kopsavilkuma cilnē **Iestatīšana**, kas atrodas laukā **Federālās iekšzemes palīdzības numuru katalogs**, piešķiriet CFDA numuru. CFDA numurs dotācijā nosaka CFDA klasteri atskaišu izveidei.
3. Kopsavilkuma cilnē **Kontaktpersonu informācija** ievadiet dotētāja informāciju, veicot šādas darbības:

    1. Laukā **Dotācijas klients** ievadiet klientu, kas ir atbildīgs par dotāciju. Esošas dotācijas gadījumā šī informācija var jau būt ievadīta.
    2. Norādiet, vai dotāciju klients ir finansētājs. Ja dotāciju klients ir finansētājs, atstājiet izvēles rūtiņu **Caurlaide** tukšu. Ja cits klients ir finansētājs un dotāciju klients ir atbildīgs par izmaksām un naudas izsekošanu, atzīmējiet izvēles rūtiņu **Caurlaide**.

4. Ja iepriekšējā darbībā atzīmējāt izvēles rūtiņu **Caurlaide**, laukā **Dotētāja aģentūra** ievadiet klientu, kas nodrošināja šo dotāciju. Dotētāja aģentūra un dotācijas klients nevar būt viens un tas pats klients.

Šeit ir caurlaides dotācijas piemērs:

Federālā valdība finansēja infrastruktūras projektu valstij. Federālā valdība deva naudu valstij tērēt. Šajā gadījumā federālā valdība ir dotētāja aģentūra, un valsts ir dotācijas klients.

> [!NOTE] 
> Pirmoreiz ieslēdzot līdzekli, sākotnējie CFDA numuri tiks ievadīti, izmantojot piešķīrumos esošos numurus.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Neiekļaut dotācijas no SEFA atskaišu izveides, pamatojoties uz dotāciju tipu

1. Dodieties uz **Projekta pārvaldība un uzskaite \> Iestatījumi \> Dotācijas \> Dotācijas tipi**.
2. Kopsavilkuma cilnē **Noklusējuma informācija** atzīmējiet izvēles rūtiņu **Neiekļaut federālo apbalvojumu izdevumu plānā**.
3. Lai saglabātu izmaiņas, atlasiet **Saglabāt**.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Federālo apbalvojumu izmeklēšanas izdevumu plāna palaišana

1. Dodieties uz **Projekta pārvaldība un uzskaite \> Pieprasījumi un atskaites \> Dotācijas pieprasījums \> Federālo apbalvojumu izdevumu plāns**.
2. Sadaļā **Parametri** veiciet tālāk norādītās darbības.

    1. Laukā **Datumu intervāls** atlasiet datumu intervāla kodu. Vai arī laukos **Sākuma datums** un **Beigu datums** definējiet datuma intervālu.
    2. Neobligāti: lai izmeklēšanā kā ieņēmumus iekļautu tikai darījumus ar rēķinu, iestatiet opciju **Iekļaut tikai rēķinu ieņēmumus** uz **Jā**.

## <a name="columns"></a>Kolonnas

Federālo apbalvojumu izmeklēšanas izmaksu plānā ietver šādas kolonnas:

- Federālā iekšzemes atbalsta klastera kataloga nosaukums
- Dotētāja aģentūra
- Caurlaides aģentūra
- Dotācijas nosaukums
- Dotācijas ID
- Dotācijas programmas ID
- Federālā iekšzemes atbalsta katalogs
- Apliecinājumi
- Izdevumi


[!INCLUDE[footer-include](../includes/footer-banner.md)]