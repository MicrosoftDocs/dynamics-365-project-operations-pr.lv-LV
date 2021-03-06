---
title: Dienasnauda
description: Šajā tēmā ir sniegta informācija par dienasnaudas kārtulām, kas tiek izmantotas izdevumu pārvaldībā.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908366"
---
# <a name="per-diems"></a>Dienasnauda

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_


Dienasnauda ir pabalsts, ko maksā darba ņēmējam, kurš dodas komandējumā. Izdevumu pārvaldībā varat izveidot dienasnaudas kārtulas dažādām ceļošanas situācijām. Dienasnaudas likmes var būt atkarīgas no gada laika, ceļojuma galamērķa vai abiem. Kad izveidojat dienasnaudas kārtulu, varat norādīt, ka noteikta procentuālā dienasnaudas likme tiek ieturēta, ja darbinieks saņem bezmaksas maltītes vai pakalpojumus. Varat iestatīt arī minimālo un maksimālo stundu skaitu, kam var piemērot darba ņēmēja komandējuma dienasnaudas likmi.

## <a name="configuration"></a>Konfigurācija 

1. Lai pievienotu dienasnaudas atrašanās vietas, ejiet uz **Iestatīšana** > **Aprēķini un kodi** > **Dienasnaudas atrašanās vietas**.
2. Katrai no iepriekš pievienotajām atrašanās vietām atlasiet dienasnaudas likmi un valūtu, kas ir derīga starp noteiktu sākuma un beigu datumu viesnīcas, maltīšu vai citu izdevumu segšanai. Dienasnaudas likmes un valūtas tiek konfigurētas sadaļā **Iestatīšana** > **Aprēķini un kodi** > **Dienasnaudas**.
3. Lapā **Dienasnaudas atrašanās vieta** konfigurējiet dienasnaudas likmju līmeņus. Dienasnaudas likmju līmeņi ļauj definēt ikdienas pabalsta procentuālo sadalījumu attiecībā uz viesnīcas, maltīšu un citiem izdevumiem. 
4. Lai norādītu maltīšu procentuālo atskaitījumu brokastīm, pusdienām vai vakariņām, atjauniniet laukus lapā **Izdevumu pārvaldības parametri** cilnē **Dienasnauda**. 
    
## <a name="submit-expenses-using-per-diem"></a>Izdevumu iesniegšana, izmantojot dienasnaudu
Lai iesniegtu izdevumus, kas attiecas uz dienasnaudu, izmantojiet izdevumu kategoriju **Dienasnauda**, kad veidojat izdevumu atskaiti. Ievadiet **Dienasnauda no datuma**, **Dienasnauda līdz datumam** un **Dienasnaudas atrašanās vieta**. Summu aprēķina, par pamatu izmantojot dienasnaudas likmes izvēlētajai atrašanās vietai, un atskaitījums par maltītēm tiek aprēķināts, par pamatu izmantojot dienasnaudas likmju līmeņus.
