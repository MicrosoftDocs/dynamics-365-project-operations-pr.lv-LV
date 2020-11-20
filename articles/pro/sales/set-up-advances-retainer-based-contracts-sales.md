---
title: Avansi un līgumi, kuru pamatā ir saistības — Lite
description: Šajā tēmā ir sniegta informācija par līguma modeļiem un avansiem, kas balstīti uz honorāriem, risinājumā Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912b235af5e561349fdfb481e5f5b7c5514669c3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180876"
---
# <a name="advances-and-retainer-based-contracts---lite"></a>Avansi un līgumi, kuru pamatā ir saistības — Lite


_**Attiecas uz:** Lite izvietošana — pāreja uz proforma rēķina izrakstīšanu_

Dynamics 365 Project Operations atbalsta uz honorāriem balstītus līgumus. Uz honorāru balstīts līgums ir vienādi sadalītu maksājumu kopums, par ko klientam tiks izrakstīts rēķins par visu projekta laiku. Šāda tipa līgumu parasti izmanto laika un materiālu vai patēriņa norēķinu modeļiem, kuros klientam ir jāpiešķir prognozējams rēķins un maksājumu plāns. Faktiskie ieņēmumi, kas iegūti katrā periodā, tiek salīdzināti ar maksājumiem, kas saņemti no klienta perioda sākumā. Atbilstoši laika un materiālu norēķinu modeļa koncepcijai katrā periodā uzkrātās ieņēmumu vērtības var atšķirties atkarībā no izmaksām. Ja uzkrātie ieņēmumi pārsniedz summu, kas saņemta perioda sākumā, projekta piegādes uzņēmums var:

- Izrakstīt klientam rēķinu par pārpalikumu 
- Atlikt ieņēmumu saskaņošanu ar nākamo rēķinu izrakstīšanas periodu un veikt vienu galīgo rēķinu projekta beigās attiecībā uz atlikušajiem nesaskaņotajiem ieņēmumiem

Galvenā atšķirība starp uz honorāru balstītu līgumslēgšanas modeli un fiksētas cenas līguma modeli risinājumā Project Operations ir tāda, ka fiksētas cenas līguma modelī rēķina summa nav saistīta vai ir saistīta ar izmaksām, kas radušās. Rēķinu izrakstīšana tiek veikta, pamatojoties uz atskaites punktu, kas atbilst izmaksām, kas radušās konkrētajā periodā. Uz honorāru balstītu līgumu ieņēmumi, kuriem var izrakstīt rēķinu, tiek reģistrēti, par pamatu izmantojot norēķinu metodi līguma rindā. Ja rēķina metode ir laiks un materiāli, rēķinos iekļautie ieņēmumi ir saistīti ar izmaksām, kas radušās katrā noteiktā periodā, un var mainīties atkarībā no perioda. Tomēr klientam tiek izrakstīts rēķins tikai par summu periodiskajā honorārā. Sistēma izmanto citu rēķinu perioda beigās, lai saskaņotu rēķinā norādītos ieņēmumus, kas ir reģistrēti perioda laikā, par to summu, par kādu klientam izrakstīts rēķins, atsākot perioda sākumu.

Šīs metodes priekšrocība ir tāda, ka klienta izmaksas kļūst prognozējamas plānotajā laikā, atšķirībā no tipiskā laika un materiālu modeļa. Organizācijai, kas piedāvā projektu, ir arī zināmas iespējas segt risku, kas saistīts ar izmaksu atgūšanu sakarā ar jebkādu darbības jomas palielināšanos, ko fiksētas cenas modelis tiem nebūtu ļāvis.

Papildus periodiskam uz honorāru balstītam plānam risinājums Project Operations var ierakstīt klientam vienreizēju avansu un saskaņot to ar dažādiem projekta izmaksu komponentiem.

Project Operations honorārs nav pieejams lietošanai, kamēr par to nav izrakstīts rēķins klientam. Tas ir norādīts attiecībā uz avansu un honorāru apakšrežģī minētajiem laukiem.

| Lauks | Apraksts | Lejupstraumes ietekme |
| --- | --- | --- |
| Pieejamā summa | Summa, kas ir pieejama izmantošanai honorāra vai avansa ierakstam. | Līdz brīdim, kad par avansu vai honorāru ir izrakstīts rēķins, tas nav pieejams izmantošanai, kas nozīmē, ka pieejamā summa būs nulle. |
| Izmantotā summa | Summa, kas jau tiek izmantota honorāra vai avansa ierakstam. | Avansu vai honorāru var daļēji piesaistīt rēķinam ar faktiskajām izmaksām, kurām būs kāda daļa, kas iezīmēta kā jau izmantota vai patērēta. Pārējā avansa vai honorāru summa ir pieejama, lai nākotnē saskaņotu rēķinu ar faktiskajām izmaksām. |
