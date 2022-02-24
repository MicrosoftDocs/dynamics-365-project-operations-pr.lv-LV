---
title: Ieņēmumu novērtējumu pārvaldība
description: Šajā tēmā ir sniegta informācija par to, kā darboties ar ieņēmumu novērtējumiem projektā.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531489"
---
# <a name="manage-revenue-estimates"></a>Ieņēmumu novērtējumu pārvaldība

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Varat izveidot, aprēķināt, grāmatot, atsaukt vai izslēgt ieņēmumu novērtējumus. To var izdarīt manuāli vai izmantojot periodisku procesu. Šajā tēmā ir sniegta informācija par to, kā darboties ar ieņēmumu novērtējumiem projektā.

### <a name="manage-revenue-estimates-manually"></a>Ieņēmumu novērtējumu pārvaldība manuāli

Fiksētas cenas ieņēmumu novērtējumu projektā vai lapā **Novērtējuma pieprasījums** (**Projektu pārvaldība un uzskaite** > **Atskaites un pieprasījumi** > **Novērtējumu pieprasījumi un atskaites**) atlasiet **Novērtējumi**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Ieņēmumu novērtējumu pārvaldība, izmantojot periodisku procesu

Pārejiet uz **Projektu pārvaldība un uzskaite** > **Periodiski** > **Novērtējumi** un atlasiet atbilstošo procesu.

## <a name="create-a-revenue-estimate"></a>Ieņēmumu novērtējuma izveide

Lai izveidotu ieņēmumu novērtējumu, izpildiet tālāk norādītās darbības. 

1. Pārejiet uz **Projektu pārvaldība un uzskaite** > **Periodiski** > **Novērtējumi**.
2. Atlasiet **Jauns**. Lapā **Novērtējuma izveide** atlasiet tālāk norādītos parametrus.

   - **Perioda kods**: šis kods nosaka, cik bieži tiek grāmatoti novērtējumi.
   - **Novērtējuma datums**: datums, kad novērtējums tiek apstrādāts.
   - **Nepārtraukti**: atzīmējiet šo izvēles rūtiņu, lai izveidotu novērtējumus tikai tad, ja novērtējumi tika grāmatoti iepriekšējā periodā vai ja novērtējums ir pirmais izveidotais novērtējums. Ja tā nav atlasīta, novērtējumi tiek izveidoti pat tad, ja novērtējumi nav grāmatoti iepriekšējā periodā.
   - **Pabeigšanas izmaksu metode**: definējiet, kā novērtēt atlikušo projekta darbu. Papildinformāciju skatiet tēmā [Pabeigšanas izmaksu metode](cost-complete-methods.md).
   - **Pabeigšanas metode**: atlasiet pabeigšanas metodi no tālāk norādītajām opcijām.
     - **Automātiski**: pabeigšanas vērtība procentos tiek aprēķināta automātiski un ir balstīta uz aprēķinā iekļautajām izmaksu rindām. Izmaksu veidne definē iekļautās izmaksu rindas.
     - **Manuāli**: pabeigšanas vērtība procentos ir vienāda ar pēdējā novērtējuma pabeigšanas procentuālo vērtību. Kad novērtējums ir izveidots, lapā **Novērtējumi** varat mainīt **Manuālais aprēķins**.
     - **No izmaksu veidnes**: automātisko un manuālo metožu kombinācija. Šī opcija tiek iestatīta automātiski vai manuāli atkarībā no noklusējuma vērtības izmaksu veidnē.
   - **Prognozes modelis**: atlasiet prognozes modeli novērtējumam.
   - **Drukāt novērtējumu sarakstu**: izveidojiet un parādiet novērtējumu sarakstu. Sarakstā ir pašreizējās funkcijas statuss. Atskaitē var drukāt visus brīdinājumus par novērtējumu. Tālāk uzskaitītie nosacījumi izraisa brīdinājumu parādīšanu novērtējumu sarakstā:
     - Pabeigšanas procentuālā vērtība pārsniedz 100 procentus.
     - Pabeigšanas procentuālā vērtība ir mazāka nekā nulle procenti.
     - Negatīva summa kolonnā **Pabeigt**.
     - Novērtējums bez atbilstošas līguma summas.
     - Novērtējums bez pievienota izmaksu novērtējuma.
   - **Rādīt informācijas žurnālu**: atlasiet šo opciju, lai saņemtu ziņojumu, kurā ir informācija par novērtētajiem projektiem, kas tika apstrādāti, palaižot darbu.


## <a name="post-wip-or-accruals"></a>NP vai uzkrājumu grāmatošana

Pēc tam, kad novērtējumi ir novērtēti, tie tiek saglabāti, samazināti vai palielināti. Pēc tam varat grāmatot NP, strādājot ar novērtēšanas principu **Pabeigts līgums**, vai grāmatot uzkrājumus, strādājot ar novērtēšanas principu **Pabeigšanas procentuālā vērtība**.
  
Novērtējuma perioda statuss mainās no **Izveidots** uz **Iegrāmatots**.

## <a name="reverse-wip-or-accruals"></a>NP vai uzkrājumu atsaukšana

Izmantojiet atsaukšanas opciju, lai kreditētu jau iegrāmatotu NP vai uzkrājumus, un pēc tam izveidojiet perioda novērtējumus.

> [!NOTE]
> Lai atsauktu periodu, kas atrodas starp citiem periodiem, atsauciet nepieciešamos novērtējuma periodus un pēc tam grāmatojiet tos atkārtoti. Visi nākamie periodi ir atkarīgi no iepriekšējo periodu novērtējumiem, tāpēc neizlaidiet nevienu periodu.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Novērtējuma projekta atcelšana un projekta pabeigšana

Pēdējais solis novērtēšanas procesā ir likvidēt novērtējuma projektu un pārtraukt fiksētās cenas projektu, kad pabeigšanas procentuālā vērtība sasniedz 100 procentus.

Izpildot izslēgšanu, notiek tālāk norādītie procesi.

- Fiksētas cenas projektam ar pabeigtu līgumu NP vērtības tiek dzēstas no bilances kontiem un grāmatotas peļņas un zaudējumu kontos.
- Fiksētas cenas projektam ar pilnu pabeigšanas procentuālo vērtību no peļņas un zaudējumu kontiem tiek noņemti uzkrājumi.

Novērtējuma statuss tiek nomainīts uz **Izslēgts**.

> [!NOTE]
> Īpašos gadījumos procentuālā vērtība var pārsniegt 100 procentus. Šādā gadījumā samaziniet pabeigšanas procentuālo vērtību, izmantojot metodi **Iestatīt pabeigšanas izmaksas uz nulli**, lai sasniegtu 100 procentus.

## <a name="reverse-elimination"></a>Izslēgšanas atsaukšana

1. Pārejiet uz **Projektu pārvaldība un uzskaite** > **Periodiski** > **Novērtējumi** > **Atsaukt izslēgšanu**. 
2. Darbību rūts cilnē **Process**, grupā **Uzturēt** atlasiet **Novērtējums**. 
3. Atlasiet **Atsaukt izslēgšanu**.

Izmantojiet šo lapu, lai atsauktu visas izslēgšanas ar konkrētu novērtējuma datumu un novērtējuma statusu **Izslēgts**. Transakcijas statuss tiek mainīts pēc atbilstošo lauku atlasīšanas.

Tas arī automātiski maina projekta statusu uz **Procesā**, ja projekta posms ir iestatīts kā pabeigts. Projekta perioda novērtējuma statuss tiek mainīts atpakaļ uz **Publicēts**.
