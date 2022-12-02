---
title: Izmaksu specifikācija
description: Šajā rakstā izskaidrots, kā detalizēti uzskaitīt izdevumus, izmantojot atjaunināto izdevumu darbvietu.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920943"
---
# <a name="expense-itemization"></a>Izmaksu specifikācija

[!include [banner](../includes/banner.md)]

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Organizācijas bieži vien pieprasa darbiniekiem sniegt detalizētu izdevumu, kas radušies ceļojuma laikā, izklāstu. Piemēram, viesnīcas rēķinā var būt vairākas atsevišķas rindas cenai par viesnīcas numuru, nodokļiem, autostāvvietu un citiem dažādiem izdevumiem, kas radušies katras uzturēšanās dienas laikā. Vai arī var būt nepieciešams sniegt detalizētāku izklāstu attiecībā uz brokastīm, pusdienām vai vakariņām. Lai kādas būtu organizācijas vajadzības, ikvienu izdevumu kategoriju var iestatīt tā, lai atspoguļotu apakškategorijas vai rindas vienumus, kas veido izdevumus. Lai gan detalizācija vienmēr ir tikusi atbalstīta sadaļā **Izdevumu pārvaldība**, darbvieta **Atjauninātie izdevumi** nodrošina efektīvāku detalizāciju, ja ir iespējots līdzeklis **Iespēja ātri uzskaitīt periodiskos izdevumus**.  

## <a name="enable-quick-itemization"></a>Ātrās detalizācijas iespējošana 

Varat izmantot līdzekli **Iespēja ātri uzskaitīt periodiskos izdevumus**, lai ātri un detalizēti uzskaitītu periodiskos izdevumus, vienlaikus novēršot vajadzību katru reizi ievadīt ikdienas izdevumus par uzturēšanas ilgumu. Lai iespējotu ātro uzskaiti, izpildiet tālāk norādītās darbības.

1. Pārejiet uz darbvietu **Līdzekļu pārvaldība** un līdzekļu sarakstā atrodiet un atlasiet **Jauna veida izdevumu atskaites**. 
2. Atlasiet **Iespējot tagad**. 
3. Līdzekļu sarakstā atrodiet un atlasiet **Iespēja ātri uzskaitīt periodiskos izdevumus**.
4. Atlasiet **Iespējot tagad**. 

## <a name="itemization-grid"></a>Uzskaites režģis 

Ja izmaksu kategorijai ir apakškategorijas vai dažādi komponenti, kas veido šos izdevumus, to var detalizēti uzskaitīt pa daļām. Lai detalizēti uzskaitītu izdevumus, atlasiet izdevumu rindu izdevumu atskaitē un rūtī **Izdevumu detalizētā informācija** atlasiet **Darbības** > **Uzskaitīt**. Slīdnī **Detalizācija** tiek atklāts režģis ar laukiem. Nākamajā tabulā ir sniegts katra lauka piemērs režģī un veids, kā lauks tiek atveidots izdevumu atskaitē. 

|     Kolonna          |     Apraksts                                                                                  |     Piemērs              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Apakškategorija    |     Apakškategoriju saraksts, kas konfigurēts izdevumu kategorijas tipam **Viesnīca**.             |     Viesnīcas numura dienas likme      |
|     Sākuma datums     |     Datums, kurā pirmo reizi radās izdevumu elements.                                           |     13.09.2021.           |
|     Dienas likme     |     Summa, kas rodas šim izdevumu elementam.                                                    |     Vairāk nekā 200                  |
|     Daudzums       |     Daudzums, cik reižu maksa tiek atkārtota nepārtraukta perioda laikā.                       |     3                    |

![Detalizēti uzskaitiet izdevumus.](media/Itemization%20screen%201.png)

Saglabājot detalizāciju, būs redzama atsevišķa detalizācijas rinda detalizācijas režģī norādītajam daudzumam. Katra rinda sākas režģī norādītajā datumā.

![Detalizēts pārskats.](media/Itemization%20screen%202.png)

