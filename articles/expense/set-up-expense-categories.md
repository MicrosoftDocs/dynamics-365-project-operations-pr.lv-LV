---
title: Izdevumu kategoriju iestatīšana
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt izdevumu kategorijas un kopīgotās kategorijas izdevumu atskaitēm.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896695"
---
# <a name="set-up-expense-categories"></a>Izdevumu kategoriju iestatīšana

_**Attiecas uz:** Project Operations scenārijiem, kas nav balstīti uz resursiem/krājumiem_

Kad darbinieki veido izdevumu atskaites, katram reģistrētajam izdevumu ierakstam ir jābūt saistītam ar izdevumu kategoriju. Izdevumu kategorijas ir atvasinātas no kopīgotām kategorijām, kuras var kopīgot organizācijas juridiskajās personās. Atkarībā no tā, kā ir definēta jūsu organizācija, šīs izdevumu kategorijas var arī kopīgot citos apgabalos. Pamatojoties uz jūsu organizācijas definīciju un ieviešanas darba grupas vadlīnijām, ir jānosaka, vai modulī Izdevumu pārvaldība lietotās kategorijas var izmantot tikai modulī Izmaksu pārvaldība vai arī tās var kopīgot citos apgabalos.

> [!NOTE]
> Šīs kategorijas var kopīgot projektu pārvaldībā un grāmatvedībā, kā arī izdevumu pārvaldībā vai arī projektu pārvaldībā un grāmatvedībā, kā arī ražošanā. Taču tās nevar kopīgot izdevumu pārvaldībā un ražošanā.

Lai varētu sākt iestatīšanas procesu, ir jāpieņem šādi lēmumi attiecībā uz katru izdevumu kategoriju:

- Kas ir izdevumu kategorija? Var būt tādas kategorijas kā lidojumi, viesnīca vai nobraukums.
- Vai izdevumu kategoriju var izmantot arī projektu pārvaldībā un grāmatvedībā? Ja var, jums ir jāpieņem arī šādi lēmumi:

    - Kuri izmaksu konti tiks izmantoti tālāk norādītajiem izdevumiem?

        - izdevumi
        - Algu sadalījums
        - WIP-izmaksu vērtība
        - Izmaksas-elements
        - WIP-izmaksu vērtība-elements
        - Uzkrātie zaudējumi
        - WIP-uzkrātie zaudējumi

    - Kuri ieņēmumu konti tiks izmantoti tālāk norādītajiem ieņēmumu avotiem?

        - Ieņēmumi, par ko izrakstīts rēķins
        - Uzkrāto ieņēmumu-pārdošanas vērtība
        - WIP-pārdošanas vērtība
        - Uzkrātie ieņēmumi-ražošana
        - WIP-ražošana
        - Uzkrātie ieņēmumi-peļņa
        - WIP-peļņa
        - Uzkrātie ieņēmumi-abonēšana
        - WIP-abonēšana

- Kāds ir izdevumu tips?
- Kāda ir izdevumu kategorijas noklusējuma maksāšanas metode?
- Vai izdevumu kategorijas izdevumi ir jāuzskaita?
- Kas ir izdevumu kategorijas galvenais noklusējuma konts?
- Kas ir izdevumu kategorijas noklusējuma krājumu PVN grupa?
- Vai izdevumu kategorijai ir atļautas papildu maksāšanas metodes? Ja ir atļautas, kādas?
- Vai šajā izdevumu kategorijā ir apakškategorijas? Ja ir apakškategorijas, jums ir jāpieņem arī šādi lēmumi:

    - Vai jebkura no apakškategorijām ir izslēgta no nodokļu atmaksas?
    - Kas ir apakškategoriju krājumu PVN grupa?
