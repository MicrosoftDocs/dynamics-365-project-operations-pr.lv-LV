---
title: Projekta līgumu projekta cenu sarakstu pārvaldīšana
description: Šajā tēmā ir sniegta informācija par projekta cenu sarakstu pārvaldību projekta līgumos.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278607"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Projekta līgumu projekta cenu sarakstu pārvaldīšana

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_

Projekta līgumi ar Dynamics 365 Project Operations ir paredzēti, lai atbalstītu vairākus aktuālus pārdošanas cenrāžus līgumā. Project Operations ir jauna saistīta entītija, ko sauc par **projekta cenrāžiem**. Šai entītijai ir relācija viens pret daudziem ar projekta līgumu.

Projekta cenrāžus izmanto, lai noteiktu projekta laika un izdevumu darījumu cenas. Ja līgumam ir viens vai vairāki projekta cenrāži, šie cenrāži tiek lietoti, lai noteiktu laika un izdevumu aplēses un faktiskās vērtības projektiem, kas saistīti ar šo līgumu, izmantojot līguma rindu.

Ja projekta līgumam nav projekta cenrāža, tiek parādīts brīdinājuma ziņojums par to, ka nav projekta cenrāžu, un jūsu aprēķiniem, faktiskajam projekta darbam un izdevumiem netiks noteiktas cenas. Pārdošanas vērtībām netiks noteikta cena.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Projekta līgumā paredzētā projekta cenu saraksta saistīšana vai atsaistīšana

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Izveidojiet vai saistiet noteiktu cenrādi, lai noteiktu uz projektiem balstītu darbu un izdevumus

1. Projekta līgumā atlasiet cilni **Projekta cenrāži**.
2. Apakšrežģī atlasiet **+ Pievienot jaunu projekta cenrādi**.
3. Izmantojot **Ātrās izveides** slīdni, atlasiet cenrādi. 

  Nolaižamajā sarakstā ir parādīti visi cenrāži, kam kontekstā ir iestatīta **Pārdošana**, ja cenrāža valūta atbilst līguma valūtai.
  
4. Ievadiet projekta cenrāža sasaisti aprakstu, atlasiet **Saglabāt** un pēc tam aizveriet **Ātrās izveides** slīdni.

   Tiek izveidota projekta cenrāža sasaiste.
   
5. Atkārtojiet 1.–4. darbību, lai projekta līgumam piesaistītu vairāk nekā vienu projekta cenrādi. Veidojiet vairākus projekta cenrāžus tikai tad, ja katram no saistītajam projekta cenrāžiem ir atšķirīgi darbības datumi.

> [!NOTE]
> Project Operations neatbalsta projekta cenrāža darbības datumu pārklāšanos. Ja darbībai ar noteiktu datumu ir vairāki projekta cenrāži, šī transakcijas cena pēc noklusējuma tiks ņemta kā nulle.

### <a name="remove-a-project-price-list-association"></a>Projekta cenrāža saistību noņemšana

- Atlasiet projekta cenrādi un pēc tam apakšrežģī atlasiet **Dzēst līguma projekta cenrādi**. 

  Cenrādis tiek noņemts no līguma projektu cenrāžiem. Pats cenrādis netiks izdzēsts. Tiks izdzēsts tikai saistījums ar līgumu.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Projekta cenrāža automātiskā noklusējuma iestatīšana līgumā

Projekta cenrādi var iestatīt kā projekta līguma noklusējuma sarakstu. Šis iestatījums var palīdzēt nodrošināt, ka visi jūsu organizācijas līgumi vienmēr tiek sākti ar attiecīgā cenu perioda standarta cenrādi.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Organizācijas noklusējuma projektu cenrāžu iestatīšana

1. Atveriet sadaļu **Iestatījumi** > **Vispārīgi** un pēc tam atlasiet vienumu **Parametri**.
2. Lai atvērtu ierakstu, saraksta lapā **Aktīvie parametri** atlasiet ierakstu un veiciet dubultklikšķi uz tā. Veicot dubultklikšķi, pārliecinieties, ka neklikšķināt uz lauka vērtības, kas ir hipersaite. 
3. Lapā **Aktīvie parametri** atlasiet cilni **Cenrādis**. Apakšrežģī redzams noklusējuma cenrāžu saraksts. Šis ir standarta izmaksu un pārdošanas cenrāžu saraksts. Ja **Pārdošanas** cenrādis šeit ir saistīts ar katru valūtu, kurā pārdodat, tiek nodrošināts, ka pārdošanas cenrādis ir noklusējuma cenrādis katram līgumam, ko izveidojat klientiem, kas veic transakcijas šajā valūtā.

### <a name="set-up-a-customer-specific-project-price-list"></a>Klientam noteikta projekta cenrāža iestatīšana

Varat arī iestatīt klientam noteiktus projekta cenrāžus, kad esat pārrunājis ar klientiem vispārējo cenu noteikšanas līgumu.

1. Dodieties uz **Pārdošana** > **Klienti**.
2. Aktīvo uzņēmumu sarakstā atlasiet klientu, kuram ir īpašs cenrādis.
3. Atlasiet klienta ierakstu, lai to atvērtu, un pēc tam atlasiet cilni **Projekta cenrāži**. Apakšrežģis rāda šim klientam noteikto projekta cenrāžu sarakstu. 
4. Šeit varat izveidot jaunu cenrāža saistību, lai šim klientam būtu noteikts projekta cenrādis.

## <a name="custom-pricing-on-a-project-contract"></a>Cenas pielāgošana projekta līgumam

Kad ir izveidoti organizācijas un klientiem noteikti noklusējuma projektu cenrāži, jūsu projekta līgumi tiek automātiski izveidoti ar šīm projekta cenrāžu saistībām. Tomēr projekta līguma cenrāži, kas attiecas uz projekta līgumu, vienmēr tiek kopēti, norādot tiem pievienoto datumu un līguma nosaukumu. Uzņēmums un projektu vadītāji pēc tam šajās kopijās var sākt labot cenas. Šīs mainītās cenas ir piemērojamas tikai šim projekta līgumam.


[!INCLUDE[footer-include](../includes/footer-banner.md)]