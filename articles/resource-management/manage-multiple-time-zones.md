---
title: Laika joslu pārvaldība
description: Izveidojot projektu, tā laika josla ir pamatota uz laika joslu, kas definēta pielietotajā darba stundu veidnē.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997745"
---
# <a name="manage-time-zones"></a>Laika joslu pārvaldība

_**Attiecas uz:** Project Operations resursu/ne krājumu scenārijiem, Lite izvietošanu —pro formas rēķinu izrakstīšanai_


## <a name="projects"></a>Projekti

Izveidojot projektu, laika josla ir pamatota uz laika joslu, kas definēta pielietotajā darba stundu veidnē. Veidlapā **Projekts** datumi vienmēr ir relatīvi attiecībā pret tā lietotāja laika joslu, kas ir pieteicies katrā cilnē, izņemot cilnē **Uzdevums**. Skatot darba sadalījuma struktūru, datumi vienmēr tiek rādīti projekta laika joslā.

## <a name="tasks"></a>Uzdevumi

Izveidojot uzdevumu, sākuma laiks, beigu laiks un stundu skaits dienā tiek kontrolētas pēc projekta darba laika. Piemēram, ja uzdevums ir izveidots projektā, kura laika zona ir -8 PST un kurā darba laiks ir no 9.00 līdz 17.00 no pirmdienas līdz piektdienai, jebkurš uzdevums, kas izveidots bez piešķires, pakļaujas projekta kalendāra sākuma laikam un beigu laikam.

## <a name="manage-resources-with-time-zones"></a>Resursu pārvaldība ar laika zonām

Lai iegūtu precīzus un prognozējamus rezultātus, izmantojot opciju **Paplašināt rezervāciju**, ir jāizpilda divi galvenie priekšnosacījumi.  

- Lietotājam ir jākonfigurē savas ierīces laika josla tādējādi, lai tā atbilstu tai laika joslai, kas definēta sistēmas iestatījumos **Personalizēšanas iestatījumi**.
 
  ![Laika joslu iestatījumi operētājsistēmā Windows 10](media/reconcile-assignments-03.png)

  ![Laika joslu iestatījumi personalizēšanas iestatījumos](media/reconcile-assignments-04.png)
 
- Rezervējamam resursam ir jābūt vismaz vienai minūtei no darba laika, kas pārklājas ar kontūrām, kas tiek izmantotas pieprasītā paplašinājuma definēšanai. Piemēram, tālāk norādītie resursi ar darba laiku no plkst. 9.00 līdz 19.00. 

  ![Resursu kontūru salīdzinājums](media/reconcile-assignments-05.png)

Tālāk sniegtajā tabulā ir norādīts:

- Projekta kalendāra veidne
- Resurss A: šim resursam ir viens un tas pats kalendārs, un tas atrodas vienā laika joslā ar projektu. Rezervācijas sākuma laiks būs 9:00.
- Resurss B: šis resurss atrodas no projekta atšķirīgā laika joslā un darbu sāk plkst. 7.00 savā laika joslā. Tomēr rezervācijas tiks sāktas ar 9:00, jo tas ir visagrākais piešķiršanas kontūras sākuma laiks.
- Resursi C un D: resursi atrodas dažādās laika zonās, kas atšķiras gan no viena no otras, gan no projekta laika joslas, un resursu rezervācijas sākas ne agrāk kā to attiecīgie pieejamie sākuma laiki.

|Entītija  |Kalendārs  |
|-|-|
|Projekta kalendāra veidne   | ![projekta kalendārs](media/reconcile-assignments-06.png) |
|Resurss A  | ![Resursa A kalendārs](media/reconcile-assignments-06.png) |
|Resurss B  |  ![Resursa B kalendārs](media/reconcile-assignments-07.png) |
|Resurss C  |  ![Resursa C kalendārs](media/reconcile-assignments-08.png) |
|Resurss D  | ![Resursa D kalendārs](media/reconcile-assignments-09.png)  |
 
Pārejot uz skatu **Saskaņošana**, tiek parādītas resursu piešķires un tiem saistītie rezervāciju deficīti.

![Saskaņošanas skats pirms paplašinājuma](media/reconcile-assignments-10.png)

Pēc tam, kad katram resursam ir izmantota rezervācijas paplašināšanas funkcija, rezervēšana tiek sekmīgi paplašināta katram resursam, jo katra resursa darba laiks pārklājas ar deficīta kontūrām.

![Saskaņošanas skats pēc rezervācijas paplašinājuma](media/reconcile-assignments-11.png) 

Ievērojiet, ka detalizētākā informācijā par rezervējumiem redzamas rezervāciju sākuma laiku atšķirības. Rezervācijas sākas ne agrāk kā piešķires kontūras sākuma laiks un ne agrāk kā resursam pieejamais sākuma laiks.

![Jaunas resursa rezervācijas plānošanas panelī](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]